# ysusd

| Contract | ABI                                                                                    | Address                                                                                    |
| :------- | :------------------------------------------------------------------------------------- | :----------------------------------------------------------------------------------------- |
| ySUSD    | [JSON](https://github.com/iearn-finance/itoken/blob/master/build/contracts/ySUSD.json) | [ysusd.iearn.eth](https://etherscan.io/address/0x36324b8168f960A12a8fD01406C9C78143d41380) |
| ySUSDv2  | [JSON](https://github.com/iearn-finance/itoken/blob/master/build/contracts/ySUSD.json) | [ysusd.iearn.eth](https://etherscan.io/address/0xF61718057901F84C4eEC4339EF8f0D86D2B45600) |

## IySUSD Interface

{% tabs %}
{% tab title="IySUSD.sol" %}

```javascript
// Solidity Interface

interface IySUSD {

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
