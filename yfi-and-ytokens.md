# YFI and yTokens

## YFI

- Yearn Governance token
- Only 30,000 minted and already fully distributed
  - Governance can mint more, if proposal to do so passes.

## yTokens

[Glossary definition](https://docs.yearn.finance/defi-glossary#ytoken).

YTokens are like a deposit receipt. They represent the liquidity provided in a Yearn product.

For example, if you deposit DAI in y.curve.fi you will receive yDAI in return.

If the product you are providing liquidity to generates profit, your yTokens will increase in value, since they represent a share of that pool. That's why you might observe a price growth. When you withdraw liquidity from the pool, your yToken will be burned.

yTokens are [ERC20](https://docs.ethhub.io/built-on-ethereum/erc-token-standards/erc20/), meaning they can be transfered and traded as any other common Ethereum token.

## yUSD

- See our [doc on yUSD](https://docs.yearn.finance/yusd) for detailed info
- LP token for yearn's yCRV yVault
- aka `yyCRV` or `yyDAI+yUSDC+yUSDT+yTUSD`
- When you deposit yCRV into the yVault you receive yUSD\*\*\*\* LP tokens
- earns interest via yCRV, fees and yield farming rewards via the vault strategy

## yCRV

- LP token for yearn's Y pool at Curve.fi/y
- Aka `yDAI+yUSDC+yUSDT+yTUSD`
- Interest earning token representing your share of the Y pool composed of DAI, USDT, USDC, and TUSD
