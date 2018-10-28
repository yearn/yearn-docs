# Pool Liquidity

## Formalized Model

Uniswap liquidity pools are autonomous and use the Constant Product Market Maker \($$x * y = k$$\). This model was formalized and the smart contract implementation passed a lightweight formal verification. yo  

* [Formalized Specification](https://github.com/runtimeverification/verified-smart-contracts/blob/uniswap/uniswap/x-y-k.pdf)
* [Lightweight Verification](https://github.com/runtimeverification/verified-smart-contracts/tree/uniswap/uniswap/results) 

## Create Exchange

The `createExchange` function is used to deploy exchange contracts for ERC20 tokens that do not yet have one.

```javascript
factory.methods.createExchange(tokenAddress).send()
```

Once an exchange is created the address can be retrieved with [getExchange](https://docs.uniswap.io/~/edit/drafts/-LPtLEzWewVX9LxoQwHY/frontend/connect-to-uniswap#get-exchange-address). 

## Exchange Reserves

Each exchange contract holds a liquidity reserve of ETH and its associated ERC20 token.  

### ETH Reserve

The ETH reserve associated with an ERC20 token exchange is the ETH balance of the exchange smart contract. 

```javascript
ethReserve = web3.eth.getBalance(exchangeAddress)
```

### ERC20 Reserve

The ERC20 reserve associated with an ERC20 token exchange is the ERC20 balance of the exchange smart contract. 

```javascript
tokenReserve = tokenContract.methods.balanceOf(exchangeAddress)
```

## Add Liquidity 

Anyone who wants can join a Uniswap liquidity pool by calling the `addLiquidity` function.

```javascript
exchange.methods.addLiquidity(
    min_liquidity, 
    max_tokens, 
    deadline 
).send({value: ethAmount})
```

Adding liquidity requires depositing and equivalent **value** of ETH and ERC20 tokens into the ERC20 token's associated exchange contract. 

## Remove Liquidity 



