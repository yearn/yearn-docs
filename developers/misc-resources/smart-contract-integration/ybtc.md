# ybtc

| Contract | ABI                                                                                   | Address                                                                                                  |
| :------- | :------------------------------------------------------------------------------------ | :------------------------------------------------------------------------------------------------------- |
| yBTC     | [JSON](https://github.com/iearn-finance/itoken/blob/master/build/contracts/yBTC.json) | [ybtc.iearn.eth](https://etherscan.io/address/0x04ef8121ad039ff41d10029c91ea1694432514e9#readContract)   |
| yBTCv2   | [JSON](https://github.com/iearn-finance/itoken/blob/master/build/contracts/yBTC.json) | [ybtcv2.iearn.eth](https://etherscan.io/address/0x04Aa51bbcB46541455cCF1B8bef2ebc5d3787EC9#readContract) |

## IyBTC Interface

{% tabs %}
{% tab title="IyBTC.sol" %}

```javascript
// Solidity Interface

interface IyBTC {

  function withdraw(uint256 _shares) external;
  function deposit(uint256 _amount) external;

  function balance() external view returns (uint256);
  function balanceDydx() external view returns (uint256);
  function balanceCompound() external view returns (uint256);
  function balanceCompoundInToken() external view returns (uint256);
  function balanceFulcrumInToken() external view returns (uint256);
  function balanceFulcrum() external view returns (uint256);
  function balanceAave() external view returns (uint256);

  function recommend() external view returns (uint256);
  function rebalance() external;

  function supplyDydx(uint256 amount) external returns(uint);
  function supplyAave(uint amount) external;
  function supplyFulcrum(uint amount) external;
  function supplyCompound(uint amount) external;

  function calcPoolValueInToken() external view returns (uint256);
  function getPricePerFullShare() external view returns (uint256);
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
