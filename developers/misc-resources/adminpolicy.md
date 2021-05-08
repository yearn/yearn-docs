# Admin Access Policy

{% hint style="info" %}
These docs are still being worked on.
{% endhint %}

## v2 Yield Tokens

| Contract | ABI | Address |
| :--- | :--- | :--- |
| yDAIv2 | [JSON](https://github.com/yearn/itoken/blob/master/build/contracts/yDAI.json) | [ydaiv2.iearn.eth](https://etherscan.io/address/0x16de59092dAE5CcF4A1E6439D611fd0653f0Bd01#readContract) |
| yUSDCv2 | [JSON](https://github.com/yearn/itoken/blob/master/build/contracts/yUSDC.json) | [yusdcv2.iearn.eth](https://etherscan.io/address/0xd6aD7a6750A7593E092a9B218d66C0A814a3436e) |
| yUSDTv2 | [JSON](https://github.com/yearn/itoken/blob/master/build/contracts/yUSDT.json) | [yusdtv2.iearn.eth](https://etherscan.io/address/0x83f798e925BcD4017Eb265844FDDAbb448f1707D) |
| yTUSDv2 | [JSON](https://github.com/yearn/itoken/blob/master/build/contracts/yTUSD.json) | [ytusdv2.iearn.eth](https://etherscan.io/address/0x73a052500105205d34daf004eab301916da8190f) |

### yDAIv2

None ✅

### yUSDCv2

None ✅

### yUSDTv2

* set\_new\_APR ✅

```text
No interaction with funds.

APR used for stateless recommend() function. Can be used to change the recommended provider. The owner could replace the existing contract to a controlled contract that could suggest a specific lending provider.
```

* set\_new\_COMPOUND ⚠️

```text
Could access funds via malicious lending contract.

Sets the downstream address for Compound. The owner could replicate the compound mint() function call and force the APR change (with the vector mentioned in set_new_APR) and withdraw funds.

This method is implemented to allow adding Compound if they support the underlying token.
```

* set\_new\_DTOKEN ✅

```text
No interaction with funds.

Can only update the ID at dydx, no way to influence any other action.

This method is implemented to allow adding dYdX if they support the underlying token.
```

* set\_new\_FULCRUM ⚠️

```text
As per set_new_COMPOUND
```

### yTUSDv2

* set\_new\_APR ✅
* set\_new\_COMPOUND ⚠️
* set\_new\_DTOKEN ✅

## Utility Contracts

| Contract | ABI | Address |
| :--- | :--- | :--- |
| APROracle | [JSON](https://github.com/yearn/apr-oracle/blob/master/build/contracts/APROracle.json) | [apr.iearn.eth](https://etherscan.io/address/0x97ff4a1b787ade6b94cca95b61f79417c673331d#code) |
| UniswapROI | [JSON](https://github.com/yearn/uniswap-roi/blob/master/build/contracts/UniswapROI.json) | [uniroi.iearn.eth](https://etherscan.io/address/0xd04ca0ae1cd8085438fdd8c22a76246f315c2687#readContract) |
| UniswapAPR | [JSON](https://github.com/yearn/uniswap-roi/blob/master/build/contracts/UniswapAPR.json) | [uniapr.iearn.eth](https://etherscan.io/address/0x4c70D89A4681b2151F56Dc2c3FD751aBb9CE3D95#readContract) |
| APRWithPoolOracle | [JSON](https://github.com/yearn/apr-oracle/blob/master/build/contracts/APRWithPoolOracle.json) | [apradj.iearn.eth](https://etherscan.io/address/0xAE8F37F0e8AD690486bFA2495113d7E94B7a7Ba6#code) |
| IEarnAPRWithPool | [JSON](https://github.com/yearn/uniswap-roi/blob/master/build/contracts/IEarnAPRWithPool.json) | [iapradj.iearn.eth](https://etherscan.io/address/0xcD5F61c392B61F440991DEf98FF6Af07FC6900D4#readContract) |

### IEarnAPRWithPool

```text
No interaction with funds.

APR used for stateless recommend() function. Can be used to change the recommended provider. The owner could influence the calculation to a specific lending provider.
```

* addAToken ✅
* addAUniToken ✅
* addCToken ✅
* addDToken ✅
* addIToken ✅
* addPool ✅
* addYToken ✅
* set\_new\_APR ✅
* set\_new\_UNI ✅
* set\_new\_UNIAPR ✅
* set\_new\_UNIROI ✅

### APRWithPoolOracle

```text
No interaction with funds.

APR used for stateless recommend() function. Can be used to change the recommended provider. The owner could influence the calculation to a specific lending provider.
```

* set\_new\_AAVE ✅
* set\_new\_DDEX ✅
* set\_new\_DYDX ✅
* set\_new\_Modifier ✅
* set\_new\_Ratio ✅
* set\_new\_blocksPerYear ✅

### UniswapROI

None ✅

### UniswapAPR

```text
No interaction with funds.
```

* set\_new\_blocksPerYear ✅

## Lending Providers

* [compound.finance](http://compound.finance/)
* [aave.com](http://aave.com/)
* [ddex.io](https://ddex.io/)
* [dydx.exchange](http://dydx.exchange/)
* [fulcrum.trade](http://fulcrum.trade/)

