# Comme créer un YIP

## Résumé

Les propositions d'amélioration \(`YIP` pour  yEarn Improvement Proposals\) décrivent les normes de la plate-forme yEarn, notamment les spécifications de  de base du protocole, les clients API  et les normes contractuelles. Il s'agit de la spécification de référence `canonical` définitive pour la logique centrale.

## Contribuer

1. Lisez [YIP-0](https://github.com/iearn-finance/YIPS/blob/master/YIPS/yip-0.md).
2. Dupliquez le répertoire en cliquant sur "Fork" en haut a droite.
3. Ajoutez votre YIP a votre duplication du répertoire. Il y a un [exemple type ici](https://github.com/iearn-finance/YIPS/blob/master/yip-X.md). 
4. Soumettez "Pull Request" au [YIPSs repertoire](https://github.com/iearn-finance/YIPS/) de yEarn's.

Your first PR should be a first draft of the final YIP. It must meet the formatting criteria enforced by the build \(largely, correct metadata in the header\). An editor will manually review the first PR for a new YIP and assign it a number before merging it. Make sure you include a `discussions-to` header with the URL to a new thread on [gov.yearn.finance](https://gov.yearn.finance/) where people can discuss the YIP as a whole.

> Note: It is important that their be community support behind a proposed `YIP` - It is up to the author\(s\) to shepard their proposal through the process.

If your YIP requires images, the image files should be included in a subdirectory of the `assets` folder for that YIP as follow: `assets/yip-X` \(for yip **X**\). When linking to an image in the YIP, use relative links such as `../assets/yip-X/image.png`.

When you believe your YIP is mature and ready to progress past the WIP phase, you should ask to have your issue added to the next governance call where it can be discussed for inclusion in a future platform upgrade. If the community agrees to include it, the YIP editors will update the state of your YIP to 'Approved'.

## YIP Statuses

* **WIP** - a YIP that is still being developed.
* **Proposed** - a YIP that is ready to be reviewed in a governance call.
* **Approved** - a YIP that has been accepted for implementation by the yEarn community.
* **Implemented** - a YIP that has been released to mainnet.
* **Rejected** - a YIP that has been rejected.

### Example YIP

```diff
-Status: Proposed
+Status: Approved
YIP: integer,
Created: 2020-09-01
-Last-Modified: 2020-09-03
+Last-Modified: 2020-09-08
```

## Validation

YIPs MUST pass some validation tests. The YIP repository ensures this by running tests using [html-proofer](https://rubygems.org/gems/html-proofer) and [yip\_validator](https://rubygems.org/gems/yip_validator).

It is possible to run the YIP validator locally:

```ruby
gem install yip_validator
yip_validator <INPUT_FILES>
```

## Copyright

Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).

