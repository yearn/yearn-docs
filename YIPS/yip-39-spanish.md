---
YIP: 39
Título: Añadir el token LP de la pool de sBTC de Curve a una yVault
Estado: Implementada
Autor: uhmpeps (@az)
Discusiones: https://gov.yearn.finance/t/proposal-add-curve-sbtc-pool-lp-tokens-yvault/3251

Fecha de creación: 08/23/2020
---

<!--You can leave these HTML comments in your merged SIP and delete the visible duplicate text guides, they will not appear and may be helpful to refer to if you edit it again. This is the suggested template for new SIPs. Note that an SIP number will be assigned by an editor. When opening a pull request to submit your SIP, please use an abbreviated title in the filename, `sip-draft_title_abbrev.md`. The title should be 44 characters or less.-->

## Explicación corta
<!--"If you can't explain it simply, you don't understand it well enough." Simply describe the outcome the proposed changes intends to achieve. This should be non-technical and accessible to a casual community member.-->

Capturar hasta $ 214 mil millones en AUM de los holders de BTC que quieren incrementar pasivamente su BTC utilizando una parte del poder de voto para aumentar las recompensas de CRV de la pool de sBTC y crear una vault para los participantes de la pool de sBTC de Curve que depositen renBTC / wBTC / sBTC en dicha pool. Esto puede atraer a los holders de Bitcoin que pueden no estar al corriente de otros usos que pueden dar a su Bitcoin.

Es la pool de sBTC de Curve que acepta renBTC / wBTC / sBTC que son igualmente aceptables y tiene el potencial de dar la mayor cantidad de recompensas.
Solo necesitamos aceptar el token LP, que es un tipo de token único que se entrega a cualquiera que deposite cualquier tipo de wrapped BTC en la pool de Curve.

## Resumen
<!--A short (~200 word) description of the proposed change, the abstract should clearly describe the proposed change. This is what *will* be done if the SIP is implemented, not *why* it should be done or *how* it will be done. If the SIP proposes deploying a new contract, write, "we propose to deploy a new contract that 
will do x".-->

Crear una vault para depositantes de tokens LP de la pool de sBTC de Curve que funcionará de manera casi idéntica a las vaults de yCRV y yYFI. Farmear tokens CRV, venderlos por más tokens LP o renBTC que luego se vuelven a depositar para crear, distribuir y componer el crecimiento del token LP.


## Motivación
<!--This is the problem statement. This is the *why* of the SIP. It should clearly explain *why* the current state of the protocol is inadequate.  It is critical that you explain *why* the change is needed, if the SIP proposes changing how something is calculated, you must address *why* the current calculation is innaccurate or wrong. This is not the place to describe how the SIP will address the issue!-->

La ventaja del más ágil. Hay espacio suficiente para ganarnos la confianza de los holders de bitcoins ($ 214 mil millones en AUM potenciales) mediante el uso de nuestro poder de voto para aumentar las recompensas de la pool de sBTC de Curve, y para crear el primer mecanismo completamente pasivo para que los holders de BTC aumenten sus Bitcoins. En este momento, sólo los holders de BTC más confiados están depositando y reciclando / farmeando CRV. Esto puede convertirse en un agujero negro para los depósitos de BTC en Curve a través de tokens renBTC y LP en yVault para ganar intereses pasivos e ingresos para la gobernanza.

## Especificación
<!--The specification should describe the syntax and semantics of any new feature, there are five sections
1. Overview
2. Rationale
3. Technical Specification
4. Test Cases
5. Configurable Values
-->

[1]

* Añadir una nueva Vault para los holders de tokens LP que depositaron fondos en la pool de sBTC de Curve con un nombre apropiado (ahora mismo no sé cómo se llama el token LP de esa pool)
* Cuando un usuario deposita el token LP de la pool de sBTC, el sistema stakea el token LP en el DAO de Curve y farmea CRV
* Tras la recepción y venta de CRV en el mercado, el sistema compra más tokens LP si hay liquidez / pools disponibles, o compra renBTC o sBTC
* Luego, xBTC se deposita de nuevo en la pool de sBTC de Curve, se generan tokens LP, que se muestran en la tabla para depositantes como ganancias, y mientras tanto, los tokens LP se depositan de nuevo en Curve DAO para seguir generando más CRV

[2]

* Usar parte del poder de voto en el DAO de Curve para aumentar las recompensas de CRV para que los depositantes de BTC ganen alrededor de 50-70% APY, haciendo que sea muy atractivo para los holders de BTC
* Asegurarse de que la yVault se publicita a las audiencias adecuadas como una alternativa viable a la posesión de una roca no funcional que no tiene ningún otro propósito actualmente.

**A FAVOR:** Añadir una nueva Vault para la pool de sBTC de Curve.

**EN CONTRA:** Ningún cambio.
