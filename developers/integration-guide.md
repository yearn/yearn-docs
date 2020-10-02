---
description: In-Progress
---

# Integration Guide

## Contract Registry Comment <a id="Contract-Registery"></a>

Our contract registry is in progress. For now see:

* [https://feel-the-yearn.vercel.app/](https://feel-the-yearn.vercel.app/)
* [https://docs.yearn.finance/faq\#lists-of-smart-contracts](https://docs.yearn.finance/faq#lists-of-smart-contracts)

## .Vault Registry Integration <a id="Vault-Registry-Integration"></a>

* `vault.token()` is the underlying token
* `token.approve(vault, 2**256-1)` to approve a deposit
* `vault.deposit(amount)` to deposit
* `vault.withdraw(amount)` to withdraw
* `vault.getPricePerFullShare()` to get the ratio to underlying token

## Planned Vault Registry Structure

![](https://i.imgur.com/xa0lgtd.jpg)

## .Graph Integrations <a id="Graph-Integrations"></a>

TBD

## API Integrations <a id="API-Integrations"></a>

Interactive API documentation can be found at [https://yearn.tools/](https://yearn.tools/) for querying:

* Vaults data \(such as strategy, token, metadata, ROI/APY\)
* User data \(such as deposits, withdrawals, transfers and earnings\)

### Examples of projects using the API

| Link | Code | By |
| :--- | :--- | :--- |
| [https://yearn.party](https://yearn.party) | [https://github.com/x48-crypto/yearn-party](https://github.com/x48-crypto/yearn-party) | [https://twitter.com/x48114](https://twitter.com/x48114) |

