# Usando a Yearn       

Graças a um recurso chamado 'zap', depositar em qualquer vault com quase qualquer token é extremamente simples.

Como funciona:

Primeiro **Conecte sua carteira** utilizando o botão no canto superior direito. Há suporte para múltiplas carteiras, mas a maioria dos usuários utilizam o [MetaMask](https://metamask.io/), que está disponível pra download de graça como uma extensão do Chrome ou pelas app stores da Apple e Android. Verifique se sua carteira está conectada a rede do Ethereum.

<p align="center">
  <img width="1266.75" height="345.75" src="https://i.imgur.com/H0Uc8e8.png">
</p>

## Se você **já possui o token necessário** para a vault que você queira depositar:

1. Selecione a vault que você queira depositar.
2. Digite a quantidade de tokens que você quer depositar na vault. Se você estiver depositando ETH, tenha certeza de que você tenha ETH necessário para pagar futuras transações que você possa fazer.

<p align="center">
  <img width="914.26" height="360.75" src="https://i.imgur.com/LGdRAMQ.png">
</p>

3. Clique em 'Approve' ou 'Deposit', dependendo se você já aprovou anteriormente.
4. Sua carteira vai pedir por uma confirmação da transação. Isso irá demorar em torno de 3 minutos, mas você pode acelerar o processo [pagando por uma taxa de gas da rede mais cara](https://blog.leverj.io/how-to-set-the-gas-limit-and-gas-price-in-metamask-1b33c38c32fd). Se sua transação ficar presa, leia [este guia](https://metamask.zendesk.com/hc/en-us/articles/360015489251-How-to-Speed-Up-or-Cancel-a-Pending-Transaction) sobre acelerar ou cancelar sua transação.

<p align="center">
  <img width="258.75" height=" 459.75" src="https://i.imgur.com/BkXBANS.png">
</p>

6. Quando a sua transação é completada, você vai ver seu balanço depositado na interface da vault, que deve aparecer no topo da lista de vaults.

<p align="center">
  <img width="928.5" height="93.75" src="https://i.imgur.com/JvNQ3l2.png">
</p>

Quando quiser fazer a retirada:

1. Selecione a vault que você deseja fazer a retirada.
2. Digite a quantia que você queira retirar, ou clique em 'Max' para retirar todo o balanço.

<p align="center">
  <img width="910.5" height="361.5" src="https://i.imgur.com/Y3NsCRb.png">
</p>

3. Clique em 'Withdraw'
4. Sua carteira vai pedir que você confirme a transação. Leia o passo 4 acima para mais detalhes.
5. Quando sua transação é completada com sucesso, os tokens vão aparecer na sua carteira novamente.

## Se você **não tiver o token necessário** para a vault que você gostaria de depositar:

Isso é uma ocorrência comum, já que muitas das vaults da Yearn geram rendimento usando o tokens de provisão de liquidez da [Curve Finance](http://curve.finance/), que são adquiridos por meio de depósitos em uma pool da Curve.

Por exemplo, se você gostaria de depositar na vault crvSTETH em vez da vault ETH, e aceitar o risco adicional que vem com uma pool da curva e um derivativo de ETH (stETH) em retorno de um rendimento maior, mas possui apenas ETH em sua carteira, o seu ETH vai precisar ser convertido em tokens crvSTETH antes de ser aceito na vault.

Felizmente, graças ao recurso 'zap', isso pode ser feito em uma única transação em forma de depósito. O exemplo abaixo explica como o mecanismo funciona com a vault de crvSTETH:

**OBSERVAÇÃO:** Zapear um token em uma vault requer mais transações do que depositar no seu token nativo. Isso significa que você pagará mais gas e potencialmente perderá uma parcela desse valor via derrapagem quando o token é trocado ou depositado na pool. A Yearn limita a derrapagem a um máximo de 1%, e a transação irá falhar caso ultrapasse o limite, onde no caso, você terá que trocar ou depositar os tokens manualmente. Veja a seção [zap](https://docs.yearn.finance/yearn-finance/yvaults/overview#zap-in-with-any-asset) para mais informações.

1. Selecione a vault crvSTETH
2. Clique no campo antes do botão 'Approve' ou 'Deposit'
3. Selecione qual token você gostaria de converter para crvSTETH. Ele irá mostrar apenas os tokens que estão em sua carteira.

<p align="center">
  <img width="909" height="363" src="https://i.imgur.com/6K1luO7.png">
</p>

4. Digite a quantidade de tokens que você quer depositar e clique em 'Approve' ou 'Deposit', dependendo se você já aprovou anteriormente.
5. Confirme a transação pela sua carteira. Veja o passo 4 no setor acima para mais detalhes.
6. Quando a sua transação é completada, você vai ver seu balanço depositado na interface da vault, que deve aparecer no topo da lista de vaults.

Quando quiser fazer a retirada:

1. Selecione a vault crvSTETH.
2. Clique no campo ao lado do botão 'Withdraw'

<p align="center">
  <img width="915.75" height="600.75" src="https://i.imgur.com/2UyXKN0.png">
</p>

3. Selecione o ativo que você gostaria de retirar. Suas opções serão crvSTETH, ETH, BTC, DAI, USDC or USDT
3. Digite a quantia que você queira retirar, ou clique em 'Max' para retirar todo o balanço.
4. Confirme a aprovação se for necessário, e aprove a transação de retirada.
5. Quando sua transação é completada com sucesso, os tokens vão aparecer na sua carteira novamente.

## Ferramentas para acompanhar os seus fundos

Se você quiser acompanhar o seu balanço em USD enquanto seus ativos estão em uma vault, conecte sua carteira no [zapper.fi](https://zapper.fi) ou um produto de acompanhamento de portfolio similar. Essa também é a forma mais fácil de dizer quanto lucro a vault te ofereceu.

O seu balanço NÃO IRÁ aumentar de forma contínua. Lucros são distribuídos para sua quota da vault quando a função harvest() é chamada, que acontece em um ritmo flutuante.

Recursos da comunidade para monitorar seus retornos:

- [Zapper](https://zapper.fi/)
- [Zerion](https://app.zerion.io/)
- [Calculadora de ROI para Yearn Vault](https://yearn-roi.xyz/#/)
- [yVault ROI](https://yvault-roi.netlify.app/)
- [https://trackavault.com/](https://trackavault.com/)
