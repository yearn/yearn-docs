# Exchange API

## **setup**

{% code-tabs %}
{% code-tabs-item title="Smart Contract" %}
```javascript
// Can only be called by factory contract during createExchange()

setup(token_addr: address):
```
{% endcode-tabs-item %}

{% code-tabs-item title="Web3" %}
```swift
// Can only be called by factory contract during createExchange()

exchangeContract.methods.setup(token: String).send()
```
{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter | Description |
| :--- | ---: |
| token\_addr | Ethereum address of an ERC20 Token |



##  ****addLiquidity

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
```swift
ethValue: String        // big integer, msg.value

exchangeContract.methods.addLiquidity(
    min_liquidity: String,        // big integer
    max_tokens: String,           // big integer
    deadline: Integer
).send({value: ethValue}) 
```
{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter | Type | Description |
| :--- | :--- | ---: |
| msg.value | uint256 | Amount of ETH added |
| min\_liquidity | uint256 | Minimum minted liquidity |
| max\_tokens | uint256 | Maximum ERC20 tokens added |
| deadline | uint256 | Transaction deadline |

| Returns |  |
| :--- | ---: |
| uint256 | Amount of liquidity tokens minted  |



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
```swift
exchangeContract.methods.removeLiquidity(
    amount: String,        // big integer
    min_eth: String,       // big integer
    max_tokens: String     // big integer
    deadline: Integer    
).send() 
```
{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter | Type | Description |
| :--- | :--- | ---: |
| amount | uint256 | Amount of liquidity burned |
| min\_eth | uint256 | Minimum ETH removed |
| min\_tokens | uint256 | Minimum ERC20 tokens removed |
| deadline | uint256 | Transaction deadline |

| Returns |  |
| :--- | ---: |
| uint256 | Amount of ETH removed  |
| uint256 | Amount of ERC20 tokens removed. |

 ****

##  **default**

{% code-tabs %}
{% code-tabs-item title="Smart Contract" %}
```javascript
// Default function in Vyper replaces the "fallback" function in Solidity

@payable
__default__(): 
```
{% endcode-tabs-item %}

{% code-tabs-item title="Web3" %}
```swift
ethAmount: String        // big integer, msg.value
web3.eth.sendTransaction({value: ethAmount})
```
{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter | Type | Description |
| :--- | :--- | ---: |
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
```swift
ethValue: String        // big integer, msg.value

exchangeContract.methods.ethToTokenSwapInput(
    min_liquidity: String,        // big integer
    max_tokens: String,           // big integer
    deadline: Integer
).send({value: ethValue})
```
{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter | Type | Description |
| :--- | :--- | ---: |
| msg.value | uint256 | Amount of ETH sold |
| min\_tokens | uint256 | Minimum ERC20 tokens bought |
| deadline | uint256 | Transaction deadline |

| Returns |  |
| :--- | ---: |
| uint256 | Amount of ERC20 tokens bought  |

 ****

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
```swift
ethValue: String        // big integer, msg.value

exchangeContract.methods.ethToTokenTransferInput(
    min_liquidity: String,        // big integer
    max_tokens: String,           // big integer
    deadline: Integer,
    recipient: String
).send({value: ethValue})
```
{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter | Type | Description |
| :--- | :--- | ---: |
| msg.value | uint256 | Amount of ETH sold |
| min\_tokens | uint256 | Minimum ERC20 tokens bought |
| deadline | uint256 | Transaction deadline |
| recipient | address | Address that receives ERC20 tokens |

| Returns |  |
| :--- | ---: |
| uint256 | Amount of ERC20 tokens bought  |

 ****

## ethToTokenSwap**Output**

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
```swift
ethValue: String        // big integer, msg.value

exchangeContract.methods.ethToTokenSwapInput(
    min_liquidity: String,        // big integer
    max_tokens: String,           // big integer
    deadline: Integer
).send({value: ethValue})
```
{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter | Type | Description |
| :--- | :--- | ---: |
| msg.value | uint256 | Maximum ETH sold |
| tokens\_bought | uint256 | Amount of ERC20 tokens bought |
| deadline | uint256 | Transaction deadline |

| Returns |  |
| :--- | ---: |
| uint256 | Amount of ETH sold |

 ****

## ethToTokenTransferOutput

{% code-tabs %}
{% code-tabs-item title="Smart Contract" %}
```javascript
@payable
ethToTokenTransferOutput(
    min_tokens: uint256, 
    deadline: uint256,
    recipient: address
): uint256
```
{% endcode-tabs-item %}

{% code-tabs-item title="Web3" %}
```swift
ethValue: String        // big integer, msg.value

exchangeContract.methods.ethToTokenSwapInput(
    min_liquidity: String,        // big integer
    max_tokens: String,           // big integer
    deadline: Integer,
    recipient: String
).send({value: ethValue})
```
{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter | Type | Description |
| :--- | :--- | ---: |
| msg.value | uint256 | Maximum ETH sold |
| tokens\_bought | uint256 | Amount of ERC20 tokens bought |
| deadline | uint256 | Transaction deadline |
| recipient | address | Address that receives ERC20 tokens |

| Returns |  |
| :--- | ---: |
| uint256 | Amount of ETH sold |

\*\*\*\*

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
```swift
exchangeContract.methods.tokenToEthSwapInput(
    tokens_sold: String,        // big integer
    min_eth: String,            // big integer
    deadline: Integer
).send()
```
{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter | Type | Description |
| :--- | :--- | ---: |
| tokens\_sold | uint256 | Amount of ERC20 tokens sold |
| min\_eth | uint256 | Minimum ETH bought |
| deadline | uint256 | Transaction deadline |

| Returns |  |
| :--- | ---: |
| uint256 | Amount of ETH bought  |

 ****

