# Exchange API

## setup

{% code-tabs %}
{% code-tabs-item title="Smart Contract" %}

```javascript
// Can only be called by factory contract during createExchange()
setup(token_addr: address):
```

{% endcode-tabs-item %}
{% code-tabs-item title="Web3" %}

```javascript
// Can only be called by factory contract during createExchange()
exchangeContract.methods.setup(token: String).send()
```

{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter   |                        Description |
| :---------- | ---------------------------------: |
| token\_addr | Ethereum address of an ERC20 Token |

## addLiquidity

{% code-tabs %}
{% code-tabs-item title="Smart Contract" %}

```javascript
@payable
addLiquidity(
    min_liquidity: uint256,
    max_tokens: uint256,
    deadline: uint256
): uint256
```

{% endcode-tabs-item %}
{% code-tabs-item title="Web3" %}

```javascript
exchangeContract.methods.addLiquidity(min_liquidity, max_tokens, deadline).send({ value: ethValue })
```

{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter      | Type    |                Description |
| :------------- | :------ | -------------------------: |
| msg.value      | uint256 |        Amount of ETH added |
| min\_liquidity | uint256 |   Minimum minted liquidity |
| max\_tokens    | uint256 | Maximum ERC20 tokens added |
| deadline       | uint256 |       Transaction deadline |

| Returns |                                   |
| :------ | --------------------------------: |
| uint256 | Amount of liquidity tokens minted |

## removeLiquidity

{% code-tabs %}
{% code-tabs-item title="Smart Contract" %}

```javascript
removeLiquidity(
    amount: uint256;
    min_eth: uint256,
    min_tokens: uint256,
    deadline: uint256
): (uint256, uint256)
```

{% endcode-tabs-item %}
{% code-tabs-item title="Web3" %}

```javascript
exchangeContract.methods.removeLiquidity(amount, min_eth, max_tokens, deadline).send()
```

{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter   | Type    |                  Description |
| :---------- | :------ | ---------------------------: |
| amount      | uint256 |   Amount of liquidity burned |
| min\_eth    | uint256 |          Minimum ETH removed |
| min\_tokens | uint256 | Minimum ERC20 tokens removed |
| deadline    | uint256 |         Transaction deadline |

| Returns |                                 |
| :------ | ------------------------------: |
| uint256 |           Amount of ETH removed |
| uint256 | Amount of ERC20 tokens removed. |

## default

{% code-tabs %}
{% code-tabs-item title="Smart Contract" %}

```javascript
// Default function in Vyper replaces the "fallback" function in Solidity
@payable
__default__():
```

{% endcode-tabs-item %}
{% code-tabs-item title="Web3" %}

```javascript
web3.eth.sendTransaction({value: ethAmount})
```

{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter | Type    |        Description |
| :-------- | :------ | -----------------: |
| msg.value | uint256 | Amount of ETH sold |

## ethToTokenSwapInput

{% code-tabs %}
{% code-tabs-item title="Smart Contract" %}

```javascript
@payable
ethToTokenSwapInput(
    min_tokens: uint256,
    deadline: uint256
): uint256
```

{% endcode-tabs-item %}
{% code-tabs-item title="Web3" %}

```javascript
exchangeContract.methods.ethToTokenSwapInput(min_liquidity, max_tokens, deadline).send({ value: ethValue })
```

{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter   | Type    |                 Description |
| :---------- | :------ | --------------------------: |
| msg.value   | uint256 |          Amount of ETH sold |
| min\_tokens | uint256 | Minimum ERC20 tokens bought |
| deadline    | uint256 |        Transaction deadline |

| Returns |                               |
| :------ | ----------------------------: |
| uint256 | Amount of ERC20 tokens bought |

## ethToTokenTransferInput

{% code-tabs %}
{% code-tabs-item title="Smart Contract" %}

```javascript
@payable
ethToTokenTransferInput(
    min_tokens: uint256,
    deadline: uint256,
    recipient: address
): uint256
```

{% endcode-tabs-item %}
{% code-tabs-item title="Web3" %}

```javascript
exchangeContract.methods.ethToTokenTransferInput(min_liquidity, max_tokens, deadline, recipient).send({value: ethValue})
```

{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter   | Type    |                        Description |
| :---------- | :------ | ---------------------------------: |
| msg.value   | uint256 |                 Amount of ETH sold |
| min\_tokens | uint256 |        Minimum ERC20 tokens bought |
| deadline    | uint256 |               Transaction deadline |
| recipient   | address | Address that receives ERC20 tokens |

| Returns |                               |
| :------ | ----------------------------: |
| uint256 | Amount of ERC20 tokens bought |

## ethToTokenSwapOutput

{% code-tabs %}
{% code-tabs-item title="Smart Contract" %}

```javascript
@payable
ethToTokenSwapOutput(
    tokens_bought: uint256,
    deadline: uint256
): uint256
```

{% endcode-tabs-item %}
{% code-tabs-item title="Web3" %}

```javascript
exchangeContract.methods.ethToTokenSwapOutput(tokens_bought, deadline).send({value: ethValue})
```

{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter      | Type    |                   Description |
| :------------- | :------ | ----------------------------: |
| msg.value      | uint256 |              Maximum ETH sold |
| tokens\_bought | uint256 | Amount of ERC20 tokens bought |
| deadline       | uint256 |          Transaction deadline |

| Returns |                    |
| :------ | -----------------: |
| uint256 | Amount of ETH sold |

## ethToTokenTransferOutput

{% code-tabs %}
{% code-tabs-item title="Smart Contract" %}

```javascript
@payable
ethToTokenTransferOutput(
    tokens_bought: uint256,
    deadline: uint256,
    recipient: address
): uint256
```

{% endcode-tabs-item %}
{% code-tabs-item title="Web3" %}

```javascript
exchangeContract.methods.ethToTokenTransferOutput(tokens_bought, deadline, recipient: String).send({value: ethValue})
```

{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter      | Type    |                        Description |
| :------------- | :------ | ---------------------------------: |
| msg.value      | uint256 |                   Maximum ETH sold |
| tokens\_bought | uint256 |      Amount of ERC20 tokens bought |
| deadline       | uint256 |               Transaction deadline |
| recipient      | address | Address that receives ERC20 tokens |

| Returns |                    |
| :------ | -----------------: |
| uint256 | Amount of ETH sold |

## tokenToEthSwapInput

{% code-tabs %}
{% code-tabs-item title="Smart Contract" %}

```javascript
tokenToEthSwapInput(
    tokens_sold: uint256,
    min_eth: uint256,
    deadline: uint256
): uint256
```

{% endcode-tabs-item %}
{% code-tabs-item title="Web3" %}

```javascript
exchangeContract.methods.tokenToEthSwapInput(tokens_sold, min_eth, deadline).send()
```

{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter    | Type    |                 Description |
| :----------- | :------ | --------------------------: |
| tokens\_sold | uint256 | Amount of ERC20 tokens sold |
| min\_eth     | uint256 |          Minimum ETH bought |
| deadline     | uint256 |        Transaction deadline |

| Returns |                      |
| :------ | -------------------: |
| uint256 | Amount of ETH bought |

## tokenToEthTransferInput

{% code-tabs %}
{% code-tabs-item title="Smart Contract" %}

```javascript
tokenToEthTransferInput(
    tokens_sold: uint256,
    min_eth: uint256,
    deadline: uint256,
    recipient: address
): uint256
```

{% endcode-tabs-item %}
{% code-tabs-item title="Web3" %}

```javascript
exchangeContract.methods.tokenToEthTransferInput(tokens_sold, min_eth, deadline, recipient).send()
```

{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter    | Type    |                 Description |
| :----------- | :------ | --------------------------: |
| tokens\_sold | uint256 | Amount of ERC20 tokens sold |
| min\_eth     | uint256 |          Minimum ETH bought |
| deadline     | uint256 |        Transaction deadline |
| recipient    | address |   Address that receives ETH |

| Returns |                      |
| :------ | -------------------: |
| uint256 | Amount of ETH bought |

## tokenToEthSwapOutput

{% code-tabs %}
{% code-tabs-item title="Smart Contract" %}

```javascript
tokenToEthSwapOutput(
    eth_bought: uint256,
    max_tokens: uint256,
    deadline: uint256
): uint256
```

{% endcode-tabs-item %}
{% code-tabs-item title="Web3" %}

```javascript
exchangeContract.methods.tokenToEthSwapOutput(eth_bought, max_tokens, deadline: Integer).send()
```

{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter   | Type    |               Description |
| :---------- | :------ | ------------------------: |
| eth\_bought | uint256 |      Amount of ETH bought |
| max\_tokens | uint256 | Maximum ERC20 tokens sold |
| deadline    | uint256 |      Transaction deadline |

| Returns |                             |
| :------ | --------------------------: |
| uint256 | Amount of ERC20 tokens sold |

## tokenToEthTransferOutput

{% code-tabs %}
{% code-tabs-item title="Smart Contract" %}

```javascript
tokenToEthTransferOutput(
    eth_bought: uint256,
    max_tokens: uint256,
    deadline: uint256,
    recipient: address
): uint256

```

{% endcode-tabs-item %}
{% code-tabs-item title="Web3" %}

```javascript
exchangeContract.methods.tokenToEthTransferOutput(eth_bought, max_tokens, deadline: Integer, recipient: String).send()
```

{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter   | Type    |               Description |
| :---------- | :------ | ------------------------: |
| eth\_bought | uint256 |      Amount of ETH bought |
| max\_tokens | uint256 | Maximum ERC20 tokens sold |
| deadline    | uint256 |      Transaction deadline |
| recipient   | address | Address that receives ETH |

| Returns |                             |
| :------ | --------------------------: |
| uint256 | Amount of ERC20 tokens sold |

## tokenToTokenSwapInput

{% code-tabs %}
{% code-tabs-item title="Smart Contract" %}

```javascript
tokenToTokenSwapInput(
    tokens_sold: uint256,
    min_tokens_bought: uint256,
    min_eth_bought: uint256,
    deadline: uint256,
    token_addr: address
): uint256
```

{% endcode-tabs-item %}
{% code-tabs-item title="Web3" %}

```javascript
exchangeContract.methods.tokenToTokenSwapInput(
    tokens_sold, min_tokens_bought, min_eth_bought, deadline, token_addr
).send()
```

{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter           | Type    |                        Description |
| :------------------ | :------ | ---------------------------------: |
| tokens\_sold        | uint256 |  Amount of input ERC20 tokens sold |
| min\_tokens\_bought | uint256 | Minimum output ERC20 tokens bought |
| min\_eth\_bought    | uint256 | Minimum ETH bought as intermediary |
| deadline            | uint256 |               Transaction deadline |
| token\_addr         | address |      Address of output ERC20 token |

| Returns |                                      |
| :------ | -----------------------------------: |
| uint256 | Amount of output ERC20 tokens bought |

## tokenToTokenTransferInput

{% code-tabs %}
{% code-tabs-item title="Smart Contract" %}

```javascript
tokenToTokenTransferInput(
    tokens_sold: uint256,
    min_tokens_bought: uint256,
    min_eth_bought: uint256,
    deadline: uint256,
    recipient: address
    token_addr: address
): uint256
```

{% endcode-tabs-item %}
{% code-tabs-item title="Web3" %}

```javascript
exchangeContract.methods.tokenToTokenTransferInput(
    tokens_sold, min_tokens_bought, min_eth_bought, deadline, recipient, token_addr
).send()
```

{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter           | Type    |                               Description |
| :------------------ | :------ | ----------------------------------------: |
| tokens\_sold        | uint256 |         Amount of input ERC20 tokens sold |
| min\_tokens\_bought | uint256 |        Minimum output ERC20 tokens bought |
| min\_eth\_bought    | uint256 |        Minimum ETH bought as intermediary |
| deadline            | uint256 |                      Transaction deadline |
| recipient           | address | Address that receives output ERC20 tokens |
| token\_addr         | address |             Address of output ERC20 token |

| Returns |                                      |
| :------ | -----------------------------------: |
| uint256 | Amount of output ERC20 tokens bought |

## tokenToTokenSwapOutput

{% code-tabs %}
{% code-tabs-item title="Smart Contract" %}

```javascript
tokenToTokenSwapOutput(
    tokens_bought: uint256,
    max_tokens_sold: uint256,
    max_eth_sold: uint256,
    deadline: uint256,
    token_addr: address
): uint256
```

{% endcode-tabs-item %}
{% code-tabs-item title="Web3" %}

```javascript
exchangeContract.methods.tokenToTokenSwapOutput(
    tokens_bought, max_tokens_sold, max_eth_sold, deadline, token_addr
).send()
```

{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter         | Type    |                          Description |
| :---------------- | :------ | -----------------------------------: |
| tokens\_bought    | uint256 | Amount of output ERC20 tokens bought |
| max\_tokens\_sold | uint256 |    Maximum input ERC20 tokens bought |
| max\_eth\_sold    | uint256 |   Maximum ETH bought as intermediary |
| deadline          | uint256 |                 Transaction deadline |
| token\_addr       | address |        Address of output ERC20 token |

| Returns |                                   |
| :------ | --------------------------------: |
| uint256 | Amount of input ERC20 tokens sold |

## tokenToTokenTransferOutput

{% code-tabs %}
{% code-tabs-item title="Smart Contract" %}

```javascript
tokenToTokenTransferOutput(
    tokens_bought: uint256,
    max_tokens_sold: uint256,
    max_eth_sold: uint256,
    deadline: uint256,
    recipient: address,
    token_addr: address
): uint256
```

{% endcode-tabs-item %}
{% code-tabs-item title="Web3" %}

```javascript
exchangeContract.methods.tokenToTokenTransferOutput(
    tokens_bought, max_tokens_sold, max_eth_sold, deadline, recipient, token_addr
).send()
```

{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter         | Type    |                               Description |
| :---------------- | :------ | ----------------------------------------: |
| tokens\_bought    | uint256 |      Amount of output ERC20 tokens bought |
| max\_tokens\_sold | uint256 |         Maximum input ERC20 tokens bought |
| max\_eth\_sold    | uint256 |        Maximum ETH bought as intermediary |
| deadline          | uint256 |                      Transaction deadline |
| recipient         | address | Address that receives output ERC20 tokens |
| token\_addr       | address |             Address of output ERC20 token |

| Returns |                                   |
| :------ | --------------------------------: |
| uint256 | Amount of input ERC20 tokens sold |

## tokenToExchangeSwapInput

{% code-tabs %}
{% code-tabs-item title="Smart Contract" %}

```javascript
tokenToTokenSwapInput(
    tokens_sold: uint256,
    min_tokens_bought: uint256,
    min_eth_bought: uint256,
    deadline: uint256,
    exchange_addr: address
): uint256

```

{% endcode-tabs-item %}
{% code-tabs-item title="Web3" %}

```javascript
exchangeContract.methods.tokenToTokenSwapInput(
    tokens_sold, min_tokens_bought, min_eth_bought, deadline, exchange_addr
).send()
```

{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter           | Type    |                            Description |
| :------------------ | :------ | -------------------------------------: |
| tokens\_sold        | uint256 |      Amount of input ERC20 tokens sold |
| min\_tokens\_bought | uint256 |     Minimum output ERC20 tokens bought |
| min\_eth\_bought    | uint256 |     Minimum ETH bought as intermediary |
| deadline            | uint256 |                   Transaction deadline |
| exchange\_addr      | address | Address of output ERC20 token exchange |

| Returns |                                      |
| :------ | -----------------------------------: |
| uint256 | Amount of output ERC20 tokens bought |

## tokenToExchangeTransferInput

{% code-tabs %}
{% code-tabs-item title="Smart Contract" %}

```javascript
tokenToExchangeTransferInput(
    tokens_sold: uint256,
    min_tokens_bought: uint256,
    min_eth_bought: uint256,
    deadline: uint256,
    recipient: address
    exchange_addr: address
): uint256
```

{% endcode-tabs-item %}
{% code-tabs-item title="Web3" %}

```javascript
exchangeContract.methods.tokenToExchangeTransferInput(
    tokens_sold, min_tokens_bought, min_eth_bought, deadline, recipient, exchange_addr
).send()

```

{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter           | Type    |                               Description |
| :------------------ | :------ | ----------------------------------------: |
| tokens\_sold        | uint256 |         Amount of input ERC20 tokens sold |
| min\_tokens\_bought | uint256 |        Minimum output ERC20 tokens bought |
| min\_eth\_bought    | uint256 |        Minimum ETH bought as intermediary |
| deadline            | uint256 |                      Transaction deadline |
| recipient           | address | Address that receives output ERC20 tokens |
| exchange\_addr      | address |    Address of output ERC20 token exchange |

| Returns |                                      |
| :------ | -----------------------------------: |
| uint256 | Amount of output ERC20 tokens bought |

## tokenToExchangeSwapOutput

{% code-tabs %}
{% code-tabs-item title="Smart Contract" %}

```javascript
tokenToExchangeSwapOutput(
    tokens_bought: uint256,
    max_tokens_sold: uint256,
    max_eth_sold: uint256,
    deadline: uint256,
    exchange_addr: address
): uint256
```

{% endcode-tabs-item %}
{% code-tabs-item title="Web3" %}

```javascript
exchangeContract.methods.tokenToExchangeSwapOutput(
    tokens_bought, max_tokens_sold, max_eth_sold, deadline, exchange_addr
).send()
```

{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter         | Type    |                            Description |
| :---------------- | :------ | -------------------------------------: |
| tokens\_bought    | uint256 |   Amount of output ERC20 tokens bought |
| max\_tokens\_sold | uint256 |      Maximum input ERC20 tokens bought |
| max\_eth\_sold    | uint256 |     Maximum ETH bought as intermediary |
| deadline          | uint256 |                   Transaction deadline |
| exchange\_addr    | address | Address of output ERC20 token exchange |

| Returns |                                   |
| :------ | --------------------------------: |
| uint256 | Amount of input ERC20 tokens sold |

## tokenToExchangeTransferOutput

{% code-tabs %}
{% code-tabs-item title="Smart Contract" %}

```javascript
tokenToExchangeTransferOutput(
    tokens_bought: uint256,
    max_tokens_sold: uint256,
    max_eth_sold: uint256,
    deadline: uint256,
    recipient: address,
    exchange_addr: address
): uint256
```

{% endcode-tabs-item %}
{% code-tabs-item title="Web3" %}

```javascript
exchangeContract.methods.tokenToExchangeTransferOutput(
    tokens_bought, max_tokens_sold, max_eth_sold, deadline, recipient, exchange_addr
).send()
```

{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter         | Type    |                               Description |
| :---------------- | :------ | ----------------------------------------: |
| tokens\_bought    | uint256 |      Amount of output ERC20 tokens bought |
| max\_tokens\_sold | uint256 |         Maximum input ERC20 tokens bought |
| max\_eth\_sold    | uint256 |        Maximum ETH bought as intermediary |
| deadline          | uint256 |                      Transaction deadline |
| recipient         | address | Address that receives output ERC20 tokens |
| exchange\_addr    | address |    Address of output ERC20 token exchange |

| Returns |                                   |
| :------ | --------------------------------: |
| uint256 | Amount of input ERC20 tokens sold |

## getEthToTokenInputPrice

{% code-tabs %}
{% code-tabs-item title="Smart Contract" %}

```javascript
@constant
getEthToTokenInputPrice(eth_sold: uint256): uint256
```

{% endcode-tabs-item %}
{% code-tabs-item title="Web3" %}

```javascript
exchangeContract.methods.getEthToTokenInputPrice(eth_sold).call()
```

{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter | Type    |        Description |
| :-------- | :------ | -----------------: |
| eth\_sold | uint256 | Amount of ETH sold |

| Returns |                                           |
| :------ | ----------------------------------------: |
| uint256 | Amount of ERC20 tokens that can be bought |

## getEthToTokenOutputPrice

{% code-tabs %}
{% code-tabs-item title="Smart Contract" %}

```javascript
@constant
getEthToTokenOutputPrice(tokens_bought: uint256): uint256
```

{% endcode-tabs-item %}
{% code-tabs-item title="Web3" %}

```javascript
exchangeContract.methods.getEthToTokenOutputPrice(tokens_bought).call()
```

{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter      | Type    |                   Description |
| :------------- | :------ | ----------------------------: |
| tokens\_bought | uint256 | Amount of ERC20 tokens bought |

| Returns |                                 |
| :------ | ------------------------------: |
| uint256 | Amount of ETH that must be sold |

## getTokenToEthInputPrice

{% code-tabs %}
{% code-tabs-item title="Smart Contract" %}

```javascript
@constant
getTokenToEthInputPrice(tokens_sold: uint256): uint256
```

{% endcode-tabs-item %}
{% code-tabs-item title="Web3" %}

```javascript
exchangeContract.methods.getTokenToEthInputPrice(tokens_sold).call()
```

{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter    | Type    |                 Description |
| :----------- | :------ | --------------------------: |
| tokens\_sold | uint256 | Amount of ERC20 tokens sold |

| Returns |                                  |
| :------ | -------------------------------: |
| uint256 | Amount of ETH that can be bought |

## getTokenToEthOutputPrice

{% code-tabs %}
{% code-tabs-item title="Smart Contract" %}

```javascript
@constant
getTokenToEthOutputPrice(eth_bought: uint256): uint256
```

{% endcode-tabs-item %}
{% code-tabs-item title="Web3" %}

```javascript
exchangeContract.methods.getTokenToEthOutputPrice(eth_bought).call()
```

{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter   | Type    |          Description |
| :---------- | :------ | -------------------: |
| eth\_bought | uint256 | Amount of ETH bought |

| Returns |                                          |
| :------ | ---------------------------------------: |
| uint256 | Amount of ERC20 tokens that must be sold |

## tokenAddress

{% code-tabs %}
{% code-tabs-item title="Smart Contract" %}

```javascript
@constant
tokenAddress(): address
```

{% endcode-tabs-item %}
{% code-tabs-item title="Web3" %}

```javascript
exchangeContract.methods.tokenAddress().call()
```

{% endcode-tabs-item %}
{% endcode-tabs %}

| Returns |                                         |
| :------ | --------------------------------------: |
| address | Address of ERC20 token sold on exchange |

## factoryAddress

{% code-tabs %}
{% code-tabs-item title="Smart Contract" %}

```javascript
@constant
factoryAddress(): address
```

{% endcode-tabs-item %}
{% code-tabs-item title="Web3" %}

```javascript
exchangeContract.methods.factoryAddress().call()
```

{% endcode-tabs-item %}
{% endcode-tabs %}

| Returns |                                          |
| :------ | ---------------------------------------: |
| address | Address of factory that created exchange |

## name

{% code-tabs %}
{% code-tabs-item title="Smart Contract" %}

```javascript
// all exchange contracts have the same name
@constant
name(): bytes32 // Uniswap V1
```

{% endcode-tabs-item %}
{% code-tabs-item title="Web3" %}

```javascript
exchangeContract.methods.tokenAddress().call()
```

{% endcode-tabs-item %}
{% endcode-tabs %}

| Returns |                         |
| :------ | ----------------------: |
| bytes32 | Name of liquidity token |

## symbol

{% code-tabs %}
{% code-tabs-item title="Smart Contract" %}

```javascript
// all exchange contracts have the same symbol
@constant
symbol(): bytes32 // UNI-V1
```

{% endcode-tabs-item %}
{% code-tabs-item title="Web3" %}

```javascript
exchangeContract.methods.tokenAddress().call()
```

{% endcode-tabs-item %}
{% endcode-tabs %}

| Returns |                           |
| :------ | ------------------------: |
| bytes32 | Symbol of liquidity token |

## decimals

{% code-tabs %}
{% code-tabs-item title="Smart Contract" %}

```javascript
// all exchange contracts have the same decimals
@constant
decimals(): uint256 // 18
```

{% endcode-tabs-item %}
{% code-tabs-item title="Web3" %}

```javascript
exchangeContract.methods.decimals().call()
```

{% endcode-tabs-item %}
{% endcode-tabs %}

| Returns |                             |
| :------ | --------------------------: |
| uint256 | Decimals of liquidity token |

## balanceOf

{% code-tabs %}
{% code-tabs-item title="Smart Contract" %}

```javascript
@constant
balanceOf(_owner: address): uint256
```

{% endcode-tabs-item %}
{% code-tabs-item title="Web3" %}

```javascript
exchangeContract.methods.balanceOf(_owner).call()
```

{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter | Type    |      Description |
| :-------- | :------ | ---------------: |
| \_owner   | address | Ethereum address |

| Returns |                                    |
| :------ | ---------------------------------: |
| uint256 | Liquidity token balance of address |

## transfer

{% code-tabs %}
{% code-tabs-item title="Smart Contract" %}

```javascript
transfer(
    _to: address,
    _value : uint256
): bool
```

{% endcode-tabs-item %}
{% code-tabs-item title="Web3" %}

```javascript
exchangeContract.methods.transfer(_to, _value).send()
```

{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter | Type    |        Description |
| :-------- | :------ | -----------------: |
| \_to      | address |  Recipient address |
| \_value   | uint256 | Amount transferred |

| Returns |                                                 |
| :------ | ----------------------------------------------: |
| bool    | True if successful. Reverts or false on failure |

## transferFrom

{% code-tabs %}
{% code-tabs-item title="Smart Contract" %}

```javascript
transferFrom(
    _from: address,
    _to: address,
    _value : uint256
): bool
```

{% endcode-tabs-item %}
{% code-tabs-item title="Web3" %}

```javascript
exchangeContract.methods.transferFrom(_from, _to, _value).send()
```

{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter | Type    |        Description |
| :-------- | :------ | -----------------: |
| \_from    | address |     Sender address |
| \_to      | address |  Recipient address |
| \_value   | uint256 | Amount transferred |

| Returns |                                                 |
| :------ | ----------------------------------------------: |
| bool    | True if successful. Reverts or false on failure |

## approve

{% code-tabs %}
{% code-tabs-item title="Smart Contract" %}

```javascript
approve(
    _spender: address,
    _value: uint256
): bool
```

{% endcode-tabs-item %}
{% code-tabs-item title="Web3" %}

```javascript
exchangeContract.methods.approve(_spender, _value).send()
```

{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter | Type    |                 Description |
| :-------- | :------ | --------------------------: |
| \_spender | address | Address of approved spender |
| \_value   | uint256 |           Spender allowance |

| Returns |                                                 |
| :------ | ----------------------------------------------: |
| bool    | True if successful. Reverts or false on failure |

## allowance

{% code-tabs %}
{% code-tabs-item title="Smart Contract" %}

```javascript
allowance(
    _owner: address,
    _spender: address
): uint256
```

{% endcode-tabs-item %}
{% code-tabs-item title="Web3" %}

```javascript
exchangeContract.methods.allowance(_owner, _spender).call()
```

{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter | Type    |                      Description |
| :-------- | :------ | -------------------------------: |
| \_owner   | address | Address of liquidity token owner |
| \_spender | uint256 |      Address of approved spender |

| Returns |                   |
| :------ | ----------------: |
| uint256 | Spender allowance |
