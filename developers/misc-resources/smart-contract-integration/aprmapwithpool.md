# aprmapwithpool

| Contract          | ABI                                                                                                     | Address                                                                                                   |
| :---------------- | :------------------------------------------------------------------------------------------------------ | :-------------------------------------------------------------------------------------------------------- |
| IIEarnAPRWithPool | [JSON](https://github.com/iearn-finance/uniswap-roi/blob/master/build/contracts/IIEarnAPRWithPool.json) | [iapradj.iearn.eth](https://etherscan.io/address/0xAE8F37F0e8AD690486bFA2495113d7E94B7a7Ba6#readContract) |

## IIEarnAPRWithPool Interface

{% tabs %}
{% tab title="IIEarnAPRWithPool.sol" %}

```javascript
// Solidity Interface

interface IIEarnAPRWithPool {

    function getAPROptions(address _token) external view returns (
      uint256 _uniswap,
      uint256 _compound,
      uint256 _unicompound,
      uint256 _fulcrum,
      uint256 _unifulcrum,
      uint256 _aave,
      uint256 _uniaave,
      uint256 _dydx,
      uint256 _ddex,
      uint256 _lendf
    );

    function getAPROptionsAdjusted(address _token, uint256 _supply) external view returns (
      uint256 _uniswap,
      uint256 _compound,
      uint256 _unicompound,
      uint256 _fulcrum,
      uint256 _unifulcrum,
      uint256 _aave,
      uint256 _uniaave,
      uint256 _dydx,
      uint256 _ddex,
      uint256 _lendf
    );

    function viewPool(address _token) external view returns;
}
```

{% endtab %}
{% endtabs %}
