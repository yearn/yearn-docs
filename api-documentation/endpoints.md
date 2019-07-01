# Endpoints

- `/status`
  - Request
  - Response
- `/pairs`
  - Request
  - Response
- `/pair/:tokenAddress`
  - Request
  - Response

## `/status`

Status endpoint to check whether the API is operational.

### Request

`GET https://api.uniswap.info/status`

### Response

`200 Success.`

## `/pairs`

Returns all Uniswap pairs supported by the API.

{% hint style="info" %}
All tokens are paired are against ETH.
{% endhint %}

### Request

`GET https://api.uniswap.info/pairs`

### Response

Note that `token_name` and `token_symbol` are optional fields, and are not present for every pair.

```json
200

{
  "pairs": [
    { "token_address": "0x9f8F72aA9304c8B593d555F12eF6589cC3A579A2", "token_name": "Maker", "token_symbol": "MKR" },
    ...
  ],
  "pairs_count": 100
}
```

## `/pair/:tokenAddress`

Returns 24-hour ETH and token volumes and last price for a given Uniswap pair.

{% hint style="info" %}
Prices are quoted relative to ETH, i.e. x tokens / 1 ETH.
{% endhint %}

### Request

`GET https://api.uniswap.info/pair/:tokenAddress`

### Response

```json
200

{
  "volume_24h": {
    "ETH": "123.123123123123123123",
    <tokenAddress>: "456.456456456456456456"
  },
  "price_last": "0.467475382554979798"
}
```