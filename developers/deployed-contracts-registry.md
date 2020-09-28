# Deployed Contracts Registry

Below is a list of relevant smart contracts and Github repositories for using and interacting with the Yearn product suite. 

# Token Contracts 

### YFI 

The Yearn ecosystem is controlled by YFI token holders who submit and vote on proposals that govern the ecosystem.  
  
| Token    | Address | 
| -------- | -------- | 
| YFI      | [0x0bc529c00c6401aef6d220be8c6ea1667f6ad93e](https://etherscan.io/token/0x0bc529c00c6401aef6d220be8c6ea1667f6ad93e)  |

### v2 Yield Tokens

The v2 tokens can be used in one lender at a time. Currently being used on Curve’s Y Pool, Yearn’s yBTC pool and sUSD pool.

| Token    | Address | Github | 
| -------- | -------- | ------ | 
| yDAIv2   | [0x16de59092dAE5CcF4A1E6439D611fd0653f0Bd01](https://etherscan.io/address/0x16de59092dAE5CcF4A1E6439D611fd0653f0Bd01)| [YDAIv2.sol](https://github.com/iearn-finance/itoken/blob/master/contracts/YDAIv2.sol) | 
| yUSDCv2  | [0xd6aD7a6750A7593E092a9B218d66C0A814a3436e](https://etherscan.io/address/0xd6aD7a6750A7593E092a9B218d66C0A814a3436e)| [YUSDCv2.sol](https://github.com/iearn-finance/itoken/blob/master/contracts/YUSDCv2.sol) |
| yUSDTv2  | [0x83f798e925BcD4017Eb265844FDDAbb448f1707D](https://etherscan.io/address/0x83f798e925BcD4017Eb265844FDDAbb448f1707D)| [YUSDTv2.sol](https://github.com/iearn-finance/itoken/blob/master/contracts/YUSDTv2.sol) |
| ysUSDv2  | [0xF61718057901F84C4eEC4339EF8f0D86D2B45600](https://etherscan.io/address/0xF61718057901F84C4eEC4339EF8f0D86D2B45600)| [YSUSDv2.sol](https://github.com/iearn-finance/itoken/blob/master/contracts/YSUSDv2.sol) |
| yTUSDv2  | [0x73a052500105205d34daf004eab301916da8190f](https://etherscan.io/address/0x73a052500105205d34daf004eab301916da8190f)| [YTUSDv2.sol](https://github.com/iearn-finance/itoken/blob/master/contracts/YTUSDv2.sol) |
| yWBTCv2   | [0x04Aa51bbcB46541455cCF1B8bef2ebc5d3787EC9](https://etherscan.io/address/0x04Aa51bbcB46541455cCF1B8bef2ebc5d3787EC9)| [YWBTCv2.sol](https://github.com/iearn-finance/itoken/blob/master/contracts/YWBTCv2.sol) |

### v3 Yield Tokens

The v3 Yield tokens allows the underlying to be spread across multiple lenders. Currently being used on Curve’s BUSD pool.

| Token    | Address | Github |
| -------- | -------- | ------ |
| yDAIv3   | [0xC2cB1040220768554cf699b0d863A3cd4324ce32](https://etherscan.io/address/0xC2cB1040220768554cf699b0d863A3cd4324ce32)| [YDAIv3.sol](https://github.com/iearn-finance/itoken/blob/master/contracts/YDAIv3.sol) |
| yUSDCv3  | [0x26EA744E5B887E5205727f55dFBE8685e3b21951](https://etherscan.io/address/0x26EA744E5B887E5205727f55dFBE8685e3b21951)| [YUSDCv3.sol](https://github.com/iearn-finance/itoken/blob/master/contracts/YUSDCv3.sol) |
| yUSDTv3  | [0xE6354ed5bC4b393a5Aad09f21c46E101e692d447](https://etherscan.io/address/0xE6354ed5bC4b393a5Aad09f21c46E101e692d447)| [YUSDCv3.sol](https://github.com/iearn-finance/itoken/blob/master/contracts/YUSDCv3.sol) |
| yBUSDv3  | [0x04bC0Ab673d88aE9dbC9DA2380cB6B79C4BCa9aE](https://etherscan.io/address/0x04bC0Ab673d88aE9dbC9DA2380cB6B79C4BCa9aE)| [YBUSDv3.sol](https://github.com/iearn-finance/itoken/blob/master/contracts/YBUSDv3.sol) |

# Vault Contracts

Vaults follow a unique strategy that are designed to maximize the yield of the deposited asset and minimize risk. The vaults are created and maintained by a Controller, who oversees the strategy execution. Profits generated from each respective vault are used to purchase more of the underlying asset in each vault. 

The Controller contract can be found [here](https://etherscan.io/address/0x9e65ad11b299ca0abefc2799ddb6314ef2d91080#code) and the source code can be found [here](https://github.com/iearn-finance/yearn-protocol/blob/develop/contracts/controllers/Controller.sol). 

### [USDC Vault](https://etherscan.io/address/0x597aD1e0c13Bfe8025993D9e79C69E1c0233522e#code)
| Strategy Address | Status | Github | 
| ---------------- | ------ | -------|
| [StrategyDForceUSDC](https://etherscan.io/address/0xA30d1D98C502378ad61Fe71BcDc3a808CF60b897#code) | Live | [StrategyDForceUSDC.sol](https://github.com/iearn-finance/yearn-protocol/blob/develop/contracts/strategies/StrategyDForceUSDC.sol) |  
| [StrategyMStableSavings](https://etherscan.io/address/0xb17cae951b5072ef48e5e762fa6221b260387503#code) | Old | [StrategyMStableSavingsUSDC.sol](https://github.com/iearn-finance/vaults/blob/master/contracts/strategies/StrategyMStableSavingsUSDC.sol) | 


### [TUSD Vault](https://etherscan.io/address/0x37d19d1c4E1fa9DC47bD1eA12f742a0887eDa74a#code)
| Strategy Address | Status | Github | 
| ---------------- | ------ | -------|
| [StrategyTUSDCurve](https://etherscan.io/address/0x1d91E3F77271ed069618b4BA06d19821BC2ed8b0#code) | Live | [StrategyTUSDCurve.sol](https://github.com/iearn-finance/yearn-protocol/blob/develop/contracts/strategies/StrategyTUSDCurve.sol) | 
| [StrategyVaultTUSD](https://etherscan.io/address/0x35cee4c61b7619956e0b2015b5411f93cbba817a#code) | Old | [StrategyVaultTUSD.sol](https://github.com/iearn-finance/vaults/blob/master/contracts/strategies/StrategyVaultTUSD.sol) |
| [StrategyMStableSavingsTUSD](https://etherscan.io/address/0xd6214317bf66921154d78e3074bada013a4de8e8#code) | Old | [StrategyMStableSavingsTUSD.sol](https://github.com/iearn-finance/vaults/blob/master/contracts/strategies/StrategyMStableSavingsTUSD.sol) | 

### [DAI Vault](https://etherscan.io/address/0xACd43E627e64355f1861cEC6d3a6688B31a6F952#code) 
| Strategy Address | Status | Github | 
| ---------------- | ------ | -------|
| [StrategyDAICurve](https://etherscan.io/address/0xAa880345A3147a1fC6889080401C791813ed08Dc#code) | Live | [StrategyDAICurve.sol](https://github.com/iearn-finance/yearn-protocol/blob/develop/contracts/strategies/StrategyDAICurve.sol) |

### [USDT Vault](https://etherscan.io/address/0x2f08119C6f07c006695E079AAFc638b8789FAf18#code)
| Strategy Address | Status | Github | 
| ---------------- | ------ | -------|
| [StrategyDForceUSDT](https://etherscan.io/address/0x787C771035bDE631391ced5C083db424A4A64bD8#code) | Live | [StrategyDForceUSDT.sol](https://github.com/iearn-finance/yearn-protocol/blob/develop/contracts/strategies/StrategyDForceUSDT.sol) | 

### [YFI Vault](https://etherscan.io/address/0xBA2E7Fed597fd0E3e70f5130BcDbbFE06bB94fe1#code) 
| Strategy Address | Status | Github | 
| ---------------- | ------ | -------|
| [StrategyYFIGovernance](https://etherscan.io/address/0x395F93350D5102B6139Abfc84a7D6ee70488797C#code) | Live | [StrategyYFIGovernance.sol](https://github.com/iearn-finance/yearn-protocol/blob/develop/contracts/strategies/StrategyYFIGovernance.sol) |
| [StrategyCreamYFI](https://etherscan.io/address/0x40BD98e3ccE4F34c087a73DD3d05558733549afB#code) | Old | [StrategyCreamYFI.sol](https://github.com/iearn-finance/yearn-protocol/blob/develop/contracts/strategies/StrategyCreamYFI.sol) |

### [curve.fi/y LP Vault](https://etherscan.io/address/0x5dbcF33D8c2E976c6b560249878e6F1491Bca25c#code)
| Strategy Address | Status | Github | 
| ---------------- | ------ | -------|
| [StrategyCurveYVoterProxy](https://etherscan.io/address/0x594a198048501A304267E63B3bAd0f0638da7628#code) | Live | [StrategyCurveYCRVVoter.sol](https://github.com/iearn-finance/yearn-protocol/blob/develop/contracts/strategies/StrategyCurveYCRVVoter.sol)|
| [StrategyYffi](https://etherscan.io/address/0xbe197e668d13746bb92e675dea2868ff14da0b73#code) | Old | --- | 
| [StrategyYffi](https://etherscan.io/address/0x382185f3ea9268e65bb16f81de6b4e725134ed72#code) | Old | --- |
| [StrategyYffi](https://etherscan.io/address/0x8816b2fb982281c36e6c535b9e56b7a4417e68cf#code) | Old | --- |
| [StrategyYffi](https://etherscan.io/address/0x2de055fec2b826ed4a7478ceddbeff82c1edfa70#code) | Old | --- |
| [StrategyYffi](https://etherscan.io/address/0x8fcb1c3f68ef7abe7b25457f35e88658086dc1ad#code) | Old | --- |

### [curve.fi/busd LP Vault](https://etherscan.io/address/0x2994529c0652d127b7842094103715ec5299bbed#code)
| Strategy Address | Status | Github | 
| ---------------- | ------ | -------|
| [StrategyCurveYBUSDVoterProxy](https://etherscan.io/address/0x2EE856843bB65c244F527ad302d6d2853921727e#code) | Live | [StrategyCurveYBUSD.sol](https://github.com/iearn-finance/yearn-protocol/blob/develop/contracts/strategies/StrategyCurveYBUSD.sol) | 

### [curve.fi/sbtc LP Vault](https://etherscan.io/address/0x7Ff566E1d69DEfF32a7b244aE7276b9f90e9D0f6#code)
| Strategy Address | Status | Github | 
| ---------------- | ------ | -------|
| [StrategyCurveBTCVoterProxy](https://etherscan.io/address/0x134c08fAeE4F902999a616e31e0B7e42114aE320#code) | Live | [StrategyCurveSBTC.sol](https://github.com/iearn-finance/yearn-protocol/blob/develop/contracts/strategies/StrategyCurveSBTC.sol) | 

### [WETH Vault](https://etherscan.io/address/0xe1237aA7f535b0CC33Fd973D66cBf830354D16c7#code) 
| Strategy Address | Status | Github | 
| ---------------- | ------ | -------|
| [StrategyMKRVaultDAIDelegate](https://etherscan.io/address/0x932fc4fd0eEe66F22f1E23fBA74D7058391c0b15#code) | Live | [StrategyMKRVaultDAIDelegate.sol](https://github.com/iearn-finance/yearn-protocol/blob/develop/contracts/strategies/StrategyMKRVaultDAIDelegate.sol) | 

# Delegated Vault Contracts 

Volatile assets can also particpate in yield farming strategies as part of the Delegated Vault product. Currently, there is only one Delegated Vault: aLINK. The Controller deposits LINK into AAVE and borrows stablecoins. The initial health factor of these loans is always above 4, and if the health factor drops below 4 at any time the Controller repays a portion of the debt in order to maintain a health factor above 4.

The stablecoins borrowed (e.g., USDC, DAI, USDT, etc.) depend on the strategy selected by the Controller. After obtaining stablecoins the Controller will deposit them into one of the yVaults identified above.

The aLINK vault uses the StrategyControllerV2 contract — found [here](https://etherscan.io/address/0x2be5d998c95de70d9a38b3d78e49751f10f9e88b#code). The source code for StrategyControllerV2 is [here](https://github.com/iearn-finance/vaults/blob/master/contracts/controllers/StrategyControllerV2.sol). 

### [aLINK Vault](https://etherscan.io/address/0x29E240CFD7946BA20895a7a02eDb25C210f9f324#code) 
| Strategy Address | Status | Github | 
| ---------------- | ------ | -------|
| [StrategyVaultUSDC](https://etherscan.io/address/0x25fAcA21dd2Ad7eDB3a027d543e617496820d8d6#code) | Live | [StrategyVaultUSDC.sol](https://github.com/iearn-finance/yearn-protocol/blob/develop/contracts/strategies/StrategyVaultUSDC.sol)

# Governance Contracts 

YFI holders govern the Yearn ecosystem and are eligble to receive a portion of protocol profits. Therefore, YFI represents a right to govern the platform and a claim on earnings. Profits are obtained from each of Yearn's products. In order to claim profits, YFI holders stake their tokens into the Governance contract.

| Contract | Status   | Address |
| -------- | -------- | -------- |
| Governance Staking (v2) | Live | [0xba37b002abafdd8e89a1995da52740bbc013d992](https://etherscan.io/address/0xba37b002abafdd8e89a1995da52740bbc013d992#code) |
| YearnGovernance (Balancer v1) | Old | [0x3a22df48d84957f907e67f4313e3d43179040d6e](https://etherscan.io/address/0x3a22df48d84957f907e67f4313e3d43179040d6e#code)| 
| YearnRewards (Yearn v1) | Old | [0x0001fb050fe7312791bf6475b96569d83f695c9f](https://etherscan.io/address/0x0001fb050fe7312791bf6475b96569d83f695c9f#code)| 
| YearnRewards (Balancer v1) | Old | [0x033e52f513f9b98e129381c6708f9faa2dee5db5](https://etherscan.io/address/0x033e52f513f9b98e129381c6708f9faa2dee5db5#code)| 
| YearnRewards (Gov. Staking v1) | Old | [0xb01419e74d8a2abb1bbad82925b19c36c191a701](https://etherscan.io/address/0xb01419e74d8a2abb1bbad82925b19c36c191a701#code)

# Status and Info Contracts 
| Utility  | Summary  | 
| -------- | -------- | 
| [YRegistry](https://etherscan.io/address/0x3ee41c098f9666ed2ea246f4d2558010e59d63a0#code) | The Vault Registry is the single source of truth for active Yearn vaults. The registry allows users to query for active Yearn vaults and vault metadata (details [here](https://hackmd.io/JDWZ6BAuSmm-VRQRp-bZXw#Vault-Registry-)). |
| [UniswapROI](https://etherscan.io/address/0xd04ca0ae1cd8085438fdd8c22a76246f315c2687#code) | On-chain uniswap pool ROI calculator |
| [APROracle](https://etherscan.io/address/0x97ff4a1b787ade6b94cca95b61f79417c673331d#code)| Allows on-chain rate comparison between Compound, Fulcrum, Aave, and dYdX. | 
| [UniswapAPR](https://etherscan.io/address/0x4c70D89A4681b2151F56Dc2c3FD751aBb9CE3D95#code)| An on-chain uniswap pool APR calculator. It calculates all values in ETH adjusted for the last year.| 
| [IEarnAPR](https://etherscan.io/address/0x9cad8ab10daa9af1a9d2b878541f41b697268eec#code)| Contract for on-chain APR decision trees between Compound, Fulcrum, Aave, and dYdX.| 
| [IEarnManager](https://etherscan.io/address/0x318135fbd0b40d48fcef431ccdf6c7926450edfb#code)| On-chain stateless execution. Recomendations based on IearnAPR| 
| [APRWithPoolOracle](https://etherscan.io/address/0xAE8F37F0e8AD690486bFA2495113d7E94B7a7Ba6#code)| APR used for stateless `recommend()` function. Can be used to change the recommended provider.| 
| [IEarnAPRWithPool](https://etherscan.io/address/0xcD5F61c392B61F440991DEf98FF6Af07FC6900D4#code)| APR used for stateless `recommend()` function. Can be used to change the recommended provider.| 

# Utility Contracts 

| Utility  | Address | 
| -------- | -------- |  
| Curve's yPool | [0xdF5e0e81Dff6FAF3A7e52BA697820c5e32D806A8](https://etherscan.io/address/0xdF5e0e81Dff6FAF3A7e52BA697820c5e32D806A8#code) | 
