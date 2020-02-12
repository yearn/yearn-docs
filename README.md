# Getting Started

{% hint style="info" %}
These docs are still being worked on.
{% endhint %}

## What is it?

The purpose of [iearn.finance](https://iearn.finance) is very simple. Yield aggregator for lending platforms that rebalances for highest yield whenever the contract is interacted with.

Full documentation available [docs.iearn.finance](http://docs.iearn.finance/)

The system currently supports;

$DAI  
$USDC  
$USDT  
sUSD  
[DAI-USDC](https://www.curve.fi/)  
wBTC  
$ETH  

Upcoming support for $BAT, $KNC, $LINK, $MKR, $REP, $SNX, $ZRX.

The system current aggregates;

[Compound](http://compound.finance/)  
[Fulcrum](https://fulcrum.trade/)  
[dYdX](http://dydx.exchange/)  
[Aave](http://aave.com/)  

Pending integration for [DDEX](https://ddex.io/) and [LENDF](https://www.lendf.me/).

## Comparative products

Similar services in this space include staked.us [RAY](https://staked.us/v/robo-advisor-yield), [idleDAI](http://idle.finance/), [topo](https://topo.finance/) (not yet launched), and metamoneymarkets (not yet launched).

## Why build it?

The system simplifies the user journey so that the #DeFi investor does not have to worry about the underlying protocols, yield hunting or understanding complex #DeFi strategies.

It simplifies complex strategies like being an LP provider to [Uniswap](https://uniswap.io/) (via iETH) or depositing DAI into cDAI with swap from cDAI to cUSDC and into [Curve](https://www.curve.fi/), a strategy example [docs.iearn.finance](http://docs.iearn.finance/)

When comparing interest, it also considers LP opportunities with the underlying token protocol, so it won’t just compare [iDAI](https://fulcrum.trade/) with [cDAI](http://compound.finance/), but also weigh up how much APR is possible by being an LP for ETH/cDAI and adjusts the cDAI performance based on this calculation.

## Anything else?

The system is built out of different mini components (heavily inspired by [DeFi_Zap](https://defizap.com/)) that are usable and composable on-chain, such as APR aggregators, recommendation decision trees, or just interfaces. Full documentation registry and interfaces available [docs.iearn.finance](http://docs.iearn.finance/)

## Detailed Introduction

With the onset of DeFi numerous strategies exist for the investor. To list just a few;

* Lend out ETH in Compound.
* Swap ETH to USDC and lend on Aave.
* Be a liquidity provider for ETH/USDC on Uniswap.

The possible strategies are an ever increasing list.

* Do you trade your ETH to DAI and invest in DSR?
* Do you go 2x long ETH on dYdX and take 50% to DAI swapped to cDAI and then 25%/25% into Uniswap cDAI/ETH liquidity?
* Do you hedge your cDAI into cUSDC and be an LP for curve.fi?

The list of possibilities and analytics becomes far too numerous to manage.

To address the above concerns we developed [iearn.finance](https://iearn.finance)

[iearn.finance](https://iearn.finance) is a set of protocols with simplicity in mind. You provide the asset you wish to earn on, swap it for it's representative token (ETH to iETH), and the underlying ETH will be invested based on the current most optimal strategy. This engine is not a rates aggregator that then puts your ETH into Fulcrum, because it has the highest rate. Instead it analyzes strategies across different spheres. It takes into consideration pool liquidity in Uniswap, and if there might be a better strategy for fees since this is a hedged position. It will look for swap opportunities between multiple exchanges for the least amount of slippage.

[iearn.finance](https://iearn.finance) is an open source protocol. There is no central token or platform fee. No bias towards any investor. Strategies can be added in an open and free manner. All smart contract functions are public.

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

## Features 27-01-2020

* Add support for [Chai](https://chai.money/) as an option
* Completed [uniroi.iearn.eth](https://etherscan.io/address/0xd04ca0ae1cd8085438fdd8c22a76246f315c2687#readContract) and liquidity considerations
* Completed [uniapr.iearn.eth](https://etherscan.io/address/0x4c70D89A4681b2151F56Dc2c3FD751aBb9CE3D95#readContract) for APR considerations
* Added [walkthrough example](https://docs.iearn.finance/walkthrough)

## Features 31-01-2020

* Invest / Redeem ZAP for [Compound](http://compound.finance), [Fulcrum](https://fulcrum.trade/), [Aave](http://aave.com/), and [dYdX](http://dydx.exchange/)
* Completed [iapr.iearn.eth](https://etherscan.io/address/0x9cad8ab10daa9af1a9d2b878541f41b697268eec#readContract) for on-chain APR decision trees
* Completed [imanage.iearn.eth](https://etherscan.io/address/0x318135fbd0b40d48fcef431ccdf6c7926450edfb#readContract) for on-chain stateless execution
* Added support for [DAI](https://etherscan.io/address/0x9d25057e62939d3408406975ad75ffe834da4cdd#readContract)
* Added support for [USDT](https://etherscan.io/address/0xa1787206d5b1bE0f432C4c4f96Dc4D1257A1Dd14)
* Added support for [USDC](https://etherscan.io/address/0xa2609b2b43ac0f5ebe27deb944d2a399c201e3da)
* Added support for [SUSD](https://etherscan.io/address/0x36324b8168f960A12a8fD01406C9C78143d41380)

## Features 03-02-2020

* Support for [DDEX](https://ddex.io/) in [apradj.iearn.eth](https://etherscan.io/address/0x0daea70A07883DDC4a0D9ECF7BcF550F92e9CDA6#code)
* Support for [LENDF](https://www.lendf.me/) in [apradj.iearn.eth](https://etherscan.io/address/0x0daea70A07883DDC4a0D9ECF7BcF550F92e9CDA6#code)
* Added support for [wBTC](https://etherscan.io/address/0x04ef8121ad039ff41d10029c91ea1694432514e9)
* Added support for Ledger
* Support for [DDEX](https://ddex.io/) in [iapradj.iearn.eth](https://etherscan.io/address/0xcD5F61c392B61F440991DEf98FF6Af07FC6900D4#readContract)
* Support for [LENDF](https://www.lendf.me/) in [iapradj.iearn.eth](https://etherscan.io/address/0xcD5F61c392B61F440991DEf98FF6Af07FC6900D4#readContract)

## Features 12-02-2020

* Added yDAI v2 upgrades [ydaiv2.iearn.eth](https://etherscan.io/address/0xF86D55A3C6d93E77977b5Ece9Ff66E45F98ee982#readContract)
* Added yUSDC v2 upgrades [yusdcv2.iearn.eth](https://etherscan.io/address/0xd6aD7a6750A7593E092a9B218d66C0A814a3436e)
* Added yUSDT v2 upgrades [yusdtv2.iearn.eth](https://etherscan.io/address/0x83f798e925BcD4017Eb265844FDDAbb448f1707D)\
* Added ySUSD v2 upgrades [ysusdv2.iearn.eth](https://etherscan.io/address/0xF61718057901F84C4eEC4339EF8f0D86D2B45600)
* Reduced gas costs from 1.5MM to 250k for withdraw & deposit

## Resources

* [Website](https://iearn.finance)
* [Github](https://github.com/iearn-finance)

## How to use it

[iearn.finance](https://iearn.finance)
