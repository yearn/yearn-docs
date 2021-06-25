# 治理和运营

自[YIP-61：治理2.0](https://gov.yearn.finance/t/yip-61-governance-2-0/10460)于2021年4月25日通过以来, Yearn已开始过渡到 **Multi-DAO(多去中心化自治组织)** 的结构，而这个新结构将由 **约束性的委派(Constrained Delegation)** 来管理。这个流程将使协议开发过程不再受官僚制度的约束，并可继续保持足够的去中心化水平。

Multi-DAO是多种为协议贡献的DAOs（去中心化自治组织）。这些独立的团体是由YFI持有者，yTeams和Multisig组成的。

- **YFI持有者**将为协议更改或治理结构投票
- **yTeams**将专注于协议或相关操作
- **Multisig**成员将执行或否决任何链上的决策

代币持有者对以下体制拥有最终决定权：yTeams的存在，Multisig的成员和各个团队操作控制的局限性。'约束性的委派'一词源于代币持有者将特定权力委托给建立和管理Yearn的各个团队。

以下是简化的治理流程：

    1. YFI持有者创建、销毁和定义yTeams的操作局限性
    2. yTeams将他们的决策通知yTx
    3. yTx创建一个委托交易并将其发送到Multisig
    4. Multisig将执行或否决其交易
    
## DAO职责

![](https://i.imgur.com/cpJP2d5.jpg)

### 代币持有者

[YFI代币持有者](https://docs.yearn.finance/governance/yfi)有责任建议提案并对有利于协议的提案进行投票。

| 提案 | 描述 |
|-----------|--------------|
|Yearn改进提案（YIP）|这是对授予YFI持有人的任何权力，或列举的权力范围之外，执行的提案|
|Yearn委托提案（YDP）|更改离散决策权的委托的提案|
|Yearn信号提案（YSP）|不具约束力的提案，旨在表明社区对任何问题的感受或意图|

具体而言，这些提案允许代币持有者做以下的各个决定：

| 权力 | 描述 |
|-------|-------------|
|管理权力|YFI持有者可以投票以创建，分配或撤销yTeams的离散权力|
|更改YFI代币合约|与YFI代币合约的任何交互，例如铸造YFI或烧毁铸币密钥，均在YFI持有者的控制之下|
|设置费用|在Yearn协议中设置标准费用结构|
|更改Multisig成员|由于Multisig成员在短期内将继续持有关键权力，因此只有YFI持有者可以投票更改Multisig成员|
|批准yTeams|正式批准或废除yTeams以控制哪些yTeams可以拥有授权|
|更改yOps签名者|由于yOps有权更改其他yTeams的签名者，因此这是更改yOps签名者的特殊权力|
|应用财库资金|从财库中支出资金|
|YIP权力|YFI持有者有权对任何尚未委托的事项提出YIP|

### yTeams

每个yTeam都有一个由代币持有者定义的客观和离散的权力。他们可以进一步细分为成员池，而成员池是独立的贡献者团队，他们与总体团队追求相似的目标。此外，一个成员池可以是多个yTeams的一部分。

| yTeam | 目标 | 成员池 |
|-------|-----------|-----------------|
|yGuard|保护机枪池|YFI Protocol Dev，YFI Strategists，YFI Mechanics，YFI Secret Admirers|
|yBrain|管理策略|YFI Strategists|
|yDev|管理协议|YFI Protocol Dev|
|yPeople|管理团队|YFI Compensation Working Group，YFI Advisors|
|yBudget|适宜地分配资金|YFI Finances，YFI Advisors|
|yFarm|增加财库|YFI Secret Admirers，YFI Secret Entrance|
|yTx|编写事务交易|YFI Doers|
|yOps|协调贡献者|YFI Ops|

根据YIP-61的定义，每个团队都被分配了特定的决策权：

| yTeam | 权力 | 描述 |
|-------|-------|-------------|
|yGuard|紧急权力|在受到攻击或出现漏洞的情况下立即干预以对各个策略或机枪池进行关闭或回滚的操作|
|yBrain|管理策略|激活，停用，调整和维护策略|
|yDev|定义Yearn协议|确定哪些代码将被视为Yearn的一部分，哪些不是|
|yDev|管理协议|维护和改进Yearn协议|
|yDev|添加策略|为机枪池添加新策略|
|yTx|委托事务交易|创建委托事务交易并将其发送给multisig以进行签名和执行|
|yPeople|酬劳团队|创建，部署，修改或终止Yearn薪酬方案|
|yBudget|制定预算|为Coordinape，拨款，招聘，运营或其他工作流创建预算|
|yFarm|财库农场操作|应用财库资金进行流动性挖矿，并为有关空投的事宜做决定|
|yOps|批准yTeam签名者|正式批准或删除每个yTeam的签名者|

### Multisig

在一个更加去中心化的系统被批准实施之前，yTeams发布的决定将由Multisig在链上执行。目前，[Multisig](https://docs.yearn.finance/resources/faq#who-is-on-the-multisig)控制以下各个权力：


| 权力 | 描述 |
|-------|-------------|
|执行权|执行YFI持有者和yTeams链上决策的权力|
|否决权|该权力允许Multisig否决任何决定，在理想情况下不应该需要|
|过渡权|一个临时的权力，它使Multisig能够在YIP-41的授权下运作，直到另一套可以涵盖全部所需交易的决策权出现为止|


## 未来的实现

Yearn正在不断为实现DAO去中心化和生产力的理想平衡铺平道路。当前阶段主要的努力是通过社交层面实现改变，未来我们会将其转为软件实现，例如：

- Multisig共识机制，它将允许每个yTeam拥有执行权
- 从代理投票转为链上投票
- 将决策权代币化为NFTs
- 利用[Coordinape](https://coordinape.com/)来完成预算分配和薪劳安排等事项