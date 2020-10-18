# How to understand CRV vote locking

This is an overview of how CRV vote locking works on Curve Finance, and how Yearn investment strategies takes advantage of this in order to increase yield.

## CRV vote locking

Vote locking, "Boosties", or "Vote boosting" is a Curve Finance feature where CRV is locked into the Curve DAO.

Vote locking CRV rewards yields **veCRV** (voting escrow CRV tokens). The longer time period that CRV is locked for, the more veCRVs are received. The minimum locking period is 1 week and the maximum period is 4 years.

veCRV enables its holders to:

- participate in Curve governance;
- **earn trading fees**; and
- **boost rewards** from liquidity provided.

### Trading fees

50% of all Curve trading fees from September 19 2020 and onwards will be distributed to veCRV holders, in the form of CRV tokens.

### Reward boosting

Vote locking CRV into veCRV allows boosting of rewards earned by providing liquidity to any Curve pool, up to a maximum of **2.5x** the reward amount.

The actual boost multiplier is determined by a formula that depends on the current pool gauge liquidity as a fraction out of the total amount of liquidity provided, and the fraction of voting power that the veCRV constitutes out of the total.

See the [Curve Guide](https://guides.curve.fi/how-to-boost-your-crv-rewards-by-vote-locking/) for more details on the formula and its calculation.

## CRV Vote Locking in Yearn

Yearn deploys a single CRV vote locking strategy that is shared across its general Curve strategies:

- [StrategyCurveYBUSDVoterProxy](https://etherscan.io/address/0x112570655b32a8c747845e0215ad139661e66e7f#code)
- [StrategyCurveBTCVoterProxy](https://etherscan.io/address/0x6d6c1ad13a5000148aa087e7cbfb53d402c81341#code)
- [StrategyCurveYVoterProxy](https://etherscan.io/address/0x07db4b9b3951094b9e278d336adf46a036295de7#code)
- [StrategyCurve3CrvVoterProxy](https://etherscan.io/address/0xC59601F0CC49baa266891b7fc63d2D5FE097A79D#code)

### Locking CRV for veCRV

**10% of all CRV earned** by the strategies are **locked up for 4 years** in the Curve DAO in order to get the maximum reward ratio of 1:1 CRV:veCRV.

Actual veCRV distribution has not yet begun, with a date for this still to be announced by Curve Finance.

### Earning Trading fees

Based on Yearn's share of the total veCRV, 50% of trading fees will be claimed as CRV, out of which 10% will in turn be locked into the Curve DAO for more veCRV.

### Bosting liquidity rewards

Actual boost provided by Curve vote locking will be determined by a formula as [described above](#Reward-boosting), but will crucially be depending on the total amount of liquidity provided in Curve pools by Yearn and its relative voting power, i.e. its share of the current total of veCRV issued.

A "Yearn boost" tool displaying Yearn's current active and potential boost is in development and will be released once available.

## More information

- Use CRV: https://www.curve.fi/usecrv
- Curve Guide for staking CRV: https://resources.curve.fi/guides/staking-your-crv
- Curve Guide for vote locking: https://guides.curve.fi/how-to-boost-your-crv-rewards-by-vote-locking/
- Curve FAQ: https://resources.curve.fi/faq/vote-locking-boost
- deFinn Infographic on CRV Voting Boost and formula: https://drive.google.com/uc?export=download&id=1DvytXXS0WXmJ65X4jg8vfuT-zWXFxxSk
- Boost calculator: https://dao.curve.fi/minter/calc
- Yearn CurveDAO proxy strategy diagram: https://twitter.com/bantg/status/1308680661801340929
