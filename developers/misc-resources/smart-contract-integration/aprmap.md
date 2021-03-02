# aprmap

| Contract  | ABI                                                                                            | Address                                                                                                |
| :-------- | :--------------------------------------------------------------------------------------------- | :----------------------------------------------------------------------------------------------------- |
| IIEarnAPR | [JSON](https://github.com/iearn-finance/uniswap-roi/blob/master/build/contracts/IEarnAPR.json) | [iapr.iearn.eth](https://etherscan.io/address/0x9cad8ab10daa9af1a9d2b878541f41b697268eec#readContract) |

## IIEarnAPR Interface

{% tabs %}
{% tab title="IIEarnAPR.sol" %}

```javascript
// Solidity Interface

interface IIEarnAPR {

    function getSNX() external view returns (
      uint256 uniapr,
      uint256 capr,
      uint256 unicapr,
      uint256 iapr,
      uint256 uniiapr,
      uint256 aapr,
      uint256 uniaapr,
      uint256 dapr
    );

    function getUSDT() external view returns (
      uint256 uniapr,
      uint256 capr,
      uint256 unicapr,
      uint256 iapr,
      uint256 uniiapr,
      uint256 aapr,
      uint256 uniaapr,
      uint256 dapr
    );

    function getBAT() external view returns (
      uint256 uniapr,
      uint256 capr,
      uint256 unicapr,
      uint256 iapr,
      uint256 uniiapr,
      uint256 aapr,
      uint256 uniaapr,
      uint256 dapr
    );

    function getMKR() external view returns (
      uint256 uniapr,
      uint256 capr,
      uint256 unicapr,
      uint256 iapr,
      uint256 uniiapr,
      uint256 aapr,
      uint256 uniaapr,
      uint256 dapr
    );

    function getZRX() external view returns (
      uint256 uniapr,
      uint256 capr,
      uint256 unicapr,
      uint256 iapr,
      uint256 uniiapr,
      uint256 aapr,
      uint256 uniaapr,
      uint256 dapr
    );

    function getREP() external view returns (
      uint256 uniapr,
      uint256 capr,
      uint256 unicapr,
      uint256 iapr,
      uint256 uniiapr,
      uint256 aapr,
      uint256 uniaapr,
      uint256 dapr
    );

    function getKNC() external view returns (
      uint256 uniapr,
      uint256 capr,
      uint256 unicapr,
      uint256 iapr,
      uint256 uniiapr,
      uint256 aapr,
      uint256 uniaapr,
      uint256 dapr
    );

    function getWBTC() external view returns (
      uint256 uniapr,
      uint256 capr,
      uint256 unicapr,
      uint256 iapr,
      uint256 uniiapr,
      uint256 aapr,
      uint256 uniaapr,
      uint256 dapr
    );

    function getLINK() external view returns (
      uint256 uniapr,
      uint256 capr,
      uint256 unicapr,
      uint256 iapr,
      uint256 uniiapr,
      uint256 aapr,
      uint256 uniaapr,
      uint256 dapr
    );

    function getSUSD() external view returns (
      uint256 uniapr,
      uint256 capr,
      uint256 unicapr,
      uint256 iapr,
      uint256 uniiapr,
      uint256 aapr,
      uint256 uniaapr,
      uint256 dapr
    );

    function getDAI() external view returns (
      uint256 uniapr,
      uint256 capr,
      uint256 unicapr,
      uint256 iapr,
      uint256 uniiapr,
      uint256 aapr,
      uint256 uniaapr,
      uint256 dapr
    );

    function getETH() external view returns (
      uint256 uniapr,
      uint256 capr,
      uint256 unicapr,
      uint256 iapr,
      uint256 uniiapr,
      uint256 aapr,
      uint256 uniaapr,
      uint256 dapr
    );

    function getUSDC() external view returns (
      uint256 uniapr,
      uint256 capr,
      uint256 unicapr,
      uint256 iapr,
      uint256 uniiapr,
      uint256 aapr,
      uint256 uniaapr,
      uint256 dapr
    );

    function getAPROptions(address _token) external view returns (
      uint256 uniapr,
      uint256 capr,
      uint256 unicapr,
      uint256 iapr,
      uint256 uniiapr,
      uint256 aapr,
      uint256 uniaapr,
      uint256 dapr
    );

    function viewPool(address _token) external view returns (
      address token,
      address unipool,
      uint256 created,
      string memory name,
      string memory symbol
    );
}
```

{% endtab %}
{% endtabs %}
