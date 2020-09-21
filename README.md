# FAQ \(Chinese\)

资产存入 yearn 是否安全？

* 请自己做好调查，并做决定是否将资产存入 yearn。

yearn 的代码经过审核了吗？

* 代码已经通过审核，查看审核报告请点击以下連結：

  [https://github.com/iearn-finance/audits](https://github.com/iearn-finance/audits)

反馈与支持 如果您有任何问题，请及时联系我们：

* [Discord](https://discord.gg/GcjxhWR)
* [Telegram](https://t.me/yearnfinance)

如果您有任何問題或者发现了任何系統漏洞，请以下面方式联系我们：

* [Github](https://github.com/iearn-finance)-在相关代码库中新增问题
* [Forum](https://gov.yearn.finance/c/feedback/)-在反馈栏中說明

### 产品

[yearn.finance](https://yearn.finance/)

* Yearn.Finance 是我们的使用者介面，為稳健收益,快速兑换,利率汇总,保险，和机枪池等的产品入口

#### 稳健收益\([https://yearn.finance/earn](https://yearn.finance/earn)\)

* 通过智能合约自动寻找最优收益
* 存入 DAI,USDC,USDT,TUSD,SUSD,WBTC 等资产，合约会自动在[Compound](https://compound.finance/)、[Dydx](https://dydx.exchange/)和 [Aave](https://app.aave.com/home)之间寻找最高收益。
* 详细信息可以查询网址[Yearn Docs](https://docs.yearn.finance/yearn.finance/yearn)

#### 快速兑换\([https://yearn.finance/zap](https://yearn.finance/zap)\)

**快速兑换是什么？**

* Zap 仅需要和智能合约交互一次就可以转换支持的代币，减少了交易费用
* Zaps 由 DefiZap 出品，提供 defi 一站式服务，网址为[Zapper.fi](https://zapper.fi)

**为什么使用快速兑换？**

* 快速兑换允许您通过一次交易就建立 DeFi 仓位。

**在 yearn 上可以用快速兑换做什么？**

* 以 DAI 为例，使用快速兑换你进需要一步就可以将 DAI 转化为 yCRV。如果正常操作，你需要首先去 yearn 的稳定收益平台，存入 DAI，收到 yDAI,然后到[Curve.fi - Yearn pool](https://www.curve.fi/iearn/deposit) 存入 yDAI，才会获得 yCRV。

**快速兑换有什么劣势？**

* 比起手动操作每个合约，可能在 Zap 一站式操作合约会消耗更多的 gas 费，但是如果交易量大并且为了节约时间，这里是快速进入 Defi 的通道。

#### 利率汇总\([https://yearn.finance/apr](https://yearn.finance/apr)\)

**什么是利率汇总池？**

* 这里展示了部分 yearn 支持币种的利率。yearn 将会放入收益最高的 Defi 项目方。

#### 机枪池\([https://yearn.finance/vaults](https://yearn.finance/vaults)\)

**什么是机枪池？它与稳健收益池有什么不同？**

* 机枪池使用了更激进的策略获取最高收益。它可以通过合约去获取类似于 CRV 的币种，然后将 CRV 出售给价格最优的去中心化交易所，将比简单的借贷获取更高收益。这些机会是存在的，但是高收益同样要承担高风险。
* Andre 对机枪池的解释可以从以下两篇文章中获取：\([https://medium.com/iearn/yearn-finance-v2-af2c6a6a3613](https://medium.com/iearn/yearn-finance-v2-af2c6a6a3613)\) \([https://medium.com/iearn/delegated-vaults-explained-fa81f1c3fce2](https://medium.com/iearn/delegated-vaults-explained-fa81f1c3fce2)\)
* 对机枪池的简单解释是：
  * 可以为任意资产提供流动性
  * 将流动资产进行质押
    * 在安全范围内管理质押品，因此不会违约
  * 借入稳定币
  * 将稳定币放入到挖矿项目
  * 扣除成本后的收益都将出售为机枪池资产，并将资产返回到机枪池

**可以不通过 yearn 而自己理财吗？**

* 可以。但是机枪池会让你高枕无忧，节约 gas 费用，并且维持健康的质押率，自动获取最高收益。

**我看到的投资回报率是实时的年化回报率吗？**

* 不是。显示的是历史平均回报率。实时年化回报率不会在机枪池测试版中出现。查看每日回报率请点击[twitter](https://twitter.com/iearnfinance)

**风险提示**

* 机枪池中存入的资产不会减少，但是借贷的债务可能增长。如果机枪池策略无法覆盖成本，那部分存入资产可能被锁定，如果机场池策略可以高于债务，存入资产将被解锁。
  * 机枪池中有一些策略可以防止以上事件发生，但任何事都无法确保万无一失。
* 截至目前，机枪池的代码尚未被审核
* 任何与机枪池交互的智能合约都存在风险

**目前运行的机枪池**

* v2 Vaults
* V2 版本机枪池
  * aLINK
  * ChainLink
* v1 Vaults
* V1 版本机枪池
  * Curve.fi/y \(yCRV\)
  * yCRV
  * DAI
  * TUSD
  * USD Coin
    * 你将会收到 yyUSDC。他和你在稳健收益池收到的代币不同，尽管有的人会叫他们同一个币种。
  * USDT

**如果使用 yCRV 在机枪池挖矿，当我提取时会收到挖出的 CRV 吗？**

* 不会。机枪池会挖出 CRV 然后自动出售。当你提取时你会获得更多的 yCRV。

**为什么 yCRVC 不等价于 1 美元，它不是稳定币吗？**

* 以上两个说法都不成立。yCRV 不等于 1 美元，你可以把 yCRV 看成\(yDAI+yUSDC+yUSDT+yTUSD\)一揽子货币指数，它会从 Curve Y 池中得到交易手续费，因此 yCRV 的价值时不断增加的。

**如果将 yCRV 从机枪池中解锁，需要额外的操作把它质押回 Curve 吗？**

* 当你从机枪池解锁 yCRV 后，你将会得到 yCRV+应计利息-费用，全部都用 yCRV 计算。取回 yCRV 后它已经质押在了 Curve 的 Y 池，可以得到手续费收益，不需要任何操作。如果你想得到 CRV，需要质押在以下网址：\([https://dao.curve.fi/minter/gauges](https://dao.curve.fi/minter/gauges)\)

**赎回存入在机枪池的资产后，我将获得哪些收益？**

* 你将会获得存入的币种，具体计算方法为存入币种+机枪池收益-费用。

**alink 的收益如何分配？**

* 存入 alink 后，将收到 yalink 的提供流动性凭证。这代表了当你提取时你可以一并提取 alink 资产赚到的收益。

**为什么机枪池的 yfi 没法获得更高收益？**

* sBTC 和 yCRV 采用了一样的策略放到了 curve 的流动池中。但是没有产品可以让 YFI 安全的挖矿，因此也没有好的策略提升 YFI 收益。

**收费**

* 所有的机枪池费用都一致：0.5%的本金+挖矿收益 5%（更准确的是每次执行收获操作的时候自动扣取 5%收益）。主要用于补充操作的 gas 费用。
* 通过治理可以修改费用比例
* 如果立即存款和取款，将回丢失本金的 0.5%

**收费到了哪里？**

* 他们去了专门的国库合约
  * 地址：[Yearn Treasury Vault](https://etherscan.io/address/0x93A62dA5a14C80f265DAbC077fCEE437B1a0Efde)
* 国库合约中保持了 50 万美元的限额，超过限额将会自动到治理合约
  * 当前地址：[ygov.finance governance staking](https://etherscan.io/address/0xBa37B002AbaFDd8E89a1995dA52740bbC013D992)

**费用原来就打到这些地址吗？**

* 不是，yearn 刚开始时直接打给了 Andre
  * 地址: [0x2d407ddb06311396fe14d4b49da5f0471447d45c](https://etherscan.io/address/0x2d407ddb06311396fe14d4b49da5f0471447d45c)
* 之后我们将费用转移到了多重签名地址
  * 地址：[0xFEB4acf3df3cDEA7399794D0869ef76A6EfAff52](https://etherscan.io/address/0xFEB4acf3df3cDEA7399794D0869ef76A6EfAff52)
* 在我们迁移到治理 V2 版本前，质押收益放在了这个地址。
  * 治理 V1 地址[0xb01419E74D8a2abb1bbAD82925b19c36C191A701](https://etherscan.io/address/0xb01419E74D8a2abb1bbAD82925b19c36C191A701)

**收益率**

* 我们计划推出一个导航页，将会清晰的展示你存入各类资产的年化收益。目前机枪池仍然为测试版，没有显示实时年化利率，但是会在推特中列出每日收益。[twitter](https://twitter.com/iearnfinance)
* 如果你使用 yCRV 机枪池挖 CRV，你可以在 Curve 首页的 Y 池查看收益率\([https://www.curve.fi/](https://www.curve.fi/)\)

#### 机枪池策略

**h4 什么是机枪池策略？**

* Yearn 的机枪池策略是针对每个机枪池制定的模块化智能合约，告诉它要借入什么资产，挖什么代币，在哪里出售挖出的代币。

**当前的策略是什么？**

* 你可以在以下网址查看当前策略[feel-the-yearn](https://feel-the-yearn.vercel.app/)
* 未来我们将制作导航页让机枪池策略和年化收益更简单易懂

**谁在控制机枪池策略？**

* 机枪池策略為 Andre 所寫，但是必須通过多重签名来决定是否可以实施策略。

**我如何创建一个收益策略？**

* 你可以在策略论坛上发布你的策略。详细说明它应该如何买/卖/挖资产和当前的年化收益。将会有一个专门的模板帮助你开始。

**如何将我的策略在 yearn 上实现？**

* 将策略发布在论坛，如果得到批准它将在机枪池執行，而你能獲得些許收入。
* * **机枪池策略什么时候改变，谁来改变，它是自动的吗？**
* 当前 Andre 去查看市场并写策略代码，并且由多签成员查看在高额的收益下代码是否安全，他们根据市场收益变化调整策略。

### [ytrade.finance](https://ytrade.finance/)

* 稳定币交易（测试网）

### [yliquidate.finance](https://yliquidate.finance/)

* 自动清算（测试网）

### [yswap.exchange](https://yswap.exchange/)

* 单边自动做市商（在主网中测试）

### [yborrow.finance](https://yborrow.finance/)

* 信用贷款从智能合约到智能合约

### [yinsure.finance](https://medium.com/iearn/yinsure-finance-a-new-insurance-primitive-77d5d4217896)

* 新型数字货币保险

## 数字代币

### YFI

* Yearn 的官方数字代币
* 仅仅铸造 30000 枚，并且已经全流通
  * 治理可以铸造更多，如果提案通过。

### yTokens

* 当您将资产存入任何 yearn 产品时，您的存入资产将被打包成为 yToken，类似于银行的存钱凭证。
* 举例：当您将 DAI 存入 y.curve.fi 时，您将收到 yDAI。
* yToken 与您存入的资产不是一一对应的，yToken 经过聚合理财后将会增值。
* 如果您将 yToken 继续存入 yearn 产品，您将会收到 yyToken。例如您将 yCRV 存入 vault，您将会收到 yyCRV。

### yCRV

* yCRV 时 yearn 在 Curve.fi Y 池的流动池占比凭证。
* 组成是`yDAI+yUSDC+yUSDT+yTUSD`
* yCRV 代表了您在 Y 池占赚取利息的凭证，组成为 DAI, USDT, USDC 和 TUSD 。
* 如何为 Curve.fi 的 Y 池提供流动性？\([https://guides.curve.fi/how-to-provide-liquidity-on-curve-fi-y-pool/](https://guides.curve.fi/how-to-provide-liquidity-on-curve-fi-y-pool/)\)
  * 长期以来 Curve 的 Y 池已经成为最受欢迎的池子，不仅可以获得高额的交易费用，而且可以在 iearn 上自动从 compound、aave 和 DyDx 上获得最优利率。

### yyCRV

* yyCRV 是用户在 yearn 机枪池存入 yCRV 的流动性凭证。
* 组成是`yyDAI+yUSDC+yUSDT+yTUSD`
* 当你将 yCRV 存入机枪池时将会收到 yyCRV 凭证。
* yCRV 将会继续给您提供收益，同时您将会收到机枪池的收益和支付部分费用。

## 交流

* [Forum](https://gov.yearn.finance/)
  * 在电报和 discord 上可以进行实时沟通，但是进行 yearn 的社区提案需要到 forum 上讨论。
* [Discord](https://discord.gg/94CmMdt)
  * 包含了非英文频道
* [Telegram - Main Chat](https://t.me/yearnfinance)
* [Telegram - Trading/Social/Fork Chat](https://t.me/yearncommunity)
* 推特
  * [yearn.finance - Official Twitter of Yearn](https://twitter.com/iearnfinance?s=20)
  * yearn.finance 的官方推特\([https://twitter.com/iearnfinance?s=20](https://twitter.com/iearnfinance?s=20)\)
  * [Andre Cronje-the leader of developer of Yearn](https://twitter.com/AndreCronjeTech)
  * Andre Cronje-Yearn 的开发团队领导推特\([https://twitter.com/AndreCronjeTech](https://twitter.com/AndreCronjeTech)\)
  * [yLearnfinance - Yearn Info](https://twitter.com/yLearnfinance)
  * Yearn 相关学习知识推特\([https://twitter.com/yLearnfinance](https://twitter.com/yLearnfinance)\)
  * [Learn 2 Yearn - Yearn Info](https://twitter.com/learn2yearn)
  * Yearn 相关信息推特\([https://twitter.com/learn2yearn](https://twitter.com/learn2yearn)\)

## yearn 治理

### 关于 yearn 的社区提案

#### 什么是 yearn 社区提案，为什么他十分重要

* yearn 改善提案帮助 yearn 生态增加功能。用户在论坛中发起提案，充分讨论，并且评估提案通过可能性。如果大量用户同意，那么可以发起链上投票。

#### 通过 yearn 链上提案需要多少票？

* 法定票数要超过总质押票数的 20%才会生效，并且同意票数要超过 50%。
* 您可以现在链上发起提案，但是如果没有经过论坛充分讨论，大家可能不会投票。

#### 如何发起提案？

* 社区提案的模版可以在[Github](https://github.com/iearn-finance/YIPS/blob/master/yip-X.md)和[forum](https://gov.yearn.finance/)找到。如果您在社区或者提案下面发贴，他也会自动加入讨论。
* 大致过程为：

  1.在 forum 上进行讨论

  2.升级到 yip（通常由 mods 完成），添加到社区提案的 github，放到链上。

  3.公布

#### 谁可以发起提案？

* 任何人都可以在 forum 和链上发起提案。

### 投票

#### 如何投票？

* 质押你的 YFI，然后你可以在链上投票[voting dashboard](https://ygov.finance/vote)

#### 在哪里查看 yearn 社区提案？

* 链接 web3 账号后可以在以下网址查看 [voting dashboard](https://ygov.finance/vote)或者 [yips.yearn.finance](https://yips.yearn.finance/all-yip)

  **为什么我需要质押才可以投票？年化收益有多高呢？**

* 你需要质押才可以投票并且可以从 yearn 生态中获取收益。年化收益没有在网站列出，需要在 discord、telegram 里询问。

#### 如何用我的 YFI 获得奖励？

* 你仅需要将 YFI 质押到[ygov.finance/stake](https://ygov.finance/stake)，在国库账户 50 万 usd 之外的收益都会奖励给投票账户。国库的地址为\([https://zapper.fi/dashboard?address=0xFEB4acf3df3cDEA7399794D0869ef76A6EfAff52https://zapper.fi/dashboard?address=0xFEB4acf3df3cDEA7399794D0869ef76A6EfAff52](https://zapper.fi/dashboard?address=0xFEB4acf3df3cDEA7399794D0869ef76A6EfAff52https://zapper.fi/dashboard?address=0xFEB4acf3df3cDEA7399794D0869ef76A6EfAff52)\).
* 如果将 YFI 进行质押投票操作（只要不进入国库地址），你需要投票 3 天后才可以提取收益。

#### 社区投票需要质押 YFI 吗？

是的你必须质押你的 YFI 到 v2 版本的才可以获得有效投票权，质押地址为[ygov.finance/stake](https://ygov.finance/stake) 。你也可以不质押投票，但只是浪费 gas 费，因此投票前必须质押。

#### 可以在投票锁定期尚未结束时拿走 yfi 吗？

* 不可以。在你最近一次投票后需要锁定 3 天，期间 yfi 不可以解除质押。

#### 我已经投票，并且我知道要锁定 3 天，在哪里可以查看确切的解锁 YFI 时间？

* 是的，你可以直接进入到质押投票的合约\([https://etherscan.io/address/0xBa37B002AbaFDd8E89a1995dA52740bbC013D992\#readContract），直接到合约的第 28 项，输入地址，这里会反馈给你一个 eth 的出块数，到达出块数后你就可以解除质押。](https://etherscan.io/address/0xBa37B002AbaFDd8E89a1995dA52740bbC013D992#readContract），直接到合约的第28项，输入地址，这里会反馈给你一个eth的出块数，到达出块数后你就可以解除质押。)

#### 在 forum 上投票和在链上投票有什么不同？

* 在 forum 上仅仅是初步民意测试，在链上的投票具有约束力，通过后将立即执行。

#### 新的无需 gas 费的投票系统怎么运作？

* 我们现在有了一个链下的可以统计到质押资产的投票系统。这个取代了原来 forum 上投票。投票系统仅需要签名就可以做多种选择，并且不需要 gas 费。对于正式的社区提案，我们仍然用链上系统。

#### 如果我质押了 YFI 投票需要锁定多久？

* 你的 YFI 在投票后会被锁定 3 天。

#### 为什么我不可以提取我的质押收益？

* 提取收益需要以下步骤 1.质押 YFI，2.进行了投票 3 天后才可以去提取收益。这个过程将会很快被优化。

### yearn 的自治社区\([https://gov.yearn.finance/t/ydao-for-community-funding/2243](https://gov.yearn.finance/t/ydao-for-community-funding/2243)\)

#### ydao 的目的是什么？

* 用于激励对 yearn 生态系统的增值贡献

#### 谁在意呢？我怎么从这里获取钱？

* 你不可以获得钱。YFI 的捐款将会用于 yearn 的产品开发，你的股份将会被稀释。

#### 谁可以加入？

* 任何人都可以加入，1 股权=0.1YFI

#### 如何加入 yDAO？

* 首先点击网页[Pokemol](https://pokemol.com/dao/0xcb46298767fb5d44c18313976c30d3eeb5071862) ，使用 web3 账户介入，点击右上角新提案按钮，点击会员。
  * 标题：你的名字/公司
  * 说明：“以 X 份的 YFI 换取 Y 份股权”（请确保与 0.1YFI 认购每份股权的金额一致）。
  * 链接：链接到您或您的企业（网站，推特，Linkedin）
  * 请求的股份：请求的股份数- Token Tribute: The amount of YFI being pledged \(you will need to unlock YFI\)
  * 代币捐赠：认捐的 YFI 数量（您需要解锁 YFI）- Loot: The number of shares being requested
  * 股份：请求的股份数量
  * 提交两项交易并进入新的成员队列后，您将需要一个支持者。请复制链接到您的提案，让我们知道您想加入\[yDAO 电报频道\]（[https://t.me/joinchat/Qn1GPBv0y7lY1vAmRCB7KA）](https://t.me/joinchat/Qn1GPBv0y7lY1vAmRCB7KA）)

#### 如何申请资金？

* 与加入方式相同，除了点击成员以外，点击资金标签，然后填写您的请求详细信息。如果您有任何疑问，可以在\[电报聊天\]（[https://t.me/joinchat/Qn1GPBv0y7lY1vAmRCB7KA）中询问。](https://t.me/joinchat/Qn1GPBv0y7lY1vAmRCB7KA）中询问。)

#### 我不会说英语，什么时候会提供翻译呢？

* 我们正在致力于将 yearn 产品翻译成为不同语言，但是它需要时间。现在你可以在这里寻找自己的母语[Discord](https://discord.gg/94CmMdt)。

## 交流

### IAndre 是 yearn 的负责人吗？

* Andre 并不是 yearn 的负责人，YFI 代币持有人决定 yearn 的生态，Andre 是 yearn 生态的开发者领导

### Andre 主要做什么？

* Andre 是 yearn 生态系统产品开发的核心成员，主要内容有：收益、交易、闪兑、清算、借贷。他还负责运行和监督机枪池。

  **什么是多重签名？他们主要做什么？**

* 多重签名的地址详细内容可以点击网站找到\([https://gov.yearn.finance/t/yfi-minting-ownership/155\)。他主要是控制 YFI 的铸造，签名生效需要 9 个人中的 6 个人签名。](https://gov.yearn.finance/t/yfi-minting-ownership/155%29。他主要是控制YFI的铸造，签名生效需要9个人中的6个人签名。)

### 9 位负责多重签名的负责人是谁？

* [Calvin Liu](https://twitter.com/cjliu49/status/1285439553180798976?s=21)
* [Coopahtroopa](https://twitter.com/Cooopahtroopa/status/1285438650550038529)
* [Cp0x.com](https://twitter.com/kaplansky1/status/1285427247286046725)
* [Curve.fi](https://twitter.com/CurveFinance/status/1285428322986389504)
* [Damir Bandalo](https://twitter.com/damirbandalo/status/1285500362015875073?s=20)
* [Daryllautk](https://twitter.com/Daryllautk/status/1285434908383444992)
* [Devops199fan](https://twitter.com/devops199fan/status/1285430347954622464)
* [Banteg](https://twitter.com/bantg/status/1285426492906909696)
* [Milkyklim](https://milkyklim.keybase.pub/yearn-social-proof.txt)
* [Calvin Liu](https://twitter.com/cjliu49/status/1285439553180798976?s=21)
* [Coopahtroopa](https://twitter.com/Cooopahtroopa/status/1285438650550038529)
* [Cp0x.com](https://twitter.com/kaplansky1/status/1285427247286046725)
* [Curve.fi](https://twitter.com/CurveFinance/status/1285428322986389504)
* [Damir Bandalo](https://twitter.com/damirbandalo/status/1285500362015875073?s=20)
* [Daryllautk](https://twitter.com/Daryllautk/status/1285434908383444992)
* [Devops199fan](https://twitter.com/devops199fan/status/1285430347954622464)
* [Banteg](https://twitter.com/bantg/status/1285426492906909696)
* [Milkyklim](https://milkyklim.keybase.pub/yearn-social-proof.txt)

### Andre 可以做哪些决定？

* Andre 能够建设 Yearn 生态并且提出新的产品。通常他会把自己的想法和建议放在 forum 上让大家查看。\([https://gov.yearn.finance/](https://gov.yearn.finance/)\)

### 多重签名小组会告诉 Andre 需要做什么吗？

* 多重签名小组之间的联系非常紧密，但是 Andrew 会将 YFI 代币持有人的决定放在首位。

### 谁还在为 yearn 写代码？有一个团队吗？

* 目前代码贡献者仅仅为 Andre。

### 在 yearn 上工作会获得报酬吗？

* 当前还不会。但庆幸的是我们通过了 36 号社区提案\([https://yips.yearn.finance/YIPS/yip-36](https://yips.yearn.finance/YIPS/yip-36)\) ，建立了一个社区资金池，规模是 50 万 usd，我们现在可以为 Andre 支付工作报酬，代码审核资金，雇佣社区开发人员以及其他 yearn 生态需要的费用。

### 我如何参与 yearn 的工作呢？

* 你可以直接发起提案申请资金，或这直接向 ydao 申请资金。

### yearn 需要工作人员吗？

* 是的，我们需要各种人来帮助 yearn 生态系统丰富产品，使它成为蓬勃发展，并为 YFI 赋予价值。您可以在 Discord 或 Telegram 中询问或者在 forum 上发布信息。说明您认为可以为 Yearn 增值的方式，以及您认为应该从社区池中获得多少收益。此外，你可以到 ydao 申请资金支持\([https://gov.yearn.finance/t/ydao-for-community-funding/2243](https://gov.yearn.finance/t/ydao-for-community-funding/2243)\)

### 如何参与 yearn 生态？

* 您可以直接使用您的 yfi 为社区提案投票，在论坛上讨论社区提案，参与电报和 discord 的讨论。如果你懂第二种语言，你可以帮助我们把社区提案翻译成对应的语言。

### 如何参与改善 yearn 生态系统？

* 你可以点击以下链接为活跃的社区提案投票。\([https://yips.yearn.finance/all-yip](https://yips.yearn.finance/all-yip)\)

## 用户界面

### 可以在手机上参与 Yearn 生态吗？

* 可以的，您连接钱包时选择 Metamask 选项就可以

## 相关项目

### [Curve](https://www.curve.fi/)

* Curve 是以太坊上的一个交易所流动性池（例如\[Uniswap\]（[https://app.uniswap.org/\#/）），旨在（1）高效稳定的代币交易（2）低风险，为流动性提供者提供的补充费用收入，](https://app.uniswap.org/#/）），旨在（1）高效稳定的代币交易（2）低风险，为流动性提供者提供的补充费用收入，) 没有机会成本。 Curve 允许用户（以及智能合约，如 1inch，Paraswap，Totle 和 Dex.ag）在 DAI 和 USDC 之间进行交易，其定制的低延误，低价算法专门针对稳定币而设计，并能赚取费用。 在后台，流动资金池也被提供给 Compound 协议或 yearn.finance，在此它为流动资金提供者带来甚至更多的收入。
* Curve 的 FAQ 网址\([https://www.curve.fi/rootfaq](https://www.curve.fi/rootfaq)\)

### [Aave](https://app.aave.com/home)

[Aave](https://app.aave.com/home)

* Aave 是开源协议并且没有中心化托管的货币借贷市场。用户可以获取存款利息或者借入资产

## 学习资源

### yearn 相关教学

* [Learn Yearn](https://www.learnyearn.finance/)
* [Medium.com/iearn](https://medium.com/iearn)
* [yCosystem](https://ycosystem.info/)

### 智能合约清单

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
* [Strategy for USDC vault](https://etherscan.io/address/0xA30d1D98C502378ad61Fe71BcDc3a808CF60b897)
* [DAI vault](https://etherscan.io/address/0xACd43E627e64355f1861cEC6d3a6688B31a6F952)

### 代币和合约信息

* [https://docs.yearn.finance/yearn.finance/yearn-1](https://docs.yearn.finance/yearn.finance/yearn-1)

### 机枪池详细信息

* [https://vaults.finance/](https://vaults.finance/)

### 数据统计

* [yieldfarming.info](https://yieldfarming.info/)
* [yVault ROI Calculator](https://py-earn.herokuapp.com/)
* [stats.finance/yearn](https://stats.finance/yearn)
* [Feel The Yearn](https://feel-the-yearn.vercel.app/)
* Yearn Initial Distribution [Dune Dashboard](https://explore.duneanalytics.com/dashboard/yearn)
* Voting Stats [Dune Dashboard](https://explore.duneanalytics.com/public/dashboards/Lqnxzm7fa8NVhKC4kc37DDFPZgqXryaIjyLRYAYp)

### 最近新闻

* [yearn.finance - Offical Twitter of Yearn](https://twitter.com/iearnfinance)
* [AndreCronjeTech](https://twitter.com/AndreCronjeTech)
* [Yearn Finance - Offical Blog](https://medium.com/iearn)

### 视频采访

* [Andre Cronje and the Philosophy of Yearn Finance](https://anchor.fm/hasu-research/episodes/6-Andre-Cronje-and-the-Philosophy-of-Yearn-Finance-ei4vds)
* [The FTX Podcast - Andre Cronje DeFI Architect](https://open.spotify.com/episode/6d14TJtQU7eB69azelpdeh)
* [Zapper Community Call - With Andre](https://www.youtube.com/watch?v=venoiaiVZ-U)
* [In DeFi My Money is Actually Mine. Its a Beautiful Concept But it Comes With Responsibilities - Andre Cronje](https://anchor.fm/camila-russo/episodes/In-DeFi-My-Money-is-Actually-Mine--Its-a-Beautiful-Concept-But-it-Comes-With-Responsibilities-Andre-Cronje-ehs3op)
* [YFI: Farming the Farmers \| Andre Cronje](http://podcast.banklesshq.com/25-king-of-the-yield-farmers-andre-cronje)

### 博客文章

* [Yearn Finance - Offical Blog](https://medium.com/iearn)
  * [Yinsure.finance: A new insurance primitive](https://medium.com/iearn/yinsure-finance-a-new-insurance-primitive-77d5d4217896)
  * [Delegated Vaults Explained](https://medium.com/iearn/delegated-vaults-explained-fa81f1c3fce2)
  * [Yearn.finance v2](https://medium.com/iearn/yearn-finance-v2-af2c6a6a3613?source=---------3------------------)
  * [Yearn Governance Forum](https://medium.com/iearn/yearn-governance-forum-7b7c9d0300ac?source=collection_home---6------2-----------------------)
  * [YFI rewards pool](https://medium.com/iearn/yfi-rewards-pool-810ef9256ec6)
  * [YFI](https://medium.com/iearn/yfi-df84573db81)

### 商标

* Can be found in the discord under [\#media-resources](https://discord.com/channels/734804446353031319/736132884443955242/740325105904779326)
* 可以在 discord 的\[\#media-resources\]频道找到\([https://discord.com/channels/734804446353031319/736132884443955242/740325105904779326](https://discord.com/channels/734804446353031319/736132884443955242/740325105904779326)\)

（翻译：林明）

