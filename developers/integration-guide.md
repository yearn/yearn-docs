---
description: In-Progress
---

# Integration Guide

### Contract Registry Comment <a id="Contract-Registery"></a>

Our contract registry is in progress. For now see:

* [https://feel-the-yearn.vercel.app/](https://feel-the-yearn.vercel.app/)
* [https://docs.yearn.finance/faq\#lists-of-smart-contracts](https://docs.yearn.finance/faq#lists-of-smart-contracts)

### .Vault Registry Integration <a id="Vault-Registry-Integration"></a>

* `vault.token()` is the underlying token
* `token.approve(vault, 2**256-1)` to approve a deposit
* `vault.deposit(amount)` to deposit
* `vault.withdraw(amount)` to withdraw
* `vault.getPricePerFullShare()` to get the ratio to underlying token

### Planned Vault Registry Structure

![](https://i.imgur.com/xa0lgtd.jpg)

### .Graph Integrations <a id="Graph-Integrations"></a>

TBD

### .API Integrations <a id="API-Integrations"></a>

TBD

