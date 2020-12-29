---
YIP: 44
Título: Mejorar las categorías de las YIPs
Estado: Implementada
Autor: sam bacha <sam@freighttrust.com>
Discusiones: https://gov.yearn.finance/t/yip-44-improve-yip-categories/3608

Fecha de creación: 2020-08-31
---


Fecha de creación: 2020-08-24
---


## Explicación corta
<!--"If you can't explain it simply, you don't understand it well enough." Simply describe the outcome the proposed changes intends to achieve. This should be non-technical and accessible to a casual community member.-->

Añadir nuevos `estado`(s) a las `YIPs` para que el(los) autor(es) pueda(n) gestionar mejor las `YIPs` en el contexto de la colaboración comunitaria y para que la gobernanza cuente con procedimientos adecuados para fomentar la cooperación comunitaria.

## Resumen
<!--A short (~200 word) description of the proposed change, the abstract should clearly describe the proposed change. This is what *will* be done if the YIP is implemented, not *why* it should be done or *how* it will be done. If the YIP proposes deploying a new contract, write, "we propose to deploy a new contract that will do x".-->

Esta propuesta *solo* agregará al estado actual de las `YIPs propuestas` en el sentido de que solo cambia los _potenciales_`estados` disponibles para una `YIP`. No supone ningún cambio en el `protocolo`: solo afecta a la documentación y los procedimientos de gobernanza (únicamente aquellos off-chain).

Propongo los siguientes cambios para reflejar un nuevo estado de las posibles 'YIPs':

1. Modificación de la plantilla de la YIP
2. Modificación del validador de Gemfile de la YIP
3. Modificación del archivo README de la YIP

## Motivación
<!--This is the problem statement. This is the *why* of the YIP. It should clearly explain *why* the current state of the protocol is inadequate.  It is critical that you explain *why* the change is needed, if the YIP proposes changing how something is calculated, you must address *why* the current calculation is inaccurate or wrong. This is not the place to describe how the YIP will address the issue!-->

 > El estado actual de los procedimientos para las `YIPS` es inadecuado, ya que limita innecesariamente los posibles resultados de una `YIP` propuesta, mientras que no brinda ni al autor(es) ni al consejo de gobernanza flexibilidad para poder tratar con las `YIPs` propuestas por la comunidad

Este es un cambio de *documentación* y *procedimiento*. De hecho, no hay una descripción explícita para proponer tales cambios en la gobernanza *(que pueda encontrar).*

Este cambio es necesario ya que explica mejor la *intención* del formato de la YIP a el(los) autor(es). También proporciona funcionalidad adicional de gobernanza en sus procedimientos a fin de no 'alienar' potencialmente a el(los) autor(es) al rechazar una YIP cuando podría haber sido retirada. Esto asegura que también el(los) autor(es) participa(n) activamente en el proceso de su propuesta presentada y en la comunidad en general (en la medida en que estén al tanto de otras YIPs con las que pueden competir).

## Especificación

*Cambios en 'NEGRITA'*

Propuesta - una YIP que está lista para ser revisada en una llamada de gobernanza
Aprobada - una YIP que ha sido aceptada para su implementación por la comunidad de yEarn.
Implementada - una YIP que ya está en mainnet.
Rechazada - una YIP que ha sido rechazada.
**Retirada - una YIP que ha sido retirada por su(s) autor(es).**
**Diferida - una YIP que la gobernanza ha decidido poner en pausa hasta que otra YIP u otro cambio con la que debería ir en conjunto sea propuesto.**
**Moribunda - una YIP que hace tiempo fue implentada. Este ha quedado obsoleta 'Y' no requiere ninguna sustitución explícita.** 

El estado "Retirada" es similar: significa que el autor de la YIP ha decidido que la YIP es en realidad una "mala" idea, o ha aceptado que otra propuesta contra la que compite es una mejor alternativa.

### Esquema de trabajo propuesto
```
Propuesta -> Aprobada -> Implementada
  ^                     |
  +----> Rechazada      +----> Moribunda 
  |
  +----> Retirada
  v
Diferida
```

#### Nuevos estados para las YIPs

> Aquellos que van a ser añadidos son:

-Retirada
-Moribunda
-Diferida

### Visión de conjunto
<!--This is a high level overview of *how* the YIP will solve the problem. The overview should clearly describe how the new feature will be implemented.-->

#### Nuevos estados para las YIPs

- Retirada
Esto significa que el autor de la YIP ha decidido que la YIP es en realidad una "mala" idea, o ha aceptado que otra propuesta contra la que compite es una mejor alternativa.
- Moribunda
Aquella YIP que ha quedado obsoleta y no quiere un reemplazo explícito debería ser marcada como "Moribunda"
- Diferida
En caso de que la gobernanza le otorge este estado a una YIP, lo que significa es que les gustaría tener más información, o que les gustaría ver si los autores pueden trabajar con otra YIP propuesta y combinarla en una sola YIP, etc.

### Razón fundamental

El razonamiento detrás de esta propuesta es que no está claro qué pasará con un YIP si los hechos materiales cambian entre su propuesta formal inicial y cuando llega la hora de ser votada por la gobernanza. Se pueden introducir cambios entre su propuesta inicial y cuando se vota por ella, o el autor puede querer retirar la propuesta antes de que llegue a ser votada. Esto también libera al consejo de gobernanza en el sentido de que ya no estaría obligado a rechazar cada YIP que puede que ya no sea relevante, sino que comparte la responsabilidad con el(los) autor(es) de la YIP.
 

### Especificación técnica
<!--
NOTE: NO PROTOCOL CHANGES ARE PROPOSED 
THE ONLY TECHNICAL CHANGES ARE IN THE RUBY VALIDATION PROCESS FOR YIPS
-->
La implementación técnica requiere:
* cambios en el validador Gemfile
* cambios en el archivo plantilla `.md`

#### Cambios en el archivo plantilla `.md` 

Más abajo hay un archivo de muestra `.yaml` que ilustra el _nuevo_ header que debería ser usado en la plantilla `yip-template.md`

```yaml
---
YIP: <número de la YIP>
Título: <título de la YIP>
Autor: < Nombre, Apellido, @githubUsrName, contacto@dirección.com >
Tipo: <Informativo | Seguimiento de Estándares>
Estado: <WIP | Propuesta | Aprobada | Diferida | Retirada | Rechazada |
           Implementada | Reemplazada | Moribunda>
    Versión: <mayor>[.<menor>]
    Fecha de creación: <Creada en: , usando el formato ISO 8601 (yyyy-mm-dd)>
    Requiere (*opcional): <Número(s) de la(s) YIP(s)>
    Implementación (*opcional): <Añadir si la YIP ha sido aceptada>

Discusiones: <Crea un hilo en https://gov.yearn.finance/ y pon el link aquí>

* Requiere: <números de las YIPs>
* Reemplaza: <Números de las YIPs>
* Reemplaza por: <Número de la YIP>
---
```

#### Validador YIP (Ruby Gem)

> versión actual: `1.0.2`, debe ser actualizada a `1.1.0`
Cambios disponibles en [github.com/iearn-finance/yip_validator/blob/master/lib/yip_validator/validator.rb#L25](https://github.com/iearn-finance/yip_validator/blob/master/lib/yip_validator/validator.rb#L25)

```ruby
    validates_inclusion_of :status, in: ['WIP', 'Proposed', 'Approved', 'Implemented', 'Rejected']
```
```ruby
    validates_inclusion_of :status, in: ['WIP', 'Proposed', 'Approved', 'Implemented', 'Rejected', 'Withdrawn', 'Deferred', 'Moribund']
```

Mira las archivos cambiados aquí [https://github.com/sambacha/yip_validator/tree/YIP-Proposed](https://github.com/sambacha/yip_validator/tree/YIP-Proposed)

### Casos de prueba

Mira los registros `travis-ci` para `Rub Gem` actualizados aquí [https://travis-ci.com/github/sambacha/yip_validator/builds/181226022](https://travis-ci.com/github/sambacha/yip_validator/builds/181226022)

```bash
total:2, valid:2, invalid:0, errors:0
	statuses: [["Withdrawn", 1], ["Implemented", 1]]
  raises exception if it includes invalid yips
spec/fixtures/invalid/yip-7.md is NOT valid:	 {:status=>["is not included in the list"]}

```

## Derechos de autor
Derechos de autor y derechos relacionados con renuncia a través de [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
