# imanage

| Contract      | ABI                                                                                                | Address                                                                                                   |
| :------------ | :------------------------------------------------------------------------------------------------- | :-------------------------------------------------------------------------------------------------------- |
| IIEarnManager | [JSON](https://github.com/iearn-finance/uniswap-roi/blob/master/build/contracts/IEarnManager.json) | [imanage.iearn.eth](https://etherscan.io/address/0x318135fbd0b40d48fcef431ccdf6c7926450edfb#readContract) |

## IIEarnManager Interface

{% tabs %}
{% tab title="IIEarnManager.sol" %}

```javascript
// Solidity Interface

interface IIEarnManager {

    function recommendSNX() public view returns (
      string memory choice,
      uint256 capr,
      uint256 iapr,
      uint256 aapr,
      uint256 dapr
    );
    function recommendUSDT() public view returns (
      string memory choice,
      uint256 capr,
      uint256 iapr,
      uint256 aapr,
      uint256 dapr
    );
    function recommendBAT() public view returns (
      string memory choice,
      uint256 capr,
      uint256 iapr,
      uint256 aapr,
      uint256 dapr
    );
    function recommendMKR() public view returns (
      string memory choice,
      uint256 capr,
      uint256 iapr,
      uint256 aapr,
      uint256 dapr
    );
    function recommendZRX() public view returns (
      string memory choice,
      uint256 capr,
      uint256 iapr,
      uint256 aapr,
      uint256 dapr
    );
    function recommendREP() public view returns (
      string memory choice,
      uint256 capr,
      uint256 iapr,
      uint256 aapr,
      uint256 dapr
    );
    function recommendKNC() public view returns (
      string memory choice,
      uint256 capr,
      uint256 iapr,
      uint256 aapr,
      uint256 dapr
    );
    function recommendWBTC() public view returns (
      string memory choice,
      uint256 capr,
      uint256 iapr,
      uint256 aapr,
      uint256 dapr
    );
    function recommendLINK() public view returns (
      string memory choice,
      uint256 capr,
      uint256 iapr,
      uint256 aapr,
      uint256 dapr
    );
    function recommendSUSD() public view returns (
      string memory choice,
      uint256 capr,
      uint256 iapr,
      uint256 aapr,
      uint256 dapr
    );
    function recommendDAI() public view returns (
      string memory choice,
      uint256 capr,
      uint256 iapr,
      uint256 aapr,
      uint256 dapr
    );
    function recommendETH() public view returns (
      string memory choice,
      uint256 capr,
      uint256 iapr,
      uint256 aapr,
      uint256 dapr
    );
    function recommendUSDC() public view returns (
      string memory choice,
      uint256 capr,
      uint256 iapr,
      uint256 aapr,
      uint256 dapr
    );

    function recommend(address _token) public view returns (
      string memory choice,
      uint256 capr,
      uint256 iapr,
      uint256 aapr,
      uint256 dapr
    );
}
```

{% endtab %}
{% endtabs %}
