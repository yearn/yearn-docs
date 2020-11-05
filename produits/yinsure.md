# yInsure

[yInsure](https://yinsure.finance/), également appelée **Cover**, est une couverture de contrat intelligente souscrite par [Nexus Mutual.](https://nexusmutual.io/) Cela est décentralisé et il n'y a pas de KYC requis pour obtenir une couverture. Il se compose de trois éléments: 



* **Les vaults de couverture** détiennent des actifs qui sont utilisés pour payer en cas de sinistre;
*  **Les vaults couverts** détiennent des actifs que le «détenteur de la couverture» désire couvrir, et;
* **Gouvernance des réclamations** qui représente le processus d'arbitrage des réclamations 

 Le système se compose de nombreux acteurs du marché, notamment: 

* **Fournisseurs de couverture:** dépose des fonds dans les vaults de couverture 
* **Titulaires de couverture:** paie des primes afin d'obtenir une couverture pour leurs vaults couverts 
* **Réclamants:** les titulaires de la couverture qui ont une réclamation approuvée et ont droit à un paiement

Bien que la couverture de contrat intelligent puisse fournir une certaine protection contre les risques de contrat intelligent, il ne s'agit pas d'une assurance.



## Les vaults de couverture

Contient les actifs utilisés dans le pool de capitaux, qui peuvent fournir un paiement en cas de réclamation. Le Cover Vaults fonctionne comme suit:

* Les fournisseurs de couverture déposent USDC dans le vault et reçoivent en retour yiUSDC 
* yiUSDC représente le dépôt initial du fournisseur de couverture et finalement la pool de capitaux de couverture.
* Les fournisseurs de couverture reçoivent des frais d'initiation et des primes hebdomadaires   payés par le titulaire de la couverture.
* Si une réclamation est approuvée, l'USDC sera payé sur le coffre-fort au détenteur de la couverture \(demandeur\).

 

## Les vaults couverts

Contient les actifs qui couvrent les détenteurs désireux d'obtenir une assurance. Les voûtes couvertes fonctionnent comme suit:

* Si un détenteur de couverture souhaite obtenir une couverture sur l'USDT, il / elle déposera l'USDT dans le vault de couverte, et en retour recevra des yiUSDT
*  yiUSDT représente le dépôt du détenteur de la couverture et peut être retiré à tout moment. 
* La somme couverte est la valeur de l'actif en dollars lors du dépôt. Le détenteur de la couverture est facturé des frais d'initiation de 0,1% au dépôt et des frais hebdomadaires continus de 0,1%.

la finalité est que les [yVaults](https://yearn.finance/vaults) \(comme yUSD\) puissent être des vaults couverts.

## Gouvernance de réclamation 

Représente le processus d'arbitrage des réclamations. Ce processus fonctionne comme suit:

* Cover holders submit claims by staking the asset they received during deposit \(yiUSDT\).
* Cover providers vote with the assets they received during deposit \(i.e., yiUSDC\) on whether the claim is valid or not.
* If a claim is approved, the cover holder receives the USDC and the cover provider receives the yiUSDT from the cover holder.
* The voting period is three days, requires 33% approvals to pass, and can be vetoed with 25% of the voting power.
* Any tokenized ERC-20 token can be covered. Base assets \(LINK, ETH, etc.\) or composite assets such as aLINK or yaLINK can also be covered.
* If cover providers deny valid claims, cover holders will no longer use the system and ultimately make it unprofitable for cover providers.

{% hint style="info" %}
### Une idée fausse courante: ce n'est pas une assurance **** <a id="9521"></a>

La couverture smart contract souscrite par Nexus Mutual n'est pas un contrat d'assurance. Il s'agit d'une couverture discrétionnaire fournie entre les membres de la mutuelle. Les membres ont l'entière discrétion sur les demandes de paiement. Les membres font confiance au modèle d'incitation économique plutôt qu'à une compagnie d'assurance. En savoir plus en lisant: [Comprendre Nexus Mutual](https://medium.com/nexus-mutual/understanding-nexus-mutual-bb2946dad919).
{% endhint %}

## Resources

* [Page d'accueil de yInsure ](https://yinsure.finance/)
* Article Medium : [yinsure.finance a new insurance primitive](https://medium.com/iearn/yinsure-finance-a-new-insurance-primitive-77d5d4217896)

