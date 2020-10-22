---
Status: In Research & Development
---

# StableCredit
StableCredit is an upcoming product in research & development that combines three pillars of existing DeFi infrastructure: 
<ul> 
  <li>Minting synthetic debt (DAI, Synthetix);</li>
  <li>Decentralized lending platform (Compound, AAVE);</li>
  <li>Automated Market Maker (AMM) functionality (Uniswap, Sushiswap).</li> 
</ul>

## Mechanics
StableCredit will enable users to deposit assets as collateral and obtain a line of credit (denominated in StableCredit USD) based on the dollar value of the assets at deposit. For example, a user can deposit 100 LINK and will obtain $1,100 worth of StableCredit USD (at the time of writing LINK is ~$11). StableCredit USD can then be traded for other assets available in the protocol. 

Exchange rates between StableCredit USD and assets in the protocol are determined by price feeds from oracles (Chainlink), and current utilization ratios of assets within the platform. For example, if liquidity providers have lent 100 DAI to the pool and 90 DAI is borrowed, the utilization ratio is 90%. Similar to how bonding curves work, there will then be a significant premium for any additional DAI borrowing (the cost to borrow DAI will be > $1). Users will be able to borrow up to 75% of the value of their collateral (i.e., utilization ratio of 75%). 

The AMM will also support single-sided liquidity exposure for liquidity providers (LPs). Current popular AMM models, such as Uniswap and Sushiswap, require LPs to deposit both assets in a liquidity pool. For example, in a ETH-USDC liquidity pool, the liquidity provider would be required to deposit ETH and USDC in a 50/50 ratio. This increases the barrier to entry for liquidity providers and also the capital requirements. Single-sided liquidity provisioning will enable LPs to deposit only one of the assets in the liquidity pool (i.e., either ETH or USDC). As a result, the barriers of entry to be a LP will be greatly reduced, and should contribute to an overall increase in capital efficiency.

## Summary
Users can: 
<ul>
  <li>Deposit collateral and obtain a line of credit (StableCredit USD);</li>
  <li>Borrow other assets with this line of credit (similar to Aave or Compound);</li>
  <li>Trade the asset borrowed for another asset in the pool (existing AMM functionality);</li>
</ul>


## Additional Learning Resources & Background
<ul>
  <li><a href="https://medium.com/iearn/introducing-stablecredit-a-new-protocol-for-decentralized-lending-stablecoins-and-amms-7252a43ee56">Initial Medium Post introducing StableCredit</a></li>
  <li><a href="https://twitter.com/finematics/status/1305188626008100865">Animation illustrating the mechanics of StableCredit</a></li>
  <li><a href="https://www.youtube.com/watch?v=SkTuMVBLBNQ&feature=youtu.be">Bankless video about StableCredit, featuring Andre Cronje</a></li>
  <li><a href="https://www.youtube.com/watch?v=bdC3rNDChbw&feature=youtu.be&t=2002">CODEUP 38 video about StableCredit, featuring Andre Cronje</a></li>   
 </ul>
