# Así es como Yearn aumenta tu rendimiento

Casi todo con lo que la yVault interactúa está disponible para el público. ¿Como Yearn consigue mejores rendimientos de los que podrían conseguir por sí mismos?

## Sinergia con Curve Finance

Muchas de las estrategias de Yearn utilizan la liquidez del programa de minería de Curve Finance. [Curve Finance](https://curve.fi/) tiene un programa de distribución de tokens por 300 años a quienes proveen liquidez para su casa de cambio descentralizada con bajo deslizamiento (diferencia entre el precio esperado y el precio del intercambio ejecutado).

### Incremento de rentabilidad con veCRV 

CRV es distribuido continuamente a usuarios que hacen staking de ciertos tokens de liquidez en el [Indicador de Curve](https://resources.curve.fi/base-features/understanding-gauges). Esas recompensas pueden incrementarse cuando el usuario bloquea su CRV en el ["Locker"](https://dao.curve.fi/locker). Dicho "Locker" da a el usuario el token veCRV que a su vez le otorga derecho de voto en la gobernanza del proyecto y el derecho de obtener una parte de la tarifa que cobra el protocolo. 

Bloquear CRV permite a los usuarios incrementar las recompensas en CRV que reciben cuando proveen liquidez en fondos de liquidez seleccionados. La cantidad de del incremento viene determinada por que tanto CRV fue bloqueado y el porcentaje que representa del total del fondo de liquidez.

![](https://i.imgur.com/QaMMdr7.png)

Usando el yVault llamado "Backscratcher", Yearn bloquea una cantidad significativa de CRV de forma indefinida y distribuye el incremento de rentabilidad entre varias yVaults. 

###  yVault "Backscratcher"

La yVault "Backscratcher" capitaliza la liquidez de minado beneficiando a Yearn y a Curve.

Los usuarios depositan CRV en la yVault la cual es bloqueada para siempre. Obtienen en retorno tokens que representan una participación de la mencionada yVault "Backscratcher". El rendimiento obtenido por las tarifas compartidas por Curve, son distribuidas en la yVault y pueden ser reclamadas por los usuarios semanalmente.

Adicionalmente, el 10% de todo el CRV obtenido por Yearn Finance es depositado en la yVault "Backscratcher" y bloqueado para siempre. Debido a esto las personas que quieran hacer stake de CRV recibirán siempre una participación mayor en el rendimiento de la yVault "Backscratcher" que si hicieran directamente staking in Curve. Además podrán ganar emisiones de los tokens Pickle y Sushi por proveer liquidez.

![](https://i.imgur.com/UfCikwk.png)

Los usuarios nunca podrán retirar el CRV originalmente depositado, pero debido a los incentivos en los fondos de liquidez yveCRV y el valor acumulado del token por las distintas fuentes de ingresos, podrán intercambiarlos por otros activos.

Yearn obtiene control sobre los incrementos de rentabilidad de los CRV bloqueados y los utiliza a través de varias yVaults.

## Rendimiento compuesto automático

Generar rendimiento compuesto requiere de costes de transacción a ser pagados en la red de Ethereum, estos pueden ser costosos y llevarse parte del retorno.

Debido a que las yVaults unen muchas transacciones de otros muchos otros depositantes, consiguen un coste de transacciones menor y por lo tanto un rendimiento mayor al utilizar las yVaults. Actualmente el coste del gas de las transacciones lo cubre la red Keep3r, lo que significa que los usuarios se benefician del rendimiento compuesto sin coste.

## Apalancamiento

Yearn utiliza el banco de hierro (C.R.E.A.M. Finance) para acceder a crédito el cual es utilizado para mejorar los rendimientos de las yVaults).Solo carteras previamente autorizadas tienen esta funcionalidad habilitada, lo que significa que habitualmente los individuos no tienen la posibilidad de hacer esto por su cuenta.

Algunas estrategias implementan tambien [prestamos Flash](https://docs.yearn.finance/resources/defi-glossary#flash-loan), los cuales habitualmente requieren de experiencia en desarrollo informático para poderlas aprovechar ya que son un servicio habilitado desde el back end.

## Colaboraciones

La yVaults "Backscratcher" solo es posible debido a las sinergias y relaciones entre Yearn y protocolos como Curve, Sushiswap y Pickle finance. Nuestras relaciones a través de Defi permiten que las yVaults obtengan beneficios que en otro sitio no serían posibles.

Yearn colabora de forma activa en el desarrollo con protocolos como los mencionados para poder crear nuevas oportunidades para generar rendimiento de capital y hacer crecer Defi como la industria en la cual se ha convertido.


