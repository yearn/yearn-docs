---
title: faq.yearn.finance
tags: "docs, faq, published"
---

# FAQ

## General

### Is it safe to invest money in Yearn?

- Please do your own research and decide for yourself.

### Is Yearn audited?

- Yes, you can find the list of audits [here](https://github.com/iearn-finance/audits).

## Feedback & Support

If you have questions about how to do anything, we can help you on:

- [Discord](http://discord.yearn.finance)
- [Telegram](https://t.me/yearnfinance)

But if you think something can be improved, or you found a bug, we want to squash it. Please post it here:

- [Github](https://github.com/iearn-finance) — create a new issue in the relevant repository.
- [Forum](https://gov.yearn.finance/c/feedback/) — post in the feedback category.

## Products

### yearn.finance

- [yearn.finance](https://yearn.finance/) hosts UIs for the **Vaults**, **Earn**, **Zap**, **APR**, and **Cover** products.

### Vaults

- [yearn.finance/vaults](https://yearn.finance/vaults)

#### What is a Vault?

- Vaults employ strategies to automate the best yield farming opportunities available.
- They were designed so that the community could work together to build new strategies to find the best yield.
- Andre explains [vaults](https://medium.com/iearn/yearn-finance-v2-af2c6a6a3613) and [delegated vaults](https://medium.com/iearn/delegated-vaults-explained-fa81f1c3fce2) in these two blog posts.
- Simply put vaults can do this:
  - Use any asset as liquidity.
  - Use liquidity as collateral and manage collateral at a safe level in order to avoid a default.
  - Borrow stablecoins.
  - Put the stablecoins to work on some farming.
  - Reinvest earned stablecoins.

#### Can't I just do all this myself though?

- Yes you could, but vaults help you save on gas, keep a good collateral/debt ratio to avoid defaults, and auto optimizes for the highest yielding stablecoin strategies, even while you are sleeping.

#### I see ROI on the vaults page. Is it the current one?

- No. This is the historical average for that vault. Current APY / returns are not shown as vaults are a beta product and being tested live.
- Various third party sites provide APY and other info, they are listed below in [Statistics](https://docs.yearn.finance/faq#statistics).

#### What are the risks?

- While the assets deposited can't decrease, the debt of the vault can increase. If a strategy does not manage to outperform the debt, then a portion of the asset will be impermanently locked. If a strategy later outperforms the debt again, the asset will again be available to withdraw. There are mechanisms in the vaults to prevent this but nothing is bulletproof.
- As of now, the Vaults have not been audited.
- Smart contract risk with any contracts that the vaults interact with.

#### What are the different yVaults?

**yLINK and yaLINK**

- **What's the difference between LINK and aLINK vaults?**
  - None in terms of returns. Deposited LINK will be deposited into Aave generating aLINK \(Aave interest bearing LINK\). So depositing directly into aLINK vault you are one step ahead in the process.
- **Why is the yield different for aLINK and LINK vaults?**
  - aLINK has a 0.5% insurance "fee" \(this is returned when it is outperformed\). LINK vault doesn't have this fee to avoid double dipping.

**yETH and yWETH**

- **What's the difference between WETH and ETH vaults?**
  - None in terms of returns. Deposited ETH it will be wrapped into WETH anyway. The WETH vault just makes it easier for other Ethereum protocols to interact with this vault.
- **How does ETH vault protect itself from liquidation?**
  - This vault reads ETH price directly from the Maker's OSM \(Oracle Security Model\), a system that reads Oracle price 1 hour in advance. This gives the vault 1 hour to pay the CDP debt before liquidation. Also, the vault keeps increasing collateralization by depositing profit on each harvest call.

**Other Vaults**

- v1 Money Market vaults, formerly called iEarn, can be found [here](https://yearn.finance/earn).
- Additional vaults can be found [here](https://yearn.finance/vaults).

#### If the current strategy for the yCRV vault is farming CRV does it just get added to my balance when I withdrawal?

- No. The vault will farm CRV then sell it on the market automatically. When you withdrawal you will get more yCRV.

#### Why isn't yCRV worth \$1, it's a stable coin right?

- No, yCRV is not worth \$1, and no it is NOT a stablecoin. You can think of yCRV as an index of yield bearing stablecoins \(yDAI+yUSDC+yUSDT+yTUSD\) that also generates yield \(trading fees from the Curve Y pool\) as well. Therefore the price of yCRV is non-decreasing.

#### If I unstake my yCRV from the yCRV vault, does that then revert it back to the Curve Y pool at Curve, or do I have to do something else like restake it there?

- When you withdraw your yCRV from the vault, you get back yCRV + plus interest accrued - fees, all in yCRV. Since it is the yCRV token you got back, it is already staked in Curve Y pool making stablecoin swap fees. No need to do anything else with Curve, unless you want to stake it [here](https://dao.curve.fi/minter/gauges) to generate CRV.

#### Why can’t we get a better APY for the YFI vault?

- You can’t get the same numbers for two completely different coins. The new sBTC is following the same strategy that the yCRV vault using curve liquidity pool. The obvious answer is that there aren’t many safe platforms accepting YFI as stake so there aren’t much valid strategies for the YFI vault right now.

#### I deposited into a vault, what will I get out when I withdrawal?

- You can only withdraw the crypto asset type that you put in.
- You will get the amount you originally put in, plus the yield you've earned, minus the fees.

#### What are the Fees?

- **0.5% fee** on funds withdrawn from active strategies
  - Each vault has some amount of the total funds idle and most of them active in the strategy. The idle funds are the difference between `vault holdings` and `strategy holdings`, you can see them on [feel the Yearn](https://feel-the-Yearn.app/).
  - When you withdraw, if your funds come from the idle funds, you won't be charged any withdrawal fee. If they come from the strategy, you will be charged the 0.5% fee.
- **5% fee** on additional yield
  - For community-made strategies, like the new yETH vault, currently 10% of this fee goes to the strategy creator. The other 90% goes to the treasury and is then distributed to governance.

#### Can you explain the 5% fee on additional yield?

- Formerly this was called a "5% fee on subsidized gas" which confused literally everyone except Andre. Technically it is not a performance fee — it's a fee on the some profit-generating transactions that incur high gas costs and are critical to the vault's internal functioning.
- Each vault has multiple levels. Here are two examples that show where this fee is taken when the `harvest()` function is called.
- yCRV Vault example:
  - Level 1: stablecoins earn interest in money markets \(compound, aave, dydx\)
  - Level 2: the level 1 tokens \(yDAI, yUSDC, yUSDT, and yTUSD\) are provided as liquidty to the yCRV pool to earn trading fees
  - Level 3: the strategy earns CRV token rewards which it recycles into yCRV—**this is the only level where the 5% fee is taken.**
- USDC Vault example:
  - Level 1: Interest for being lent out at Compound
  - Level 2: COMP liquidated to USDC
  - Level 3: The strategy earns DF tokens rewards from DForce that get harvested and sold for USDC—**this is the only level where the 5% fee is taken.**

#### Where do the fees go?

- They go to a dedicated treasury [contract](https://etherscan.io/address/0x93A62dA5a14C80f265DAbC077fCEE437B1a0Efde).
- From the treasury they stay up to the \$500k limit, over that amount they are redirected to the governance staking [contract](https://etherscan.io/address/0xBa37B002AbaFDd8E89a1995dA52740bbC013D992).

#### Did the fees always go there?

- No, when Yearn started they went directly to Andre's [address](https://etherscan.io/address/0x2d407ddb06311396fe14d4b49da5f0471447d45c).
- Then we handed off to the [multisig](https://etherscan.io/address/0xFEB4acf3df3cDEA7399794D0869ef76A6EfAff52) and fees went directly there.
- And before our current gov v2, staking rewards went [here](https://etherscan.io/address/0xb01419E74D8a2abb1bbAD82925b19c36C191A701)

#### Yield

- We plan to make a dashboard in the future that will clearly show your current APY of all the positions you have open. Currently for the Vaults as they are still in beta we are not showing the APY live, but it is post on [twitter](https://twitter.com/iearnfinance) around once a day. You can roughly estimate the yield you are getting by looking at what the [current strategy](https://feel-the-Yearn.vercel.app/) is farming and checking what its APY is.
- For example if yCRV vault is farming the CRV token, you can check what the yield is on [Curve's homepage](https://www.curve.fi/) for the Y pool

### Vault Strategies

#### What is a Vault Strategy?

- Yearn's vault strategies are modular smart contracts for each vault that tells it what assets to borrow, which assets to farm, and where it should sell the farmed assets.

#### What are the current strategies?

- You can view the current strategies implemented at [feel-the-Yearn](https://feel-the-Yearn.vercel.app/).
- In the future we plan to make a dashboard to make the strategies and APY easy to understand.

#### Who is in control of the strategies?

- Developers write them but the multi-sig, instructed by YFI voters, decides if they will be implemented or not.

#### How can I make a strategy?

- For now you can post your strategy on the forum in the strategy section. Detailing what it should buy/sell/farm and what the current APY is. There will be a template to help you get started.

#### What is the process for getting my strategy onto Yearn?

- Post it on the forum or get in touch with the developer team, if you get support for your idea and it ends up being implemented and approved, it will be used in the vaults and you can get paid for it.

#### When does a strategy changes and who changes it? Is it automatic?

- Strategy creators watch the markets and write strategies that they think are safe while giving the highest yield. They change them according to current yields on the market.

### Earn

- [yearn.finance/earn](https://yearn.finance/earn)

#### What is Earn?

- Earn is a yield aggregator for lending platforms that rebalances for highest yield during contract interaction.
- Deposit DAI, USDC, USDT, TUSD, or sUSD and it will auto lend to the highest lending rate on these platforms [Compound](https://compound.finance/), [Dydx](https://dydx.exchange/) or [Aave](https://app.aave.com/home) \(Ddex and Fulcrum are currently disabled\).
- Learn more in the [Yearn Docs](https://docs.yearn.finance/yearn.finance/yearn)

### Zap

- [yearn.finance/zap](https://yearn.finance/zap)

#### What is Zap?

- Zap allows users to convert supported tokens with just one contract interaction to reduce transaction costs.
- Zaps were made by DefiZap which is now [Zapper.fi](https://zapper.fi) as a type of all in one DeFi routing service.

#### Why use a Zap?

- "Zaps allow you get into a DeFi position in one transaction — it’s called zapping in." - [How to use Zaps guide](https://defitutorials.substack.com/p/how-to-use-defizap).
  - Note that this is an old article and [Zapper](https://zapper.fi) was formed as a result of DeFiSnap + DeFiZap coming together to create the ultimate hub for Decentralized Finance aka \#DeFi. So some of the stuff in the article above is out of date, but you can still use Zaps on Zapper.fi.

#### So what can I do with Zaps on Yearn?

- With a zap you can take your DAI, for example, and get yCRV with it in one transaction. Normally, to turn DAI into yCRV, you would have to go to earn, deposit DAI and receive yDAI, then go to [Curve.fi - Yearn pool](https://www.curve.fi/iearn/deposit) and deposit your yDAI and then you would get yCRV. This is a lot to do, so instead you can do it in one transaction!

#### That sounds awesome, what's the downside?

- Well, it does take a lot of gas and could be costly, even more so than doing it yourself manually, but if you have a big transaction and are in a rush it is a great method to get into a DeFi position or liquidity pool fast.

### yInsure / Cover

- [yinsure.finance](https://yinsure.finance/)

#### What's yInsure?

- yInsure, also known as **Cover**, is a pooled coverage system providing insurance against smart contract risk.
- It has no KYC requirement and is underwritten by Nexus Mutual.
- Learn more in this [article](https://medium.com/iearn/yinsure-finance-a-new-insurance-primitive-77d5d4217896).

### Products Currently in Research & Development

#### yTrade

- [ytrade.finance](https://ytrade.finance/)
- Leveraged stable coin trades \(testnet\).

#### yLiquidate

- [yliquidate.finance](https://yliquidate.finance/)
- 0 capital automated liquidations for Aave \(testnet\).

#### ySwap

- [yswap.exchange](https://yswap.exchange/)
- Single sided automated market maker \(testing in mainnet\).

#### yBorrow

- [yborrow.finance](https://yborrow.finance/)
- Credit delegation vaults for smart contract to smart contract lending \(testnet\).

## Communication

- [Forum](https://gov.yearn.finance)
  - A lot of real-time discussion happens on the telegram and discord but for a proposal to turn into a YIP \(Yearn Improvement Proposal\) it needs to be posted and discussed on the forum.
  - This is the main place token holders check for governance related issues.
- [Discord](http://discord.yearn.finance/)
  - Including non-English channels.
- [Telegram](https://t.me/yearnfinance) - Main Chat.
- [Telegram](https://t.me/yearncommunity) - Trading/Social/Fork Chat.
- Twitter
  - [yearn.finance](https://twitter.com/iearnfinance?s=20) - Official Twitter of Yearn
  - [Andre Cronje](https://twitter.com/AndreCronjeTech?s=20) - Yearn's founder and creator
  - [yLearnfinance](https://twitter.com/yLearnfinance) - Yearn Info
  - [Learn 2 Yearn](https://twitter.com/learn2Yearn) - Yearn Info

## Governance

### All about YIPs

#### What is a YIP? Why do they matter?

- A YIP or Yearn Improvement Proposal is how features are added to the Yearn ecosystem. Users start a proposal on the forum, discuss it and gauge the sentiment of if the proposal will be accepted. If a lot of users agree with it then it can be posted on-chain for everyone to vote on.

#### How many people need to vote to pass a YIP proposed on-chain?

- The quorum is 20%. Which means that 20% of the staked YFI needs to vote on a proposal for it to pass or else it will fail. Also, it has to have at least 50% of the votes for yes.
- You can post your proposal on-chain first but if people haven't talked about it, they probably won't vote for it.

#### How do I make a proposal?

- The default template for proposals can be found on [Github](https://github.com/iearn-finance/YIPS/blob/master/yip-X.md) + on the [forum](https://gov.yearn.finance) if you make a post under proposals or discussion it will auto-fill in the template as well.
- The process is roughly:
  1. forum discussion
  2. promote to YIP \(usually done by mods\), add YIP to github, put on chain
  3. announce

#### Who can make a proposal?

- Anyone can post a proposal both on the forum and on-chain.

### Voting

#### How do I vote?

- Stake your YFI and then you can cast your vote for YIPs that are on-chain on the voting [dashboard](https://ygov.finance/vote)

#### Can I vote if my YFI is in the YFI vault?

- No, your YFI must be staked in the governance [contract](https://ygov.finance/staking) in order to vote.

#### Where can I view the YIPs?

- You can view them on the voting [dashboard](https://ygov.finance/vote) if you login to your web3 account or at [yips.yearn.finance](https://yips.yearn.finance/all-yip).

#### Why should I stake? What is the APY \(Annual Percentage Yield\)?

- You should stake if you want to vote on YIPs and get rewards that are generated from the Yearn ecosystem. The APY for staking is currently not listed on the UI. You can ask on the chat what the rate is.

#### What do I have to do to get rewards with my YFI?

- All you need to do is stake YFI at [ygov.finance/stake](https://ygov.finance/stake) and you will get rewards if the treasury is at or above 500k usd. You can check the treasury address [here](https://zapper.fi/dashboard?address=0xFEB4acf3df3cDEA7399794D0869ef76A6EfAff52).
- Note that if you stake you get rewards \(as long as they are not going to the treasury\) but you can only claim them within 3 days of voting.

#### Does staking my YFI matter for voting?

- Yes. You have to stake your YFI at [ygov.finance/stake](https://ygov.finance/stake) in the v2 tab under Governance V2 to have your votes count. As of now, you can vote without staking, but you will waste your gas and it won't count so make sure you have staked first if you want to vote.

#### What if I want to take my YFI out before the end of the vote lock?

- You can't, sorry. The lock lasts 3 days after you last voted, until then you cannot unstake your tokens.
- If you try to unstake your tokens before the lock ends you will see a very high gas cost, this is an error, you will not be able to unstake until the 3 day lock has ended

#### I voted and I know the vote lock is 3 days, is there anywhere I can see exactly how long I have left till I can unstake my YFI?

- Yes! You can read the contract directly ygov.finance staking [contract](https://etherscan.io/address/0xBa37B002AbaFDd8E89a1995dA52740bbC013D992#readContract) go to 28 votelock and input your eth address. This will give you the eth block number when you can unstake.

#### What’s the difference between voting for a poll on the forum and an on-chain vote?

- A poll just gauges the sentiment of what the community is feeling on the proposal while a on-chain vote will be binding and will take effect if it passes.

#### What about the new gasless voting thing?

- We now have an off-chain signaling system that uses staked balances from ygov. This replaces the older, informal forum polls which were vulnerable to sybil attacks. It can do multiple choice and doesn't cost gas to use, you sign with your wallet instead. We still use the normal on-chain voting system for YIPs.

#### How long is my YFI tied up if I stake it?

- Your YFI is locked for 3 days after you vote.

#### Why can't I claim my staking rewards!

- To claim your staking rewards you have to 1\) be staked and 2\) have voted within 3 days to be able to claim them. This will be fixed in an update soon.

### yDAO

- Pokemol [site](https://pokemol.com/dao/0xcb46298767fb5d44c18313976c30d3eeb5071862/).
- Forum [post](https://gov.yearn.finance/t/ydao-for-community-funding/2243).

#### What is its purpose?

- Used to fund value-added contributions to the Yearn ecosystem.

#### Who cares, how do I make money from this?

- You don't. This is solely for allocating funding for projects, and the YFI donated will be spent and your share value will be diluted.

#### Who can join?

- Open for anyone to join with a base rate of 1 Share = 0.1 YFI.

#### How can I join?

- Go here to [Pokemol](https://pokemol.com/dao/0xcb46298767fb5d44c18313976c30d3eeb5071862) sign in with your web3 account. Click New Proposal button in the top right. Click member.
  - Title: your name/entity
  - Description: “Pledging X amount of YFI in exchange for Y Shares” \(Please make this consistent with the amount being pledged at 0.1 YFI per share\)
  - Link: Link to you or your entity \(Website, Twitter, Linkedin\)
  - Shares Requested: The number of Shares being requested
  - Token Tribute: The amount of YFI being pledged \(you will need to unlock YFI\)
  - Loot: The number of shares being requested
  - After you submitted the two transactions and are in the new member queue, you will need a sponsor. Please copy the link to your proposal and let us know you’d like to join in the [yDAO Telegram channel](https://t.me/joinchat/Qn1GPBv0y7lY1vAmRCB7KA)

#### How can I request funding?

- The same ways as joining except instead of click member click the funding tab and fill in the details of your request. You can ask in the [telegram chat](https://t.me/joinchat/Qn1GPBv0y7lY1vAmRCB7KA) if you have any questions.

#### I don't speak English, when will everything be translated?

- We are working on translating to other languages but it will take time. For now you can go to your language in the global section in [Discord](http://discord.yearn.finance/).

## Community

### Does Yearn have a manifesto?

- Some contributors got together and wrote a post about how they think about the protocol, with others joining in to support it. It's available [on the forum](https://gov.yearn.finance/t/how-we-think-about-yearn/).

### Is Andre Cronje in charge of Yearn?

- Andre isn't in charge of Yearn, the YFI token holders make the decisions on how to govern Yearn, Andre is one of the developers in the Yearn ecosystem.

### What is the multisig and what do they do?

- The multi-signature address is explained in detail in this [thread](https://gov.yearn.finance/t/yfi-minting-ownership/155). Basically, it is a 6 of 9 multi-signature account that has control over minting YFI if a vote to mint tokens has passed successfully.

### Who are the 9 multisig signers?

- [Cp0x.com](https://twitter.com/kaplansky1/status/1285427247286046725)
- [Daryllautk](https://twitter.com/Daryllautk/status/1285434908383444992)
- [Devops199fan](https://twitter.com/devops199fan/status/1285430347954622464)
- [Banteg](https://twitter.com/bantg/status/1285426492906909696)
- [Milkyklim](https://milkyklim.keybase.pub/yearn-social-proof.txt)
- [Joe Mahon aka Substreight](https://twitter.com/Substreight/status/1299780260737630209)
- [Tarun Chitra, Gauntlet](https://twitter.com/gauntletnetwork/status/1299778153674616833)
- [Vasiliy Shapovalov, p2p.org](https://twitter.com/_vshapovalov/status/1299799139635679232)
- [Mariano Conti, ex-MakerDAO](https://twitter.com/nanexcool)

### Have the multisig signers changed?

- Yes, [YIP-40](https://gov.yearn.finance/t/yip-40-replace-inactive-multisig-signers/3535) changed four of the signers
- Outgoing signers were:
  - [Coopahtroopa](https://twitter.com/Cooopahtroopa/status/1285438650550038529)
  - [Michael, Curve.fi](https://twitter.com/CurveFinance/status/1285428322986389504)
  - [Calvin Liu](https://twitter.com/cjliu49/status/1285439553180798976)
  - [Damir Bandalo](https://twitter.com/damirbandalo/status/1285500362015875073)

### What decisions can Andre make on his own?

- Andre can build out the Yearn ecosystem and come up with new products. Usually, he posts his thoughts and ideas on the [forum](https://gov.yearn.finance) or on his [medium blog](https://andrecronje.medium.com) for everyone to see.

### Does the multisig group tell him what to do?

- They are in close contact with one another, but Andre's priorities are his own. They can be instructed via YIPs.

### Who else writes code for Yearn? Is there a team?

- Yes! Meet some of the developers behind Yearn:

  - [@banteg](https://gov.yearn.finance/u/banteg)
  - [@fubuloubu](https://gov.yearn.finance/u/fubuloubu)
  - [@x48](https://gov.yearn.finance/u/x48)
  - [@doug](https://gov.yearn.finance/u/doug)
  - [@luciano](https://gov.yearn.finance/u/luciano)
  - [@orbxball](https://gov.yearn.finance/u/orbxball)

### Does anyone get paid for working on Yearn?

- Yes. Yearn has a core team that receives recurring payments. Grants are also distributed to valuable contributors in a monthly basis. For instance, see the [September Grants Announcement](https://gov.yearn.finance/t/september-grants-announcement/7044).

### How can I work for Yearn?

- If you want to contribute to the project as well just reach out to our community managers on [Discord](http://discord.yearn.finance/)/[Telegram](https://t.me/yearnfinance)/[Twitter](https://twitter.com/iearnfinance). We'll also release soon a Contributor's Guide.

### Do you have any job openings?

- Yes, we do! We need all kinds of people to help make the Yearn ecosystem a thriving product and to give value to YFI. You can ask in the Discord or Telegram about applying or post on the forum. State how you think you can add value to Yearn, and how much you think you should be paid from the community pool. Also, you can go to the [yDAO](https://gov.yearn.finance/t/ydao-for-community-funding/2243) as well for funding on your work for the Yearn ecosystem.

### How to Participate?

- You can participate in YFI by voting on YIPs that are active, discussing the YIPs yet to be proposed on-chain on the forums and talking about YFI in the Telegram and Discord. If you know a second language help us translate the site and YIPs into that language.

### Ongoing efforts to improve the Yearn ecosystem

- You can view the active YIPs [here](https://yips.yearn.finance/all-yip)

## User Interface

### Can I use the Yearn ecosystem dApps on my phone?

- Yes, you have to use the Metamask browser

## Technical Support

### I sent my ETH transaction but it says pending? How do I fix this?

- You should always make sure to set your gas properly if you want a transaction to go through quickly. Check current gas prices at [Ethgasstation](https://ethgasstation.info/) or [gasnow](https://www.gasnow.org/).
- If you're using MetaMask and you put your transaction through but it's going too slow, you have the option to speed it up by clicking the `speed up` button below your last pending transaction under "activity". This should resend the same TX again with a higher gas price to get it confirmed faster.
- If you've tried everything and your transaction is still stuck pending, you can fix it by sending a transaction to the nonce of the first stuck transaction with a high gas price to overwrite the stuck queue. Here's a good [guide](https://ethgasstation.info/blog/stuck-transaction-guide) explaining how to do this.

### Why is the withdrawal fee so high?

- If you're seeing higher than normal fees while using the Yearn ecosystem then it may be due to Ethereum congestion and abnormally high gas costs. Check [Ethgasstation](https://ethgasstation.info/). Your options are to wait until gas prices drop or spend the money to process your transaction now.
- If the gas prices are crazy high, that means there is an error and the transaction will not be able to process. For instance if you are trying to deposit a token you don't have or if there is no cover available for a contract at [http://yinsure.finance/](http://yinsure.finance/).

## Related Projects

### [Curve](https://www.curve.fi)

- Curve is an exchange liquidity pool on Ethereum \(like [Uniswap](https://app.uniswap.org/#/)\) designed for \(1\) extremely efficient stablecoin trading \(2\) low risk, supplemental fee income for liquidity providers, without an opportunity cost. Curve allows users \(and smart contracts like 1inch, Paraswap, Totle and Dex.ag\) to trade between DAI and USDC with a bespoke low slippage, low fee algorithm designed specifically for stablecoins and earn fees. Behind the scenes, the liquidity pool is also supplied to the Compound protocol or yearn.finance where it generates even more income for liquidity providers.
- Curve [FAQ](https://www.curve.fi/rootfaq).

### [Aave](https://app.aave.com/home)

- Aave is an open source and non-custodial protocol enabling the creation of money markets. Users can earn interest on deposits and borrow assets.

## Resources

### Where can I learn more about Yearn?

- [Learn Yearn](https://www.learnyearn.finance/)
- [Medium.com/iearn](https://medium.com/iearn)
- [yCosystem](https://ycosystem.info/)

### Lists of Smart Contracts

- [https://gov.yearn.finance/t/yearn-contracts/1951](https://gov.yearn.finance/t/yearn-contracts/1951)
- [https://etherscan.io/accounts/label/yearn-finance](https://etherscan.io/accounts/label/yearn-finance)
  - sign-in required
- [Delegated controller](https://etherscan.io/address/0x2be5d998c95de70d9a38b3d78e49751f10f9e88b#readContract)
- [StrategyVaultTUSD](https://etherscan.io/address/0x35CEE4c61B7619956e0B2015B5411F93CBba817A#code)
- [yLINK token](https://etherscan.io/address/0x881b06da56bb5675c54e4ed311c21e54c5025298#code)
- [yaLINK token](https://etherscan.io/address/0x29e240cfd7946ba20895a7a02edb25c210f9f324#readContract)
- [StrategyMStableSavingsTUSD](https://etherscan.io/address/0xd6214317bf66921154d78e3074bada013a4de8e8#readContract)
- [yTUSD](https://etherscan.io/address/0x37d19d1c4e1fa9dc47bd1ea12f742a0887eda74a)
- [yTokenRebalance](https://etherscan.io/address/0x19b6424C58aFcee6D0cb954D4B8d44B9b5e9cC09#code)
- [CollateralVaultProxy](https://etherscan.io/address/0xf0988322b8392245d6232e520bf3cdf912b043c4)
- [USDC strategy for LINK](https://etherscan.io/address/0x25fAcA21dd2Ad7eDB3a027d543e617496820d8d6)
- [Strategy for USDC vault](https://etherscan.io/address/0xA30d1D98C502378ad61Fe71BcDc3a808CF60b897)
- [Strategy for USDC vault](https://etherscan.io/address/0xA30d1D98C502378ad61Fe71BcDc3a808CF60b897)
- [DAI vault](https://etherscan.io/address/0xACd43E627e64355f1861cEC6d3a6688B31a6F952)

### Registry of Tokens and Utility Contracts

- [https://docs.yearn.finance/yearn.finance/yearn-1](https://docs.yearn.finance/yearn.finance/yearn-1)

### Vaults Detail Reference

- [https://vaults.finance/](https://vaults.finance/)

### Statistics

- [yieldfarming.info](https://yieldfarming.info/)
- [yVault ROI Calculator](https://py-earn.herokuapp.com/)
- [stats.finance/yearn](https://stats.finance/yearn)
- [Feel The Yearn](https://feel-the-yearn.vercel.app/)
- Initial Distribution [Dune Dashboard](https://explore.duneanalytics.com/dashboard/yearn)
- Voting Stats [Dune Dashboard](https://explore.duneanalytics.com/public/dashboards/Lqnxzm7fa8NVhKC4kc37DDFPZgqXryaIjyLRYAYp)
- Vaults Stats [Dune Dashboard](https://explore.duneanalytics.com/public/dashboards/g0bGfgloeXBd9C18jpBjdXi5KkQjR7IXYqFRUnHk)

### Latest Yearn News

- [yearn.finance](https://twitter.com/iearnfinance) - Offical Twitter of Yearn
- [AndreCronjeTech](https://twitter.com/AndreCronjeTech)
- [Yearn Finance](https://medium.com/iearn) - Offical Blog

### Podcasts

- [Unchained - Andre Cronje on YFI and the Fair Launch: ‘I’m Lazy’](https://unchainedpodcast.com/andre-cronje-of-yearn-finance-on-yfi-and-the-fair-launch-im-lazy/)
- [Andre Cronje and the Philosophy of Yearn Finance](https://anchor.fm/hasu-research/episodes/6-Andre-Cronje-and-the-Philosophy-of-Yearn-Finance-ei4vds)
- [The FTX Podcast - Andre Cronje DeFI Architect](https://open.spotify.com/episode/6d14TJtQU7eB69azelpdeh)
- [Zapper Community Call - With Andre](https://www.youtube.com/watch?v=venoiaiVZ-U)
- [In DeFi My Money is Actually Mine. Its a Beautiful Concept But it Comes With Responsibilities - Andre Cronje](https://anchor.fm/camila-russo/episodes/In-DeFi-My-Money-is-Actually-Mine--Its-a-Beautiful-Concept-But-it-Comes-With-Responsibilities-Andre-Cronje-ehs3op)
- [YFI: Farming the Farmers \| Andre Cronje](http://podcast.banklesshq.com/25-king-of-the-yield-farmers-andre-cronje)

### Blogs

- [Yearn Finance - Offical Blog](https://medium.com/iearn)
  - [Yinsure.finance: A new insurance primitive](https://medium.com/iearn/yinsure-finance-a-new-insurance-primitive-77d5d4217896)
  - [Delegated Vaults Explained](https://medium.com/iearn/delegated-vaults-explained-fa81f1c3fce2)
  - [yearn.finance v2](https://medium.com/iearn/yearn-finance-v2-af2c6a6a3613?source=---------3------------------)
  - [Yearn Governance Forum](https://medium.com/iearn/yearn-governance-forum-7b7c9d0300ac?source=collection_home---6------2-----------------------)
  - [YFI rewards pool](https://medium.com/iearn/yfi-rewards-pool-810ef9256ec6)
  - [YFI](https://medium.com/iearn/yfi-df84573db81)

### Logos

- Can be found in the Discord under [\#media-resources](https://discord.com/channels/734804446353031319/736132884443955242/740325105904779326)
