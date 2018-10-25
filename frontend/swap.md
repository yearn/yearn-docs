# Swap tokens

## Formalized Model

Uniswap prices are autonomous and use the Constant Product Market Maker \($$x * y = k$$\). This model was formalized and the smart contract implementation passed a lightweight formal verification.  

* [Formalized Model](https://github.com/runtimeverification/verified-smart-contracts/blob/uniswap/uniswap/x-y-k.pdf)
* [Lightweight Verification](https://github.com/runtimeverification/verified-smart-contracts/tree/uniswap/uniswap/results) 

## ETH ⇄ ERC20 Calculations

The only variables needed to price when trading between ETH and ERC20 tokens is:

* ETH reserve on relevant ERC20 exchange
* ERC20 reserve on relevant ERC20
* Amount sold \(exact input\) or amount bought \(exact output\)

### Sell \(exact input\)

```javascript
// Sell ETH for ERC20
inputAmount = userInputEthValue
inputReserve = web3.eth.getBalance(exchangeAddress)
outputReserve = tokenContract.methods.balanceOf(exchangeAddress)

// Sell ERC20 for ETH
inputAmount = userInputTokenValue
inputReserve = tokenContract.methods.balanceOf(exchangeAddress)
outputReserve = web3.eth.getBalance(exchangeAddress)

// Output amount bought 
numerator = inputAmount * outputReserve * 997
denominator = inputReserve * 1000 + inputAmount * 997
outputAmount = numerator / denominator

// Liquidity Provider Fee (built into formula)
fee = inputAmount * 0.003

// Exchange Rate
rate = outputAmount / inputAmount
```

### Buy \(exact output\)

```javascript
// Sell ETH for ERC20
inputAmount = userInputEthValue
inputReserve = web3.eth.getBalance(exchangeAddress)
outputReserve = tokenContract.methods.balanceOf(exchangeAddress)

// Sell ERC20 for ETH
inputAmount = userInputTokenValue
inputReserve = tokenContract.methods.balanceOf(exchangeAddress)
outputReserve = web3.eth.getBalance(exchangeAddress)

// Output amount bought 
numerator = inputAmount * outputReserve * 997
denominator = inputReserve * 1000 + inputAmount * 997
outputAmount = numerator / denominator

// Liquidity Provider Fee (built into formula)
fee = inputAmount * 0.003

// Exchange Rate
rate = outputAmount / inputAmount
```



## ERC20 ⇄ ERC20 Calculations



## Deadlines

Many Uniswap functions include a transaction `deadline` that sets a time after which a transaction can no longer be executed. This limits miners  holding signed transactions for extended durations and executing them based off market movements. It also reduces uncertainty around transactions that take a long time to execute due to issues with gas price. 

Deadlines are calculated by adding the desired amount of time \(in seconds\) to the latest Ethereum block timestamp. 

```javascript
web3.eth.getBlock('latest', (error, block) => {
    deadline = block.timestamp + 300    // TX expires in 300 seconds (5 minutes)  
})
```



## Recipients



## ETH to ERC20

### Parameters



### Trading 



## ERC20 to ETH





## ERC20 to ERC20





## Custom Pools

