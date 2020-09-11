## Features

- Add support for dYdx, Compound, Aave, and Fulcrum [APR](https://github.com/iearn-finance/apr-oracle/blob/master/contracts/APROracle.sol)
- Swap between ETH and any asset via on-chain dex aggregators for minimum [slippage](https://github.com/iearn-finance/zap/blob/master/contracts/UniSwap_ETH_cDAI.sol)
- [Uniswap liquidity provider strategy](https://github.com/iearn-finance/zap/blob/master/contracts/UniSwap_ETH_cDAI.sol)
- [ETH to DAI into aprDAI strategy](https://github.com/iearn-finance/zap/blob/master/contracts/UniSwap_ETH_cDAI.sol)
- [aprDAI into DAI into ETH strategy](https://github.com/iearn-finance/zap/blob/master/contracts/UniSwap_ETH_cDAI.sol)
- [issue](https://github.com/iearn-finance/itoken/blob/master/contracts/IEther.sol) representative interest token on invest
- [shares pool calculation](https://github.com/iearn-finance/itoken/blob/master/contracts/IEther.sol)
- [shares redemption strategy](https://github.com/iearn-finance/itoken/blob/master/contracts/IEther.sol)
- [pool value calculation](https://github.com/iearn-finance/itoken/blob/master/contracts/IEther.sol)

## Features 27-01-2020

- Add support for [Chai](https://chai.money/) as an option
- Completed [uniroi.iearn.eth](https://etherscan.io/address/0xd04ca0ae1cd8085438fdd8c22a76246f315c2687#readContract) and liquidity considerations
- Completed [uniapr.iearn.eth](https://etherscan.io/address/0x4c70D89A4681b2151F56Dc2c3FD751aBb9CE3D95#readContract) for APR considerations
- Added [walkthrough example](https://docs.iearn.finance/walkthrough)

## Features 31-01-2020

- Invest / Redeem ZAP for [Compound](http://compound.finance), [Fulcrum](https://fulcrum.trade/), [Aave](http://aave.com/), and [dYdX](http://dydx.exchange/)
- Completed [iapr.iearn.eth](https://etherscan.io/address/0x9cad8ab10daa9af1a9d2b878541f41b697268eec#readContract) for on-chain APR decision trees
- Completed [imanage.iearn.eth](https://etherscan.io/address/0x318135fbd0b40d48fcef431ccdf6c7926450edfb#readContract) for on-chain stateless execution
- Added support for [DAI](https://etherscan.io/address/0x9d25057e62939d3408406975ad75ffe834da4cdd#readContract)
- Added support for [USDT](https://etherscan.io/address/0xa1787206d5b1bE0f432C4c4f96Dc4D1257A1Dd14)
- Added support for [USDC](https://etherscan.io/address/0xa2609b2b43ac0f5ebe27deb944d2a399c201e3da)
- Added support for [SUSD](https://etherscan.io/address/0x36324b8168f960A12a8fD01406C9C78143d41380)

## Features 03-02-2020

- Support for [DDEX](https://ddex.io/) in [apradj.iearn.eth](https://etherscan.io/address/0x0daea70A07883DDC4a0D9ECF7BcF550F92e9CDA6#code)
- Support for [LENDF](https://www.lendf.me/) in [apradj.iearn.eth](https://etherscan.io/address/0x0daea70A07883DDC4a0D9ECF7BcF550F92e9CDA6#code)
- Added support for [wBTC](https://etherscan.io/address/0x04ef8121ad039ff41d10029c91ea1694432514e9)
- Added support for Ledger
- Support for [DDEX](https://ddex.io/) in [iapradj.iearn.eth](https://etherscan.io/address/0xcD5F61c392B61F440991DEf98FF6Af07FC6900D4#readContract)
- Support for [LENDF](https://www.lendf.me/) in [iapradj.iearn.eth](https://etherscan.io/address/0xcD5F61c392B61F440991DEf98FF6Af07FC6900D4#readContract)

## Features 12-02-2020

- Added yDAI v2 upgrades [ydaiv2.iearn.eth](https://etherscan.io/address/0x16de59092dAE5CcF4A1E6439D611fd0653f0Bd01#readContract)
- Added yUSDC v2 upgrades [yusdcv2.iearn.eth](https://etherscan.io/address/0xd6aD7a6750A7593E092a9B218d66C0A814a3436e)
- Added yUSDT v2 upgrades [yusdtv2.iearn.eth](https://etherscan.io/address/0x83f798e925BcD4017Eb265844FDDAbb448f1707D)
- Added ySUSD v2 upgrades [ysusdv2.iearn.eth](https://etherscan.io/address/0xF61718057901F84C4eEC4339EF8f0D86D2B45600)
- Added yTUSD v2 upgrades [ytusdv2.iearn.eth](https://etherscan.io/address/0x73a052500105205d34daf004eab301916da8190f)
- Added yWBTC v2 upgrades [ybtcv2.iearn.eth](https://etherscan.io/address/0x04Aa51bbcB46541455cCF1B8bef2ebc5d3787EC9#readContract)
- Reduced gas costs from 1.5MM to 250k for withdraw & deposit

## Features 16-02-2020

- Added to [duneanalytics.com](https://www.duneanalytics.com/) dashboards
- Integrated [renproject.io](https://renproject.io/)
- Curve Finance yToken pool deployed to [y.curve.fi](https://y.curve.fi/)
- Added [Nexus Mutual](https://app.nexusmutual.io/#/SmartContractCover) cover for [iearn.finance](http://iearn.finance/) and [y.curve.fi](https://y.curve.fi/)
- [paraswap.io](https://paraswap.io/#/DAI-TUSD/1000) integrates [y.curve.fi](https://y.curve.fi/)
- [defisnap.io](https://www.defisnap.io/) included v2 yTokens
- [0x](https://0x.org/) integrates [y.curve.fi](https://y.curve.fi/)

## Features 22-02-2020

- Added [Zap In](https://twitter.com/iearnfinance/status/1229362220297080832) into [y.curve.fi](https://y.curve.fi/)
- Added [Swap](https://twitter.com/iearnfinance/status/1229362220297080832) for usdt.curve.fi and compound.curve.fi pools to [y.curve.fi](https://y.curve.fi/)
- Added [Zap Out](https://twitter.com/iearnfinance/status/1229362220297080832) from [y.curve.fi](https://y.curve.fi/)
- [1inch.exchange](https://1inch.exchange/) integration
- [defipulse.com](http://defipulse.com/) integration
- [pools.fyi](http://pools.fyi/) integration
- Full comprehensive cover launched with [opyn.co](http://opyn.co/)
