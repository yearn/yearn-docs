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
factoryContract.methods.initializeFactory(template: String).send()
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
addLiquidity(
    min_liquidity: uint256, 
    max_tokens: uint256, 
    deadline: uint256
): uint256
```
{% endcode-tabs-item %}

{% code-tabs-item title="Web3" %}
```swift
factoryContract.methods.initializeFactory(token: String).send()
```
{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter | Type | Description |  |
| :--- | :--- | :--- | :--- |
| min\_liquidity | uint256 | Minimum minted liquidity |  |
| max\_tokens | uint256 | Maximum tokens deposited |  |
| deadline | uint256 | Transaction deadline |  |
| msg.value | wei | Amount of Ether deposited |  |

|  |  |
| :--- | ---: |
| uint256 | Amount of liquidity tokens minted  |

 ****



