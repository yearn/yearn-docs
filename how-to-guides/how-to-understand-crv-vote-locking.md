# Comprendre le verrouillage des votes CRV

Ceci est un aperçu du fonctionnement du verrouillage des votes CRV sur Curve Finance et de la manière dont les stratégies d'investissement Yearn en tirent parti pour augmenter le rendement.

##  Verrouillage des votes CRV

Verrouillage des votes, "Boosties", or "Vote boosting" sont des fonctionnalités de Curve Finance pour lesquelles le jeton CRV est verrouillé dans la DAO de Curve.

Le verrouillage des jetons CRV pour voter génère des **veCRV** \(qui représente les CRV verrouiller pour voter\). Plus la période de verrouillage de vos CRV est longue, plus vous recevez de veCRV. La durée minimum de verrouillage est de 1 semaine, et la durée maximum est de 4ans.

La possession de veCRV permet de::

* participer à la gouvernance de Curve;
* **gagner des frais de trading** ; et 
* **boost rewards** \(augmenter vos récompenses\) sur la liquidité fournie.

### Frais de trading

50% de tous les frais de trading sur Curve à partir du 19 septembre 2020 vont être distribués aux possesseurs veCRV sous la forme de jetons CRV.

### Boost des récompenses

Le verrouillage des CRV pour obtenir des veCRV permet d'obtenir un boost des récompenses gagnées par les fournisseurs de liquidité de n'importe quelle piscine Curve, jusqu'à un maximum de  **2.5x**  la quantité de récompense.

Le multiplicateur de boost actuel est déterminé par une formule qui dépend de la liquidité actuelle dans la jauge de pool en tant que fraction du montant total de liquidité fournie, et de la fraction des droits de vote que le veCRV offre par rapport au total de veCRV .

Consultez [Curve Guide](https://guides.curve.fi/how-to-boost-your-crv-rewards-by-vote-locking/) pour plus de détails et les formules utilisées pour le calcul.  

## Vérrouillage des CRV dans Yearn

Yearn déploie une seule stratégie de verrouillage des votes CRV qui est partagée pour l'intégralité de ses stratégies utilisant Curve:

* [StrategyCurveYBUSDVoterProxy](https://etherscan.io/address/0x112570655b32a8c747845e0215ad139661e66e7f#code)
* [StrategyCurveBTCVoterProxy](https://etherscan.io/address/0x6d6c1ad13a5000148aa087e7cbfb53d402c81341#code)
* [StrategyCurveYVoterProxy](https://etherscan.io/address/0x07db4b9b3951094b9e278d336adf46a036295de7#code)
* [StrategyCurve3CrvVoterProxy](https://etherscan.io/address/0xC59601F0CC49baa266891b7fc63d2D5FE097A79D#code)

### Verrouillage des CRV pour obtenir des veCRV

 **10% de tous les CRV générés**  par la stratégie sont  **vérouillé pour 4ans**  dans la DAO de Curve dans le mais obtiennent le maximum de récompense avec un ratio de 1: 1 CRV: veCRV.

Acutellement, la distribution des veCRV n'a pas encore débutée, une date doit encore être annoncée par Curve Finance.

### Recevoir les frais de trading

En fonction de la part de Yearn de la quantité totale de veCRV, 50% des frais de trading seront réclamés sous forme de CRV. 10% de cette quantité sera ensuite verrouillé dans la DAO Curve pour obtenir plus de veCRV.

### Boost des récompenses de liquidité

Le boost en court, obtenu grâce au verrouillage des CRV sera déterminé par la formule décrite [précédement](how-to-understand-yvault-roi.md), mais dépendra essentiellement du montant total de liquidité fourni dans les pools Curve par Yearn et de son pouvoir de vote relatif, c'est-à-dire sa part du total actuel de veCRV.

Un outil "Yearn boost" affiche le boost actuel et potentiel de Yearn est en cours de développement et sera publié une fois disponible.

## Informations complémentaires

* Utilisation des CRV: [https://www.curve.fi/usecrv](https://www.curve.fi/usecrv)
* Guide de Curve pour le staking des CRV: [https://resources.curve.fi/guides/staking-your-crv](https://resources.curve.fi/guides/staking-your-crv)
* Guide de curve pour le verrouillage des CRV pour voter: [https://guides.curve.fi/how-to-boost-your-crv-rewards-by-vote-locking/](https://guides.curve.fi/how-to-boost-your-crv-rewards-by-vote-locking/)
* Curve FAQ: [https://resources.curve.fi/faq/vote-locking-boost](https://resources.curve.fi/faq/vote-locking-boost)
* Infographie de deFinn sur le boost CRV et la formule: [https://drive.google.com/uc?export=download&id=1DvytXXS0WXmJ65X4jg8vfuT-zWXFxxSk](https://drive.google.com/uc?export=download&id=1DvytXXS0WXmJ65X4jg8vfuT-zWXFxxSk)
* Boost calculator: [https://dao.curve.fi/minter/calc](https://dao.curve.fi/minter/calc)
* Diagram de la statégie proxy Yearn CurveDAO: [https://twitter.com/bantg/status/1308680661801340929](https://twitter.com/bantg/status/1308680661801340929)

