# Factory API

## initializeFactory

{% code-tabs %}
{% code-tabs-item title="Smart Contract" %}

```javascript
initializeFactory(template: address)
```

{% endcode-tabs-item %}
{% code-tabs-item title="Web3" %}

```javascript
factoryContract.methods.initializeFactory(template).send()
```

{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter | Description |
| :--- | ---: |
| template | Ethereum address of exchange template |

## createExchange

{% code-tabs %}
{% code-tabs-item title="Smart Contract" %}

```javascript
createExchange(token: address): address
```

{% endcode-tabs-item %}
{% code-tabs-item title="Web3" %}

```javascript
factoryContract.methods.initializeFactory(token).send()
```

{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter | Type | Description |
| :--- | :--- | ---: |
| token | address | Ethereum address of an ERC20 token |

| Returns |  |
| :--- | ---: |
| address | Ethereum address of a Uniswap exchange  |

## getExchange

{% code-tabs %}
{% code-tabs-item title="Smart Contract" %}

```javascript
@constant
getExchange(token: address): address
```

{% endcode-tabs-item %}
{% code-tabs-item title="Web3" %}

```javascript
factoryContract.methods.getExchange(token).call()
```

{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter | Type | Description |
| :--- | :--- | ---: |
| token | address | Ethereum address of an ERC20 token |

| Returns |  |
| :--- | ---: |
| address | Ethereum address of a Uniswap exchange  |

## getToken

{% code-tabs %}
{% code-tabs-item title="Smart Contract" %}

```javascript
@constant
getToken(exchange: address): address
```

{% endcode-tabs-item %}
{% code-tabs-item title="Web3" %}

```javascript
factoryContract.methods.getToken(exchange).call()
```

{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter | Type | Description |
| :--- | :--- | ---: |
| exchange | address | Ethereum address of a Uniswap exchange |

| Returns |  |
| :--- | ---: |
| address | Ethereum address of an ERC20 token  |

## getTokenWithId

{% code-tabs %}
{% code-tabs-item title="Smart Contract" %}

```javascript
@constant
getTokenWithId(token_id: uint256): address
```

{% endcode-tabs-item %}
{% code-tabs-item title="Web3" %}

```javascript
factoryContract.methods.getToken(exchange).call()
```

{% endcode-tabs-item %}
{% endcode-tabs %}

| Parameter | Type | Description |
| :--- | :--- | ---: |
| token\_id | uint256 | Uniswap ID for an ERC20 token |

| Returns |  |
| :--- | ---: |
| address | Ethereum address of an ERC20 token  |
