# Factory API

## **initialize**Factory

{% code-tabs %}
{% code-tabs-item title="Smart Contract" %}
```javascript
initializeFactory(template: address):
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
| template | Ethereum address of exchange template |



##  ****createExchange

{% code-tabs %}
{% code-tabs-item title="Smart Contract" %}
```javascript
createExchange(token: address): address
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
| token | address | Ethereum address of an ERC20 token |

| Returns |  |
| :--- | ---: |
| address | Ethereum address of a Uniswap exchange  |

 ****

## getExchange

{% code-tabs %}
{% code-tabs-item title="Smart Contract" %}
```javascript
@constant
getExchange(token: address): address
```
{% endcode-tabs-item %}

{% code-tabs-item title="Web3" %}
```swift
factoryContract.methods.getExchange(token: String).call()
```
{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter | Type | Description |
| :--- | :--- | ---: |
| token | address | Ethereum address of an ERC20 token |

| Returns |  |
| :--- | ---: |
| address | Ethereum address of a Uniswap exchange  |

\*\*\*\*

## get**Token**

{% code-tabs %}
{% code-tabs-item title="Smart Contract" %}
```javascript
@constant
getToken(exchange: address): address
```
{% endcode-tabs-item %}

{% code-tabs-item title="Web3" %}
```swift
factoryContract.methods.getToken(exchange: String).call()
```
{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter | Type | Description |
| :--- | :--- | ---: |
| exchange | address | Ethereum address of a Uniswap exchange |

| Returns |  |
| :--- | ---: |
| address | Ethereum address of an ERC20 token  |

\*\*\*\*

## get**TokenWithId**

{% code-tabs %}
{% code-tabs-item title="Smart Contract" %}
```javascript
@constant
getTokenWithId(token_id: uint256): address
```
{% endcode-tabs-item %}

{% code-tabs-item title="Web3" %}
```swift
factoryContract.methods.getToken(exchange: BigNumber).call()
```
{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter | Type | Description |
| :--- | :--- | ---: |
| token\_id | uint256 | Uniswap ID for an ERC20 token |

| Returns |  |
| :--- | ---: |
| address | Ethereum address of an ERC20 token  |

\*\*\*\*



