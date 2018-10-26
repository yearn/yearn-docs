# Trade tokens

In Uniswap, there is a separate exchange contract for each ERC20. Each exchange holds a reserve of both ETH and its associated ERC20 token. Users can trade between the two in either direction. This is done by adding to the reserve of one and withdrawing from the reserve of the other. Pricing is automatic, and based on the $$x * y = k$$ market maker equation. This model prices assets based off the relative sizes of the two reserves and the size of the incoming trade. 

## ETH ⇄ ERC20 Calculations

The only variables needed to determine price when trading between ETH and ERC20 tokens is:

* ETH reserve size in exchange contract
* ERC20 reserve size in exchange contract
* Amount sold \(exact input\) or amount bought \(exact output\)

### Amount Bought \(sell order\)

Given an exact input amount \(sell order\), the amount bought is calculated:

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
```

### Amount Sold \(buy order\)

Given an exact output amount \(buy order\), the amount that must be sold is calculated:

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

### Liquidity Provider Fee

There is a 0.3% liquidity provider fee built into the price formula. This can be calculated:   

```javascript
fee = inputAmount * 0.003
```

### Exchange Rate

The exchange rate is simply the output amount divided by the input amount.

```javascript
rate = outputAmount / inputAmount
```

## ERC20 ⇄ ERC20 Calculations



The only variables needed to determine price when trading between ETH and ERC20 tokens is:

* ETH reserve on input ERC20 exchange
* ERC20 reserve on input ERC20 exchange
* ETH reserve on output ERC20 exchange
* ERC20 reserve on relevant ERC20
* Amount sold \(exact input\) or amount bought \(exact output\)

### Amount Bought \(sell order\)

Given an exact input amount \(sell order\), the amount bought is calculated:

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
```

### Amount Sold \(buy order\)

Given an exact output amount \(buy order\), the amount that must be sold is calculated:

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

### Liquidity Provider Fee

There is a 0.3% liquidity provider fee built into the price formula. This can be calculated:   

```javascript
fee = inputAmount * 0.003
```

### Exchange Rate

The exchange rate is simply the output amount divided by the input amount.

```javascript
rate = outputAmount / inputAmount
```

## Deadlines

Many Uniswap functions include a transaction `deadline` that sets a time after which a transaction can no longer be executed. This limits miners  holding signed transactions for extended durations and executing them based off market movements. It also reduces uncertainty around transactions that take a long time to execute due to issues with gas price. 

Deadlines are calculated by adding the desired amount of time \(in seconds\) to the latest Ethereum block timestamp. 

```javascript
web3.eth.getBlock('latest', (error, block) => {
    deadline = block.timestamp + 300    // TX expires in 300 seconds (5 minutes)  
})
```



## Recipients



## ETH ⇄ ERC20 Trades

### Parameters



### Trading 



## ERC20 to ERC20





## Custom Pools

