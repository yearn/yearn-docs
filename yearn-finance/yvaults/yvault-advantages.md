# Yearn如何为你提高收益

几乎所有与yVaults（机枪池）交互的操作都是开源的。那么，Yearn为何有能力让其用户获得比自行操作更高的收益呢？ 

## Curve Finance协同作用

Yearn的许多策略都利用了Curve Finance的流动性挖矿计划。[Curve Finance](https://curve.fi/)是一个低滑点去中心化交易所，他们为流动性提供者创建了一个可持续300年的代币分配计划。

### veCRV Boosts（提升能力）

CRV会持续地被分发给在Curve的[gauge](https://resources.curve.fi/base-features/understanding-gauges)中持有某些流动性提供者代币的用户。当用户在[Locker](https://dao.curve.fi/locker)（锁币柜）中锁定他们的CRV后，他们所得到的CRV奖励会增加。作为交换，这个Locker会给予质押者veCRV代币，而veCRV将赋予质押者在治理中投票的权利并让他们赚取协议费用的一部分。 

锁定CRV会让用户在符合条件的池中提供流动性时提升他们可获得的CRV奖励。提升的数量将取决于被锁定的CRV数量及其在池中的相对份额。

![](https://i.imgur.com/QaMMdr7.png)

在Backscratcher yVault中，Yearn已无限期地锁定了大量的CRV并将boosts（提升能力）分配给各个yVaults。  

### Backscratcher yVault

Backscratcher yVault以对Curve和Yearn都有利的方式来应用流动性挖矿。 

用户将CRV存入无限锁定的yVault。作为交换，他们会收到一个代表Backscratcher池份额的代币。通过Curve的费用分配，从Curve中获得的收入会被分发到Backscratcher池中，而存款人可以每周赎出他们的份额。 

另外，Yearn Finance赚取的所有CRV的10%会被存入Backscratcher中并无限期地锁定。因此，对于想质押CRV的用户来说，于其在Curve自行质押，他们可通过Backscratcher yVault质押以获得更高的份额。此外，他们还可以通过提供流动性赚取额外的SUSHI和PICKLE等代币。

![](https://i.imgur.com/UfCikwk.png)

用户将永远无法提取他们原来存入的CRV，但由于yveCRV流动性的激励以及代币从各种收入来源产生的价值，他们能够以某种价格将其换成另一种资产。 

作为交换，Yearn将拥有已被锁定的CRV的控制权，并会将得到的boosts（提升能力）分配给各个yVaults。

## 自动复利

在以太坊区块链上的复利操作需要交易费用。这可能会很昂贵并且会减少回报。

由于yVaults将你与许多其他存款人的交易分批进行，因此使用机枪池的成本会更低，而回报会更高。目前，gas费用是由Keep3r网络承担的，这意味着用户可在不承担任何费用的情况下得到自動复利的好处。 

## 杠杆 

Yearn利用Iron Bank（C.R.E.A.M. Finance）来获得用于提高yVault收益的信贷。只有列入白名单的地址才能使用此功能，这意味着普通用户将无法自己执行这个操作。 

一些策略会应用[闪电贷](https://docs.yearn.finance/resources/defi-glossary#flash-loan)，这通常是一种后端操作，需要有开发经验才能利用。 

## 合作关系

多亏于与Curve，SushiSwap和Pickle Finance等协议的合作关系，我们可以实现Backscratcher yVault的优势。我们在DeFi中与其它协议的合作关系让yVault存款人获得他们在其他地方无法获得的好处。

Yearn积极地与以上提到的协议合作开发，旨在创造新的良机并帮助DeFi行业整体的发展。 


