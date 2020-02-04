# Smart Contract Interface

| Contract | ABI | Address |
| -- | -- | -- |
| APRWithPoolOracle | [JSON](https://github.com/iearn-finance/apr-oracle/blob/master/build/contracts/APRWithPoolOracle.json) | [apradj.iearn.eth](https://etherscan.io/address/0x9f0842A5b18578abe1f7a5AdE0C1f915116254d7#code) |

## APRWithPoolOracle Interface

{% tabs %}
{% tab title="APRWithPoolOracle.sol" %}
```javascript
// Solidity Interface

interface APRWithPoolOracle {
  function getLENDFAPR(address token) external view returns (uint256);
  function getLENDFAPRAdjusted(address token, uint256 _supply) external view returns (uint256);
  function getDDEXAPR(address token) external view returns (uint256);
  function getDDEXAPRAdjusted(address token, uint256 _supply) external view returns (uint256);
  function getCompoundAPR(address token) external view returns (uint256);
  function getCompoundAPRAdjusted(address token, uint256 _supply) external view returns (uint256);
  function getFulcrumAPR(address token) external view returns(uint256);
  function getFulcrumAPRAdjusted(address token, uint256 _supply) external view returns(uint256);
  function getDyDxAPR(uint256 marketId) external view returns(uint256);
  function getDyDxAPRAdjusted(uint256 marketId, uint256 _supply) external view returns(uint256);
  function getAaveCore() external view returns (address);
  function getAaveAPR(address token) external view returns (uint256);
  function getAaveAPRAdjusted(address token, uint256 _supply) external view returns (uint256);
}

```
{% endtab %}
{% endtabs %}
