# Smart Contract Interface

| Contract | ABI | Address |
| -- | -- | -- |
| UniswapROI | [JSON](https://github.com/iearn-finance/uniswap-roi/blob/master/build/contracts/UniswapAPR.json) | [uniapr.iearn.eth](https://etherscan.io/address/0xd04ca0ae1cd8085438fdd8c22a76246f315c2687#readContract) |


## UniswapROI Interface

{% tabs %}
{% tab title="UniswapROI.sol" %}
```javascript
// Solidity Interface

interface IUniswapROI {

    function getCDAIUniROI() public view returns (uint256, uint256);
    function getCBATUniROI() public view returns (uint256, uint256);
    function getCETHUniROI() public view returns (uint256, uint256);
    function getCREPUniROI() public view returns (uint256, uint256);
    function getCSAIUniROI() public view returns (uint256, uint256);
    function getCUSDCUniROI() public view returns (uint256, uint256);
    function getCWBTCUniROI() public view returns (uint256, uint256);
    function getCZRXUniROI() public view returns (uint256, uint256);


    function getIZRXUniROI() public view returns (uint256, uint256);
    function getIREPUniROI() public view returns (uint256, uint256);
    function getIKNCUniROI() public view returns (uint256, uint256);
    function getIWBTCUniROI() public view returns (uint256, uint256);
    function getIUSDCUniROI() public view returns (uint256, uint256);
    function getIETHUniROI() public view returns (uint256, uint256);
    function getISAIUniROI() public view returns (uint256, uint256);
    function getIDAIUniROI() public view returns (uint256, uint256);
    function getILINKUniROI() public view returns (uint256, uint256);
    function getISUSDUniROI() public view returns (uint256, uint256);

    function getADAIUniROI() public view returns (uint256, uint256);
    function getATUSDUniROI() public view returns (uint256, uint256);
    function getAUSDCUniROI() public view returns (uint256, uint256);
    function getAUSDTUniROI() public view returns (uint256, uint256);
    function getASUSDUniROI() public view returns (uint256, uint256);
    function getALENDUniROI() public view returns (uint256, uint256);
    function getABATUniROI() public view returns (uint256, uint256);
    function getAETHUniROI() public view returns (uint256, uint256);
    function getALINKUniROI() public view returns (uint256, uint256);
    function getAKNCUniROI() public view returns (uint256, uint256);
    function getAREPUniROI() public view returns (uint256, uint256);
    function getAMKRUniROI() public view returns (uint256, uint256);
    function getAMANAUniROI() public view returns (uint256, uint256);
    function getAZRXUniROI() public view returns (uint256, uint256);
    function getASNXUniROI() public view returns (uint256, uint256);
    function getAWBTCUniROI() public view returns (uint256, uint256);

    function getDAIUniROI() public view returns (uint256, uint256);
    function getTUSDUniROI() public view returns (uint256, uint256);
    function getUSDCUniROI() public view returns (uint256, uint256);
    function getUSDTUniROI() public view returns (uint256, uint256);
    function getSUSDUniROI() public view returns (uint256, uint256);
    function getLENDUniROI() public view returns (uint256, uint256);
    function getBATUniROI() public view returns (uint256, uint256);
    function getETHUniROI() public view returns (uint256, uint256);
    function getLINKUniROI() public view returns (uint256, uint256);
    function getKNCUniROI() public view returns (uint256, uint256);
    function getREPUniROI() public view returns (uint256, uint256);
    function getMKRUniROI() public view returns (uint256, uint256);
    function getMANAUniROI() public view returns (uint256, uint256);
    function getZRXUniROI() public view returns (uint256, uint256);
    function getSNXUniROI() public view returns (uint256, uint256);
    function getWBTCUniROI() public view returns (uint256, uint256);

    function calcUniswapROI(address token) public view returns (uint256, uint256);
}
```
{% endtab %}
{% endtabs %}
