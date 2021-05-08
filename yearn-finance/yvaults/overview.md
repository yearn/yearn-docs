# Overview

## What are yVaults?

<<<<<<< Updated upstream
[yVaults](https://yearn.finance/vaults) are like savings accounts for your crypto assets. Simp that it then routes it through a strategy which seeks out the highest yield available in DeFi.
=======
[yVaults](https://yearn.finance/vaults) are like savings accounts for your crypto assets. They accept your deposit, then route it through a strategies which seek out the highest yield available in DeFi. 

## yVault Fee Structure

|yVault Version|Withdrawal Fee|Performance Fee|Management Fee|
|--------------|:-----------:|:-------------:|:------------:|
|v1|0.5%|5%|-|
|v2|-|20%|2%|

- Withdrawal Fee: One time fee during withdrawal
- Performance Fee: Percent deducted from income 
- Management Fee: Percent deducted from total balance per year.
>>>>>>> Stashed changes

## V2 yVault Features:

1. **Up to 20 strategies per vault:** This will increase the flexibility to manage capital efficiently during different market scenarios. Each strategy has a capital cap. This is useful to avoid over allocating funds to a strategy which cannot increase APY anymore.
2. **Strategist and Guardian are the new Controllers:** The Controller concept is not available in V2 yVaults and has been replaced by a Guardian and the Strategy creator \(strategist\). These 2 actors oversee strategy performance and are empowered to take action to improve capital management or act on critical situations.
3. **Automated vault housekeeping \(Keep3r network\):** `harvest()` and `earn()` calls are now automated through the Keep3r bots network. These 2 function calls are used to purchase new underlying collateral by selling the farmed tokens while moving the profits back to the vault and later into strategies. The keep3r network takes the heavy lifting of doing these calls and running with the gas costs in exchange for keep3r tokens. This approach unloads humans from these housekeeping tasks.
4. **Bouncers and Guest lists**: Yearn has created an unique development process for new vaults. All vaults are launched as Test Vaults \(tyvToken\) to start with. Test vaults have a cap and therefore their strategies as well. Also, the Bouncer has a guest list of wallets which can interact by depositing and withdrawing funds in the Test Vaults. This approach prevents uninformed users from potentially losing funds in a not production ready product.

<<<<<<< Updated upstream
## V1 Vaults

V1 yVaults have a 0.5% withdrawal fee and a 20% fee on additional yield whenever the `harvest()` function is called, [see the FAQ](https://docs.yearn.finance/faq#what-are-the-fees) for more details. Individual profits are allocated on a pro-rata basis determined by the share each depositor contributes to the pool.

=======
>>>>>>> Stashed changes