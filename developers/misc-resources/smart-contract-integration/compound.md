# compound

| Contract | Address                                                                                                                    |
| :------- | :------------------------------------------------------------------------------------------------------------------------- |
| CDAI     | [0x5d3a536E4D6DbD6114cc1Ead35777bAB948E3643](https://etherscan.io/address/0x5d3a536E4D6DbD6114cc1Ead35777bAB948E3643#code) |
| CBAT     | [0x6C8c6b02E7b2BE14d4fA6022Dfd6d75921D90E4E](https://etherscan.io/address/0x6C8c6b02E7b2BE14d4fA6022Dfd6d75921D90E4E#code) |
| CETH     | [0x4Ddc2D193948926D02f9B1fE9e1daa0718270ED5](https://etherscan.io/address/0x4Ddc2D193948926D02f9B1fE9e1daa0718270ED5#code) |
| CREP     | [0x158079Ee67Fce2f58472A96584A73C7Ab9AC95c1](https://etherscan.io/address/0x158079Ee67Fce2f58472A96584A73C7Ab9AC95c1#code) |
| CSAI     | [0xF5DCe57282A584D2746FaF1593d3121Fcac444dC](https://etherscan.io/address/0xF5DCe57282A584D2746FaF1593d3121Fcac444dC#code) |
| CUSDC    | [0x39AA39c021dfbaE8faC545936693aC917d5E7563](https://etherscan.io/address/0x39AA39c021dfbaE8faC545936693aC917d5E7563#code) |
| CWBTC    | [0xC11b1268C1A384e55C48c2391d8d480264A3A7F4](https://etherscan.io/address/0xC11b1268C1A384e55C48c2391d8d480264A3A7F4#code) |
| CZRX     | [0xB3319f5D18Bc0D84dD1b4825Dcde5d5f7266d407](https://etherscan.io/address/0xB3319f5D18Bc0D84dD1b4825Dcde5d5f7266d407#code) |

## Compound Interface

{% tabs %}
{% tab title="Compound.sol" %}

```javascript
// Solidity Interface

interface Compound {
  function supply(address asset, uint amount) external returns (uint);
  function withdraw(address asset, uint requestedAmount) external returns (uint);
  function getSupplyBalance(address account, address asset) view external returns (uint);
  function supplyRatePerBlock() external view returns (uint);
  function mint(uint mintAmount) external returns (uint);
  function redeem(uint redeemTokens) external returns (uint);
  function balanceOf(address account) external view returns (uint);
}
```

{% endtab %}
{% endtabs %}
