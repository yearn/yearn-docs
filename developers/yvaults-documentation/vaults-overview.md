# Vaults Overview

This document gives a _generalized and high level overview_ of how the protocol and its actors, smart contracts, and other services interact with each other. The aim is to build intuition about how Yearn products work.

{% hint style="info" %}
All vaults are different. This is not a formal specification. Contracts and components are subject to change without notice.
{% endhint %}

![yearn-protocol](https://raw.githubusercontent.com/lehnberg/yearn-diagrams/master/yearn-protocol/yearn-protocol-v0.06.svg)

All contracts are open source and available from the [/yearn-protocol](https://github.com/iearn-finance/yearn-protocol) GitHub repo.

## Protocol Contracts

### Vaults

Example: [yWETH.sol](https://github.com/iearn-finance/yearn-protocol/blob/develop/contracts/vaults/yWETH.sol)

Vaults act as the representation of the user in the system, and is the internal customer for investments. There is one vault per deposit token, and they are agnostic to the strategies they interact with.

Their primary tasks are to:

- **process user deposits and withdrawals**, minting or burning LP tokens as receipts for these;
- **manage disposable funds**, ensuring there is enough to satisfy the minimum amount available to handle withdrawals, and issuing withdrawal requests from strategies when more funds need to be added; and
- **deposit funds into strategies**, when there is a surplus of funds in the vault above what's required to be kept at disposal.

### Controller

[Controller.sol](https://github.com/iearn-finance/yearn-protocol/blob/develop/contracts/controllers/Controller.sol)

The Controller act as the gatekeeping interface between vaults and strategies and oversees communication and fund flows. Deposits and withdrawals in and out of strategies flow through the `Controller`. It keeps track of the addresses for the active vaults, strategies, tokens, and strategy rewards destination, acting as a pseudo-registry that verifies the origin and destination of a transaction. The `Controller` also handles strategy migration, moving funds from an old strategy to a new one.

### Registry

[YRegistry.sol](https://github.com/iearn-finance/yearn-protocol/blob/develop/contracts/registries/YRegistry.sol)

The registry is a wrapper of the controller that contains additional meta-data about active addresses. Its functionality is currently being expanded.

### Strategies

Example: [CurveYCRVVoter.sol](https://github.com/iearn-finance/yearn-protocol/blob/develop/contracts/strategies/CurveYCRVVoter.sol)

Strategies are investment instruction sets, written by a `Strategist`. They are agnostic to the vaults that use them.

Strategies execute step-by-step functions with the objective to generate yield. They do so by interacting with:

- **other Yearn services**, such as vaults, lending, and insurance; and
- **external 3rd party services**, such as Aave, Curve, Chainlink and Maker.

Rewards are claimed and re-invested into the strategies, with deductions for Management fees and for compensating the `Strategist`.

### Treasury

The `Treasury` contract accumulates all the Management fees sent from the strategies. It's an intermediate contract that can convert between different tokens, currently normalizing all rewards into yCRV. It calls two functions:

- `toVoters()`, sending part of the fees to the governance voters, as a reward for their participation; and
- `toGovernance()`, sending part of the fees to the multi-sig to cover gas costs and other expenses.

### Governance

[StrategyYFIGovernance.sol](https://github.com/iearn-finance/yearn-protocol/blob/develop/contracts/strategies/StrategyYFIGovernance.sol)

Yearn Governance is a combination of the YFI staking contract to participate in Governance voting, and the 6-of-9 multi-sig that executes the decisions by the YFI holders.

Governance manages the `Vaults`, `Controller`, and `Strategies` by calling functions on these contracts.

#### Vault management

- **Set governing address**, through `setGovernance()`, in order to upgrade governance contracts.
- **Set controller for the vault**, through `setController()`, in order to upgrade controllers.
- **Set amount of disposable funds at hand in vault**, through `setMin()`, in order to manage how large withdrawal amounts require a Vault to issue a withdrawal request to a Strategy, via the Controller.

#### Controller management

- **Set governing address**, through `setGovernance()`, in order to upgrade governance contracts.
- **Add vaults** for the Controller to manage, through `setVault()`, in order to introduce new vaults.
- **Set address to receive management fees**, through `setRewards()` in order to upgrade the Treasury.

#### Strategy management

- **Set Strategist address**, through `setStrategist()`, in order for Strategists to receive their rewards and to interact with the system.
- **Add an approved Strategy**, through `approveStrategy()` on the Controller, in order for Strategists to be able to activate the Strategy in question.
- **Remove an approved Strategy**, through `revokeStrategy()` on the Controller, in order to prevent Strategists from being able to activate the Strategy in question.

## Protocol Actors

### User

A Yearn end-user.

- Deposits funds into vaults, to receive LP tokens, through calling `deposit()`;
- Withdraws funds from vaults, by depositing (effectively burning) LP tokens into vaults and receiving the corresponding deposit token amount back in return, through calling `withdraw()`. If the vault does not have enough funds to handle the withdrawal, this triggers a cascading `withdraw()` call via the `Controller` to the Strategy to liquidate enough funds to process the withdrawal.

### Keeper

Automated bot that calls contract functions. It queries the Registry to get the appropriate Vault and Strategy addresses and then calls:

- `earn()` on the Vault, which checks for funds available to be deposited into a Strategy and then deposits those.
- `harvest()` on the Strategy, which triggers the Strategy claim any rewards, pay management and Strategist fees, and re-invest the remainder into itself again.

### Strategist

Creates and manages Strategies.

- Interacts with the Controller to set the active strategy, through `setStrategy()`. **Only Strategies approved by Governance can be set.**
- Is paid the Strategist management fee directly from the Strategy.
