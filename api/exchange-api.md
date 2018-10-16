# Exchange API

## **setup**

{% code-tabs %}
{% code-tabs-item title="Smart Contract" %}
```javascript
setup(token_addr: address):
```
{% endcode-tabs-item %}

{% code-tabs-item title="Web3" %}
```swift
// Setup is called by the factory at time of creation 
// It can only be called once and never needs to be called from Web3
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
// Strings should represent integer values

ethValue: String 

exchangeContract.methods.addLiquidity(
    min_liquidity: String, 
    max_tokens: String,
    deadline: Integer
).send({value: ethValue})
```
{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter | Type | Description |
| :--- | :--- | ---: |
| min\_liquidity | uint256 | Minimum minted liquidity |
| max\_tokens | uint256 | Maximum ERC20 tokens deposited |
| deadline | uint256 | Transaction deadline |
| msg.value | wei | Amount of ETH added |

|  |  |
| :--- | ---: |
| uint256 | Amount of liquidity tokens minted  |

 ****

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
factoryContract.methods.initializeFactory(token: String).send()
```
{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter | Type | Description |
| :--- | :--- | ---: |
| amount | uint256 | Minimum minted liquidity |
| min\_eth | uint256 | Maximum ERC20 tokens deposited |
| min\_tokens | uint256 | Transaction deadline |
| deadline | uint256 | Amount of ETH deposited |

|  |  |
| :--- | ---: |
| uint256 | Amount of ETH removed  |
| uint256 | Amount of ERC20 tokens removed. |

 ****

