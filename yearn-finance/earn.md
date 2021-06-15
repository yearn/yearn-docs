# Earn

Earn é um agregador de empréstimos que tem como objetivo maximizar o rendimento para as seguintes moedas - DAI, USDC, USDT, TUSD, sUSD, ou wBTC. Isso é feito realocando essas moedas entre diferentes protocolos de empréstimos \([AAVE](https://aave.com), [dYdX](https://dydx.exchange/), e [Compound](https://compound.finance)\) operando na blockchain do Ethereum.

Como exemplo, um usuário pode depositar DAI na pool yDAI da Earn. A Yearn vai, por meio de contratos inteligentes, depositar DAI em um dos três protocolos \(AAVE, dYdX, Compound\). A Yearn retira de um protocolo e deposita em outro automaticamente de acordo com as mudanças nas taxas de juros entre os protocolos. Como resultado, os usuários sempre vão receber juros optimizados em seu depósito em DAI.

![](https://i.imgur.com/jLlg0WU.png)

A Earn é o componente chave da yPool em Curve.Finance, que representa um cesto de quatro yTokens: yDai, yUSDC, yUSDT, e yTUSD. Os quatro yTokens subjacentes são constantemente optimizados para render a quantia máxima de juros disponível no mercado \(descrito acima\), enquanto também serve como uma pool de liquidez para esses tokens. Usuários podem interagir com essa pool para fazerem trocas entre qualquer um dos quatro tokens com baixa derrapagem. Portanto, provedores de liquidez da yPool recebem juros optimizados em seus depósitos de stablecoins e taxas dos usuários fazendo trocas na pool.

Desde Setembro de 2020, o retorno anualizado YTD dos provedores de liquidez da yPool é estimado em torno de 9.11%. Como yDAI+yUSD+yUSDT+yTUSD é um token de acúmulo de juros continuo, seu preço está acima de  \$1 e sobe constantemente.

![](https://i.imgur.com/U4KcWyE.png)

## Recursos

- [Página da Earn](https://v1.yearn.finance/earn)
