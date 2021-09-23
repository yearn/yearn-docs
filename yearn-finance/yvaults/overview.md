# Visión general

## ¿Qué son las yVaults?

Las [yVaults](https://yearn.finance/vaults) son como cuentas de ahorros para cripto-activos. Aceptan depósitos los cuales están expuestos a estrategias que buscan la mayor rentabilidad disponible en DeFI.

![](https://i.imgur.com/yXnJqsn.png)

## Deposita cualquier activo

Gracias a [Zapper](https://zapper.fi/), es muy fácil depositar en las yVaults siempre y cuando tengas un token que puedas intercambiar (hacer Zap) en Uniswap con menos de 1% de deslizamiento. La vault acepta el token, lo convierte en el token requerido por la misma y lo deposita, todo en la misma transacción. 

Cuando retiras, puedes hacer Zap de vuelta a uno de los siguientes tokens: 
- ETH, WETH, DAI, USDT, USDC, WBTC

## Structura de comision de la yVault

|Versión de yVault|Comisión de retiro|Comisión de desempeño|Comisión de gestión|
|--------------|:-----------:|:-------------:|:------------:|
|v1|0.5%|5%|-|
|v2|-|20%|2%|

**Comisión de retiro**: Comisión única cobrada de tu balance en el momento del retiro. Esto fue eliminado de todas las vaults y solo existió en la iteración V1.

**Comisión de desempeño**: Deducida del rendimiento obtenido cada vez que la vault obtiene el rendimiento (harvests) de la estrategia.

**Comisión de gestión**: Tarifa fija cobrada de los depósitos de la vault en el transcurso de 1 año. Se obtiene creando nuevas acciones de la vault lo que hace que se diluyan los participantes de la misma. Esto se realiza al momento de cosechar los rendimientos de la misma (harvest) y se calcula con base en el tiempo desde la cosecha anterior.

Por ejemplo, si una vault toma aproximadamente .0055% de los depósitos diarios de media (2 (percent)/365 (days)): 
- Diluirá los tokens de la vault entre 5 por .0055% después de 5 días sin cosecha.
- Diluirá los tokens de la vault entre 7 por .0055% después de 7 días sin cosecha.
- Las vaults solo serán cosechadas si es rentable después de las comisiones para que el usuario no retire menos de lo depositado.

En la interfaz de [yearn.finance](https://yearn.finance/), la rentabilidad se muestra como APY (porcentaje de rentabilidad anual) neto. Esto quiere decir que tanto las comisiones como los retornos compuestos son tomados en consideración en los ratios presentados. Como las cosechas no ocurren en un momento establecido, la rentabilidad es estimada basada en data histórica. Para mas información, ver [Cómo entender el ROI de las yVault](https://docs.yearn.finance/resources/guides/how-to-understand-yvault-roi)

## Mejoras de las yVault v2

- **Hasta 20 estrategias por vault:** Esto aumenta la flexibilidad de manejo de capital de forma eficiente durante los diferentes escenarios de mercado. Cada estrategia tiene un máximo de capital. Esto es útil para evitar la sobre localización de fondos a una estrategia que no pueda aumentar más el APY. 
- **Estrategas y guardianes son los nuevos controllers:** El concepto de controller no está disponible en vaults v2 y han sido reemplazados por Guardian y el creador de la estrategia (Estratega). Estos dos actores pueden supervisar el desempeño de la estrategia y tienen el poder de tomar acciones para mejorar la gestión del capital o actuar en una situación crítica.
- **Mantenimiento de vault automatizado \(red de Keep3r\):** Las funciones de `cosechar()` y `ganar()` son automatizadas a través de bots de la red de Keep3r. Estas 2 funciones son utilizadas para comprar nuevos colaterales subyacentes vendiendo los tokens ganados y moviendo las ganancias a las vaults y a su vez a las distintas estrategias. La red de Keep3r se encarga del difícil trabajo de ejecutar estas funciones y cubre el coste del gas a cambio de tokens de Keep3r. Este enfoque elimina a los humanos del proceso de mantenimiento de la vault.
- **Seguridad y lista de invitados**Yearn ha creado un proceso de desarrollo único para nuevas vaults. Todas las nuevas Vaults son lanzadas como vaults de prueba \(tyvToken\) para empezar. Estas vaults de prueba y sus estrategias tienen un techo. Además el seguridad tiene una lista de carteras de permitidas (lista de invitados) con las que puede interactuar, depositando y retirando fondos de las mismas.Este enfoque previene a usuarios desinformados de potenciales pérdidas de fondos en un producto que no está listo para producción.
