# Comme créer un YIP

## Résumé

Les propositions d'amélioration \(`YIP` pour  yEarn Improvement Proposals\) décrivent les normes de la plate-forme yEarn, notamment les spécifications de  de base du protocole, les clients API  et les normes contractuelles. Il s'agit de la spécification de référence `canonical` définitive pour la logique centrale.

## Contribuer

1. Lisez [YIP-0](https://github.com/iearn-finance/YIPS/blob/master/YIPS/yip-0.md).
2. Dupliquez le répertoire en cliquant sur "Fork" en haut a droite.
3. Ajoutez votre YIP a votre duplication du répertoire. Il y a un [exemple type ici](https://github.com/iearn-finance/YIPS/blob/master/yip-X.md). 
4. Soumettez "Pull Request" au [YIPSs repertoire](https://github.com/iearn-finance/YIPS/) de yEarn's.

Votre premier PR \(public relation, publication\)devrait être une première ébauche du YIP final. Il doit répondre aux critères de mise en forme imposés par la construction \(en grande partie, des métadonnées correctes dans l'en-tête\). Un éditeur examinera manuellement le premier PR pour un nouveau YIP et lui attribuera un numéro avant de le fusionner. Assurez-vous d'inclure un en-tête une `discussions-to` avec l'URL d'un nouveau fil sur [gov.yearn.finance](https://gov.yearn.finance/)  où les gens peuvent discuter du YIP dans son ensemble.

> Remarque: Il est important qu'il y est un soutient à la communauté lorsque un `YIP`est proposé - Il appartient aux auteurs de présenter leur proposition tout au long du processus.

Si votre YIP nécessite des images, les fichiers image doivent être inclus dans un sous-répertoire du dossier `assets` pour ce YIP comme suit: `assets/yip-X` \(for yip **X**\). Lorsque vous créez un lien vers une image dans le YIP, utilisez des liens relatifs tels que `../assets/yip-X/image.png`.  
  
 Lorsque vous pensez que votre YIP est mature et prêt à passer au-delà de la phase WIP, vous devriez demander que votre publication soit ajoutée au prochain appel de gouvernance où il pourra être discuté pour être inclus dans une future mise à niveau de la plateforme. Si la communauté accepte de l'inclure, les éditeurs YIP mettront à jour l'état de votre YIP en «Approuvé».

## Les status des YIPs 

* **WIP** - un YIP qui est toujours en court de développement 
* **Proposed** - un YIP qui est prêt à être examiné pour la gouvernance au cours d'un "governance call".
* **Approved** - un YIP dont la mise en œuvre a été acceptée par la communauté yEarn
* **Implemented** - un YIP qui a été publié sur le mainnet.
* **Rejected** - un YIP qui a été rejeté.

### Example de YIP

```diff
-Status: Proposed
+Status: Approved
YIP: integer,
Created: 2020-09-01
-Last-Modified: 2020-09-03
+Last-Modified: 2020-09-08
```

## Validation

Les YIPs DOIVENT passer des tests de validation. Le dépositaire du YIP réalise cela en exécutant des tests en utilisant [html-proofer](https://rubygems.org/gems/html-proofer) et [yip\_validator](https://rubygems.org/gems/yip_validator).

Il est possible d'exécuter le validateur YIP localement:

```ruby
gem install yip_validator
yip_validator <INPUT_FILES>
```

## Copyright

Copyright and droits connexes abandonnés via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).

