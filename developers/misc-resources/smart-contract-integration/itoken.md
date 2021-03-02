# itoken

| Contract | ABI                                                                                     | Address                                                                                        |
| :------- | :-------------------------------------------------------------------------------------- | :--------------------------------------------------------------------------------------------- |
| iEther   | [JSON](https://github.com/iearn-finance/itoken/blob/master/build/contracts/IEther.json) | [ieth.iearn.eth](https://etherscan.io/address/0x9dde7cdd09dbed542fc422d18d89a589fa9fd4c0#code) |

## iToken Interface

{% tabs %}
{% tab title="IIEther.sol" %}

```javascript
// Solidity Interface

interface IIEther {
  // Invest ETH
  function invest() external payable;
  function calcPoolValueInETH() external view returns (uint);
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
