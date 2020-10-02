---
Título: faq.yearn.finance
tags: 'docs, faq, published'
---

# FAQ

## General

### ¿Es seguro invertir dinero en yearn?

* Por favor, investiga por tu cuenta y toma la decisión tú solo.

### ¿Ha sido yearn auditado?

* Sí, puedes encontrar la lista de audiciones de seguridad [aquí](https://github.com/iearn-finance/audits).

## Comentarios & Asistencia

Si tienes alguna pregunta a cerca de algo, te podemos ayudar en:

* [Discord](http://discord.yearn.finance)
* [Telegram](https://t.me/yearnfinance)

Por otro lado, si crees que algo puede mejorarse o has encontrado algún bug, nos encantaría arreglarlo. Puedes reportarlo aquí:

* [Github](https://github.com/iearn-finance) — crea un nuevo issue en el repositorio que corresponda.
* [Forum](https://gov.yearn.finance/c/feedback/) — crea un post en la categoría feedback del foro.

## Productos

### yearn.finance

* [yearn.finance](https://yearn.finance/) aloja los UIs de los productos **Vaults**, **Earn**, **Zap**, **APR**, y **Cover**.

### Vaults

* [yearn.finance/vaults](https://yearn.finance/vaults)

#### ¿Qué es una Vault?

* Las Vaults usan estrategias para automatizar las mejores oportunidades de yield farming disponibles.
* Fueron diseñadas para que la comunidad pudiera trabajar en conjunto para construir nuevas estrategias y así encontrar los mejores rendimientos.
* Andre explica las [Vaults](https://medium.com/iearn/yearn-finance-v2-af2c6a6a3613) y las [Vaults delegadas](https://medium.com/iearn/delegated-vaults-explained-fa81f1c3fce2) en estas dos publicaciones.
* En pocas palabras, las Vaults pueden hacer esto:
  * Utilizar cualquier activo como liquidez.
  * Utilizar la liquidez como garantía y gestionar la garantía a un nivel seguro para que nunca sea liquidada.
  * Pedir prestadas monedas estables.
  * Ponger las monedas estables a farmear.
  * Reinvertir las monedas estables ganadas.

#### ¿No puedo hacer todo esto yo mismo?

* Sí, podrías hacerlo, pero las vaults sirven para ahorrar gas, mantener un buen ratio aval/deuda para que el aval no sea liquidado y cambia automáticamente a la estrategia que de el rendimiento más alto posible, incluso mientras estás dormido.

#### Veo que se muestra el ROI en la página de las vaults, ¿es el ROI actual?

* No, es un valor histórico promediado para la vault en cuestión. El APY / ganancias actuales no se muestran ya que las vaults son un producto en beta y se están probando en vivo. 
* Varios sitios de terceras personas proporcionan el APY actual y otro tipo de información. Estos sitios puedes encontrarse más abajo en [Estadísticas](https://docs.yearn.finance/faq#statistics).

#### ¿Cuáles son los riesgos?

* Aunque los activos depositados no pueden disminuir, la deuda de la vault sí puede. Si una estrategia no logra superar a la deuda, una parte de los activos quedarán bloqueados de forma temporal. Si la estrategia vuelve a superar a la deuda, los activos se desbloquearán.
  * Hay mecanismos en las vaults para evitarlo pero nada es totalmente seguro.
* Hasta ahora, las vaults no han sido auditadas.
* Riesgo de contrato inteligente \(comúnmente conocido como smart contract en la comunidad de habla inglesa\) con cualquier contrato con el que interactúen las vaults.

#### ¿Cuáles son las diferentes yVaults?

**yLINK y yaLINK**

* **¿Cuál es la diferencia entre la vault de LINK y la de aLINK?**
  * Ninguna en términos de ganancias. El LINK depositado en la vault será depositado en Aave generando aLINK \( LINK que genera intereses en Aave\). Por tanto, depositando directamente en la vault de aLINK te saltas un paso del proceso.
* **¿Por qué el rendimiento de las vaults de aLINK y LINK son diferentes?**
  * aLINK tiene una "tarifa" de seguro del 0.5%  \(se devuelve cuando se supera \). La vault de LINK no tiene esta tarifa para la aparición de un rendimiento      negativo.

**yETH y yWETH**

* **¿Cuál es la diferencia entre las vaults de ETH y la de WETH?**
  * Ninguna en términos de ganancias. El ETH depositado será convertido en WETH en cualquier caso. La vault de WETH hace más fácil a otros protocolos de Ethereum interactuar con esta vault.
* **¿Qué hace la vault de ETH para protegerse de una liquidación?**
  * Esta vault obtiene el precio de ETH directamente del oráculo de Maker \(Maker's Oracle Security Model\), un sistema que lee el precio del Oráculo con 1 hora de ventaja. Esto le da a la vault 1 hora para pagar la deuda de la CDP antes de que se produzca la liquidación del ETH que se usa como aval para el préstamo de DAI. Además, la vault aumenta el ratio de colateralización depositando las ganancias conseguidas en la CDP.

**Otras vaults**

* Las vaults conocidas como v1 Money Market vaults, anteriormente llamadas iEarn, pueden ser encontradas [aquí](https://yearn.finance/earn).
* El resto de las vaults pueden encontrarse [aquí](https://yearn.finance/vaults).

#### Si la estrategia actual para la vault de yCRV está farmeando CRV, ¿se añadirán esos tokens a mi saldo cuando saque mis fondos de la vault?

* No. La vault farmeará CRV que será vendido en el mercado automáticamente. Cuando decidas retirar tus fondos de la vault, recibirás más yCRV de los que depositaste inicialmente.

#### ¿Por qué el token yCRV no vale $1?, es una moneda estable ¿verdad?

* No, el token yCRV no vale $1, y NO es una moneda estable. Puedes pensar en yCRV como si fuera un índice de monedas estables \(yDAI+yUSDC+yUSDT+yTUSD\) que genera rendimientos y que también recibe tarifas \(más concretamente, tarifas de los intercambios hechos en la Y pool de Curve\). Por lo tanto, el precio del token yCRV no decrece. 

#### Si retiro mis tokens yCRV de la vault de yCRV, ¿son retirados también de la Y pool de Curve? ¿Tengo que hacer algo más, como volver a depositarlos en la pool?

* Cuando retiras tus tokens yCRV de la vault, recibes de vuelta tu depósito de yCRV además de los intereses ganados, todo pagado en tokens yCRV. Dado que el token yCRV es lo que recibes de vuelta, este ya está de por sí stakeado en la Y pool de Curve generando redimientos en forma de tarifas pagadas a la hora de intercambiar monedas estables en la Y pool. No necesitas hacer nada más en Curve, a no ser que quieras stakear tus tokens [aquí](https://dao.curve.fi/minter/gauges) para generar CRV.

#### ¿Por qué no se puede obtener un mejor rendimiento de la vault de YFI?

* No puedes esperar obtener el mismo rendimiento para dos monedas totalmente distintas. La nueva vault de sBTC sigue la misma estrategia que la vault de yCRV que usa la pool de liquidez de Curve. La respuesta obvia es que no hay muchas plataformas seguras que acepten depósitos de YFI por lo que no hay muchas estrategias válidas para la vault de YFI ahora mismo.

#### He depositado en una vault, ¿qué recibiré de vuelta cuando decida dejar de usarla?

* Cuando decidas sacar tus fondos de la vault, siempre obtendrás de vuelta el mismo tipo de monedas que depositaste.
* Recibirás los fondos que depositaste más el rendimiento generado menos las posibles tarifas.

#### ¿Cuáles son las tarifas ?

* **Tarifa del 0.5%** sobre fondos retirados de estrategias activas.
  * Cada vault tiene una cierta cantidad de los fondos totales inactivos mientras que la mayoría de estos participan activamente en la estrategia. Los fondos inativos son la diferencia entre`vault holdings` y `strategy holdings` que pueden consultarse en [feel the yearn](https://feel-the-yearn.app/).
  * Cuando retiras tus fondos, si estos son extraídos de los fondos inactivos de la vault, 
  * When you withdraw, if your funds come from the idle funds, you won't be charged any withdrawal fee. If they come from the strategy, you will be charged the 0.5% fee.
* **5% fee** on additional yield
  * For community-made strategies, like the new yETH vault, currently 10% of this fee goes to the strategy creator. The other 90% goes to the treasury and is then distributed to governance.

#### Can you explain the 5% fee on additional yield?

* Formerly this was called a "5% fee on subsidized gas" which confused literally everyone except Andre. Technically it is not a performance fee — it's a fee on the some profit-generating transactions that incur high gas costs and are critical to the vault's internal functioning.
* Each vault has multiple levels. Here are two examples that show where this fee is taken when the `harvest()` function is called.
* yCRV Vault example:
  * Level 1: stablecoins earn interest in money markets \(compound, aave, dydx\)
  * Level 2: the level 1 tokens \(yDAI, yUSDC, yUSDT, and yTUSD\) are provided as liquidty to the yCRV pool to earn trading fees
  * Level 3: the strategy earns CRV token rewards which it recycles into yCRV—**this is the only level where the 5% fee is taken.**
* USDC Vault example:
  * Level 1: Interest for being lent out at Compound
  * Level 2: COMP liquidated to USDC
  * Level 3: The strategy earns DF tokens rewards from DForce that get harvested and sold for USDC—**this is the only level where the 5% fee is taken.**

#### Where do the fees go? ¿A donde van las tarifas recolectadas?

* They go to a dedicated treasury [contract](https://etherscan.io/address/0x93A62dA5a14C80f265DAbC077fCEE437B1a0Efde).
* From the treasury they stay up to the $500k limit, over that amount they are redirected to the governance staking [contract](https://etherscan.io/address/0xBa37B002AbaFDd8E89a1995dA52740bbC013D992).

#### Did the fees always go there? ¿Han las tarifas siempre a ese sitio?

* No, when yearn started they went directly to Andre's [address](https://etherscan.io/address/0x2d407ddb06311396fe14d4b49da5f0471447d45c).
* Then we handed off to the [multisig](https://etherscan.io/address/0xFEB4acf3df3cDEA7399794D0869ef76A6EfAff52) and fees went directly there.
* And before our current gov v2, staking rewards went [here](https://etherscan.io/address/0xb01419E74D8a2abb1bbAD82925b19c36C191A701)

#### Yield Rendimiento

* We plan to make a dashboard in the future that will clearly show your current APY of all the positions you have open. Currently for the Vaults as they are still in beta we are not showing the APY live, but it is post on [twitter](https://twitter.com/iearnfinance) around once a day. You can roughly estimate the yield you are getting by looking at what the [current strategy](https://feel-the-yearn.vercel.app/) is farming and checking what its APY is.
* For example if yCRV vault is farming the CRV token, you can check what the yield is on [Curve's homepage](https://www.curve.fi/) for the Y pool

### Vault Strategies Estrategias de las Vaults

#### What is a Vault Strategy? ¿Qué es una estrategia de una Vault?

* Yearn's vault strategies are modular smart contracts for each vault that tells it what assets to borrow, which assets to farm, and where it should sell the farmed assets.

#### What are the current strategies? ¿Cuáles son las estrategias actuales?

* You can view the current strategies implemented at [feel-the-yearn](https://feel-the-yearn.vercel.app/).
* In the future we plan to make a dashboard to make the strategies and APY easy to understand.

#### Who is in control of the strategies? ¿Quién controla las estrategias?

* Andre and other developers write them but the multi-sig decides if they will be implemented or not.

#### How can I make a strategy? ¿Cómo puedo hacer una estrategia?

* For now you can post your strategy on the forum in the strategy section. Detailing what it should buy/sell/farm and what the current APY is. There will be a template to help you get started.

#### What is the process for getting my strategy onto yearn? ¿Cuál es el proceso a seguir para incluir mi estrategia en yearn?

* Post it on the forum and if it gets approved it will be used in the vaults and you can get paid for it.

#### When does a strategy changes and who changes it? Is it automatic? ¿Cuándo cambia una estrategia y quién lo hace?

* For now Andre watches the markets and writes strategies that he and the multi-sig thinks are safe while giving the highest yield. They change them according to current yields on the market.

### Earn

* [yearn.finance/earn](https://yearn.finance/earn)

#### What is Earn? ¿Qué es Earn?

* Earn is a yield aggregator for lending platforms that rebalances for highest yield during contract interaction.
* Deposit DAI, USDC, USDT, TUSD, or sUSD and it will auto lend to the highest lending rate on these platforms [Compound](https://compound.finance/), [Dydx](https://dydx.exchange/) or [Aave](https://app.aave.com/home) \(Ddex and Fulcrum are currently disabled\).
* Learn more in the [Yearn Docs](https://docs.yearn.finance/yearn.finance/yearn)

### Zap

* [yearn.finance/zap](https://yearn.finance/zap)

#### What is Zap? ¿Qué es Zap?

* Zap allows users to convert supported tokens with just one contract interaction to reduce transaction costs.
* Zaps were made by DefiZap which is now [Zapper.fi](https://zapper.fi) as a type of all in one DeFi routing service.

#### Why use a Zap? ¿Qué ventajas ofrece Zap?

* "Zaps allow you get into a DeFi position in one transaction — it’s called zapping in." - [How to use Zaps guide](https://defitutorials.substack.com/p/how-to-use-defizap).
  * Note that this is an old article and [Zapper](https://zapper.fi) was formed as a result of DeFiSnap + DeFiZap coming together to create the ultimate hub for Decentralized Finance aka \#DeFi. So some of the stuff in the article above is out of date, but you can still use Zaps on Zapper.fi.

#### So what can I do with Zaps on yearn? Entonces, ¿qué puedo hacer con Zap en yearn?

* With a zap you can take your DAI, for example, and get yCRV with it in one transaction. Normally, to turn DAI into yCRV, you would have to go to earn, deposit DAI and receive yDAI, then go to [Curve.fi - Yearn pool](https://www.curve.fi/iearn/deposit) and deposit your yDAI and then you would get yCRV. This is a lot to do, so instead you can do it in one transaction!

#### That sounds awesome, what's the downside? Tiene muy buena pinta, ¿hay alguna desventaja?

* Well, it does take a lot of gas and could be costly, even more so than doing it yourself manually, but if you have a big transaction and are in a rush it is a great method to get into a DeFi position or liquidity pool fast.

### yInsure / Cover

* [yinsure.finance](https://yinsure.finance/)

#### What's yInsure? ¿Qué es yInsure?

* yInsure, also known as **Cover**, is a pooled coverage system providing insurance against smart contract risk.
* It has no KYC requirement and is underwritten by Nexus Mutual.
* Learn more in this [article](https://medium.com/iearn/yinsure-finance-a-new-insurance-primitive-77d5d4217896).

### Products Currently in Research & Development Productos que actualmente están bajo Investigación & Desarrollo

#### yTrade

* [ytrade.finance](https://ytrade.finance/)
* Leveraged stable coin trades \(testnet\).

#### yLiquidate

* [yliquidate.finance](https://yliquidate.finance/)
* 0 capital automated liquidations for Aave \(testnet\).

#### ySwap

* [yswap.exchange](https://yswap.exchange/)
* Single sided automated market maker \(testing in mainnet\).

#### yBorrow

* [yborrow.finance](https://yborrow.finance/)
* Credit delegation vaults for smart contract to smart contract lending \(testnet\).

## Comunicación

* [Foro](https://gov.yearn.finance)
  * A lot of real-time discussion happens on the telegram and discord but for a proposal to turn into a YIP \(Yearn Improvement Proposal\) it needs to be posted and discussed on the forum.
  * This is the main place token holders check for governance related issues.
* [Discord](http://discord.yearn.finance/)
  * Incluídos canales para hablar en idiomas distintos al inglés.
* [Telegram](https://t.me/yearnfinance) - Canal principal.
* [Telegram](https://t.me/yearncommunity) - Canal de Trading/Social/Forks.
* Twitter
  * [yearn.finance](https://twitter.com/iearnfinance?s=20) - Twitter oficial de Yearn
  * [Andre Cronje](https://twitter.com/AndreCronjeTech?s=20) - Desarrollador principal de Yearn
  * [yLearnfinance](https://twitter.com/yLearnfinance) - Información a cerca de Yearn
  * [Learn 2 Yearn](https://twitter.com/learn2yearn) - Información a acerca de Yearn

## Gobernanza

### Todo a cerca de las YIPs

#### ¿Qué es una YIP? ¿Por qué son importantes?

* A YIP or Yearn Improvement Proposal is how features are added to the yearn ecosystem. Users start a proposal on the forum, discuss it and gauge the sentiment of if the proposal will be accepted. If a lot of users agree with it then it can be posted on-chain for everyone to vote on.

#### How many people need to vote to pass a YIP proposed on-chain?

* The quorum is 20%. Which means that 20% of the staked YFI needs to vote on a proposal for it to pass or else it will fail. Also, it has to have at least 50% of the votes for yes.
* You can post your proposal on-chain first but if people haven't talked about it, they probably won't vote for it.

#### How do I make a proposal? ¿Cómo hago una propuesta?

* The default template for proposals can be found on [Github](https://github.com/iearn-finance/YIPS/blob/master/yip-X.md) + on the [forum](https://gov.yearn.finance) if you make a post under proposals or discussion it will auto-fill in the template as well.
* The process is roughly:
  1. forum discussion
  2. promote to YIP \(usually done by mods\), add YIP to github, put on chain
  3. announce

#### Who can make a proposal? ¿Quién puede hacer una propuesta?

* Anyone can post a proposal both on the forum and on-chain.

### Votaciones

#### How do I vote? ¿Cómo puedo votar?

* Stake your YFI and then you can cast your vote for YIPs that are on-chain on the voting [dashboard](https://ygov.finance/vote)

#### Can I vote if my YFI is in the YFI vault? ¿Puedo votar si tengo mis tokens YFI en la vault de YFI?

* No, your YFI must be staked in the governance [contract](https://ygov.finance/staking) in order to vote.

#### Where can I view the YIPs? ¿Dónde puedo ver las YIPs?

* You can view them on the voting [dashboard](https://ygov.finance/vote) if you login to your web3 account or at [yips.yearn.finance](https://yips.yearn.finance/all-yip).

#### Why should I stake? What is the APY \(Annual Percentage Yield\)? ¿Por qué debería stakear? ¿Cuál es el APY \(Porcentaje de rendimiento anual\)?

* You should stake if you want to vote on YIPs and get rewards that are generated from the yearn ecosystem. The APY for staking is currently not listed on the UI. You can ask on the chat what the rate is.

#### What do I have to do to get rewards with my YFI? ¿Qué tengo que hacer para recibir recompensas con mis tokens YFI?

* All you need to do is stake YFI at [ygov.finance/stake](https://ygov.finance/stake) and you will get rewards if the treasury is at or above 500k usd. You can check the treasury address [here](https://zapper.fi/dashboard?address=0xFEB4acf3df3cDEA7399794D0869ef76A6EfAff52).
* Note that if you stake you get rewards \(as long as they are not going to the treasury\) but you can only claim them within 3 days of voting.

#### Does staking my YFI matter for voting? A la hora de votar, ¿es importante tener stakeados mis tokens YFI?

* Yes. You have to stake your YFI at [ygov.finance/stake](https://ygov.finance/stake) in the v2 tab under Governance V2 to have your votes count. As of now, you can vote without staking, but you will waste your gas and it won't count so make sure you have staked first if you want to vote.

#### What if I want to take my YFI out before the end of the vote lock?

* You can't, sorry. The lock lasts 3 days after you last voted, until then you cannot unstake your tokens.
* If you try to unstake your tokens before the lock ends you will see a very high gas cost, this is an error, you will not be able to unstake until the 3 day lock has ended

#### I voted and I know the vote lock is 3 days, is there anywhere I can see exactly how long I have left till I can unstake my YFI?

* Yes! You can read the contract directly ygov.finance staking [contract](https://etherscan.io/address/0xBa37B002AbaFDd8E89a1995dA52740bbC013D992#readContract) go to 28 votelock and input your eth address. This will give you the eth block number when you can unstake.

#### What’s the difference between voting for a poll on the forum and an on-chain vote?

* A poll just gauges the sentiment of what the community is feeling on the proposal while a on-chain vote will be binding and will take effect if it passes.

#### What about the new gasless voting thing?

* We now have an off-chain signaling system that uses staked balances from ygov. This replaces the older, informal forum polls which were vulnerable to sybil attacks. It can do multiple choice and doesn't cost gas to use, you sign with your wallet instead. We still use the normal on-chain voting system for YIPs.

#### How long is my YFI tied up if I stake it?

* Your YFI is locked for 3 days after you vote.

#### Why can't I claim my staking rewards!

* To claim your staking rewards you have to 1\) be staked and 2\) have voted within 3 days to be able to claim them. This will be fixed in an update soon.

### yDAO

* [Sitio](https://pokemol.com/dao/0xcb46298767fb5d44c18313976c30d3eeb5071862/) de Pokemol.
* [Hilo](https://gov.yearn.finance/t/ydao-for-community-funding/2243) en el foro oficial.

#### What is its purpose? ¿Cuál es su utilidad/propósito/objetivo?

* Used to fund value-added contributions to the yearn ecosystem.

#### Who cares, how do I make money from this? A quién le importa, ¿Cómo puedo hacer dinero de esto?

* You don't. This is solely for allocating funding for projects, and the YFI donated will be spent and your share value will be diluted.

#### Who can join? ¿Quién puede unirse?

* Open for anyone to join with a base rate of 1 Share = 0.1 YFI.

#### How can I join? ¿Cómo puedo unirme?

* Go here to [Pokemol](https://pokemol.com/dao/0xcb46298767fb5d44c18313976c30d3eeb5071862) sign in with your web3 account. Click New Proposal button in the top right. Click member.
  * Title: your name/entity
  * Description: “Pledging X amount of YFI in exchange for Y Shares” \(Please make this consistent with the amount being pledged at 0.1 YFI per share\)
  * Link: Link to you or your entity \(Website, Twitter, Linkedin\)
  * Shares Requested: The number of Shares being requested
  * Token Tribute: The amount of YFI being pledged \(you will need to unlock YFI\)
  * Loot: The number of shares being requested
  * After you submitted the two transactions and are in the new member queue, you will need a sponsor. Please copy the link to your proposal and let us know you’d like to join in the [yDAO Telegram channel](https://t.me/joinchat/Qn1GPBv0y7lY1vAmRCB7KA)

#### How can I request funding? ¿Cómo puedo solicitar financiación?

* The same ways as joining except instead of click member click the funding tab and fill in the details of your request. You can ask in the [telegram chat](https://t.me/joinchat/Qn1GPBv0y7lY1vAmRCB7KA) if you have any questions.

#### I don't speak English, when will everything be translated? No hablo inglés, ¿Cuándo estará todo disponible en otros idiomas?

* We are working on translating to other languages but it will take time. For now you can go to your language in the global section in [Discord](http://discord.yearn.finance/).

## Comunidad

### Is Andre Cronje in charge of yearn? ¿Está Andre Cronje a cargo de yearn?

* Andre isn't in charge of Yearn, the YFI token holders make the decisions on what to build and governance decisions, Andre is the lead developer of the yearn ecosystem.

### What does Andre do? ¿Qué es lo que hace Andre?

* Andre is the main developer building out the products that comprise the yearn ecosystem: Yearn, Ytrade, Yswap, Yliquidate, Yborrow. He is also currently in charge of running the Vaults and overseeing them.

### What is the multisig and what do they do? ¿Qué es la multisig y cuáles son sus funciones?

* The multi-signature address is explained in detail in this [thread](https://gov.yearn.finance/t/yfi-minting-ownership/155). Basically, it is a 6 of 9 multi-signature account that has control over minting YFI if a vote to mint tokens has passed successfully.

### Who are the 9 multisig signers? ¿Quiénes son los 9 firmantes de la multisig?

* [Cp0x.com](https://twitter.com/kaplansky1/status/1285427247286046725)
* [Daryllautk](https://twitter.com/Daryllautk/status/1285434908383444992)
* [Devops199fan](https://twitter.com/devops199fan/status/1285430347954622464)
* [Banteg](https://twitter.com/bantg/status/1285426492906909696)
* [Milkyklim](https://milkyklim.keybase.pub/yearn-social-proof.txt)
* [Joe Mahon aka Substreight](https://twitter.com/Substreight/status/1299780260737630209)
* [Tarun Chitra, Gauntlet](https://twitter.com/gauntletnetwork/status/1299778153674616833)
* [Vasiliy Shapovalov, p2p.org](https://twitter.com/_vshapovalov/status/1299799139635679232)
* [Mariano Conti, ex-MakerDAO](https://twitter.com/nanexcool)

### Have the multisig signers changed? ¿Se ha cambiado en alguna ocasión alguno de los firmates de la multisig?

* Yes, [YIP-40](https://gov.yearn.finance/t/yip-40-replace-inactive-multisig-signers/3535) changed four of the signers
* Outgoing signers were:
  * [Coopahtroopa](https://twitter.com/Cooopahtroopa/status/1285438650550038529)
  * [Michael, Curve.fi](https://twitter.com/CurveFinance/status/1285428322986389504)
  * [Calvin Liu](https://twitter.com/cjliu49/status/1285439553180798976)
  * [Damir Bandalo](https://twitter.com/damirbandalo/status/1285500362015875073)

### What decisions can Andre make on his own? ¿Qué decisiones puede tomar Andre por su cuenta?

* Andre can build out the Yearn ecosystem and come up with new products. Usually, he posts his thoughts and ideas on the [forum](https://gov.yearn.finance) for everyone to see.

### Does the multisig group tell him what to do? ¿Los integrantes de la multisig le dicen a él lo que tiene que hacer?

* They are in close contact with one another, but Andre's priorities are decided by YFI token holders via YIPs.

### Who else writes code for yearn? Is there a team? ¿Quién más escribe código para yearn? ¿Hay algún equipo?

* Right now it's just Andre.

### Does anyone get paid for working on yearn?

* As of this moment, not yet, but thanks to the passage of [YIP 36](https://yips.yearn.finance/YIPS/yip-36) and the creation of a community pool of funds that will be kept at 500k usd, we can now pay Andre for his work, fund audits, and pay for new devs to be hired along with anything else the the yearn ecosystem needs.

### How can I work for yearn?

* You can make a YIP to apply for funding from the 500k USD treasury directly or ask the yDAO for funding.

### Do you have any job openings?

* Yes, we do! We need all kinds of people to help make the yEarn ecosystem a thriving product and to give value to YFI. You can ask in the Discord or Telegram about applying or post on the forum. State how you think you can add value to Yearn, and how much you think you should be paid from the community pool. Also, you can go to the [yDAO](https://gov.yearn.finance/t/ydao-for-community-funding/2243) as well for funding on your work for the Yearn ecosystem.

### How to Participate?

* You can participate in YFI by voting on YIPs that are active, discussing the YIPs yet to be proposed on-chain on the forums and talking about YFI in the Telegram and Discord. If you know a second language help us translate the site and YIPs into that language.

### Ongoing efforts to improve the Yearn ecosystem

* You can view the active YIPs [here](https://yips.yearn.finance/all-yip)

## User Interface

### Can I use the Yearn ecosystem dApps on my phone?

* Yes, you have to use the Metamask browser

## Technical Support Soporte técnico

### I sent my ETH transaction but it says pending? How do I fix this?

* You should always make sure to set your gas properly if you want a transaction to go through quickly. Check current gas prices at [Ethgasstation](https://ethgasstation.info/) or [gasnow](https://www.gasnow.org/).
* If you're using MetaMask and you put your transaction through but it's going too slow, you have the option to speed it up by clicking the `speed up` button below your last pending transaction under "activity". This should resend the same TX again with a higher gas price to get it confirmed faster.
* If you've tried everything and your transaction is still stuck pending, you can fix it by sending a transaction to the nonce of the first stuck transaction with a high gas price to overwrite the stuck queue. Here's a good [guide](https://ethgasstation.info/blog/stuck-transaction-guide) explaining how to do this.

### Why is the withdrawal fee so high?

* If you're seeing higher than normal fees while using the yearn ecosystem then it may be due to Ethereum congestion and abnormally high gas costs. Check [Ethgasstation](https://ethgasstation.info/). Your options are to wait until gas prices drop or spend the money to process your transaction now.
* If the gas prices are crazy high, that means there is an error and the transaction will not be able to process. For instance if you are trying to deposit a token you don't have or if there is no cover available for a contract at [http://yinsure.finance/](http://yinsure.finance/).

## Related Projects

### [Curve](https://www.curve.fi)

* Curve is an exchange liquidity pool on Ethereum \(like [Uniswap](https://app.uniswap.org/#/)\) designed for \(1\) extremely efficient stablecoin trading \(2\) low risk, supplemental fee income for liquidity providers, without an opportunity cost. Curve allows users \(and smart contracts like 1inch, Paraswap, Totle and Dex.ag\) to trade between DAI and USDC with a bespoke low slippage, low fee algorithm designed specifically for stablecoins and earn fees. Behind the scenes, the liquidity pool is also supplied to the Compound protocol or yearn.finance where it generates even more income for liquidity providers.
* Curve [FAQ](https://www.curve.fi/rootfaq).

### [Aave](https://app.aave.com/home)

* Aave is an open source and non-custodial protocol enabling the creation of money markets. Users can earn interest on deposits and borrow assets.

## Resources

### Where can I learn more about yearn?

* [Learn Yearn](https://www.learnyearn.finance/)
* [Medium.com/iearn](https://medium.com/iearn)
* [yCosystem](https://ycosystem.info/)

### Lists of Smart Contracts

* [https://gov.yearn.finance/t/yearn-contracts/1951](https://gov.yearn.finance/t/yearn-contracts/1951)
* [https://etherscan.io/accounts/label/yearn-finance](https://etherscan.io/accounts/label/yearn-finance)
  * sign-in required
* [Delegated controller](https://etherscan.io/address/0x2be5d998c95de70d9a38b3d78e49751f10f9e88b#readContract)
* [StrategyVaultTUSD](https://etherscan.io/address/0x35CEE4c61B7619956e0B2015B5411F93CBba817A#code)
* [yLINK token](https://etherscan.io/address/0x881b06da56bb5675c54e4ed311c21e54c5025298#code)
* [yaLINK token](https://etherscan.io/address/0x29e240cfd7946ba20895a7a02edb25c210f9f324#readContract)
* [StrategyMStableSavingsTUSD](https://etherscan.io/address/0xd6214317bf66921154d78e3074bada013a4de8e8#readContract)
* [yTUSD](https://etherscan.io/address/0x37d19d1c4e1fa9dc47bd1ea12f742a0887eda74a)
* [yTokenRebalance](https://etherscan.io/address/0x19b6424C58aFcee6D0cb954D4B8d44B9b5e9cC09#code)
* [CollateralVaultProxy](https://etherscan.io/address/0xf0988322b8392245d6232e520bf3cdf912b043c4)
* [USDC strategy for LINK](https://etherscan.io/address/0x25fAcA21dd2Ad7eDB3a027d543e617496820d8d6)
* [Strategy for USDC vault](https://etherscan.io/address/0xA30d1D98C502378ad61Fe71BcDc3a808CF60b897)
* [Strategy for USDC vault](https://etherscan.io/address/0xA30d1D98C502378ad61Fe71BcDc3a808CF60b897)
* [DAI vault](https://etherscan.io/address/0xACd43E627e64355f1861cEC6d3a6688B31a6F952)

### Registry of Tokens and Utility Contracts

* [https://docs.yearn.finance/yearn.finance/yearn-1](https://docs.yearn.finance/yearn.finance/yearn-1)

### Vaults Detail Reference

* [https://vaults.finance/](https://vaults.finance/)

### Estadísticas

* [yieldfarming.info](https://yieldfarming.info/)
* [yVault ROI Calculator](https://py-earn.herokuapp.com/)
* [stats.finance/yearn](https://stats.finance/yearn)
* [Feel The Yearn](https://feel-the-yearn.vercel.app/)
* Initial Distribution [Dune Dashboard](https://explore.duneanalytics.com/dashboard/yearn)
* Voting Stats [Dune Dashboard](https://explore.duneanalytics.com/public/dashboards/Lqnxzm7fa8NVhKC4kc37DDFPZgqXryaIjyLRYAYp)
* Vaults Stats [Dune Dashboard](https://explore.duneanalytics.com/public/dashboards/g0bGfgloeXBd9C18jpBjdXi5KkQjR7IXYqFRUnHk)

### Latest Yearn News

* [yearn.finance](https://twitter.com/iearnfinance) - Offical Twitter of Yearn
* [AndreCronjeTech](https://twitter.com/AndreCronjeTech)
* [Yearn Finance](https://medium.com/iearn) - Offical Blog

### Podcasts

* [Unchained - Andre Cronje on YFI and the Fair Launch: ‘I’m Lazy’](https://unchainedpodcast.com/andre-cronje-of-yearn-finance-on-yfi-and-the-fair-launch-im-lazy/)
* [Andre Cronje and the Philosophy of Yearn Finance](https://anchor.fm/hasu-research/episodes/6-Andre-Cronje-and-the-Philosophy-of-Yearn-Finance-ei4vds)
* [The FTX Podcast - Andre Cronje DeFI Architect](https://open.spotify.com/episode/6d14TJtQU7eB69azelpdeh)
* [Zapper Community Call - With Andre](https://www.youtube.com/watch?v=venoiaiVZ-U)
* [In DeFi My Money is Actually Mine. Its a Beautiful Concept But it Comes With Responsibilities - Andre Cronje](https://anchor.fm/camila-russo/episodes/In-DeFi-My-Money-is-Actually-Mine--Its-a-Beautiful-Concept-But-it-Comes-With-Responsibilities-Andre-Cronje-ehs3op)
* [YFI: Farming the Farmers \| Andre Cronje](http://podcast.banklesshq.com/25-king-of-the-yield-farmers-andre-cronje)

### Blogs

* [Yearn Finance - Offical Blog](https://medium.com/iearn)
  * [Yinsure.finance: A new insurance primitive](https://medium.com/iearn/yinsure-finance-a-new-insurance-primitive-77d5d4217896)
  * [Delegated Vaults Explained](https://medium.com/iearn/delegated-vaults-explained-fa81f1c3fce2)
  * [Yearn.finance v2](https://medium.com/iearn/yearn-finance-v2-af2c6a6a3613?source=---------3------------------)
  * [Yearn Governance Forum](https://medium.com/iearn/yearn-governance-forum-7b7c9d0300ac?source=collection_home---6------2-----------------------)
  * [YFI rewards pool](https://medium.com/iearn/yfi-rewards-pool-810ef9256ec6)
  * [YFI](https://medium.com/iearn/yfi-df84573db81)

### Logos

* Can be found in the Discord under [\#media-resources](https://discord.com/channels/734804446353031319/736132884443955242/740325105904779326)

