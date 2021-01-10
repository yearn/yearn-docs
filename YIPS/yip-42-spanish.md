---
YIP: 42
Título: Añadir renBTC a yVaults	
Estado: Rechazada 
Autor: Azeem (@zu-ctrl)
Discusiones: https://gov.yearn.finance/t/proposal-yrenbtc-delegated-vault/3470
Implementación: https://github.com/zu-ctrl/yfi-str-pub/blob/master/StrategyCreamRENBTC.sol
Fecha de creación: 08/26/2020
---
<!--You can leave these HTML comments in your merged SIP and delete the visible duplicate text guides, they will not appear and may be helpful to refer to if you edit it again. This is the suggested template for new SIPs. Note that an SIP number will be assigned by an editor. When opening a pull request to submit your SIP, please use an abbreviated title in the filename, `sip-draft_title_abbrev.md`. The title should be 44 characters or less.-->

## Explicación corta
<!--"If you can't explain it simply, you don't understand it well enough." Simply describe the outcome the proposed changes intends to achieve. This should be non-technical and accessible to a casual community member.-->
Añadir renBTC como un activo volátil para ser usado como aval en una yVault delegada.

## Resumen
<!--A short (~200 word) description of the proposed change, the abstract should clearly describe the proposed change. This is what *will* be done if the SIP is implemented, not *why* it should be done or *how* it will be done. If the SIP proposes deploying a new contract, write, "we propose to deploy a new contract that will do x".-->
Añadir renBTC como un activo volátil para ser usado como aval en una yVault delegada.

## Motivación
<!--This is the problem statement. This is the *why* of the SIP. It should clearly explain *why* the current state of the protocol is inadequate.  It is critical that you explain *why* the change is needed, if the SIP proposes changing how something is calculated, you must address *why* the current calculation is innaccurate or wrong. This is not the place to describe how the SIP will address the issue!-->

wBTC tiene tasas de crecimiento bastante buenas como se puede ver en DeFi Pulse, pero como solución de custodia se ve obstaculizada por sistemas basados en la confianza con los que los holders de BTC no se sienten cómodos en general.

RenBTC es una representación tokemizada de BTC en la blockchain de Ethereum. Es un ERC20 y está respaldado 1: 1 con BTC real custodiado en RenVM, un custodio descentralizado. Se puede canjear en cualquier momento por BTCs reales.

Cuando Curve creó una oportunidad para que RenBTC generara retornos, el TVL de RenVM creció muy deprisa. Esta es una señal clara de que cuando la solución correcta está disponible, hay MUCHOS BTCs esperando para saltar y farmear en ETH. Estemos ahí para ellos.

Consulte el hilo con una mayoría abrumadora A FAVOR del enfoque estratégico en BTC. Este es un voto para aprobar la estrategia actual, para que entre en funcionamiento y comience a generar retornos para los depositantes de RenBTC sin obligarlos a averiguar cómo funcionan los depósitos de Curve. 

## Especificación
<!--The specification should describe the syntax and semantics of any new feature, there are five sections-->

La estrategia propuesta para los modelos anteriores es la estrategia actual de la Vault de YFI la cual farmea CREAM y compra más YFI vendiendo CREAM. Necesitaremos una nueva Vault que acepte depósitos de RenBTC.

> Estrategia 1:
* Agregar una nueva Vault que acepte RenBTC 
* Los usuarios depositan RenBTC, comienzan a farmear CREAM  y se devuelven las ganancias a los depositantes como renBTC, siguiendo la misma estrategia de la Vault de YFI.

**A FAVOR:** Añadir una nueva Vault de renBTC e implementar la Estrategia 1 - StrategyCreamRENBTC.

**EN CONTRA:** Sin cambios.

## Derechos de autor
Derechos de autor y derechos relacionados con renuncia a través de [CC0](https://creativecommons.org/publicdomain/zero/1.0/).

