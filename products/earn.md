# Earn

Earn is a lending aggregator that strives to attain the highest yield for supported coins \(DAI, USDC, USDT, TUSD, sUSD, or wBTC\) at all times. It does this by programmatically shifting these coins between several lending protocols \([AAVE](https://aave.com), [dYdX](https://dydx.exchange/), and [Compound](https://compound.finance)\) operating on the Ethereum blockchain.

For example, a user can deposit DAI into the Earn yDAI pool. Yearn will programmatically deposit DAI into one of three lending protocols \(AAVE, dYdX, Compound\). Yearn will withdraw from one protocol and deposit to another automatically as interest rates change between protocols. As a result, the user will receive the optimal interest rate on his or her DAI deposit at all times.

![](https://i.imgur.com/jLlg0WU.png)

Earn is a key component of the yPool at Curve.Finance, which represents a basket of four yTokens: yDai, yUSDC, yUSDT, and yTUSD. The underlying four yTokens are constantly optimizing to yield the highest available interest in the market \(described above\), while also serving as a liquidity pool for these tokens. Users can interact with this pool to swap between any of the four tokens with little slippage. Therefore, liquidity providers of the yPool receive the optimized interest rates on their stablecoin deposits and trading fees from users swapping tokens from the pool.

As of September 2020, the YTD annualized return for yPool liquidity providers is estimated to be 9.11%. Since yDAI+yUSD+yUSDT+yTUSD is a continuously accruing interest-bearing token, its price is above \$1 and is constantly increasing.

![](https://i.imgur.com/U4KcWyE.png)

## Resources

- [Earn Homepage](https://yearn.finance/earn)
