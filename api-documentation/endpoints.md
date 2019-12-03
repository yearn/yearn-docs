# Endpoints

- [`/v1/summary`](#v1summary)
  - [Request](#request)
  - [Response](#response)
- [`/v1/assets`](#v1assets)
  - [Request](#request-1)
  - [Response](#response-1)
- [`/v1/tickers`](#v1tickers)
  - [Request](#request-2)
  - [Response](#response-2)
- [`/v1/orderbook/:exchangeAddress`](#v1orderbookexchangeaddress)
  - [Request](#request-3)
  - [Response](#response-3)
- [`/v1/trades/:exchangeAddress`](#v1tradesexchangeaddress)
  - [Request](#request-4)
  - [Response](#response-4)

{% hint style="info" %}
All Uniswap pairs consist of ETH (treated as the base currency) paired with an ERC20 token (treated as the quote currency).
{% endhint %}

## `/v1/summary`

Returns data for the top 50 Uniswap pairs sorted by current ETH liquidity. Results are cached for 1 hour.

### Request

`GET https://api.uniswap.info/v1/summary`

### Response

```json
{
  "0x...": {                     // token address
    "name": "...",               // not necesssarily included for all pairs
    "symbol": "...",             // not necesssarily included for all pairs
    "exchange_address": "0x...",
    "last_price": "1.234",       // denominated in tokens/ETH
    "base_volume": "123.456",    // denominated in ETH
    "quote_volume": "1234.56"    // denominated in tokens
  },
  ...
}
```

## `/v1/assets`

Returns the top 50 Uniswap pairs sorted by current ETH liquidity. Results are cached for 24 hours.

### Request

`GET https://api.uniswap.info/v1/assets`

### Response

```json
{
  "0x...": {                    // token address
    "name": "...",              // not necesssarily included for all pairs
    "symbol": "...",            // not necesssarily included for all pairs
    "exchange_address": "0x..."
  },
  ...
}
```

## `/v1/tickers`

Returns data for the top 50 Uniswap pairs sorted by current ETH liquidity. Results are cached for 1 hour.

### Request

`GET https://api.uniswap.info/v1/tickers`

### Response

```json
{
  "0x...": {                     // token address
    "last_price": "1.234",       // denominated in tokens/ETH
    "base_volume": "123.456",    // denominated in ETH
    "quote_volume": "1234.56"    // denominated in tokens
  },
  ...
}
```

## `/v1/orderbook/:exchangeAddress`

Returns (simulated) orderbook data for the given Uniswap pair. Since Uniswap has a continuous orderbook, fixed amounts in an interval are chosen for bids and asks, and prices are derived from the Uniswap formula. Results are cached for 1 hour.

### Request

`GET https://api.uniswap.info/v1/orderbook/:exchangeAddress`

### Response

```json
{
  "timestamp": 1234567 // UNIX timestamp
  "bids": [
    ["12", "1.2"],     // denominated in ETH, tokens/ETH
    ["24", "1.1"],     // denominated in ETH, tokens/ETH
    ...
  ],
  "asks": [
    ["12", "1.3"],     // denominated in ETH, tokens/ETH
    ["24", "1.4"],     // denominated in ETH, tokens/ETH
    ...
  ]
}
```

## `/v1/trades/:exchangeAddress`

Returns all trades in the last 24 hours for the given Uniswap pair. Results are cached for 1 hour.

### Request

`GET https://api.uniswap.info/v1/trades/:exchangeAddress`

### Response

```json
[
  {
    "trade_id": "...", 
    "price": "1.234",           // denominated in tokens/ETH
    "base_volume": "123.456",   // denominated in ETH
    "quote_volume": "1234.56",  // denominated in tokens
    "trade_timestamp": 1234567, // UNIX timestamp
    "type": "sell"              // sell or buy
  },
  ...
]
```
