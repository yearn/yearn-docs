# Using Yearn
Depositing into Yearn Vaults can be done in a few steps. In the guide below, the DAI v2 vault will be used as an example.
### Connecting Your Wallet
The easiest way to use Yearn is through Metamask. Connect your Metamask wallet by clicking *Connect Wallet* on the top right corner, and then selecting Metamask. Your wallet will be shown as connected when the *Connect Wallet* button shows a green dot and your wallet address. The UI will automatically detect tokens in your wallet address and their amounts.
### Your First Deposit
Before depositing in any of the vaults, an approval transaction must be done to allow vault smart contracts to spend your tokens. This is the first of two transactions, with the second being the actual deposit, transferring your tokens to the vault. Note that unless you are confident in altering the spend approval amount, this defaults to infinity and only needs to be done once per smart contract, making any subsequent deposits not need approval transactions. The *Deposit* button will show as *Approve* if your connected wallet address has not yet made an approval transaction for your selected token.

![](https://i.imgur.com/eXGp2nN.png)
- Look for the DAI v2 vault from the list of vaults on the [Yearn.Finance](https://yearn.finance/vaults/) website.
- Click it to show the deposit interface.
- Enter an amount or click *Max*.
- Click *Approve*

A Metamask window will pop up for you to confirm the approval transaction.

![](https://i.imgur.com/n6wqqND.png)

- Click *Confirm* and wait for the transaction to be confirmed.

Another Metamask window will pop up automatically for you to confirm the deposit transaction.

![](https://i.imgur.com/DqAQuzm.png)

- Click *Confirm* and wait for the transaction to be confirmed.

Your deposit is now complete. This will be represented by [ytokens](https://docs.yearn.finance/yearn-finance/yvaults/vault-tokens) in your wallet address. You may track your deposit on [Zapper.fi](https://zapper.fi), [Zerion.io](https://app.zerion.io), and [Trackavault](https://trackavault.com) among many others.

### Withdrawal
Withdrawal can be done on the same interface. It is right below the deposit form.
- Select an amount to withdraw, or click *Max*.
- Click *Withdraw* and wait for the transaction to be confirmed.

Your withdrawal is now complete.

### Zaps
*Zap* is the term used for multiple actions combined and executed in one transaction. An example of this would be swapping ETH to DAI then depositing that DAI in the DAI v2 vault all in one transaction, instead of having to swap and deposit separately. With the recent Zapper.fi integration, all vaults can now be zapped into and out of from any ERC20 token in your wallet address.
