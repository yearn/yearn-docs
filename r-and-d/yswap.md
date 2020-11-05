---
description: Not recommended for retail use
---

# ySwap

## Aperçu

[ySwap](https://yswap.exchange/) est actuellement en phase de test et n'est pas disponible pour une utilisation générale. Il s'agit d'un market maker automatisé \(AMM = automated market maker\) permettant une liquidité unilatérale et une atténuation des pertes impermanentes \(IL = impermanent loss \). ySwap crée des pools de trading décentralisés \(similaires à Uniswap\), dans lesquels les traders peuvent acheter ou vendre. De plus, les utilisateurs peuvent fournir de la liquidité en utilisant un seul jeton, alors que sur Uniswap, ils auraient besoin des deux jetons dans la pool avec un ratio 50/50. Cela supprime les barrières à l'entrée pour les fournisseurs de liquidité potentiels qui peuvent ne pas avoir les deux jetons d'une pool. Les jetons suivants peuvent être échangés:

* **wrapped BTC:** renBTC, wBTC, sBTC
* **AAVE tokens:** aBTC, aLEND, aMKR, aMANA, aKNC, aLINK, aUSDC, aREP, aZRX, aBAT, aDAI, aTUSD, aUSDT, aBUSD, aSUSD, aSNX
* **Standard ERC-20s:** LEND, MKR, MANA, KNC, LINK, USDC, REP, ZRX, BAT, DAI, TUSD, USDT, BUSD, SUSD, SNX,
* **Synthetix tokens:** sAUD, sEUR, sCHF, sGBP, sJPY, sXAG, sXAU

## Mécanique

aUSD is immediately minted when a user deposits into one of the ySwap AMM pools. aUSD is a synthetic stablecoin that is pegged to the price of $1. The amount of aUSD minted depends on the market value of the asset deposited. Market prices are provided by [Chainlink](https://chain.link/)'s decentralized oracles, therefore only coins with [Chainlink price feeds](https://feeds.chain.link/) are eligible to be traded. A list of the current price feeds supported by Chainlink oracles can be found [here](https://feeds.chain.link/).

Immediately after deposit, the deposited token and aUSD are added to the ySwap pool, and the depositor receives a LP token in return, representing his or her share of the pool. Traders make trades using the [ySwap interface](https://yswap.exchange/).

_If a trader desires to sell aLINK for aLEND the following steps will occur:_

* The interface will deposit the trader's aLINK into the ySwap LINK pool;
* The dollar amount of the aLINK, at the time of trade, is made using the aUSD to the aLEND pool;
* ySwap sends the amount of aLEND purchased to the trader.

The AMM is a constant product market maker \(CPMM\) and uses a bonding curve, similar in design to Uniswap. If the dollar value of the asset increases, depositors will receive the full amount of the deposit back. If the dollar value of the asset decreases, depositors will receive the full amount of the deposit back plus an additional amount in aUSD. This additional aUSD amount is meant to compensate liquidity providers for exposure to impermanent loss, which occurs during volatile price changes of assets.

