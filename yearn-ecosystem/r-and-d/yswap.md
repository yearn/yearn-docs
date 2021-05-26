---
description: Not recommended for retail use
---

# ySwap

## Overview

[ySwap](https://yswap.exchange/) is currently in the testing phase and not available for general use. It's an automated market maker \(AMM\) enabling single-sided liquidity and impermanent loss \(IL\) mitigation. ySwap creates decentralized trading pools \(similar to Uniswap\), which traders can buy or sell from. Additionally, users can provide liquidity using only one token, whereas on Uniswap they would need both tokens in the pool at a 50/50 ratio. This removes barriers of entry for potential liquidity providers who may not have both tokens in a pool. The following tokens are available to be traded:

- **wrapped BTC:** renBTC, wBTC, sBTC
- **AAVE tokens:** aBTC, aLEND, aMKR, aMANA, aKNC, aLINK, aUSDC, aREP, aZRX, aBAT, aDAI, aTUSD, aUSDT, aBUSD, aSUSD, aSNX
- **Standard ERC-20s:** LEND, MKR, MANA, KNC, LINK, USDC, REP, ZRX, BAT, DAI, TUSD, USDT, BUSD, SUSD, SNX,
- **Synthetix tokens:** sAUD, sEUR, sCHF, sGBP, sJPY, sXAG, sXAU

## Mechanics

aUSD is immediately minted when a user deposits into one of the ySwap AMM pools. aUSD is a synthetic stablecoin that is pegged to the price of \$1. The amount of aUSD minted depends on the market value of the asset deposited. Market prices are provided by [Chainlink](https://chain.link/)'s decentralized oracles, therefore only coins with [Chainlink price feeds](https://feeds.chain.link/) are eligible to be traded. A list of the current price feeds supported by Chainlink oracles can be found [here](https://feeds.chain.link/).

Immediately after deposit, the deposited token and aUSD are added to the ySwap pool, and the depositor receives a LP token in return, representing his or her share of the pool. Traders make trades using the [ySwap interface](https://yswap.exchange/).

_If a trader desires to sell aLINK for aLEND the following steps will occur:_

- The interface will deposit the trader's aLINK into the ySwap LINK pool;
- The dollar amount of the aLINK, at the time of trade, is made using the aUSD to the aLEND pool;
- ySwap sends the amount of aLEND purchased to the trader.

The AMM is a constant product market maker \(CPMM\) and uses a bonding curve, similar in design to Uniswap. If the dollar value of the asset increases, depositors will receive the full amount of the deposit back. If the dollar value of the asset decreases, depositors will receive the full amount of the deposit back plus an additional amount in aUSD. This additional aUSD amount is meant to compensate liquidity providers for exposure to impermanent loss, which occurs during volatile price changes of assets.
