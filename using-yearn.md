# yearnの使い方 

zapと呼ばれる機能のおかげで、入金がとても簡単になりました。どんなトークンでも全てのvaultに入金できます。

こちらが使い方です：

まず、右上のボタンで**ウォレットの接続**を行います。複数の種類のウォレットがサポートされていますが、ほとんどの人は、Chromeの拡張機能として、またはAppleやAndroidのアプリストアを通じて無料でダウンロードできる[MetaMask](https://metamask.io/)を使用しています。ウォレットがイーサリアムのネットワークに接続されていることを確認してください。

<p align="center">
  <img width="1266.75" height="345.75" src="https://i.imgur.com/H0Uc8e8.png">
</p>


## **入金したいvaultに必要なトークン**をすでに持っている場合

1\. 入金したい金庫を選択してください。

2\. vaultに入金したいトークンの量を入力します。ETHを預ける場合は、今後の取引をする際のガス代に十分な量のETHを残しておくようにしてください。

<p align="center">
  <img width="914.26" height="360.75" src="https://i.imgur.com/LGdRAMQ.png">
</p>

3\. Approve前の場合は「Approve」を、Approve済の場合は「入金」ボタンをクリックしてください。

4\. あなたのウォレットが取引の確認を求めます。これには約3分かかりますが、「ネットワークに高いガス料金を支払う」(https://blog.leverj.io/how-to-set-the-gas-limit-and-gas-price-in-metamask-1b33c38c32fd)ことで早くすることができます。トランザクションが止まってしまった場合は、[ガイド](https://metamask.zendesk.com/hc/en-us/articles/360015489251-How-to-Speed-Up-or-Cancel-a-Pending-Transaction)を参照して、トランザクションのスピードアップまたはキャンセルを行ってください。


<p align="center">
  <img width="258.75" height=" 459.75" src="https://i.imgur.com/BkXBANS.png">
</p>

5\. 取引が成功すると、Vaultのインターフェースに入金された残高が表示され、Vaultリストの一番上に表示されます。


<p align="center">
  <img width="928.5" height="93.75" src="https://i.imgur.com/JvNQ3l2.png">
</p>

出金をする場合： 

1\. 出金したい金庫を選択します。

2\. 出金したい金額を入力するか、「Max」をクリックすると残高全体を引き出すことができます。

<p align="center">
  <img width="910.5" height="361.5" src="https://i.imgur.com/Y3NsCRb.png">
</p>

3\. 「Withdraw」をクリックします。

4\. ウォレットが取引の確認を求めてきます。詳細は上記のステップ4を参照してください。

5\. トランザクションが成功すると、トークンは再びあなたのウォレットに表示されます。


## **入金したいVaultに必要なトークン**を持っていない場合。

Yearnの金庫の多くは、[Curve Finance](http://curve.finance/)の流動性プロバイダー(LP)トークンを使用して利回りを得ているため、このようなことはよく起こります。Curveプールに入金することで入手できます。

例えば、ETHのvaultではなくcrvSTETHのvaultに入金し、カーブプールやETHデリバティブ（stETH）による追加リスクを受け入れて高い利回りを得たいが、自分のウォレットにはETHしかない場合、Vaultで受け入れる前にETHをcrvSTETHトークンに変換する必要があります。

ありがたいことに、Yearnの「zap」機能により、この作業はすべて入金と同じトランザクションで行うことができます。ここでは、crvSTETHの保管場所を例にして、その仕組みを説明します。

**注意** トークンをvaultにZappingすると、ネイティブのトークンを預けるよりも多くの取引が必要になります。これは、トークンをスワップしたり、プールに預けたりする際に、より多くのガスを支払うことになり、スリッページによって価値を失う可能性があることを意味します。Yearnはスリッページを1％に制限しており、スリッページがそれを超えるとトランザクションは失敗します。その場合、トークンを手動でスワップまたはデポジットする必要があります。詳細は[zap](https://docs.yearn.finance/yearn-finance/yvaults/overview#zap-in-with-any-asset)の章を参照してください。

1\. crvSTETHのVaultを選択します。

2\. Approve または Deposit ボタンの横にあるドロップダウンボックスをクリックしてください。

3\. crvSTETHに変換したいトークンを選択します。あなたのウォレットに入っているトークンのみが表示されます。

<p align="center">
  <img width="909" height="363" src="https://i.imgur.com/6K1luO7.png">
</p>

4\. 入金したいトークンの金額を入力し、以前にapproveしたかどうかに応じて「approve」または「deposit」をクリックします。

5\. ウォレットを通じて取引を確認します。詳細は、上記セクションのステップ4を参照してください。

6\. トランザクションが成功すると、Vaultのインターフェースに入金された残高が表示され、Vaultリストの一番上に表示されます。

出金する場合： 

1\. crvSTETH Vault を選択します。

2\. 「Withdraw」ボタンの横にあるドロップダウンボックスをクリックします。

<p align="center">
  <img width="915.75" height="600.75" src="https://i.imgur.com/2UyXKN0.png">
</p>

3\. 出金時にどの資産を受け取りたいかを選択します。選択肢は、crvSTETH、ETH、BTC、DAI、USDC、USDTとなります。

4\. 出金したい金額を入力するか、「Max」をクリックして残高全体を引き出すことができます。

5\. 必要に応じて approve を確認し、出金取引を承認してください。

6\. 取引が成功すると、トークンがあなたのウォレットに再び表示されます。


## 資金をチェックするツール 

あなたの資産がvaultに入っている間、米ドルの残高がどのように変化するかを確認したい場合は、あなたのウォレットを[zapper.fi](https://zapper.fi)または同様のポートフォリオ・トラッキングプロダクトに接続してください。これは、Vaultがお客様にどれだけの利益をもたらしたかを知る最も簡単な方法でもあります。

お客様の残高が継続的に増えることはありません。利益は harvest() 関数が呼ばれたときに、あなたの金庫のシェアに分配されますが、これは変動的に起こります。


あなたのリターンをチェックするためのコミュニティリソース:

- [Zapper](https://zapper.fi/)
- [Zerion](https://app.zerion.io/)
- [Yearn Vault ROI Calculator](https://yearn-roi.xyz/#/)
- [yVault ROI](https://yvault-roi.netlify.app/)
- [https://trackavault.com/](https://trackavault.com/)


