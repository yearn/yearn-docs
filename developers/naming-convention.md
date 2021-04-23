# Naming conventions

## yVaults

### Dev Cheat Sheet (Examples)

- **Vanilla ERC20 tokens**
  - Name: `${token.symbol()} or override yVault`
  - Symbol: `yv${token.symbol()} or override`
    - **Examples:** `USDC yVault`, `yvUSDC`, `aLINK yVault`, `yvaLINK`
- **LP positions**
  - **Curve**
    - Name: `Curve + pool + Pool yVault`
      - **Examples:** `Curve sBTC Pool yVault`, `Curve 3pool yVault`, `Curve Y Pool yVault`
    - Symbol: `yvCurve-pool`
      - **Examples:** `yvCurve-sBTC`, `yvCurve-3pool`, `yvCurve-Y`. We make an exception for the last one and call it `yUSD`.
  - **Uniswap**
    - Name: `Uniswap + v${self.version()} + TOKEN-TOKEN + LP yVault`
      - **Examples:** `Uniswap v2 USDT-WETH LP yVault`, `Uniswap v2 WBTC-WETH LP yVault`
    - Symbol: `yvUni-TOKEN-TOKEN`
      - **Examples:** `yvUni-USDT-WETH`, `yvUni-WBTC-WETH`
    - Note: Version was included for Uniswap LP tokens to help limit confusion between UNI-v2 LP tokens and upcoming UNI-v3 LP tokens.
  - **Balancer**
    - Name: `Balancer + TOKEN-TOKEN + Pool yVault`
      - **Examples:** `Balancer USDT-WETH Pool yVault`, `Balancer WBTC-WETH Pool yVault`
    - Symbol: `yvBal-TOKEN-TOKEN`
      - **Examples:** `yvBal-USDT-WETH`, `yvBal-WBTC-WETH`
  - **SushiSwap**
    - Name: `SushiSwap + TOKEN-TOKEN + LP yVault`
      - **Examples:** `SushiSwap USDT-WETH LP yVault`, `Uniswap v2 WBTC-WETH LP yVault`
    - Symbol: `yvSushi-TOKEN-TOKEN`
      - **Examples:** `yvSushi-USDT-WETH`, `yvSushi-WBTC-WETH`
- **Experimental**
  - No hard rules for `name` or `symbol`, just be sure to end `name` with "yVault".
    - **Examples:** `yveCRV-DAO yVault`, `yveCRV-DAO`, `St. Banteg of Yearn Patron of Plebs Lido St. Ether yVault`, `sboypoplyvstETH`

### Overview and Explanation

- Acceptable alternative names include Yearn Vaults, or informally referring to the product as vaults.
- When referring to a specific yVault, the preferred name is generally `TOKEN + yVault`; this matches the `name` field on the yVault contract. However, it is also acceptable to use `yvTOKEN + Vault`, `Yearn + TOKEN + Vault` or `yvTOKEN`; the latter matches `symbol` in the contract.
  - **Examples:** `DAI yVault`, `yvDAI Vault`, `Yearn DAI Vault`, or simply `yvDAI`
- For each yVault, name and symbol conventions are as follows:
  - Name: `${token.symbol()} or override yVault`
  - Symbol: `yv${token.symbol()} or override`
- A `version` field is included in the token contract to correspond to the major yVault release version.
  - Additionally, developers may find it useful to denote `version` within the `name` field itself to help clarify the token to be deposited. Useful examples include Uniswap LPs (below), and also v1 vs v2 Aave aTokens.
- The predominant use case for name and symbol override is for LP tokens. The use of the term `Pool` or `LP` is interchangeable, and will be selected based on colloquial use for each protocol.
  - For instance, Curve and Balancer LP positions are typically referred to as pools since they can contain more than two tokens, while Uniswap and SushiSwap positions are typically referred to as LPs.
  - **Curve**
    - Name: `Curve + pool + Pool yVault`
      - **Examples:** `Curve sBTC Pool yVault`, `Curve 3pool yVault`, `Curve Y Pool yVault`
      - In this case, `pool` is taken directly from Curve.fi's UI, and we can adjust for capitalization as needed. In the case of the `3pool`, the redundant "Pool" is removed.
    - Symbol: `yvCurve-pool`
      - **Examples:** `yvCurve-sBTC`, `yvCurve-3pool`, `yvCurve-Y`
    - Note: In this methodology, `yvCurve-Y` refers to the vault previously known as `yUSD`. Please see below for a more detailed discussion on proper use of `yUSD`.
  - **Uniswap**
    - Name: `Uniswap + v${self.version()} + TOKEN-TOKEN + LP yVault`
      - **Examples:** `Uniswap v2 USDT-WETH LP yVault`, `Uniswap v2 WBTC-WETH LP yVault`
    - Symbol: `yvUni-TOKEN-TOKEN`
      - **Examples:** `yvUni-USDT-WETH`, `yvUni-WBTC-WETH`
    - Note: Version was included for Uniswap LP tokens to help limit confusion between UNI-v2 LP tokens and upcoming UNI-v3 LP tokens.
  - **Balancer**
    - Name: `Balancer + TOKEN-TOKEN + Pool yVault`
      - **Examples:** `Balancer USDT-WETH Pool yVault`, `Balancer WBTC-WETH Pool yVault`
    - Symbol: `yvBal-TOKEN-TOKEN`
      - **Examples:** `yvBal-USDT-WETH`, `yvBal-WBTC-WETH`
    - Note: Since Balancer allows more than two tokens per pool, append as many `TOKEN` as needed for the pool in question.
  - **SushiSwap**
    - Name: `SushiSwap + TOKEN-TOKEN + LP yVault`
      - **Examples:** `SushiSwap USDT-WETH LP yVault`, `Uniswap v2 WBTC-WETH LP yVault`
    - Symbol: `yvSushi-TOKEN-TOKEN`
      - **Examples:** `yvSushi-USDT-WETH`, `yvSushi-WBTC-WETH`

## yVault Want Token

- In Yearn's UI, it may be useful to denote the desired token to deposit into a specific yVault. For basic ERC20 `want` tokens, `name` and `symbol` can be pulled directly from the token contract and utilized as-is.
  - **Examples:** `USD Coin`, `USDC`, `ChainLink Token`, `LINK`
- However, for LP positions, naming needs to be standardized.
  - Curve
    - Name: `Curve + pool + Pool`
      - **Examples:** `Curve sBTC Pool`, `Curve 3pool`, `Curve Y Pool`, `Curve Compound Pool`
      - In this case, `pool` is taken directly from Curve.fi's UI, and we can adjust for capitalization as needed. In the case of the `3pool`, the redundant "Pool" is removed.
    - Symbol: `crvPOOL or override`
      - **Examples:** `crvBUSD`, `crvCOMP`, `crvGUSD`, `crvMUSD`, `crvTBTC`, `crvSBTC`, `yCRV`, `3Crv`
    - These names were chosen as `crvBUSD` and `crvSBTC` are already fairly widely used, and applying this formula works well for other pools. `yCRV` and `3Crv` are the allowed exceptions, as `yCRV` is the most widely used name for that pool, and `3Crv` usage is now fairly common with the recent admin fee distribution.
  - Uniswap
    - Name: `Uniswap + v${self.version()} + TOKEN-TOKEN + LP`
      - **Examples:** `Uniswap v2 USDT-WETH LP`, `Uniswap v2 WBTC-WETH LP`
    - Symbol: `TOKEN-TOKEN UNI`
      - **Examples:** `USDT-WETH UNI`, `WBTC-WETH UNI`
  - Balancer
    - Name: `Balancer + TOKEN-TOKEN + Pool`
      - **Examples:** `Balancer USDT-WETH Pool`, `Balancer WBTC-WETH Pool`
    - Symbol: `TOKEN-TOKEN BPT`
      - **Examples:** `USDT-WETH BPT`, `WBTC-WETH BPT`
    - Note: Since Balancer allows more than two tokens per pool, append as many `TOKEN` as needed for the pool in question.
  - SushiSwap
    - Name: `SushiSwap + TOKEN-TOKEN + LP`
      - **Examples:** `SushiSwap USDT-WETH LP`, `Uniswap v2 WBTC-WETH LP`
    - Symbol: `TOKEN-TOKEN SLP`
      - **Examples:** `USDT-WETH SLP`, `WBTC-WETH SLP`

## yUSD

- While the term `yUSD` was used to refer to the Curve Y Pool yVault in the past, under our updated naming convention this vault token is now `yvCurve-Y`. However, usage of `yUSD` is still permissable when referring to the asset itself.
  - **Example:** Yearn pays monthly grants in `yUSD`.
- In the future, if Yearn creates a new `yUSD` that is a collection of several yVault tokens (as has been previously discussed), then the current `yUSD` will simply be referred to as `yvCurve-Y` and only the new token will be `yUSD`.

## yEarn

- These are Yearn's original yield-aware tokens, whose v2 and v3 contracts can be found [here](https://docs.yearn.finance/developers/deployed-contracts-registry#v2-yield-tokens).
- These products should be referred to as yEarn Tokens, `underlying token name + Earn`, or `y{token.symbol()}v${self.version()}`
  - **Examples:** `yDAIv2`, `yDAI Earn`, `yBUSDv3`, `yBUSD Earn`

## Test Products

- For deployed contracts that have not reached their final production version, a simple modification is included to designate these on the contract level as being test products.
  - Name: `${token.symbol()} or override + Test + Product`
  - Symbol: `yt${token.symbol()} or override`
  - **Examples:** `DAI Test yVault`, `ytDAI`
- Additionally, the v2 yVault contracts have upgradeable `name` and `symbol` fields. This means that should a test contract perform well, these fields can be updated to reflect that it is no longer a test contract, removing the need to deploy new contracts.

## Future Products

- Future products can follow a simple naming convention: `y + product`, where the product and any potential token names follow similar guidelines as above with yVaults. These can then be further modified as needed based on the product\(s\).
  - **Examples:** `ySwap`, `yBorrow`, `yTrade`
