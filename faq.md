---
title: faq.yearn.finance
tags: 'docs, faq, published'
---

# FAQ

## General

### Est-il sûr d'investir de l'argent dans yearn?

* Vous êtes priés de faire vos propres recherches et de décidez par vous-même.

### Est ce que yearn est audité?

* Oui, vous pouvez retrouver la liste des audits [ici](https://github.com/iearn-finance/audits).

## Feedback & Support

Si vous avez des questions sur la façon de faire quoi que ce soit, nous pouvons vous aider sur::

* [Discord](http://discord.yearn.finance)
* [Telegram](https://t.me/yearnfinance)

Mais si vous pensez que quelque chose peut être amélioré ou si vous avez trouvé un bug, nous voulons le résoudre. Veuillez le poster ici:

* [Github](https://github.com/iearn-finance) — create a new issue in the relevant repository.
* [Forum](https://gov.yearn.finance/c/feedback/) — post in the feedback category.

## Produits

### yearn.finance

* [yearn.finance](https://yearn.finance/) héberge des interfaces utilisateur pour les produits  suivant:  **Vaults**, **Earn**, **Zap**, **APR**, et **Cover** .

### Vaults \(coffres-forts\)

* [yearn.finance/vaults](https://yearn.finance/vaults)

#### Qu'est ce qu'un  Vault?

* Les Vaults utilisent des stratégies pour automatiser les meilleurs rendement disponibles.
* Ils ont été conçus pour que la communauté puisse travailler ensemble pour élaborer de nouvelles stratégies afin de trouver le meilleur rendement.
* Andre a expliqué les [vaults](https://medium.com/iearn/yearn-finance-v2-af2c6a6a3613) et les [delegated vaults](https://medium.com/iearn/delegated-vaults-explained-fa81f1c3fce2) dans ses deux posts.
* Simplement, les vaults peuvent faire cela:
  * Utilisez n'importe quel actif comme liquidité.
  * Utilisez la liquidité comme garantie \(collateral\) et gérez la garantie à un niveau sûr afin de ne jamais faire défaut.
  * Emprunter des stablecoins.
  * Utiliser ces stablecoins pour générer des intérets
  * Réinvestir les stablecoins engendrés.

#### Mais je ne peux pas faire tout ça moi-même?

* Oui, vous pouvez, mais les vaults vous aident à économiser sur les frais de gaz, à  maintenir à un bon ratio collatéral / dette afin de ne pas faire vous faire liquider, et à optimiser automatiquement  les stratégies utilisant des stablecoins pour générer des  intérets les plus important possibles, même lorsque vous dormez.

#### **Je vois un rendement dans la page dédiée aux vaults, est-ce le rendement actuel?**

* Non. C’est le rendement historique moyen pour ce vault. L’APY / rendement actuels ne sont pas montrés puisque les vaults sont en beta et en phase de test.
* Plusieurs sites de tiers propose des infos sur les APY des vaults et plus, vous les trouverez ci-dessous dans [Statistiques](https://docs.yearn.finance/faq#statistics).

#### **Quels sont les risques?**

* Alors que les actifs déposés ne peuvent diminuer, la dette d’un vault peut. Si une stratégie ne parvient pas a surperformé la dette, alors une partie des fonds peut être bloquée de façon impermanente. Si une stratégie surperforme la dette, les actifs se débloquent.
  * Il existe des méchanismes dans les vaults pour parvenir à ces bloquage, mais rien n’est parfait.
* Aujourd’hui, les vaults n’ont pas encore été audités.
* Il y a un risque de smart contract lié avec chaque contrat avec lequel le vault intéragit.

#### **Quels sont les différents yVaults?**

**yLINK et yaLINK**

* **Quelle est la différence entre les vaults LINK et aLINK?**
  * Aucun en terme de rendement. Les LINK déposés dans le vault seront déposés dans Aave pour générer des aLINK.
* **Pourquoi le rendement affiché des deux vaults est-il différent?**
  * aLINK a un frais d’assurance de 0.5%, qui est remboursé si surperformé. Le vault LINK ne l’a pas pour éviter de le répéter.

**yETH et yWETH**

* **Quelle est la différence entre les vaults ETH et WETH?**
  * Aucun en terme de rendement. Les ETH déposés seront transformés en WETH. Avoir un vault WETH facilite l’interaction pour d’autres protocoles Ethereum.
* **Comment le vault ETH se protège de la liquidation?**
  * Ce vault prend le prix de l’ETH directement du Maker OSM \(Oracle Security Model\), un système qui lit le prix des Oracle une heure en avance. Cela laisse une heure au vault pour payer sa dette avant la liquidation. D’autre part, le vault continue d’augmenter ses garanties en redéposant les profits à chaque récolte.

**Les autres vaults**

* Les vaults de marchés monétaires v1, anciennement appelés iEarn, peuvent être trouvés [ici](https://yearn.finance/earn).
* D’autres vaults peuvent être trouvés [ici](https://yearn.finance/vaults).

**Si la stratégie actuelle pour la vault yCRV cultive du CRV, il est juste ajouter à mon solde quand je le retire?**

* Non. Le vault va cultiver du CRV puis le vendre au marché automatiquement. Au retrait, vous aurez plus de yCRV

#### **Pourquoi le yCRV ne vaut pas 1$, n’est-ce pas un stablecoin?**

* Non, yCRV ne vaut pas 1$ et n’est PAS un stablecoin. Vous pouvez penser à yCRV comme un index de stablecoins à rendement \(yDAI+yUSDC+yUSDT+yTUSD\), qui génère lui-même du rendement \(frais de trading de la pool Curve Y\). Le prix du yCRV est donc non-décroissant.

**Si je retire mes yCRV du vault, est-ce qu’ils sont reconvertis dans la pool Curve y, ou dois-je faire quelque chose d’autre?**

* En retirant ses yCRV du vault, vous récupérez des yCRV + les intérêts en yCRV. Puisque vous récupérez des tokens yCRV, ils sont déjà stake dans la pool Curve Y et générent des intérêts. Vous n’avez rien à faire. Vous pouvez les stake [ici](https://dao.curve.fi/minter/gauges) pour générer des CRV en plus.

#### **Pourquoi n’y a-t-il pas un meilleur rendement pour le vault YFI?**

* Les vaults de deux monnaies différentes auront un rendement surement différents. Le nouveau vault sBTC suit la même stratégie que le vault yCRV, et pourtant leurs rendements sont bien différents. La meilleure réponse serait que seulement peu de plateformes acceptent de staké du YFI et il y a donc peu de stratégies différentes possibles pour l’instant.

#### **J’ai déposé des fonds dans un vault, que vais-je récupérer lors du retrait?** 

* Vous récupérerez toujours uniquement le même type d’actif que celui que vous aurez déposé.
* Vous récupérerez le montant déposé, plus le rendement gagné grâce à la pool, moins les frais.

**Quels sont les frais?**

\*\*\*\*

* **0.5% de frais** sur les fonds retirés d’une stratégie active
  * Chaque vault a un certain montant des fonds déposés qui dort, et la majorité utilisé dans la stratégie. Les fonds dormants sont la différence entre `vault holdings` et `strategy holdings`, vous pouvez les consulter sur [feel the yearn](https://feel-the-yearn.app/).
  * Quand vous retirez, si vos fonds viennent des fonds dormants, vous ne paierez aucun frais. S’ils sont utilisés activement dans une stratégie, vous paierez les frais de retraits de 0.5%.
* **5% de frais** sur le rendement additionnel
  * Destinés aux stratégies créées par la communauté, comme la nouvelle stratégie du vault yETH. Actuellement, 10% de ces frais vont au créateur de la stratégie. Les 90% restantes sont redirigés à la trésorerie, puis redistribués à la gouvernance.

#### 

**Pouvez-vous expliquer les 5% de frais sur le rendement additionnel?**

* Avant, ce frais s’appelait un frais sur le “gas subventionné”, ce que seul Andre comprenait vraiment. Techniquement, ce n’est pas un frais de performance - c’est un frais appliqués sur certaines transactions génératrices de profit qui demande un coût de gas élevé et sont critiques au bon fonctionnement interne du vault.
* Chaque vault a plusieurs niveaux. Voici deux exemples illustrant où est prélevé ce frais lorsque la fonction `harvest()` est appellée.
* Exemple du vault yCRV:
  * Niveau 1: les stablecoins gagnent des intérêts sur les marchés monétaires \(Compound, Aave, dYdX\).
  * Niveau 2: les tokens du niveau 1 \(yDAI, yUSDC, yUSDT, et yTUSD\) sont fournis comme liquidité à la pool yCRV pour récupérer des frais de trading.
  * Niveau 3: la stratégie gagne des tokens CRV en récompense, qu’elle réinvestis dans la pool yCRV - **c’est le seul niveau où ce frais de 5% est perçu**.
* Exemple du vault USDC:
  * Niveau 1: Intérêts perçus pour être prêtés sur Compound.
  * Niveau 2: le COMP est vendue pour du USDC
  * Niveau 3: La stratégie gagne des tokens DF de DForce, qui sont récoltés et vendus pour de l’USDC - **c’est le seul niveau ou les 5% de frais sont perçus.**

**Où vont les frais?**

* Ils vont directement vers un [contrat](https://etherscan.io/address/0x93A62dA5a14C80f265DAbC077fCEE437B1a0Efde) dédié à la trésorerie.
* Cette trésorerie se remplit jusqu’à atteindre 500k$, limite après laquelle ces fonds sont redirigés vers le [contrat](https://etherscan.io/address/0xBa37B002AbaFDd8E89a1995dA52740bbC013D992) de staking de gouvernance.

**Les frais allaient-ils toujours là?**

* Non, quand yearn a commencé ils allaient directement vers l’[addresse](https://etherscan.io/address/0x2d407ddb06311396fe14d4b49da5f0471447d45c) d’Andre.
* Ensuite, une addresse [multisig](https://etherscan.io/address/0xFEB4acf3df3cDEA7399794D0869ef76A6EfAff52) a été mise en place et les fonds y ont été redirigés.
* Avant la v2 de la gouvernance, les récompenses de staking allaient [ici](https://etherscan.io/address/0xb01419E74D8a2abb1bbAD82925b19c36C191A701).

**Rendement**

* La création d’un dashboard qui montrerait clairement l’APY actuel de toutes les positions ouvertes est prévue. Pour l’instant, les Vaults étant toujours en beta, nosu n’affichons pas les APY en temps réel, mais ils sont postés sur [Twitter](https://twitter.com/iearnfinance) régulièrement. Vous pouvez obtenir une estimation en allant regarder quelles sont les stratégies des vaults.
* Par exemple, si le vault yCRV cultive du CRV, vous pouvez vérifier le rendement actuel sur la [page d’accueil de Curve](https://www.curve.fi/) pour la Y pool.

#### Stratégies des Vaults

**Qu’est ce qu’une stratégie de vault?**

* Les stratégies des vaults yearn sont des smarts contracts modulables qui indiquent à chaque vault quels actifs emprunter, quels actifs cultiver et ou ces actifs cultivés devraient être vendus.

**Quelles sont les stratégies actuelles?**

* Vous pouvez aller voir les stratégies mises en place sur [feel-the-yearn](https://feel-the-yearn.vercel.app/).
* À l’avenir, nous prévoyons de créer un dashboard pour rendre les stratégies et les rendements plus compréhensibles.

**Qui a le contrôle les stratégies?**

* Andre et d’n’importe quel développeur peut les écrire, mais les signataires de la multi-sig décident si elles sont mises en place ou non.

**How can I make a strategy?**

* Pour l’instant, vous pouvez poster vos stratégies sur le forum en détaillant ce qu’elle devrait acheter/vendre/cultiver and quel serait le rendement actuel. Il y a un modème pour vous aider.

**Quel est le processus pour que ma stratégie soit utilisée sur yearn?**

* En la postant sur le forum et si elle est approuvée, elle sera utilisée dans les vaults et vous pourrez être rémunéré.

**Quand une stratégie change-t-elle, et qui la change? Est-ce automatique?**

* Pour l’instant Andre regarde le marché et écrit les stratégies que lui et les multi-sig pensent sécurisées tout en obtenant le meilleur rendement. Ils les changent en fonction des rendements du marché.

### Earn

* [yearn.finance/earn](https://yearn.finance/earn)

#### Qu’est-ce que Earn?

* Earn est un aggrégateur de plateformes de prêt qui rebalance les fonds entre elles pour obtenir le meilleur rendement.
* Vous pouvez déposer du DAI, USDC, USDT, TUSD, or sUSD et les fonds seront automatiquement prêtés aux meilleurs taux sur [Compound](https://compound.finance/), [dYdX](https://dydx.exchange/) or [Aave](https://app.aave.com/home) \(Ddex et Fulcrum sont arrêtés\).
* Learn more in the [Yearn Docs](https://docs.yearn.finance/yearn.finance/yearn).

### Zap

* [yearn.finance/zap](https://yearn.finance/zap)

#### What is Zap?

* Zap permet aux utilisateurs de convertir leurs tokens disponibles en seulement une interactions, réduisant les frais de transactions.
* Les Zaps ont été créés par DefiZap qui est maintenant [Zapper.fi](https://zapper.fi/), une sorte de service de routage DeFi tout-en-un.

#### Pourquoi utiliser Zap?

* “Les Zaps vous permettent de rentrer dans une position DeFi en seulement une transaction - ça s’appelle zapping in.” - [Guide d’utilisation de Zaps](https://defitutorials.substack.com/p/how-to-use-defizap)
  * À noter que certaines sections de l’article ne sont pas à jour.

#### Que puis-je faire avec Zaps dans Yearn?

* Avec un zap, vous pouvez transférer vos DAI en yCRV en une transaction par exemple. Normallement, vous auriez du aller sur yearn.finance/earn, déposer des DAI, récupérer des yDAI, et déposer ces yDAI sur [curve.fi](http://curve.fi/) pour récupérer des yCRV. Avec Zap, tout ça se fait en une transaction!

#### Super, quels sont les désavantages?

* Cela pourrait coûter plus cher en frais que de tout faire soi-même, mais ça reste plus rapide.

### yInsure / Cover

* [yinsure.finance](https://yinsure.finance/)

#### Qu’est-ce que yInsure?

* yInsure, aussi connu sous le nom de Cover, est un système de couverture commune qui assure contre les risques liés aux smarts contracts.
* Il n’y a pas de KYC, et est souscrit par Nexus Mutual.
* Vous pouvez en apprendre plus en listant cet [article](https://medium.com/iearn/yinsure-finance-a-new-insurance-primitive-77d5d4217896).

### Produits Actuellement en Recherche et Développement

#### yTrade

* [ytrade.finance](https://ytrade.finance/)
* Trading de stablecoins avec levier \(testnet\)

#### yLiquidate

* [yliquidate.finance](https://yliquidate.finance/)
* Liquidations automatique pour Aave \(testnet\)

#### ySwap

* [yswap.exchange](https://yswap.exchange/)
* Automated Marker Maker à côté unique \(test en mainnet\)

#### yBorrow

* [yborrow.finance](https://yborrow.finance/)
* Vaults de délégation de crédit pour du prêt de smart contract a smart contract \(testnet\).

## Communication

* [Forum](https://gov.yearn.finance/)
  * Beaucoup de discussion en temps réel ont lieu sur le Telegram et le Discord, mais pour qu’une proposition devienne une YIP \(Yearn Improvement Proposal\) il faut qu’elle soit postée et discuté sur le forum.
  * C’est l’endroit principal pour que les détenteurs du token puissent aller vérifier les sujets de gouvernance.
* [Discord](https://discord.gg/94CmMdt)
  * Comprenant des sections dans toutes les langues
* [Telegram](https://t.me/yearnfinance) - Main Chat
* [Telegram](https://t.me/yearncommunity) - Trading/Social/Fork Chat.
* Twitter
  * [yearn.finance](https://twitter.com/iearnfinance?s=20) - Twitter officiel de Yearn
  * [Andre Cronje](https://twitter.com/AndreCronjeTech?s=20) - Développeur principal de Yearn
  * [yLearnfinance](https://twitter.com/yLearnfinance) - Informations sur Yearn
  * [Learn 2 Yearn](https://twitter.com/learn2yearn) - Informations sur Yearn

## Gouvernance

### Tout sur les YIPs

#### Qu’est-ce qu’une YIP? Pourquoi sont-elles importantes?

* Une YIP, ou Yearn Improvement Proposal _\(Proposition d’Amélioration de Yearn\)_, est la façon dont les nouvelles fonctionnalités sont ajoutées à l’écossytème yearn. Les utilisateurs ouvrent uen proposition sur le forum, celle-ci est discutée et sont niveau d’approbation est évalué. Si beaucoup d’utilisateurs sont d’accords avec cette propostion, elle peut ensuite être postée on-chain pour que tout le monde puisse la voter.

#### Combien de personnes doivent voter pour qu’une YIP proposée on-chain passe?

* Le quorum est de 20%. Ce qui signifie qu’au moins 20% des YFI stakés dans le contrat de gouvernance doivent voter pour qu’une proposition puisse passer. Ensuite, plus de 50% des votes doivent être au “Oui” pour que la proposition soit mise en oeuvre.

#### Comment faire une proposition?

* Il y a un modèle sur [Github](https://github.com/iearn-finance/YIPS/blob/master/yip-X.md), et sur le [forum](https://gov.yearn.finance/) si vous postez sous “proposals” ou “discussion”, le modèle devrait s’auto-remplir.
* Le processus est généralement:
  1. Discussion sur le forum
  2. YIP officielle \(généralement faite par les modérateurs\), ajoutée au github et mise on-chain
  3. Annonce

#### Qui peut faire une proposition?

* N’importe qui peut poster une proposition que ce soit sur le forum ou on-chain.

### Le Vote

#### Comment voter?

* Il faut staker vos YFI dans le contrat de [gouvernance](https://ygov.finance/stake), puis voter pour les YIPs qui sont on-chain sur le [dashboard](https://ygov.finance/vote) des votes.

#### Puis-je voter si mes YFI sont dans le vault YFI?

* Non, vos YFI doivent être stakés dans le [contract](https://ygov.finance/staking) de gouvernance pour pouvoir voter.

#### Où puis-je voir les YIPs?

* Vous pouvez les consulter sur le [dashboard](https://ygov.finance/vote) de votes en se connectant avec votre wallet web3, ou à [yips.yearn.finance](https://yips.yearn.finance/all-yip).

#### Pourquoi dois-je staker? Quel est le rendement?

* Vous devez staker vos YFI pour pouvoir voter sur les YIPs et recevoir les récompenses générées par l’écosystème de yearn. L’APY du staking n’est actuellement pas affichée. Il est possible de la demander sur le chat.

#### Que dois-je faire pour recevoir les récompenses avec mes YFI?

* Tout ce que vous avez à faire est de staker vos YFI à [ygov.finance/stake](https://ygov.finance/stake) et vous recevrez vos récompenses si la trésorerie dépasse les 500k$. Vous pouvez vérifier l’addresse de la trésorerie [ici](https://zapper.fi/dashboard?address=0xFEB4acf3df3cDEA7399794D0869ef76A6EfAff52).
* À noter qu’en stakant, les récompenses que vous obtenez peuvent seulement être récoltées 3 jours après avoir voter.

#### Est-ce que staker mes YFI est important pour voter?

* Oui. Staker ses YFI à [ygov.finance/stake](https://ygov.finance/stake) dans la section v2 sous Gouvernance V2 est nécessaire pour que vos votes soient pris en compte. Actuellement, vous pouvez voter sans staker, mais vous gâcherez votre gas et les votes ne seront pas pris en compte.

#### Que faire si je souhaite retirer mes YFI avant la fin du verrouillage?

* Ce n’est pas possible, désolé. Le verrouillage dure 3 jours après que votre dernier vote, avant cette date vous ne pourrez pas retirer vos tokens.
* Si vous essayez de les retirer avant la fin des 3 jours, vous aurez un frais de gas très élevé. C’est une erreur, même en les payant vous ne pourrez pas retirer vos tokens.

#### J’ai voté et je sais qu’il faut que j’attende 3 jours, y a-t-il un endroit où je puisse voir le temps restant avant de pouvoir unstake mes YFI?

* Oui! Vous pouvez lire directement le [smart contract](https://etherscan.io/address/0xBa37B002AbaFDd8E89a1995dA52740bbC013D992#readContract), allez au votelock \(28\) et rentrez votre addresse. Vous devriez voir le numéro de block ethereum auquel vous pourrez unstake vos tokens.

#### Quelle est la différence entre voter pour un sondage sur le forum et voter on-chain?

* Un sondage a seulement pour but d’évaluer le sentiment de la communauté enver une proposition, alors qu’un vote on-chain a pour but de décider de la mise en oeuvre de la proposition, qui aura lieu si le vote passe.

#### Qu’en est-il du nouveau système de vote sans gas?

* Nous avons maintenant un système de signalement off-chain qui utilise les balances stakés sur ygov. Cela replace les anciens et informels sondages qui étaient vulnérable à des attaques de sybil. Il permet de choisir plusieurs choix et ne comprend aucun coût en gas, il faut signer avec son wallet. Le système de vote on-chain est toujours utilisé pour les YIPs.

#### Pourquoi ne puis-je pas récupérer mes récompenses de staking?

* Pour récupérer vos récompenses vous devez 1\) avoir des tokens stakés, et 2\) avoir voté depuis plus de trois jours pour pouvoir récupérer. Cela devrait être modifié dans une prochaine mise à jour.

### yDAO

* Pokemol [site](https://pokemol.com/dao/0xcb46298767fb5d44c18313976c30d3eeb5071862/)
* Forum [post](https://gov.yearn.finance/t/ydao-for-community-funding/2243)

#### Quel est son but?

* Utilisé pour financer des contributions à valeur ajoutée à l’écosystème yearn.

#### Comment puis-je gagner de l’argent avec?

* Ce n’est pas le but. C’est uniquement pour allouer du financement à des projets, les YFI donnés seront dépensés et la valeur de vos parts sera diluée.

#### Qui peut la rejoindre?

* Ouvert à tous avec une taux de base de 1 part = 0.1 YFI.

#### Comment puis-je en faire partie?

* En vous connectan ici à Pokemol avec votre wallet web3. Cliquez sur New Proposal sur le boutton en haut à droite. Cliquez sur member.
  * Titre: votre nom/entité
  * Description: “J’engage X YFI en échange de Y parts” \(Restez consistant avec le montant de 0.1 YFI = une part s’il vous plaît.\)
  * Lien: Lien vers votre entité \(Site web, Twitter, Linkedin\)
  * Share Requested: Le nombre de parts qui sont demandées
  * Token tribute: La quantité de YFI que vous souhaitez donner.
  * Loot: Le nombre de parts demandées.
  * Après avoir soumis vos deux transactions et être dans la liste d’attente pour les nouveaux membres, vous aurez besoin d’un sponsor. Copiez le lien de votre proposition et indiquez nous que vous souhaitez rejoindre le [Telegram de la yDAO](https://t.me/joinchat/Qn1GPBv0y7lY1vAmRCB7KA).

#### Comment puis-je demander du financement?

* Sur le même site que pour devenir membre mais dans la section “funding”. Vous pouvez demander de l’aide dans le [chat telegram](https://t.me/joinchat/Qn1GPBv0y7lY1vAmRCB7KA).

## Communauté

### Andre Cronje dirige-t-il yearn?

* Andre ne dirige pas Yearn, les détenteurs du token YFI prennent les décisions à propos de ce qui doit être développé et de la gouvernance. Andre est le développeur principal de l’écosystème yearn.

### Que fait Andre?

* Andre est le développeur principal de yearn, il développent les produits compris dans l’écossytème: Yearn, Ytrade, Yswap, Yliquidate, Yborrow. Il est aussi actuellement responsable des Vaults.

### Qu’est-ce que la multisig et que font-ils?

* L’addresse multi-signature est expliquée en détails dans cette [thread](https://gov.yearn.finance/t/yfi-minting-ownership/155). Essentiellement, c’est un compte à multi-signature \(6 sur 9\) qui contrôle la création de YFI si un vote pour créer plus de tokens passe.

### Qui sont les 9 multisignataires?

* [Cp0x.com](https://twitter.com/kaplansky1/status/1285427247286046725)
* [Daryllautk](https://twitter.com/Daryllautk/status/1285434908383444992)
* [Devops199fan](https://twitter.com/devops199fan/status/1285430347954622464)
* [Banteg](https://twitter.com/bantg/status/1285426492906909696)
* [Milkyklim](https://milkyklim.keybase.pub/yearn-social-proof.txt)
* [Joe Mahon aka Substreight](https://twitter.com/Substreight/status/1299780260737630209)
* [Tarun Chitra, Gauntlet](https://twitter.com/gauntletnetwork/status/1299778153674616833)
* [Vasiliy Shapovalov, p2p.org](https://twitter.com/_vshapovalov/status/1299799139635679232)
* [Mariano Conti, ex-MakerDAO](https://twitter.com/nanexcool)

### Les multisignataires ont-ils changé?

* Oui, YPI-40 a changé quatre des signataires
* Les signataires qui ont été remplacés sont:
  * [Coopahtroopa](https://twitter.com/Cooopahtroopa/status/1285438650550038529)
  * [Michael, Curve.fi](https://twitter.com/CurveFinance/status/1285428322986389504)
  * [Calvin Liu](https://twitter.com/cjliu49/status/1285439553180798976)
  * [Damir Bandalo](https://twitter.com/damirbandalo/status/1285500362015875073)

### Quelles décisions Andre peut-il prendre seul?

* Andre peut développer l’écosystème Yearn et sortir de nouveaux produits. En général, il poste ses pensées et idées sur le forum pour que tout le monde puisse être au courant.

### Est-ce que le groupe de multisignataires peut lui dire quoi faire?

* Ils sont en contact les uns avec les autres, mais les priorités d’Andre sont décidées par les détenteurs de YFI à travers les YIPs.

### Qui d’autre écrit du code pour yearn? Y a-t-il une équipe?

* Actuellement, seulement Andre.

### Est-ce que certaines personnes sont payées pour travailler sur yearn?

* Pour l’instant pas encore, mais grâce au passage de la YIP 36 et la création d’une réserve de fonds par la communauté qui devrait rester à 500k$, nous pouvons désormais rémunérer Andre pour son travail, financer des audits, et payer pour de nouveaux développeurx à embaucher, et tout ce dont l’écosystème Yearn aurait besoin.

### Comment puis-je travailler pour Yearn?

* Tu peux créer une YIP pour demander du financement de la trésorerie, ou en demander à la yDAO.

### Avez-vous des postes ouverts?

* Oui! Nous avons besoin de tous types de personnes qui peuvent aider à faire de l’écosystème Yearn un produit en plein essor et à ajouter de la valeur à YFI. Vous pouvez demander dans le Discord ou le Telegram pour candidater, ou poster sur le forum. Dites nous comment vous pensez pouvoir apporter de la valeur à Yearn, er combien vous pensez que vous devriez être payé de la réserve communautaire. Aussi, vous pouvez aller sur la yDAO pour demander du financement pour votre travail sur l’écossytème.

### Comment participer?

* Vous pouvez participer dans YFI en votant sur des YIPs actives, en discutant sur le forum des YIPs qui attendent d’être proposées on-chain, et en parlant de YFI sur Discord et Telegram. Si vous connaissez une autre langue vous pouvez nous aider à traduire le site et les YIPs dans cette langue.

### Efforts en court pour améliorer Yearn

* Vous pouvez consulter les YIPs actives [ici](https://yips.yearn.finance/all-yip).

## Interface Utilisateur

### Puis-je utiliser les dApps de l’écosystème Yearn sur mon smartphone?

* Oui, en utilisant le moteur de recherche [Metamask](https://metamask.io/download.html).

## Technical Support

### J’ai envoyé ma transaction ETH mais elle est marquée comme “pending”? Comment régler ça?

* Vous devez toujours faire attention à régler correctement votre gas si vous voulez qu’une transaction se déroule rapidement. Vérifiez les prix actuels du gas chez [Ethgasstation](https://ethgasstation.info/) ou [gasnow](https://www.gasnow.org/).
* Si vous utilisez MetaMask et que vous avez effectué votre transaction mais qu’elle est trop lente, vous avez la possibilité de l’accélérer en cliquant sur le bouton d’accélération situé sous votre dernière transaction en attente sous “activité”. Cela devrait vous permettre de renvoyer la même transaction avec un prix de gas plus élevé pour la faire confirmer plus rapidement.
* Si vous avez tout essayé et que votre transaction est toujours bloquée en attente, vous pouvez la corriger en envoyant une transaction au nonce de la première transaction bloquée avec un prix de l’essence élevé pour écraser la file d’attente bloquée. Voici un bon [guide](https://ethgasstation.info/blog/stuck-transaction-guide/#:~:text=Select) expliquant comment faire.

### Pourquoi les frais de retraits sont si élevés?

* Si vous constatez des frais plus élevés que la normale lors de l’utilisation de l’écosystème Yearn, cela peut être dû à la congestion d’Ethereum et au coût anormalement élevé du gas. Consultez la page [Ethgasstation](https://ethgasstation.info/). Vous avez le choix entre attendre que le prix du gas baisse ou dépeaugmenter votre prix de gas pour traiter votre transaction maintenant.
* Si les prix du gas sont extrêmement élevés, cela signifie qu’il y a une erreur et que la transaction ne pourra pas être traitée. Par exemple, si vous essayez de déposer un jeton que vous n’avez pas ou s’il n’y a pas de couverture disponible pour un contrat sur [http://yinsure.finance/](http://yinsure.finance/).

## Projets Reliés

### [Curve](https://www.curve.fi/)

* Curve est un échange de réserves de liquidité sur Ethereum \(comme [Uniswap](https://app.uniswap.org/#/)\) fait pour 1\) de l’échange extrêmement efficient de stablecoins, 2\) un revenu supplémentaire à faible risque pour les fournisseurs de liquidités, sans coût d’opportunité. Curve permet aux utilisateurs \(et aux smart contracts comme 1inch, Paraswap, Totle et [Dex.ag](http://dex.ag/)\) de négocier entre DAI et USDC avec un algorithme sur mesure à faible glissement et à faible coût, conçu spécifiquement pour les stablecoins et gagner des commissions. Derrière, la réserve de liquidités est également fournie au protocole Compound ou yearn.finance où il génère encore plus de revenus pour les fournisseurs de liquidités.
* Curve [FAQ](https://www.curve.fi/rootfaq).

### [Aave](https://app.aave.com/home)

* Aave est un protocole open source et non-gardien qui permet la création de marchés monétaires. Les utilisateurs peuvent gagner des intérêts sur leurs dépôts et emprunter des actifs.

## Ressources

### Où puis-je en apprendre plus sur Yearn?

* [Learn Yearn](https://www.learnyearn.finance/)
* [Medium.com/iearn](https://medium.com/iearn)
* [yCosystem](https://ycosystem.info/)

### Liste des Smart Contracts

* [https://gov.yearn.finance/t/yearn-contracts/1951](https://gov.yearn.finance/t/yearn-contracts/1951)
* [https://etherscan.io/accounts/label/yearn-finance](https://etherscan.io/accounts/label/yearn-finance)
  * sign-in required
* [Delegated controller](https://etherscan.io/address/0x2be5d998c95de70d9a38b3d78e49751f10f9e88b#readContract)
* [StrategyVaultTUSD](https://etherscan.io/address/0x35CEE4c61B7619956e0B2015B5411F93CBba817A#code)
* [yLINK token](https://etherscan.io/address/0x881b06da56bb5675c54e4ed311c21e54c5025298#code)
* [yaLINK token](https://etherscan.io/address/0x29e240cfd7946ba20895a7a02edb25c210f9f324#readContract)
* [StrategyMStableSavingsTUSD](https://etherscan.io/address/0xd6214317bf66921154d78e3074bada013a4de8e8#readContract)
* [yTUSD](https://etherscan.io/address/0x37d19d1c4e1fa9dc47bd1ea12f742a0887eda74a)
* [yTokenRebalance](https://etherscan.io/address/0x19b6424C58aFcee6D0cb954D4B8d44B9b5e9cC09#code)
* [CollateralVaultProxy](https://etherscan.io/address/0xf0988322b8392245d6232e520bf3cdf912b043c4)
* [USDC strategy for LINK](https://etherscan.io/address/0x25fAcA21dd2Ad7eDB3a027d543e617496820d8d6)
* [Strategy for USDC vault](https://etherscan.io/address/0xA30d1D98C502378ad61Fe71BcDc3a808CF60b897)
* [DAI vault](https://etherscan.io/address/0xACd43E627e64355f1861cEC6d3a6688B31a6F952)

### Référence détaillée des vaults

[https://vaults.finance/](https://vaults.finance/)

### Statistiques

* [yieldfarming.info](https://yieldfarming.info/)
* [yVault ROI Calculator](https://py-earn.herokuapp.com/)
* [stats.finance/yearn](https://stats.finance/yearn)
* [Feel The Yearn](https://feel-the-yearn.vercel.app/)
* [Initial Distribution Dune Dashboard](https://explore.duneanalytics.com/dashboard/yearn)
* [Voting Stats Dune Dashboard](https://explore.duneanalytics.com/public/dashboards/Lqnxzm7fa8NVhKC4kc37DDFPZgqXryaIjyLRYAYp)
* [Vaults Stats Dune Dashboard](https://explore.duneanalytics.com/public/dashboards/g0bGfgloeXBd9C18jpBjdXi5KkQjR7IXYqFRUnHk)

### Dernières News Yearn

* [yearn.finance](https://twitter.com/iearnfinance) - Compte Twitter officiel de Yearn
* [AndreCronjeTech](https://twitter.com/AndreCronjeTech) - Compte Twitter officiel d’Andre Cronje
* [Yearn Finance](https://medium.com/iearn) - Blog Officiel

### Podcasts

* [Unchained - Andre Cronje on YFI and the Fair Launch: ‘I’m Lazy’](https://unchainedpodcast.com/andre-cronje-of-yearn-finance-on-yfi-and-the-fair-launch-im-lazy/)
* [Andre Cronje and the Philosophy of Yearn Finance](https://anchor.fm/hasu-research/episodes/6-Andre-Cronje-and-the-Philosophy-of-Yearn-Finance-ei4vds)
* [The FTX Podcast - Andre Cronje DeFI Architect](https://open.spotify.com/episode/6d14TJtQU7eB69azelpdeh)
* [Zapper Community Call - With Andre](https://www.youtube.com/watch?v=venoiaiVZ-U)
* [In DeFi My Money is Actually Mine. Its a Beautiful Concept But it Comes With Responsibilities - Andre Cronje](https://anchor.fm/camila-russo/episodes/In-DeFi-My-Money-is-Actually-Mine--Its-a-Beautiful-Concept-But-it-Comes-With-Responsibilities-Andre-Cronje-ehs3op)
* [YFI: Farming the Farmers \| Andre Cronje](http://podcast.banklesshq.com/25-king-of-the-yield-farmers-andre-cronje)

### Blogs

* [Yearn Finance - Blog Officiel](https://medium.com/iearn)
  * [Yinsure.finance: A new insurance primitive](https://medium.com/iearn/yinsure-finance-a-new-insurance-primitive-77d5d4217896)
  * [Delegated Vaults Explained](https://medium.com/iearn/delegated-vaults-explained-fa81f1c3fce2)
  * [Yearn.finance v2](https://medium.com/iearn/yearn-finance-v2-af2c6a6a3613?source=---------3------------------)
  * [Yearn Governance Forum](https://medium.com/iearn/yearn-governance-forum-7b7c9d0300ac?source=collection_home---6------2-----------------------)
  * [YFI rewards pool](https://medium.com/iearn/yfi-rewards-pool-810ef9256ec6)
  * [YFI](https://medium.com/iearn/yfi-df84573db81)

### Logos

* Dans le discord sour \#media-resources

