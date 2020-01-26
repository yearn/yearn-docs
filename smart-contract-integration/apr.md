# Smart Contract Interface

| Contract | ABI | Address |
| -- | -- | -- |
| APROracle | [JSON](https://github.com/iearn-finance/apr-oracle/blob/master/build/contracts/APROracle.json) | [apr.iearn.eth](https://etherscan.io/address/0x97ff4a1b787ade6b94cca95b61f79417c673331d#code) |

## APR Interface

{% tabs %}
{% tab title="IAPROracle.sol" %}
```javascript
// Solidity Interface

interface IAPROracle {
  function recommendDAI() external view returns (string memory);
  function recommendETH() external view returns (string memory);
  function recommendUSDC() external view returns (string memory);
  function getAllCompoundAPR()
      external
      view
      returns (
          uint256 cDAI,
          uint256 cBAT,
          uint256 cETH,
          uint256 cREP,
          uint256 cSAI,
          uint256 cUSDC,
          uint256 cWBTC,
          uint256 cZRC
      );

  // Compound
  function getCDAIAPR() external view returns (uint256);
  function getCBATAPR() external view returns (uint256);
  function getCETHAPR() external view returns (uint256);
  function getCREPAPR() external view returns (uint256);
  function getCSAIAPR() external view returns (uint256);
  function getCUSDCAPR() external view returns (uint256);
  function getCWBTCAPR() external view returns (uint256);
  function getCZRCAPR() public view returns (uint256);
  function getCompoundAPR(address token) public view returns (uint256);

  function getAllDyDxAPR()
      external
      view
      returns (
          uint256 dSAI,
          uint256 dETH,
          uint256 dUSDC,
          uint256 dDAI
      );

  // dYdX
  function getDyDxSAIAPR() public view returns(uint256);
  function getDyDxETHAPR() public view returns(uint256);
  function getDyDxUSDCAPR() public view returns(uint256);
  function getDyDxDAIAPR() public view returns(uint256);

  function getAllFulcrumAPR()
      external
      view
      returns (
          uint256 iZRX,
          uint256 iREP,
          uint256 iKNC,
          uint256 iWBTC,
          uint256 iUSDC,
          uint256 iETH,
          uint256 iSAI,
          uint256 iDAI,
          uint256 iLINK,
          uint256 iSUSD
      );

  // Fulcrum
  function getIZRXAPR() public view returns (uint256);
  function getIREPAPR() public view returns (uint256);
  function getIKNCAPR() public view returns (uint256);
  function getIWBTCAPR() public view returns (uint256);
  function getIUSDCAPR() public view returns (uint256);
  function getIETHAPR() public view returns (uint256);
  function getISAIAPR() public view returns (uint256);
  function getIDAIAPR() public view returns (uint256);
  function getILINKAPR() public view returns (uint256);
  function getISUSDAPR() public view returns (uint256);

  function getFulcrumAPR(address token) public view returns(uint256);

  function getDyDxAPR(uint256 marketId) public view returns(uint256);

  function getAllAaveAPR()
      external
      view
      returns (
          uint256 aDAI,
          uint256 aTUSD,
          uint256 aUSDC,
          uint256 aUSDT,
          uint256 aSUSD,
          uint256 aBAT,
          uint256 aETH,
          uint256 aLINK,
          uint256 aKNC,
          uint256 aREP,
          uint256 aZRX,
          uint256 aSNX
      );

  function getADAIAPR() public view returns (uint256);
  function getATUSDAPR() public view returns (uint256);
  function getAUSDCAPR() public view returns (uint256);
  function getAUSDTAPR() public view returns (uint256);
  function getASUSDAPR() public view returns (uint256);
  function getALENDAPR() public view returns (uint256);
  function getABATAPR() public view returns (uint256);
  function getAETHAPR() public view returns (uint256);
  function getALINKAPR() public view returns (uint256);
  function getAKNCAPR() public view returns (uint256);
  function getAREPAPR() public view returns (uint256);
  function getAMKRAPR() public view returns (uint256);
  function getAMANAAPR() public view returns (uint256);
  function getAZRXAPR() public view returns (uint256);
  function getASNXAPR() public view returns (uint256);
  function getAWBTCAPR() public view returns (uint256);

  function getAaveAPR(address token) public view returns (uint256);
}
```
{% endtab %}
{% endtabs %}
