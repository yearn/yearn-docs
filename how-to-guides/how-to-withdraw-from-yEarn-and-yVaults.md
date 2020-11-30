# How to withdraw from yVaults

This is a simple process similar to sending a transaction with your wallet. You will need to define an amount and approve the trasaction.
Remember to check the gas fees to make sure you transaction will not fail and you are aware of the transaction costs.
For this guide, we will use the [curve.fi/y LP](https://www.curve.fi/iearn/) yVault.

## Visual Walkthrough

1\) Go to [Vaults page](https://yearn.finance/vaults) and click on “Connect your wallet”
- Once you've connected your wallet the website will display the balance you have desposited in each vault.
- Scroll down through the page and click on the yVault you want to withdraw your funds from.

![](https://i.imgur.com/DzylU6s.png)

2\) Define how much you want to withdraw

![](https://i.imgur.com/69A6y2Q.png)

- You can choose through the UI the percentage you want to withdraw as highlighted in the screenshot above. You can also introduce in the input field the amount you prefer. Alternatively, you can click on "Withdraw All" which will trigger your wallet to start the transaction approval process in just 1 click. 

3\) What do you get?
- You will get back into your wallet the unwrapped token you originally deposited (DAI).
- The amount of tokens you will receive can differ from the amount displayed by the UI. This is due to the 0.5% withdrawal fee which can be applied to the amount to be withdrawn.

### WAIT! What is this 0.5% fee?
- Andre explains it pretty well [here](https://www.youtube.com/watch?v=bdC3rNDChbw&feature=youtu.be&t=637) and [here](https://www.youtube.com/watch?v=bdC3rNDChbw&feature=youtu.be&t=1254)
- The 0.5% withdrawal fee is applied to certain vaults only and, for these vaults, it is not applied to all withdrawals.
- The 0.5% withdrawal fee was created to create a "buffer" (idle) fund inside the yVault. 
- This buffer is applied to subsidize small withdrawals costs:
    - If your withdrawal is smaller than the current vault's buffer, then your tokens will come from the buffer inside the vault. 
    - If your withdrawal is bigger than the buffer, then the vault's strategy will need to move the funds from the third-party platforms in order to give you your tokens. In this case, you need to pay the 0.5% withdrawal fee. 
- Find [how to calculate the current vault's buffer](https://docs.yearn.finance/faq#what-are-the-fees) (idle funds).
- Since the complecity of the transaction is bigger when the withdraw fee is paid compared with when it's not, this might result in very different gas fee paid. As reference, here is a table with the estimate cost in gas of withdrawing from any yVault with the active strategies up to this date (21/11/2020):

![](https://i.imgur.com/ZN15p1S.png)

4\) Check that you received your tokens
- Click Withdraw button, approve the transaction through your wallet and check if transaction succeeds in etherscan.
- Once transaction succeeds, then refresh the yVault page.
- The yVault should be displaying updated values based on your decision.
- Your wallet should display the right amount of tokens.

