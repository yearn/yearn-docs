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

Du aUSD est immédiatement généré \(mint\) lorsqu'un utilisateur dépose dans l'une des pools AMM ySwap. Le aUSD est un stablecoin synthétique qui est indexé au prix de 1 $. Le montant d'AUSD frappé dépend de la valeur marchande de l'actif déposé. Les prix du marché sont fournis par les oracles décentralisés de [Chainlink](https://chain.link/), par conséquent, seules les pièces avec des "[price feeds" Chainlink ](https://feeds.chain.link/)peuvent être échangées. Une liste des flux de prix actuels pris en charge par les oracles Chainlink peut être trouvée [ici](https://feeds.chain.link/).

Immédiatement après le dépôt, le token déposé et un USD sont ajoutés au pool ySwap, et le déposant reçoit en retour un token LP, représentant sa part du pool. Les traders effectuent des transactions en utilisant [l'interface ySwap.](https://yswap.exchange/)

_Si un trader souhaite  échanger du aLINK pour du aLEND les étapes suivantes seront réalisées:_

* L'interface va déposer les aLINK du trader dans la pool ySwap;
* Le montant en dollars de l'aLINK, au moment de la transaction, est effectué à l'aide de l'aUSD de la pool aLEND
* ySwap envois le montant de aLEND au trader acheteur

L'AMM est un "constant product market maker"  \(CPMM\) et utilise une bonding curve, de conception similaire à Uniswap. Si la valeur en dollars de l'actif augmente, les déposants recevront le montant total du dépôt. Si la valeur en dollars de l'actif diminue, les déposants recevront le montant total du dépôt plus un montant supplémentaire en USD. Ce montant supplémentaire en aUSD est destiné à compenser les fournisseurs de liquidité pour l'exposition à des pertes non permanentes, qui se produisent lors de variations de prix volatiles des actifs.

