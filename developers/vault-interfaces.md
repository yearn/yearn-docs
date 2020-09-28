# Vault Interfaces

## [IStrategy](https://github.com/iearn-finance/yearn-protocol/blob/develop/interfaces/yearn/IStrategy.sol)
### want()
```
function want() external view returns (address);
```
Returns address of the strategy’s unwrapped token. In case of StrategyDAICurve it will return the DAI address.

### deposit()
```
function deposit() external;
```

Deposits it's own "want" tokens into the pool defined by the strategy itself. For StrategyDAICurve, deposits DAI into Curve's Y Pool (minting yCRV) and then deposits yCRV into Yearn's Y Vault (minting yUSD).

This method is public and can be called by anyone. It's called by Controller on earn() method.

### withdraw(address)
```
function withdraw(address) external;
```
Controller only. Used to drain the strategy for a defined non-core token passed to the function.

### withdraw(uint256)
```
function withdraw(uint256) external;
```
Controller only. Used to partially withdraw funds from the contract. If not enough, funds are withdrawn from the strategy they are invested in.

In case Strategy implements harvest() a withdrawal fee might be applied.

### withdrawAll()
```
function withdrawAll() external returns (uint256);
```
Controller only. Used to withdraw all strategy funds, usually when migrating strategies. 

It uses the withdraw() function and performs a set of cascading/sequential withdraw functions depending on the strategy. 

If strategy implements liquidity pools or lending platforms, then withdrawal from these platforms should be performed until the Vault’s unwrapped token is delivered back to the vault.


### skim()
```
function skim() external;
```
Used when the strategy implements a lending platform, such as Aave. This function returns the remaining amount that can be borrowed from the lending platform.

{% hint style="info" %} skim() is not used by any current strategies. {% endhint %}

### balanceOf()

```
function balanceOf() external view returns (uint256);
```
Calculates the strategy balance (contract balance + invested balance).


## [IVault](https://github.com/iearn-finance/yearn-protocol/blob/develop/interfaces/yearn/IVault.sol)

### token()
```
function token() external view returns (address);

```

Returns the vault’s unwrapped native token address. In case of DAI Vault, it will return DAI, in case of curve.fi/y LP Vault it will return yUSD (yDAI/yUSDC/yUSDT/yTUSD).

### underlying()
```
function underlying() external view returns (address);

```

This is only implemented in Delegated Vaults. It returns the native underlying token. In the case of aLINK delegated vault the underlying returns the address of the LINK token.

### name()
```
function name() external view returns (string memory);

```
Returns the vault’s wrapped token name. In case of DAI Vault, it will return “yearn Dai Stablecoin".

### symbol()
```
function symbol() external view returns (string memory);

```

Returns the vault’s wrapped token symbol. In case of DAI Vault, it will returns a string “yDai”.

### decimals()
```
function decimals() external view returns (uint8);

```

Returns the amount of decimals for this vault’s wrapped token. In case of DAI Vault, it will return 18.

### controller()
```
function controller() external view returns (address);

```
Returns the address from Vault’s controller. In case of DAI Vault, it will return 0x9e65ad11b299ca0abefc2799ddb6314ef2d91080.

### governance()
```
function governance() external view returns (address);

```

Returns the address from Vault’s governance. In case of DAI Vault, it will return 0xfeb4acf3df3cdea7399794d0869ef76a6efaff52.

### getPricePerFullShare()
```
function getPricePerFullShare() external view returns (uint256);
```
Returns the price of the Vault’s token. In case of DAI Vault, it will return the price of 1 yDAI. The calculation is:

$$
{nativeTokenBalance \over yTokenTotalSupply}
$$

Where "nativeTokenBalance" is the current balance of native token (DAI, e.g.) in the Vault, Controller and Strategy contracts. And "yTokenTotalSupply" is the total supply of the Vault's Y Token (yDAI, e.g.).

## [IController](https://github.com/iearn-finance/yearn-protocol/blob/develop/interfaces/yearn/IController.sol)

### withdraw(address, uint256)
```
function withdraw(address, uint256) external;

```

Vaults only. Calls strategies withdraw() function for the amount defined in unit256.

### balanceOf(address)
```
function balanceOf(address) external view returns (uint256);
```

Returns the balance of a specific token in the Strategy.

### earn(address, uint256)
```
function earn(address, uint256) external;
```

Transfers to the strategy the yield generated from harvest() function (when available) or from the yield generating underlying platform (lending or LP).

### want(address)
```
function want(address) external view returns (address);
```

Returns the strategies or vaults unwrapped token.

{% hint style="info" %} The current deployed controller doesn't use this anymore. You need to load the strategy, then call strategy.want(). {% endhint %}

### rewards()
```
function rewards() external view returns (address);

```
Returns the address of the TreasuryVault which is where the reward tokens go.

### vaults(address)

```
function vaults(address) external view returns (address);

```
Returns the corresponding Vault address for a specific Token.

### strategies(address)
```
function strategies(address) external view returns (address);

```
Returns the corresponding Strategy address for a specific Token.