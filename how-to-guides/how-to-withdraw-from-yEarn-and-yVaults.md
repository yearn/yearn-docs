# How to withdraw from yVaults

This is a simple process similar to sending a transaction with your wallet. You will need to define an amount and approve the transaction.

Remember to check the gas fees to ensure your transaction will not fail and you are aware of the transaction costs.

For the purpose of this guide, we will use the [curve.fi/y LP](https://www.curve.fi/iearn/) yVault as an example.

## Visual Walkthrough

1. Go to [Vaults page](https://yearn.finance/vaults) and click on “Connect your wallet”.

   - Once you've connected your wallet, the website will display the balance you have deposited in each vault.
   - Scroll down through the page and click on the yVault you want to withdraw your funds from.

     ![](https://i.imgur.com/DzylU6s.png)

1. Enter the amount you wish to withdraw:

   ![](https://i.imgur.com/69A6y2Q.png)

   - You can choose from pre-defined percentages of your available balance, or enter a specific amount Alternatively, you can click on "Withdraw All" to trigger your wallet to start the transaction approval process for the full available amount in just one click.

1. Complete the transaction:
   - Click the Withdraw button, approve the transaction in your wallet, and wait for the transaction to complete successfully.
   - Once completed, your wallet should contain your tokens.
   - Refreshing the Yearn vaults page, the yVault should be displaying updated values accordingly.
1. In your wallet you will then have received:
   - The unwrapped token you originally deposited (in this example DAI).
   - The actual token amount received may differ from the amount displayed in the UI, due to the 0.5% withdrawal fee which may be applied.

### WAIT! What is this 0.5% fee?

- Andre explains it pretty well [here](https://www.youtube.com/watch?v=bdC3rNDChbw&feature=youtu.be&t=637) and [here](https://www.youtube.com/watch?v=bdC3rNDChbw&feature=youtu.be&t=1254).
- The 0.5% withdrawal fee is only applied to certain vaults, and not to all withdrawals from those vaults.
- There is a "buffer" (idle) fund inside these vaults. This buffer is used to for efficient handling of smaller sized withdrawals:
  - If your withdrawal is smaller than the vault's current buffer, then your tokens will come from the buffer inside the vault, and no fee will be applied.
  - If your withdrawal is larger than the buffer, then the vault's strategy will be required to request funds from the Strategy in order to perform the withdrawal. In this case, the 0.5% withdrawal fee is applied.
  - Also see: [How to calculate the current vault's buffer](https://docs.yearn.finance/faq#what-are-the-fees) (idle funds).
- When the withdrawal fee is applied, the complexity of the transaction is larger, which has an impact on gas used. This may result in different gas fees. As a reference, below is a table with the estimated gas cost associated with withdrawing from vaults as per the time of this writing:

  ![](https://i.imgur.com/ZN15p1S.png)
