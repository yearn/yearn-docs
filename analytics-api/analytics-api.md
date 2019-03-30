# Uniswap API

## api/v1/ticker

```text
https://uniswap-analytics.appspot.com/api/v1/ticker?exchangeAddress=
```

| Parameter | Description |
| :--- | ---: |
| exchangeAddress | Ethereum address of a Uniswap exchange |

| Returns |  |
| :--- | ---: |
| symbol | The token symbol for this exchange |
| startTime | UTC timestamp for earliest transaction referred to |
| endTime | UTC timestamp for latest transaction referred to |
| price | The marginal price for 1 ETH |
| invPrice | The marginal price for 1 unit of this ERC20 token in ETH |
| highPrice | The highest price within start and end time |
| lowPrice | The lowest price within start and end time |
| weightedAvgPrice | The average price of all trades within start and end time weighted by volume |
| priceChange | The delta in price from start to end time |
| priceChangePercent | The percent delta in price from start to end time |
| ethLiquidity | How much ETH this exchange holds |
| erc20Liquidity | How many ERC20 tokens this exchange holds |
| lastTradePrice | The most recent trade price |
| lastTradeEthQty | The most recent trade ETH quantity |
| lastTradeErc20Qty | The most recent trade ERC20 quantity |
| tradeVolume | How much volume this exchange has experienced in trades from start to end time |
| count | How many individual trades this exchange has experienced from start to end time |
| theme | \(Optional\) Hex color used for displaying this exchange |

