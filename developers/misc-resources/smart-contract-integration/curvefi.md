# curvefi

| Contract | ABI                                                                                                    | Address                                                                                  |
| :------- | :----------------------------------------------------------------------------------------------------- | :--------------------------------------------------------------------------------------- |
| ICurveFi | [JSON](https://github.com/curvefi/curve-contract/blob/compounded/deployed/2020-01-21_mainnet/swap.abi) | [curve.fi](https://etherscan.io/address/0x2e60CF74d81ac34eB21eEff58Db4D385920ef419#code) |

## ICurveFi Interface

{% tabs %}
{% tab title="ICurveFi.sol" %}

```javascript
// Solidity Interface

interface ICurveFi {

  function get_virtual_price() external view returns (uint256);
  function get_dy(
    int128 i,
    int128 j,
    uint256 dx
  ) external view returns (uint256);
  function get_dy_underlying(
    int128 i,
    int128 j,
    uint256 dx
  ) external view returns (uint256);
  function coins(int128 arg0) external view returns (address);
  function underlying_coins(int128 arg0) external view returns (address);
  function balances(int128 arg0) external view returns (uint256);

  function add_liquidity(
    uint256[2] calldata amounts,
    uint256 deadline
  ) external;
  function exchange(
    int128 i,
    int128 j,
    uint256 dx,
    uint256 min_dy,
    uint256 deadline
  ) external;
  function exchange_underlying(
    int128 i,
    int128 j,
    uint256 dx,
    uint256 min_dy,
    uint256 deadline
  ) external;
  function remove_liquidity(
    uint256 _amount,
    uint256 deadline,
    uint256[2] calldata min_amounts
  ) external;
  function remove_liquidity_imbalance(
    uint256[2] calldata amounts,
    uint256 deadline
  ) external;
}
```

{% endtab %}
{% endtabs %}
