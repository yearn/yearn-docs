---
description: In Development
---

# StableCredit

{% embed url="https://medium.com/iearn/introducing-stablecredit-a-new-protocol-for-decentralized-lending-stablecoins-and-amms-7252a43ee56" %}

## Explanations
1. Finematics explains the whole process in 30 secs: https://twitter.com/finematics/status/1305188626008100865
2. Andre joined the CODEUP 38 and explained himself the product: https://www.youtube.com/watch?v=bdC3rNDChbw&feature=youtu.be&t=2002
3. Economic Designs also took a shot at explaining it: https://twitter.com/lisajytan/status/1304584889237270528

## Other concepts

* Stablecredit uses single-sided [Automatic Market Makers](https://docs.yearn.finance/defi-glossary#automated-market-maker). Here is more info on how AMMs work: https://www.youtube.com/watch?v=842acSWmBC4&t=336s
* [Collateral](https://docs.yearn.finance/defi-glossary#collateralization), Multicollateral.
* MakerDAO and [MakerDAO CDPs](https://docs.yearn.finance/defi-glossary#maker) is a lending system which StableCredit builds on conceptually. It takes the basic concept, but StableCredit decentralizes it and evolves the concept.
* Utilization Ratio is the maximum amount of credit a user will get from their deposited amount.


## What the user gets
1. The user gets a Credit Line, by providing "almost any token". Currently any token available in the [CHAINLINK oracle (price feeds)](https://feeds.chain.link/)
1. The credit line is given to the user in a StableCredit token. This is a new token minted. This token is a stable token. The user can only get up to 75% from the total amount deposited into the StableCredit contract. This 75% is the utilization ratio.
