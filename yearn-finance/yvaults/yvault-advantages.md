#  Yearnが利回りを増やす方法

yVaultsが扱うものは、ほとんどすべてが公開されています。では、Yearnはどのようにしてユーザーが自力で実現できる以上の利回りを提供しているのでしょうか？

## Curve Finance との相乗効果

Yearnの戦略の多くは、Curve Financeのリクイディティマイニングプログラムを利用しています。[Curve Finance](https://curve.fi/)は、低スリッページの分散型取引所に流動性を提供した人に300年かけてトークンを配布するプログラムを持っています。

### veCRV Boosts について

CRVは、Curveの[gauge](https://resources.curve.fi/base-features/understanding-gauges)に特定の流動性を提供したユーザーに継続的に配布されます。これらのCRVの報酬は、ユーザーが自分のCRVを[Locker](https://dao.curve.fi/locker)にロックすることで増やすことができます。このLockerは、代わりにステークホルダーにveCRVを与え、ガバナンスへの投票権とプロトコルの手数料の一部を請求する権利があります。

CRVをロックすることで、ユーザーは適格なプールで流動性を提供する際に受け取るCRV報酬を高めることができます。ブーストの量は、ロックされたCRVの量と、プールにおける相対的なステーク比率によって決まります。

![](https://i.imgur.com/QaMMdr7.png)

YearnはBackscratcherのyVaultを使って膨大な量のCRVを無期限にロックしており、ブーストを様々なyVaultに分配しています。

### Backscratcher yVault について

Backscratcher yVaultは、CurveとYearnの両方にメリットのある方法で流動性マイニングを利用しています。

ユーザーはCRVをyVaultに預け、無期限にロックします。その代わりに、Backscratcherプールのシェアを表すトークンを受け取ります。Curveで得られた収益は、Backscratcherのプールに分配され、入金者は週単位で請求することができます。

さらに、Yearn Financeが獲得した全CRVの10％がBackscratcherに入金され無期限にロックされます。このため、CRVをステークしたい人は、Curveに直接ステークするよりも、BackscratcherのyVaultにステークした方が常に高いシェアのBackscratcher yVaultの収益を受け取ることができます。また、流動性を提供することで、SUSHIやPICKLEなどのトークンの排出権を得ることができます。

![](https://i.imgur.com/UfCikwk.png)

ユーザーは元のCRVを引き出すことはできませんが、yveCRVの流動性に対するインセンティブと、様々な収益源から発生するトークンの価値により、ある価格で別の資産と交換することができます。

その報酬として、ロックされたCRVのブーストに対するコントロールがYearnに与えられ、様々なyVaults全体で活用されます。

## 自動複利の金利 

利回りを複利化するには、イーサリアムのブロックチェーンに取引手数料を支払う必要があります。これはコストがかかり、リターンを削ることになります。

yVaultは、あなたの取引を他の多くの預金者と一括で行うため、Vaultを使うことで累積的に低コストかつ高リターンの利回りを得ることができます。現在、ガス代はKeep3rネットワークが負担しているため、ユーザーはコストを負担せずにリターンを得ていることになります。

## レバレッジ

Yearnは、Iron Bank（C.R.E.A.M.ファイナンス）を利用して、yVaultの利回りを高めるために使用されるクレジットにアクセスしています。この機能を利用できるのは、ホワイトリストに登録されたアドレスのみであり、通常、個人ではこの機能を利用することはできません。

また、一部の戦略では[フラッシュローン](https://docs.yearn.finance/resources/defi-glossary#flash-loan)を導入していますが、これはバックエンドサービスの一種であり、活用するには開発経験が必要です。

## パートナーシップ

BackscratcherのyVaultは、Curve、SushiSwap、Pickle Financeなどのプロトコルとの相乗的な関係があってこそ成り立つものです。DeFi全体での関係により、yVaultの預金者は他では得られないメリットを得ることができます。

Yearnは、利回りの新しい機会を作り、業界としてのDeFiをさらに発展させるために、上記のようなプロトコルと積極的に共同開発を行っています。


