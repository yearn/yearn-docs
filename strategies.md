## strategies

{% hint style="info" %}
These docs are still being worked on.
{% endhint %}

## 1split.eth

[1split.eth](https://etherscan.io/address/1split.eth#code) is an on-chain dex aggregator developed by [1inch.exchange](https://1inch.exchange/). The contract allows on-chain quotes and swaps between all ERC20 assets from MultiSwap, Oasis, 0x, Kyber, Uniswap, Synthetix, Synth Depot, Bancor, Airswap, and Curve.fi.

This allows [iearn.finance](https://iearn.finance) to aggregate the best rates on-chain without any slippage for token swaps, when trying to determine the value in the strategy. The quote functionality is used to determine slippage and to calculate that into the overall strategy.

## apr.iearn.eth

[apr.iearn.eth](https://etherscan.io/address/0x97ff4a1b787ade6b94cca95b61f79417c673331d#code) is an on-chain defi rate aggregator. The contract allows on-chain rate comparison between [Compound](http://compound.finance), [Fulcrum](https://fulcrum.trade/), [Aave](http://aave.com/), and [dYdX](http://dydx.exchange/).

This allows real time comparison of highest returning yields across multiple platforms for all supported tokens.

## uniroi.iearn.eth

[uniroi.iearn.eth](https://etherscan.io/address/0xd04ca0ae1cd8085438fdd8c22a76246f315c2687#readContract) is an on-chain uniswap pool ROI calculator. It calculates all values in ETH the duration of the pool existence.

The ROI is required for snapshots to be able to get 30 day, 7 day, or APR averages.

## uniapr.iearn.eth

[uniapr.iearn.eth](https://etherscan.io/address/0x4c70D89A4681b2151F56Dc2c3FD751aBb9CE3D95#readContract) is an on-chain uniswap pool APR calculator. It calculates all values in ETH adjusted for the last year.

## defizap.eth

- ETH split via [1split.eth](https://etherscan.io/address/1split.eth#code) into wBTC and ETH. wBTC deposited into iWBTC. Uniswap liquidity for iWBTC/ETH. [wBTCUnipool.DeFiZap.eth](https://defizap.com/zaps/unipoolwbtc) [4.21%](https://pools.fyi/#/returns/0x4d2f5cfba55ae412221182d8475bc85799a5644b)
- ETH split via [1split.eth](https://etherscan.io/address/1split.eth#code) into sETH and ETH. Uniswap liquidity for sETH/ETH [sETHUnipool.DeFiZap.eth](https://defizap.com/zaps/unipoolseth) [1.75%](https://pools.fyi/#/returns/0xe9cf7887b93150d4f2da7dfc6d502b216438f244)
- ETH split via [1split.eth](https://etherscan.io/address/1split.eth#code) into DAI and ETH. DAI deposited into [Chai](https://chai.money/). Uniswap liquidity for CHAI/ETH. [CHAIUnipool.DeFiZap.eth](https://defizap.com/zaps/unipoolchai) [-5.25%](https://pools.fyi/#/returns/0x6c3942b383bc3d0efd3f36efa1cbe7c8e12c8a2b?period=30)
- ETH split via [1split.eth](https://etherscan.io/address/1split.eth#code) into DAI and ETH. DAI deposited in [cDAI](https://compound.finance/). Uniswap liquidity for cDAI/ETH [cDAIPool.DeFiZap.eth](https://defizap.com/zaps/unipoolcdai) [4.79%](https://pools.fyi/#/returns/0x34E89740adF97C3A9D3f63Cc2cE4a914382c230b?period=30)

## uniswap.exchange

Uniswap is an on-chain liquidity pool for cross ERC20/ETH swaps. It allows ERC20 to ERC20 via double swaps involving ERC20 to ETH and ETH to ERC20. Fees are 0.3% per swap. These fees are rewarded to liquidity providers.

[pools.fyi](https://pools.fyi/#/) shows pool ROI per pair

## iearn.eth

[iearn.finance](https://iearn.finance) is a combination of these strategies. It analyzes the asset you want to invest and the highest returning strategy for it. So for ETH, it would analyze ETH vs cETH vs iETH vs aETH vs dETH. It would add % slippage as an adjusted result to offset the APR. After which it will calculate the highest volume pools that match the tokens. These strategies can be as simple as ETH into Compound, or as complex as ETH split to ETH/DAI, DAI into cDAI, and ETH/cDAI into Uniswap.

This is what the [iearn.finance] protocol does.

## iETH shares

We start from a fresh pool 0 balance.

1 ETH is deposited. 1 iETH is minted. At this point 1 ETH = 1 iETH.

We have the following metrics;

| Pool  | Shares |
| ----- | ------ |
| 1 ETH | 1 iETH |

+1 ETH is deposited. 1 iETH is minted.

| Pool  | Shares |
| ----- | ------ |
| 2 ETH | 2 iETH |

1 iETH can claim 1 ETH.

The pool increases interest by 10%.

| Pool    | Shares | Value   |
| ------- | ------ | ------- |
| 2.2 ETH | 2 iETH | 1.1 ETH |

Now 1 iETH = 1.1 ETH

+1 ETH is deposited. 0.91 iETH is minted.

The reason for this is that iETH functions as a % of shares of the pool.

In this case;

```
value(1 ETH) * total shares (2 iETH) / pool (2.2 ETH)

1 * 2 / 2.2

0.91 iETH

This iETH is worth 0.909 / total shares (2.91) * pool (3.2)

1 ETH.
```

So as the pool value increases over time, the ratio of ETH to iETH will decouple. But the value of ETH that iETH can claim increases.
