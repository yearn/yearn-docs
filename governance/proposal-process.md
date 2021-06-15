# Proposal Process

The Yearn ecosystem is controlled by YFI token holders who submit and vote on off-chain proposals that govern the ecosystem. Proposals that generate a majority support (>50% of the vote) are implemented by a 9 member multi-signature wallet. 

Changes must be signed by 6 out of the 9 wallet signers in order to be implemented. The [members of the multi-signature wallet](https://docs.yearn.finance/resources/faq#who-is-on-the-multisig) were voted in by YFI holders and are subject to change from future governance votes. 
# Discussion

Discussion regarding changes in the protocol happen on a variety of platforms such as:

 - [Governance Forum](https://gov.yearn.finance/)
 - [Discord](https://discord.yearn.finance)
 - [Telegram](https://t.me/yearnfinance)

It is recommended to get as much feedback as possible from the various channels of communication before introducing a formal proposal. The governance forum and Discord server have dedicated channels for specific topics.

# Proposal

## Types of proposals

**Yearn Improvement Proposals** (YIPs) are an all-encompassing vehicle for exercising power that token holders are granted. After [YIP-61](https://gov.yearn.finance/t/yip-61-governance-2-0/10460), **Yearn Delegation Proposals** (YDPs) were introduced, which allow token holders to change where any discrete decision-making power is delegated.

![](https://i.imgur.com/ZRNp2Zq.png)

### Previous and current proposals
- Previous: [Proposal Repository](https://docs.yearn.finance/governance/proposal-repository)
- Current: [Snapshot](https://snapshot.page/#/yearn) 

### Requirements to pass proposals
- 3 day discussion on the [forum](https://gov.yearn.finance/)
  - At least 25% vote 'for' the change
- 1 YFI in possession to submit to snapshot
- 5 day [snapshot](https://snapshot.org/#/ybaby.eth) with over 50% passing votes

## Making a proposal

Anyone can post a proposal on the forum for discussion within the community. If it's promoted to off-chain votation (via [Snapshot](https://snapshot.page/#/yearn)), only someone holding 1 YFI can submit it to Snapshot. In case your proposal made it to off-chain votation and you don't have enough YFI, mods will help you.

The default template for proposals can be found on [Github](https://github.com/yearn/YIPS/blob/master/yip-X.md) + on the [forum](https://gov.yearn.finance) if you make a post under proposals or discussion it will auto-fill in the template as well.

**Resources**:
- [Proposal How-To](https://gov.yearn.finance/t/proposal-how-to/106)
- [YIP 0: YIP Purpose and Guidelines](https://yips.yearn.finance/YIPS/yip-0)
- [YIP 44: Improve YIP Categories](https://yips.yearn.finance/YIPS/yip-44)
- [YIP 55: Formalize the YIP Introduction and Voting Process](https://gov.yearn.finance/t/yip-55-formalize-the-yip-process/7959)

# Voting

## How do I vote?

- Holding or staking YFI in the following places will enable you to vote on Yearn's [Snapshot](https://snapshot.page/#/yearn) page:
	- Your wallet
	- YFI yVault V2 (equivalent to holding the yvYFI token)
	- Balancer YFI/WETH LP token
	- Uniswap YFI/WETH LP token
	- Sushiswap YFI/WETH LP token staked in MasterChef
	- MakerDAO YFI collateral
	- Unit Protocol YFI collateral
	- Bancor

## What’s the difference between voting for a poll on the forum and an off-chain vote?

- A poll just gauges the sentiment of what the community is feeling on the proposal while an off-chain vote (via [Snapshot](https://snapshot.page/#/yearn)) will be binding and will take effect if it passes.

# Implementation

Once a Snapshot votes have passed, changes will be implemented by Yearn's protocol or operations team and signed by the multi-sig, if necessary.
