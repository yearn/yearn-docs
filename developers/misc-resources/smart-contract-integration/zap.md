# zap

| Contract            | ABI                                                                                               | Address                                                                                       |
| :------------------ | :------------------------------------------------------------------------------------------------ | :-------------------------------------------------------------------------------------------- |
| Uniswap_ETH_CDAIZAP | [JSON](https://github.com/iearn-finance/zap/blob/master/build/contracts/UniSwap_ETH_CDAIZap.json) | [zap.iearn.eth](https://etherscan.io/address/0xb82674cfa16bb28d9b70bec830ff24baec6b1337#code) |

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
