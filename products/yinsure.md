# yInsure

[yInsure](https://yinsure.finance/), also referred as **Cover**, is a non-KYC, pooled insurance coverage underwritten by [Nexus Mutual](https://nexusmutual.io/). It consists of three components: Insurer Vaults, Insured Vaults, and Claim Governance. Insurer Vaults hold the assets that are used to insure claimaints, the Insured Vault holds the assets claimants desire to be insured, and Claim Governance represent the insurance arbitration process.

## Insurer Vaults

Contains the assets used in the capital pool, which insure claimants. The Insurer Vaults works as follow:

* Insurance providers deposit USDC to the vault, and in return receive yiUSDC.
* yiUSDC represents insurers' original deposit and ultimately the insurance capital pool.
* Insurers receive initiaton fees and weekly premiums paid by insurees.
* If a claim is approved, USDC will be paid out of the insurer vault to the insuree \(claimant\).

## Insured Vaults

Contains the assets insurees desire to obtain insurance on. The Insured Vaults work as follows:

* If an insuree wishes to obtain insurance on USDT he or she would deposit USDT to the insured vault, and in return receive yiUSDT.
* yiUSDT represents the insurees deposit and can be withdrawn at any time.
* The insured sum is the value of the asset in dollars at deposit. The insuree is charged a 0.1% initiation fee at deposit and ongoing 0.1% weekly fees.

## Claim Governance

Represents the claim arbitration process. This process works as follows:

* Insurees submit claims by staking the asset they received during deposit \(yiUSDT\).
* Insurers vote with the assets they received during deposit \(i.e., yiUSDC\) on whether the claim is valid or not.
* If a claim is approved the insurees receive the USDC and the insurers receive the yiUSDT from the insurees.
* The voting period is three days, requires 33% approvals to pass, and can be vetoed with 25% of the voting power.
* Any tokenized ERC-20 token can be insured. Base assets \(LINK, ETH, etc. \) or composite asets such as aLINK or yaLINK can also be insured.
* If insurance providers deny valid claims insurees will no longer use the system and ultimately make it unprofitable for insurance providers.

## Resources

* [yInsure Homepage](http://yinsure.finance/)
* Medium article: [yinsure.finance a new insurance primitive](https://medium.com/iearn/yinsure-finance-a-new-insurance-primitive-77d5d4217896)

