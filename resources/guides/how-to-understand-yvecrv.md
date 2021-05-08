# How to Understand yveCRV

On February 6th 2021 Yearn Finance launched its latest product, yveCRV.

## Why is it called yveCRV?

yveCRV stands for veCRV-DAO yVault and is [listed on CoinGecko](https://www.coingecko.com/en/coins/vecrv-dao-yvault).

### List of tokens

* **CRV** - Curve DAO Token
* **veCRV** - voting escrow CRV tokens \(the longer it’s locked up for, the greater the rewards\), you can read more about CRV vote locking [here](how-to-understand-crv-vote-locking.md).
* **yveCRV** - the “y” prefix is used for all of Yearn’s vaults

## How do I participate?

Deposit CRV into the yveCRV vault: [https://yearn.finance/vaults](https://yearn.finance/vaults)

As with all vaults, if you are depositing for the first time two transactions are required. First you need to approve the transaction. This allows CRV to be deposited into Yearn vaults. And then you decide how much CRV you would like to deposit. Pleas refer to the [general guide](how-to-participate-in-a-yvault.md) for more information.

Alternatively, you can buy yveCRV directly on [Sushiswap](https://app.sushiswap.fi/swap). The contract address is [0xc5bddf9843308380375a611c18b50fb9341f502a](https://etherscan.io/address/0xc5bddf9843308380375a611c18b50fb9341f502a).

## What are the benefits of depositing into this vault?

Depositing CRV in this vault allows you to earn:

* Trading fees from Curve Finance
* Additional CRV rewards
* A boost to your CRV rewards that you cannot get elsewhere

Rewards are shown here: [https://crv.ape.tax/](https://crv.ape.tax/)

## How is this vault different from the other vaults?

Other vaults increase your holding in the token that you deposit. For example, the yETH vault increases your ETH holdings.

The yveCRV vault pays weekly rewards in LP 3pool Curve \(3CRV\). 3CRV is a combination of DAI+USDT+USDC. Please refer to [Curve's website](https://www.curve.fi/3pool) for current weights. DAI, USDT and USDC are USD stablecoins therefore 3CRV is expected to maintain a price close to $1.

The other key difference is that **deposited CRV is locked forever**. It **cannot be withdrawn**, as the vault perpetually re-locks CRV upon their expiration. Instead you earn a stream of 3CRV rewards for as long as people continue to trade on the Curve Finance protocol.

## Where do the rewards come from?

yveCRV earns rewards from trading fees, CRV rewards and “boosties”. Holding CRV in your wallet gives you exposure to the price of CRV. You want the price of Crv to increase. Depositing CRV on Curve Finance means that you receive a share of the trading fees on Curve Finance.

Curve Finance introduced extra rewards, called “boosties”, if the CRV is locked in Curve Finance for a minimum of 1 week and a maximum of 4 years. Please refer to the [CRV vote locking guide](how-to-understand-crv-vote-locking.md) for more information.

Rewards are paid weekly.

## What if I don’t claim my weekly rewards?

They continue to accrue so don’t worry if you forget or don’t want to pay gas fees every week.

## What are the risks?

* You have to determine the risks for yourself.
* You are exposed to smart contract risk from Yearn vaults and Curve Finance.
* Any losses that occur due to the Curve Finance protocol can be mitigated by [purchasing Cover](https://yearn.finance/cover).
* yveCRV earns trading fees from trading that occurs on Curve Finance. If trading fees are lower than expected then your returns will be lower than expected. Trading volume data on Curve Finance is available from [Coingecko](https://www.coingecko.com/en/exchanges/curve#statistics).

## Is it true that I can earn even more rewards from Sushi and Pickle?

With yveCRV you’re already earning the highest return on your CRV.

However, we’re making the most of Yearn’s ecosystem by partnering with Sushiswap and Pickle to give you even more rewards.

### How can I earn extra Sushi rewards?

You can provide [yveCrv/ETH liquidity on Sushiswap](https://app.sushiswap.fi/token/0xc5bddf9843308380375a611c18b50fb9341f502a) to earn extra rewards. Note that if you earn Sushi rewards you will not be able to claim the 3Pool rewards as well. By providing yveCRV-WETH liquidity to Sushiswap, you may be exposed to [impermanent loss](https://medium.datadriveninvestor.com/impermanent-loss-in-defi-the-risks-involved-in-providing-liquidity-67c54fdf1cfc).

### What are the latest Sushi rewards?

Search for “yveCRV” on [Sushiswap analytics](https://analytics.sushiswap.fi/) to find the latest rewards. [WETH-yveCRV-DAO pool data](https://analytics.sushiswap.fi/pools/132) is also available. As the WETH-yveCRV LP grows in size, Sushi rewards per LP units held will decrease. Sushi rewards are determined by governance.

### How can I earn extra Pickle rewards?

Deposit your Sushiswap LP into the [Pickle jar](https://app.pickle.finance/jars).

## How can I stay up-to-date with vaults?

Subscribe to Yearn’s weekly [state of the vaults](https://medium.com/yearn-state-of-the-vaults) newsletter.

## Still have questions?

Please visit [Telegram or discord](https://github.com/philburrrt/yearn-docs/tree/6343b74028de10da3ff16079f4a3f0b115e34312/resources/README.md#communication_channels) and ask away!

