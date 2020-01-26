# Getting Started

{% hint style="info" %}
These docs are still being worked on.
{% endhint %}

With the onset of DeFi numerous strategies exist for the investor. To list just a few;

* Lend out ETH in Compound.
* Swap ETH to USDC and lend on Aave.
* Be a liquidity provider for ETH/USDC on Uniswap.

The possible strategies are an exhaustive list.

* Do you trade your ETH to DAI and invest in DSR?
* Do you go 2x long ETH on dYdX and take 50% to DAI swapped to cDAI and then 25%/25% into Uniswap cDAI/ETH liquidity?
* Do you hedge your cDAI into cUSDC and be an LP for curve.fi?

The list of possibilities and analytics becomes far too numerous to manage.

To address the above concerns we developed iearn.finance

iearn.finance is a set of protocols with simplicity in mind. You provide the asset you wish to earn on, swap it for it's representative token (ETH to iETH), and the underlying ETH will be invested based on the current most optimal strategy. This engine is not simplistically a rates aggregator that then puts your ETH into Fulcrum, because it has the highest rate. Instead it analyzes strategies across different spheres. It takes into consideration pool liquidity in Uniswap, and if there might be a better strategy for fees since this is a hedged position. It will look for swap oppurtunities between multiple exchanges for the least amount of slippage.

iearn is an open source protocol. There is no central token or platform fee. No bias towards any investor. Strategies can be added in an open and free manner. All smart contract functions are public.

## Features

* Add support for dYdx, Compound, Aave, and Fulcrum [APR](https://github.com/iearn-finance/apr-oracle/blob/master/contracts/APROracle.sol)
* Swap between ETH and any asset via on-chain dex aggregators for minimum [slippage](https://github.com/iearn-finance/zap/blob/master/contracts/UniSwap_ETH_cDAI.sol)
* [Uniswap liquidity provider strategy](https://github.com/iearn-finance/zap/blob/master/contracts/UniSwap_ETH_cDAI.sol)
* [ETH to DAI into aprDAI strategy](https://github.com/iearn-finance/zap/blob/master/contracts/UniSwap_ETH_cDAI.sol)
* [aprDAI into DAI into ETH strategy](https://github.com/iearn-finance/zap/blob/master/contracts/UniSwap_ETH_cDAI.sol)
* [issue](https://github.com/iearn-finance/itoken/blob/master/contracts/IEther.sol) representative interest token on invest
* [shares pool calculation](https://github.com/iearn-finance/itoken/blob/master/contracts/IEther.sol)
* [shares redemption strategy](https://github.com/iearn-finance/itoken/blob/master/contracts/IEther.sol)
* [pool value calculation](https://github.com/iearn-finance/itoken/blob/master/contracts/IEther.sol)

## Resources

* [Website](https://iearn.finance)
* [Github](https://github.com/iearn-finance)

## How it works

The TLDR is a tokenized interest pool that optimizes on-chain investments strategies.

Or simplistically put, invest ETH get iETH, iETH accrues interest. iETH is a normal token.

The system does a the following;

Get pools with best liquidity rates on Uniswap (Adding additional pool support as well, but for now just uniswap supported).

See which pool tokens have the highest rate of return including their own interest rates (so factoring on iDAI vs cDAI vs aDAI vs dDAI).

After the decision tree, splits the investment (ETH) 50/50, compares trade rates at Uniswap, Kyber, Multiswap, Paraswap, Maker, 0x, Airswap, Oasis for the best swap rate with least amount of slippage. Swap that portion of ETH for DAI. Deposits the DAI into Fulcrum, dYdX, Compound, or Aave dependent on best rates, deposit the ETH/cDAI (for example) pair into Uniswap.

Additional strategies; 2x long ETH on dYdX for 100% ETH exposure, CompoundSwap system that trades between iETH/cDAI, or iDAI/cETH etc which uses itself as a first line vendor and falls through to the on-chain aggregated engine as a second line support. Reasoning for this is to use cETH/iETH as well in the pool swap instead of just 50% ETH to add the ETH rewards ontop as well.

Here is an example of the [invest strategy](https://etherscan.io/tx/0x7e7fa4fe01bba24ee2383386c3804ed8ee79c1ed787b8177aa9c963cd489b355)

Here is an example of the [redeem strategy](https://etherscan.io/tx/0x3854a62e3026c9f559b92e9c9b15393a2228ae0f359c6a20d479d2f0e3aa0b93)

[Contract code](https://etherscan.io/address/0x9dde7cdd09dbed542fc422d18d89a589fa9fd4c0#code)

Simple [metamask interface](https://iearn.finance/)

## How to use it

[iearn.finance](https://iearn.finance)
