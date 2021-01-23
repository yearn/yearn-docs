# Integration Guide

## Integration Points

- [Vault Registry](integration-guide.md#Vault-Registry)
- [Subgraph](integration-guide.md#Subgraph)
- [API](integration-guide.md#API)

### Vault Registry <a id="Vault-Registry"></a>

The Yearn Vault Registry \(aka yRegistry\) is a smart contract deployed on the ethereum mainnet. The Vault Registry is the single source of truth for active Yearn vaults. The registry allows users to query for active Yearn vaults and vault metadata \(see "[available data](integration-guide.md#Vault-Registry-Available-Data)" below\).

#### Details

- Currently vaults are added manually by Yearn governance.
- In the future the vault registry may be integrated into the vault lifecycle \(meaning new vaults would get added into the registry during their deployment process\).

#### Interact

- ENS: [registry.ychad.eth](https://etherscan.io/enslookup-search?search=registry.ychad.eth)
- Address: [0x3ee41c098f9666ed2ea246f4d2558010e59d63a0](https://etherscan.io/address/0x3ee41c098f9666ed2ea246f4d2558010e59d63a0#readContract)

#### Code

- [https://github.com/iearn-finance/yearn-protocol/blob/develop/contracts/registries/YRegistry.sol](https://github.com/iearn-finance/yearn-protocol/blob/develop/contracts/registries/YRegistry.sol)

#### Available data <a id="Vault-Registry-Available-Data"></a>

- Vault addresses \(methods: `getVaults`\).
- Active controller address per vault \(methods: `getVaultInfo`, `getVaultsInfo`\).
- Active strategy address per vault \(methods: `getVaultInfo`, `getVaultsInfo`\).
- Vault type \(normal, wrapped, delegated\) \(methods: `isDelegated`, `isWrapped`\).
- Governance address \(methods: `governance`\).

#### Integrations

- Yearn API - utilizes vault registry as the single source of truth in many API calls.

#### Future Integrations

- Yearn Subgraph - in the future we would like the Yearn subgraph to index new vaults automatically using the Vault registry. In order to accomplish this the vault registry must first be incorporated into the vault lifecycle.

### Subgraph <a id="Subgraph"></a>

The Yearn Subgraph is a GraphQL-based public API running on [The Graph](https://thegraph.com) that can be utilized to extract current and historical data from the Yearn ecosystem.

#### Details

- See [README](https://github.com/juanmardefago/subgraph-y/blob/master/README.md) for detailed integration details.

#### Interact

- [Graph Explorer](https://thegraph.com/explorer/subgraph/iearn-finance/yearn-finance)

#### Code

- [Github](https://github.com/juanmardefago/subgraph-y)

#### Available data

- Vault snapshot \(current contract values\).
- Vault metrics per vault \(net deposits, withdrawals, transfers, earnings, etc.\).
- Vault metrics per user \(net deposits, withdrawals, transfers, earnings, etc.\).
- Active controller address per vault.
- Active strategy address per vault.
- Historical harvest events and earnings.

#### Integrations

**Examples of projects using the Yearn Subgraph**

| Link                                                             | Code                                                                                   | By                                                                                                                       |
| :--------------------------------------------------------------- | :------------------------------------------------------------------------------------- | :----------------------------------------------------------------------------------------------------------------------- |
| [https://yearn.tools](https://yearn.tools)                       | [https://github.com/yearn-integrations/api](https://github.com/yearn-integrations/api) | [x48](https://twitter.com/x48_crypto), [Lucinao](https://twitter.com/lbertenasco), [Graham](https://twitter.com/grahamu) |
| [https://yvault-roi.netlify.app](https://yvault-roi.netlify.app) | [https://github.com/rrridges/yvault-roi](https://github.com/rrridges/yvault-roi)       | [Matt Ridges](https://twitter.com/rrridges)                                                                              |
| [https://www.yfistats.com](https://www.yfistats.com)             |                                                                                        | [Bob_The_Builder](https://twitter.com/Bob_The_Buidler)                                                                   |

### API <a id="API"></a>

Yearn API is a collection of Serverless API endpoints focused on Yearn integrations.

#### Details

**Goals**

- Provide free API endpoints to simplify 3rd party integration with Yearn.
- Provide an "API playground" \(Swagger UI\) anyone can use to quickly browse and test available APIs.
- Document all existing APIs.
- Allow the entire API stack to be forked to enable community involvement in API development.

**Data Sources**

- Vault Registry - Yearn API utilizes the vault registry in a number of endpoints to maintain a list of active vaults.
- Subgraph - Yearn API utilizes the Yearn Subgraph for various metrics endpoints.

#### Interact

- Yearn API Playground \(Swagger UI\): [https://yearn.tools](https://yearn.tools).

#### Code

- [Github](https://github.com/yearn-integrations/api)

#### Available data

- Current vault snapshots.
- Vault listings from vault registry \(with injected strategy/controller/token metadata\).
- Vault metrics per user \(net deposits, withdrawals, transfers, earnings, etc.\).
- Vault transactions per user.
- Vault APY data.

#### Integrations

**Examples of projects using the API**

| Link                                                     | Code                                                                                             | By                                        |
| :------------------------------------------------------- | :----------------------------------------------------------------------------------------------- | :---------------------------------------- |
| [https://yearn.finance](https://yearn.finance)           | [https://github.com/iearn-finance/iearn-finance](https://github.com/iearn-finance/iearn-finance) | [Yearn](https://twitter.com/iearnfinance) |
| [https://yearn.party](https://yearn.party)               | [https://github.com/x48-crypto/yearn-party](https://github.com/x48-crypto/yearn-party)           | [x48](https://twitter.com/x48_crypto)     |
| [https://feel-the-yearn.app](https://feel-the-yearn.app) |                                                                                                  | [Graham](https://twitter.com/grahamu)     |
