---
description: Welcome to the Uniswap docs!
---

# Getting Started

Designed with simplicity in mind Uniswap provides an interface for seamless exchange of ERC20 tokens on Ethereum. By eliminating unnecessary forms of rent extraction and middlemen it allows faster, more efficient exchange. Where it makes tradeoffs, decentralization, censorship resistance, and security are prioritized. 

Uniswap is open source and functions as a public good. There is no central token or platform fee. No special treatment is given to early investors, adopters, or developers. Token listing is open and free. All smart contract functions are public and all upgrades are opt-in. 

This site will serve as a project overview for Uniswap - explaining how it works, how to use it, and how to build on top of it. These docs are actively being worked on and more information will be added soon.

## Uniswap V1 Features

* Add support for any ERC20 token using the Uniswap factory
* Join market making pools to collect fees on ETH-ERC20 pairs
* Liquidity-sensitive automated pricing using constant product formula
* Trade ETH for any ERC20 without wrapping
* Trade any ERC20 for any ERC20 in a single transaction 
* Trade and transfer to a different address in a single transaction
* Lowest gas cost of any decentralized exchange
* Support for private and custom uniswap exchanges
* Buy ERC20 tokens from any wallet using ENS
* Partially verified smart contracts written in Vyper
* Mobile optimized open source frontend implementation  
* Funded through an Ethereum Foundation grant

## How it works

Uniswap is made up of a series of ETH-ERC20 exchange contracts. There is exactly one exchange contract per ERC20 token. If a token does not yet have an exchange it can be created by anyone using the Uniswap factory contract. The factory serves as a public registry and is used to look up all token and exchange addresses added to the system.

Each exchange holds a reserve of both ETH and its associated ERC20 token. Anyone can contribute to these reserves and become a liquidity provider on that exchange. Providing liquidity is different than buying or selling; it requires depositing an equivalent value of both ETH and the relevant ERC20 token into an exchange's reserves. Reserves are pooled across all providers and an internal "pool token" \(ERC20\) is used to track each providers relative contribution. Providers can burn their pool tokens at any time to withdraw a proportional share of the liquidity reserves. 

Exchange contracts are automated market makers between ETH and their associated ERC20 token. Traders can swap between ETH and ERC20 tokens in either direction by adding to the liquidity reserves of one and withdrawing from the liquidity reserves of the other. The exchange rate is set using the "constant product" market making formula. This formula automatically adjusts the exchange rate based off of the relative size of their reserves and the size of the incoming trade. For example, an ETH-to-ERC20 trade increases the size of the ETH reserve and lowers the size of the ERC20 reserve. This causes a shift in the reserve ratio, increasing the ERC20 token's price relative to ETH. A small liquidity provider fee \(0.3%\) is taken out of each trade and added to the reserves. This increases reserve sizes by 0.3% of trade volume adding to the value of pool tokens. This splits fees among liquidity providers proportional to their reserve contribution.





