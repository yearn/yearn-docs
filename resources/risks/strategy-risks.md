# Strategy Risks

Yearn earns income from lending, liquidity mining and trading fees. This income is often increased using leverage.

## Lending

Collateralized lending is when an asset is lent in return for a yield paid by the borrower. The borrower has to lock up a greater amount of collateral than the value of the loan to incentivize the repayment of the loan.

|Risk|Description|
|----|-----------|
|Governance|Admin key holders change lending protocol adversely, e.g. change the interest rate model in such a way that discourages borrowing|
|Technological|Smart contract risk of interacting with lending protocols|
|Market|Low demand for borrowing the asset causes low lending yields|
||Collateral price falls causing the lending protocol to become undercollateralized |
||Lent assets become unavailable to withdraw because the utilization ratio becomes too high|
|Operational|Delays or inability to withdraw assets from the lending protocol in an emergency|

## Liquidity Mining

Liquidity mining involves interacting with a protocol to earn the protocol’s native tokens. The interaction can be as simple as staking an asset in a protocol’s staking contract, or more complicated such as staking SNX to mint sUSD in Synthetix to earn SNX rewards.

In most cases the liquidity mined token is exchanged for the Want token on an AMM.


|Risk|Description|
|----|-----------|
|Governance|Admin key holders change protocol adversely, e.g. introduce penalties for withdrawals|
|Technological|Smart contract risk of rewards contract|
||Smart contract risk of AMM used to exchange the liquidity mined token for the Want token|
|Market|Fall in price of token being farmed|
||Liquidity of liquidity mined token on AMM is reduced or removed|
|Operational Risk|Delays or inability to withdraw liquidity in an emergency|

The [Safe Farming Committee](https://gov.yearn.finance/t/introducing-yearn-safe-farming-committee/10533) decides which protocols are secure.

## Trading Fees

Trading fees are earned in Automated Market Makers (AMMs) by providing liquidity.


|Risk|Description|
|----|-----------|
|Governance|Admin key holders change protocol adversely, e.g. reduce rewards paid to liquidity providers|
|Technological|Smart contract risk of AMM (e.g. Curve Finance, Sushiswap or Uniswap)|
|Market|Trading volumes reduce leading to lower fees|
||Impermanent loss](https://academy.binance.com/en/articles/impermanent-loss-explained) due to the pool’s token prices changing relative to each other|
|Operational Risk|Delays or inability to withdraw liquidity from the AMM in an emergency|

## Leverage

|Risk|Description|
|----|-----------|
|Governance|Admin key holders change the lending protocol adversely|
|Technological|Smart contract risk of lending protocol (Aave, Compound Finance, Maker, Unit protocol)|
|Market|Risk that the debt is liquidated due to a price fall|
||Risk that income is lower than the cost of the flash loan|
|Oracle|Incorrect price feed|
||liquidation penalties|
|Operational Risk|Operational risk of managing debt positions
|


## Strategy Scoring System

[Initial attempt](https://docs.google.com/document/d/18M2eJNsshKJlIAD_dSVGfMvTkIgZYJzXjT538QSmALo/edit?usp=sharing) at a strategy scoring system.
