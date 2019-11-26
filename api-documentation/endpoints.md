# Endpoints

- `/pair/:tokenAddress`
  - Request
  - Response
- `/pairs`
  - Request
  - Response


## `/pair/:tokenAddress`

Returns data for a given Uniswap pair.

{% hint style="info" %}
All Uniswap pairs consist of an ERC20 token paired against ETH.
{% endhint %}

### Request

`GET https://api.uniswap.info/pair/:tokenAddress`

### Response

```javascript
{
  "token_address": "0x...",                 // normalized to checksum
  "token_name": "...",                      // not included for all pairs
  "token_symbol": "...",                    // not included for all pairs
  "liquidity_last": "1.111111111111111111", // in units of ETH
  "price_last": "2.222222222222222222",     // in units of x tokens / 1 ETH
  "volume_24h": {
    "ETH": "3.333333333333333333",          // in units of ETH
    "0x...": "4.444444444444444444"         // in units of tokens
  }
}
```

## `/pairs`

Returns data for all Uniswap pairs.

### Request

`GET https://api.uniswap.info/pairs`

### Response

```javascript
{
  "pairs": [
    { ... }, // see `/pair/:tokenAddress` for the structure of return pair data
    ...
  ],
  "pairs_count": 123
}
```

