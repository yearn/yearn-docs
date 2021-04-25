---
Status: En Recherche & Développement
---

# StableCredit

StableCredit est un nouveau produit en recherche et développement qui combine trois piliers de l'infrastructure DeFi existante:

- Création de dette synthétique (DAI, Synthetix).
- Plateforme de prêt décentralisées (Compound, AAVE).
- Fonctionnalités des Automated Market Makers, AMM (Uniswap, Sushiswap). 

## Mécanismes

StableCredit permettra aux utilisateurs le dépôt d'actifs comme collatéral et l'obtention d'une ligne de crédit (exprimée en StableCredit USD) basée sur la valeur en dollar de l'actif déposé. Par exemple, un utilisateur peut déposer 100 LINK et obtiendra 1100$ de StableCredit USD (le LINK valant ~11$ à l'écriture de ces lignes). Le StableCredit USD peut être échangé pour d'autres actifs disponibles dans le protocole. 

Les cours de change entre le StableCredit USD et les actifs dans le protocol sont déterminés par les prix fournis par des oracles (Chainlink), ainsi que l'actuel ratio d'utilisation des actifs au sein de la plateforme. Par exemple, si les fournisseurs de liquidité (LP) ont prêté 100 DAI à la pool et que 90 DAI sont empruntés, le ration d'utilisation est de 90%. Comme les systèmes utilisant des courbes de liaison (Bonding Curves), il y aura une prime importante pour tout emprunt additionnel de DAI (le coût d'emprunt du DAI sera > \$1). Les utilisateurs pourront emprunter jusqu'à 75% de la valeur de leur collatéral (exemple pour un ration d'utilisation de 75%).

L'AMM permettra aussi l'exposition de liquidité unilatéral pour les fournisseurs de liquidité (LPs). Actuellement, les modèles populaires d'AMM, comme  Uniswap ou SushiSwap, requièrent des LPs qu'ils déposent les 2 actifs dans la pool. Par exemple, dans une pool de liquidité ETH-USDC, les fournisseurs de liquidités doivent déposer de l'ETH et de l'USDC à un ration de 50/50. Cela augmente la barrière à l'entrée ainsi que le capital nécessaire. L'approvisionnement unilatéral en liquidités permettra aux LP de ne déposer qu'un seul des actifs dans la pool de liquidités. (dans cet exemple, soit de l'ETH soit de l'USDC). La barrière à l'entrée pour devenir un LP est donc grandement réduite et cela contribue à une efficacité du capital déposée accrue. 

## Résumé

Les utilisateurs peuvent:

- Déposer du collatéral et obtenir une ligne de crédit (StableCredit USD).
- Emprunter d'aurtes actifs avec cette ligne de crédit (similaire à Aave ou Compound).
- Échanger l'actif emprunté pour un autre actif dans la pool (fonctionnalité des AMM existantes).

## Ressources pédagogiques supplémentaires et contexte (en anglais)

- [Post Medium original : Introducing StableCredit](https://medium.com/iearn/introducing-stablecredit-a-new-protocol-for-decentralized-lending-stablecoins-and-amms-7252a43ee56)
- [Animation illustrant les mécanismes de StableCredit](https://twitter.com/finematics/status/1305188626008100865)
- [Vidéo de Bankless à propos de StableCredit, avec Andre Cronje](https://www.youtube.com/watch?v=SkTuMVBLBNQ)
- [Vidéo CODEUP 38 à propos de StableCredit, avec Andre Cronje](https://www.youtube.com/watch?v=bdC3rNDChbw&feature=youtu.be&t=2002)
