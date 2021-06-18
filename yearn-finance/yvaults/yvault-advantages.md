# How Yearn increases your yield 

Almost everything that yVaults interact with is available to the public. So how is Yearn able to offer users better yield than they'd be able to achieve on their own? 

## Curve Finance Synergy 

Many of Yearn's strategies utilize Curve Finance's liquidity mining program. [Curve Finance](https://curve.fi/) has a 300 year token distribution program for those who provide liquidity for their low slippage decentralized exchange.

### veCRV Boosts 

CRV is distributed continuously to users who stake certain liquidity provider tokens in Curve's [gauge](https://resources.curve.fi/base-features/understanding-gauges). Those CRV rewards can be increased when the user locks up their CRV in the [Locker](https://dao.curve.fi/locker). This locker gives the staker veCRV in return, which bears the right to vote in governance and to claim a portion of the protocol's fees. 

Locking CRV allows users to boost the CRV rewards they are receiving when providing liquidity in eligible pools. The amount of the boost is determined by how much CRV was locked and their relative stake in the pool. 

![](https://i.imgur.com/QaMMdr7.png)

Using the Backscratcher yVault, Yearn locks up a significant amount of CRV indefinitely, and distributes the boosts to various yVaults.  

### Backscratcher yVault

The Backscratcher yVault capitalizes on liquidity mining in a way that's beneficial to both Curve and Yearn. 

Users deposit CRV into the yVault which is locked infinitely. In return they receive a token that represents a share of the Backscratcher pool. Revenue earned from the curve through curve fee sharing is distributed in the Backscratcher pool and can be redeemed by depositors on a weekly basis. 

Additionally, 10% of all CRV earned by Yearn Finance is deposited into Backscratcher and locked infinitely. Because of this, people who want to stake CRV will always receive a higher share of the Backscratcher yVault's revenue than staking directly through Curve. They also can earn emissions of tokens like SUSHI and PICKLE for providing liquidity. 

![](https://i.imgur.com/UfCikwk.png)

Users will never be able to withdraw their original CRV, but because of the incentives on yveCRV liquidity and the value that the token accrues from various sources of revenue, they will be able to swap it for another asset for some price. 

In return, control over the locked CRV's boosts is given to Yearn, and utilized throughout various yVaults. 

## Auto-compounding yield 

Compounding yield requires transaction fees to be paid to the Ethereum blockchain. This can be expensive and cut into returns. 

Because yVaults batch your transaction with many other depositors, it is cumulatively lower cost and higher return to farm using the vaults. Currently, gas costs are covered by the Keep3r network, meaning that users are compounding returns while bearing no cost. 

## Leverage 

Yearn utilizes the Iron Bank (C.R.E.A.M. Finance) to access credit that is used to enhance yVault yields. Only white-listed addresses have this feature available to them, meaning that typically, individuals are not able to do this on their own. 

Some strategies also implement [flash loans](https://docs.yearn.finance/resources/defi-glossary#flash-loan), which is typically a back-end service that requires development experience to take advantage of. 

## Partnerships

The Backscratcher yVault is only possible due to synergistic relationships with protocols like Curve, SushiSwap and Pickle Finance. Our relationships across DeFi allow yVault depositors benefits that they cannot get elsewhere. 

Yearn actively collaborates on development with protocols like the ones mentioned in order to create new opportunities for yield and further DeFi as an industry. 



