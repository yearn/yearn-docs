# Vault Interfaces

## [IStrategy](https://github.com/iearn-finance/yearn-protocol/blob/develop/interfaces/yearn/IStrategy.sol)

### want\(\)

Returns address of the strategy’s unwrapped token.

{% tabs %}
{% tab title="Smart Contract" %}
```javascript
function want() external view returns (address);
```
{% endtab %}
{% endtabs %}

🔓 **Access**: Anyone

| Returns | Description |
| :--- | ---: |
| address | Strategy’s unwrapped token |

### deposit\(\)

Deposits `want` token into another smart contact defined by the strategy itself.

{% tabs %}
{% tab title="Smart Contract" %}
```javascript
function deposit() external;
```
{% endtab %}
{% endtabs %}

🔓 **Access**: Anyone

### withdraw\(address\)

Withdraws strategy's non-core token \(collects dust\).

{% tabs %}
{% tab title="Smart Contract" %}
```javascript
function withdraw(token_addr: address) external;
```
{% endtab %}
{% endtabs %}

🔓 **Access**: Controller only

| Parameter | Type | Description |
| :--- | :--- | ---: |
| token\_addr | address | Token to be drained from Strategy. |

### withdraw\(uint256\)

Partially withdraws user funds from the contract. In case Strategy implements `harvest()` a withdrawal fee might be applied.

{% tabs %}
{% tab title="Smart Contract" %}
```javascript
function withdraw(amount: uint256) external;
```
{% endtab %}
{% endtabs %}

🔓 **Access**: Controller only

| Parameter | Type | Description |
| :--- | :--- | ---: |
| amount | uint256 | Amount to be withdrawn |

### withdrawAll\(\)

Withdraws all user funds, usually when migrating strategies. It uses the withdraw\(\) function and performs a set of cascading/sequential withdraw functions depending on the strategy.

If strategy implements liquidity pools or lending platforms, then withdrawal from these platforms should be performed until the Vault’s unwrapped token is delivered back to the vault.

{% tabs %}
{% tab title="Smart Contract" %}
```javascript
function withdrawAll() external returns (uint256);
```
{% endtab %}
{% endtabs %}

🔓 **Access**: Controller only

| Returns | Description |
| :--- | ---: |
| uint256 | The amount withdrawn |

### skim\(\)

Returns the remaining amount that can be borrowed from the lending platform. Used when the strategy implements a lending platform, such as Aave.

{% tabs %}
{% tab title="Smart Contract" %}
```javascript
function skim() external;
```
{% endtab %}
{% endtabs %}

🔓 **Access**: Anyone

{% hint style="info" %}
skim\(\) is not used by any current strategies.
{% endhint %}

### balanceOf\(\)

Calculates the strategy `want` balance.

{% tabs %}
{% tab title="Smart Contract" %}
```javascript
function balanceOf() external view returns (uint256);
```
{% endtab %}
{% endtabs %}

🔓 **Access**: Anyone

| Returns | Description |
| :--- | ---: |
| uint256 | Strategy `want` balance |

## [IVault](https://github.com/iearn-finance/yearn-protocol/blob/develop/interfaces/yearn/IVault.sol)

### token\(\)

Returns the vault’s unwrapped native token address.

{% tabs %}
{% tab title="Smart Contract" %}
```javascript
function token() external view returns (token_addr: address);
```
{% endtab %}
{% endtabs %}

🔓 **Access**: Anyone

| Returns | Description |
| :--- | ---: |
| address | Vault’s unwrapped native token address |

### underlying\(\)

Returns the native underlying token. In case of aLINK delegated vault the `underlying` returns the address of the LINK token.

{% tabs %}
{% tab title="Smart Contract" %}
```javascript
// This is only implemented in Delegated Vaults.
function underlying() external view returns (token_addr: address);
```
{% endtab %}
{% endtabs %}

🔓 **Access**: Anyone

| Returns | Description |
| :--- | ---: |
| address | Native underlying token address |

### name\(\)

Returns the vault’s wrapped token name, e.g. “yearn Dai Stablecoin".

{% tabs %}
{% tab title="Smart Contract" %}
```javascript
function name() external view returns (string memory);
```
{% endtab %}
{% endtabs %}

🔓 **Access**: Anyone

| Returns | Description |
| :--- | ---: |
| string | Vault’s wrapped token name |

### symbol\(\)

Returns the vault’s wrapped token symbol, e.g. “yDai”

{% tabs %}
{% tab title="Smart Contract" %}
```javascript
function symbol() external view returns (string memory);
```
{% endtab %}
{% endtabs %}

🔓 **Access**: Anyone

| Returns | Description |
| :--- | ---: |
| string | Vault’s wrapped token symbol |

### decimals\(\)

Returns the amount of decimals for this vault’s wrapped token.

{% tabs %}
{% tab title="Smart Contract" %}
```javascript
function decimals() external view returns (uint8);
```
{% endtab %}
{% endtabs %}

🔓 **Access**: Anyone

| Returns | Description |
| :--- | ---: |
| uint8 | Amount of decimals for this vault’s wrapped token |

### controller\(\)

Returns Vault’s controller address.

{% tabs %}
{% tab title="Smart Contract" %}
```javascript
function controller() external view returns (token_addr: address);
```
{% endtab %}
{% endtabs %}

🔓 **Access**: Anyone

| Returns | Description |
| :--- | ---: |
| address | Vault’s controller contract |

### governance\(\)

Returns the address from Vault’s governance, currently multisig address `0xfeb4acf3df3cdea7399794d0869ef76a6efaff52`.

{% tabs %}
{% tab title="Smart Contract" %}
```javascript
function governance() external view returns (address);
```
{% endtab %}
{% endtabs %}

🔓 **Access**: Anyone

| Returns | Description |
| :--- | ---: |
| address | Vault’s governance contract |

### getPricePerFullShare\(\)

Returns price of the Vault’s token denominated to unwrapped token.

The calculation is:

$$
{nativeTokenBalance \over yTokenTotalSupply}
$$

Where "nativeTokenBalance" is the current balance of native token \(DAI, e.g.\) in the Vault, Controller and Strategy contracts. And "yTokenTotalSupply" is the total supply of the Vault's Y Token \(yDAI, e.g.\).

{% tabs %}
{% tab title="Smart Contract" %}
```javascript
function getPricePerFullShare() external view returns (uint256);
```
{% endtab %}
{% endtabs %}

🔓 **Access**: Anyone

| Returns | Description |
| :--- | ---: |
| uint256 | Price of the Vault’s token. |

## [IController](https://github.com/iearn-finance/yearn-protocol/blob/develop/interfaces/yearn/IController.sol)

### withdraw\(address, uint256\)

Calls `strategy.withdraw()` function for the amount defined in `unit256`. `token_addr` is used to identify which strategy you want to withdraw from.

{% tabs %}
{% tab title="Smart Contract" %}
```javascript
function withdraw(token_addr: address, amount: uint256) external;
```
{% endtab %}
{% endtabs %}

🔓 **Access**: Vaults only

| Parameter | Type | Description |
| :--- | :--- | ---: |
| token\_addr | address | Token address that defines current strategy |
| amount | uint256 | Amount to be withdrawn |

### balanceOf\(address\)

Returns the balance of a specific token in the Strategy defined by `token_addr`.

{% tabs %}
{% tab title="Smart Contract" %}
```javascript
function balanceOf(token_addr: address) external view returns (uint256);
```
{% endtab %}
{% endtabs %}

🔓 **Access**: Anyone

| Parameter | Type | Description |
| :--- | :--- | ---: |
| token\_addr | address | Token address that defines current strategy |

| Returns | Description |
| :--- | ---: |
| uint256 | Balance of a specific token in the Strategy. |

### earn\(address, uint256\)

Transfers to the strategy the yield generated from `harvest()` function \(when available\) or from the yield generating underlying platform \(lending or LP\).

{% tabs %}
{% tab title="Smart Contract" %}
```javascript
function earn(token_addr: address, amount: uint256) external;
```
{% endtab %}
{% endtabs %}

🔓 **Access**: Anyone

| Parameter | Type | Description |
| :--- | :--- | ---: |
| token\_addr | address | Token to be withdrawn |
| amount | uint256 | Amount to be withdrawn |

### want\(address\)

{% tabs %}
{% tab title="Smart Contract" %}
```javascript
function want(token_addr: address) external view returns (address);
```
{% endtab %}
{% endtabs %}

🔓 **Access**: Anyone

| Returns | Description |
| :--- | ---: |
| address | Strategy's or vault's unwrapped token. |

{% hint style="info" %}
The current deployed controller doesn't use this anymore. You need to load the strategy, then call `strategy.want()`
{% endhint %}

### rewards\(\)

Returns the address of the TreasuryVault which is where the reward tokens go.

{% tabs %}
{% tab title="Smart Contract" %}
```javascript
function rewards() external view returns (treasury_addr: address);
```
{% endtab %}
{% endtabs %}

🔓 **Access**: Anyone

| Returns | Description |
| :--- | ---: |
| address | TreasuryVault contract |

### vaults\(address\)

Returns the corresponding Vault address for specific token.

{% tabs %}
{% tab title="Smart Contract" %}
```javascript
function vaults(token_addr: address) external view returns (vault_addr: address);
```
{% endtab %}
{% endtabs %}

🔓 **Access**: Anyone

| Returns | Description |
| :--- | ---: |
| address | Corresponding Vault address |

### strategies\(address\)

Returns the corresponding Strategy address for specific Token.

{% tabs %}
{% tab title="Smart Contract" %}
```javascript
function strategies(token_addr: address) external view
returns (strategy_addr: address);
```
{% endtab %}
{% endtabs %}

🔓 **Access**: Anyone

| Returns | Description |
| :--- | ---: |
| address | Corresponding Strategy address |

