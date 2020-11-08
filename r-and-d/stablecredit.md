---
description: In Development
---

# StableCredit

{% embed url="https://medium.com/iearn/introducing-stablecredit-a-new-protocol-for-decentralized-lending-stablecoins-and-amms-7252a43ee56" caption="" %}

## Explications

1. Finematics [explique](https://twitter.com/finematics/status/1305188626008100865) le processus complet en 30 secs.
2. Andre rejoint  le CODEUP 38 et [expllique](https://www.youtube.com/watch?v=bdC3rNDChbw&feature=youtu.be&t=2002) le produit lui meme.
3. Economic Designs also takes a shot at [explaining](https://twitter.com/lisajytan/status/1304584889237270528) it.
4. Bankless [discussed](https://www.youtube.com/watch?v=SkTuMVBLBNQ&feature=youtu.be), with Andre, StableCredit in detail.

## Les autres concepts

* Stablecredit uses single-sided [Automated Market Makers](https://docs.yearn.finance/defi-glossary#automated-market-maker). Here is more [info](https://www.youtube.com/watch?v=842acSWmBC4&t=336s) on how AMMs work.
* [Collateral](https://docs.yearn.finance/defi-glossary#collateralization), Multicollateral.
* MakerDAO and [MakerDAO CDPs](https://docs.yearn.finance/defi-glossary#maker) is a lending system which StableCredit builds on conceptually.
* Utilization Ratio is the maximum amount of credit a user will get from the deposited amount.

## Qu'est ce que l'utilisateur recoit ?

1. Les utilisateurs recoivent une ligne de credit The user gets a Credit Line by providing "almost any token". Currently, any token available in the [CHAINLINK oracle \(price feeds\)](https://feeds.chain.link/).
2. The credit line is given to the user in a StableCredit token. This is a new token minted. This token is a stable token. The user can only get up to 75% from the total amount deposited into the StableCredit contract. This 75% is called utilization ratio.

