# 如何使用Yearn       

多亏了一个名为'Zap'的功能，大家可以用几乎任何代币存入所有的机枪池中。 

这是操作方法: 

首先，使用右上角的按钮**连接你的钱包**。此应用程序支持多种类型的钱包，但大多数人使用[MetaMask](https://metamask.io/)，它可作为Chrome扩展程序，也可通过Apple和Android应用商店免费下载。确保你的钱包已连接到以太坊网络。

<p align="center">
  <img width="1266.75" height="345.75" src="https://i.imgur.com/H0Uc8e8.png">
</p>

## 如果你已经拥有你想要存入的机枪池**所需的代币**： 

- 选择你要存入的机枪池。
- 输入你要存入机枪池的代币数量。如果你要存入的是ETH，请确保你有剩下足够的ETH来支付未来你可能需要进行的交易。

<p align="center">
  <img width="914.26" height="360.75" src="https://i.imgur.com/LGdRAMQ.png">
</p>

- 点击'Approve批准'或'Deposit存款'按钮，这取决于你之前是否已批准。
- 你的钱包会要求你确认交易。这大约需要3分钟，但你可以通过[支付更高的gas费用](https://blog.leverj.io/how-to-set-the-gas-limit-and-gas-price-in-metamask-1b33c38c32fd)来加快速度。如果你的交易卡住，请参阅[本指南](https://metamask.zendesk.com/hc/en-us/articles/360015489251-How-to-Speed-Up-or-Cancel-a-Pending-Transaction)以了解如何加快或取消交易。


<p align="center">
  <img width="258.75" height=" 459.75" src="https://i.imgur.com/BkXBANS.png">
</p>

- 当你的交易成功后，你将在机枪池的界面中看到你的存入余额，该余额应该会出现在机枪池列表的顶部。

<p align="center">
  <img width="928.5" height="93.75" src="https://i.imgur.com/JvNQ3l2.png">
</p>

当你准备退出时：

- 选择你要退出的机枪池
- 输入你要提取的金额，或点击'Max'以提取全部余额

<p align="center">
  <img width="910.5" height="361.5" src="https://i.imgur.com/Y3NsCRb.png">
</p>

- 点击'Withdraw提取'
- 你的钱包会要求你确认交易。有关详细信息，请参阅步骤4
- 交易成功后，代币会再次出现在你的钱包中

## 如果你**没有想要存入的机枪池所需的代币**:

这很常见，因为许多Yearn的机枪池是通过使用[Curve Finance](http://curve.finance/)流动性提供者（LP）代币产生收益的，而这些代币是通过存入Curve池获得的。

例如，如果你宁愿存入crvSTETH机枪池而不是ETH机枪池，并接受Curve池和ETH衍生币（stETH）带来的额外风险以换取更高的收益，但如果你的钱包中只有ETH，则你的ETH需要先转换为crvSTETH代币，然后才能被机枪池接受。 

多亏于Yearn的'zap'功能，这一切都可以在与你的存款相同的交易中完成。以下是使用crvSTETH机枪池作为示例的操作：

**注意**：将代币转移到机枪池中将需要比存入原生代币更多的交易。这意味着当代币被交换或存入池中时，你将支付更多的gas费用，并且可能会因滑点而损失价值。Yearn将滑点限制为1%，如果滑点超过该值，交易将会失败，在这种情况下，你必须自己手动交换或存入代币。有关更多详细信息，请参阅我们的[zap](https://docs.yearn.finance/yearn-finance/yvaults/overview#zap-in-with-any-asset)章节。

- 选择crvSTETH机枪池
- 点击'Approve批准'或'Deposit存款'按钮旁边的下拉框
- 选择你要转换为crvSTETH的代币。它只会显示你钱包中已有的代币

<p align="center">
  <img width="909" height="363" src="https://i.imgur.com/6K1luO7.png">
</p>

- 输入你想要存入的代币数量，然后根据你之前是否已批准该代币，点击'Approve批准'或'Deposit存入'
- 通过你的钱包确认交易。有关更多详细信息，请参阅上一部分中的步骤4
- 当你的交易成功后，你将在机枪池的界面中看到你的存入余额，该余额会出现在机枪池列表的顶部

当你准备退出时：

- 选择crvSTETH机枪池
- 点击'Withdraw提取'按钮旁边的下拉框

<p align="center">
  <img width="915.75" height="600.75" src="https://i.imgur.com/2UyXKN0.png">
</p>

- 选择你希望在提款后收到的资产。你可用的选择是crvSTETH、ETH、BTC、DAI、USDC或USDT
- 输入你要提取的金额，或点击'Max'以提取全部余额
- 如果需要，请确认批准，然后批准提款交易
- 当你的交易成功后，代币会再次出现在你的钱包中

## 可用于追踪资金的工具 

如果你想查看你的资产在机枪池中时你的美元余额如何变化，请将你的钱包连接到[zapper.fi](https://zapper.fi)或类似的投资组合跟踪工具。这也是了解机枪池为你赚取了多少利润最简单的方法。

你的余额不会持续增加。当harvest()函数被调用后，利润将分配到你在机枪池中的份额，该函数调用的發生頻率是不定时的。


追踪你的回报的社区资源：

- [Zapper](https://zapper.fi/)
- [Zerion](https://app.zerion.io/)
- [Yearn机枪池ROI计算器](https://yearn-roi.xyz/#/)
- [yVault ROI](https://yvault-roi.netlify.app/)
- [https://trackavault.com/](https://trackavault.com/)