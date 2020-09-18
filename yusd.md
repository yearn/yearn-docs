# yUSD

yUSD ![](https://i.imgur.com/XdOzWfW.png =20x) is an ERC-20 token issued by Yearn that represents shares in our most popular vault: the yCRV Vault (listed as `curve.fi/y LP` on our [vaults page](https://yearn.finance/vaults)).

yUSD makes DeFi simple by automatically maximizing yield and minimizing risk for our depositors. On the backend, the yCRV Vault implements modular, autonomous, yield-aware strategies. These are created and regularly updated by the best minds in DeFi, all under the control of Yearn governance.

## How to Get yUSD

_Supported wallets: Metamask, Trustwallet, Trezor, or Torus._

1. Load your wallet with DAI, USDC, USDT, TUSD, or yCRV
1. [Go to vaults.finance](https://vaults.finance/)
1. Connect your wallet
1. Deposit your coins into the vault, receive yUSD

## DeFi's Reserve Currency

yUSD is becoming the reserve currency for DeFi as more and more protocols adopt it. It's a better USD—a smart-asset backed by a basket of stablecoins autonomously working to harvest yield from the industry's best and most trusted sources such as Aave, Compound, dydx, and Curve. And all without exposing deposits to impermanent loss.

Yearn's philosophy is to not jump into the newest yield opportunities right away. We do due diligence and assess risk-adjusted return to ensure sustainability and safety for our users and community.

## yUSD in Detail

You may also see yUSD referred to as `yyCRV` and `yyDAI+yUSDC+yUSDT+yTUSD`—both of these names are accurate and describe yUSD's composition.

yUSD accrues earnings from three tiers of Yearn's modular strategies:

### Tier 1: Money Markets

At the base level, DAI, USDC, USDT, and TUSD are each wrapped into our 3rd generation yield-aware tokens: yDAI, yUSDC, yUSDT, and yTUSD. These tokens autonomously seek out the highest single-asset ROI from Aave, Compound, and dydx.

### Tier 2: Y Curve Pool

At the next level up, yDAI, yUSDC, yUSDT, and yTUSD provide liquidity in the Curve and Yearn partnership pool (curve.fi/y). yCRV—the [LP token](https://docs.yearn.finance/defi-glossary#liquidity-providers) for this pool—grows in value from fees charged on stablecoin swaps within the pool. It also generates (soon-to-be-boosted) CRV rewards which are harvested in the next tier up.

### Tier 3: Sustainable Yield

At the highest level, yUSD accesses community-developed yield strategies to take advantage of emergent opportunities in the DeFi space. These strategies build on top of the lower tier legos and function autonomously to make earning high yield safe and simple. Created by developers who are rewarded for their efforts, these strategies are assessed and voted on before being incorporated into the Yearn system.

At this tier the current strategy sits on top of the lower two tiers and harvests CRV rewards to recycle them back into yCRV—increasing the vault's base asset and the value of yUSD.

## Why yUSD?

Instead of having stablecoins languishing in your wallet, holding yUSD automatically earns you the best risk-adjusted yield without you having to do anything. Your yUSD is not only earning the best yield available on lending platforms, it also accrues trading fees from users who swap from one stablecoin to another on Curve, and benefits from automatic reward harvesting.

It's DeFi made simple.

## Resources

- yUSD
  - CoinGecko: https://www.coingecko.com/en/coins/yusd
  - yUSD Token contract: [0x5dbcF33D8c2E976c6b560249878e6F1491Bca25c](https://etherscan.io/address/0x5dbcF33D8c2E976c6b560249878e6F1491Bca25c)
- Code
  - The vaults.finance source code on [github](https://github.com/banteg/yearn-recycle)
  - The current strategy: [StrategyCurveYCRVVoter](https://etherscan.io/address/0xc999fb87AcA383A63D804A575396F65A55aa5aC8#code)
- FAQ
  - https://docs.yearn.finance/faq#vaults
