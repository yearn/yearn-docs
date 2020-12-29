---
title: faq.yearn.finance
tags: "documenti, faq, pubblicato"
---

# FAQ

## Generale

### È sicuro investire denaro su Yearn?

- Fate le vostre ricerche e decidete voi stessi.

### Yearn è verificato?

- Sì, potete trovare l'elenco delle verifiche [qui](https://github.com/iearn-finance/audits).

## Feedback e Supporto

Se avete domande su come fare qualcosa, possiamo aiutarvi su:

- [Discord](http://discord.yearn.finance)
- [Telegram](https://t.me/yearnfinance)

Ma se pensate che qualcosa possa essere migliorato, o se avete trovato un bug, noi siamo qui per risolverlo. Vi preghiamo di pubblicarlo qui:

- [Github](https://github.com/iearn-finance) — crea un nuovo argomento nel relativo repository.
- [Forum](https://gov.yearn.finance/c/general-chat/feedback/2) — scrivi nella categoria feedback.

## Prodotti

### yearn.finance

- [yearn.finance](https://yearn.finance/) ospita gli UI per i prodotti **Vaults**, **Earn**, **Zap**, **APR** e **Cover**.

### Vault

- [yearn.finance/vaults](https://yearn.finance/vaults)

#### Cos'è un Vault?

- I Vault impiegano strategie per automatizzare le migliori opportunità di rendimento per l'agricoltura disponibili.
- Sono stati ideati in modo che la comunità potesse lavorare insieme per costruire nuove strategie per trovare la migliore resa.
- Andre spiega [i vault](https://medium.com/iearn/yearn-finance-v2-af2c6a6a3613) e [delegated vaults](https://medium.com/iearn/delegated-vaults-explained-fa81f1c3fce2) in questi due post.
- In poche parole, i Vault possono:
  - Usare qualsiasi attivita come liquidità..
  - Usare la liquidità come garanzia e gestire la garanzia a un livello sicuro per evitare un'inadempienza.
  - Prendere in prestito le stablecoin.
  - Impiegare le stablecoin per l'agricoltura.
  - Reinvestire le stablecoin guadagnate.

#### Non posso fare tutto questo da solo?

- Sì che puoi farlo, ma i vault ti aiutano a risparmiare sul gas, a mantenere un buon rapporto garanzie/debito per evitare le inadempienze e ottimizzare automaticamente per le strategie stablecoin a più alto rendimento, anche mentre stai dormendo.

#### Vedo il ROI sulla pagina dei vault. È quello attuale?

- No. TQuesta è la media storica per quel vault. Gli attuali APY/rendimenti non vengono mostrati come vault, sono un prodotto beta e vengono testati dal vivo.
- Vari siti di terze parti forniscono APY e altre informazioni, sono elencati qui sotto in [Statistiche](https://docs.yearn.finance/faq#statistics).

#### Quali sono i rischi?

- Mentre gli asset depositati non possono diminuire, il debito del vault può aumentare. Se una strategia non riesce a superare il debito, allora una parte del patrimonio sarà definitivamente bloccata. Se una strategia in seguito supera di nuovo il debito, l'attività sarà di nuovo disponibile a ritirarsi. Esistono meccanismi nei vault per prevenire questo, ma nulla è a prova di proiettile.
- Per ora, solo _alcuni_ Vault sono stati [controllati](https://github.com/iearn-finance/yearn-audits/blob/bdb3868c98e4fe2427898db05154942a9192efb1/MixBytes%20-%20Yearn.Finance%20protocol%20v.1%20Smart%20Contracts%20Audit%20Security%20Audit%20Report.pdf).
- Smart contract risk con qualsiasi contratto con cui i vault interagiscono.

#### Quali sono i diversi yVaults?

**yLINK e yaLINK**

- **Qual è la differenza tra i vault LINK e aLINK?**
  - Nessuna in termini di restituzioni. Il LINK depositato sarà depositato in Aave generando aLINK \(Aave interest bearing LINK\). Quindi depositando direttamente in un vault aLINK si è un passo avanti nel processo.
- **Perchè il rendimento è diverso per i vault aLINK e LINK?**
  - aLINK ha una "tassa" assicurativa dello 0,5% (che viene restituita quando viene superata). Il vault LINK non ha questa tassa per evitare la double dip.

**yETH e yWETH**

- **Qual è la differenza tra vault WETH e vault ETH?**
  - Nessuna in termini di restituzioni. L'ETH depositato sarà comunque avvolto in WETH. Il vault WETH rende solo più facile l'interazione di altri protocolli dell'Ethereum con questo vault.
- **In che modo il vault ETH si protegge dalla liquidazione?**
  - Questo vault legge il prezzo dell'ETH direttamente dal Maker's OSM \(Oracle Security Model\), un sistema che legge il prezzo Oracle con 1 ora di anticipo. Questo dà al vault 1 ora di tempo per pagare il debito del CDP prima della liquidazione. Inoltre, il vault continua ad aumentare la collateralizzazione depositando profitti ad ogni harvest call.

**Altri Vault**

- v1 Money Market vault, precedentemente chiamati iEarn, si trovano [qui](https://yearn.finance/earn).
- Altri vault si trovano [qui](https://yearn.finance/vaults).

#### Se l'attuale strategia per il vault yCRV è CRV, viene semplicemente aggiunto al mio saldo quando lo ritiro?

- No. Il vault coltivere il CRV e poi lo vendera sul mercato automaticamente. Quando si ritira si ottiene più yCRV.

#### Perché yCRV non vale \$1, é una moneta stabile, giusto?

- No, yCRV non vale \$1, e no NON é una moneta stabile. Si può pensare a yCRV come ad un indice di rendimento di stablecoin \(yDAI+yUSDC+yUSDT+yUSDT+yTUSD\) che genera anche il rendimento \(commissioni di negoziazione dal pool Curve Y). Pertanto, il prezzo di yCRV non è in diminuzione.

#### Se tolgo il mio yCRV dal vault di yCRV, questo lo riporta al pool Curve Y alla Curve, o devo fare qualcos'altro come reinvestirlo?

- Quando si ritira il proprio yCRV dal vault, si ottiene il yCRV + più gli interessi maturati - le tasse, tutto in yCRV. Dal momento che è il token yCRV che hai recuperato, è già investito nel pool di Curve Y, facendo le commissioni di swap stablecoin. Non c'è bisogno di fare altro con Curve, a meno che non vogliate investirlo [qui](https://dao.curve.fi/minter/gauges) per generare CRV.

#### Perchè non possiamo ottenere un APY migliore per il vault YFI?

- Non si possono ottenere gli stessi numeri per due monete completamente diverse. Il nuovo sBTC sta seguendo la stessa strategia del vault yCRV utilizzando il liquidity pool di Curve. La risposta ovvia è che non ci sono molte piattaforme sicure che accettano YFI come staking, quindi in questo momento non ci sono molte strategie valide per il vault YFI.

#### Ho depositato in un vault, cosa ne ricavo quando faccio un prelievo?

- È possibile ritirare solo il tipo di asset crittografato che si è inserito.
- Riceverai l'importo che hai originariamente inserito, più il rendimento che hai guadagnato, meno le spese.

#### Quali sono le tasse?

- **Tassa dello 0,5%** sui fondi prelevati dalle strategie attive
  - Ogni vault ha una parte dei fondi totali inattivi e la maggior parte di essi è attiva nella strategia. I fondi inattivi sono la differenza tra i `fondi del vault` e i `fondi della strategia`, li puoi vedere su [feel the Yearn](https://feel-the-Yearn.app/).
  - Quando ritiri, se i tuoi fondi provengono dai fondi inattivi, non ti verrà addebitata nessuna commissione di prelievo. Se provengono dalla strategia, ti verrà addebitata la tassa dello 0,5%.
- **Tassa del 5%** sul rendimento supplementare
  - Per le strategie di comunità, come il nuovo yETH vault, attualmente il 10% di questa quota va al creatore della strategia. L'altro 90% va alla tesoreria e viene poi distribuito alla governance.

#### Puoi spiegare la commissione del 5% sul rendimento aggiuntivo?

- Prima si chiamava "tassa del 5% sul gas sovvenzionato", che confondeva letteralmente tutti tranne Andre. Tecnicamente non si tratta di una tassa di performance, ma di una tassa su alcune transazioni che generano profitti e che comportano costi elevati per il gas e che sono fondamentali per il funzionamento interno del vault.
- Ogni vault ha diversi livelli. Qui ci sono due esempi che mostrano dove viene presa questa tassa quando viene richiesta la funzione `harvest()`.
- Esempio di yCRV Vault:
  - Livello 1: le stablecoin guadagnano interesse nei mercati monetari \(compound, aave, dydx\)
  - Livello 2: i token di livello 1 (yDAI, yUSDC, yUSDT e yTUSD) sono forniti come liquidity pool di yCRV per guadagnare commissioni di trading
  - Livello 3: la strategia guadagna premi in token CRV che ricicla in yCRV-**questo è l'unico livello in cui viene presa la tassa del 5%.**
-  Esempio di USDC Vault:
  - Livello 1: interesse per essere prestato a Compound
  - Livello 2: COMP liquidata a USDC
  - Livello 3: la strategia guadagna i token DF ricompensati da DForce che vengono raccolti e venduti per USDC-**questo è l'unico livello in cui viene presa la commissione del 5%.**

#### Dove vanno a finire le commissioni?

- Vanno ad una tesoreria dedicata [contratto](https://etherscan.io/address/0x93A62dA5a14C80f265DAbC077fCEE437B1a0Efde).
- Dalla tesoreria rimangono fino al limite di \$500k, oltre tale importo vengono reindirizzati alla governance [contratto](https://etherscan.io/address/0xBa37B002AbaFDd8E89a1995dA52740bbC013D992).

#### Le tasse sono sempre andate lì?

- No, quando YEARN stata avviata, le tasse andavano direttamente all'indirizzo [indirizzo](https://etherscan.io/address/0x2d407ddb06311396fe14d4b49da5f0471447d45c) di Andre..
- Poi abbiamo consegnato al [multisig](https://etherscan.io/address/0xFEB4acf3df3cDEA7399794D0869ef76A6EfAff52) e i compensi sono andati direttamente lì.
- E prima del nostro attuale gov v2, le ricompense in stake sandavano [qui](https://etherscan.io/address/0xb01419E74D8a2abb1bbAD82925b19c36C191A701)

#### Rendimento

- Abbiamo in programma di realizzare in futuro una dashboard che mostrerà chiaramente il vostra attuale APY di tutte le posizioni aperte. Attualmente per i vault, poiché sono ancora in beta, non mostriamo le APY live, ma vengono pubblicate su [twitter](https://twitter.com/iearnfinance) circa una volta al giorno. Puoi stimare approssimativamente il rendimento che stai ottenendo osservando quale [strategia attuale](https://feel-the-Yearn.vercel.app/) è l'agricoltura e verificando quale sia la sua APY.
- Per esempio, se il vault di yCRV sta coltivando il token CRV, puoi controllare qual è la resa sul sito [homepage di Curve](https://www.curve.fi/) per il pool Y

### Strategie del vault

#### Cos'è la strategia del Vault?

- Le strategie di YEARN dei vault sono smart contract modulari per ogni vault che indicano quali asset prendere in prestito, quali asset coltivare e dove vendere gli asset coltivati.

#### Quali sono le strategie attuali?

- È possibile visualizzare le strategie attuali implementate in [feel-the-Yearn](https://feel-the-Yearn.vercel.app/).
- In futuro, abbiamo in programma di creare una dashboard per rendere le strategie e l'APY facili da capire.

#### Chi ha il controllo delle strategie?

- Le scrivono gli sviluppatori, ma è il multi-sig, istruito dagli elettori YFI, a decidere se saranno implementate o meno.

#### Come posso creare una strategia?

- Per ora puoi pubblicare la tua strategia sul forum nella sezione strategie. Specificando cosa vorresti comprare/vendere/allevare e qual è l'APY attuale. Ci sarà un modello che ti aiuterò ad iniziare.

#### Qual è il processo per far arrivare la mia strategia su YEARN?

- Pubblicatela sul forum o contattate il team di sviluppo, se otterrete il supporto per la vostra idea e se finirà per essere implementata e approvata, verrà utilizzata nei vault e potrete essere pagati.

#### Quando cambia una strategia e chi la cambia? È automatica?

- I creatori di strategie osservano i mercati e scrivono strategie che ritengono sicure e che danno il massimo rendimento. Le cambiano in base ai rendimenti attuali del mercato.

### Earn

- [yearn.finance/earn](https://yearn.finance/earn)

#### Che cos'è Earn?

- Earn è un aggregatore di rendimento per piattaforme di prestito che riequilibra il rendimento più alto durante l'interazione del contratto.
- Deposita DAI, USDC, USDT, USDT, TUSD, o sUSD e presterà automaticamente al tasso di prestito più alto su queste piattaforme [Compound](https://compound.finance/), [Dydx](https://dydx.exchange/) o [Aave](https://app.aave.com/home) \(Ddex e Fulcrum sono attualmente disabilitati\).
- Per saperne di più, consulta i [Documenti Yearn](https://docs.yearn.finance/products/earn)

### Zap

- [yearn.finance/zap](https://yearn.finance/zap)

#### Che cos'è Zap?

- Zap consente agli utenti di convertire i token supportati con una sola interazione contrattuale per ridurre i costi di transazione.
- Gli Zap sono stati realizzati da DefiZap che ora è [Zapper.fi](https://zapper.fi) come un servizio di routing DeFi tutto in uno.

#### Perchè utilizzare uno Zap?

- "Gli Zap consentono di entrare in una posizione DeFi in una transazione - si chiama zapping in." - [Guida all'uso degli Zap](https://defitutorials.substack.com/p/how-to-use-defizap).
  - Si noti che questo è un vecchio articolo e che [Zapper](https://zapper.fi) è stato creato come risultato dell'unione di DeFiSnap + DeFiZap per creare l'ultimo hub per la Finanza Decentrata alias \#DeFi. Quindi alcune informazioni contenute nell'articolo di cui sopra sono obsolete, ma è ancora possibile utilizzare Zaps su Zapper.fi.

#### Allora cosa posso fare con Zaps su Yearn?

- Con uno zap puoi prendere il tuo DAI, per esempio, e ottenere yCRV in una sola transazione. Normalmente, per trasformare il DAI in yCRV, dovresti andare su Earn, depositare il DAI e ricevere yDAI, poi andare su [Curve.fi - Yearn pool](https://www.curve.fi/iearn/deposit) e depositare il tuo yDAI e poi riceverai yCRV. Questo è molto complesso, quindi invece si può fare in una sola transazione!

#### Sembra fantastico, qual è il lato negativo?

- Beh, ci vuole molto gas e potrebbe essere costoso, anche più che farlo da soli manualmente, ma se hai una transazione importante e hai fretta è un ottimo metodo per entrare velocemente in una posizione DeFi o in un liquidity pool.

### yInsure / Cover

- [yinsure.finance](https://yinsure.finance/)

#### Che cosa è yInsure?

- yInsure, noto anche come **Cover**, è un sistema di copertura in pool che fornisce un'assicurazione contro lo smart contract risk.
- Non ha nessun requisito KYC ed è sottoscritto da Nexus Mutual.
- Scopri di più in questo [articolo](https://medium.com/iearn/yinsure-finance-a-new-insurance-primitive-77d5d4217896).

### Prodotti Attualmente in Ricerca e Sviluppo

#### yTrade

- [ytrade.finance](https://ytrade.finance/)
- Negoziazioni stabili di monete con effetto leva \(testnet\).

#### yLiquidate

- [yliquidate.finance](https://yliquidate.finance/)
- 0 liquidazioni automatiche di capitale per Aave \(testnet\).

#### ySwap

- [yswap.exchange](https://yswap.exchange/)
- Market maker automatizzato su un solo lato \(testing in mainnet\).

#### yBorrow

- [yborrow.finance](https://yborrow.finance/)
- Delegazioni di credito per smart contract a smart contract \(testnet\).

## Comunicazione

- [Forum](https://gov.yearn.finance)
  -Si discute molto in tempo reale sul Telegram e su Discord, ma perché una proposta si trasformi in una YIP \(YEARN Proposta di Miglioramento\) deve essere postata e discussa sul forum.
  - Questo é il luogo principale in cui i titolari di token controllano le questioni relative alla governance.
- [Discord](http://discord.yearn.finance/)
  - Inclusi i canali non inglesi.
- [Telegram](https://t.me/yearnfinance) - Chat principale.
- [Telegram](https://t.me/yearncommunity) - Chat commerciale, sociale e di lavoro.
- Twitter
  - [yearn.finance](https://twitter.com/iearnfinance?s=20) - Twitter ufficiale di Yearn
  - [Andre Cronje](https://twitter.com/AndreCronjeTech?s=20) - Il fondatore e creatore di Yearn
  - [yLearnfinance](https://twitter.com/yLearnfinance) - Info su Yearn
  - [Learn 2 Yearn](https://twitter.com/learn2Yearn) - Info su Yearn

## Governance

### Tutto su YIPs

#### Cos'é un YIP? Perché sono importanti?

- Una proposta di miglioramento YIP o YEARN é il modo in cui le caratteristiche vengono aggiunte all'ecosistema YEARN. Gli utenti iniziano una proposta sul forum, ne discutono e valutano se la proposta sarà accettata. Se molti utenti sono d'accordo, la proposta potr essere pubblicata online per consentire a tutti di votare.

#### Quante persone devono votare per approvare una proposta YIP?

- Il quorum è del 20%. Il che significa che il 20% di YFI deve votare una proposta per farla approvare, altrimenti non verrà approvata. Inoltre, deve avere almeno il 50% dei voti per il sì.
- Puoi pubblicare prima la tua proposta, ma se la gente non ne ha parlato, probabilmente non voterà a favore.

####  Come faccio a fare una proposta?

-Il modello predefinito per le proposte può essere trovato su [Github](https://github.com/iearn-finance/YIPS/blob/master/yip-X.md) + sul [forum](https://gov.yearn.finance) se fai un post sotto proposte o discussioni, si compilerà automaticamente anche nel modello.
- Il procedimento è all'incirca il seguente:
  1. discussione sul forum
  2. promote to YIP \(usually done by mods\), add YIP to github, put on chain
  3. announce

#### Who can make a proposal?

- Anyone can post a proposal both on the forum and on-chain.

### Voting

#### How do I vote?

- Stake your YFI and then you can cast your vote for YIPs that are on-chain on the voting [dashboard](https://ygov.finance/vote)

#### Can I vote if my YFI is in the YFI vault?

- No, your YFI must be staked in the governance [contract](https://ygov.finance/staking) in order to vote.

#### Where can I view the YIPs?

- You can view them on the voting [dashboard](https://ygov.finance/vote) if you login to your web3 account or at [yips.yearn.finance](https://yips.yearn.finance/all-yip).

#### Why should I stake? What is the APY \(Annual Percentage Yield\)?

- You should stake if you want to vote on YIPs and get rewards that are generated from the Yearn ecosystem. The APY for staking is currently not listed on the UI. You can ask on the chat what the rate is.

#### What do I have to do to get rewards with my YFI?

- All you need to do is stake YFI at [ygov.finance/stake](https://ygov.finance/stake) and you will get rewards if the treasury is at or above 500k usd. You can check the treasury address [here](https://zapper.fi/dashboard?address=0xFEB4acf3df3cDEA7399794D0869ef76A6EfAff52).
- Note that if you stake you get rewards \(as long as they are not going to the treasury\) but you can only claim them within 3 days of voting.

#### Does staking my YFI matter for voting?

- Yes. You have to stake your YFI at [ygov.finance/stake](https://ygov.finance/stake) in the v2 tab under Governance V2 to have your votes count. As of now, you can vote without staking, but you will waste your gas and it won't count so make sure you have staked first if you want to vote.

#### What if I want to take my YFI out before the end of the vote lock?

- You can't, sorry. The lock lasts 3 days after you last voted, until then you cannot unstake your tokens.
- If you try to unstake your tokens before the lock ends you will see a very high gas cost, this is an error, you will not be able to unstake until the 3 day lock has ended

#### I voted and I know the vote lock is 3 days, is there anywhere I can see exactly how long I have left till I can unstake my YFI?

- Yes! You can read the contract directly ygov.finance staking [contract](https://etherscan.io/address/0xBa37B002AbaFDd8E89a1995dA52740bbC013D992#readContract) go to 28 votelock and input your eth address. This will give you the eth block number when you can unstake.

#### What’s the difference between voting for a poll on the forum and an on-chain vote?

- A poll just gauges the sentiment of what the community is feeling on the proposal while a on-chain vote will be binding and will take effect if it passes.

#### What about the new gasless voting thing?

- We now have an off-chain signaling system that uses staked balances from ygov. This replaces the older, informal forum polls which were vulnerable to sybil attacks. It can do multiple choice and doesn't cost gas to use, you sign with your wallet instead. We still use the normal on-chain voting system for YIPs.

#### How long is my YFI tied up if I stake it?

- Your YFI is locked for 3 days after you vote.

#### Why can't I claim my staking rewards!

- To claim your staking rewards you have to 1\) be staked and 2\) have voted within 3 days to be able to claim them. This will be fixed in an update soon.

### yDAO

- Pokemol [site](https://pokemol.com/dao/0xcb46298767fb5d44c18313976c30d3eeb5071862/).
- Forum [post](https://gov.yearn.finance/t/ydao-for-community-funding/2243).

#### What is its purpose?

- Used to fund value-added contributions to the Yearn ecosystem.

#### Who cares, how do I make money from this?

- You don't. This is solely for allocating funding for projects, and the YFI donated will be spent and your share value will be diluted.

#### Who can join?

- Open for anyone to join with a base rate of 1 Share = 0.1 YFI.

#### How can I join?

- Go here to [Pokemol](https://pokemol.com/dao/0xcb46298767fb5d44c18313976c30d3eeb5071862) sign in with your web3 account. Click New Proposal button in the top right. Click member.
  - Title: your name/entity
  - Description: “Pledging X amount of YFI in exchange for Y Shares” \(Please make this consistent with the amount being pledged at 0.1 YFI per share\)
  - Link: Link to you or your entity \(Website, Twitter, Linkedin\)
  - Shares Requested: The number of Shares being requested
  - Token Tribute: The amount of YFI being pledged \(you will need to unlock YFI\)
  - Loot: The number of shares being requested
  - After you submitted the two transactions and are in the new member queue, you will need a sponsor. Please copy the link to your proposal and let us know you’d like to join in the [yDAO Telegram channel](https://t.me/joinchat/Qn1GPBv0y7lY1vAmRCB7KA)

#### How can I request funding?

- The same ways as joining except instead of click member click the funding tab and fill in the details of your request. You can ask in the [telegram chat](https://t.me/joinchat/Qn1GPBv0y7lY1vAmRCB7KA) if you have any questions.

#### I don't speak English, when will everything be translated?

- We are working on translating to other languages but it will take time. For now you can go to your language in the global section in [Discord](http://discord.yearn.finance/).

## Community

### Does Yearn have a manifesto?

- Some contributors got together and wrote a post about how they think about the protocol, with others joining in to support it. It's available [on the forum](https://gov.yearn.finance/t/how-we-think-about-yearn/).

### Is Andre Cronje in charge of Yearn?

- Andre isn't in charge of Yearn, the YFI token holders make the decisions on how to govern Yearn, Andre is one of the developers in the Yearn ecosystem.

### What is the multisig and what do they do?

- The multi-signature address is explained in detail in this [thread](https://gov.yearn.finance/t/yfi-minting-ownership/155). Basically, it is a 6 of 9 multi-signature account that has control over minting YFI if a vote to mint tokens has passed successfully.

### Who are the 9 multisig signers?

- [Cp0x.com](https://twitter.com/kaplansky1/status/1285427247286046725)
- [Daryllautk](https://twitter.com/Daryllautk/status/1285434908383444992)
- [Devops199fan](https://twitter.com/devops199fan/status/1285430347954622464)
- [Banteg](https://twitter.com/bantg/status/1285426492906909696)
- [Milkyklim](https://milkyklim.keybase.pub/yearn-social-proof.txt)
- [Joe Mahon aka Substreight](https://twitter.com/Substreight/status/1299780260737630209)
- [Tarun Chitra, Gauntlet](https://twitter.com/gauntletnetwork/status/1299778153674616833)
- [Vasiliy Shapovalov, p2p.org](https://twitter.com/_vshapovalov/status/1299799139635679232)
- [Mariano Conti, ex-MakerDAO](https://twitter.com/nanexcool)

### Have the multisig signers changed?

- Yes, [YIP-40](https://gov.yearn.finance/t/yip-40-replace-inactive-multisig-signers/3535) changed four of the signers
- Outgoing signers were:
  - [Coopahtroopa](https://twitter.com/Cooopahtroopa/status/1285438650550038529)
  - [Michael, Curve.fi](https://twitter.com/CurveFinance/status/1285428322986389504)
  - [Calvin Liu](https://twitter.com/cjliu49/status/1285439553180798976)
  - [Damir Bandalo](https://twitter.com/damirbandalo/status/1285500362015875073)

### What decisions can Andre make on his own?

- Andre can build out the Yearn ecosystem and come up with new products. Usually, he posts his thoughts and ideas on the [forum](https://gov.yearn.finance) or on his [medium blog](https://andrecronje.medium.com) for everyone to see.

### Does the multisig group tell him what to do?

- They are in close contact with one another, but Andre's priorities are his own. They can be instructed via YIPs.

### Who else writes code for Yearn? Is there a team?

- Yes! Meet some of the developers behind Yearn:

  - [@banteg](https://gov.yearn.finance/u/banteg)
  - [@fubuloubu](https://gov.yearn.finance/u/fubuloubu)
  - [@x48](https://gov.yearn.finance/u/x48)
  - [@doug](https://gov.yearn.finance/u/doug)
  - [@luciano](https://gov.yearn.finance/u/luciano)
  - [@orbxball](https://gov.yearn.finance/u/orbxball)

### Does anyone get paid for working on Yearn?

- Yes. Yearn has a core team that receives recurring payments. Grants are also distributed to valuable contributors in a monthly basis. For instance, see the [September Grants Announcement](https://gov.yearn.finance/t/september-grants-announcement/7044).

### How can I work for Yearn?

- If you want to contribute to the project as well just reach out to our community managers on [Discord](http://discord.yearn.finance/)/[Telegram](https://t.me/yearnfinance)/[Twitter](https://twitter.com/iearnfinance). We'll also release soon a Contributor's Guide.

### Do you have any job openings?

- Yes, we do! We need all kinds of people to help make the Yearn ecosystem a thriving product and to give value to YFI. You can ask in the Discord or Telegram about applying or post on the forum. State how you think you can add value to Yearn, and how much you think you should be paid from the community pool. Also, you can go to the [yDAO](https://gov.yearn.finance/t/ydao-for-community-funding/2243) as well for funding on your work for the Yearn ecosystem.

### How to Participate?

- You can participate in YFI by voting on YIPs that are active, discussing the YIPs yet to be proposed on-chain on the forums and talking about YFI in the Telegram and Discord. If you know a second language help us translate the site and YIPs into that language.

### Ongoing efforts to improve the Yearn ecosystem

- You can view the active YIPs [here](https://yips.yearn.finance/all-yip)

## User Interface

### Can I use the Yearn ecosystem dApps on my phone?

- Yes, you have to use the Metamask browser

## Technical Support

### I sent my ETH transaction but it says pending? How do I fix this?

- You should always make sure to set your gas properly if you want a transaction to go through quickly. Check current gas prices at [Ethgasstation](https://ethgasstation.info/) or [gasnow](https://www.gasnow.org/).
- If you're using MetaMask and you put your transaction through but it's going too slow, you have the option to speed it up by clicking the `speed up` button below your last pending transaction under "activity". This should resend the same TX again with a higher gas price to get it confirmed faster.
- If you've tried everything and your transaction is still stuck pending, you can fix it by sending a transaction to the nonce of the first stuck transaction with a high gas price to overwrite the stuck queue. Here's a good [guide](https://ethgasstation.info/blog/stuck-transaction-guide) explaining how to do this.

### Why is the withdrawal fee so high?

- If you're seeing higher than normal fees while using the Yearn ecosystem then it may be due to Ethereum congestion and abnormally high gas costs. Check [Ethgasstation](https://ethgasstation.info/). Your options are to wait until gas prices drop or spend the money to process your transaction now.
- If the gas prices are crazy high, that means there is an error and the transaction will not be able to process. For instance if you are trying to deposit a token you don't have or if there is no cover available for a contract at [http://yinsure.finance/](http://yinsure.finance/).

## Related Projects

### [Curve](https://www.curve.fi)

- Curve is an exchange liquidity pool on Ethereum \(like [Uniswap](https://app.uniswap.org/#/)\) designed for \(1\) extremely efficient stablecoin trading \(2\) low risk, supplemental fee income for liquidity providers, without an opportunity cost. Curve allows users \(and smart contracts like 1inch, Paraswap, Totle and Dex.ag\) to trade between DAI and USDC with a bespoke low slippage, low fee algorithm designed specifically for stablecoins and earn fees. Behind the scenes, the liquidity pool is also supplied to the Compound protocol or yearn.finance where it generates even more income for liquidity providers.
- Curve [FAQ](https://www.curve.fi/rootfaq).

### [Aave](https://app.aave.com/home)

- Aave is an open source and non-custodial protocol enabling the creation of money markets. Users can earn interest on deposits and borrow assets.

## Resources

### Where can I learn more about Yearn?

- [Learn Yearn](https://www.learnyearn.finance/)
- [Medium.com/iearn](https://medium.com/iearn)
- [yCosystem](https://ycosystem.info/)

### Lists of Smart Contracts

- [https://gov.yearn.finance/t/yearn-contracts/1951](https://gov.yearn.finance/t/yearn-contracts/1951)
- [https://etherscan.io/accounts/label/yearn-finance](https://etherscan.io/accounts/label/yearn-finance)
  - sign-in required
- [Delegated controller](https://etherscan.io/address/0x2be5d998c95de70d9a38b3d78e49751f10f9e88b#readContract)
- [StrategyVaultTUSD](https://etherscan.io/address/0x35CEE4c61B7619956e0B2015B5411F93CBba817A#code)
- [yLINK token](https://etherscan.io/address/0x881b06da56bb5675c54e4ed311c21e54c5025298#code)
- [yaLINK token](https://etherscan.io/address/0x29e240cfd7946ba20895a7a02edb25c210f9f324#readContract)
- [StrategyMStableSavingsTUSD](https://etherscan.io/address/0xd6214317bf66921154d78e3074bada013a4de8e8#readContract)
- [yTUSD](https://etherscan.io/address/0x37d19d1c4e1fa9dc47bd1ea12f742a0887eda74a)
- [yTokenRebalance](https://etherscan.io/address/0x19b6424C58aFcee6D0cb954D4B8d44B9b5e9cC09#code)
- [CollateralVaultProxy](https://etherscan.io/address/0xf0988322b8392245d6232e520bf3cdf912b043c4)
- [USDC strategy for LINK](https://etherscan.io/address/0x25fAcA21dd2Ad7eDB3a027d543e617496820d8d6)
- [Strategy for USDC vault](https://etherscan.io/address/0xA30d1D98C502378ad61Fe71BcDc3a808CF60b897)
- [Strategy for USDC vault](https://etherscan.io/address/0xA30d1D98C502378ad61Fe71BcDc3a808CF60b897)
- [DAI vault](https://etherscan.io/address/0xACd43E627e64355f1861cEC6d3a6688B31a6F952)

### Registry of Tokens and Utility Contracts

- [https://docs.yearn.finance/developers/deployed-contracts-registry](https://docs.yearn.finance/developers/deployed-contracts-registry)

### Vaults Detail Reference

- [https://vaults.finance/](https://vaults.finance/)

### Statistics

- [yieldfarming.info](https://yieldfarming.info/)
- [yVault ROI Calculator](https://py-earn.herokuapp.com/)
- [stats.finance/yearn](https://stats.finance/yearn)
- [Feel The Yearn](https://feel-the-yearn.vercel.app/)
- Initial Distribution [Dune Dashboard](https://explore.duneanalytics.com/dashboard/yearn)
- Voting Stats [Dune Dashboard](https://explore.duneanalytics.com/public/dashboards/Lqnxzm7fa8NVhKC4kc37DDFPZgqXryaIjyLRYAYp)
- Vaults Stats [Dune Dashboard](https://explore.duneanalytics.com/public/dashboards/g0bGfgloeXBd9C18jpBjdXi5KkQjR7IXYqFRUnHk)

### Latest Yearn News

- [yearn.finance](https://twitter.com/iearnfinance) - Offical Twitter of Yearn
- [AndreCronjeTech](https://twitter.com/AndreCronjeTech)
- [Yearn Finance](https://medium.com/iearn) - Offical Blog

### Podcasts

- [Unchained - Andre Cronje on YFI and the Fair Launch: ‘I’m Lazy’](https://unchainedpodcast.com/andre-cronje-of-yearn-finance-on-yfi-and-the-fair-launch-im-lazy/)
- [Andre Cronje and the Philosophy of Yearn Finance](https://anchor.fm/hasu-research/episodes/6-Andre-Cronje-and-the-Philosophy-of-Yearn-Finance-ei4vds)
- [The FTX Podcast - Andre Cronje DeFI Architect](https://open.spotify.com/episode/6d14TJtQU7eB69azelpdeh)
- [Zapper Community Call - With Andre](https://www.youtube.com/watch?v=venoiaiVZ-U)
- [In DeFi My Money is Actually Mine. Its a Beautiful Concept But it Comes With Responsibilities - Andre Cronje](https://anchor.fm/camila-russo/episodes/In-DeFi-My-Money-is-Actually-Mine--Its-a-Beautiful-Concept-But-it-Comes-With-Responsibilities-Andre-Cronje-ehs3op)
- [YFI: Farming the Farmers \| Andre Cronje](http://podcast.banklesshq.com/25-king-of-the-yield-farmers-andre-cronje)

### Blogs

- [Yearn Finance - Offical Blog](https://medium.com/iearn)
  - [Yinsure.finance: A new insurance primitive](https://medium.com/iearn/yinsure-finance-a-new-insurance-primitive-77d5d4217896)
  - [Delegated Vaults Explained](https://medium.com/iearn/delegated-vaults-explained-fa81f1c3fce2)
  - [yearn.finance v2](https://medium.com/iearn/yearn-finance-v2-af2c6a6a3613?source=---------3------------------)
  - [Yearn Governance Forum](https://medium.com/iearn/yearn-governance-forum-7b7c9d0300ac?source=collection_home---6------2-----------------------)
  - [YFI rewards pool](https://medium.com/iearn/yfi-rewards-pool-810ef9256ec6)
  - [YFI](https://medium.com/iearn/yfi-df84573db81)

### Logos

- Can be found in the Discord under [\#media-resources](https://discord.com/channels/734804446353031319/736132884443955242/740325105904779326)
