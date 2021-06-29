# Protocol Risks

Yearn’s core products are the vaults. Each vault runs at least one strategy, and each strategy is exposed to at least one protocol. Strategy and protocol risks are described [here](https://docs.yearn.finance/resources/risks/strategy-risks) and [here](https://docs.yearn.finance/resources/risks/protocol-risks) respectively.

The key protocols to which Yearn’s vaults are exposed are lending protocols, AMMs and protocols that enable leverage.

## Lending Protocols

One of the simplest strategies is collateralized lending which involves lending assets on lending protocols to earn a yield. For example, the optimized lending strategy used by the Dai vault lends Dai on the highest yielding lending protocol.

Yearn’s vaults are exposed to the lending protocols Aave, Compound Finance, dYdX and Alpha Homora.

|Risk|Description|
|----|-----------|
|Governance|Admin key holders (or token holders) change the lending protocol adversely, e.g. accept risky assets with lenient risk parameters|
|Technological|Smart contract risk from interacting with lending protocols|
||Liquidations do not occur as expected|
|Market|The value of the loans exceed the value of the collateral|
||Low demand for borrowing leads to low yields|
||Accepted assets become impaired|
|Oracle|Incorrect price feed causes the collateral to go to such a value that the loan is liquidated|

## Automated Market Makers

AMMs are used in Yearn’s vault strategies to earn trading fees (and liquidity mining rewards if available) and to exchange liquidity mined tokens for the Want token.

Examples of the AMMs to which Yearn’s vaults are exposed are Curve Finance, Sushiswap and Uniswap. Curve Finance is predominantly used to earn trading fees and farm CRV rewards, whereas Sushiswap and Uniswap are used to exchange liquidity mined tokens for the Want token.


|Risk|Description|
|----|-----------|
|Market|Lack of liquidity for the token being exchanged|
||Trading volumes reduce leading to lower fees|
||Impermanent loss due to the pool’s token prices changing relative to each other|
|Technological|Smart contract risk from interacting with AMMs|
|Governance|Token holders vote to change the AMM adversely|

## Leverage-enabling protocols

Leverage-enabling protocols are used in Yearn’s vault strategies to increase the yield. This is possible when a non-leveraged strategy earns a higher return than the cost of borrowing.

Examples of the leverage-enabling protocols to which Yearn’s vaults are exposed are Maker, Unit Protocol, Aave, dYdX and Cream.Finance.

Maker and Unit Protocol enable the minting of stablecoins against collateral. The stablecoins can then be invested in yield-bearing strategies.

Aave and dYdX offer flash loans which allows Yearn’s strategies to take out a loan, deploy the capital in a strategy and repay the loan in one transaction.

Cream.Finance, in combination with Ironbank, allows strategies to increase yield with protocol-to-protocol uncollateralized borrowing. This is because Yearn’s strategies have been white-listed by Cream.Finance allowing them to borrow depositors’ funds that have not been lent out, in order to deploy in strategies that have a greater return than the cost of borrowing.


|Risk|Description|
|----|-----------|
|Governance|Multi-sig or token holders vote to change the protocol adversely|
||Poorly chosen risk parameters for onboarded collateral of Maker or Unit Protocol, e.g. collateralization ratios that are too low|
|Technological|Smart contract risk|
|Market|Liquidations are not processed correctly on Maker or Unit Protocol|
||Stablecoin peg is not maintained (Dai and USDP for Maker and Unit Protocol respectively)|
||Cost of uncollateralized borrowing from Cream.Finance increases such that Yearn’s strategies cannot utilize it|
|Oracle|Incorrect price feed leads to incorrect liquidation of positions  (Maker and Unit Protocol)|

## Liquidity mining protocols


A core strategy for Yearn’s vaults is to liquidity mine (or yield farm) protocols.
Liquidity mining involves interacting with a protocol to earn the protocol’s native tokens. The interaction can be as simple as staking an asset in a protocol’s staking contract, or it can be more complicated such as staking SNX to mint sUSD in Synthetix to earn SNX rewards.
In most cases the liquidity mined token is exchanged for the Want token on an AMM. For example, in the Dai vault the COMP token is farmed by supplying Dai to Compound Finance to earn COMP rewards, which are exchanged for more Dai.


|Risk|Description|
|----|-----------|
|Governance|Admin key holders change protocol adversely, e.g. introduce penalties for withdrawals or steal funds|
|Technological|Smart contract risk of protocol or rewards contract|
|Market|Fall in price of token being farmed reducing the APY|
||Liquidity of liquidity mined token on AMM is reduced or removed |
|Oracle|Delays or inability to withdraw liquidity in an emergency|

The [Safe Farming Committee](https://gov.yearn.finance/t/introducing-yearn-safe-farming-committee/10533) considers these risks in detail and decides which protocols are secure.
