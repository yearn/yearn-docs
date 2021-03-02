# Vault Interfaces

## IStrategy

Source code: [yearn-protocol/develop/interfaces/yearn/IStrategy.sol](https://github.com/iearn-finance/yearn-protocol/blob/develop/interfaces/yearn/IStrategy.sol)

### function `want()`

Returns the address of the unwrapped token that the Strategy takes as deposit.

{% tabs %}
{% tab title="Solidity" %}

```javascript
function want() external view returns (address);
```

{% endtab %}
{% endtabs %}

|        |     | type    | desc                                               |
| ------ | --- | ------- | -------------------------------------------------- |
| Output | 0   | address | Address of the token the Strategy takes as deposit |

### function `deposit()`

Deposits token (same as `want()` returns) into a smart contact specified by the Strategy.

{% tabs %}
{% tab title="Solidity" %}

```javascript
function deposit() external;
```

{% endtab %}
{% endtabs %}

### func `withdraw(address)`

Dust collecting function to create additional rewards out of tokens that were incorrectly sent to the Strategy.

Takes an ERC20 token address and should send the full amount of any such tokens in the Strategy to the Controller.

This function should have access control enforcing the Controller only to be its allowed caller, and checks in place to ensure that the token types to withdraw are not those used by the Strategy.

{% tabs %}
{% tab title="Solidity" %}

```javascript
function withdraw(address) external;
```

{% endtab %}
{% endtabs %}

|       |     | type    | desc                       |
| ----- | --- | ------- | -------------------------- |
| Input | 0   | address | ERC-20 token to be drained |

### function `withdraw(uint256)`

Partially withdraws funds (denominated in `want()` token) from the Strategy, and should always only be sending these to the Vault. In case the Strategy implements `harvest()`, a withdrawal fee may be applied. This function should have access control enforcing the Controller only to be its allowed caller.

{% tabs %}
{% tab title="Solidity" %}

```javascript
function withdraw(uint256) external;
```

{% endtab %}
{% endtabs %}

|       |     | type | desc                   |
| ----- | --- | ---- | ---------------------- |
| Input | 0   | uint | Amount to be withdrawn |

### function `skim()`

Used to obtain the remaining amount that can be borrowed from the lending platform. Relevant when the Strategy implements a lending platform, such as Aave.

{% tabs %}
{% tab title="Solidity" %}

```javascript
function skim() external;
```

{% endtab %}
{% endtabs %}

### function `withdrawAll()`

Withdraws the entire amount of `want()` tokens available, and should always only be sending these to the Vault. This function should have access control enforcing the Controller only to be its allowed caller. Typically used when migrating strategies.

The function typically uses `withdraw()` and performs a set of sequential function calls depending on the Strategy.

If the Strategy implements liquidity pools or lending platforms, then withdrawal from these platforms should be performed until the Vault’s unwrapped token is delivered back to the vault.

Returns a `uint256` of the total amount withdrawn.

{% tabs %}
{% tab title="Solidity" %}

```javascript
function withdrawAll() external returns (uint256);
```

{% endtab %}
{% endtabs %}

|        |     | type    | desc                 |
| ------ | --- | ------- | -------------------- |
| Output | 0   | uint256 | The amount withdrawn |

### function `balanceOf()`

Returns the Strategy's current `want()` token balance.

{% tabs %}
{% tab title="Solidity" %}

```javascript
function balanceOf() external view returns (uint256);
```

{% endtab %}
{% endtabs %}

|        |     | type    | desc                              |
| ------ | --- | ------- | --------------------------------- |
| Output | 0   | uint256 | Strategy's `want()` token balance |

## IVault

Source code: [yearn-protocol/develop/interfaces/yearn/IVault.sol](https://github.com/iearn-finance/yearn-protocol/blob/develop/interfaces/yearn/IVault.sol)

### function `token()`

Returns the unwrapped native token address that the Vault takes as deposit.

{% tabs %}
{% tab title="Solidity" %}

```javascript
function token() external view returns (address);
```

{% endtab %}
{% endtabs %}

|        |     | type    | desc                                   |
| ------ | --- | ------- | -------------------------------------- |
| Output | 0   | address | Vault’s unwrapped native token address |

### function `underlying()`

Returns the native underlying token address in Delegated Vaults. For example, in case of aLINK delegated vault, `underlying()` returns the address of the LINK token.

{% tabs %}
{% tab title="Solidity" %}

```javascript
// This is only implemented in Delegated Vaults.
function underlying() external view returns (address);
```

{% endtab %}
{% endtabs %}

|        |     | type    | desc                                              |
| ------ | --- | ------- | ------------------------------------------------- |
| Output | 0   | address | Delegated Vault’s underlying native token address |

### function `name()`

Returns the vault’s wrapped token name as a string, e.g. “yearn Dai Stablecoin".

{% tabs %}
{% tab title="Solidity" %}

```javascript
function name() external view returns (string memory);
```

{% endtab %}
{% endtabs %}

|        |     | type   | desc                       |
| ------ | --- | ------ | -------------------------- |
| Output | 0   | string | Vault’s wrapped token name |

### function `symbol()`

Returns the vault’s wrapped token symbol as a string, e.g. “yDai”.

{% tabs %}
{% tab title="Solidity" %}

```javascript
function symbol() external view returns (string memory);
```

{% endtab %}
{% endtabs %}

|        |     | type   | desc                         |
| ------ | --- | ------ | ---------------------------- |
| Output | 0   | string | Vault’s wrapped token symbol |

### function `decimals()`

Returns the amount of decimals for this vault’s wrapped token as a `uint8`.

{% tabs %}
{% tab title="Solidity" %}

```javascript
function decimals() external view returns (uint8);
```

{% endtab %}
{% endtabs %}

|        |     | type  | desc                                         |
| ------ | --- | ----- | -------------------------------------------- |
| Output | 0   | uint8 | No of decimals of the vault's wrapped token. |

### func `controller()`

Returns the address of the Vault's Controller.

{% tabs %}
{% tab title="Solidity" %}

```javascript
function controller() external view returns (address);
```

{% endtab %}
{% endtabs %}

|        |     | type    | desc                        |
| ------ | --- | ------- | --------------------------- |
| Output | 0   | address | Vault’s Controller contract |

### function `governance()`

Returns the address of the Vault’s governance contract.

{% tabs %}
{% tab title="Solidity" %}

```javascript
function governance() external view returns (address);
```

{% endtab %}
{% endtabs %}

|        |     | type    | desc                        |
| ------ | --- | ------- | --------------------------- |
| Output | 0   | address | Vault’s Governance contract |

### function `getPricePerFullShare()`

Returns the price of the Vault’s wrapped token, denominated in the unwrapped native token.

The calculation is:

$$
{nativeTokenBalance \over yTokenTotalSupply}
$$

Where `nativeTokenBalance` is the current balance of native token \(e.g. DAI\) in the Vault, Controller and Strategy contracts. And `yTokenTotalSupply` is the total supply of the Vault's wrapped Token \(e.g. yDAI\).

{% tabs %}
{% tab title="Solidity" %}

```javascript
function getPricePerFullShare() external view returns (uint256);
```

{% endtab %}
{% endtabs %}

|        |     | type    | desc                                                                         |
| ------ | --- | ------- | ---------------------------------------------------------------------------- |
| Output | 0   | uint256 | Price of the Vault’s wrapped token denominated in the unwrapped native token |

### function `deposit()`

Deposits the specified amount of the native unwrapped token (same as `token()` returns) into the Vault.

{% tabs %}
{% tab title="Solidity" %}

```javascript
function deposit(uint256) external;
```

{% endtab %}
{% endtabs %}

|       |     | type    | desc                              |
| ----- | --- | ------- | --------------------------------- |
| Input | 0   | uint256 | Amount to deposit into the Vault. |

### function `depositAll()`

Deposits the maximum available amount of the native unwrapped token (same as `token()` returns) into the Vault.

{% tabs %}
{% tab title="Solidity" %}

```javascript
function depositAll() external;
```

{% endtab %}
{% endtabs %}

### function `withdraw()`

Withdraws the specified amount of the native unwrapped token (same as `token()` returns) from the Vault.

{% tabs %}
{% tab title="Solidity" %}

```javascript
function withdraw(uint256) external;
```

{% endtab %}
{% endtabs %}

|       |     | type    | desc                               |
| ----- | --- | ------- | ---------------------------------- |
| Input | 0   | uint256 | Amount to withdraw from the Vault. |

### function `withdrawAll()`

Withdraws the maximum available amount of the native unwrapped token (same as `token()` returns) from the Vault.

{% tabs %}
{% tab title="Solidity" %}

```javascript
function withdrawAll() external;
```

{% endtab %}
{% endtabs %}

## IController

Source code: [yearn-protocol/develop/interfaces/yearn/IController.sol](https://github.com/iearn-finance/yearn-protocol/blob/develop/interfaces/yearn/IController.sol)

### function `withdraw()`

Calls `Strategy.withdraw()` function for the amount defined in `unit256` in the Strategy of the specified address. This function should have access control enforcing the Vault to be its only allowed caller.

{% tabs %}
{% tab title="Solidity" %}

```javascript
function withdraw(address, uint256) external;
```

{% endtab %}
{% endtabs %}

|       |     | type    | desc                                     |
| ----- | --- | ------- | ---------------------------------------- |
| Input | 0   | address | Address of the Strategy to withdraw from |
| Input | 1   | uint256 | Amount to withdraw                       |

### function `balanceOf()`

Returns the Strategy's balance of the specified token.

{% tabs %}
{% tab title="Solidity" %}

```javascript
function balanceOf(address) external view returns (uint256);
```

{% endtab %}
{% endtabs %}

|        |     | type    | desc                               |
| ------ | --- | ------- | ---------------------------------- |
| Input  | 0   | address | Token that is used in the Strategy |
| Output | 0   | uint256 | Balance of the specified token     |

### function `earn()`

Transfers the profits earned from the yield generating activities of the Strategy to the Vault. Takes an address of a token to withdraw and an amount.

{% tabs %}
{% tab title="Solidity" %}

```javascript
function earn(address, uint256) external;
```

{% endtab %}
{% endtabs %}

|       |     | type    | desc                                                 |
| ----- | --- | ------- | ---------------------------------------------------- |
| Input | 0   | address | Token to be withdrawn to the Vault from the Strategy |
| Input | 1   | uint256 | Amount to be withdrawn                               |

### function `want()`

{% hint style="info" %}
Not used by the currently deployed controller. Please refer to [`Strategy.want()`](#function-want) instead.
{% endhint %}

{% tabs %}
{% tab title="Solidity" %}

```javascript
function want(address) external view returns (address);
```

{% endtab %}
{% endtabs %}

### function `rewards()`

Returns the address of the Treasury which is where the system reward fees go.

{% tabs %}
{% tab title="Solidity" %}

```javascript
function rewards() external view returns (address);
```

{% endtab %}
{% endtabs %}

|        |     | type    | desc              |
| ------ | --- | ------- | ----------------- |
| Output | 0   | address | Treasury contract |

### function `vaults()`

Takes a token address and returns the corresponding Vault address.

{% tabs %}
{% tab title="Solidity" %}

```javascript
function vaults(address) external view returns (address);
```

{% endtab %}
{% endtabs %}

|        |     | type    | desc                                                      |
| ------ | --- | ------- | --------------------------------------------------------- |
| Input  | 0   | address | Token to find a Vault address for                         |
| Output | 0   | address | Vault address that is associated with the specified token |

### function `strategies()`

Takes a token address and returns the corresponding Strategy address.

{% tabs %}
{% tab title="Solidity" %}

```javascript
function strategies(address) external view returns (address);
```

{% endtab %}
{% endtabs %}

|        |     | type    | desc                                                         |
| ------ | --- | ------- | ------------------------------------------------------------ |
| Input  | 0   | address | Token to find a Strategy address for                         |
| Output | 0   | address | Strategy address that is associated with the specified token |
