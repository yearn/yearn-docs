# interface

| Contract            | ABI                                                                                               | Address                                                                                                                    |
| :------------------ | :------------------------------------------------------------------------------------------------ | :------------------------------------------------------------------------------------------------------------------------- |
| APROracle           | [JSON](https://github.com/iearn-finance/apr-oracle/blob/master/build/contracts/APROracle.json)    | [apr.iearn.eth](https://etherscan.io/address/0x97ff4a1b787ade6b94cca95b61f79417c673331d#code)                              |
| Uniswap_ETH_CDAIZAP | [JSON](https://github.com/iearn-finance/zap/blob/master/build/contracts/UniSwap_ETH_CDAIZap.json) | [0xB82674CfA16bb28D9b70bEC830fF24BAEC6B1337](https://etherscan.io/address/0xb82674cfa16bb28d9b70bec830ff24baec6b1337#code) |
| iEther              | [JSON](https://github.com/iearn-finance/itoken/blob/master/build/contracts/IEther.json)           | [0x9Dde7cdd09dbed542fC422d18d89A589fA9fD4C0](https://etherscan.io/address/0x9dde7cdd09dbed542fc422d18d89a589fa9fd4c0#code) |

## APR Interface

{% tabs %}
{% tab title="IAPROracle.sol" %}

```javascript
// Solidity Interface

interface IAPROracle {
  function recommendDAI() external view returns (string memory);
  function recommendETH() external view returns (string memory);
  function recommendUSDC() external view returns (string memory);
  function getAllCompoundAPR()
      external
      view
      returns (
          uint256 cDAI,
          uint256 cBAT,
          uint256 cETH,
          uint256 cREP,
          uint256 cSAI,
          uint256 cUSDC,
          uint256 cWBTC,
          uint256 cZRC
      );

  // Compound
  function getCDAIAPR() external view returns (uint256);
  function getCBATAPR() external view returns (uint256);
  function getCETHAPR() external view returns (uint256);
  function getCREPAPR() external view returns (uint256);
  function getCSAIAPR() external view returns (uint256);
  function getCUSDCAPR() external view returns (uint256);
  function getCWBTCAPR() external view returns (uint256);
  function getCZRCAPR() public view returns (uint256);
  function getCompoundAPR(address token) public view returns (uint256);

  function getAllDyDxAPR()
      external
      view
      returns (
          uint256 dSAI,
          uint256 dETH,
          uint256 dUSDC,
          uint256 dDAI
      );

  // dYdX
  function getDyDxSAIAPR() public view returns(uint256);
  function getDyDxETHAPR() public view returns(uint256);
  function getDyDxUSDCAPR() public view returns(uint256);
  function getDyDxDAIAPR() public view returns(uint256);

  function getAllFulcrumAPR()
      external
      view
      returns (
          uint256 iZRX,
          uint256 iREP,
          uint256 iKNC,
          uint256 iWBTC,
          uint256 iUSDC,
          uint256 iETH,
          uint256 iSAI,
          uint256 iDAI,
          uint256 iLINK,
          uint256 iSUSD
      );

  // Fulcrum
  function getIZRXAPR() public view returns (uint256);
  function getIREPAPR() public view returns (uint256);
  function getIKNCAPR() public view returns (uint256);
  function getIWBTCAPR() public view returns (uint256);
  function getIUSDCAPR() public view returns (uint256);
  function getIETHAPR() public view returns (uint256);
  function getISAIAPR() public view returns (uint256);
  function getIDAIAPR() public view returns (uint256);
  function getILINKAPR() public view returns (uint256);
  function getISUSDAPR() public view returns (uint256);

  function getFulcrumAPR(address token) public view returns(uint256);

  function getDyDxAPR(uint256 marketId) public view returns(uint256);

  function getAllAaveAPR()
      external
      view
      returns (
          uint256 aDAI,
          uint256 aTUSD,
          uint256 aUSDC,
          uint256 aUSDT,
          uint256 aSUSD,
          uint256 aBAT,
          uint256 aETH,
          uint256 aLINK,
          uint256 aKNC,
          uint256 aREP,
          uint256 aZRX,
          uint256 aSNX
      );

  function getADAIAPR() public view returns (uint256);
  function getATUSDAPR() public view returns (uint256);
  function getAUSDCAPR() public view returns (uint256);
  function getAUSDTAPR() public view returns (uint256);
  function getASUSDAPR() public view returns (uint256);
  function getALENDAPR() public view returns (uint256);
  function getABATAPR() public view returns (uint256);
  function getAETHAPR() public view returns (uint256);
  function getALINKAPR() public view returns (uint256);
  function getAKNCAPR() public view returns (uint256);
  function getAREPAPR() public view returns (uint256);
  function getAMKRAPR() public view returns (uint256);
  function getAMANAAPR() public view returns (uint256);
  function getAZRXAPR() public view returns (uint256);
  function getASNXAPR() public view returns (uint256);
  function getAWBTCAPR() public view returns (uint256);

  function getAaveAPR(address token) public view returns (uint256);
}
```

{% endtab %}
{% endtabs %}

## ZAP Interface

{% tabs %}
{% tab title="IUniSwap\_ETH\_CDAIZap.sol" %}

```javascript
// Solidity Interface

interface IUniSwap_ETH_CDAIZap {
    function getExpectedReturn(uint256 eth) external view returns (uint256);
    function LetsInvest(address _towhomtoissue, uint256 _minReturn) external payable returns (uint);
    function getUniswapExchangeContractAddress() external view returns (address);
    function Redeem(address payable _towhomtosend, uint256 _amount) external stopInEmergency returns (uint);
    function getMaxTokens(address _UniSwapExchangeContractAddress, IERC20 _ERC20TokenAddress, uint _value) external view returns (uint);
    function getEthBalance(address _UniSwapExchangeContractAddress) external view returns (uint);
    function getTokenReserves(address _UniSwapExchangeContractAddress, IERC20 _ERC20TokenAddress) external view returns (uint);
    function getTotalShares(address _UniSwapExchangeContractAddress) external view returns (uint);
    function getReturn(address _UniSwapExchangeContractAddress, IERC20 _ERC20TokenAddress, uint _value) external view returns (uint, uint, uint);
    function calcReturnETHFromShares(uint _value) external view returns (uint, uint, uint);
    function uniBalanceOf(address _owner) external view returns (uint);
    function cBalanceOf(address _owner) external view returns (uint);
    function calcReturnSharesFromETH(uint _value) external view returns (uint);
    function getTokenToEthOutputPrice(uint _tokens) external view returns (uint);
    function getSharesReturn(address _UniSwapExchangeContractAddress, IERC20 _ERC20TokenAddress, uint _ethValue) external view returns (uint);
}
```

{% endtab %}
{% endtabs %}

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
