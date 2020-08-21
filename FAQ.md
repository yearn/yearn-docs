---
title: faq.yearn.finance
---

# General

## Is it safe to invest money in yearn?
- Please do your own research and decide for yourself.

## Is yearn audited?
- Yes, you can find the list of audits [here](https://github.com/iearn-finance/audits)

<br>

# Feedback & Support
If you have questions about how to do anything, we can help you on:
- [Discord](https://discord.gg/GcjxhWR)
- [Telegram](https://t.me/yearnfinance)

<br>

But if you think something can be improved, or you found a bug, we want to squash it. Please post it here:
- [Github](https://github.com/iearn-finance) — create a new issue in the relevant repository
- [Forum](https://gov.yearn.finance/c/feedback/) — post in the feedback category
<br>

# Products

## [yearn.finance](https://yearn.finance/)
- Yearn.Finance hosts UIs for the **Earn**, **Zap**, **APR**, and **Vaults** products
### [Earn](https://yearn.finance/earn)
- Yield aggregator for lending platforms that rebalances for highest yield during contract interaction.
- Deposit DAI, USDC, USDT, TUSD, or sUSD and it will auto lend to the highest lending rate on these platforms [Compound](https://compound.finance/), [Dydx](https://dydx.exchange/), or [Aave](https://app.aave.com/home) (Ddex and Fulcrum are currently disabled)
- Info on this can be found in the [Yearn Docs](https://docs.yearn.finance/yearn.finance/yearn)
- Profit switching lender to optimize lending yields (live)

### [Zaps](https://yearn.finance/zap)

#### What is a Zap?
- Zap allows users to convert supported tokens with just one contract interaction to reduce transaction costs
- Zaps were made by DefiZap which is now [Zapper.fi](https://zapper.fi) as a type of all in one defi routing service. 

#### Why use a Zap?
- "Zaps allow you get into a DeFi position in one transaction—it’s called zapping in." - [How to use Zaps guide](https://defitutorials.substack.com/p/how-to-use-defizap)
    - Note that this is an old article and [Zapper](https://zapper.fi) was formed as a result of DeFiSnap + DeFiZap coming together to create the ultimate hub for Decentralized Finance aka #DeFi. So some of the stuff in the article above is out of date, but you can still use Zaps on Zapper.fi

#### So what can I do with Zaps on yearn?
- With as zap you can take your DAI, for example, and get yCurve with it in one transaction. Normally, to turn DAI in to yCRV, you would have to go to earn, deposit DAI and receive yDAI, then go to [Curve.fi - Yearn pool](https://www.curve.fi/iearn/deposit) and deposit your yDAI and then you would get yCRV. This is alot to do so instead you can do it in one transaction!

#### That sounds awesome, what's the downside?
- Well, it does take a lot of gas and could be costly, even more so than doing it yourself manually, but if you have a big transaction and are in a rush it is a great method to get into a DeFi position or liquidity pool fast. 

### [APR](https://yearn.finance/apr)
#### What is this even for?
- It's a table that shows you the current APR for some yearn-supported tokens across lending platforms. The highest APR for each coin is the provider that Earn is lending these coins to at the moment.

### [Vaults](https://yearn.finance/vaults)

#### What is a Vault? How is it different from Earn?
- A Vault takes a more active approach than simply lending out coins for the highest APY. Via strategies it can farm coins such as CRV and then sell them, into the best DEX, to higher profits than simple lending. Yield is achieved by providing the asset for lending, LP, or farming strategies. These are opportunities that exist in defi. Vaults automate these processes and provide the highest (risk adjusted) yield available.
- Andre explains vaults here [Yearn Finance v2](https://medium.com/iearn/yearn-finance-v2-af2c6a6a3613) and here [Delegated Vaults Explained](https://medium.com/iearn/delegated-vaults-explained-fa81f1c3fce2) in these two blog posts.
- Simply put vaults can do this:
    - Provided liquidity can be any asset.
    - Use liquidity as collateral
        - Manage collateral at a safe level so you never default
    - Borrow stablecoins
    - Put the stablecoin to work on some farming
    - Any stablecoin earned above the debt (i.e. gains) are sold for the vault asset and returned to the vault.

#### Can't I just do all this myself though?
- Yes you could, but vaults help you save on gas, keep it at a good collateral/debt ratio so you dont default, and auto optimizes for highest yielding stablecoin strategies, even when you are sleeping.

#### I see ROI on the vaults page is the current APY?
- No. This is the historical average for that vault. Current APY / returns are not shown as the vaults is a beta product and being tested live. The returns are posted around once a day on [twitter](https://twitter.com/iearnfinance)

#### Risks
- While the assets deposited can't decrease, the debt of the vault can. If a strategy does not manage to outperform the debt, then a portion of the asset will be impermanently locked. If a strategy then outperforms the debt again, this asset will become unlocked.
    - There are mechanisms in the vaults to help this not to happen, but nothing is foolproof
- As of now, the Vaults have not been audited
- Smart contract risk with any contracts that the vaults interact with.

#### Currently Active Vaults
- v2 Vaults
    - aLINK
        - Why is the yield different for the two link vaults on [stats.finance/yearn](https://stats.finance/yearn)?
            - [aLINK has a 0.5% insurance fee](https://twitter.com/iearnfinance/status/1293772592004976641)
    - ChainLink
- v1 Vaults
    - Curve.fi/y (yCRV)
    - DAI
    - TUSD
    - USD Coin
        - You will receive yyUSDC. It's not the same token you will receive in Earn, even if everybody calls them the same.
    - USDT

#### If the current strategy for the yCRV vault is farming crv does it just get added to my balance when I withdrawal?
- No. The vault will farm CRV then sell it on the market automatically. When you withdrawal you will get more yCRV.

#### Why isn't yCRV worth $1, it's a stable coin right?
- No, yCRV is not worth $1 and no it is NOT a stablecoin. You can think of yCRV as an index of yield bearing stablecoins (yDAI+yUSDC+yUSDT+yTUSD) that also generates yield (trading fees from the Curve Y pool) as well. Therefore the price of yCRV is always increasing.

#### If I unstake my yCRV from the yCRV vault does that then revert it back to the Curve Y pool at Curve, or do I have to do something else like restake it there?
- When you withdraw your yCRV from the vault, you get back yCRV + plus interest accrued - fees, all in yCRV. Since it is the yCRV token you got back, it is already staked in Curve Y pool making stablecoin swap fees. No need to do anything else with Curve, unless you want to stake it [here](https://dao.curve.fi/minter/gauges) to generate CRV.

#### I deposited into a vault what will I get out when I withdrawal?
- You will always withdrawal only the coin type you put in + the pool yield - fees.

#### Fees
- The fee on all vaults is 0.5% on withdrawals and a 5% fee whenever the harvest() function is called on the vaults which helps subsidize gas costs. The harvest function does the selling of the farmed asset on the market.
- Fees can be changed by governance.
- If you deposit and withdraw immediately, you will lose 0.5% of your principle

#### Yield
- We plan to make a dashboard in the future that will clearly show your current APY of all the positions you have open. Currently for the Vaults as they are still in beta we are not showing the APY live, but it is post on [twitter](https://twitter.com/iearnfinance) around once a day. You can roughly estimate the yield you are getting by looking at what the [current strategy](https://feel-the-yearn.vercel.app/) is farming and checking what its apy is.
- For example if yCRV vault is farming the CRV token, you can check what the yield is on [Curve's homepage](https://www.curve.fi/) for the Y pool

### Vault Strategies

#### What is a Vault Strategy?
- Yearn's vault strategies are modular smart contracts for each vault that tells it what assets to borrow, which coins to farm, and where it should sell the farmed assets.

#### What are the current strategies?
- You can view the current strategies implemented at [feel-the-yearn](https://feel-the-yearn.vercel.app/)
- In the future we plan to make a dashboard to make the strategies and APY easy to understand.

#### Who is in control of the strategies?
- Andre writes them but the multi-sig decides if they will be implemented or not.

#### How can I make a strategy?
- For now you can post your strategy on the forum in the strategy section. Detailing what it should buy/sell/farm and what the current apy is. There will be a template to help you get started.

#### What is the process for getting my strategy onto yearn?
- Post it on the forum and if it gets approved it will be used in the vaults and you can get paid for it.

#### When does a strategy changes and who changes it? Is it automatic?
- For now Andre watches the markets and writes strategies that he and the multi-sig thinks are safe while giving the highest yield. They change them according to current yields on the market.

## [ytrade.finance](https://ytrade.finance/)
- Leveraged stable coin trades (testnet)

## [yliquidate.finance](https://yliquidate.finance/)
- 0 capital automated liquidations for Aave (testnet)

## [yswap.exchange](https://yswap.exchange/)
- Single sided automated market maker (testing in mainnet)

## [yborrow.finance](https://yborrow.finance/)
- Credit delegation vaults for smart contract to smart contract lending (testnet)

## [yinsure.finance](https://medium.com/iearn/yinsure-finance-a-new-insurance-primitive-77d5d4217896) 
- Prototype for a new kind of tokenized insurance (testnet)

<br>

# Tokens

## YFI
- Yearn Governance token
- Only 30,000 minted and already fully distributed
    - Governance can mint more, if proposal to do so passes.

## yTokens
- When you deposit into any yearn service your depost is wrapped and returned as a yToken representing the liquidity provided
- For example, if you deposit DAI in y.curve.fi you will receive yDAI in return
- Amounts of yToken and deposited token will differ since the yToken represents a share of a pool that is increasing in value
- If you deposit a yToken into another yearn service you will get a yyToken back


## yCRV
- LP token for yearn's Y pool at Curve.fi
- Aka `yDAI+yUSDC+yUSDT+yTUSD`
- Interest earning token representing your share of the Y pool composed of DAI, USDT, USDC, and TUSD 
- Via [How to provide liquidity on Curve.fi Y pool?](https://guides.curve.fi/how-to-provide-liquidity-on-curve-fi-y-pool/)
    - Curve Finance Y pool has long been one of the most popular pools on Curve Finance due to its strong returns from trading fees supplemented by iEarn which also lends your stable coin in the background to the lending protocol with the best lending rates out of Compound, dYdX and AAVE.


## yyCRV
- LP token for yearn's yCRV yVault
- aka `yyDAI+yUSDC+yUSDT+yTUSD`
- When you deposit yCRV into the yVault you receive yyCRV LP tokens
- earns interest via yCRV, fees and yield farming rewards via the vault strategy

<br>

# Communication
- [Forum](https://gov.yearn.finance/)
    - A lot of real-time discussion happens on the telegram and discord, but for a proposal to turn into a YIP (Yearn Improvement Proposal) it needs to be posted and discussed on the forum.
    - This is the main place token holders check for governance related issues.
- [Discord](https://discord.gg/94CmMdt)
    - Including non-English channels
- [Telegram - Main Chat](https://t.me/yearnfinance)
- [Telegram - Trading/Social/Fork Chat](https://t.me/yearncommunity)
- Twitter
    - [yearn.finance - Official Twitter of Yearn](https://twitter.com/iearnfinance?s=20)
    - [Andre Cronje - Lead Developer of Yearn](https://twitter.com/AndreCronjeTech?s=20)

<br>

# Governance

## All about YIPs

### What is a YIP? Why do they matter?
- A YIP or Yearn Improvement Proposal is how features are added to the yearn ecosystem. Users start a proposal on the forum, discuss it, and gauge the sentiment of if the proposal will be accepted. If a lot of users agree with it, then it can be posted on-chain for everyone to vote on. 

### How many people need to vote to pass a YIP proposed on-chain?
- The quorum is 20%. Which means that 20% of the staked YFI needs to vote on a proposal for it to pass, or else it will fail. Also, it has to have at least 50% of the votes for yes.
- You can post your proposal on-chain first, but if people haven't talked about it, they probably won't vote for it.

### How do I make a proposal?
- The default template for proposals can be found on [Github](https://github.com/iearn-finance/YIPS/blob/master/yip-X.md) + on the [forum](https://gov.yearn.finance/) if you make a post under proposals or discussion it will auto-fill in the template as well. 

### Who can make a proposal?
- Anyone can post a proposal both on the forum and on-chain.

## Voting 

### How do I vote? 
- Stake your YFI and then you can cast your vote for YIPs that are on-chain on the [voting dashboard](https://ygov.finance/vote)

### Where can I view the YIPs?
- You can view them on the [voting dashboard](https://ygov.finance/vote) if you login to your web3 account or at [yips.yearn.finance](https://yips.yearn.finance/all-yip)

### Why should I stake? What is the APY (Annual Percentage Yield)?
- You should stake if you want to vote on YIPs and get rewards that are generated from the yearn ecosystem. The APY for staking is currently not listed on the UI. You can ask on the chat what the rate is.

### What do I have to do to get rewards with my YFI?
- All you need to do is stake YFI at [ygov.finance/stake](https://ygov.finance/stake) and you will get rewards IF the treasury is at or above 500k usd. You can check the treasury address [here](https://zapper.fi/dashboard?address=0xFEB4acf3df3cDEA7399794D0869ef76A6EfAff52https://zapper.fi/dashboard?address=0xFEB4acf3df3cDEA7399794D0869ef76A6EfAff52).
- Note that if you stake you get rewards (as long as they are not going to the treasury), but you can only claim them within 3 days of voting. 

### Does staking my YFI matter for voting?
- Yes. You have to stake your YFI at [ygov.finance/stake](https://ygov.finance/stake) in the v2 tab under Governance V2 to have your votes count. As of now, you can vote without staking, but you will waste your gas and it won't count so make sure you have staked first if you want to vote.

### What if I want to take my YFI out before the end of the vote lock?
- You can't, sorry. The lock lasts 3 days after you last voted, until then you cannot unstake your tokens.

### I voted and I know the vote lock is 3 days, is there anywhere I can see exactly how long I have left till I can unstake my YFI?
- Yes! You can read the contract directly [ygov.finance staking contract](https://etherscan.io/address/0xBa37B002AbaFDd8E89a1995dA52740bbC013D992#readContract) go to 28 votelock and input your eth address. This will give you the eth block number when you can unstake.

### What’s the difference between voting for a poll on the forum and an on-chain vote?
- A poll just gauges the sentiment of what the community is feeling on the proposal while a on-chain vote will be binding and will take effect if it passes.

### How long is my YFI tied up if I stake it?
- Your YFI is locked for 3 days after you vote

### Why can't I claim my staking rewards! 
- To claim your staking rewards you have to 1) be staked and 2) have voted. Within 3 days to be able to claim them. This will be fixed in an update soon.

## [yDAO](https://gov.yearn.finance/t/ydao-for-community-funding/2243) 

### What is its purpose?
- Used to fund value-added contributions to the yearn ecosystem.

### Who cares, how do I make money from this?
- You don't. This is solely for allocating funding for projects, and the YFI donated will be spent and your share value will be diluted.

### Who can join?
- Open for anyone to join with a base rate of 1 Share = 0.1 YFI

### How can I join?
- Go here to [Pokemol](https://pokemol.com/dao/0xcb46298767fb5d44c18313976c30d3eeb5071862) sign in with your web3 account. Click New Proposal button in the top right. Click member. 
    - Title: your name/entity
    - Description: “Pledging X amount of YFI in exchange for Y Shares” (Please make this consistent with the amount being pledged at 0.1 YFI per share.)
    - Link: Link to you or your entity (Website, Twitter, Linkedin)
    - Shares Requested: The number of Shares being requested
    - Token Tribute: The amount of YFI being pledged (you will need to unlock YFI)
    - Loot: The number of shares being requested
    - After you submitted the two transactions and are in the new member queue, you will need a sponsor. Please copy the link to your proposal and let us know you’d like to join in the [yDAO Telegram channel](https://t.me/joinchat/Qn1GPBv0y7lY1vAmRCB7KA)

### How can I request funding?
- The same ways as joining except instead of click member click the funding tab and fill in the details of your request. You can ask in the [telegram chat](https://t.me/joinchat/Qn1GPBv0y7lY1vAmRCB7KA) if you have any questions.

### I don't speak English, when will everything be translated?
- We are working on translating to other languages but it will take time. For now you can go to your language in the global section in [Discord](https://discord.gg/94CmMdt).


<br>


# Community

## Is Andre Cronje in charge of yearn?
- Andre isn't in charge of Yearn, the YFI token holders make the decisions on what to build and governance decisions, but Andre is the lead developer of the yearn ecosystem.

## What does Andre do?
- Andre is the main developer building out the products that comprise the yearn ecosystem: Yearn, Ytrade, Yswap, Yliquidate, Yborrow. He is also currently in charge of running the Vaults and overseeing them. 

## What is the multisig and what do they do?
- The multi-signature address is explained in detail in this [thread](https://gov.yearn.finance/t/yfi-minting-ownership/155). Basically it is a 6 of 9 multi-signature account that has control over minting YFI, if a vote to mint tokens has passed successfully.

## Who are the 9 multisig signers?
- [Calvin Liu](https://twitter.com/cjliu49/status/1285439553180798976?s=21)
- [Coopahtroopa](https://twitter.com/Cooopahtroopa/status/1285438650550038529)
- [Cp0x.com](https://twitter.com/kaplansky1/status/1285427247286046725)
- [Curve.fi](https://twitter.com/CurveFinance/status/1285428322986389504)
- [Damir Bandalo](https://twitter.com/damirbandalo/status/1285500362015875073?s=20)
- [Daryllautk](https://twitter.com/Daryllautk/status/1285434908383444992)
- [Devops199fan](https://twitter.com/devops199fan/status/1285430347954622464)
- [Banteg](https://twitter.com/bantg/status/1285426492906909696)
- [Milkyklim](https://milkyklim.keybase.pub/yearn-social-proof.txt)

## What decisions can Andre make on his own?
- Andre can build out the Yearn ecosystem and come up with new products. Usually he posts his thoughts and ideas on the [forum](https://gov.yearn.finance/) for everyone to see.

## Does the multisig group tell him what to do?
- They are in close contact with one another, but Andre's priorities are decided by YFI token holders via YIPS.

## Who else writes code for yearn? Is there a team?
- Right now it's just Andre

## Does anyone get paid for working on yearn?
- As of this moment, not yet, but thanks to the passage of [YIP 36](https://yips.yearn.finance/YIPS/yip-36) and the creation of a community pool of funds that will be kept at 500k usd, we can now pay Andre for his work, fund audits, and pay for new devs to be hired along with anything else the the yearn ecosystem needs.

## How can I work for yearn?
- You can make a YIP to apply for funding from the 500k USD treasury directly or ask the yDAO for funding.

## Do you have any job openings?
- Yes, we do! We need all kinds of people to help make the yEarn ecosystem a thriving product and to give value to YFI. You can ask in the Discord or Telegram about applying or post on the forum. State how you think you can add value to Yearn, and how much you think you should be paid from the community pool. Also, you can go to the [yDAO](https://gov.yearn.finance/t/ydao-for-community-funding/2243) as well for funding on your work for the Yearn ecosystem.

## How to Participate
- You can participate in YFI by voting on YIPs that are active, discussing the YIPs yet to be proposed on-chain on the forums, and talking about YFI in the telegram and discord. If you know a second language help us translate the site and YIPs into that language. 

## Ongoing efforts to improve the Yearn ecosystem
- You can view the active YIPs [here](https://yips.yearn.finance/all-yip)

<br>

# User Interface
## Can I use the Yearn ecosystem dApps on my phone?
- Yes, you have to use the Metamask browser

<br>

# Related Projects
## [Curve](https://www.curve.fi/)
- Curve is an exchange liquidity pool on Ethereum (like [Uniswap](https://app.uniswap.org/#/)) designed for (1) extremely efficient stablecoin trading (2) low risk, supplemental fee income for liquidity providers, without an opportunity cost. Curve allows users (and smart contracts like 1inch, Paraswap, Totle and Dex.ag) to trade between DAI and USDC with a bespoke low slippage, low fee algorithm designed specifically for stablecoins and earn fees. Behind the scenes, the liquidity pool is also supplied to the Compound protocol or yearn.finance where it generates even more income for liquidity providers.
- Curve [FAQ](https://www.curve.fi/rootfaq)

## [Aave](https://app.aave.com/home)
- Aave is an open source and non-custodial protocol enabling the creation of money markets. Users can earn interest on deposits and borrow assets.

<br>

# Resources

## Where can I learn more about yearn?
- [Learn Yearn](https://www.learnyearn.finance/)
- [Medium.com/iearn](https://medium.com/iearn)
- [yCosystem](https://ycosystem.info/)

## Lists of Smart Contracts
- https://gov.yearn.finance/t/yearn-contracts/1951
- https://etherscan.io/accounts/label/yearn-finance
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

## Registry of Tokens and Utility Contracts
- https://docs.yearn.finance/yearn.finance/yearn-1

## Vaults Detail Reference
- https://vaults.finance/

## Statistics

- [yieldfarming.info](https://yieldfarming.info/)
- [yVault ROI Calculator](https://py-earn.herokuapp.com/)
- [stats.finance/yearn](https://stats.finance/yearn)
- [Feel The Yearn](https://feel-the-yearn.vercel.app/)
- Yearn Initial Distribution [Dune Dashboard](https://explore.duneanalytics.com/dashboard/yearn)
- Voting Stats [Dune Dashboard](https://explore.duneanalytics.com/public/dashboards/Lqnxzm7fa8NVhKC4kc37DDFPZgqXryaIjyLRYAYp)


## Latest Yearn News
- [yearn.finance - Offical Twitter of Yearn](https://twitter.com/iearnfinance)
- [AndreCronjeTech](https://twitter.com/AndreCronjeTech)
- [Yearn Finance - Offical Blog](https://medium.com/iearn)

## Podcasts
- [Andre Cronje and the Philosophy of Yearn Finance](https://anchor.fm/hasu-research/episodes/6-Andre-Cronje-and-the-Philosophy-of-Yearn-Finance-ei4vds)
- [The FTX Podcast - Andre Cronje DeFI Architect](https://open.spotify.com/episode/6d14TJtQU7eB69azelpdeh)
- [Zapper Community Call - With Andre](https://www.youtube.com/watch?v=venoiaiVZ-U)
- [In DeFi My Money is Actually Mine. Its a Beautiful Concept But it Comes With Responsibilities - Andre Cronje](https://anchor.fm/camila-russo/episodes/In-DeFi-My-Money-is-Actually-Mine--Its-a-Beautiful-Concept-But-it-Comes-With-Responsibilities-Andre-Cronje-ehs3op)
- [YFI: Farming the Farmers | Andre Cronje](http://podcast.banklesshq.com/25-king-of-the-yield-farmers-andre-cronje)

## Blogs
- [Yearn Finance - Offical Blog](https://medium.com/iearn)
    - [Yinsure.finance: A new insurance primitive](https://medium.com/iearn/yinsure-finance-a-new-insurance-primitive-77d5d4217896)
    - [Delegated Vaults Explained](https://medium.com/iearn/delegated-vaults-explained-fa81f1c3fce2)
    - [Yearn.finance v2](https://medium.com/iearn/yearn-finance-v2-af2c6a6a3613?source=---------3------------------)
    - [Yearn Governance Forum](https://medium.com/iearn/yearn-governance-forum-7b7c9d0300ac?source=collection_home---6------2-----------------------)
    - [YFI rewards pool](https://medium.com/iearn/yfi-rewards-pool-810ef9256ec6)
    - [YFI](https://medium.com/iearn/yfi-df84573db81)

## Logos
- Can be found in the discord under [#media-resources](https://discord.com/channels/734804446353031319/736132884443955242/740325105904779326)
