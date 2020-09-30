# uniswapapr

| Contract   | ABI                                                                                              | Address                                                                                                  |
| :--------- | :----------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------- |
| UniswapAPR | [JSON](https://github.com/iearn-finance/uniswap-roi/blob/master/build/contracts/UniswapAPR.json) | [uniapr.iearn.eth](https://etherscan.io/address/0x4c70D89A4681b2151F56Dc2c3FD751aBb9CE3D95#readContract) |

## UniswapAPR Interface

{% tabs %}
{% tab title="IUniswapAPR.sol" %}

```javascript
// Solidity Interface

contract IUniswapAPR {

    function getBlocksPerYear() external view returns (uint256);

    function calcUniswapAPRADAI() external view returns (uint256, uint256);
    function calcUniswapAPRCDAI() external view returns (uint256, uint256);
    function calcUniswapAPRCETH() external view returns (uint256, uint256);
    function calcUniswapAPRCSAI() external view returns (uint256, uint256);
    function calcUniswapAPRCUSDC() external view returns (uint256, uint256);
    function calcUniswapAPRDAI() external view returns (uint256, uint256);
    function calcUniswapAPRIDAI() external view returns (uint256, uint256);
    function calcUniswapAPRISAI() external view returns (uint256, uint256);
    function calcUniswapAPRSUSD() external view returns (uint256, uint256);
    function calcUniswapAPRTUSD() external view returns (uint256, uint256);
    function calcUniswapAPRUSDC() external view returns (uint256, uint256);
    function calcUniswapAPRCHAI() external view returns (uint256, uint256);

    function calcUniswapAPRFromROI(uint256 roi, uint256 createdAt) external view returns (uint256);

    function calcUniswapAPR(address token, uint256 createdAt) external view returns (uint256);
}
```

{% endtab %}
{% endtabs %}
