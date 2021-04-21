# Yearn and Curve Synergy

One of the critical components of Yearn’s infrastructure includes a collaborative relationship with [Curve.fi](http://curve.fi/). Several Yearn vaults provide liquidity into Curve pools and stake the liquidity provider \(LP\) tokens into the respective gauges, earning CRV rewards. Yearn locks 10% of all CRV rewards earned into the yveCRV-DAO vault \(“Backscratcher”\) to obtain an additional amount of CRV. In the strategy descriptions which follow, vaults that are boosted are indicated with a 🚀.

For a deeper understanding, refer to the _Understanding Curve Boost Multipliers_ section near the end of this document.

Furthermore, the remaining 90% of the CRV earned are swapped into the respective LP tokens, and re-deposited into the vault. The only exception is the yvUSDN3Crv vault that locks 50% of the CRV earned into the Backscratcher vault and swaps the remaining 50%.





