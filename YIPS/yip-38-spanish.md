---
YIP: 38
Título: Distribuir / Conservar las recompensas de Balancer
Estado: Implementada
Autor: Klim K (@milkyklim)
Discusiones: https://gov.yearn.finance/t/yip-38-distribute-keep-balancer-rewards/2436

Fecha de creación: 08/18/2020
---

<!--You can leave these HTML comments in your merged SIP and delete the visible duplicate text guides, they will not appear and may be helpful to refer to if you edit it again. This is the suggested template for new SIPs. Note that an SIP number will be assigned by an editor. When opening a pull request to submit your SIP, please use an abbreviated title in the filename, `sip-draft_title_abbrev.md`. The title should be 44 characters or less.-->

## Explicación corta
<!--"If you can't explain it simply, you don't understand it well enough." Simply describe the outcome the proposed changes intends to achieve. This should be non-technical and accessible to a casual community member.-->

Quedarse con los tokens $BAL obtenidos como parte del capital operacional en vez de distribuirlos a los stakers de la antigua pool de gobernanza de $BPT.


## Resumen
<!--A short (~200 word) description of the proposed change, the abstract should clearly describe the proposed change. This is what *will* be done if the SIP is implemented, not *why* it should be done or *how* it will be done. If the SIP proposes deploying a new contract, write, "we propose to deploy a new contract that will do x".-->

Unos ~891 $BAL tokens (~18500$) fueron enviados a una de las antiguas pools de distribución. Esos tokens han sido confiscados y fueron depositados en la wallet de la multisig. Tenemos que decidir entre distribuirlos o quedárnoslos y usarlos como capital operacional.

## Motivación
<!--This is the problem statement. This is the *why* of the SIP. It should clearly explain *why* the current state of the protocol is inadequate.  It is critical that you explain *why* the change is needed, if the SIP proposes changing how something is calculated, you must address *why* the current calculation is innaccurate or wrong. This is not the place to describe how the SIP will address the issue!-->
Dado que los tokens $BAL pertenecen a los stakers de BPT (balancer pool token) es esencial decidir qué deberíamos hacer con estos tokens.

Sin embargo, la cantidad de $BAL incautada es 3 veces menor que las ganancias generadas por el protocolo en una semana ($18k vs $60k). Por tanto, propongo que los tokens $BAL se queden en la wallet de la multisig y que cuenten como capital operativo, en vez de construir un contrato para que puedan ser reclamados - esta solución ahorra tiempo y gas.

## Especificación
<!--The specification should describe the syntax and semantics of any new feature, there are five sections
1. Overview
2. Rationale
3. Technical Specification
4. Test Cases
5. Configurable Values
-->

### Visión de futuro
<!--This is a high level overview of *how* the SIP will solve the problem. The overview should clearly describe how the new feature will be implemented.-->

El staker más grande recibiría aproximadamente el 31% del total de tokens $BAL, como puede verse en la siguiente gráfica: 

https://explore.duneanalytics.com/embed/query/7901/visualization/15749?api_key=8AAmxEmXrkxj56sw0hjDtrVbMN7jZtmsZ6SmZfFo 

A pesar de que pueda parecer una cantidad grande, hay un montón de pequeños stakers que recibirían menos de 8$. Teniendo en cuenta los precios del gas y el hecho de que la gente tenga que reclamar su $BAL ellos mismos, sostengo que es más razonable quedarnos con los tokens $BAL y usarlos como capital operativo para el protocolo.

Además, esta propuesta ahorra tiempo ya que nos ahorramos la implementación de un contrato de distribución personalizado.


### Razonamiento fundamental
<!--This is where you explain the reasoning behind how you propose to solve the problem. Why did you propose to implement the change in this way, what were the considerations and trade-offs. The rationale fleshes out what motivated the design and why particular design decisions were made. It should describe alternate designs that were considered and related work. The rationale may also provide evidence of consensus within the community, and should discuss important objections or concerns raised during discussion.-->

Teniendo en cuenta el precio actual del gas y el hecho de que la gente va a tener que reclamar su $BAL ellos mismos, sostengo que es más razonable  conservar el $BAL como capital operativo para el equipo.

**A FAVOR:** Conservar los tokens $BAL y asignarlos al capital operacional.

**EN CONTRA:** Permitir a los stakers reclamar los tokens $BAL.
