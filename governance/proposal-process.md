# 提案のプロセス

Yearnのエコシステムは、YFIトークン保有者がエコシステムを支配するオフチェーン提案を提出し、投票することで管理されています。多数の支持（投票率50％以上）を得た提案は、9人のメンバーによるマルチシグネチャーウォレットによって実行されます。

変更を実行するには、ウォレットの署名者9名のうち6名の署名が必要です。[マルチシグネチャーウォレットのメンバー](https://docs.yearn.finance/resources/faq#who-is-on-the-multisig)は、YFIホルダーの投票により決定されたものであり、今後のガバナンス投票により変更される可能性があります。

# ディスカッション

プロトコルの変更に関するディスカッションは、以下のように様々なプラットフォームで行われます。

 - [ガバナンスフォーラム](https://gov.yearn.finance/)
 - [Discord](https://discord.yearn.finance)
 - [Telegram](https://t.me/yearnfinance)

正式な提案をする前に、様々なコミュニケーションのチャンネルからできるだけ多くのフィードバックを得ることをお勧めします。ガバナンスフォーラムとDiscordサーバーには、特定のトピックのための専用チャンネルが用意されています。

# 提案

## 提案の種類

**Yearn Improvement Proposals** (YIPs) は、トークン・ホルダーに与えられた権限を行使するための包括的な手段です。  [YIP-61](https://gov.yearn.finance/t/yip-61-governance-2-0/10460)以降、 **Yearn Delegation Proposals** (YDPs) が導入され、トークン・ホルダーが個別に意思決定権の委譲先を変更することができるようになりました。

![](https://i.imgur.com/ZRNp2Zq.png)

### 過去の提案と現在の提案
- 過去: [提案リポジトリ](https://docs.yearn.finance/governance/proposal-repository)
- 現在: [スナップショット](https://snapshot.page/#/yearn) 

### 提案を通すための条件
- [フォーラム]での3日間のディスカッション(https://gov.yearn.finance/)
  - 少なくとも25%以上の変更に賛成する投票
- スナップショットに提出するYFIを1枚保有
- 5日間の[スナップショット](https://snapshot.org/#/ybaby.eth)で50%以上の通過票を獲得

## 提案の作成

誰でもフォーラムに提案を投稿して、コミュニティ内で議論することができます。提案がオフチェーン投票（[Snapshot](https://snapshot.page/#/yearn)経由）に進んだ場合、YFIを1つ持っている人だけがSnapshotに投稿できます。あなたの提案がオフチェーンでの投票に進み、十分なYFIを持っていない場合は、管理者があなたをサポートします。

提案のデフォルトテンプレートは[Github](https://github.com/yearn/YIPS/blob/master/yip-X.md)と[フォーラム](https://gov.yearn.finance)にあります。提案や議論に投稿すると、テンプレートが自動入力されます。

**資料**:
- [提案の方法](https://gov.yearn.finance/t/proposal-how-to/106)
- [YIP 0: YIPの目的とガイドライン](https://yips.yearn.finance/YIPS/yip-0)
- [YIP 44: YIPカテゴリーの改善](https://yips.yearn.finance/YIPS/yip-44)
- [YIP 55: YIP導入・投票プロセスの正式化](https://gov.yearn.finance/t/yip-55-formalize-the-yip-process/7959)

# 投票

## 投票の方法

- 以下の場所でYFIを保有またはステーキングすることで、Yearnの[Snapshot](https://snapshot.page/#/yearn)ページへの投票が可能になります。:
	- 自分のウォレット
	- YFI yVault V2 (yvYFIトークンを持っているのと同じ状態)
	- Balancer YFI/WETH LP token
	- Uniswap YFI/WETH LP token
	- Sushiswap YFI/WETH LP token staked in MasterChef
	- MakerDAO YFI collateral
	- Unit Protocol YFI collateral
	- Bancor

## フォーラムでの投票とオフチェーンでの投票の違い

- 投票は、コミュニティがその提案に対してどのように感じているかという気持ちを測るだけですが、オフチェーンでの投票（[Snapshot](https://snapshot.page/#/yearn)経由）は拘束力があり、可決された場合には有効となります。

# 実装

スナップショットの投票が成立すると、変更はYearnのプロトコルチームやオペレーションチームによって実行され、必要に応じてマルチシグによって署名されます。