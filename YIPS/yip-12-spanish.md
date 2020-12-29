---
YIP: 12
Título: Reducción del quorum para aceptar una propuesta
Estado: Implementada
Autor: cp287 (@illlefr4u)
Discusiones: https://gov.yearn.finance/t/yip-12-reducing-the-quorum-for-accepting-proposal/578
Fecha de creación: 2020-07-24
Implementación: https://etherscan.io/tx/0x64ff868305c1271c51b85a4f69f547f3137bebeae611eff1e0a2d86714469b77#
---

## Explicación corta
<!--"If you can't explain it simply, you don't understand it well enough." Simply describe the outcome the proposed changes intends to achieve. This should be non-technical and accessible to a casual community member.-->
Ahora mismo es complicado para el mecanismo de gobernanza de yEarn conseguir el 33% de quorum. Para que el sistema de control funcione, el umbral debe ser reducido para que se puedan tomar algunas decisiones.

## Resumen
<!--A short (~200 word) description of the proposed change, the abstract should clearly describe the proposed change. This is what *will* be done if the YIP is implemented, not *why* it should be done or *how* it will be done. If the YIP proposes deploying a new contract, write, "we propose to deploy a new contract that will do x".-->

Se propone reducir el quorum para aceptar una propuesta al 20%.
En este momento, ningún cambio on-chain es necesario dado que la comprobación del quorum mínimo se hace off-chain. Por tanto, bastará con aprobar la decisión en una votación on-chain.

## Motivación 
<!--This is the problem statement. This is the *why* of the YIP. It should clearly explain *why* the current state of the protocol is inadequate.  It is critical that you explain *why* the change is needed, if the YIP proposes changing how something is calculated, you must address *why* the current calculation is innaccurate or wrong. This is not the place to describe how the YIP will address the issue!-->

En estos momentos, es complicado para el mecanismo de gobernanza de yEarn llegar al quorum del 33%. Un claro ejemplo se pudo ver en la importante propuesta 1 que no consiguió llegar al quorum.
Esto se debe a:
- la pasividad y falta de motivación para participar en la gobernanza;
- los incentivos negativos para participar (bloqueo de fondos).

Por esto, yEarn está bajo la amenaza de quedarse como está para siempre consecuencia de no poder llegar al quorum mínimo requerido (con muy alta probabilidad, la participación en las votación disminuirá con el tiempo).

Hay varias soluciones a este problema, las cuales describo más abajo, y propongo empezar a discutir sobre ellas, pero es crítico en estos momentos tomar una sencilla decisión para que el protocolo siga avanzando y así la comunidad pueda seguir tomando decisiones sobre cúal será el camino de desarrollo del protocolo.
Bajo mi punto de vista, dicha decisión es reducir el quorum mínimo al 20%, la cual propongo para su votación.

Otras formas de abarcar el problema del quorum podrían ser:

- distribuir recompensas sólo si se participa en las votaciones;
- delegación de votos (implementar esto puede llevar algo de tiempo);
- el quorum no debe ser un % de TODOS los tokens, sino un % de aquellos que están “en custodia” para votar;
- debería haber un calendario de quorum mediante el cual se reduzca el quorum 1%-2% el primer año si después de x tiempo ninguna propuesta llega al quorum, 0.5%-1% el segundo año, etc

**A FAVOR**: El quorum mínimo para aceptar una propuesta se reduce al 20%

**EN CONTRA**: No hacer ningún cambio al quorum mínimo requerido.

## Metadatos

| Nombre                | Valor                                      |
|---------------------|--------------------------------------------|
| Propuesta por         | 0x74630370197b4c4795bFEeF6645ee14F8cf8997D |
| Votos totales a favor     | 5291919.8701 (66.22%)                      |
| Votos totales en contra | 2699427.0543 (33.77%)                      |
| Quorum              | 39.76% ✔                                   |
| Bloque inicial         | 10522307                                   |
| Bloque final           | 10539587                                   |

Fuente: [yieldfarming.info YFI Governance Information](https://yieldfarming.info/yearn/vote/)

## Derechos de autor
Derechos de autor y derechos relacionados con renuncia a través de [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
