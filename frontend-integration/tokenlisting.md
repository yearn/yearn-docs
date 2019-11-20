# Token Listing

It is possible that a token you are interested in is not included in the token dropdown on [https://uniswap.exchange/swap](https://uniswap.exchange/swap), however, all tokens that have a deployed uniswap exhchange are supported on the the front-end.

There are three ways to interact with tokens that are not yet included on the default list.

## 1. Paste the token address into the search box.

If a token is not included in the list of tokens, try pasting the token address into the search box. It should populate the dropdown with the token you are looking for.

![](../.gitbook/assets/tokensearch.png)

## 2. Custom Linking

[https://uniswap.exchange](https://uniswap.exchange) supports custom linking to all tokens that have a Uniswap exchange. See [this page](linking.md) for details on how to link.

For example, to populate the output token field with an unlisted coin, we can specify the outputCurrency in the URL and pass in the token's address like this:

`https://uniswap.exchange/swap?outputCurrency=0xfA3E941D1F6B7b10eD84A0C211bfA8aeE907965e`

## 3. Make a request to get your token listed

For tokens that have high market caps, high liquidity provision, or high dex trading volume, you can fill out a request to be added to the drop down menu on uniswap.exhange here: [https://github.com/Uniswap/uniswap-frontend/issues/new?assignees=&labels=token+request&template=token-request.md&title=](https://github.com/Uniswap/uniswap-frontend/issues/new?assignees=&labels=token+request&template=token-request.md&title=)

