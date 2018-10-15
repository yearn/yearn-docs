# Factory API

## **initialize**Factory

{% code-tabs %}
{% code-tabs-item title="Smart Contract" %}
```javascript
initializeFactory(template: address):
```
{% endcode-tabs-item %}

{% code-tabs-item title="Web3" %}
```javascript
factory.methods.initializeFactory(template: string).send()
```
{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter | Description |
| :--- | ---: |
| template | Ethereum address of exchange template |



##  ****createExchange

```javascript
createExchange(token: address): address
```

| Parameter | Type | Description |
| :--- | :--- | ---: |
| token | address | Ethereum address of an ERC20 token |

| Returns |  |
| :--- | ---: |
| address | Ethereum address of a Uniswap exchange  |

 ****

## getExchange

```javascript
getExchange(token: address): address
```

| Parameter | Type | Description |
| :--- | :--- | ---: |
| token | address | Ethereum address of an ERC20 token |

| Returns |  |
| :--- | ---: |
| address | Ethereum address of a Uniswap exchange  |

\*\*\*\*

## get**Token**

```javascript
getToken(exchange: address): address
```

| Parameter | Type | Description |
| :--- | :--- | ---: |
| exchange | address | Ethereum address of a Uniswap exchange |

| Returns |  |
| :--- | ---: |
| address | Ethereum address of an ERC20 token  |

\*\*\*\*

## get**TokenWithId**

```javascript
getTokenWithId(token_id: uint256): address
```

| Parameter | Type | Description |
| :--- | :--- | ---: |
| token\_id | uint256 | Uniswap ID for an ERC20 token |

| Returns |  |
| :--- | ---: |
| address | Ethereum address of an ERC20 token  |

\*\*\*\*



