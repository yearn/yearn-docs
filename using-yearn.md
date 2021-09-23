# ¿Cómo usar Yearn?

Gracias a la función llamada "Zap", es muy fácil depositar en cualquier vault con gran variedad de tokens.

Así es como funciona:

Primero, conecta tu cartera usando el botón de la esquina superior derecha. Hay múltiples carteras soportadas, pero la más utilizada es [Metamask](https://metamask.io/), cuya extensión de Chrome puedes descargar gratuitamente o a través de las tiendas de aplicaciones de Android y Apple. Asegurate de que la cartera está conectada a la red de Ethereum.

<p align="center">
  <img width="1266.75" height="345.75" src="https://i.imgur.com/H0Uc8e8.png">
</p>

## Si **ya tienes el token** para la vault donde quieres depositar:

1\. Selecciona la Vault en la que quieres depositar.

2\. Ingresa la cantidad de tokens que quieres depositar en la vault. Si estás depositando ETH, asegúrate de que dejas suficiente ETH en cartera para pagar el gas de futuras transacciones que probablemente tengas que realizar.

<p align="center">
  <img width="914.26" height="360.75" src="https://i.imgur.com/LGdRAMQ.png">
</p>

3\. Haz clic en "Aprobar" o "Depositar", dependiendo de si lo has aprobado anteriormente.

4\. La cartera te pedirá que confirmes la transacción. Esto tomará unos 3 minutos, pero puedes acelerarlo [pagando una cantidad mayor de gas a la red](https://blog.leverj.io/how-to-set-the-gas-limit-and-gas-price-in-metamask-1b33c38c32fd). Si la transacción queda atascada, [ver esta guía](https://metamask.zendesk.com/hc/en-us/articles/360015489251-How-to-Speed-Up-or-Cancel-a-Pending-Transaction) para acelerar o cancelar la transacción.

<p align="center">
  <img width="258.75" height=" 459.75" src="https://i.imgur.com/BkXBANS.png">
</p>

5\. Cuando la transacción sea exitosa, verás el balance del depósito en la interfaz de la vault, el cual aparecerá en la parte superior de la lista de las vaults.

<p align="center">
  <img width="928.5" height="93.75" src="https://i.imgur.com/JvNQ3l2.png">
</p>

Cuando estés listo para retirar:

1\. Selecciona la vault de la cual quieres retirar.

2\. Escribe la cantidad que quieres retirar o haz clic en "Max" para retirar todo lo depositado.

<p align="center">
  <img width="910.5" height="361.5" src="https://i.imgur.com/Y3NsCRb.png">
</p>

3\. Haz clic en "Retirar".

4\. La cartera te pedirá que confirmes la transacción. Ver el paso 4 anteriormente explicado para más detalles.

5\. Cuando la transacción sea exitosa, los tokens se mostrarán en tu cartera de nuevo.

## Si **no tienes el token requerido** para el vault en el que quieres depositar:

Esto es muy posible ya que muchas de las vaults de Yearn generan rentabilidad usando los tokens de proveedor de liquidez (LP) de [Curve Finance](http://curve.finance/) los cuales son adquiridos depositando en los fondos de liquidez de Curve.

Por ejemplo, si prefieres depositar en la vault de crvSTETH y no en la vault de ETH, y aceptas el riesgo adicional que viene con el fondo de liquidez de Curve y el derivado de utilizar un sintético de ETH (stETH)a cambio de una mayor rentabilidad, pero solo posees ETH en tu cartera, tu ETH tendrá que ser convertido al token crvSTETH antes de ser aceptado en la vault.

Por suerte, debido al "zap" de Yearn, todo esto puede realizarse en la misma transacción en el momento del depósito. Así es como funciona usando la vault crvSTETH como ejemplo : 

**NOTA:** Hacer "zap" para poder depositar en la vault requerirá más transacciones que depositar simplemente el token requerido. Esto significa que pagarás más gas y potencialmente perderás valor cuando el token se intercambie o deposite en el fondo de liquidez. Yearn limita el deslizamiento a 1% y la transferencia fallará si excede ese porcentaje, en ese caso deberá intercambiar o depositar los tokens manualmente. Ver nuestra sección de [zap](https://docs.yearn.finance/yearn-finance/yvaults/overview#zap-in-with-any-asset) para mas detalles. 

1\. Selecciona el vault crvSTETH.

2\. Haz clic en el desplegable en "aprobar" o "depositar" según el caso.

3\. Selecciona el token que quieres convertir en crvSETH. Sólo se mostrarán los tokens que están en tu cartera.

<p align="center">
  <img width="909" height="363" src="https://i.imgur.com/6K1luO7.png">
</p>

4\. Escribe la cantidad de tokens que quisieras depositar y haz clic en "aprobar" o "depositar" dependiendo de si lo has aprobado antes o no.

5\. Confirma la transacción a través de tu cartera. Ver paso 4 de la sección de arriba para más detalles.

6\. Cuando la transacción sea exitosa, verás el balance depositado en la interfaz de la vault el cual aparece de primero en la lista de la vault.

Cuando estés listo para retirar:

1\. Selecciona el vault crvSTETH.

2\. Haz click en el desplegable en el botón de "Retirar"

<p align="center">
  <img width="915.75" height="600.75" src="https://i.imgur.com/2UyXKN0.png">
</p>

3\. Selecciona que activo quieres recibir al retirar. Tus opciones serán crvSTETH, ETH, BTC, DAI, USDC or USDT.

4\. Escribe la cantidad que quieres retirar o haz clic en "Max" para retirar el balance completo.

5\. Confirma la aprobación de ser necesario y luego aprueba la transacción de retiro.

6\. Cuando la transacción sea exitosa el token se mostrará en la cartera de nuevo.

## Herramientas para trackear tus fondos

Si quieres ver como cambia tu balance de USD mientras tus activos están en la vault, conecta con [zapper.fi](https://zapper.fi) o otro producto de seguimiento de cartera. Esta es también la forma más fácil de saber cuánta rentabilidad ha generado la vault para ti.

El balance no aumentará continuamente. La rentabilidad será distribuida en función del porcentaje de participación en la vault cuando se haga el llamado de la función de cosecha. Este llamado es fluctuante.

Recursos de la comunidad para monitorear tus retornos:

- [Zapper](https://zapper.fi/)
- [Zerion](https://app.zerion.io/)
- [Yearn Vault ROI Calculator](https://yearn-roi.xyz/#/)
- [yVault ROI](https://yvault-roi.netlify.app/)
- [https://trackavault.com/](https://trackavault.com/)
