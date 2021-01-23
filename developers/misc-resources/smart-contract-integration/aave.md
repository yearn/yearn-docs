# aave

{% tabs %}
{% tab title="LendingPoolCore.sol" %}

```javascript
// Solidity Interface

interface LendingPoolCore  {
  function getReserveCurrentLiquidityRate(address _reserve)
  external
  view
  returns (
      uint256 liquidityRate
  );
}
```

{% endtab %}
{% endtabs %}
