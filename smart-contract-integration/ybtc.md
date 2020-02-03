# Smart Contract Interface

| Contract | ABI | Address |
| -- | -- | -- |
| yBTC | [JSON](https://github.com/iearn-finance/itoken/blob/master/build/contracts/yBTC.json) | [ybtc.iearn.eth](https://etherscan.io/address/0x04ef8121ad039ff41d10029c91ea1694432514e9#readContract) |

## IyBTC Interface

{% tabs %}
{% tab title="IyBTC.sol" %}
```javascript
// Solidity Interface

interface IyBTC {

  function recommend() external view returns (uint256);

  function supplyDydx(uint256 amount) external returns(uint);

  function balance() external view returns (uint256);

  function getAave() external view returns (address);
  function getAaveCore() external view returns (address);

  function approveToken() external;

  function balanceDydx() external view returns (uint256);
  function balanceCompound() external view returns (uint256);
  function balanceCompoundInToken() external view returns (uint256);
  function balanceFulcrumInToken() external view returns (uint256);
  function balanceFulcrum() external view returns (uint256);
  function balanceAave() external view returns (uint256);

  function rebalance() external;

  function supplyAave(uint amount) external;
  function supplyFulcrum(uint amount) external;
  function supplyCompound(uint amount) external;

  // Invest ETH
  function invest(uint256 _amount) external;

  // Invest self eth from external profits
  function investSelf() external;

  function calcPoolValueInToken() external view returns (uint256);

  function getPricePerFullShare() external view returns (uint256);

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
