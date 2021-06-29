# Vault Tokens

[yVault Tokens](https://docs.yearn.finance/resources/defi-glossary#ytoken) are like a deposit receipt. They represent a user's share of the yVault that they are participating in.

**For example**, if you deposit YFI in a yVault you will receive yvYFI in return. yvYFI would be the yVault Token.

If your yVault generates profit, the share price of your yVault tokens will increase. This happens because there are more underlying tokens in the yVault to redeem upon withdrawal.

![](https://i.imgur.com/OtK6kAA.png)

*The yvYFI token at [Etherscan](https://etherscan.io/token/0xE14d13d8B3b85aF791b2AADD661cDBd5E6097Db1#readContract), showing its name, total assets and price per share.*

Once a user's liquidity is withdrawn from the yVault, their yVault Token will be burned. yVault Tokens are [ERC20](https://docs.ethhub.io/built-on-ethereum/erc-token-standards/erc20/), meaning they can be transferred and traded as any other common Ethereum token.

## V2 yVault Tokens

| Vault | Input Token | Output Token | 
| :--- | :--- | :--- | 
| YFI | [YFI](https://etherscan.io/token/0x0bc529c00c6401aef6d220be8c6ea1667f6ad93e) | [yvYFI](https://etherscan.io/token/0xE14d13d8B3b85aF791b2AADD661cDBd5E6097Db1) |
| 1INCH | [1INCH](https://etherscan.io/token/0x111111111117dc0aa78b770fa6a738034120c302) | [yv1INCH](https://etherscan.io/token/0xB8C3B7A2A618C552C23B1E4701109a9E756Bab67) |
| WETH | [WETH](https://etherscan.io/token/0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2) | [yvWETH](https://etherscan.io/token/0xa9fE4601811213c340e850ea305481afF02f5b28) |
| USDC | [USDC](https://etherscan.io/token/0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48) | [yvUSDC](https://etherscan.io/token/0x5f18c75abdae578b483e5f43f12a39cf75b973a9) |
| HEGIC | [HEGIC](https://etherscan.io/token/0x584bC13c7D411c00c01A62e8019472dE68768430) | [HEGIC](https://etherscan.io/token/0x584bC13c7D411c00c01A62e8019472dE68768430) |
| DAI | [DAI](https://etherscan.io/token/0x6b175474e89094c44da98b954eedeac495271d0f) | [yvDAI](https://etherscan.io/token/0x19d3364a399d251e894ac732651be8b0e4e85001) |
| WBTC | [WBTC yVault](https://etherscan.io/address/0xcb550a6d4c8e3517a939bc79d0c7093eb7cf56b5) | [WBTC yVault](https://etherscan.io/address/0xcb550a6d4c8e3517a939bc79d0c7093eb7cf56b5) |
| USDT | [WBTC yVault](https://etherscan.io/address/0xcb550a6d4c8e3517a939bc79d0c7093eb7cf56b5) | [yvUDST](https://etherscan.io/token/0x7Da96a3891Add058AdA2E826306D812C638D87a7) |
| crvIB | [Curve Iron Bank Pool yVault](https://etherscan.io/address/0x27b7b1ad7288079A66d12350c828D3C00A6F07d7) | [yCurve-IronBank](https://etherscan.io/token/0x27b7b1ad7288079A66d12350c828D3C00A6F07d7) |
| crvSETH | [Curve sETH Pool yVault](https://etherscan.io/address/0x986b4AFF588a109c09B50A03f42E4110E29D353F) | [yvCurve-sETH](https://etherscan.io/token/0x986b4AFF588a109c09B50A03f42E4110E29D353F) |
| crvstETH | [Curve stETH Pool yVault](https://etherscan.io/address/0xdcd90c7f6324cfa40d7169ef80b12031770b4325) | [yvCurve-stETH](https://etherscan.io/token/0xdcd90c7f6324cfa40d7169ef80b12031770b4325) |
| crvSBTC | [Curve sBTC Pool yVault](https://etherscan.io/address/0x8414Db07a7F743dEbaFb402070AB01a4E0d2E45e) | [yvCurve-sBTC](https://etherscan.io/token/0x8414Db07a7F743dEbaFb402070AB01a4E0d2E45e) |
| crvRENBTC | [Curve renBTC Pool yVault](https://etherscan.io/address/0x7047F90229a057C13BF847C0744D646CFb6c9E1A) | [yvCurve-renBTC](https://etherscan.io/token/0x7047F90229a057C13BF847C0744D646CFb6c9E1A) |
| crvOBTC | [Curve oBTC Pool yVault](https://etherscan.io/address/0xe9Dc63083c464d6EDcCFf23444fF3CFc6886f6FB) | [yvCurve-oBTC](https://etherscan.io/token/0xe9Dc63083c464d6EDcCFf23444fF3CFc6886f6FB) |
| crvPBTC | [Curve pBTC Pool yVault](https://etherscan.io/address/0x3c5DF3077BcF800640B5DAE8c91106575a4826E6) | [yvCurve-pBTC](https://etherscan.io/token/0x3c5DF3077BcF800640B5DAE8c91106575a4826E6) | 
| crvTBTC | [Curve tBTC Pool yVaut](https://etherscan.io/address/0x23D3D0f1c697247d5e0a9efB37d8b0ED0C464f7f) | [yvCurve-tBTC](https://etherscan.io/token/0x23D3D0f1c697247d5e0a9efB37d8b0ED0C464f7f) | 
| crvFRAX | [Curve FRAX Pool yVault](https://etherscan.io/address/0xB4AdA607B9d6b2c9Ee07A275e9616B84AC560139#code) | [yvCurve-FRAX](https://etherscan.io/token/0xB4AdA607B9d6b2c9Ee07A275e9616B84AC560139) | 
| crvLUSD | [Curve LUSD Pool yVault](https://etherscan.io/address/0x5fA5B62c8AF877CB37031e0a3B2f34A78e3C56A6#code) | [yvCurve-LUSD](https://etherscan.io/token/0x5fA5B62c8AF877CB37031e0a3B2f34A78e3C56A6) | 
| crvSAAVE | [Curve sAave Pool yVault](https://etherscan.io/address/0xb4D1Be44BfF40ad6e506edf43156577a3f8672eC#code) | [yvCurve-sAave](https://etherscan.io/token/0xb4D1Be44BfF40ad6e506edf43156577a3f8672eC) | 
| crvBBTC | [Curve BBTC Pool yVault](https://etherscan.io/address/0x8fA3A9ecd9EFb07A8CE90A6eb014CF3c0E3B32Ef) | [yvCurve-BBTC](https://etherscan.io/token/0x8fA3A9ecd9EFb07A8CE90A6eb014CF3c0E3B32Ef) | 
| yvBOOST | [Yearn Compounding veCRV yVault](https://etherscan.io/address/0x9d409a0A012CFbA9B15F6D4B36Ac57A46966Ab9a) | [yvBOOST](https://etherscan.io/token/0x9d409a0A012CFbA9B15F6D4B36Ac57A46966Ab9a) | 

## V1 yVault Tokens

| Vault | Input Token | Output Token |
| :--- | :--- | :--- |
| crvLINK | [linkCRV](https://etherscan.io/token/0xcee60cfa923170e4f8204ae08b4fa6a3f5656f3a) | [yvlinkCRV](https://etherscan.io/token/0x96Ea6AF74Af09522fCB4c28C269C26F59a31ced6) |
| crvUSDP | [usdp3CRV](https://etherscan.io/token/0x7Eb40E450b9655f4B3cC4259BCC731c63ff55ae6) | [yvusdp3CRV](https://etherscan.io/token/0x1B5eb1173D2Bf770e50F10410C9a96F7a8eB6e75) |
| crvANKR | [ankrCRV](https://etherscan.io/token/0xaA17A236F2bAdc98DDc0Cf999AbB47D47Fc0A6Cf) | [yvankrCRV](https://etherscan.io/token/0xE625F5923303f1CE7A43ACFEFd11fd12f30DbcA4) |
| yCRV\(yUSD\) | [yDAI+yUSDC+yUSDT+yTUSD](https://etherscan.io/token/0xdF5e0e81Dff6FAF3A7e52BA697820c5e32D806A8) | [yyDAI+yUSDC+yUSDT+yTUSD](https://etherscan.io/token/0x5dbcf33d8c2e976c6b560249878e6f1491bca25c) |
| crvMUSD | [musd3CRV](https://etherscan.io/token/0x1AEf73d49Dedc4b1778d0706583995958Dc862e6) | [yvmusd3CRV](https://etherscan.io/token/0x0FCDAeDFb8A7DfDa2e9838564c5A1665d856AFDF) |
| crvGUSD | [gusd3CRV](https://etherscan.io/token/0xD2967f45c4f384DEEa880F807Be904762a3DeA07) | [yvgusd3CRV](https://etherscan.io/token/0xcC7E70A958917cCe67B4B87a8C30E6297451aE98) |
| crvDUSD | [dusd3CRV](https://etherscan.io/token/0x3a664Ab939FD8482048609f652f9a0B0677337B9) | [yvdusd3CRV](https://etherscan.io/address/0x8e6741b456a074F0Bc45B8b82A755d4aF7E965dF#code) |
| crvUSDN | [usdn3CRV](https://etherscan.io/token/0x4f3E8F405CF5aFC05D68142F3783bDfE13811522) | [yvusdn3CRV](https://etherscan.io/token/0xFe39Ce91437C76178665D64d7a2694B0f6f17fE3) |
| crvUSDT | [ust3CRV](https://etherscan.io/token/0x94e131324b6054c0D789b190b2dAC504e4361b53) | [yvusdt3CRV](https://etherscan.io/token/0xF6C9E9AF314982A4b38366f4AbfAa00595C5A6fC) |
| crvHUSD | [husd3CRV](https://etherscan.io/token/0x5B5CFE992AdAC0C9D48E05854B2d91C73a003858) | [yvhusd3CRV](https://etherscan.io/token/0x39546945695DCb1c037C836925B355262f551f55) |
| crvBUSD | [yDAI+yUSDC+yUSDT+yBUSD \(bCrv\)](https://etherscan.io/token/0x3B3Ac5386837Dc563660FB6a0937DFAa5924333B) | [yyDAI+yUSDC+yUSDT+yBUSD](https://etherscan.io/token/0x2994529C0652D127b7842094103715ec5299bBed) |
| crvSUSD | [crvPlain3andSUSD \(sCrv\)](https://etherscan.io/token/0xC25a3A3b969415c80451098fa907EC722572917F) | [yvcrvPlain3andSUSD](https://etherscan.io/token/0x5533ed0a3b83F70c3c4a1f69Ef5546D3D4713E44) |
| 3Crv | [3Crv](https://etherscan.io/token/0x6c3F90f043a72FA612cbac8115EE7e52BDe6E490) | [y3Crv](https://etherscan.io/token/0x9cA85572E6A3EbF24dEDd195623F188735A5179f) |
| crvEURS | [eursCRV](https://etherscan.io/token/0x194eBd173F6cDacE046C53eACcE9B953F28411d1) | [yveursCRV](https://etherscan.io/token/0x98B058b2CBacF5E99bC7012DF757ea7CFEbd35BC) |
| crvHBTC | [hCRV](https://etherscan.io/token/0xb19059ebb43466C323583928285a49f558E572Fd) | [yvhCRV](https://etherscan.io/token/0x46AFc2dfBd1ea0c0760CAD8262A5838e803A37e5) |

