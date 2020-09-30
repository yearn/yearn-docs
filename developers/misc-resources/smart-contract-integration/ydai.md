# ydai

| Contract | ABI                                                                                   | Address                                                                                                  |
| :------- | :------------------------------------------------------------------------------------ | :------------------------------------------------------------------------------------------------------- |
| yDAIv1   | [JSON](https://github.com/iearn-finance/itoken/blob/master/build/contracts/yDAI.json) | [ydai.iearn.eth](https://etherscan.io/address/0x9d25057e62939d3408406975ad75ffe834da4cdd#readContract)   |
| yDAIv2   | [JSON](https://github.com/iearn-finance/itoken/blob/master/build/contracts/yDAI.json) | [ydai.iearn.eth](https://etherscan.io/address/0x16de59092dAE5CcF4A1E6439D611fd0653f0Bd01#readContract)   |
| yDAIv3   | [JSON](https://github.com/iearn-finance/itoken/blob/master/build/contracts/yDAI.json) | [ydaiv3.iearn.eth](https://etherscan.io/address/0xC2cB1040220768554cf699b0d863A3cd4324ce32#readContract) |

## IyDAI Interface

{% tabs %}
{% tab title="IyDAI.sol" %}

```javascript
// Solidity Interface

interface IyDAI {

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
