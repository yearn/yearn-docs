# Factory API

## **initialize**Factory

```javascript
initializeFactory(template: address):
```

| Parameter | Description |
| :--- | ---: |
| template | Ethereum address of exchange template |

\*\*\*\*[**Code**](https://github.com/Uniswap/contracts-vyper/blob/master/contracts/uniswap_factory.vy#L13)\*\*\*\*

\*\*\*\*

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

\*\*\*\*[**Code**](https://github.com/Uniswap/contracts-vyper/blob/master/contracts/uniswap_factory.vy#L19)\*\*\*\*

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

 ****[**Code**](https://github.com/Uniswap/contracts-vyper/blob/master/contracts/uniswap_factory.vy#L35)\*\*\*\*

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

\*\*\*\*[**Code**](https://github.com/Uniswap/contracts-vyper/blob/master/contracts/uniswap_factory.vy#L40)\*\*\*\*

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

\*\*\*\*[**Code**](https://github.com/Uniswap/contracts-vyper/blob/master/contracts/uniswap_factory.vy#L45)

\*\*\*\*



