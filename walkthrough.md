## walkthrough

{% hint style="info" %}
These docs are still being worked on.
{% endhint %}

## iearn.finance

You want to invest 1 ETH.

The system starts by collecting the APR rates from [Compound](http://compound.finance), [Fulcrum](https://fulcrum.trade/), [Aave](http://aave.com/), [dYdX](http://dydx.exchange/) and [Chai](https://chai.money/). This is achieved via [apr.iearn.eth](https://etherscan.io/address/0x97ff4a1b787ade6b94cca95b61f79417c673331d#readContract)

This gives the following rates;

| Token | APR   |
| ----- | ----- |
| cDAI  | 7.54% |
| cBAT  | 0.32% |
| cETH  | 0.02% |
| cREP  | 0.01% |
| cUSDC | 3.53% |
| cWBTC | 1.80% |
| cZRC  | 0.22% |
| dETH  | 0.02% |
| dUSDC | 3.79% |
| dDAI  | 5.72% |
| iZRX  | 0.16% |
| iKNC  | 0.03% |
| iWBTC | 1.19% |
| iUSDC | 3.86% |
| iETH  | 0.44% |
| iDAI  | 7.82% |
| iLINK | 2.93% |
| iSUSD | 3.91% |
| aDAI  | 8.67% |
| aTUSD | 9.10% |
| aUSDC | 4.66% |
| aUSDT | 8.06% |
| aSUSD | 3.75% |
| aBAT  | 0.03% |
| aETH  | 0.16% |
| aLINK | 0.01% |
| aKNC  | 0.01% |
| aREP  | 1.45% |
| aSNX  | 1.53% |
| CHAI  | 7.50% |

Our goal is to grow our ETH investment in ETH. So we are only interested in direct investments (ETH into cETH vs iETH vs dETH vs aETH) or hedged pool positions (ETH/cDAI) where the 50% growth would be greater than the net gain on ETH.

For example; 1 ETH + 0.03% or 0.5 ETH + 6% + 0.5 ETH (hedged).

So next consideration are uniswap pools with sufficient liquidity. We will only consider pools with greater than 50 ETH liquidity.

We get the liquidity via [uniroi.iearn.eth](https://etherscan.io/address/0xd04ca0ae1cd8085438fdd8c22a76246f315c2687#readContract). After collecting the qualifying pools, we need to get their current APR to adjust to our model, we collect this from [uniapr.iearn.eth](https://etherscan.io/address/0x4c70D89A4681b2151F56Dc2c3FD751aBb9CE3D95#readContract), the results as follows;

| Token | APR   | UniROI  |
| ----- | ----- | ------- |
| cDAI  | 7.54% | -17.46% |
| cBAT  | 0.32% |         |
| cETH  | 0.02% | 0.38%   |
| cREP  | 0.01% |         |
| cUSDC | 3.53% |         |
| cWBTC | 1.80% |         |
| cZRC  | 0.22% |         |
| dETH  | 0.02% |         |
| dUSDC | 3.79% |         |
| dDAI  | 5.72% |         |
| iZRX  | 0.16% |         |
| iKNC  | 0.03% |         |
| iWBTC | 1.19% |         |
| iUSDC | 3.86% |         |
| iETH  | 0.44% |         |
| iDAI  | 7.82% |         |
| iLINK | 2.93% |         |
| iSUSD | 3.91% |         |
| aDAI  | 8.67% |         |
| aTUSD | 9.10% |         |
| aUSDC | 4.66% |         |
| aUSDT | 8.06% |         |
| aSUSD | 3.75% |         |
| aBAT  | 0.03% |         |
| aETH  | 0.16% |         |
| aLINK | 0.01% |         |
| aKNC  | 0.01% |         |
| aREP  | 1.45% |         |
| aSNX  | 1.53% |         |
| CHAI  | 7.50% | -7.57%  |
| sETH  | 0.00% | 1.1%    |
| MKR   | 0.00% | 1.6%    |
| REP   | 0.00% | 3.8%    |
| DAI   | 0.00% | 5.2%    |
| SNX   | 0.00% | -2.8%   |
| sETH  | 0.00% | 1.1%    |
| KNC   | 0.00% | 2.7%    |
| sUSD  | 0.00% | 2.3%    |
| ZRX   | 0.00% | 9.1%    |

We use uniswap pairs to hedge, so this means currently with the supported set, the following options are available to us;

| Token | APR   | UniROI  | Net    |
| ----- | ----- | ------- | ------ |
| cDAI  | 7.54% | -17.46% | -9.92% |
| cETH  | 0.02% | 0.38%   | 0.4%   |
| dETH  | 0.02% |         | 0.02%  |
| iETH  | 0.44% |         | 0.44%  |
| aETH  | 0.16% |         | 0.16%  |
| CHAI  | 7.50% | -7.57%  | -0.07% |
| sETH  | 0.00% | 1.1%    | 1.1%   |
| MKR   | 0.00% | 1.6%    | 1.6%   |
| REP   | 0.00% | 3.8%    | 3.8%   |
| DAI   | 0.00% | 5.2%    | 5.2%   |
| SNX   | 0.00% | -2.8%   | -2.8%  |
| sETH  | 0.00% | 1.1%    | 1.1%   |
| KNC   | 0.00% | 2.7%    | 2.7%   |
| sUSD  | 0.00% | 2.3%    | 2.3%   |

Leaving the current best strategy as a liquidity provider for ETH/DAI at 5.2%

So we collect quotes for 50% of the ETH via [1split.eth](https://etherscan.io/address/1split.eth#code), compare the net result of slippage and fees to see if 5.2% is still higher than our runner up of 3.8%. And if yes, we transfer 50% of the ETH to DAI and become an LP for the ETH/DAI pool.
