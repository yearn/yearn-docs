---
description: Welcome to the Uniswap docs!
---

# Getting Started

Designed with simplicity in mind Uniswap provides an interface for seamless exchange of ERC20 tokens on Ethereum. By eliminating unnecessary forms of rent extraction and middlemen it allows faster, more efficient exchange. Where it makes tradeoffs, decentralization, censorship resistance, and security were prioritized. 

Uniswap is open source and functions as a public good. There is no central token or platform fee. No special treatment is given to early investors, adopters, or developers. Token listing is open and free. All smart contract functions are public and all upgrades are opt-in. 

This site will serve as a project overview for Uniswap - explaining how it works, how to use it, and how to build on top of it. These docs are actively being worked on and more information will be added soon.



## Uniswap V1 Features

* Add support for any ERC20 token using the Uniswap factory
* Join market making pools to collect fees on ETH-ERC20 pairs
* Liquidity-sensitive automated pricing using constant product formula
* Trade ETH for any ERC20 without wrapping
* Trade any ERC20 for any ERC20 in a single transaction 
* Lowest gas cost of any decentralized exchange
* Support for private and custom uniswap exchanges
* Buy ERC20 tokens from any wallet using ENS
* Partially verified smart contracts written in Vyper
* Mobile optimized open source frontend implementation  
* Funded through an Ethereum Foundation grant



### How it works

Uniswap is made up of a series of ETH-to-ERC20 exchange contracts. There is exactly one exchange contract per ERC20 token. If a token does not yet have an exchange it can be created by anyone using the Uniswap factory contract. The factory serves as a public registry and is used to look up all token and exchange addresses added to the system.

{% page-ref page="contract/vyper.md" %}

Each exchange contract holds a reserve of both ETH and its associated ERC20 token. Anyone can contribute to these reserves and become a liquidity provider on that exchange. Providing liquidity is different than buying or selling; it requires depositing an equivalent value of both ETH and the relevant ERC20 token to an exchange's reserves. Liquidity reserves are pooled across all providers on an exchange and an internal "pool token" \(also ERC20\) is used to track each providers relative contribution. Liquidity providers can burn their pool tokens at any time to remove their liquidity 

Users can trade between the two in either direction  



Anyone can contribute to these reserves of an exchange by depositing 



