# ईयर का उपयोग करना       

'ज़ैप' नामक एक विशेषता के कारन, लगभग कोईी भी टोकन को किसी भी तिजोरी में जमा करना बेहद आसान है। 

ये काम कैसे करता है : 

सबसे पहले, ऊपरी दाएं कोने में स्थित बटन का उपयोग करके **अपना बटुआ जुडिये**। कई प्रकार के बटुवे  समर्थित हैं, लेकिन अधिकांश लोग [मेटामास्क] (https://metamask.io/) का उपयोग करते हैं, जिसे क्रोम एक्सटेंशन के रूप में या ऐप्पल और एंड्रॉइड ऐप दुकान के माध्यम से मुफ्त में डाउनलोड किया जा सकता है। सुनिश्चित करें कि आपका वॉलेट एथेरियम नेटवर्क से जुड़ा है।

<p align="center">
  <img width="1266.75" height="345.75" src="https://i.imgur.com/H0Uc8e8.png">
</p>

## यदि आपके पास उस तिजोरी के लिए **पहले से ही आवश्यक टोकन** है, जिसमें आप जमा करना चाहते हैं तो:

1. उस तिजोरी का चयन करें जिसमें आप टोकन जमा करना चाहते हैं।
2. टोकन की राशि दर्ज करें जिसे आप तिजोरी में जमा करना चाहते हैं। यदि आप ईटीएच(ETH) जमा कर रहे हैं, तो सुनिश्चित करें कि आपके पास भविष्य के लेन-देन के भुगतान करने के लिए पर्याप्त ईटीएच(ETH) बचा है जो आपको करने की आवश्यकता हो सकती है।

<p align="center">
  <img width="914.26" height="360.75" src="https://i.imgur.com/LGdRAMQ.png">
</p>

3. 'स्वीकृति' या 'जमा' बटन पर क्लिक करें, यह इस पर निर्भर करता है कि आपने पहले स्वीकृत किया है या नहीं 
4. आपका वॉलेट आपसे लेनदेन की पुष्टि करने के लिए कहेगा। इसमें लगभग ३ मिनट का समय लगेगा, लेकिन आप [नेटवर्क को अधिक गैस शुल्क देकर] इसे गति दे सकते हैं।(https://blog.leverj.io/how-to-set-the-gas-limit-and-gas-price-in-metamask-1b33c38c32fd). यदि आपका लेन-देन अटक जाता है, तो [यह मार्गदर्शिका] देखें(https://metamask.zendesk.com/hc/en-us/articles/360015489251-How-to-Speed-Up-or-Cancel-a-Pending-Transaction) लेन-देन में तेजी लाने या रद्द करने पर।

<p align="center">
  <img width="258.75" height=" 459.75" src="https://i.imgur.com/BkXBANS.png">
</p>

6. When your transaction succeeds, you will see your deposited balance in the vault's interface, which should appear at the top of the vault list.

<p align="center">
  <img width="928.5" height="93.75" src="https://i.imgur.com/JvNQ3l2.png">
</p>

When you're ready to withdraw: 

1. Select the vault that you would like to withdraw from.
2. Enter the amount you want to withdraw, or click 'Max' to withdraw the entire balance.

<p align="center">
  <img width="910.5" height="361.5" src="https://i.imgur.com/Y3NsCRb.png">
</p>

3. Click 'Withdraw'
4. Your wallet will ask you to confirm the transaction. See step 4 above for more details. 
5. When your transaction succeeds, the tokens will show up in your wallet again

## If you **don't have the required token** for the vault that you would like to deposit in:

This can be a common occurrence, because many of Yearn's vaults generate yield by using [Curve Finance](http://curve.finance/) liquidity provider (LP) tokens, which are acquired through depositing into a Curve pool. 

So for instance, if you would rather deposit into the crvSTETH vault instead of the ETH vault, and accept the additional risk that comes with the curve pool and an ETH derivative (stETH) in return for higher yield, but you only have ETH in your wallet, your ETH will need to be converted to a crvSTETH token before it is accepted in the vault. 

Thankfully, due to Yearn's 'zap' feature, this can all be done in the same transaction as your deposit. Here's how it works using the crvSTETH vault as an example:

**NOTE:** Zapping a token into a vault will require more transactions than depositing the native token. This means you will be paying more in gas and potentially lose value to slippage when the token is swapped or deposited into a pool. Yearn limits slippage to 1% and the transaction will fail if slippage exceeds that, in which case you will have to swap or deposit the tokens manually. See our [zap](https://docs.yearn.finance/yearn-finance/yvaults/overview#zap-in-with-any-asset) section for more details.

1. Select the crvSTETH vault
2. Click the dropdown box by the 'Approve' or 'Deposit' button 
3. Select which token you would like to be converted into crvSTETH. It will only display the tokens that are in your wallet.

<p align="center">
  <img width="909" height="363" src="https://i.imgur.com/6K1luO7.png">
</p>

4. Enter the amount of tokens you would like to deposit and click 'Approve' or 'Deposit' depending on whether or not you have previously approved the token. 
4. Confirm the transaction through your wallet. See step 4 in the section above for more details. 
5. When your transaction succeeds, you will see your deposited balance in the vault's interface, which should appear at the top of the vault list.

When you're ready to withdraw: 

1. Select the crvSTETH vault
2. Click the dropdown box by the 'Withdraw' button

<p align="center">
  <img width="915.75" height="600.75" src="https://i.imgur.com/2UyXKN0.png">
</p>

3. Select which asset you would like to receive upon withdrawal. Your options will be the crvSTETH, ETH, BTC, DAI, USDC or USDT
3. Enter the amount you want to withdraw, or click 'Max' to withdraw the entire balance.
4. Confirm the approval if needed, and then approve the withdrawal transaction.
5. When your transaction succeeds, the tokens will show up in your wallet again

## Tools to track your funds 

If you would like to see how your USD balance changes while your assets are in a vault, connect your wallet to [zapper.fi](https://zapper.fi) or a similar portfolio tracking product.This is also the easiest way to tell how much profit the vault has made for you. 

Your balance WILL NOT increase continuously. Profit will be distributed to your share of the vault when the harvest() function is called, which happens on a fluctuating basis. 

Community resources to monitor your returns:

- [Zapper](https://zapper.fi/)
- [Zerion](https://app.zerion.io/)
- [Yearn Vault ROI Calculator](https://yearn-roi.xyz/#/)
- [yVault ROI](https://yvault-roi.netlify.app/)
- [https://trackavault.com/](https://trackavault.com/)
