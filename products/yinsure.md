# yInsure

[yInsure](https://yinsure.finance/), also referred to as **Cover**, is a smart contract cover underwritten by [Nexus Mutual](https://nexusmutual.io/). It is decentralised and there is no KYC required to obtain cover. It consists of three components:

- **Cover Vaults** hold assets that are used to provide payment in the event of a claim;
- **Covered Vaults** hold assets that the "cover holder" desires to be covered, and;
- **Claim Governance** which represents the claim arbitration process

The system consists of many market participants, including:

- **Cover providers:** Deposits funds into the Cover Vaults
- **Cover holders:** Pays premiums in order to obtain cover for their Covered Vaults
- **Claimants:** Cover holders who have an approved claim and are entitled to payment

While smart contract cover can provide some protection against smart contract risks, it is **not** insurance.

## Cover Vaults

Contains the assets used in the capital pool, which can provide payment in the event of a claim. The Cover Vaults works as follows:

- Cover providers deposit USDC to the vault, and in return receive yiUSDC.
- yiUSDC represents cover provider's original deposit and ultimately the cover capital pool.
- Cover providers receive initiation fees and weekly premiums paid by the cover holder.
- If a claim is approved, USDC will be paid out of the cover vault to the cover holder \(claimant\).

## Covered Vaults

Contains the assets that cover holders desire to obtain insurance on. The Covered Vaults work as follows:

- If a cover holder wishes to obtain cover on USDT, he/she would deposit USDT to the Covered Vault, and in return receive yiUSDT.
- yiUSDT represents the cover holder's deposit and can be withdrawn at any time.
- The covered sum is the value of the asset in dollars at deposit. The cover holder is charged a 0.1% initiation fee at deposit and ongoing 0.1% weekly fees.

The intention is that [yVaults](https://yearn.finance/vaults) \(such as yUSD\) can be Covered Vaults.

## Claim Governance

Represents the claim arbitration process. This process works as follows:

- Cover holders submit claims by staking the asset they received during deposit \(yiUSDT\).
- Cover providers vote with the assets they received during deposit \(i.e., yiUSDC\) on whether the claim is valid or not.
- If a claim is approved, the cover holder receives the USDC and the cover provider receives the yiUSDT from the cover holder.
- The voting period is three days, requires 33% approvals to pass, and can be vetoed with 25% of the voting power.
- Any tokenized ERC-20 token can be covered. Base assets \(LINK, ETH, etc.\) or composite assets such as aLINK or yaLINK can also be covered.
- If cover providers deny valid claims, cover holders will no longer use the system and ultimately make it unprofitable for cover providers.

{% hint style="info" %}

### **A Common Misconception: Not Insurance** <a id="9521"></a>

The smart contract cover underwritten by Nexus Mutual is not a contract of insurance. It is a discretionary cover provided by members of the mutual to each other. Members have full discretion on which claims payments are made. Members are putting trust in the economic incentive model rather than an insurance company. Learn more on [Understanding Nexus Mutual](https://medium.com/nexus-mutual/understanding-nexus-mutual-bb2946dad919).
{% endhint %}

## Resources

- [yInsure Homepage](http://yinsure.finance/)
- Medium article: [yinsure.finance a new insurance primitive](https://medium.com/iearn/yinsure-finance-a-new-insurance-primitive-77d5d4217896)
