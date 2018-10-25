# Pool Liquidity

## Formalized Model

Uniswap prices are autonomous and use the Constant Product Market Maker \($$x * y = k$$\). This model was formalized and the smart contract implementation passed a lightweight formal verification.   

* [Formalized Specification](https://github.com/runtimeverification/verified-smart-contracts/blob/uniswap/uniswap/x-y-k.pdf)
* [Lightweight Verification](https://github.com/runtimeverification/verified-smart-contracts/tree/uniswap/uniswap/results) 

## Create Exchange

This `createExchange` function is used to deploy an exchange for an ERC20 token that does not yet have one.

```javascript
factory.methods.createExchange(tokenAddress).send()
```





## Add Liquidity 





## Remove Liquidity 



