---
YIP: 36
Título: Recompensas del sistema como capital operativo
Estado: Implementada
Autor: Andre Cronje (@andrecronje), iTo, n00b (@jchi18), Artem K (@banteg)
Discusiones: https://gov.yearn.finance/t/system-rewards-as-operational-capital/1974

Fecha de creación: 2020-08-10
---

## Explicación corta

Asignar las recompensas del sistema como capital operacional para gastos del protocolo en vez de enviarlas a la gobernanza.

## Resumen

Cubrir los gastos operacionales sin necesidad de crear más YFI.

## Motivación

La comunidad de YFI está trabajando con Delphi y Gauntlet para desarrollar un modelo económico y un calendario de inflación. Hasta que este proceso sea completado, el proyecto necesitará fondos para cualquier gasto operacional incluyendo, pero no exclusivamente, auditorías de seguridad, costos de implementación, gastos de consultoría y compensaciones. 

Con el actual estado del mercado, las recompensas generadas por el sistema son suficientes para cubrir estos gastos operacionales. Esta YIP propone que las recompensas generadas por el protocolo sean dirijadas a la Multisig en vez de a la gobernanza. De esta forma, se pueden cubrir los gastos operacionales sin necesidad de crear más YFI.

**A FAVOR:** Usar las recompensas del protocolo para gastos operacionales almacenándolas en un tesoro de capacidad máxima \$500k. Cualquier excedente será distribuído entre los participantes en la gobernanza. 

**EN CONTRA:** Seguir dirijiendo las recompensas a la gobernanza.

## Especificación

El 100% de las recompensas generadas por el sistema serán dirijidas al tesoro de la Multisig.

El tesoro debe mantener un colchón equivalente a 500.000 USD. El excedente será distribuido entre los stakers de YFI en el contrato de gobernanza.

## Metadatos

| Nombre                | Valor                                      |
|---------------------|--------------------------------------------|
| Propuesta por         | 0x24394A4758DBdCf6fcbC14dc35af64Ac0D9a450A |
| Votos totales a favor     | 2002.4442 (94.51%)                         |
| Votos totales en contra | 116.1982 (5.48%)                           |
| Quorum              | 45.11% ✔                                   |
| Bloque inicial         | 10633194                                   |
| Bloque final           | 10650474                                   |

Fuente: [yieldfarming.info YFI Governance Information](https://yieldfarming.info/yearn/vote/)

## Derechos de autor

Derechos de autor y derechos relacionados con renuncia a través de [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
