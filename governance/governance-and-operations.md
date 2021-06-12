# Governance and Operations

Since [YIP-61: Governance 2.0](https://gov.yearn.finance/t/yip-61-governance-2-0/10460) passed on April 25th, 2021, yearn began the transition into a **multi-DAO** structure, managed by **constrained delegation**. This approach allows protocol development to not be stiffened by bureaucracy while maintaining a sufficient level of decentralization. 

Multi-DAO refers to the fluid number of decentralized autonomous organizations (DAOs) that contribute to the protocol in some unique way. These independent groups consist of YFI holders, yTeams and the Multisig.

- **YFI holders** vote for changes to the protocol or the protocols governance structure
- **yTeams** focus on specific aspects of the protocol or relevant operations
- **Multisig** members execute or veto any on-chain decisions

Token holders have ultimate say over what yTeams exist, who is part of the Multisig, and the limitations of each group's operational control. The term 'constrained delgation' originates from token holders delegating specific powers to various groups that build and manage yearn.

A simplified flow of governance would look like this:

    1. YFI holders create, destroy and define limitations of yTeams 
    2. yTeam notifies yTx of a decision 
    3. yTx creates a delegated transaction and send it to the Multisig 
    4. Multisig executes or vetos the transaction
    
## DAO Responsibilities

![](https://i.imgur.com/IDysF5O.png)

### Token Holders 

it is the [YFI token](https://docs.yearn.finance/governance/yfi) holder's duty to create and vote for proposals that improve the protocol. 

| Proposals | Descriptions |
|-----------|--------------|
|Yearn Improvement Proposal (YIP)|A proposal to execute on any power delegated to YFI holders or outside the scope of enumerated powers|
|Yearn Delegation Proposal (YDP)|A proposal to change where any discrete decision-making power is delegated|
|Yearn Signaling Proposal (YSP)|A non-binding proposal to signal community feelings or intent on any issue|

Specifically, these proposals allow token holders to make the following decisions: 

| Power | Description |
|-------|-------------|
|Manage Powers|YFI holders can vote to create, assign, or revoke discrete powers to or from yTeams|
|Change YFI Token Contract|Any interaction with the YFI token contract, such as to mint YFI or burn the minting keys, remains under the control of YFI holders.|
|Set Fees|Set the standard fee structures in the Yearn Protocol|
|Change Multisig Signers|As the Multisig will continue to hold critical powers over the near term, only YFI holders can vote to change its signers|
|Ratify yTeams|Formally ratify or deratify yTeams to control which yTeams can hold delegated powers|
|Change yOps Signers|As yOps has the power to change signers of other yTeams, this is a special power to change the signers of yOps|
|Spend Treasury Funds|Spend funds from the treasury|
|YIP Power|YFI Holders have the power to propose a YIP on anything not already delegated|
### yTeams

Each yTeam has an objective and discrete powers which are defined by token holders. They can be broken further into membership pools, which are separate groups of contributors working towards similar goals as the overarching team. Additionally, one membership pool can bet a part of multiple yTeams.

| yTeam | Objective | Membership Pool |
|-------|-----------|-----------------|
|yGuard|Protect the vaults|YFI Protocol Dev, YFI Strategists, YFI Mechanics, YFI Secret Admirers|
|yBrain|Manage the strats|YFI Strategists|
|yDev|Manage the protocol|YFI Protocol Dev|
|yPeople|Curate the team|YFI Compensation Working Group, YFI Advisors|
|yBudget|Spend money well|YFI Finances, YFI Advisors|
|yFarm|Grow the treasury|YFI Secret Admirers, YFI Secret Entrance|
|yTx|Write transactions|YFI Doers|
|yOps|Coordinate contributors|YFI Ops|

Each yTeam is assigned specific decision-making powers, defined by YIP-61: 

| yTeam | Power | Description |
|-------|-------|-------------|
|yGuard|Emergency Powers|Immediately intervene in case of attack or bug to shutdown or rollback strategies or vaults|
|yBrain|Manage Strategies|Activate, deactivate, tune, and maintain strategies|
|yDev|Define Yearn Protocol|Decide what code is considered part of yearn and what isn’t|
|yDev|Manage Protocol|Maintain and improve the Yearn Protocol|
|yDev|Add Strategies|Add new strategies to vaults|
|yTx|Delegate Transactions|Create delegated transactions for the multisig to sign and execute|
|yPeople|Pay Team|Create, deploy, modify, or terminate Yearn compensation packages|
|yBudget|Set Budgets|Create budgets for coordinape, grants, hiring, operations, or other workstreams|
|yFarm|Farm Treasury|Farm with the treasury and make decisions on airdrops|
|yOps|Ratify yTeam Signers|Formally approve or remove signers for each yTeam|

### Multisig 

Decisions issued by yTeams will be executed on-chain by the Multisig until a more decentralized system is approved for implimentation. In the mean time, the [Multisig](https://docs.yearn.finance/resources/faq#who-is-on-the-multisig) controls the following:


| Power | Description |
|-------|-------------|
|Execution Power|The power to execute decisions made by YFI holders and yTeams on-chain|
|Veto Power|This power allows the Multisig to veto any decision and ideally should not be needed|
|Transitionary Power|A temporary power enabling the Multisig to operate under the mandate of YIP-41 until the set of decision-making powers covers all needed transactions|


## Future Implementations 

Yearn is continuously paving the way towards an ideal balance of DAO decentralization and productivity. The current phase of efforts impliment changes mostly on the social layer, and in the future we will be moving towards software implementations such as: 

- Multisig consensus mechanisms that allows each yTeam to have execution power 
- Move from proxy voting to on-chain voting
- tokenize decision-making powers as NFTs
- Utilize [Coordinape](https://coordinape.com/) for things like budget allocation and compensation