---
YIP: 10
Título: Transición a un sistema de votación basado en YFI
Estado: Implementada
Autor: Rewkang (@rewkang)
Discusiones: https://gov.yearn.finance/t/yip-10-transitionary-yfi-only-voting/481
Fecha de creación: 2020-07-24
Implementación: https://etherscan.io/address/0xBa37B002AbaFDd8E89a1995dA52740bbC013D992
---

## Explicación corta
<!--"If you can't explain it simply, you don't understand it well enough." Simply describe the outcome the proposed changes intends to achieve. This should be non-technical and accessible to a casual community member.-->
El actual sistema de gobernanza de yEarn pone el protocolo en peligro de caer en manos de agentes hostiles. La mejor acción que se puede tomar de inmediato es transladar temporalemente el protocolo a un nuevo sistema de votación controlado por un contrato desplegado por Andre.

## Resumen
<!--A short (~200 word) description of the proposed change, the abstract should clearly describe the proposed change. This is what *will* be done if the YIP is implemented, not *why* it should be done or *how* it will be done. If the YIP proposes deploying a new contract, write, "we propose to deploy a new contract that will do x".-->
Actualizar la página de votación ygov.finance para que redirija al nuevo sistema de votación controlado por un contrato donde sólo se puede stakear YFI.

Contrato: [Etherscan](https://etherscan.io/address/0xad7e09665caa3404d9c6525d5997a10fc6c12cfe)

## Motivación
<!--This is the problem statement. This is the *why* of the YIP. It should clearly explain *why* the current state of the protocol is inadequate.  It is critical that you explain *why* the change is needed, if the YIP proposes changing how something is calculated, you must address *why* the current calculation is innaccurate or wrong. This is not the place to describe how the YIP will address the issue!-->

El contrato de votación actual de yEarn acepta BTP (Balancer Pool Tokens) de una pool consistente en 98% yCRV / 2% YFI. Esto ha creado una dinámica donde poseedores de grandes cantidades de monedas estables tienen una cantidad desproporcionada de poder de voto y, por tanto, de poder sobre la gobernaza, mientras que aquellas personas con una mayor proporción de YFI vs. monedas estables están subrepresentadas en la gobernanza. La gobernanza debe ser dictada por aquellos con intereses a largo plazo en el protocolo - los poseedores de YFI - sin importar la composición de sus portafolios. Además de esto, el protocolo es ahora mismo muy vulnerable a un intento hostil de grandes poseedores de monedas estables por hacerce con el control de la gobernanza para crear más YFI y lucrarse. 

Hay múltiples formas de afrontar el sistema de votación/gobernanza del protocolo a largo plazo que se están debatiendo, por lo que llevará algo de tiempo lograr un consenso en la comunidad. Mientras esto se analiza y se discute, deberíamos transicionar inmediatamente a una estructura de gobernanza temporal donde sólo YFI se puede utilizar para votar, mitigando de esta manera las posibles acciones hostiles contra el protocolo. 

La comunidad podrá reemplazar esta estructura temporal de votación aprobando una nueva YIP en el futuro.

**A FAVOR**:  La gobernanza pasa a depender del nuevo contrato donde se puede votar únicamente con YFI.

**EN CONTRA**: No hay cambios en la gobernanza.

## Metadatos

| Nombre                | Valor                                      |
|---------------------|--------------------------------------------|
| Propuesta por         | 0x09173487b272311Edda01F45f97911aEB6aBd602 |
| Votos totales a favor     | 13641124.8956 (77.08%)                     |
| Votos totales en contra | 4054142.5578 (22.91%)                      |
| Quorum              | 45.92% ✔                                   |
| Bloque inicial         | 10518707                                   |
| Bloque final           | 10535987                                   |

Fuente: [yieldfarming.info YFI Governance Information](https://yieldfarming.info/yearn/vote/)

## Derechos de autor
Derechos de autor y derechos relacionados con renuncia a través de [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
