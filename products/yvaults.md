# yVaults

L'objectif des Vaults est de permettre à la communauté de créer et d'utiliser rapidement et en toute sécurité les robots agricoles \( yield farming robots \) avec les rendements les plus efficaces, créés par les meilleurs stratèges de l'industrie.

Les yVaults ont des frais de retrait de 0,5% et des frais de 5% sur le rendement supplémentaire chaque fois que la fonction `harvest()`  est appelée, voir la [FAQ](https://docs.yearn.finance/faq#quels-sont-les-frais) pour plus de détails. Les bénéfices individuels sont répartis au prorata, déterminé par la part de chaque déposant dans la pool.

### Les yVaults disponibles

Il existe actuellement neuf yVaults. Vous pouvez y accéder ici: [https://yearn.finance/vaults](https://yearn.finance/vaults) 1. 1. ETH/WETH 2. YFI 3. yDAI+yUSDC+yUSDT+yTUSD \(yCRV\) 4. crvBUSD 5. crvBTC 6. DAI 7. TUSD 8. USDC 9. USDT

Les jetons identifiés ci-dessus sont déposés dans leurs yVaults respectifs et utilisés pour farmer en utilisant les opportunités actuelles sur le marché.

 Les vaults sont créés et gérés par un contrôleur, qui supervise l'exécution de la stratégie. Les bénéfices générés par chaque  vault  sont utilisés pour acheter davantage d'actif sous-jacent dans chaque vault \(par exemple, les bénéfices du vault YFI sont utilisés pour acheter des YFI supplémentaires\); _par conséquent, les coffres représentent une stratégie d'achat et de conservation continue \(buys-and-hold\)._

### Méchanisme du Vault yETH  

Le contrôleur ouvre une position de dette colatéralisée  \(CDP = colleratlized debt position \) sur MakerDAO en utilisant l'ETH comme garantie et génere  le DAI. Ce DAI est déposé dans le vault yDAI. Le ratio de garantie - une mesure de levier financier - doit toujours être d'au moins 200%. Les robots automatisés remboursent périodiquement la dette en DAI si le ratio tombe en dessous de 200%. Le DAI est échangé sur  [Curve](https://www.curve.fi/) et n'est pas acheté sur le marché libre \(c'est-à-dire que le yDAI est brûlé et échangé contre du DAI\). L'excédent de DAI obtenu grâce à l'agriculture de rendement est utilisé pour acheter de l'ETH supplémentaire, qui est déposé dans le vault yETH.

![](https://i.imgur.com/ZASptpX.png)

### Les yVaults délégués

Les actifs volatils peuvent également participer à des stratégies d'agriculture de rendement dans le cadre de produit délégué yVault. Actuellement, il n'y a qu'un seul yVault délégué: le aLINK. 

Les bénéfices générés par le yVault délégué sont utilisés pour acheter davantage de l'actif sous-jacent. Représentant à nouveau une stratégie d'achat et de conservation continue \(_continuous buy-and-hold strategy\)_, permettant au depositaire de rester exposé à 100% à l'actif. Les depositaire peuvent retirer leurs dépôts initiaux et les bénéfices accumulés, le cas échéant, à tout moment, moyennant des frais de 0,5% prélevés sur le dépôt.

#### Méchanisme

Le contrôleur dépose du LINK dans AAVE et emprunte des stablecoins. Si à tout moment le health factor tombe en dessous de la valeur configurée du vault\(actuellement définie sur 2\), le contrôleur rembourse une partie de la dette afin de maintenir un health factor au-dessus de sa valeur configurée. 

Les stablecoins empruntés \(par exemple, USDC, DAI, USDT, etc.\) dépendent de la stratégie choisie par le contrôleur. Après avoir obtenu des stablecoins, le contrôleur les déposera dans l'un des yVaults indiqués ci-dessus.

![](https://i.imgur.com/8AVJU0d.png)

## Resources

* [Vaults Homepage](https://yearn.finance/vaults)
* Article sur Medium: [yETH vault explained](https://medium.com/iearn/yeth-vault-explained-c29d6b93a371)
* Article sur Medium: [Delegated Vaults Explained](https://medium.com/iearn/delegated-vaults-explained-fa81f1c3fce2)

