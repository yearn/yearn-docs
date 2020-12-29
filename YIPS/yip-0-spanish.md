---
YIP: 0
Título: Propósito y guías para una YIP
Estatus: Implementada 
Autor: La comunidad de yEarn
Discuciones: https://gov.yearn.finance/
Fecha de creación: 2020-07-22
Fecha de actualización: 2020-09-03
---

## ¿Qué es una YIP?

Una YIP es una propuesta de mejora de yEarn (yEarn Improvement Proposal en inglés) que ha sido adaptada de las SIP utilizadas por Synthetix. La finalidad de este proceso es asegurar que los cambios en yEarn son transparentes y democráticos. Una YIP es un documento que provee información a la comunidad de yEarn a cerca de un cambio propuesto que afecta al sistema. El autor de esta es el responsable de buscar el concenso y la aprobación de la comunidad, además de documentar los pros y contras presentados por los distintos miembros de la comunidad acerca del cambio propuesto.

## Fundamento de las YIPs

Nosotros pretendemos que las YIPs sean el principal mecanismo mediante el cual se proponen mejoras, se analiza la posición de la comunidad frente a un problema y se documentan posibles cambios en yEarn. Como estas son almacenadas en archivos de texto en un repositorio, esta queda guardada para su revisión en un futuro.

Se recomienda encarecidamente que cada YIP contenga una propuesta clave o una idea nueva. Cuanto más concisa sea la YIP, más probabilidades tendrá de tener éxito.

Una YIP debe de cumplir ciertos criterios para ser aceptada. Debe de ser clara y debe tener una descripción completa y detallada de la propuesta que se quiere hacer. La propuesta debe de representar un cambio significativo en un aspecto del sistema.

## Esquema de trabajo de una YIP

Las partes involucradas en el proceso son el *autor*, los [*editores*](#yip-editors) y la comunidad de yEarn.

:warning: Antes de empezar, evalúa detenidamente tu idea. Pregúntale a la comunidad de yEarn primero si la idea es original para evitar perder el tiempo en una propuesta que será rechazada en base a una investigación previa (buscar en Internet no siempre va a funcionar). Además, también es de cierta utilidad asegurarte de que la idea es aplicable a la comunidad entera y no solo al autor de ella. Sólo por el hecho de que una idea le parezca buena a su autor no significa que vaya a tener el efecto previsto por él. Los foros públicos en los que puedes captar el interés de los demás hacia tu YIP son [el Discord de yEarn no oficial] o [el canal de Telegram de yEarn no oficial].

Tu papel como autor es escribir la YIP usando el estilo y el formato descrito a continuación, guiar las discusiones en los foros apropiados y construir concenso alrededor de la idea. Este es el camino que sigue una YIP exitosa: 

```
Propuesta -> Aprobada -> Implementada
  ^                     |
  +----> Rechazada      +----> Moribunda 
  |
  +----> Retirada
  v
Diferida
```
Cada cambio de estado es pedido por el autor de la YIP y revisado por los editores. Haz un pull request para actualizar el estado de la YIP. Por favor, incluye también una dirección donde la gente debería ir para continuar la discusión a cerca de tu YIP. Los editores procesarán el cambio de estado siguiendo las siguientes directrices:

* **Work in progress (WIP)** -- Cuando un autor ha preguntado la comunidad de yEarn si su idea tiene alguna posibilidad de salir adelante, él redactará un borrador de YIP como un [pull request]. Considera incluir también una implementación si servirá de ayuda a la hora de que otras personas estudien la YIP.

* **Propuesta** Si está de acuerdo, un editor asignará a la YIP un número y fusionará la pull request. El editor no denegará ninguna YIP sin justificación. Las YIPs propuestas se discutirán en los canales apropiados. Si hay un nivel razonable de consenso en torno al cambio en la convocatoria de gobernanza, el cambio pasará a estar aprobado. Si el cambio es controvertido, se puede realizar una votación entre los titulares de tokens para resolver el problema o se puede retrasar la aprobación hasta que se alcance el consenso.

* **Aprobada** -- Esta YIP ha sido acogida positivamente por la comunidad y ahora se prioriza su desarrollo.
* **Implementada** -- Esta YIP ha sido implementada y desplegada en mainnet.
* **Rechazada** -- Esta YIP ha fracasado en su intento de conseguir el conceso de la comunidad.
* **Retirada** --  Esta YIP ha sido retirada por su autor o autores.
* **Diferida** -- Esta YIP está pendiente de otra YIP u otro cambio con el que se debería incluir en conjunto.
* **Moribunda** -- Esta YIP ha sido implementada en el pasado pero ahora ha quedado obsoleta y no requiere un reemplazo explícito.

## ¿Qué forma una YIP exitosa?

Cada YIP debe de estar compuesta por las siguientes partes:

- Preámbulo - RFC 822 style headers que contienen metadatos a cerca de la YIP, incluído el número de la YIP, un pequeño título descriptivo (limitado a 44 caracteres) y los datos del autor.
- Explicación corta - “Si no puedes explicarlo con palabras sencillas, entonces es que no lo entiendes lo suficiente.” Proporcione una explicación simplificada y accesible para la gente del YIP.
- Resumen - Una descripción corta (~200 palabras) del problema técnico que se está abordando.
- Motivación (*opcional) - La motivación es una parte crítica para las YIPs que desean cambiar yEarn. Aquí se debe explicar claramente por qué la especificación existente es inadecuada para resolver el problema que la YIP resuelve. Las YIPs presentadas sin suficiente motivación pueden ser rechazadas por completo.
- Especificación - La especificación técnica debe describir la sintaxis y semántica de cualquier característica nueva.
- Razonamiento fundamental - El fundamento da cuerpo a la especificación al describir qué motivó el diseño y por qué se tomaron decisiones de diseño particulares. Debe describir los diseños alternativos que se consideraron y el trabajo relacionado. El razonamiento también debe proporcionar evidencia de consenso dentro de la comunidad y en él se debe discutir las objeciones o preocupaciones importantes que surjan durante la discusión.
- Casos de prueba - se pueden agregar casos de prueba durante la fase de implementación, pero son necesarios antes de la implementación.
- Exención de derechos de autor: todos los YIP deben ser de dominio público. Consulte la parte inferior de esta YIP para ver un ejemplo de exención de derechos de autor.

## Formatos de YIP y plantillas

Las YIPs deben ser escritas usando el formato [markdown].
Las imágenes deben incluirse en el subdirectorio de la carpeta `assets` para cada YIP de la siguiente forma: `assets/yip-X` (para la YIP **X**). Para vincular una imagen en la YIP, usa vínculos relativos como `../assets/yip-X/image.png`.

## Preámbulo del header YIP

Cada YIP debe empezar con un estilo de preámbulo del header [RFC 822](https://www.ietf.org/rfc/rfc822.txt), precedido y seguido por tres guiones (`---`). Este header también se conoce como ["front matter" by Jekyll](https://jekyllrb.com/docs/front-matter/). Los headers deben aparecer en el siguiente orden. Headers marcados con "*" son opcionales y se describen más abajo. Todos los demás headers son necesarios.

` yip:` < YIP number > (Esto es determinado por el editor de la YIP)

` Título:` < YIP title >

` Autor:` < Una lista con el nombre(s) del autor(es) o su(s) nombre(s) de usuario(s) o nombre(s) y email(s). Los detalles están más abajo. >

` * Discusiones en:` < Una url que dirija al hilo oficial en gov.yearn.finance \>

` Estado:` < WIP | PROPUESTA | APROBADA | IMPLEMENTADA >

` Creada:` < Fecha de creación >

` * Actualizada:` < Lista de fechas separadas por comas >

` * Requiere:` < Numero(s) de YIP >

` * Resolución:` < Una url que dirija a la resolución de esta YIP \>

Headers que permiten listas deben separar los elementos con comas.
Headers que requieran fechas siempre se introducirán en el formato ISO 8601 (yyyy-mm-dd).

#### Header `autor` 

El header del `autor` opcionalmente enumera los nombres, direcciones de correo electrónico o nombres de usuario de los autores / propietarios de la YIP. Aquellos que prefieren el anonimato pueden usar solo un nombre de usuario, o un nombre y un nombre de usuario. El formato del valor del header del autor debe ser:


> Random J. User &lt;correo@dominio.ain&gt;

o

> Random J. User (@nombredeusuario)

si el correo electrónico o el nombre de usuario de GitHub están incluídos, y

> Random J. User

si la dirección de correo no se especifica.

#### Header `discusiones en` 

Mientras que una YIP esté en estado WIP o propuesta, un header `discusiones en` indicará la dirección de URL en [gov.yearn.finance](https://gov.yearn.finance/) donde la discusión sobre la YIP está teniendo lugar.

#### Header `creada`

El header `creada` guarda la fecha en la que se le asignó un número a la YIP. Ambos headers deben usar el formato yyyy-mm-dd, por ejemplo 2001-08-14.


#### Header `actualizada` 

El header `actualizada` guarda la(s) fecha(s) cuando la YIP fue actualizada con cambios "sustanciales". Este header es válido únicamente para YIPs con estado de borrador o activa.

#### Header `requiere`

Las YIPs pueden tener un header `requiere`, indicando el número de las YIPs de la que esta depende.

## Archivos auxiliares 

Las YIPs puede incluir archivos auxiliares tales como diagramas. Dichos archivos deben ser llamados YIP-XXXX-Y.ext, donde “XXXX” es el número de la YIP, “Y” es un número de serie (empieza en 1) y “ext” es la extensión del archivo (i.e. “png”).

## Editores  de las YIPs

Actualmente, los editores son:

` * Artem K (@banteg)`

` * Cooper Turley (@Cooopahtroopa)`

` * Daryl Lau (@Daryllautk)`

` * Klim K (@milkyklim)`

` * Sunil Srivatsa (@alphastorm)`

## Responsabilidades de los editores de las YIPs

Cada vez que se propone una nueva YIP, un editor hace lo siguiente:

- Lee la YIP para comprobar que está lista, es decir, es sólida y está completa. Las ideas tienen que tener sentido tecnicamente hablando, incluso si no parece que vaya a llegar al estado final.
- Comprueba que el título describa adecuadamente el contenido de la YIP.
- Comprueba el lenguaje utilizado en la YIP (ortografía, gramática, estructura sintáctica, etc.), el markup (Github flavored Markdown) y el estilo del código.

Si la YIP no estuviese lista, el editor la envía de vuelta al autor para su revisión, incluyendo instrucciones específicas.

En cuanto la YIP está lista para el repositorio, el editor:


- Asigna un número a la YIP (generalmente el número del pull request o, si así lo quiere el autor, el número del issue si ha habido una discusión en la sección de issues de este repositorio a cerca de esta YIP).

- Fusiona el correspondiente pull request.

- Comunica al autor de la YIP cuál es el siguiente paso a seguir.

Los editores monitorizan los cambios hechos a la YIP, corrijiendo errores en la estructura, gramática u ortografía de la YIP. 

Los editores no juzgan el contenido de las YIPs, únicamente prestan un servicio administrativo y editorial.

## Historia

El documento de las YIPs, en su mayoría, ha sido copiado y modificado inspirándose en la forma de las SIPs de Synthetix. Cualquier comentario a cerca del documento de las YIPs debe ser dirijido a los editores.

### Bibliografía

[el Discord de yEarn no oficial]: http://discord.yearn.finance
[el canal de Telegram de yEarn no oficial]: https://t.me/yearnfinance
[pull request]: https://github.com/iearn-finance/YIPS/pulls
[markdown]: https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet

## Derechos de autor

Derechos de autor y derechos relacionados con renuncia a través de [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
