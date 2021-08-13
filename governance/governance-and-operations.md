# Verwaltung und Betrieb

Seit [YIP-61: Governance 2.0](https://gov.yearn.finance/t/yip-61-governance-2-0/10460) am 25. April 2021 verabschiedet wurde, begann Yearn den Übergang zu einer **multi-DAO** Struktur, die durch eine eingeschränkte Delegation verwaltet wird. Dieser Ansatz ermöglicht es, die Entwicklung von Protokollen einerseits nicht durch Bürokratie zu erschweren und andererseits gleichzeitig ein ausreichendes Maß an Dezentralisierung beizubehalten.

Multi-DAO bezieht sich auf die nicht festgelegte Anzahl dezentraler autonomer Organisationen (DAOs), die auf eine einzigartige Weise zum Protokoll beitragen. Diese unabhängigen Gruppen bestehen aus YFI-Inhabern, yTeams und der Multisig.

- **YFI holders** stimmen über die Änderungen oder der Verwaltungsstruktur des Protokolls ab
- **yTeams** konzentrieren sich auf bestimmte Aspekte des Protokolls oder relevante Vorgänge.
- **Multisig** führen Entscheidungen bezüglich der Kette aus oder legen ein Veto ein

Die Token-Inhaber haben das letzte Wort darüber, welche yTeams es gibt, wer Teil der Multisig ist und wie weit die operative Kontrolle der einzelnen Gruppen reicht. Der Begriff 'eingeschränkte Delgation' stammt von Token-Inhabern, die bestimmte Befugnisse an verschiedene Gruppen delegieren, die Yearn aufbauen und verwalten.

Ein vereinfachter Ablauf der Verwaltung würde folgendermaßen aussehen:

    1. YFI-Inhaber erstellen, zerstören und definieren die Grenzen von yTeams
    2. yTeam informiert yTx über eine Entscheidung 
    3. yTx erstellt eine delegierte Transaktion und sendet diese an die Multisig
    4. Multisig führt die Transaktion aus oder widerruft sie
    
## DAO Verantwortlichkeiten

![](https://i.imgur.com/IDysF5O.png)

### Token-Inhaber

Es ist die Pflicht des [YFI Token](https://docs.yearn.finance/governance/yfi) Inhabers, Vorschläge zur Verbesserung des Protokolls zu machen und dafür zu stimmen.

| Vorschläge | Beschreibungen |
|-----------|--------------|
|Yearn Improvement Proposal (YIP)|Ein Vorschlag zur Ausübung von Befugnissen, die den YFI-Inhabern übertragen wurden oder die nicht in den Bereich der aufgezählten Befugnisse fallen|
|Yearn Delegation Proposal (YDP)|Ein Vorschlag zur Änderung des Delegationsortes für diskrete Entscheidungsbefugnisse|
|Yearn Signaling Proposal (YSP)|Ein unverbindlicher Vorschlag, um Gefühle oder Absichten der Gemeinschaft zu einem bestimmten Thema zu signalisieren|

Diese Vorschläge ermöglichen es den Token-Inhabern, die folgenden Entscheidungen zu treffen:

| Befugnisse | Beschreibungen |
|-------|-------------|
|Befugnisse verwalten|YFI-Inhaber können darüber abstimmen, diskrete Befugnisse für yTeams zu schaffen, zu übertragen oder zu widerrufen|
|YFI-Token Vertrag ändern|Jegliche Interaktion mit dem YFI Token-Vertrag, wie z.B. das Minting von YFI oder das Vernichten der Schlüssel für das Minting, bleibt unter der Kontrolle der YFI-Inhaber|
|Gebühren festsetzen|Festlegung der Standardgebührenstrukturen im Yearn-Protokoll|
|Multisig-Unterzeichner ändern|Da die Multisig in nächster Zeit weiterhin entscheidende Befugnisse haben wird, können nur die YFI-Inhaber über einen Wechsel der Unterzeichner abstimmen|
|yTeams ratifizieren|yTeams formell zu ratifizieren oder zu deratifizieren, um zu kontrollieren, welche yTeams über delegierte Befugnisse verfügen können|
|yOps Unterzeichner ändern|Da yOps die Möglichkeit hat, Unterzeichner anderer yTeams zu ändern, ist dies eine besondere Befugnis, die Unterzeichner von yOps zu ändern|
|Finanzmittel ausgeben|Mittel aus der Finanzkasse ausgeben|
|YIP-Befugnis|Die YFI-Inhaber sind befugt, einen YIP für alles vorzuschlagen, was nicht bereits delegiert wurde|

### yTeams

Jedes yTeam hat ein Ziel und bestimmte Befugnisse, die von den Token-Inhabern festgelegt werden. Sie können weiter in Mitgliederpools unterteilt werden, bei denen es sich um separate Gruppen von Mitwirkenden handelt, die auf ähnliche Ziele wie das übergeordnete Team hinarbeiten. Außerdem kann ein Mitgliederpool ein Teil mehrerer yTeams sein.

| yTeam | Zielsetzung | Mitgliedschaftspool |
|-------|-----------|-----------------|
|yGuard|Schutz der Vaults|YFI Protokollentwickler, YFI Strategen, YFI Mechaniken, YFI geheime Bewunderer|
|yBrain|Verwaltung der Strategien|YFI Strategen|
|yDev|Verwaltung des Protokolls|YFI Protokollentwickler|
|yPeople|Das Team zusammenstellen|YFI Arbeitsgruppe Finanzen, YFI Berater|
|yBudget|Geld sinnvoll ausgeben|YFI Finanzen, YFI Berater|
|yFarm|Die Schatzkammer aufbauen|YFI geheime Bewunderer, YFI Geheimzugang|
|yTx|Transaktionen erstellen|YFI Macher|
|yOps|Koordination von Beteiligten|YFI Koordination|

Jedem yTeam werden bestimmte Entscheidungsbefugnisse zugewiesen, die in YIP-61 festgelegt sind:

| yTeam | Befugnisse | Beschreibungen |
|-------|-------|-------------|
|yGuard|Notfallbefugnisse|Im Falle eines Angriffs oder Fehlers sofort eingreifen, um Strategien zurückzusetzen oder den Vault abzuschalten|
|yBrain|Strategien verwalten|Strategien aktivieren, deaktivieren, abstimmen und pflegen|
|yDev|Yearn-Protokoll definieren|Entscheiden, welcher Code als Teil von yearn gilt und welcher nicht|
|yDev|Protokoll verwalten|Verwaltung und Verbesserung des Yearn-Protokolls|
|yDev|Strategien einfügen|Neue Strategien zum Vault hinzufügen|
|yTx|Transaktionen delegieren|Delegierte Transaktionen erstellen, die von der Multisig unterzeichnet und ausgeführt werden können|
|yPeople|Team bezahlen|Erstellen, Bereitstellen, Ändern oder Beenden von Yearn-Vergütungspaketen|
|yBudget|Budgets festlegen|Erstellung von Budgets für Coordinape, Stipendien, Einstellungen, Tätigkeiten oder andere Arbeitsbereiche|
|yFarm|Die Schatzkammer aufbauen|Mit der Schatzkammer zusammenarbeiten und Entscheidungen über Airdrops treffen|
|yOps|Ratifizierung von yTeam Unterzeichnern|Unterzeichner für jedes yTeam formell freigeben oder entfernen|

### Multisig 

Entscheidungen, die von yTeams getroffen werden, werden von der Multisig auf der Kette ausgeführt, bis ein dezentraleres System zur Einführung freigegeben wird. In der Zwischenzeit kontrolliert die the [Multisig](https://docs.yearn.finance/resources/faq#who-is-on-the-multisig) folgendes:


| Befugnis | Beschreibungen |
|-------|-------------|
|Durchsetzungskraft|Die Befugnis, Entscheidungen von YFI-Inhabern und yTeams auf der Kette auszuführen|
|Veto-Recht|Diese Befugnis ermöglicht es der Multisig, gegen jede Entscheidung ein Veto einzulegen. Im Idealfall sollte es nicht benötigt werden|
|Befugnis im Übergangsprozess|Eine vorübergehende Befugnis, die es der Multisig ermöglicht, unter dem Mandat von YIP-41 zu arbeiten, bis die Entscheidungsbefugnisse alle erforderlichen Transaktionen abdecken|


## Zukünftige Implementierungen

Yearn arbeitet kontinuierlich an einem idealen Gleichgewicht zwischen der Dezentralisierung und Produktivität der DAOs. In der aktuellen Phase werden Änderungen vor allem auf der sozialen Ebene vorgenommen, und in Zukunft werden wir uns in Richtung Software-Implementierungen bewegen, wie zum Beispiel:

- Multisig-Konsensmechanismen, die es jedem yTeam ermöglichen, Ausführungsbefugnisse zu haben
- Übergang von der Stimmrechtsvertretung zur Stimmabgabe auf der Kette
-	Die Entscheidungsbefugnisse als NFTs zu tokenisieren
-	Nutzung von [Coordinape](https://coordinape.com/) für Dinge wie Budgetzuweisung und Vergütung
