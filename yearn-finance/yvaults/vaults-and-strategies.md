# Vault and Strategy Contract Links

When you deposit, your funds first go to the vault contract and then are deployed to various strategy contracts.

Guardians and strategists monitor deposits in order ensure the optimal returns and to be available during critical situations. 

## Single Asset Vaults

| Vault Name                | Vault Contract | Strategy Contract          |
|---------------------------|----------------|----------------------------|
|YFI|[YFI yVault](https://etherscan.io/address/0xE14d13d8B3b85aF791b2AADD661cDBd5E6097Db1)|[StrategyLenderYieldOptimiser](https://etherscan.io/address/0x6a97FC93e39b3f792f1fD6e01565ff412B002D20#code), [StrategyMakerYFIDAIDelegate](https://etherscan.io/address/0xd7c172cBB4BeE22511611e92377b0fB375bbFd43)|
|1INCH|[1INCH yVault](https://etherscan.io/address/0xB8C3B7A2A618C552C23B1E4701109a9E756Bab67)|[StrategyLenderYieldOptimiser](https://etherscan.io/address/0x86eD4F77d40182b8686a25e125FB3f5a04203CaA), [Strategy1INCHGovernance](0xB12F6A5776EDd2e923fD1Ce93041B2000A22dDc7)|
|WETH|[WETH yVault](https://etherscan.io/address/0xa9fE4601811213c340e850ea305481afF02f5b28)|[StrategyCurveWETHSingleSided](https://etherscan.io/address/0xda988eBb26F505246C59Ba26514340B634F9a7a2), [StrategyLenderYieldOptimizer](https://etherscan.io/address/0xeE697232DF2226c9fB3F02a57062c4208f287851), [StrategysteCurveWETHSingleSided](https://etherscan.io/address/0xeE697232DF2226c9fB3F02a57062c4208f287851), [StrategyIdleWETHYield](https://etherscan.io/address/0x030bFfF524BbE7A77C789A0993cE8EF23cF8Efe9), [StrategyMakerETHDAIDelegate](https://etherscan.io/address/0x0E5397B8547C128Ee20958286436b7BC3f9faAa4)|
|USDC|[USDC yVault](https://etherscan.io/address/0x5f18c75abdae578b483e5f43f12a39cf75b973a9)|[PoolTogetherUSDCoin](https://etherscan.io/address/0x387fCa8d7e2e09655b4F49548607B55C0580fC63), [StrategyGenericLevCompFarm](https://etherscan.io/address/0x4d7d4485fd600c61d840ccbec328bfd76a050f87), [StrategyAH2EarncyUSDC](https://etherscan.io/address/0x86Aa49bf28d03B1A4aBEb83872cFC13c89eB4beD#code), [StrategyIdleUSDCYield](https://etherscan.io/address/0x414D8F5c21dAF33105eE6416bcdA99a50A47C0e5#code), [IBLevComp](https://etherscan.io/address/0xE68A8565B4F837BDa10e2e917BFAaa562e1cD143), [SingleSidedCrvUSDC](https://etherscan.io/address/0x80af28cb1e44C44662F144475d7667C9C0aaB3C3)|
|HEGIC|[HEGIC yVault](https://etherscan.io/address/0xe11ba472f74869176652c35d30db89854b5ae84d)|[StrategyHegicETH](https://etherscan.io/address/0x41d638024c525c70a53b883608048e705e061f2c), [StrategyHegicWBTC](https://etherscan.io/address/0x0ce77bc655afaac83947c2e859819185966ca825), [StrategyLenderYieldOptimiser](https://etherscan.io/address/0x0cf55d57d241161e0ec68e72cbb175dbfe84173a)|
|DAI|[DAI yVault](https://etherscan.io/address/0x19d3364a399d251e894ac732651be8b0e4e85001)|[StrategyLenderYieldOptimiser](https://etherscan.io/address/0x32b8C26d0439e1959CEa6262CBabC12320b384c4), [StrategyGenericLevCompFarm](https://etherscan.io/address/0x4031afd3b0f71bace9181e554a9e680ee4abe7df),[StrategyAH2EarncyDAI](https://etherscan.io/address/0x7D960F3313f3cB1BBB6BF67419d303597F3E2Fa8), [IBLevComp](https://etherscan.io/address/0x80af28cb1e44C44662F144475d7667C9C0aaB3C3), [StrategyIdleDAIYield](https://etherscan.io/address/0x9b8F90078E74AcaD449798554f1bE3F4157C932D), [SingleSidedCrvDAI](https://etherscan.io/address/0x6a6B94A78cBA0F55BC4D41b37f2229427800B4dA), [PoolTogetherDaiStablecoin](https://etherscan.io/address/0x57e848A6915455a7e77CF0D55A1474bEFd9C374d)|
|WBTC|[WBTC yVault](https://etherscan.io/address/0xcb550a6d4c8e3517a939bc79d0c7093eb7cf56b5)|[StrategyIdleWBTCYield](https://etherscan.io/address/0x3E14d864E4e82eD98849Bf666971f39Cf49Ca986)|
|USDT|[USDT yVault](https://etherscan.io/address/0x7Da96a3891Add058AdA2E826306D812C638D87a7)|[StrategyLenderYieldOptimizer](https://etherscan.io/address/0x2f87c5e8396F0C41b86aad4F3C8358aB21681952), [StrategyIdleUSDTYield](https://etherscan.io/address/0x01b54c320d6B3057377cbc71d953d1BBa84df44e), [StrategySidedCrvUSDT](https://etherscan.io/address/0x01b54c320d6B3057377cbc71d953d1BBa84df44e),|


## Liquidity Provider Token Vaults

| Vault                     | Contract       | Strategies                 |
|---------------------------|----------------|----------------------------|
|crvIB|[Curve Iron Bank Pool yVault](https://etherscan.io/address/0x27b7b1ad7288079A66d12350c828D3C00A6F07d7)|[StrategyCurveIBVoterProxy](https://etherscan.io/address/0x5148C3124B42e73CA4e15EEd1B304DB59E0F2AF7)|
|crvSETH|[Curve sETH Pool yVault](https://etherscan.io/address/0x986b4AFF588a109c09B50A03f42E4110E29D353F)|[StrategyCurveEcrvVoterProxy](https://etherscan.io/address/0xB5F6747147990c4ddCeBbd0d4ef25461a967D079#code)|
|crvstETH|[Curve stETH Pool yVault](https://etherscan.io/address/0xdcd90c7f6324cfa40d7169ef80b12031770b4325)|[StrategystETHCurve](https://etherscan.io/address/0xebfc9451d19e8dbf36aaf547855b4dc789ca793c)|
|crvSBTC|[Curve sBTC Pool yVault](https://etherscan.io/address/0x8414Db07a7F743dEbaFb402070AB01a4E0d2E45e)|[CurvecrvRenWSBTCVoterProxy](https://etherscan.io/address/0xdD92491B9F55620C043d55D25620a7B126451ddD)|
|crvRENBTC|[Curve renBTC Pool yVault](https://etherscan.io/address/0x7047F90229a057C13BF847C0744D646CFb6c9E1A)|[CurvecrvRenWBTCVoterProxy](https://etherscan.io/address/0x2A94A56fBEE72ACEC39ea0269c1356a8DFbC4765)|
|crvOBTC|[Curve oBTC Pool yVault](https://etherscan.io/address/0xe9Dc63083c464d6EDcCFf23444fF3CFc6886f6FB)|[CurveoBTC/sbtcCRVVoterProxy](https://etherscan.io/address/0x24579b82E06aBe25C8ffC4Ee6C2dB676e57F1a32)|
|crvPBTC|[Curve pBTC Pool yVault](https://etherscan.io/address/0x3c5DF3077BcF800640B5DAE8c91106575a4826E6)|[CurvepBTC/sbtcCRVVoterProxy](https://medium.com/yearn-state-of-the-vaults/the-vaults-at-yearn-9237905ffed3)|
|crvTBTC|[Curve tBTC Pool yVaut](https://etherscan.io/address/0x23D3D0f1c697247d5e0a9efB37d8b0ED0C464f7f)|[Curvetbtc/sbtcCrvVoterProxy](https://medium.com/yearn-state-of-the-vaults/the-vaults-at-yearn-9237905ffed3)|
|crvFRAX|[Curve FRAX Pool yVault](https://etherscan.io/address/0xB4AdA607B9d6b2c9Ee07A275e9616B84AC560139#code)|[CurveFRAX3CRV-fVoterProxy](https://etherscan.io/address/0xb622F17e1ba8C51b9BD760Fb37994a55b1e5CD85#code)|
|crvLUSD|[Curve LUSD Pool yVault](https://etherscan.io/address/0x5fA5B62c8AF877CB37031e0a3B2f34A78e3C56A6#code)|[CurveLUSD3CRv-fVoterProxy](https://etherscan.io/address/0x21e5a745d77430568C074569C06e6c765922626a#code)|
|crvSAAVE|[Curve sAave Pool yVault](https://etherscan.io/address/0xb4D1Be44BfF40ad6e506edf43156577a3f8672eC#code)|[CurvesaCRVVoterProxy](https://etherscan.io/address/0xE73817de3418bB44A4FeCeBa53Aa835333C550e7#code)|
|crvBBTC|[Curve BBTC Pool yVault](https://etherscan.io/address/0x8fA3A9ecd9EFb07A8CE90A6eb014CF3c0E3B32Ef)|[CurvebBTC/sbtcCRVVoterProxy](https://etherscan.io/address/0xABCBB67Ef2757bCCff074014658d9BD13f559632)|
|crvLINK|[yearn Curve.fi LINK/sLINK](https://etherscan.io/address/0x96Ea6AF74Af09522fCB4c28C269C26F59a31ced6)|[StrategyCurveLINKVoterProxy](https://etherscan.io/address/0x153Fe8894a76f14bC8c8B02Dd81eFBB6d24E909f)|
|crvUSDP|[yearn Curve.fi USDP/3Crv](https://etherscan.io/address/0x1B5eb1173D2Bf770e50F10410C9a96F7a8eB6e75)|[StrategyCurveUSDPVoterProxy](https://etherscan.io/address/0xDdf11AEB5Ce1E91CF19C7E2374B0F7A88803eF36)|
|crvANKR|[yearn Curve.fi ETH/aETH](https://etherscan.io/address/0xE625F5923303f1CE7A43ACFEFd11fd12f30DbcA4#code)|[StrategyCurveAnkrVoterProxy](https://etherscan.io/address/0xBdCeae91e10A80dbD7ad5e884c86EAe56b075Caa#code)|
|yCRV(yUSD)|[yearn Curve.fi yDAI/yUSDC/yUSDT/yTUSD](https://etherscan.io/address/0x5dbcf33d8c2e976c6b560249878e6f1491bca25c)|[StrategyCurveYVoterProxy](https://etherscan.io/address/0x07DB4B9b3951094B9E278D336aDf46a036295DE7#code)|
|crvMUSD|[yearn Curve.fi MUSD/3Crv](https://etherscan.io/address/0x0FCDAeDFb8A7DfDa2e9838564c5A1665d856AFDF#code)|[StrategyCurvemUSDVoterProxy](https://etherscan.io/address/0xBA0c07BBE9C22a1ee33FE988Ea3763f21D0909a0#code)|
|crvGUSD|[yearn Curve.fi GUSD/3Crv](https://etherscan.io/address/0xcC7E70A958917cCe67B4B87a8C30E6297451aE98#code)|[StrategyCurveGUSDVoterProxy](https://etherscan.io/address/0xD42eC70A590C6bc11e9995314fdbA45B4f74FABb#code)|
|crvDUSD|[yearn Curve.fi DUSD/3Crv](https://etherscan.io/address/0x8e6741b456a074F0Bc45B8b82A755d4aF7E965dF#code)|[StrategyCurveDUSDVoterProx](https://etherscan.io/address/0x33F3f002b8f812f3E087E9245921C8355E777231#code)|
|crvUSDN|[Curve.fi USDN/3Crv](https://etherscan.io/address/0x4f3E8F405CF5aFC05D68142F3783bDfE13811522)|[StrategyCurveUSDNVoterProxy](https://etherscan.io/address/0x406813fF2143d178d1Ebccd2357C20A424208912#code)|
|crvUSDT|[yearn Curve.fi UST/3Crv](https://etherscan.io/address/0xF6C9E9AF314982A4b38366f4AbfAa00595C5A6fC#code)|[StrategyCurveUSTVoterProxy](https://etherscan.io/address/0x3be2717DA725f43b7d6C598D8f76AeC43e231B99#code)
|crvHUSD|[yearn Curve.fi HUSD/3CRV](https://etherscan.io/address/0x39546945695DCb1c037C836925B355262f551f55#code)|[StrategyCurveHUSDVoterProxy](https://etherscan.io/address/0xb21C4d2f7b2F29109FF6243309647A01bEB9950a#code)|
|crvBUSD|[yearn Curve.fi yDAI/yUSDC/yUSDT/yBUSD](https://etherscan.io/address/0x2994529C0652D127b7842094103715ec5299bBed#code)|[StrategyCurveBUSDVoterProxy](https://etherscan.io/address/0x112570655b32A8c747845E0215ad139661e66E7F#code)|
|crvSUSD|[yearn Curve.fi DAI/USDC/USDT/sUSD](https://etherscan.io/address/0x5533ed0a3b83F70c3c4a1f69Ef5546D3D4713E44#code)|[StrategyCurvesUSDVoterProxy ](https://etherscan.io/address/0xd7F641697ca4e0e19F6C9cF84989ABc293D24f84#code)|
|3Crv|[yearn Curve.fi DAI/USDC/USDT](https://etherscan.io/address/0x9cA85572E6A3EbF24dEDd195623F188735A5179f#code)|[StrategyCurve3CrvVoterProxy](https://etherscan.io/address/0xC59601F0CC49baa266891b7fc63d2D5FE097A79D#code)|
|crvEURS|[yearn Curve.fi EURS/sEUR](https://etherscan.io/address/0x98B058b2CBacF5E99bC7012DF757ea7CFEbd35BC#code)|[StrategyCurveEURVoterProxy](https://etherscan.io/address/0x22422825e2dFf23f645b04A3f89190B69f174659#code)|
|crvHBTC|[yearn Curve.fi hBTC/wBTC](https://etherscan.io/token/0x46AFc2dfBd1ea0c0760CAD8262A5838e803A37e5)|[StrategyCurveHBTCVoterProxy](https://etherscan.io/address/0xE02363cB1e4E1B77a74fAf38F3Dbb7d0B70F26D7#code)|

## Locked Token Vaults

| Vault                     | Contract       | Strategies                 |
|---------------------------|----------------|----------------------------|
|yveCRV|[veCRV-DAO yVault](https://etherscan.io/address/0xc5bDdf9843308380375a611c18B50Fb9341f502A#code)||
|yvBOOST|[Yearn Compounding veCRV yVault](https://etherscan.io/address/0x9d409a0A012CFbA9B15F6D4B36Ac57A46966Ab9a)|[StrategyYearnVECRV](https://etherscan.io/address/0x683b5C88D48FcCfB3e778FF0fA954F84cA7Ce9DF)|



