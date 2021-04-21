# v2 yVault Descriptions

v2 yVaults are able to employ multiple strategies per vault \(up to 20 strategies simultaneously\), unlike v1 yVaults that are only able to employ one strategy per vault.

![](https://miro.medium.com/max/256/0*aKL4yfJzNvYxRsET.png)

### v2 YFI yVault \([yvYFI](https://etherscan.io/address/0xE14d13d8B3b85aF791b2AADD661cDBd5E6097Db1#readContract)\) <a id="8459"></a>

[StrategyLenderYieldOptimiser](https://etherscan.io/address/0x6a97FC93e39b3f792f1fD6e01565ff412B002D20#code)  
This strategy lends YFI tokens on various lending platforms such as CREAM and AAVE to gain yield.

[StrategyMakerYFIDAIDelegate](https://etherscan.io/address/0xd7c172cBB4BeE22511611e92377b0fB375bbFd43)  
This strategy uses YFI to mint DAI at MakerDAO. This newly minted DAI is then deposited into the v2 DAI yVault.

![](https://miro.medium.com/max/256/0*XC-ncn6fhvFtjQFr.png)

### v2 1INCH yVault \([yv1INCH](https://etherscan.io/address/0xB8C3B7A2A618C552C23B1E4701109a9E756Bab67)\) <a id="d40d"></a>

[StrategyLenderYieldOptimiser](https://etherscan.io/address/0x86eD4F77d40182b8686a25e125FB3f5a04203CaA)  
Lends 1INCH tokens on C.R.E.A.M. to gain interest.

[Strategy1INCHGovernance](https://etherscan.io/address/0xB12F6A5776EDd2e923fD1Ce93041B2000A22dDc7)  
Stakes 1INCH token on 1INCH DAO to collect governance rewards. Rewards are harvested and deposited back into the vault.

![](https://miro.medium.com/max/256/0*06LkNSiZlajnt89Y.png)

### v2 WETH yVault \([yvWETH](https://etherscan.io/address/0xa9fE4601811213c340e850ea305481afF02f5b28)\) <a id="05fc"></a>

_V2 ETH vVault is wrapping the deposited ETH and depositing here._

[StrategyLenderYieldOptimiser](https://etherscan.io/address/0xeE697232DF2226c9fB3F02a57062c4208f287851)  
Lends WETH \(ETH\) on Alpha Homora to gain interest. However, if yields are better elsewhere these funds will be shifted there.

[StrategysteCurveWETHSingleSided](https://etherscan.io/address/0xeE697232DF2226c9fB3F02a57062c4208f287851)  
Supplies WETH to the liquidity pool on Curve [here](https://www.curve.fi/steth/deposit) to obtain [steCRV](https://etherscan.io/address/0x06325440D014e39736583c165C2963BA99fAf14E) tokens which it then puts into the v2 Curve stETH Pool yVault \([yvsteCRV](https://etherscan.io/address/0xdcd90c7f6324cfa40d7169ef80b12031770b4325)\) to gain yield.

[StrategyIdleWETHYield](https://etherscan.io/address/0x030bFfF524BbE7A77C789A0993cE8EF23cF8Efe9)  
Supplies WETH on Idle Finance to farm COMP and IDLE. Rewards are harvested, sold for more WETH, and deposited back to the vault.

[StrategyMakerETHDAIDelegate](https://etherscan.io/address/0x0E5397B8547C128Ee20958286436b7BC3f9faAa4)  
This strategy uses ETH to mint DAI at MakerDAO. This newly minted DAI is then deposited into the v2 DAI yVault.

![](https://miro.medium.com/max/256/0*XidpVOAUpe71JTb3.png)

### v2 USDC yVault \([yvUSDC](https://etherscan.io/address/0x5f18c75abdae578b483e5f43f12a39cf75b973a9)\) <a id="e713"></a>

[StrategyGenericLevCompFarm](https://etherscan.io/address/0x4d7d4485fd600c61d840ccbec328bfd76a050f87)   
Supplies USDC on Compound and borrows an additional amount of USDC to maximize COMP farming. Flashloans are used to obtain additional USDC from dYdX in order to gain additional leverage and boost the APY. Earned COMP is harvested and sold for more USDC and re-deposited into the vault.

[StrategyAH2EarncyUSDC](https://etherscan.io/address/0x86Aa49bf28d03B1A4aBEb83872cFC13c89eB4beD#code)  
Lends USDC on Alpha Homora v2 to generate interest. Users of Alpha Homora borrow USDC to perform leveraged yield-farming on Alpha Homora’s platform.

[StrategyIdleUSDCYield](https://etherscan.io/address/0x414D8F5c21dAF33105eE6416bcdA99a50A47C0e5#code)   
Supplies USDC on Idle.finance to farm COMP and IDLE. Rewards are harvested, sold for more USDC, and re-deposited into the vault.

[IBLevComp](https://etherscan.io/address/0xE68A8565B4F837BDa10e2e917BFAaa562e1cD143)  
Supplies USDC on Compound and borrows an additional amount of USDC from Ironbank to maximize COMP farming. Earned COMP is harvested, sold for more USDC, and re-deposited into the vault.

[SingleSidedCrvUSDC](https://etherscan.io/address/0x80af28cb1e44C44662F144475d7667C9C0aaB3C3)  
Deposits USDC to a USDC curve pool on [curve.fi](http://curve.fi/), and switches to the most profitable curve pool.

![](https://miro.medium.com/max/256/0*KnYZJ6Zkf4XPwFvc.png)

### v2 HEGIC yVault \([yvHEGIC](https://etherscan.io/address/0xe11ba472f74869176652c35d30db89854b5ae84d)\) <a id="eb1c"></a>

[StrategyHegicETH](https://etherscan.io/address/0x41d638024c525c70a53b883608048e705e061f2c), [StrategyHegicWBTC](https://etherscan.io/address/0x0ce77bc655afaac83947c2e859819185966ca825), [StrategyLenderYieldOptimiser](https://etherscan.io/address/0x0cf55d57d241161e0ec68e72cbb175dbfe84173a)   
These three strategies work together to alternatively use HEGIC to buy ETH or WBTC lots on [HEGIC.co](https://www.hegic.co/). While the vault is building up the required 888,000 HEGIC needed to buy a lot, it lends it out on C.R.E.A.M to earn interest. The vault also keeps a buffer of HEGIC in reserve for withdrawals earning interest in CREAM.

![](https://miro.medium.com/max/256/0*sUO1Z1qMsbLL0IQh.png)

### v2 DAI yVault \([yvDAI](https://etherscan.io/address/0x19d3364a399d251e894ac732651be8b0e4e85001)\) <a id="05d8"></a>

[StrategyLenderYieldOptimiser](https://etherscan.io/address/0x32b8C26d0439e1959CEa6262CBabC12320b384c4)  
Splits lending DAI between dYdX and cream.finance to gain interest. The proportions are adjusted each time the strategy calls harvest.

[StrategyGenericLevCompFarm](https://etherscan.io/address/0x4031afd3b0f71bace9181e554a9e680ee4abe7df)   
Supplies DAI on Compound and borrows an additional amount of DAI via a flashloan from dYdX to maximize COMP farming. Earned COMP is harvested and sold for more DAI then re-deposited into the vault.

[StrategyAH2EarncyDAI](https://etherscan.io/address/0x7D960F3313f3cB1BBB6BF67419d303597F3E2Fa8)  
Lends DAI on Alpha Homora v2 to generate interest. Users of Alpha Homora borrow DAI to perform leveraged yield-farming on Alpha’s platform.

[IBLevComp](https://etherscan.io/address/0x80af28cb1e44C44662F144475d7667C9C0aaB3C3)  
Supplies DAI on Compound and opens a long-term debt for an additional amount of DAI from Ironbank without the need for collateral, to maximize COMP farming. Earned COMP is harvested and sold for more DAI and re-deposited into the vault.

[StrategyIdleDAIYield](https://etherscan.io/address/0x9b8F90078E74AcaD449798554f1bE3F4157C932D)  
Supplies DAI to idle.finance to farm COMP and IDLE. Rewards are harvested, sold for more DAI, and deposited back to the vault.

[SingleSidedCrvDAI](https://etherscan.io/address/0x6a6B94A78cBA0F55BC4D41b37f2229427800B4dA)  
Deposits DAI to a DAI Curve Pool on [curve.fi](http://curve.fi/) and switches to the most profitable curve pool.

[PoolTogetherDaiStablecoin](https://etherscan.io/address/0x57e848A6915455a7e77CF0D55A1474bEFd9C374d)  
Supplies DAI to the [PoolTogether](https://pooltogether.com/) protocol to farm POOL. Rewards are harvested, sold for more DAI, and deposited back into the vault. If it gets the prize of the week it will also be added to the vault.

![](https://miro.medium.com/max/256/0*6islP1Hf0SmBgZjz.png)

### v2 WBTC yVault \([yvWBTC](https://etherscan.io/address/0xcb550a6d4c8e3517a939bc79d0c7093eb7cf56b5)\) <a id="9cf8"></a>

[StrategyIdleWBTCYield](https://etherscan.io/address/0x3E14d864E4e82eD98849Bf666971f39Cf49Ca986)   
Supply WBTC on idle.finance to earn COMP and IDLE. Rewards are harvested, sold for more WBTC, and deposited into the vault.

![](https://miro.medium.com/max/256/0*deZOAl4GIy6AlD-t.png)

### v2 Curve Iron Bank yVault \([yvCurve-IB](https://etherscan.io/address/0x27b7b1ad7288079A66d12350c828D3C00A6F07d7)\) <a id="b969"></a>

[StrategyCurveIBVoterProxy](https://etherscan.io/address/0x5148C3124B42e73CA4e15EEd1B304DB59E0F2AF7) 🚀  
This vault accepts deposits of [ib3CRV](https://etherscan.io/address/0x5282a4eF67D9C33135340fB3289cc1711c13638C) tokens obtained by supplying either cyDAI, cyUSDC, or cyUSDT to the liquidity pool on Curve [here](https://www.curve.fi/ib/deposit) in exchange for ib3CRV tokens. ib3CRV are staked in the gauge on Curve.finance to earn CRV rewards. Rewards are swapped for one of the underlying assets and resupplied to the liquidity pool to obtain more ib3CRV.

![](https://miro.medium.com/max/256/0*nYrBo4K97YtFsU5T.png)

### v2 Curve sETH Pool yvault \([yveCRV](https://etherscan.io/address/0x986b4AFF588a109c09B50A03f42E4110E29D353F)\) <a id="8368"></a>

[StrategyCurveEcrvVoterProxy](https://etherscan.io/address/0xB5F6747147990c4ddCeBbd0d4ef25461a967D079#code) 🚀   
This vault accepts deposits of [eCRV](https://etherscan.io/address/0xA3D87FffcE63B53E0d54fAa1cc983B7eB0b74A9c) tokens obtained by supplying either ETH or sETH to the liquidity pool on Curve [here](https://www.curve.fi/seth/deposit). eCRV tokens are staked in the gauge on Curve to earn CRV rewards. Rewards are swapped for one of the underlying assets and resupplied to the liquidity pool to obtain more eCRV.

![](https://miro.medium.com/max/256/0*f_UoMEtMRrsmdgNg.png)

### v2 Curve stETH Pool yVault \([yvsteCRV](https://etherscan.io/address/0xdcd90c7f6324cfa40d7169ef80b12031770b4325)\) <a id="d70c"></a>

[StrategystETHCurve](https://etherscan.io/address/0xebfc9451d19e8dbf36aaf547855b4dc789ca793c) 🚀   
This vault accepts deposits of [steCRV](https://etherscan.io/address/0x06325440D014e39736583c165C2963BA99fAf14E) tokens obtained by supplying either ETH or stETH to the liquidity pool on Curve [here](https://www.curve.fi/steth/deposit). steCRV are staked in the gauge on curve.finance to earn CRV and [LDO](https://www.coingecko.com/en/coins/lido-dao) rewards. Rewards are swapped for WETH and resupplied to the liquidity pool to obtain more steCRV.

![](https://miro.medium.com/max/256/0*5lXzxMsjn3OcilZl.png)

### v2 Curve sBTC Pool yVault \([yvCurve-sBTC](https://etherscan.io/address/0x8414Db07a7F743dEbaFb402070AB01a4E0d2E45e)\) <a id="4a22"></a>

[CurvecrvRenWSBTCVoterProxy](https://etherscan.io/address/0xdD92491B9F55620C043d55D25620a7B126451ddD) 🚀  
This vault accepts deposits of [sbtcCrv](https://etherscan.io/address/0x075b1bb99792c9E1041bA13afEf80C91a1e70fB3) tokens obtained by supplying either renBTC, wBTC or sBTC to the liquidity pool on Curve [here](https://www.curve.fi/sbtc/deposit). sbtcCrv tokens are staked in the gauge on Curve to earn CRV rewards. Rewards are swapped for one of the underlying assets and resupplied to the liquidity pool to obtain more sbtcCrv.

