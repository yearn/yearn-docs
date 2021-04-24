# How to understand the Hegic v2 vault

## Why do we need a Hegic vault?

To earn options trading fees from the Hegic protocol you need to hold a staking lot. A staking lot requires 888,000 Hegic, so the price of a staking lot varies with the price of Hegic. In early March the Hegic price was around $0.30 which meant a staking lot cost over $250k.

Most people do not hold enough Hegic for a staking lot and so the vault allows them to pool their Hegic together to earn options trading fees from the Hegic protocol.

## How do I participate?

Deposit Hegic into the yHegic vault [here](https://yearn.finance/vaults).

As with all vaults, if you are depositing for the first time two transactions are required. First you need to approve the transaction. This allows Hegic to be deposited into Yearn vaults. And then you decide how much Hegic you would like to deposit. Click [here](https://docs.yearn.finance/how-to-guides/how-to-participate-in-a-yvault) for a general guide.

The Hegic token contract address is [here](https://etherscan.io/address/0x584bc13c7d411c00c01a62e8019472de68768430).

And the contract of the vault is here [here](https://etherscan.io/address/0xe11ba472f74869176652c35d30db89854b5ae84d).

## What are the benefits of depositing into this vault?

Depositing Hegic into this vault allows you to earn:

- Options trading fees from the Hegic protocol
- Lending rewards on Cream Finance

## How is this vault different from the other vaults?

The Hegic vault is similar to other vaults in that it increases your holding of Hegic.

Hegic is an options protocol and the token enables you to earn options trading fees. However, there’s one important difference with Hegic. You need to acquire a staking lot for 888,000 Hegic before you can start earning options trading fees.

Hegic pays rewards in WBTC or ETH depending on whether the staking lot is for WBTC or ETH options. The Hegic vault then sells these rewards for Hegic on Sushiswap so that your holding of Hegic increases.

The vault strategist decides the assignment of the strategies based on market conditions. The change is sent to the strategist multi-sig where other strategists review the change and execute the transaction.

For example, in early March 2021, Hegic's ETH pool did not have enough liquidity and so ETH lot holders would not have got any profit. To mitigate the lack of liquidity in the ETH pool at the time, the yvHegic vault had more WBTC lots than ETH lots.

## Where do the rewards come from?

yHegic earns rewards from options trading fees on the Hegic protocol and/or from lending on Cream.

Depositing Hegic into the Hegic vault means that you receive a share of the options trading fees on the Hegic protocol.

Data on Hegic staking lots and rewards can be found [here](https://duneanalytics.com/slash125/hegic-v2).

## Simplified diagram

![](https://i.imgur.com/AmXlSjZ.png)

## More detailed diagram

![](https://i.imgur.com/WrqQuYW.png)

![](https://i.imgur.com/brmJp9t.png)

## Can I read the code?

Yes, [here](https://etherscan.io/address/0x0Ce77bc655aFaAc83947c2e859819185966Ca825#code).

## What are the fees charged by Yearn?

Yearn charges a 2% annual management fee on all v2 vaults and a 20% performance fee. More information on the fee structure may be found [here](https://docs.yearn.finance/faq#what-are-the-fees).

## What are the fees charged by Ethereum?

Ethereum charges gas fees for each transaction. There are three transaction fees that the user will have to pay directly:

- Approving Yearn to spend the Hegic token from your wallet
- Depositing the Hegic tokens
- Withdrawing the Hegic tokens from the vault

Gas fees on Ethereum have historically been volatile, as shown [here](https://bitinfocharts.com/comparison/ethereum-transactionfees.html), so you need to deposit enough such that the returns will sufficiently cover the cost of your transactions. The gas fees will be smaller as a proportion of your returns if you deposit more or do not withdraw from the vault for a longer period of time.

## What are the risks that could lead to loss of funds?

You have to determine the risks for yourself.

All assets and protocols on Ethereum are exposed to something going wrong with Ethereum.

You are exposed to the risk of loss of funds from smart contract risk from Yearn vaults and the Hegic Protocol.

Any losses that occur due to the Hegic protocol can be covered [here](https://yearn.finance/cover).

## What affects the yield?

Hegic earns options trading fees from trading that occurs on the Hegic protocol. If options trading fees are lower than expected then your returns will be lower.

| No. | Dependency                                                                                                    | Directional Impact                                                                                                                                  |
| :-: | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
|  1  | The rewards from a Hegic staking lot and the Hegic [lending rate on Cream](https://app.cream.finance/markets) | The higher the rewards on Hegic or Cream, the greater the return                                                                                    |
|  2  | The remainder when the number of Hegic tokens in the vault are divided by 888,000                             | Assuming the rewards from a Hegic staking lot are greater than the lending rewards on Cream then the smaller the remainder, the greater the rewards |
|  3  | wBTC options volume on Hegic                                                                                  | More [volume](https://duneanalytics.com/slash125/hegic-v2) means a higher yield                                                                     |
|  4  | Price of wBTC relative to Hegic                                                                               | The higher the [price of wBTC relative to Hegic](https://www.coingecko.com/en/coins/hegic), the more Hegic can be bought with the wBTC rewards      |
|  5  | Slippage on Sushiswap                                                                                         | The lower the slippage the greater the amount of Hegic received, therefore the greater the return                                                   |
|  6  | Ethereum gas fees                                                                                             | The lower the [gas fees](https://bitinfocharts.com/comparison/ethereum-transactionfees.html), the greater the return                                |

## Which protocols are used by the strategy?

| No. | Protocol name                              | Type                                      | Use in Strategy                                               |
| :-: | ------------------------------------------ | ----------------------------------------- | ------------------------------------------------------------- |
|  1  | [Hegic](https://www.hegic.co/)             | wBTC or ETH call and put options protocol | Staking Hegic to earn rewards                                 |
|  2  | [Sushiswap](https://sushi.com/)            | Automated Market Maker                    | Swap ETH or wBTC for Hegic                                    |
|  3  | [Cream](https://app.cream.finance/markets) | Lending protocol                          | Lending the Hegic that is not used in a staking lot, on Cream |

## Which assets are used by the strategy?

| No. |                         Asset name                         | Type                                           | Use in Strategy                                                 |
| :-: | :--------------------------------------------------------: | ---------------------------------------------- | --------------------------------------------------------------- |
|  1  |     [Hegic](https://www.coingecko.com/en/coins/hegic)      | Governance token of the Hegic protocol         | Earned by the Hegic vault                                       |
|  2  | [wBTC](https://www.coingecko.com/en/coins/wrapped-bitcoin) | Wrapped bitcoin on Ethereum (ann ERC-20 token) | Earned from wBTC options trading, swapped to Hegic on Sushiswap |
|  3  |     [ETH](https://www.coingecko.com/en/coins/ethereum)     | ETH the asset                                  | Earned from ETH options trading, swapped to Hegic on Sushiswap  |

## How can I stay up-to-date with vaults?

Subscribe to Yearn’s weekly [state of the vaults](https://medium.com/yearn-state-of-the-vaults) newsletter.

## Still have questions?

Please visit [Telegram or discord](../README.md#communication_channels) and ask away!
