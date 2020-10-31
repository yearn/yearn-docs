# Cómo crear una YIP

## Resumen

Las propuestas de mejora de Yearn \(`YIPs`\) describen los estándares para la plataforma de Yearn, incluidas las especificaciones del protocolo central, las API del cliente y los estándares de los smart contracts. Esta es la especificación `canónica` definitiva de referencia para la lógica central.

## Aportar

1. Revisa la [YIP-0](https://github.com/iearn-finance/YIPS/blob/master/YIPS/yip-0.md).
2. Crea un fork del repositorio haciendo click en "Fork" arriba a la derecha.
3. Añade tu YIP a tu versión del repositorio. Hay una plantilla de YIP disponible [aquí](https://github.com/iearn-finance/YIPS/blob/master/yip-X.md).
4. Envía una PR \(Pull Request\) al [repositorio de YIPs](https://github.com/iearn-finance/YIPS/) de Yearn.

Tu primer PR debería ser un primer borrador de la YIP final. Este debe cumplir todos los criterios de formato impuestos por el compilador \(en gran parte, metadatos correctos en el header\). Un editor revisará manualmente la primera PR para cada nueva YIP y le asignará un número antes de incluirla en el repositorio. Asegúrate de incluir en el header `discussions-to`  la URL del nuevo hilo creado en el [foro oficial](https://gov.yearn.finance/) donde la gente podrá discutir a cerca de la YIP y los cambios propuestos.

> Nota: Es importante que haya apoyo de la comunidad hacia la `YIP` propuesta. Depende del autor \(es\) llevar su propuesta a lo largo del proceso.

Si tu YIP requiere imágenes, los archivos de imagen deben incluirse en un subdirectorio de la carpeta `assets` para dicha YIP de la siguiente manera: `assets/yip-X` \(para una YIP **X**\). Cuando se vincule a una imagen dentro de la YIP, usa enlaces relativos como `../assets/yip-X/image.png`.

Cuando creas que tu YIP está madura y lista para avanzar más allá de la fase WIP \(Work In Progress\), debes solicitar que tu issue se agregue a la próxima llamada de gobernanza donde se podrá discutir su inclusión en una futura actualización de la plataforma. Si la comunidad acepta incluirlo, los editores de las YIPs actualizarán el estado de tu YIP a 'Aprobada'.

## Estados de una YIP

* **WIP \(Work In Progress\)** - una YIP que aún está siendo desarrollada.
* **Propuesta** - una YIP que está lista para ser revisada en una llamada de gobernanza.
* **Aprobada** - una YIP que ha sido aceptada por la comunidad de Yearn para ser implementada.
* **Implementada** - una YIP ha sido implementada y desplegada en mainnet.
* **Rechazada** - una YIP que ha sido rechazada.

### Ejemplo de YIP

```diff
-Status: Proposed
+Status: Approved
YIP: integer,
Created: 2020-09-01
-Last-Modified: 2020-09-03
+Last-Modified: 2020-09-08
```

## Validación

Las YIPs DEBEN pasar algunos tests de validación. El repositorio de las YIPs se asegura de esto corriendo algunos tests usando [html-proofer](https://rubygems.org/gems/html-proofer) y [yip\_validator](https://rubygems.org/gems/yip_validator).

Es posible correr el validador de YIPs localmente de la siguiente forma:

```ruby
gem install yip_validator
yip_validator <INPUT_FILES>
```

## Derechos de autor

Derechos de autor y derechos relacionados con renuncia a través de [CC0](https://creativecommons.org/publicdomain/zero/1.0/).

