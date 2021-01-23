# ycrv

| Contract | ABI                                                                                   | Address                                                                                   |
| :------- | :------------------------------------------------------------------------------------ | :---------------------------------------------------------------------------------------- |
| IyCRV    | [JSON](https://github.com/iearn-finance/itoken/blob/master/build/contracts/yCRV.json) | [ycrv.iearn.eth](https://etherscan.io/address/0x9Ce551A9D2B1A4Ec0cc6eB0E0CC12977F6ED306C) |

## IyUSDT Interface

{% tabs %}
{% tab title="IyCRV.sol" %}

```javascript
// Solidity Interface

interface IyCRV {
  function balanceCompound() public view returns (uint256);
  function supplyCompound(uint amount) public;
  function invest(uint256 _amount) external;

  function crvapr() external view returns (uint256);

  function calcPoolValueInToken() external view returns (uint);

  function getPricePerFullShare() external view returns (uint);

  // Redeem any invested tokens from the pool
  function redeem(uint256 _shares) external;
}
```

{% endtab %}
{% endtabs %}

## ERC20 Token Interface

{% tabs %}
{% tab title="TokenInterface.sol" %}

```javascript
// https://theethereum.wiki/w/index.php/ERC20_Token_Standard
contract ERC20Interface {
    function totalSupply() public view returns (uint);
    function balanceOf(address tokenOwner) public view returns (uint balance);
    function allowance(address tokenOwner, address spender) public view returns (uint remaining);
    function transfer(address to, uint tokens) public returns (bool success);
    function approve(address spender, uint tokens) public returns (bool success);
    function transferFrom(address from, address to, uint tokens) public returns (bool success);
    // optional
    function name() external view returns (string);
    function symbol() external view returns (string);
    function decimals() external view returns (string);

    event Transfer(address indexed from, address indexed to, uint tokens);
    event Approval(address indexed tokenOwner, address indexed spender, uint tokens);
}
```

{% endtab %}
{% endtabs %}
