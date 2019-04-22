# Trade tokens

In Uniswap, there is a separate exchange contract for each ERC20 token. These exchanges hold reserves of both ETH and their associated ERC20. Instead of waiting to be matched in an order-book, users can make trades against the reserves at any time. Reserves are pooled between a decentralized network of liquidity providers who collect fees on every trade. 

Pricing is automatic, based on the $$x * y = k$$ market making formula which automatically adjusts prices based off the relative sizes of the two reserves and the size of the incoming trade. Since all tokens share ETH as a common pair, it is used as an intermediary asset for direct trading between any ERC20 ⇄ ERC20 pair. 

## ETH ⇄ ERC20 Calculations

The variables needed to determine price when trading between ETH and ERC20 tokens is:

* ETH reserve size of the ERC20 exchange
* ERC20 reserve size of the ERC20 exchange
* Amount sold \(input\) or amount bought \(output\)

### Amount Bought \(sell order\)

For sell orders \(exact input\), the amount bought \(output\) is calculated:

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

For buy orders \(exact output\), the cost \(input\) is calculated:

```javascript
// Buy ERC20 with ETH
outputAmount = userInputTokenValue
inputReserve = web3.eth.getBalance(exchangeAddress)
outputReserve = tokenContract.methods.balanceOf(exchangeAddress)

// Buy ETH with ERC20 
outputAmount = userInputEthValue
inputReserve = tokenContract.methods.balanceOf(exchangeAddress)
outputReserve = web3.eth.getBalance(exchangeAddress)

// Cost
numerator = outputAmount * inputReserve * 1000
denominator = (outputReserve - outputAmount) * 997
inputAmount = numerator / denominator + 1
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

The variables needed to determine price when trading between two ERC20 tokens is:

* ETH reserve size of the input ERC20 exchange 
* ERC20 reserve size of the input ERC20 exchange 
* ETH reserve size of the output ERC20 exchange 
* ERC20 reserve size of the output ERC20 exchange
* Amount sold \(input\) or amount bought \(output\)

### Amount Bought \(sell order\)

For sell orders \(exact input\), the amount bought \(output\) is calculated:

```javascript
// TokenA (ERC20) to ETH conversion
inputAmountA = userInputTokenAValue
inputReserveA = tokenContractA.methods.balanceOf(exchangeAddressA)
outputReserveA = web3.eth.getBalance(exchangeAddressA)

numeratorA = inputAmountA * outputReserveA * 997
denominatorA = inputReserveA * 1000 + inputAmountA * 997
outputAmountA = numeratorA / denominatorA

// ETH to TokenB conversion 
inputAmountB = outputAmountA    
inputReserveB = web3.eth.getBalance(exchangeAddressB)
outputReserveB = tokenContract.methods.balanceOf(exchangeAddressB)

numeratorB = inputAmountB * outputReserveB * 997
denominatorB = inputReserveB * 1000 + inputAmountB * 997
outputAmountB = numeratorB / denominatorB    
```

### Amount Sold \(buy order\)

For buy orders \(exact output\), the cost \(input\) is calculated:

```javascript
// Buy TokenB with ETH
outputAmountB = userInputEthValue
inputReserveB = web3.eth.getBalance(exchangeAddressB)
outputReserveB = tokenContractB.methods.balanceOf(exchangeAddressB)

// Cost
numeratorB = outputAmountB * inputReserveB * 1000
denominatorB = (outputReserveB - outputAmountB) * 997
inputAmountB = numeratorB / denominatorB + 1

// Buy ETH with TokenA
outputAmountA = userInputEthValue
inputReserveA = tokenContractA.methods.balanceOf(exchangeAddressA)
outputReserveA = web3.eth.getBalance(exchangeAddressA)

// Cost
numeratorA = outputAmountA * inputReserveA * 1000
denominatorA = (outputReserveA - outputAmountA) * 997
inputAmountA = numeratorA / denominatorA + 1
```

### Liquidity Provider Fee

There is a 0.3% liquidity provider fee to swap from TokenA to ETH on the input exchange. There is another 0.3% liquidity provider fee to swap the remaining ETH to TokenB. 

```javascript
exchangeAFee = inputAmountA * 0.003
exchangeBFee = inputAmountB * 0.003
```

Since users only inputs Token A, it can be represented to them as:

```javascript
combinedFee = inputAmountA * 0.00591
```

### Exchange Rate

The exchange rate is simply the output amount divided by the input amount.

```javascript
rate = outputAmountB / inputAmountA
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

Uniswap allows traders to swap tokens and transfer the output to a new `recipient` address. This allows for a type of payment where the payer sends one token and the payee receives another. 

## ETH ⇄ ERC20 Trades

Coming soon...



## ERC20 ⇄ ERC20 Trades

Coming soon...



## Custom Pools

Coming soon...

