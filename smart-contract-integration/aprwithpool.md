# Smart Contract Interface

| Contract | ABI | Address |
| -- | -- | -- |
| APRWithPoolOracle | [JSON](https://github.com/iearn-finance/apr-oracle/blob/master/build/contracts/APRWithPoolOracle.json) | [apradj.iearn.eth](https://etherscan.io/address/0xDAe803688cbaa5eB0EA17e1332569F0C235f5A54#code) |

## APRWithPoolOracle Interface

{% tabs %}
{% tab title="APRWithPoolOracle.sol" %}
```javascript
// Solidity Interface

interface APRWithPoolOracle {

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
