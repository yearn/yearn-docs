# Find and create exchanges

## Create factory instance

You will need:

* [Web3.js](https://web3js.readthedocs.io/en/1.0/web3.html) connection
* [Factory ABI](https://raw.githubusercontent.com/Uniswap/contracts-vyper/master/abi/uniswap_factory.json)
* Factory Ethereum address

```javascript
factoryAddress = "0xf5D915570BC477f9B8D6C0E980aA81757A3AaC36"
 
factoryContract = new web3.eth.Contract(factoryABI, factoryAddress)
```

## Using the registry

### Get Exchange Address

There is a separate exchange contract for every ERC20 token. The `getExchange` function is used retrieve the exchange address associated with an ERC20 token.

```javascript
exchangeAddress = factoryContract.methods.getExchange(tokenAddress)
```

If the return value is `0x0000000000000000000000000000000000000000` the token does not yet have an exchange. 

### Get Token Address 

The ERC20 token associated with a Uniswap exchange can be found using the `getToken` function. 

```javascript
tokenAddress = factoryContract.methods.getToken(exchangeAddress)
```

If the return value is `0x0000000000000000000000000000000000000000` the input address is not a Uniswap exchange.





