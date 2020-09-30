# yusdc

| Contract | ABI                                                                                    | Address                                                                                      |
| :------- | :------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------- |
| yUSDCv1  | [JSON](https://github.com/iearn-finance/itoken/blob/master/build/contracts/yUSDC.json) | [yusdc.iearn.eth](https://etherscan.io/address/0xa2609b2b43ac0f5ebe27deb944d2a399c201e3da)   |
| yUSDCv2  | [JSON](https://github.com/iearn-finance/itoken/blob/master/build/contracts/yUSDC.json) | [yusdcv2.iearn.eth](https://etherscan.io/address/0xd6aD7a6750A7593E092a9B218d66C0A814a3436e) |
| yUSDCv3  | [JSON](https://github.com/iearn-finance/itoken/blob/master/build/contracts/yUSDC.json) | [yusdcv3.iearn.eth](https://etherscan.io/address/0x26EA744E5B887E5205727f55dFBE8685e3b21951) |

## IyUSDC Interface

{% tabs %}
{% tab title="IyUSDC.sol" %}

```javascript
// Solidity Interface

interface IyUSDC {

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
