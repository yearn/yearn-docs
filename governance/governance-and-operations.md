# 治理和运营

自[YIP-61: 治理 2.0](https://gov.yearn.finance/t/yip-61-governance-2-0/10460) 于2021年4月25日通过以来, yearn开始向 **多DAO（Multi-DAO）** 结构过渡，由 **约束委派（Constrained Delegation）** 进行管理。这种方法允许协议开发不受官僚主义的束缚，同时保持足够的权力下放水平。

多DAO是指不稳定数目的，以某种独特方式为协议做出贡献的去中心化自治组织 (Decentralized Autonomous Organizations, DAOs)。这些独立的团队由YFI持有者、yTeams和多签成员组成。

- **YFI持有者** 对协议或协议治理结构的变更进行投票选举
- **yTeams** 侧重于协议或相关操作的特定方面
- **多签** 成员执行或否决任何链上决策

代币持有者对yTeams的存在，谁是多签的一部分，以及每个团体操控的限制有着最终决定权。“约束委派”一词源于代币持有者将特定权力下放给建立和管理代币的各种团体。

治理的简化流程如下所示：

    1. YFI持有者创建、销毁yTeams以及定义对其的限制
    2. yTeam通知yTx一项决定
    3. yTx创建委托事项并发送给多签成员
    4. 多签成员执行或否决事项
    
## DAO 职责

![](https://i.imgur.com/IDysF5O.png)

### 代币持有者

[YFI代币持有者](https://docs.yearn.finance/governance/yfi)有责任创建并票选出改进协议的提案。

| 提案 | 描述 |
|-----------|--------------|
|Yearn改进提案 (YIP)|该提案使得授予给YFI持有者的任何权力或超出列举权力范围的任何权力生效|
|Yearn委托提案 (YDP)|该提案变更了任何单独的决策权被委托的位置|
|Yearn信号提案 (YSP)|一个不具约束力的提案，表明社区对任何问题的感受或意图|

具体而言，这些提案允许代币持有者做出以下决定：

| 权力 | 描述 |
|-------|-------------|
|管理权力|YFI持有者可以投票创建、分配或撤销yTeams的单独权力|
|变更YFI代币合约|任何与YFI代币合约的交互，例如铸造YFI或烧毁铸币密钥，均由YFI持有者控制。|
|设置费用|在Yearn协议中设置标准费用结构|
|更改多签成员|由于多签成员在近期将继续持有关键权力，因此只有YFI持有者可以投票更改多签成员|
|批准yTeams|正式批准或废除yTeams，以控制哪些yTeams可以拥有授权|
|更改yOps签名者|由于yOps有权更改其他yTeams的签名者，因此该权力是更改yOps签名者的特殊权力|
|花费国库资金|花费国库中的资金|
|YIP权力|YFI持有者有权对任何尚未委托的事项提出YIP|
### yTeams

每个yTeam都有一个由令牌持有者定义的，客观的，单独的权力。它们可以进一步细分为成员池，成员池是一组独立的贡献者，他们致力于实现与总体团队相似的目标。此外，一个成员池可以成为多个yTeam的一部分。

| yTeam | 目标 | 成员池 |
|-------|-----------|-----------------|
|yGuard|保护机枪池|YFI Protocol Dev, YFI Strategists, YFI Mechanics, YFI Secret Admirers|
|yBrain|管理策略|YFI Strategists|
|yDev|管理协议|YFI Protocol Dev|
|yPeople|管理团队|YFI Compensation Working Group, YFI Advisors|
|yBudget|合理开支|YFI Finances, YFI Advisors|
|yFarm|发展国库|YFI Secret Admirers, YFI Secret Entrance|
|yTx|编写事务|YFI Doers|
|yOps|协同贡献者|YFI Ops|

每个yTeam都有特定的决策权，由YIP-61定义：

| yTeam | 权力 | 描述 |
|-------|-------|-------------|
|yGuard|紧急权力|在受到攻击或出现漏洞的情况下立即干预关闭或回滚策略或机枪池|
|yBrain|管理策略|激活、停用、调整和维护策略|
|yDev|定义Yearn协议|确定哪些代码被视为Yearn的一部分，哪些不是|
|yDev|管理协议|维护和完善Yearn协议|
|yDev|添加策略|为机枪池添加新策略|
|yTx|委托事务|为多签成员创建委托事务以进行签名和执行|
|yPeople|酬劳团队|创建、部署、修改或终止Yearn薪酬|
|yBudget|制定预算|为协调、拨款、招聘、运营或其他工作流创建预算|
|yFarm|耕作国库|用国库进行流动性挖矿，并决定空投事宜|
|yOps|批准yTeam签名者|正式批准或删除每个yTeam的签名者|

### 多签成员

yTeams发布的决策将由多签成员在链上执行，直到一个更加去中心化的系统被批准实施。同时，[多签](https://docs.yearn.finance/resources/faq#who-is-on-the-multisig)控制以下内容：


| 权力 | 描述 |
|-------|-------------|
|执行权|执行YFI持有者和yTeams链上决策的权力|
|否决权|该权力允许多签成员否决任何决定，理想情况下不应被行使|
|过渡权力|该临时权力允许多签成员能够在YIP-41的授权下运作，直到一套决策能够权涵盖所有需求事务|


## 未来实现

Yearn正在不断为实现DAO去中心化和生产力的理想平衡铺平道路。当前阶段主要努力通过社交层面实现改变，未来我们将转为通过软件实现，例如：

- 多签共识机制，允许每个yTeam拥有执行权
- 从代理投票转为链上投票
- 将决策权代币化为NFT
- 利用[Coordinape](https://coordinape.com/)完成预算分配和薪劳安排等事项
