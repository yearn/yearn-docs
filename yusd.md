# yUSD

yUSD is an ERC-20 token issued by Yearn that **represents shares** in the most popular vault: the yCRV Vault \(listed as `curve.fi/y LP` on [vaults page](https://yearn.finance/vaults)\).

yUSD makes DeFi simple by automatically maximizing yield and minimizing risk for depositors. On the backend, the yCRV Vault implements modular, autonomous, yield-aware strategies.

These are created and regularly updated by Yearn's community, all under the **control of Yearn governance.**

## How to Get yUSD

Full visual walkthrough here: [How to Mint yUSD](how-to-guides/how-to-mint-yusd.md).

_Supported wallets: Metamask, Trustwallet, Trezor, or Torus._

1. Load your wallet with DAI, USDC, USDT, TUSD, or yCRV.
2. Go to [vaults.finance](https://vaults.finance/).
3. Connect your wallet.
4. Deposit your coins into the vault, receive yUSD.

## yUSD in Detail

You may also see yUSD referred to as `yyCRV` and `yyDAI+yUSDC+yUSDT+yTUSD` – both of these names are accurate and describe yUSD's composition.

yUSD accrues earnings from **three tiers** of Yearn's modular strategies:

### Tier 1: Money Markets

At the base level, DAI, USDC, USDT, and TUSD are each wrapped into our 3rd generation yield-aware tokens: yDAI, yUSDC, yUSDT, and yTUSD. These tokens autonomously seek out the **highest single-asset ROI** from Aave, Compound, and dydx.

### Tier 2: Y Curve Pool

At the next level up, yDAI, yUSDC, yUSDT, and yTUSD provide liquidity in the **Curve and Yearn partnership pool** \(curve.fi/y\). yCRV – the [LP token](https://docs.yearn.finance/defi-glossary#liquidity-providers) for this pool grows in value from fees charged on stablecoin swaps within the pool.

It also generates CRV rewards which are harvested in the next tier up.

### Tier 3: Sustainable Yield

At the highest level, yUSD accesses community developed yield strategies to take advantage of emergent opportunities in the DeFi space.

Created by developers who are rewarded for their efforts, these strategies are assessed and voted on before being incorporated into the Yearn system.

At this tier the current strategy sits on top of the lower two tiers and **harvests CRV rewards to recycle them back into yCRV**—increasing the vault's base asset and the value of yUSD.

## Resources

- yUSD
  - CoinGecko: [https://www.coingecko.com/en/coins/yusd](https://www.coingecko.com/en/coins/yusd)
  - yUSD Token contract: [0x5dbcF33D8c2E976c6b560249878e6F1491Bca25c](https://etherscan.io/address/0x5dbcF33D8c2E976c6b560249878e6F1491Bca25c)
- Code
  - The vaults.finance source code on [GitHub](https://github.com/banteg/yearn-recycle)
  - The current strategy: [StrategyCurveYCRVVoter](https://etherscan.io/address/0xc999fb87AcA383A63D804A575396F65A55aa5aC8#code)
- FAQ
  - [https://docs.yearn.finance/faq\#vaults](https://docs.yearn.finance/faq#vaults)
