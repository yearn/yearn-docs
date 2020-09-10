# yVaults

The goal of the Vaults program is to empower the community to quickly and safely create and utilize the most effective yield farming robots created by the industry's best strategists.

yVaults have a 0.5% withdrawal fee and a 5% fee on additional yield whenever the `harvest()` function is called, [see the FAQ](https://docs.yearn.finance/faq#what-are-the-fees) for more details. Individual profits are allocated on a pro-rata basis determined by the share each depositor contributes to the pool.

### Available yVaults

There are currently nine yVaults. You can access them here: [https://yearn.finance/vaults](https://yearn.finance/vaults) 1. ETH/WETH 2. YFI 3. yDAI+yUSDC+yUSDT+yTUSD \(yCRV\) 4. crvBUSD 5. crvBTC 6. DAI 7. TUSD 8. USDC 9. USDT

The tokens identified above are deposited into their respective yVaults and used to yield farm using current opportunities in the market.

The vaults are created and maintained by a Controller, who oversees the strategy execution. Profits generated from each respective vault are used to purchase more of the underlying asset in each vault \(e.g., the YFI vault's profits are used to purchase additional YFI\); therefore, _the vaults represent a a continuous buy-and-hold strategy._

### yETH Vault Mechanics

The Controller opens a colleratlized debt position \(CDP\) at MakerDAO using ETH as collateral and mints DAI. The DAI is deposited into the yDAI vault. The collateralization ratio—a metric of financial leverage—is targeted to always be at least 200%. Automated bots periodically pay down the DAI debt if the ratio falls below 200%. The DAI is redeemed from [Curve](http://curve.fi/) and is not purchased from the open market \(i.e., yDAI is burned and redeemed for DAI\). Excess DAI earned from yield farimging are used to purchase additional ETH, which is deposited into the yETH vault.

![](https://i.imgur.com/ZASptpX.png)

### Delegated yVaults

Volatile assets can also particpate in yield farming strategies as part of the deleagted yVault product. Currently, there is only one delegated yVaults: aLINK.

Profits generated from the delegated yVault are used to purchase more of the underlying asset. Once again representing _a continuous buy-and-hold strategy_. Depositors can withdraw their initial deposits and accrued profits, if any, at any time after a 0.5% withdrawal fee.

#### Mechanics

The Controller deposits LINK into AAVE and borrows stablecoins. The initial health factor of these loans is always above 4, and if the health factor drops below 4 at any time the Controller repays a portion of the debt in order to maintain a health factor above 4.

The stablecoins borrowed \(e.g., USDC, DAI, USDT, etc.\) depend on the strategy selected by the Controller. After obtaining stablecoins the Controller will deposit them into one of the yVaults identified above.

![](https://i.imgur.com/8AVJU0d.png)

## Resources

* [Vaults Homepage](https://yearn.finance/vaults)
* Medium Article: [yETH vault explained](https://medium.com/iearn/yeth-vault-explained-c29d6b93a371)

