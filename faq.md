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
  * Utilizar la liquidez como aval para un préstamo y gestionar el préstamo   para que el aval nunca sea liquidado.
  * Pedir prestadas monedas estables.
  * Ponger las monedas estables a farmear.
  * Reinvertir las monedas estables ganadas.

#### ¿No puedo hacer todo esto yo mismo?

* Sí, podrías hacerlo, pero las Vaults sirven para ahorrar gas, mantener un buen ratio aval/deuda para que el aval no sea liquidado y cambia automáticamente a la estrategia que de el rendimiento más alto posible, incluso mientras estás durmiendo.

#### Veo que se muestra el ROI en la página de las Vaults, ¿es el ROI actual?

* No, es un valor histórico promediado para la Vault en cuestión. El APY / ganancias actuales no se muestran ya que las Vaults son un producto en beta y se están probando en vivo. 
* Varios sitios de terceras personas proporcionan el APY actual y otro tipo de información. Estos sitios pueden encontrarse más abajo en [Estadísticas](https://docs.yearn.finance/faq#statistics).

#### ¿Cuáles son los riesgos?

* Aunque los activos depositados no pueden disminuir, la deuda de la Vault sí puede. Si una estrategia no logra superar a la deuda, una parte de los activos quedarán bloqueados de forma temporal. Si la estrategia vuelve a superar a la deuda, los activos se desbloquearán.
  * Hay mecanismos en las Vaults para evitarlo pero nada es totalmente seguro.
* Hasta ahora, las Vaults no han sido auditadas.
* Riesgo de contrato inteligente \(comúnmente conocido como smart contract en la comunidad de habla inglesa\) con cualquier contrato con el que interactúen las Vaults.

#### ¿Cuáles son las diferentes yVaults?

**yLINK y yaLINK**

* **¿Cuál es la diferencia entre la Vault de LINK y la de aLINK?**
  * Ninguna en términos de ganancias. El LINK depositado en la Vault será depositado en Aave generando aLINK \( LINK que genera intereses en Aave\). Por tanto, depositando directamente en la vault de aLINK te saltas un paso del proceso.
* **¿Por qué el rendimiento de las Vaults de aLINK y LINK son diferentes?**
  * aLINK tiene una "tarifa" de seguro del 0.5%  \(se devuelve cuando se supera \). La Vault de LINK no tiene esta tarifa para evitar la aparición de un rendimiento negativo.

**yETH y yWETH**

* **¿Cuál es la diferencia entre las Vaults de ETH y la de WETH?**
  * Ninguna en términos de ganancias. El ETH depositado será convertido a WETH en cualquier caso. La Vault de WETH hace más fácil a otros protocolos de Ethereum interactuar con esta Vault.
* **¿Qué hace la Vault de ETH para protegerse de una liquidación?**
  * Esta Vault obtiene el precio de ETH directamente del oráculo de Maker \(Maker's Oracle Security Model\), un sistema que lee el precio del Oráculo con 1 hora de ventaja. Esto le da a la Vault 1 hora para pagar la deuda de la CDP antes de que se produzca la liquidación del ETH que se usa como aval para el préstamo de DAI. Además, la vault aumenta el ratio de colateralización depositando las ganancias conseguidas en la CDP.

**Otras Vaults**

* Las Vaults conocidas como v1 Money Market Vaults, anteriormente llamadas iEarn, pueden ser encontradas [aquí](https://yearn.finance/earn).
* El resto de las Vaults pueden encontrarse [aquí](https://yearn.finance/vaults).

#### Si la estrategia actual para la Vault de yCRV está farmeando CRV, ¿se añadirán esos tokens a mi saldo cuando saque mis fondos de la Vault?

* No. La Vault farmeará CRV que será vendido en el mercado automáticamente. Cuando decidas retirar tus fondos de la Vault, recibirás más tokens yCRV de los que depositaste inicialmente.

#### ¿Por qué el token yCRV no vale $1?, es una moneda estable ¿verdad?

* No, el token yCRV no vale $1, y NO es una moneda estable. Puedes pensar en yCRV como si fuera un índice de monedas estables \(yDAI+yUSDC+yUSDT+yTUSD\) que genera rendimientos y que también recibe tarifas \(más concretamente, tarifas de los intercambios hechos en la Y pool de Curve\). Por lo tanto, el precio del token yCRV no decrece. 

#### Si retiro mis tokens yCRV de la Vault de yCRV, ¿son retirados también de la Y pool de Curve? ¿Tengo que hacer algo más, como volver a depositarlos en la pool?

* Cuando retiras tus tokens yCRV de la Vault, recibes de vuelta tu depósito de yCRV además de los intereses ganados, todo pagado en tokens yCRV. Dado que el token yCRV es lo que recibes de vuelta, este ya está de por sí stakeado en la Y pool de Curve generando redimientos en forma de tarifas pagadas a la hora de intercambiar monedas estables en la Y pool. No necesitas hacer nada más en Curve, a no ser que quieras stakear tus tokens [aquí](https://dao.curve.fi/minter/gauges) para generar CRV.

#### ¿Por qué no se puede obtener un mejor rendimiento de la Vault de YFI?

* No puedes esperar obtener el mismo rendimiento para dos monedas totalmente distintas. La nueva v
* Vault de sBTC sigue la misma estrategia que la Vault de yCRV que usa la pool de liquidez de Curve. La respuesta obvia es que no hay muchas plataformas seguras que acepten depósitos de YFI por lo que no hay muchas estrategias válidas para la vault de YFI ahora mismo.

#### He depositado en una Vault, ¿qué recibiré de vuelta cuando decida dejar de usarla?

* Cuando decidas sacar tus fondos de la Vault, siempre obtendrás de vuelta el mismo tipo de monedas que depositaste.
* Recibirás los fondos que depositaste más el rendimiento generado menos las posibles tarifas.

#### ¿Cuáles son las tarifas ?

* **Tarifa del 0.5%** sobre fondos retirados de estrategias activas.
  * Cada Vault tiene una cierta cantidad de los fondos totales inactivos mientras que la mayoría de estos participan activamente en la estrategia. Los fondos inativos son la diferencia entre`vault holdings` y `strategy holdings` que pueden consultarse en [feel the yearn](https://feel-the-yearn.app/).
  * Cuando retiras tus fondos, si estos son extraídos de los fondos inactivos de la Vault, no tendrás que pagar ninguna tarifa de retiro. En cambio, si los fondos son extraídos de la estrategia, se aplicará una tafica del 0.5% del total que se va a retirar.
* **Tarifa del 5%** en rendimientos adicionales
  * Para estrategias hechas por un miembro de la comunidad, como la nueva Vault de yETH, un 10% de esta tarifa va destinada al creador de la estrategia. EL otro 90% va al tesoro desde donde es distribuída a los stakers del contracto de gobernanza.

#### ¿Podrías explicarme la tarifa del 5% en rendimientos adicionales?

* Anteriormente, esta se llamaba "tarifa del 5% sobre el gas subsidiado" que confundía literalmente a todos excepto a Andre. Técnicamente, no es una tarifa de rendimiento, sino una tarifa sobre algunas transacciones generadoras de ganancias que incurren en altos costes de gas y que son fundamentales para el funcionamiento interno de la Vault.
* Cada Vault está compuesta por distintos niveles. A continuación tienes dos ejemplos para ilustrar de donde se descuenta la tarifa cuando la función `harvest()` es llamada.
* Ejemplo para la Vault de yCRV:
  * Nivel 1: monedas estables ganan intereses en plataformas de lending \(compound, aave, dydx\)
  * Nivel 2: los tokens del nivel 1 \(yDAI, yUSDC, yUSDT y yTUSD\) son depositados como liquidez en la pool de yCRV para obtener tarifas de trading
  * Nivel 3: La estrategia farmea tokens CRV que son vendidos por yCRV—**este es el único nivel donde la tarifa del 5% es aplicada.**
* Ejemplo para la Vault de USDC:
  * Nivel 1: Intereses generados por prestar las monedas en Compound
  * Nivel 2: COMP es vendido por USDC
  * Nivel 3: La estrategia farmea tokens DF de DForce que son vendidos por USDC—**este es el único nivel donde la tarifa del 5% es aplicada.**

#### ¿A dónde van las tarifas recolectadas?

* Van al [contrato](https://etherscan.io/address/0x93A62dA5a14C80f265DAbC077fCEE437B1a0Efde) del tesoro.
* El tesoro recibirá las tarifas recolectadas hasta un límite máximo de $500k, cualquier cantidad extra será redirijida al [contrato](https://etherscan.io/address/0xBa37B002AbaFDd8E89a1995dA52740bbC013D992) de gobernanza.

#### ¿Han ido las tarifas siempre a ese contrato?

* No, al comienzo de yearn iban directamente a la [cuenta](https://etherscan.io/address/0x2d407ddb06311396fe14d4b49da5f0471447d45c) de Andre.
* Después, el control pasó a la [multisig](https://etherscan.io/address/0xFEB4acf3df3cDEA7399794D0869ef76A6EfAff52) y las tarifas iban allí directamente.
* Antes de la versión actual del contrato de gobernanza, las recompensas de staking iban [aquí](https://etherscan.io/address/0xb01419E74D8a2abb1bbAD82925b19c36C191A701).

#### Rendimiento

* Tenemos planeado hacer un tablón en el futuro donde se mostrará claramente el APY actual de todas las posiciones que tienes abiertas. Actualmente, para las Vaults, ya que todavía están en versión beta, no mostramos el APY en vivo, pero este se publica en [twitter](https://twitter.com/iearnfinance) una vez al día. Puedes estimar aproximadamente el rendimiento que estás obteniendo observando cuál es la [estrategia actual](https://feel-the-yearn.vercel.app/) y verificando cuál es su APY.
* Por ejemplo, si la Vault yCRV está farmeando el token CRV, puedes verificar cuál es el rendimiento en la [página de inicio de Curve](https://www.curve.fi/) para la pool Y.

### Estrategias de las Vaults

#### ¿Qué es una estrategia de una Vault?

* Las estrategias de las Vaults de yearn son smart contracts escritos para cada Vault que le dice qué activos prestar, qué tokens farmear y dónde deberían ser vendidos estos tokens farmeados.

#### ¿Cuáles son las estrategias actuales?

* Puedes ver las estrategias activas para cada Vault en [feel-the-yearn](https://feel-the-yearn.vercel.app/).
* En el futuro tenemos pensado hacer un tablón donde se podrá entender de forma sencilla las estrategias y el APY de cada una de las Vaults.

#### ¿Quién controla las estrategias?

* Andre y otros desarrolladores las escriben pero la multisig decide si son implementadas o no.

#### ¿Cómo puedo hacer una estrategia?

* Por ahora, puedes hacer un post en el foro en la sección de estrategias detallando en qué consiste tu estrategia, es decir, qué debería comprar/vender/farmear y cuál es el rendimiento actual.

#### ¿Cuál es el proceso a seguir para incluir mi estrategia en yearn?

* Publícala en el foro y, si es aprobada, será utilizada en una de las Vaults, además podrás recibir una compensación económica por ello.

#### ¿Cuándo cambia una estrategia y quién lo hace?, ¿es un proceso automático?

* Por ahora, Andre está al corriente de lo que pasa en los mercados y escribe estrategias que él y la multisig piensan que pueden ser seguras y tienen un buen rendimiento. Ellos cambian las estrategias en función de los rendimimentos disponibles en el mercado actual.

### Earn

* [yearn.finance/earn](https://yearn.finance/earn)

#### ¿Qué es Earn?

* Earn es un agregador de rendimientos para plataformas de préstados que se rebalancea para obtener el mayor rendimiento con cada interacción con el contrato.
* Deposita DAI, USDC, USDT, TUSD o sUSD y Earn prestará los fondos automáticamente en la plataforma que ofrezca el mayor rendimiento. Las plataformas donde pueden ser depositados los fondos son [Compound](https://compound.finance/), [Dydx](https://dydx.exchange/) y [Aave](https://app.aave.com/home) \(Ddex y Fulcrum están excluídos de momento\).
* Aprende más sobre Earn en la [documentación de Yearn](https://docs.yearn.finance/yearn.finance/yearn).

### Zap

* [yearn.finance/zap](https://yearn.finance/zap)

#### ¿Qué es Zap?

* Zap permite a los usuarios intercambiar entre distintos tokens en una única transacción reduciendo el coste de gas de esta.
* Los Zaps fueron hechos por DefiZap, ahora conocidos como [Zapper.fi](https://zapper.fi), como un tipo de servicio de enrutamiento todo en uno para DeFi.
* Zaps were made by DefiZap which is now [Zapper.fi](https://zapper.fi) as a type of all in one DeFi routing service.

#### ¿Qué ventajas ofrece Zap?

* "Los Zaps te permiten acceder a una posición de DeFi en una única transacción - conocidas como zapping in." - [Guía de cómo usar Zaps](https://defitutorials.substack.com/p/how-to-use-defizap).
  * Ten en cuenta que este es un artículo antiguo y [Zapper](https://zapper.fi) se formó como resultado de la unión de DeFiSnap + DeFiZap para crear el centro definitivo para las finanzas descentralizadas, también conocido como \#DeFi. Por lo tanto, algunas de las cosas explicadas en el artículo anterior están desactualizadas, pero aún puedes usar Zaps en Zapper.fi.

#### Entonces, ¿qué puedo hacer con Zap en yearn?

* Con un Zap puedes coger, por ejemplo, tus tokens DAI y obtener yCRV con ellos en una única transacción. Normalmente, para convertir DAI en yCRV, tendrías que ir a earn, depositar DAI y recibir yDAI, luego ir a la [pool de Yearn de Curve](https://www.curve.fi/iearn/deposit) y depositar tu yDAI para acabar obteniendo  los tokens yCRV. Esto supone hacer un montón de transacciones, ¡pero con Zap puedes hacerlo en una única transacción!

#### Tiene muy buena pinta, ¿hay alguna desventaja?

* Bueno, se necesita mucho gas y podría ser costoso, incluso más que hacerlo tú mismo manualmente, pero si tienes una transacción grande y tienes prisa, es un excelente método para entrar rápidamente en una posición de DeFi o en una pool de liquidez. .

### yInsure / Cover

* [yinsure.finance](https://yinsure.finance/)

#### ¿Qué es yInsure?

* yInsure, también conocido como **Cover**, es un sistema de cobertura conjunta que proporciona un seguro contra el riesgo de smart contract.
* yInsure no quiere KYC \(identificación del usuario\) y está suscrito a Nexus Mutual.
* Puedes aprender más a cerca de yInsure en este [artículo](https://medium.com/iearn/yinsure-finance-a-new-insurance-primitive-77d5d4217896).

### Productos que actualmente están en Investigación & Desarrollo

#### yTrade

* [ytrade.finance](https://ytrade.finance/)
* Operaciones apalancadas \(leveraged\) con monedas estables \(testnet\).

#### yLiquidate

* [yliquidate.finance](https://yliquidate.finance/)
* Liquidaciones automatizadas de capital para Aave \(testnet\).

#### ySwap

* [yswap.exchange](https://yswap.exchange/)
* Market maker unilateral automatizado \(prueba en mainnet\).

#### yBorrow

* [yborrow.finance](https://yborrow.finance/)
* Vaults de delegación de crédito para smart contracts a contratos de lending \(testnet\).

## Comunicación

* [Foro](https://gov.yearn.finance)
  * Mucha discusión en tiempo real ocurre en Telegram y en Discord, pero para que una propuesta se convierta en una YIP \(Yearn Improvement Proposal\), debe publicarse y discutirse en el foro. 
  * Este es el lugar principal donde los holders de YFI discuten a cerca de problemas relacionados con la gobernanza del protocolo.
* [Discord](http://discord.yearn.finance/)
  * Incluídos canales para hablar en idiomas distintos al inglés.
* [Telegram](https://t.me/yearnfinance) - Canal principal.
* [Telegram](https://t.me/yearncommunity) - Canal de Trading/Social/Forks.
* Twitter
  * [yearn.finance](https://twitter.com/iearnfinance?s=20) - Twitter oficial de Yearn.
  * [Andre Cronje](https://twitter.com/AndreCronjeTech?s=20) - Desarrollador principal de Yearn.
  * [yLearnfinance](https://twitter.com/yLearnfinance) - Información a cerca de Yearn.
  * [Learn 2 Yearn](https://twitter.com/learn2yearn) - Información a acerca de Yearn.

## Gobernanza

### Todo a cerca de las YIPs

#### ¿Qué es una YIP? ¿Por qué son importantes?

* Una propuesta de mejora de Yearn o YIP es la forma de agregar características al ecosistema de Yearn. Los usuarios inician una propuesta en el foro, la discuten y evalúan si la propuesta será aceptada. Si muchos usuarios están de acuerdo con la propuesta, se puede publicar on-chain para que todos puedan votarla.

#### ¿Cuánta gente tiene que votar para que una YIP sea aprobada on-chain?

* El quorum es del 20%. Esto significa que el 20% de los tokens YFI stakeados deben votar la propuesta para que pase, o esta fracasará. Además, la propuesta debe tener al menos el 50% de los votos a favor.
* Puedes publicar tu propuesta on-chain primero, pero si la gente no ha discutido a cerca de ella primero probablemente no votarán.

#### ¿Cómo puedo hacer una propuesta?

* Puedes encontrar la plantilla para las propuestas en [Github](https://github.com/iearn-finance/YIPS/blob/master/yip-X.md) y en el [foro](https://gov.yearn.finance) si creas un post en la sección de propuestas o discusión, la plantilla se cargará automáticamente.
* El proceso consiste básicamente en:
  1. dicusión en el foro
  2. promoción a YIP \(normalmente hecho por los mods\), añadir la YIP a Github, enviarla para ser votada on-chain
  3. anunciarla

#### ¿Quién puede hacer una propuesta?

* Cualquier persona puede crear una propuesta en el foro y on-chain.

### Votaciones

#### ¿Cómo puedo votar?

* Stakea tus tokens YFI y entonces podrás votar por YIPs on-chain en el [tablón de votaciones](https://ygov.finance/vote).

#### ¿Puedo votar si tengo mis tokens YFI en la Vault de YFI?

* No, tus tokens YFI deben estar stakeados en el [contrato de gobernanza](https://ygov.finance/staking) para poder votar.

#### ¿Dónde puedo ver las YIPs?

* Puedes verlas en el [tablón de votaciones](https://ygov.finance/vote) si conectas tu cuenta web3 o en [yips.yearn.finance](https://yips.yearn.finance/all-yip).

#### ¿Por qué debería stakear? ¿Cuál es el APY \(Porcentaje de rendimiento anual\)?

* Deberías stakear si quieres votar por YIPs y recibir recompensas que son generadas del ecosistema de Yearn. El APY por stakear no se muestra ahora mismo en el UI. Puedes preguntar en el chat cuál es el valor actual.

#### ¿Qué tengo que hacer para recibir recompensas con mis tokens YFI?

* Todo lo que tienes que hacer es stakear tus tokens YFI en [ygov.finance/stake](https://ygov.finance/stake) y recibirás recompensas si el tesoro del protocolo tiene más de $500k. Puedes consultar la cuenta del tesoro [aquí](https://zapper.fi/dashboard?address=0xFEB4acf3df3cDEA7399794D0869ef76A6EfAff52).
* Fíjate que si stakeas, obtienes recompensas \(siempre y cuando no estén yendo al tesoro\), pero sólo puedes reclamarlas dentro de un intervalo de 3 días después de votar.

#### A la hora de votar, ¿es importante tener stakeados mis tokens YFI?

* Sí. Necesitas stakear tus tokens YFI en [ygov.finance/stake](https://ygov.finance/stake) en la sección Governance V2 para que tus votos cuenten. Ahora mismo, puedes votar sin stakear, pero solamente gastarás gas y no se tendrá en cuenta tu voto, así que asegúrate de stakear primero si quieres votar.

#### ¿Qué pasa si quiero retirar mis tokens YFI antes de que acabe el período de espera?

* No puedes, lo siento. El bloqueo dura 3 días después de tu última votación, hasta que acabe no puedes retirar tus tokens.
* Si intentas retirar tus tokens antes de que acabe el período de espera podrás comprobar que el coste de gas de la transacción será muy alto. Esto no significa que si lo pagas podrás retirar tus tokens, sino que la transacción fallará y tendrás que esperar hasta que acabe el período de espera de 3 días.

#### He votado y sé que el período de espera es de 3 días, ¿hay algún sitio donde pueda ver exactamente cuánto tiempo queda para poder retirar mis tokens YFI?

* ¡Sí! puedes leerlo directamente en el [contrato](https://etherscan.io/address/0xBa37B002AbaFDd8E89a1995dA52740bbC013D992#readContract) de staking. Ve al input 28 \(votelock\) y escribe la dirección de tu cuenta de ETH, te dirá el bloque exacto a partir del cual podrás retirar tus tokens.

#### ¿Cuál es la diferencia entre votar en una encuesta y una votación on-chain?

* Una encuesta solo mide el sentimiento de lo que la comunidad piensa sobre la propuesta, mientras que una votación on-chain será vinculante y entrará en vigencia si se aprueba.

#### ¿De qué va el nuevo sistema de votación que no cuesta gas?

* Ahora tenemos un sistema de señalización off-chain que utiliza los tokens stakeados en ygov. Esto reemplaza las antiguas encuestas del foro que  eran informales y vulnerables a los ataques de sybil. Puedes elegir entre opciones múltiples y no cuesta gas usarlo, unicamente tienes que firmar un mensaje con tu wallet que no cuesta nada. Seguimos utilizando el sistema de votación on-chain normal para las YIPs.

#### ¿Durante cuánto tiempo estarán bloqueados mis tokens YFI después de votar?

* Tus tokens YFI estarán bloqueados durante 3 días después de votar.

#### ¿¡Por qué no puedo reclamar mis recompensas de staking!?

* Para poder reclamar tus recompensas de staking tienes que: 1\) haber stakeado tokens 2\) haber votado en los últimos 3 días. Esto será cambiado en una futura actualización.

### yDAO

* [Sitio](https://pokemol.com/dao/0xcb46298767fb5d44c18313976c30d3eeb5071862/) de Pokemol.
* [Hilo](https://gov.yearn.finance/t/ydao-for-community-funding/2243) en el foro oficial.

#### ¿Cuál es su utilidad/propósito/objetivo?

* Su objetivo es el de financiar contribuciones valiosas al ecosistema de yearn.

#### A quién le importa, ¿Cómo puedo hacer dinero de esto?

* No puedes. Su único objetivo es el de financiar projectos, los tokens YFI donados serán gastados y el valor de tu acción se diluirá.

#### ¿Quién puede unirse?

* Cualquier persona puede unirse adquiriendo una acción por 0.1 YFI.

#### ¿Cómo puedo unirme?

* Ve a [Pokemol](https://pokemol.com/dao/0xcb46298767fb5d44c18313976c30d3eeb5071862) y regístrate con tu cuenta web3. Has click en "New Proposal" arriba a la derecha. Has click en "member".
  * Title: tu nombre/entidad.
  * Description: “Pledging X amount of YFI in exchange for Y Shares” \(Por favor, haga que esto sabiendo que cada acción cuesta 0.1 YFI\).
  * Link: Link a tu \(Página web, Twitter, Linkedin\) o la de tu entidad.
  * Shares Requested: Número de acciones que se quieren adquirir.
  * Token Tribute: La cantidad de YFI que vas a pagar.
  * Loot: Número de acciones que quieres adquirir.
  * After you submitted the two transactions and are in the new member queue, you will need a sponsor. Please copy the link to your proposal and let us know you’d like to join in the [yDAO Telegram channel](https://t.me/joinchat/Qn1GPBv0y7lY1vAmRCB7KA)
  * Después de enviar las dos transacciones necesarias y estés en la cola de miembros nuevos, necesitarás un patrocinador.

#### ¿Cómo puedo solicitar financiación?

* The same ways as joining except instead of click member click the funding tab and fill in the details of your request. You can ask in the [telegram chat](https://t.me/joinchat/Qn1GPBv0y7lY1vAmRCB7KA) if you have any questions.

#### No hablo inglés, ¿Cuándo estará todo disponible en otros idiomas?

* We are working on translating to other languages but it will take time. For now you can go to your language in the global section in [Discord](http://discord.yearn.finance/).

## Comunidad

### ¿Está Andre Cronje a cargo de yearn?

* Andre isn't in charge of Yearn, the YFI token holders make the decisions on what to build and governance decisions, Andre is the lead developer of the yearn ecosystem.

### ¿Qué es lo que hace Andre?

* Andre is the main developer building out the products that comprise the yearn ecosystem: Yearn, Ytrade, Yswap, Yliquidate, Yborrow. He is also currently in charge of running the Vaults and overseeing them.

### ¿Qué es la multisig y cuáles son sus funciones?

* The multi-signature address is explained in detail in this [thread](https://gov.yearn.finance/t/yfi-minting-ownership/155). Basically, it is a 6 of 9 multi-signature account that has control over minting YFI if a vote to mint tokens has passed successfully.

### ¿Quiénes son los 9 firmantes de la multisig?

* [Cp0x.com](https://twitter.com/kaplansky1/status/1285427247286046725)
* [Daryllautk](https://twitter.com/Daryllautk/status/1285434908383444992)
* [Devops199fan](https://twitter.com/devops199fan/status/1285430347954622464)
* [Banteg](https://twitter.com/bantg/status/1285426492906909696)
* [Milkyklim](https://milkyklim.keybase.pub/yearn-social-proof.txt)
* [Joe Mahon aka Substreight](https://twitter.com/Substreight/status/1299780260737630209)
* [Tarun Chitra, Gauntlet](https://twitter.com/gauntletnetwork/status/1299778153674616833)
* [Vasiliy Shapovalov, p2p.org](https://twitter.com/_vshapovalov/status/1299799139635679232)
* [Mariano Conti, ex-MakerDAO](https://twitter.com/nanexcool)

### ¿Se ha cambiado en alguna ocasión alguno de los firmates de la multisig?

* Yes, [YIP-40](https://gov.yearn.finance/t/yip-40-replace-inactive-multisig-signers/3535) changed four of the signers
* Outgoing signers were:
  * [Coopahtroopa](https://twitter.com/Cooopahtroopa/status/1285438650550038529)
  * [Michael, Curve.fi](https://twitter.com/CurveFinance/status/1285428322986389504)
  * [Calvin Liu](https://twitter.com/cjliu49/status/1285439553180798976)
  * [Damir Bandalo](https://twitter.com/damirbandalo/status/1285500362015875073)

### ¿Qué decisiones puede tomar Andre por su cuenta?

* Andre can build out the Yearn ecosystem and come up with new products. Usually, he posts his thoughts and ideas on the [forum](https://gov.yearn.finance) for everyone to see.

### ¿Los integrantes de la multisig le dicen a él lo que tiene que hacer?

* They are in close contact with one another, but Andre's priorities are decided by YFI token holders via YIPs.

### ¿Quién más escribe código para yearn? ¿Hay algún equipo?

* Right now it's just Andre.

### ¿Le pagan a alguien por trabajar en yearn?

* As of this moment, not yet, but thanks to the passage of [YIP 36](https://yips.yearn.finance/YIPS/yip-36) and the creation of a community pool of funds that will be kept at 500k usd, we can now pay Andre for his work, fund audits, and pay for new devs to be hired along with anything else the the yearn ecosystem needs.

### ¿Quién puede trabajar para yearn?

* You can make a YIP to apply for funding from the 500k USD treasury directly or ask the yDAO for funding.

### ¿Tenéis alguna oferta de trabajo abierta?

* Yes, we do! We need all kinds of people to help make the yEarn ecosystem a thriving product and to give value to YFI. You can ask in the Discord or Telegram about applying or post on the forum. State how you think you can add value to Yearn, and how much you think you should be paid from the community pool. Also, you can go to the [yDAO](https://gov.yearn.finance/t/ydao-for-community-funding/2243) as well for funding on your work for the Yearn ecosystem.

### ¿Cómo puedo participar?

* You can participate in YFI by voting on YIPs that are active, discussing the YIPs yet to be proposed on-chain on the forums and talking about YFI in the Telegram and Discord. If you know a second language help us translate the site and YIPs into that language.

### Esfuerzos puestos en marcha para mejorar el ecosistema de Yearn

* You can view the active YIPs [here](https://yips.yearn.finance/all-yip)

## Interfaz de usuario

### ¿Puedo usar las dApps de yearn en mi teléfono móvil?

* Sí, puedes hacerlo si tienes un buscador con Metamask instalado.

## Soporte técnico

### I sent my ETH transaction but it says pending? How do I fix this? He enviado una transacción de ETH pero dice que está pendiente, ¿qué puedo hacer para arreglarlo?

* You should always make sure to set your gas properly if you want a transaction to go through quickly. Check current gas prices at [Ethgasstation](https://ethgasstation.info/) or [gasnow](https://www.gasnow.org/).
* If you're using MetaMask and you put your transaction through but it's going too slow, you have the option to speed it up by clicking the `speed up` button below your last pending transaction under "activity". This should resend the same TX again with a higher gas price to get it confirmed faster.
* If you've tried everything and your transaction is still stuck pending, you can fix it by sending a transaction to the nonce of the first stuck transaction with a high gas price to overwrite the stuck queue. Here's a good [guide](https://ethgasstation.info/blog/stuck-transaction-guide) explaining how to do this.

### ¿Por qué la tarifa de retiro es tan alta?

* Si ves que la tarifa es más alta de lo normal cuando vas a usar algún producto del ecosistema de yearn puede ser por congestión en Ethereum que se traduce en un coste anormalmente alto del gas. Puedes comprobar el valor óptico del precio del gas en [Ethgasstation](https://ethgasstation.info/). Tus opciones son esperar a que los precios del gas bajen o pagar el precio del gas para enviar tu transacción ahora.
* Si los precios del gas son una locura, eso significa que hay un error y la transacción no se procesará. Por ejemplo, si intentas depositar un token que no tienes o no hay covertura disponible para un contrato en [http://yinsure.finance/](http://yinsure.finance/).

## Projectos relacionados

### [Curve](https://www.curve.fi)

* Curve is an exchange liquidity pool on Ethereum \(like [Uniswap](https://app.uniswap.org/#/)\) designed for \(1\) extremely efficient stablecoin trading \(2\) low risk, supplemental fee income for liquidity providers, without an opportunity cost. Curve allows users \(and smart contracts like 1inch, Paraswap, Totle and Dex.ag\) to trade between DAI and USDC with a bespoke low slippage, low fee algorithm designed specifically for stablecoins and earn fees. Behind the scenes, the liquidity pool is also supplied to the Compound protocol or yearn.finance where it generates even more income for liquidity providers.
* Curve [FAQ](https://www.curve.fi/rootfaq).

### [Aave](https://app.aave.com/home)

* Aave es un protocolo de código abierto y descentralizado que permite la creación de money makers. Los usuarios pueden ganar intereses sobre depósitos y prestar activos.

## Recursos

### ¿Dónde puedo aprender más sobre yearn?

* [Learn Yearn](https://www.learnyearn.finance/)
* [Medium.com/iearn](https://medium.com/iearn)
* [yCosystem](https://ycosystem.info/)

### Lista de Smart Contracts relacionados con productos de yearn

* [https://gov.yearn.finance/t/yearn-contracts/1951](https://gov.yearn.finance/t/yearn-contracts/1951)
* [https://etherscan.io/accounts/label/yearn-finance](https://etherscan.io/accounts/label/yearn-finance)
  * Es necesario registrarte.
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

### Registro de tokens y demás contratos

* [https://docs.yearn.finance/yearn.finance/yearn-1](https://docs.yearn.finance/yearn.finance/yearn-1)

### Vaults Detail Reference

* [https://vaults.finance/](https://vaults.finance/)

### Estadísticas

* [yieldfarming.info](https://yieldfarming.info/)
* [yVault ROI Calculator](https://py-earn.herokuapp.com/)
* [stats.finance/yearn](https://stats.finance/yearn)
* [Feel The Yearn](https://feel-the-yearn.vercel.app/)
* Distribución inicial [Dune Dashboard](https://explore.duneanalytics.com/dashboard/yearn)
* Estadísticas de votación [Dune Dashboard](https://explore.duneanalytics.com/public/dashboards/Lqnxzm7fa8NVhKC4kc37DDFPZgqXryaIjyLRYAYp)
* Estadísticas de las Vaults [Dune Dashboard](https://explore.duneanalytics.com/public/dashboards/g0bGfgloeXBd9C18jpBjdXi5KkQjR7IXYqFRUnHk)

### Últimas noticias sobre yearn

* [yearn.finance](https://twitter.com/iearnfinance) - Twitter oficial de yearn
* [AndreCronjeTech](https://twitter.com/AndreCronjeTech)
* [Yearn Finance](https://medium.com/iearn) -  Blog oficial

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

* Pueden encontrarse en el Discord en el canal [\#media-resources](https://discord.com/channels/734804446353031319/736132884443955242/740325105904779326)

