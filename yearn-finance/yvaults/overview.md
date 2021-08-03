# Übersicht

## Was sind yVaults?

[yVaults](https://yearn.finance/vaults) sind wie Sparkonten für dein Kryptoguthaben. Sie nehmen deine Einzahlung an und nutzen dann für sie eine Strategie, die die in DeFi höchste verfügbare Rendite ausfindig macht.

![](https://i.imgur.com/yXnJqsn.png)
 
## Mit jedem Vermögenswert einsteigen

Dank [Zapper](https://zapper.fi/) kann in yVaults extrem einfach eingezahlt werden. Solange du einen Token besitzt, der auf Uniswap mit weniger als 1 % Slippage getauscht werden kann, wird der Vault den Token akzeptieren, ihn in den für den Vault erforderlichen Wert umwandeln und alles in der gleichen Transaktion einzahlen.

Bei der Auszahlung können die Benutzer in einen der folgenden Token zurückzappen:
- ETH, WETH, DAI, USDT, USDC, WBTC

## yVault-Gebührenstruktur

|yVault Version|Rücktrittsgebühr|Leistungsgebühr|Managementgebühr|
|--------------|:-----------:|:-------------:|:------------:|
|v1|0.5%|5%|-|
|v2|-|20%|2%|

- Rücktrittsgebühr: Einmalige Gebühr bei Rücktritt.
- Leistungsgebühr: Prozentsatz, der vom Gewinn abgezogen wird.
- Managementgebühr: Prozentsatz, der pro Jahr vom Gesamtsaldo abgezogen wird.

## v2 yVault Verbesserungen

- **Bis zu 20 Strategien pro Vault:** Dies erhöht die Flexibilität für ein effizientes Kapitalmanagement in verschiedenen Marktszenarien. Jede Strategie hat eine Kapitalobergrenze. Dies ist nützlich, um zu vermeiden, dass zu viele Mittel einer Strategie zugewiesen werden, die den effektiven APY nicht mehr steigern kann.
- **Stratege und Betreuer sind die neuen Kontrolleure:** Das Konzept des Controllers ist in V2 yVaults nicht mehr verfügbar und wurde durch einen Guardian und den Strategie-Ersteller \(strategist\) ersetzt. Diese beiden Akteure überwachen die Leistung der Strategie und sind befugt, Maßnahmen zur Verbesserung des Kapitalmanagements zu ergreifen oder auf kritische Situationen zu reagieren.
- **Automatisierte Verwaltung des Vaults \(Keep3r network\):** `harvest()` und `earn()`-Aufrufe sind jetzt durch das Keep3r-Bots-Netzwerk automatisiert. Diese beiden Funktionsaufrufe werden verwendet, um neue zugrundeliegende Sicherheiten zu kaufen, indem die verdienten Token verkauft werden, während die Gewinne zurück in den Vault und später in Strategien verschoben werden. Das Keep3r-Netzwerk übernimmt die schwere Aufgabe, diese Anrufe zu tätigen und die Gasgebühren im Austausch gegen Keep3r-Tokens zu tragen. Dieser Ansatz entlastet die Menschen von diesen Verwaltungsaufgaben.
- **Türsteher und Gästelisten:** Yearn hat einen einzigartigen Entwicklungsprozess für neue Vaults entwickelt. Alle Vaults werden zu Beginn als Testvault (tyvToken) gestartet. Testvaults haben eine Obergrenze und somit auch ihre Strategien. Außerdem hat der Türsteher (Bouncer) eine Gästeliste von Wallets, die interagieren können, indem sie Einlagen und Abhebungen in den Testvaults vornehmen. Dieser Ansatz verhindert, dass uninformierte Benutzer möglicherweise Gelder in einem noch nicht produktionsreifen Produkt verlieren.
