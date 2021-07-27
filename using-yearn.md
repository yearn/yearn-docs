## Verwendung von Yearn 
Dank einer Funktion namens "zap" ist es extrem einfach, mit fast jedem Token in einen beliebigen Vault einzuzahlen.

So funktioniert es:
**Verbinde zunächst dein Wallet** über den Button oben rechts. Mehrere Arten von Wallets werden unterstützt, aber die meisten Leute verwenden [MetaMask](https://metamask.io/), die kostenlos als Chrome-Erweiterung oder über die Apple und Android App Stores heruntergeladen werden kann. Stelle sicher, dass dein Wallet mit dem Ethereum-Netzwerk verbunden ist.

<p align="center">
  <img width="1266.75" height="345.75" src="https://i.imgur.com/H0Uc8e8.png">
</p>

## Wenn du bereits den erforderlichen Token für den Vault besitzt, in den du einzahlen möchtest:

1\. Wähle den Vault aus, in den du einzahlen möchtest.
 
2\. Gib die Menge an Token ein, die du in den Vault einzahlen möchtest. Wenn du ETH einzahlst, vergewissere dich, dass du genug ETH übrig hast, um für zukünftige Transaktionen zu bezahlen, die du eventuell durchführen musst

<p align="center">
  <img width="914.26" height="360.75" src="https://i.imgur.com/LGdRAMQ.png">
</p>

3\.	Klicke auf " Approve"oder " Deposit", je nachdem, ob du es zuvor genehmigt hast.
 
4\.	Dein Wallet wird dich zur Bestätigung der Transaktion auffordern. Dies wird etwa drei Minuten dauern, aber du kannst es durch [die Zahlung einer höheren Gasgebühr an das Netzwerk beschleunigen](https://blog.leverj.io/how-to-set-the-gas-limit-and-gas-price-in-metamask-1b33c38c32fd). Wenn deine Transaktion festhängt, lies diese Anleitung zum Beschleunigen oder Abbrechen der Transaktion durch.

<p align="center">
  <img width="258.75" height=" 459.75" src="https://i.imgur.com/BkXBANS.png">
</p>

5\.	Wenn deine Transaktion erfolgreich ist, siehst du dein Depotguthaben in der Oberfläche des Vault, das ganz oben in der Vaultliste angezeigt werden sollte.

<p align="center">
  <img width="928.5" height="93.75" src="https://i.imgur.com/JvNQ3l2.png">
</p>
 
Wenn du zum Abheben bereit bist:

1\.	Wählen den Vault, von dem du eine Auszahlung vornehmen möchtest.

2\.	Gib den gewünschten Betrag ein, oder klicke auf 'Max', um das gesamte Kontoguthaben abzuheben.

<p align="center">
  <img width="910.5" height="361.5" src="https://i.imgur.com/Y3NsCRb.png">
</p>

3\.	Klicke auf 'Withdraw'.

4\.	Dein Wallet wird dich auffordern, die Buchung zu bestätigen. Siehe Schritt 4 für weitere Details.

5\.	Wenn deine Transaktion erfolgreich durchgeführt wurde, werden die Token wieder in deinem Wallet angezeigt.

## Wenn du nicht über das erforderliche Token für den Vault verfügst, in den du einzahlen möchtest:

Dies kann häufig vorkommen, da viele der Vault von Yearn Erträge durch die Verwendung von [Curve Finance](http://curve.finance/) Liquidity Provider (LP) Token generieren, die durch Einzahlung in einen Curve-Pool erworben werden.

Wenn du also zum Beispiel lieber in den crvSTETH-Vault statt in den ETH-Vault einzahlen möchtest und das zusätzliche Risiko akzeptierst, das mit dem Curve-Pool und einem der ETH-Derivate (stETH) im Austausch für eine höhere Rendite einhergeht, du aber nur ETH in deinem Wallet hast, müssen deine ETH in ein crvSTETH-Token umgewandelt werden, ehe sie in dem Vault akzeptiert werden.

Glücklicherweise kann dies dank der 'zap'-Funktion von Yearn in der gleichen Transaktion wie deiner Einzahlung erledigt werden. Hier siehst du, wie es funktioniert mit dem crvSTETH Vault als Beispiel:

**HINWEIS:** Das Zappen eines Tokens in einen Vault erfordert mehr Transaktionen als das Einzahlen des ursprünglichen Tokens. Das bedeutet, dass du mehr Gasgebühren bezahlst und möglicherweise Wert durch Slippage verlieren, wenn der Token getauscht oder in einen Pool eingezahlt wird. Yearn begrenzt Slippage auf 1% und die Transaktion wird fehlschlagen, wenn das Slippage diesen Wert überschreitet. Weitere Details findest du in unserem Abschnitt über [zap](https://docs.yearn.finance/yearn-finance/yvaults/overview#zap-in-with-any-asset).

1\.	Wähle den crvSTETH-Vault

2\.	Klicke auf das Dropdown-Feld neben der Schaltfläche 'Approve' oder 'Deposit'.

3\.	Wähle aus, welche Token du in crvSTETH umwandeln möchtest. Es werden nur die Token angezeigt, die sich in deinem Wallet befinden.

<p align="center">
  <img width="909" height="363" src="https://i.imgur.com/6K1luO7.png">
</p>
 
4\.	Gib den gewünschten Tokenbetrag ein und klicke auf 'Approve' oder 'Deposit', je nachdem, ob du den Token zuvor genehmigt hast oder nicht.

5\.	Bestätige die Transaktion über dein Wallet. Siehe Schritt 4 im oberen Abschnitt für weitere Details.

6\.	Wenn deine Transaktion erfolgreich durchgeführt wurde, siehst du deinen hinterlegten Kontostand in der Oberfläche des Vault, der oben in der Vaultliste erscheinen sollte.

Wenn du bereit bist, etwas abzuheben:

1\.	Wähle den crvSTETH-Vault aus

2\.	Klicke auf das Dropdown-Feld neben der Schaltfläche Withdraw'.

<p align="center">
  <img width="915.75" height="600.75" src="https://i.imgur.com/2UyXKN0.png">
</p>

3\.	Wähle aus, welches Asset du bei der Auszahlung erhalten möchtest. Deine Optionen werden die crvSTETH, ETH, BTC, DAI, USDC oder USDT sein.

4\.	Gib den gewünschten Abhebungsbetrag ein, oder klicke auf 'Max', um das gesamte Guthaben abzuheben.

5\.	Bestätige gegebenenfalls die Genehmigung und genehmige dann die Abhebungstransaktion.

6\.	Wenn deine Transaktion erfolgreich durchgeführt wurde, werden die Token wieder in deinem Wallet angezeigt.

## Tools zum Verfolgen deiner Anlagen

Wenn du beobachten möchtest, wie sich dein USD-Saldo verändert, während sich dein Guthaben in einem Vault befindet, kannst du dein Wallet mit [zapper.fi](https://zapper.fi) oder einem ähnlichen Portfolio-Tracking-Produkt verbinden. Dies ist auch der einfachste Weg, um festzustellen, wie viel Gewinn der Vault für dich gemacht hat.

Dein Guthaben wird sich NICHT kontinuierlich erhöhen. Der Gewinn wird auf deinen Anteil am Vault verteilt, wenn die Funktion harvest() aufgerufen wird, was in einer unregelmäßigen Basis geschieht.

Community-Ressourcen zur Übersicht über deine Gewinne:

- [Zapper](https://zapper.fi/)
- [Zerion](https://app.zerion.io/)
- [Yearn Vault ROI Calculator](https://yearn-roi.xyz/#/)
- [yVault ROI](https://yvault-roi.netlify.app/)
- [https://trackavault.com/](https://trackavault.com/)
