# Como a Yearn aumenta o seu rendimento

Quase tudo aquilo que é interagido pelas yVaults está disponível ao público. Então como a Yearn consegue oferecer aos usuários um rendimento melhor do que os mesmos fariam sozinhos?

## Sinergia com a Curve Finance

Várias das estratégias da Yearn utilizam o programa de mineração de liquidez da Curve Finance. A [Curve Finance](https://curve.fi/) possui um programa de distribuição de tokens de 300 anos para aqueles que proverem liquidez exchanges decentralizadas com baixa derrapagem.

### Estímulos de veCRV

CRV é distribuido continuamente para usuários que fizerem staking de certos tokens de provedores de liquidez no [gauge](https://resources.curve.fi/base-features/understanding-gauges) da Curve. Essas recompensas em CRV podem ser aumentadas trancando os seus CRV no [Locker](https://dao.curve.fi/locker). Esse locker retorna ao staker veCRV, que lhe garante poder de voto na governança e uma porção das taxas do protocolo.

Trancar CRV permite aos usuários estimularem suas recompensar de CRV que eles recebem ao prover liquidez nas pools elegíveis. A quantidade de estímulo é determinada pela quantidade de CRV trancado e seu stake relativo na pool.

![](https://i.imgur.com/QaMMdr7.png)

Usando o yVault Backscratcher, a Yearn tranca uma quantia significativa de CRV indefinidamente, e distribui o estímulo para várias yVaults.

### yVault Backscratcher

A yVault Backscratcher capitaliza a mineração de liquidez de forma que é benéfica para ambas a Curve e a Yearn.

Usuários depositam CRV na yVault que é trancado indefinidamente. Em retorno eles recebem um token que representa uma partição da pool Backscratcher. A receita gerada pela curve por via da distribuição de taxas da curve é distribuída na pool da Backscratcher e pode ser redimido pelos depositantes toda semana.

Além disso, 10% de todos os CRV adquiridos pela Yearn Finance são depositados no Backscratcher e trancados indefinidamente. Por causa disso, as pessoas que querem fazer stake de CRV irão sempre receber uma partição maior da receita da yVault Backscratcher comparado a fazer staking diretamente na Curve. Eles também recebem emissões de tokens como SUSHI e PICKLE ao prover liquidez.

![](https://i.imgur.com/UfCikwk.png)

Usuários não poderão retirar seu CRV original, mas por causa dos incentivos na liquidez de yveCRV, e o valor que o token acumula vindo de várias fontes de receita, eles poderão troca-lo por outro ativo por algum preço.

Em retorno, o controle sobre os estimulos de CRV trancados é dado para a Yearn, e utilizado através de várias yVaults.

## Rendimento auto composto

Rendimento composto requer que taxas de transações sejam pagos na blockchain do Ethereum. Isso pode ser caro e cortar lucros.

Visto que yVaults agrupa sua transação com a de outros depositantes, o custo é cumulativamente menor e o retorno de farms usando a vault é maior. Hoje em dia, custos de gas são cobertos pela rede Keep3r, o que significa que usuários estão adquirindo seus retornos sem bancar por custos.

## Alavancagem

A Yearn utiliza o Iron Bank (C.R.E.A.M. Finance) para acessar crédito que é utilizado para aprimorar o rendimento das yVaults. Apenas endereços em uma lista branca podem utilizar, o que em geral implica que indivíduos não podem fazer isso por conta própria.

Algumas estratégias também implementam [flash loans](https://docs.yearn.finance/resources/defi-glossary#flash-loan), que são um serviço back-end que requerem experiência em desenvolvimento para ser usufruído.

## Parcerias

O yVault Backscratcher só é possível graças a sinergia entre protocolos como Curve, SushiSwap e Pickle Finance. Nosso relacionamento ao redor do ecossistema DeFi permite que depositantes das yVaults adquiram benefícios que não seriam possíveis em outro lugar.

A Yearn colabora ativamente no desenvolvimento com protocolos como os mencionados, que nos permite criar novas oportunidades de rendimento e avançar a indústria DeFi.
