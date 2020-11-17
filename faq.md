# FAQ \(Portuguese\)

# Geral

## Investir o teu dinheiro na yearn é seguro?

- Por favor, tire suas próprias conclusões, avaliando os riscos e decidindo por ti mesmo.

## A yearn é auditada?

- Sim, podes encontrar a lista das auditorias aqui.

# Suporte e Feedback

- Se tiveres alguma questão ou dúvida acerca de como usar a yearn, podes nos encontrar no:

  - [Discord](http://discord.yearn.finance/)
  - [Telegram](https://t.me/yearnfinance)

- Se achas que alguma coisa pode ser melhorada, ou encontraste um bug, nós queremos tratar do assunto. Por favor, descreve-o no:

  - [Github](https://github.com/iearn-finance) - Cria um tópico no repositório relevante
  - [Forum](https://gov.yearn.finance/c/feedback/) - Cria um post

# Produtos:

## yearn.finance

- Em [yearn.finance](https://yearn.finance/) podes encontrar as diferentes interfaces para os vários produtos (Vaults, Earn, Zap, APR e Cover)

## Vaults

- [yearn.finance/vaults](https://yearn.finance/vaults)

### O que é um Vault?

- Os Vaults utilizam estratégias que automatizam a gestão dos teus fundos de forma a aproveitar as melhores oportunidades a nível de incentivos à liquidez (yield farming), rentabilizando ao máximo o teu capital.
- Foram desenhados de maneira a que a comunidade possa trabalhar junta de forma a construir e alterar estratégias com o objetivo de assegurar a melhor utilização possível do capital, em qualquer nível.
- Nestes duas publicações em blog, o Andre explica detalhadamente como funcionam os yearn finance v2 [vaults](https://medium.com/iearn/yearn-finance-v2-af2c6a6a3613) e os [Delegated Vaults](https://medium.com/iearn/delegated-vaults-explained-fa81f1c3fce2).
- Resumidamente, os vaults são capazes do seguinte:
  - A liquidez pode ser fornecida em qualquer ativo;
  - A liquidez é utilizada como colateral;
    - O colateral é gerido de maneira segura tal que nunca entres em insolvência (default);
  - Stablecoins são pedidas em empréstimo contra o teu colateral;
  - As stablecoins são fornecidas como liquidez numa ou mais aplicações, recebendo por isso incentivos (yield farming);
  - Os retornos (stablecoins recebidas para além do montante emprestado) são automaticamente vendidos para o ativo fornecido inicialmente e reaplicados no vault;

### Mas eu não poderia simplesmente fazer tudo isto sozinho?

- Sim, poderias, mas os vaults ajudam-te a poupar nos custos com gas, mantêm automaticamente o teu colateral/rácio de dívida de maneira a proteger-te da insolvência e auto-otimizam constantemente os fundos de forma a aproveitar as estratégias de aplicação de stablecoins mais rentáveis que estejam disponíveis, mesmo enquanto dormes.

### O ROI apresentado na página dos vaults é o atual rendimento percentual anual (APY)?

- Não. É a média histórica para esse vault. Retornos/APYs atuais ainda não são apresentados, já que os vaults são um produto em fase beta que estão a ser testados atualmente.
- Existe uma série de outros websites externos que apresentam as APYs e outras informações, estão listados abaixo em [Estatísticas](https://docs.yearn.finance/faq#statistics).

### Quais são os riscos?

- Enquanto que os ativos depositados não podem decrescer, a dívida do vault pode. Se a estratégia não for capaz de obter um retorno superior á dívida, então uma porção do ativo ficará impermanentemente indisponível. Assim que a estratégia em vigor passar a ser mais rentável que a dívida, o ativo ficará outra vez disponível gradualmente.
  - Apesar de existirem mecanismos nos vaults que impedem isto de acontecer, nada é infalível.
- Até agora, os Vaults ainda não foram auditados.
- Existe risco de erro de "smart contracts" em qualquer dos contratos com os quais os vaults interagem.

### Quais são os diferentes vaults? (needs updating)

- Vaults v2:
  - aLINK
  - LINK
- Vaults v1:
  - curve.fi/y (yCRV)
  - DAI
  - TUSD
  - USDC
    - Receberás yyUSDC. Não é o mesmo token que recebes usando o produto Earn, ainda que toda a gente os trate identicamente.
  - USDT

### Porque é que os retornos dos dois vaults LINK são diferentes em stats.finance.yearn?

- O vault aLINK tem uma taxa de seguro de 0.5%.

### Se a estratégia atual do vault yCRV é utilizar a liquidez fornecida de forma a receber incentivos em CRV, quer dizer que irei receber CRV quando retirar os meus fundos?

- Não. A estratégia atual vende o CRV recebido por yCRV automaticamente, pelo que simplesmente receberás mais yCRV.

### Porque é que yCRV não vale exatamente \$1, é uma stablecoin certo?

- Não, yCRV não vale necessariamente \$1 nem é uma stablecoin. Podes encarar yCRV como um índice de stablecoins que geram juro e também comissões resultantes de trocas feitas na Y pool da Curve. Assim sendo, o valor de yCRV está em constante crescimento.

### Se eu retirar o meu yCRV do vault yCRV, esse yCRV é automaticamente revertido de volta para a Y pool da Curve ou é preciso eu fazer alguma coisa, como depositá-lo na Y pool de novo?

- Quando yCRV é retirado do vault, é recebido de volta + retornos obtidos - as taxas pagas, tudo em yCRV. Como é o próprio token yCRV que recebes de volta, isso quer dizer que continua depositado na Y pool da Curve e continuará a ganhar valor devido a trocas entre stablecoins utilizando a pool. Não tens portanto que fazer mais nada, a não ser que queiras fazer staking manualmente na curve de forma a gerar CRV.

### Porque é que não é possível obter um retorno (APY) melhor no vault YFI?

- Não faz sentido comparar os valores do vault de um ativo com os valores gerados por outro ativo completamente diferente, já que para alguns ativos existem muito menos estratégias disponíveis, com diferentes rentabilidades. Por exemplo, o vault sBTC utiliza a mesma estratégia que o vault yCRV (gerar CRV via staking) e, por isso, apresenta valores semelhantes. Ao mesmo tempo, como não existem muitas plataformas que aceitem YFI como depósito, existem poucas estratégias de aplicação de YFI disponíveis e, por isso, os retornos são limitados.

### Eu fiz um depósito num vault. O que é que eu receberei quando retirar o meu depósito, exatamente?

- Em primeiro lugar, receberás de volta sempre o mesmo ativo que depositaste. A quantia recebida será equivalente ao depósito inicial + a tua proporção do retorno gerado pelo vault - taxas.

### Quais são as taxas?

- Existe uma taxa de 0.5% sobre o total dos fundos retirados do vault.
  - Cada vault tem uma parte dos fundos inativos e maior parte dos fundos a serem usados para a estratégia atual. Os fundos inativos são a diferença entre o montante total detido pelo vault e o montante detido pela própria estratégia. Estes montantes podem ser visualizados em feel-the-yearn (link).
  - Quando retiras os teus fundos, se eles vierem dos fundos inativos, não é cobrada nenhuma taxa. Se vierem da estratégia, no entanto, será cobrada uma taxa de 0.5% do total.
- Além disso, determinadas transações geradoras de lucro que a estratégia execute resultam numa taxa de 5% para subsidiar os custos com gas sempre que a funcão harvest() é chamada.
  - Para estratégias criadas pela comunidade, como o novo vault yETH, 10% dessa taxa de 5% é recebida pelo criador da estratégia, enquanto que o resto acresce à tesouraria da yearn.

### Podes explicar a taxa de 5% para subsídio de custos com gas?

- Utilizando o vault USDC como exemplo, quando a função harvest() é chamada, o lucro gerado vem de três fontes:
  - Juros por estarem depositados na Compound.
  - COMP recebido que é liquidado de volta para USDC.
  - Tokens DF da DForce recebidos que também são liquidados para USDC.
- Neste caso, só a 3ª transação (receber e vender os DF tokens) é que incorre a taxa de 5% de subsídio aos custos com gas.
- Essa taxa é cobrada pois o sistema utiliza gas adicional que de outra forma não teria sido usado.

<<<<<<< HEAD

- **0.5% fee** on funds withdrawn from active strategies
  - Each vault has some amount of the total funds idle and most of them active in the strategy. The idle funds are the difference between `vault holdings` and `strategy holdings`, you can see them on [feel the yearn](https://feel-the-yearn.app/).
  - When you withdraw, if your funds come from the idle funds, you won't be charged any withdrawal fee. If they come from the strategy, you will be charged the 0.5% fee.
- **5% fee** on additional yield
  - # For community-made strategies, like the new yETH vault, currently 10% of this fee goes to the strategy creator. The other 90% goes to the treasury and is then distributed to governance.

### Para onde vão as taxas?

> > > > > > > ce18874... Add Portuguese version

- As comissões são direcionadas para um contrato específico de tesouraria.
  - Endereço: Tesouraria Yearn
- Até chegarem ao limite de \$500k, continuam na tesouraria, e, assim que se chegue a esse limite, o excesso é reencaminhado para o contrato de governância (??governance staking contract??).
  - Endereço: ygov.finance governance staking

### As taxas sempre foram parar nesses endereços?

- Não, no início da yearn iam diretamente para o Andre.
  - Endereço: 0x2d407ddb06311396fe14d4b49da5f0471447d45c
- Eventualmente, foram entregues ao endereço multi-assinatura e recebidas aí diretamente.
  - Endereço: 0x2d407ddb06311396fe14d4b49da5f0471447d45c
- E, antes da criação do atual contrato de governância (v2), as staking rewards eram encaminhadas para:
  - Endereço: 0xb01419E74D8a2abb1bbAD82925b19c36C191A701

### Retornos

- No futuro, estará disponível uma dashboard que te permite visualizar todas as tuas posições e investimentos, tal como as suas atuais APYs. Dado que os Vaults agora ainda estão em fase beta, atualmente as APYs não são mostradas no website, mas são postadas no [Twitter](https://twitter.com/iearnfinance) diariamente. É também possível obter uma estimativa aproximada observando a [atual estratégia](https://feel-the-yearn.vercel.app/) em vigor e verificando manualmente qual a sua APY.
- Por exemplo, se a atual estratégia do vault yCRV é staking dos tokens LP da curve.fi/y pool na DAO da Curve de forma a receber CRV, pode-se usar as APYs disponibilizadas na [homepage da Curve](https://www.curve.fi/) como estimativas.

<<<<<<< HEAD

- No, when yearn started they went directly to Andre's [address](https://etherscan.io/address/0x2d407ddb06311396fe14d4b49da5f0471447d45c).
- Then we handed off to the [multisig](https://etherscan.io/address/0xFEB4acf3df3cDEA7399794D0869ef76A6EfAff52) and fees went directly there.
- # And before our current gov v2, staking rewards went [here](https://etherscan.io/address/0xb01419E74D8a2abb1bbAD82925b19c36C191A701)

### Estratégias dos Vaults

> > > > > > > ce18874... Add Portuguese version

#### O que é a estratégia de um Vault?

<<<<<<< HEAD

- We plan to make a dashboard in the future that will clearly show your current APY of all the positions you have open. Currently for the Vaults as they are still in beta we are not showing the APY live, but it is post on [twitter](https://twitter.com/iearnfinance) around once a day. You can roughly estimate the yield you are getting by looking at what the [current strategy](https://feel-the-yearn.vercel.app/) is farming and checking what its APY is.
- # For example if yCRV vault is farming the CRV token, you can check what the yield is on [Curve's homepage](https://www.curve.fi/) for the Y pool
- As estratégias dos vaults da Yearn são smart contracts modulares para cada ciclo que 'diz' ao vault que ativos usar como colateral, que ativos pedir emprestado, que contrato/plataforma usar para receber incentivos á liquidez e onde vender os ativos recebidos como incentivo.
  > > > > > > > ce18874... Add Portuguese version

#### Quais são as estratégias atuais?

- Atualmente, é possível verificar quais as etratégias em vigor em [feel-the-yearn](https://feel-the-yearn.vercel.app/). No futuro, planeamos disponibilizar uma dashboard que descreva as estratégias de maneira clara, tal como os seus retornos (APYs).

#### Quem controla as estratégias?

- Atualmente, são escritas pelo Andre, mas necessitam aprovação do endereço multi-assinatura para serem implementadas.

<<<<<<< HEAD

- You can view the current strategies implemented at [feel-the-yearn](https://feel-the-yearn.vercel.app/).
- # In the future we plan to make a dashboard to make the strategies and APY easy to understand.

#### Como é que eu posso desenvolver uma estratégia?

> > > > > > > ce18874... Add Portuguese version

- Para já, a melhor maneira é postar nos fóruns da yearn na seção das Estratégias, detalhando que ativos usa, de que maneira os usa, quais os incentivos á liquidez que aproveita, como/onde vende os incentivos recebidos, etc. Eventualmente, será disponibilizado um template para facilitar a criação de estratégias.

<<<<<<< HEAD

- # Andre and other developers write them but the multi-sig decides if they will be implemented or not.

#### Como é que uma estratégia muda e quem é que a muda?

> > > > > > > ce18874... Add Portuguese version

- Para já, o Andre está atento aos mercados e desenvolve estratégias que ele e o comitê multi-assinatura considerem seguras, mas suficientemente rentáveis. Dependo dos diferentes retornos disponíveis no mercado, podem ser alteradas.

## Earn

<<<<<<< HEAD

#### What is the process for getting my strategy onto yearn?

- # Post it on the forum and if it gets approved it will be used in the vaults and you can get paid for it.
- [yearn.finance/earn](https://yearn.finance/earn)

### O que é a Earn?

> > > > > > > ce18874... Add Portuguese version

- A Earn é um agregador de rendimentos que utiliza diferentes plataformas de crédito (lending&borrowing) e distribui fundos por essas plataformas de forma a receber o juro mais alto possível, sendo que redistribui os fundos entre plataformas automaticamente de forma a receber sempre o maior rendimento possível.
- Deposite stablecoins - DAI, USDC, TUSD, USDT ou sUSD - na Earn e serão automaticamente emprestadas á plataforma que pague a maior taxa de juro atualmente, de entre a [Compound](https://compound.finance/), a [Dydx](https://dydx.exchange/), a [Aave](https://app.aave.com/home) ou a dForce (a DDex e a Fulcrum estão atualmente desativadas).
- Aprende mais em [Yearn Docs](https://docs.yearn.finance/yearn.finance/yearn).

<<<<<<< HEAD

- # For now Andre watches the markets and writes strategies that he and the multi-sig thinks are safe while giving the highest yield. They change them according to current yields on the market.

## Zap

> > > > > > > ce18874... Add Portuguese version

- [yearn.finance/zap](https://yearn.finance/zap)

### O que é a Zap?

- A Zap permite aos utilizadores converter um token suportado em outro com apenas uma interação com um contrato, o que reduz significativamente os custos de transacção.
- A Zap foi desenvolvida pela DefiZap (que é agora a [zapper.fi](https://zapper.fi/)) como uma espécie de um serviço de routing tudo-em-um para ativos/tokens utilizados em DeFi.

### Porquê usar a Zap?

- A Zap permite-te entrar numa posição numa plataforma DeFi em uma única transação - chama-se 'zapping in' -.
- Como usar a Zap? - '[How to use Zaps - Guide](https://defitutorials.substack.com/p/how-to-use-defizap)'
  - Notar que este é um artigo antigo antes da [Zapper](https://zapper.fi/) ter sido formada como resultado da combinação da DefiZap + DefiSnap em um único hub definitivo para finanças descentralizadas, por isso alguma informação poderá estar fora de data, mas é mais que suficiente para conseguires usares Zaps na zapper.fi.

### O que é que eu posso fazer com Zaps na yearn?

- Podes, por exemplo, pegar em DAI e transformá-la em liquidity pool tokens da [curve.fi/y pool (yCRV)](https://www.curve.fi/iearn/deposit) numa única transação. Para comparar, o processo normal seria pegar em DAI, depositá-la na yearn e receber yDAI e só depois ir a curve.fi para depositar a yDAI e receber yCRV. As Zaps transformam este processo em uma só transacção.

### Isso parece-me ótimo, mas quais são as desvantagens?

- Bem, dado tratar-se de uma transação mais complexa, os custos em gas podem ser bastante altos, em alguns casos até mais altos do que executando o processo manualmente. Assim, é ideal caso queiras, por exemplo, sair (ou entrar) de uma posição/investimento com urgência ou, também, caso um usuário prefira uma forma simples e não-técnica de participar em DeFi.

## APR

- [yearn.finance/apr](yearn.finance/apr)

### Qual é o objetivo desta página?

- Na página APR podes encontrar uma tabela que te mostra os juros pagos a depósitos em tokens suportados pela yearn em diversas plataformas de crédito. Nessa tabela, a plataforma que, para dado ativo, tiver o retorno/juro mais alto é a plataforma que a yearn usa atualmente para depósitos desse ativo.

## Cover

- [yinsure.finance](yinsure.finance)

### O que é o Cover?

- Também conhecida como yInsure, o **Cover** é um serviço de cobertura conjunta (ou seja, 'pooled') que disponibiliza seguros contra o risco de falhas em smart contracts.
- Não exige verificação da identidade (Know Your Customer) e é subscrita pela Nexus Mutual.
- Aprenda mais neste [artigo Medium](https://medium.com/iearn/yinsure-finance-a-new-insurance-primitive-77d5d4217896).

## Outros produtos atualmente em fase de teste

<<<<<<< HEAD

#### So what can I do with Zaps on yearn?

=======

### yTrade

> > > > > > > ce18874... Add Portuguese version

- [ytrade.finance](ytrade.finance)
- Trades alavancadas entre diferentes stablecoins (testnet)

### yLiquidate

- [yliquidate.finance](yliquidate.finance)
- Liquidações de zero-capital automatizadas para a Aave (testnet)

### ySwap

- [yswap.exchange ](yswap.exchange)
- Criador de mercado 'single side' (que aceita liquidez em um único ativo) automatizado (em teste na mainnet)

### yBorrow

- [yborrow.finance](yborrow.finance)
- Vaults com delegação de crédito para empréstimos entre smart contracts (testnet)

<br>

# Tokens

## YFI

- O token de governância da Yearn.
- Existem 30000 e já foram totalmente distribuídos.
  - A governância pode emitir mais, caso os detentores de YFI votem a favor de uma proposta que implemente novas emissões.

## yTokens

- Quando depositas um ativo em qualquer dos serviços da Yearn, o teu depósito é empacotado por um wrapper e devolvido como um yToken que representa a liquidez providenciada.
- Por exemplo, se depositares DAI em y.curve.fi, receberás yDAI.
- As quantias depositadas em dado token e recebidas na forma do yToken correspondente serão sempre diferentes, já que o yToken representa uma parte de uma 'pool' cujo valor está constantemente a aumentar (porque recebe juros, taxas de trocas, incentivos á liquidez, etc).
- Ao depositares um yToken noutro serviço da yearn, naturalmente também receberás de volta um yyToken.

## yCRV

- Token LP da curve.fi/y pool
- Ou seja, yDAI+yUSDT+yUSDC+yTUSD
- Token a que acresce juros representante da tua porção da Y pool, composta por DAI, USDT, USDC e TUSD;
  - É um dos produtos mais populares da Curve, já que recebe tanto juros por estar emprestado através da yearn (que escolhe a plataforma mais rentável entre a Compound, a Dydx e a Aave) como taxas de troca da Curve por estar também depositado para facilitar swaps.
  - Mais informação em How to provide liquidity on Curve.fi Y pool

## yUSD

- yUSD é o LP token do vault yCRV da yearn, previamente conhecido como yyCRV ou yyDAI+yyUSDT+yyUSDC+yyTUSD. Ou seja, é yUSD que recebes de volta quando fazes um depósito em yCRV no vault yCRV.
- Para além dos juros e taxas de troca que já acrescem ao valor de yCRV, o LP token yUSD recebe rendimentos provenientes da execução da estratégia do vault.
  - Neste caso recebe também os retornos resultantes da incentivização á liquidez via geração de CRV.
  - O CRV gerado é vendido por yCRV e devolvido ao vault, daí que o valor de yUSD seja superior ao valor de yCRV (da mesma maneira que o valor de yCRV é superior ao valor de DAI/USDC/USDT/TUSD já que acresce de juros e taxas de troca).

<br>

# Comunicação

- [Fóruns](https://gov.yearn.finance)

  - Grande parte da discussão em tempo real acontece no Telegram e no Discord, mas para que uma proposta seja partilhada com a comunidade e eventualmente transformada num YIP (Yearn Improvement Proposal) oficial tem que ser postada e discutida nos fóruns.
  - Este é a principal plataforma onde os detentores de YFI encontram toda a discussão em termos de assuntos relacionados com a governância da Yearn.

- [Discord](https://discord.gg/94CmMdt)

  - Incluindo canais em várias línguas que não o inglês

- [Telegram](https://t.me/yearnfinance)

  - Canal principal

- [Telegram](https://t.me/yearncommunity)

  - Canal social/de trading

- Twitter
  <<<<<<< HEAD
  - [yearn.finance](https://twitter.com/iearnfinance?s=20) - Official Twitter of Yearn
  - [Andre Cronje](https://twitter.com/AndreCronjeTech?s=20) - Lead Developer of Yearn
  - [yLearnfinance](https://twitter.com/yLearnfinance) - Yearn Info
  - # [Learn 2 Yearn](https://twitter.com/learn2yearn) - Yearn Info
  - [yearn.finance](https://twitter.com/iearnfinance?s=20) - Twitter oficial da Yearn
  - [Andre Cronje](https://twitter.com/AndreCronjeTech?s=20) - Programador-chefe da Yearn
  - [yLearnfinance](https://twitter.com/yLearnfinance) - Informações relativas á Yearn
  - [Learn 2 Yearn](https://twitter.com/learn2yearn) - Informações relativas á Yearn

<br>
>>>>>>> ce18874... Add Portuguese version

# Governância

## Tudo sobre YIPs

### O que são YIPs e porque é que interessam?

<<<<<<< HEAD

- # A YIP or Yearn Improvement Proposal is how features are added to the yearn ecosystem. Users start a proposal on the forum, discuss it and gauge the sentiment of if the proposal will be accepted. If a lot of users agree with it then it can be posted on-chain for everyone to vote on.
- Uma YIP ou Yearn Improvement Proposal é modo como alterações são feitas ao ecossistema da yearn. O(s) utilizador(es) cria uma proposta nos fóruns, discute-a com a comunidade e mede a recetividade da comunidade para com a mudança em causa. Se for claro que se trata de uma proposta suportada pela maior parte da comunidade, então a proposta será postada on-chain (ou seja, na própria blockchain) para que os detentores votem com o seu YFI.
- Qualquer holder de YFI pode submeter uma proposta on-chain mas se esta não for postada e discutida nos fóruns pela comunidade, é pouco provável que os detentores votem em seu favor.
  > > > > > > > ce18874... Add Portuguese version

### Quantos detentores têm de votar para passar um YIP proposto on-chain?

- O quorum (a percentagem mínima dos votos totais que tem de participar) é de 20%. Ou seja, pelo menos 20% dos YFI tokens que estejam em staking no contrato de governância têm de votar para que a proposta passe. Naturalmente, para que tal aconteça é também necessário que mais do que 50% dos votos sejam a favor da proposta.

### Como é que eu faço uma proposta?

- O template base para redação de propostas está disponível no [github](https://github.com/iearn-finance/YIPS/blob/master/yip-X.md). Além disso, se criares um post nos [fóruns](https://gov.yearn.finance/) usando o tópico Proposta, esse template aparecerá automaticamente no corpo do post.
- Assim, o processo para implementação de uma proposta é basicamente:
  - Discussão nos fóruns
  - Caso seja bem recebida, os moderadores promoveram a proposta a YIP nos fóruns e será adicionada à lista de YIPs
  - Redação da proposta no github e, em seguida, publicação on-chain
  - Anúncio e promoção da proposta
  - Votação e, se aceita, implementação

### Quem é que pode fazer uma proposta?

- Qualquer pessoa, tanto nos fóruns como on-chain.

## Votação

### Como é que eu voto?

- Em primeiro lugar, é necessário que tenhas YFI e que este esteja em staking staked no contrato de governância. Caso assim seja, na [dashboard](https://ygov.finance/vote) de voto verás as YIPs atualmente on-chain e poderás submeter o teu voto.

### Eu posso votar se tiver o meu YFI depositado no vault yYFI?

- Não, tem obrigatoriamente de estar staked no [contrato](https://ygov.finance/staking) de governância.

### Onde é que eu posso ver as YIPs?

- Podes vê-las na [dashboard](https://ygov.finance/vote) de voto conetando-te com a tua conta web3 (a tua wallet, como a Metamask por exemplo) ou simplesmente em [yips.yearn.finance](https://yips.yearn.finance/all-yip)

### Qual é a vantagem de eu colocar YFI na governância? Qual é o retorno anual (APY)?

<<<<<<< HEAD

- # You should stake if you want to vote on YIPs and get rewards that are generated from the yearn ecosystem. The APY for staking is currently not listed on the UI. You can ask on the chat what the rate is.
- Tu deves procurar fazer staking de YFI no contrato de governância caso estejas interessado em votar nas YIPs e receber as recompensas geradas pelo ecossistema da yearn (as receitas resultantes das diferentes taxas cobradas).
- O retorno atual proveniente dessas recompensas não é apresentado atualmente na webpage, dado que a yearn só gera receitas há relativamente pouco tempo e não são, para já, constantes. No entanto, podes perguntar no Discord ou no Telegram caso queiras saber qual a melhor maneira de o estimar.
  > > > > > > > ce18874... Add Portuguese version

### O que é que eu tenho de fazer com o meu YFI para receber recompensas?

- A única coisa que tens de fazer é assegurar que tens o teu YFI em staking no contrato de governância, em [ygov.finance/stake](https://ygov.finance/stake), e receberás recompensas desde que a tesouraria esteja acima do fundo operacional de \$500k. Podes ver o endereço da tesouraria aqui (link).
- Note, no entanto, que se as quiseres remover tens de ter votado nos últimos 3 dias.

### É obrigatório ter o meu YFI em staking para participar nas votações?

- Sim. Tens de ter o teu YFI em staking em [ygov.finance/stake](ygov.finance/stake) no segmento v2 para que os teus votos contem. Atualmente, podes iniciar uma transação de voto na dashboard de voto sem teres YFI em staking mas o teu voto não contará e desperdiçarás o custo em gas, portanto assegura-te sempre que tens o YFI em staking antes de votar.

### E se, após votar, eu quiser retirar o meu YFI do contrato de governância antes do período de 3 dias de 'lock' (??tradução), posso fazê-lo?

- Não. O período de lock pós-voto é de 3 dias e enquanto durar, não é possível fazer unstaking do contrato de governância. Antes de votar, certifica-te sempre que não vais precisar mover o teu YFI nos próximos dias.

### Eu votei e sei que o 'lock' pós-voto é de 3 dias, é possível saber quanto tempo falta até que possa retirar o meu YFI do contrato de governância?

- Sim. Podes referir ao contrato de [governância diretamente](https://etherscan.io/address/0xBa37B002AbaFDd8E89a1995dA52740bbC013D992#readContract), vais ao número 28 - votelock e digite o teu endereço ethereum. O contrato irá dizer-te o número do bloco de ethereum a partir do qual já podes fazer unstake do teu YFI.

### Qual é a diferença entre votar numa sondagem nos fóruns e votar on-chain?

- Uma sondagem simplesmente serve para medir a recetividade/interesse da comunidade na proposta e o seu resultado não é de maneira nenhuma vinculativo. No entanto, se uma proposta for aceita on-chain, esse veredicto é vinculativo e será obrigatoriamente implementado.

### E o novo mecanismo de voting sem custos de gas, qual é o seu propósito?

- Atualmente, já temos disponível um mecanismo de sinalização off-chain que utiliza os balanços de staking de cada endereço que vota. Este mecanismo veio substituir as sondagens informais nos fóruns que eram vulneráveis a ataques de sybil.
- É possível criar propostas de múltipla excolha e os votos não exigem uma transação com custos em gas, simplesmente assinas o voto com o teu endereço. Para os YIPs, é utilizada a votação on-chain normal via a dashboard em ygov.finance

### Quanto tempo é que o meu YFI fica trancado se eu o colocar em staking e votar num YIP?

- Após um voto, o YFI fica trancado durante 3 dias.

### Porque é que eu não posso remover as minhas recompensas de staking?

- Para poderes receber as recompensas, tens de:
  1. Estar em staking no contrato de governância;
  2. Ter votado;
- Após votar, poderás remover as tuas recompensas durante um período de 3 dias. Isto será resolvido brevemente em um update.

## yDAO

- Website [Pokemol](https://pokemol.com/dao/0xcb46298767fb5d44c18313976c30d3eeb5071862/)

- Post introdutório nos [fóruns](https://gov.yearn.finance/t/ydao-for-community-funding/2243)

<<<<<<< HEAD

- # Used to fund value-added contributions to the yearn ecosystem.

### Qual é o objetivo da yDAO?

> > > > > > > ce18874... Add Portuguese version

- Financiar contribuições criadoras de valor para o ecossistema da yearn.

### O que é que isso interessa, como é que eu faço dinheiro com a yDAO?

- Não fazes. O único propósito da yDAO é alocar financiamento para projetos, o YFI/DAI comprometido será gasto e o valor das tuas ações diluído.

### Quem é que pode participar?

- Qualquer pessoa pode receber 1 ou mais ações a um rácio de 0.1YFI por ação.

### Como é que eu participo?

- Vais á app [Pokemol](https://pokemol.com/dao/0xcb46298767fb5d44c18313976c30d3eeb5071862) e conectes a tua conta web3. Depois escolhe Nova Proposta e clique em Novo Membro.
  - Título: O teu nome/pseudónimo/entidade
  - Descrição: "Contribuo X quantidade de YFI em troca de Y ações" (Por favor, mantêm a consistência com o rácio de 0.1YFI contribuído por 1 ação)
  - Link: Introduz um link para uma página tua ou da tua entidade (website, twitter, Linkedin, etc...)
  - Ações requeridas: O número de ações que requeres.
  - Contributo: A quantidade de YFI que contribuis.
  - Saque: O número de ações que requeres.
- Após teres submetido as duas transações necessárias e estares na fila dos novos membros, vais precisar de um patrocinador. Por favor copie o link da tua proposta e vem nos dizer que queres entrar no canal de [Telegram da yDAO](https://t.me/joinchat/Qn1GPBv0y7lY1vAmRCB7KA).

### Como é que eu peço financiamento?

- O processo é o mesmo que para te registrares exceto que em vez de clicares em Novo Membro, utilizas o separador de financiamento e preenches com os detalhes do teu pedido. Se tiveres alguma questão, podes perguntar no canal de [telegram](https://t.me/joinchat/Qn1GPBv0y7lY1vAmRCB7KA).

<br>

# Comunidade

<<<<<<< HEAD

### Is Andre Cronje in charge of yearn?

- Andre isn't in charge of Yearn, the YFI token holders make the decisions on what to build and governance decisions, Andre is the lead developer of the yearn ecosystem.

### What does Andre do?

- # Andre is the main developer building out the products that comprise the yearn ecosystem: Yearn, Ytrade, Yswap, Yliquidate, Yborrow. He is also currently in charge of running the Vaults and overseeing them.

## O Andre Cronje está no comando da yearn?

- Não, o Andre não controla a yearn, quem o faz são os detentores de YFI, que tomam todas as decisões de governância. No entanto, o Andre é o programador-chefe e o responsável por grande parte das contribuições técnicas.

## O que é que o Andre faz exatamente?

- O Andre é o principal programador e contribuidor técnico para a implementação e desenvolvimento de todos os produtos que formam o ecossistema da yearn: Yearn, Ytrade, Yswap, Yinsure, Yliquidate, Yborrow, etc. Além disso, ele é responsável também, no momento, pela execução das estratégias dos Vaults e da sua supervisão.
  > > > > > > > ce18874... Add Portuguese version

## O que é que é o endereço multi-assinatura e o que é que ele faz?

- É uma conta de [multiassinatura](https://gov.yearn.finance/t/yfi-minting-ownership/155) 6-em-9 (ou seja, existem 9 participantes e no mínimo 6 têm de estar de acordo para poder ser feita uma transação) que têm controle sobre a emissão de YFI, caso algum voto para emissão de novos tokens alguma vez passe.

## Quem são os 9 assinantes do endereço multi-assinatura?

- [Cp0x.com](https://twitter.com/kaplansky1/status/1285427247286046725)
- [Daryllautk](https://twitter.com/Daryllautk/status/1285434908383444992)
- [Devops199fan](https://twitter.com/devops199fan/status/1285430347954622464)
- [Banteg](https://twitter.com/bantg/status/1285426492906909696)
- [Milkyklim](https://milkyklim.keybase.pub/yearn-social-proof.txt)
- [Joe Mahon AKA Substreight](https://twitter.com/Substreight)
- [Tarun Chitra, Gauntlet](https://twitter.com/tarunchitra)
- [Vasiliy Shapovalov, p2p.org](https://twitter.com/_vshapovalov)
- [Mariano Conti, ex-MakerDAO](https://twitter.com/nanexcool)

## Os partipantes deste endereço podem mudar?

- Sim, podem. De fato, a [YIP-40](https://gov.yearn.finance/t/yip-40-replace-inactive-multisig-signers/3535) determinou a substituição de 4 assinantes:
  - [Coopahtroopa](https://twitter.com/Cooopahtroopa/status/1285438650550038529)
  - [Michael, Curve.fi](https://twitter.com/CurveFinance/status/1285428322986389504)
  - [Calvin Liu](https://twitter.com/cjliu49/status/1285439553180798976?s=21)
  - [Damir Bandalo](https://twitter.com/damirbandalo/status/1285500362015875073?s=20)

## Que decisões é que o Andre pode tomar independentemente?

<<<<<<< HEAD

- # Andre can build out the Yearn ecosystem and come up with new products. Usually, he posts his thoughts and ideas on the [forum](https://gov.yearn.finance) for everyone to see.
- O Andre pode desenvolver o ecossistema da yearn autonomamente, desenvolvendo os produtos atuais e criando/concebendo novos produtos e ideias. Normalmente, ele posta as suas ideias e motivações nos [fóruns](https://gov.yearn.finance/) para que toda a gente veja e discuta.
  > > > > > > > ce18874... Add Portuguese version

## Quem mais escreve código para a yearn, existe alguma equipe?

<<<<<<< HEAD

- They are in close contact with one another, but Andre's priorities are decided by YFI token holders via YIPs.

### Who else writes code for yearn? Is there a team?

- Right now it's just Andre.

### Does anyone get paid for working on yearn?

- As of this moment, not yet, but thanks to the passage of [YIP 36](https://yips.yearn.finance/YIPS/yip-36) and the creation of a community pool of funds that will be kept at 500k usd, we can now pay Andre for his work, fund audits, and pay for new devs to be hired along with anything else the the yearn ecosystem needs.

### How can I work for yearn?

- # You can make a YIP to apply for funding from the 500k USD treasury directly or ask the yDAO for funding.
- Por enquanto é só o Andre.

## Há alguém que receba um salário para trabalhar na yearn?

- Por enquanto ainda não mas com a passagem da [YIP-36](https://yips.yearn.finance/YIPS/yip-36) e a criação de uma tesouraria comunitária mantida nos \$500k, já será possível pagar ao Andre pelo seu trabalho, financiar auditorias, contratar novos programadores e preencher qualquer outro cargo, dependendo das necessidades da ecossistema da yearn.

## Como é que eu posso trabalhar para a yearn?

- Podes criar uma proposta/YIP como aplicação a financiamento diretamente da tesouraria ou, então, podes requerir financiamento da yDAO.

## Existe alguma vaga disponível?

- Sim! Nós precisamos de todo o tipo de pessoas e competências para transformar a yEarn num ecossistema próspero, aumentar o número de utilizadores e particpantes e, assim, valorizar o YFI token.
- Podes perguntar no Discord ou no Telegram relativamente a aplicações ou podes também postar nos fóruns. Descreve a maneira como achas que podes acrescentar valor á yearn e quanto achas que precisas para financiar a tua atividade. Para além disso, podes requerir financiamento através da [yDAO](https://gov.yearn.finance/t/ydao-for-community-funding/2243).

## Como participar?

> > > > > > > ce18874... Add Portuguese version

- Podes participar na yearn votando em YIPs ativas, discutindo as YIPs que ainda não chegaram a votação on-chain, discutindo a yearn e YFI no telegram ou discord, ajudando usuários inexperientes, promovendo a yearn nas redes sociais, etc.
- Para além disso, se sabes uma linguagem que ainda não está disponível, podes nos ajudar a traduzir este site e todas as YIPs disponíveis.

<<<<<<< HEAD

- # Yes, we do! We need all kinds of people to help make the yEarn ecosystem a thriving product and to give value to YFI. You can ask in the Discord or Telegram about applying or post on the forum. State how you think you can add value to Yearn, and how much you think you should be paid from the community pool. Also, you can go to the [yDAO](https://gov.yearn.finance/t/ydao-for-community-funding/2243) as well for funding on your work for the Yearn ecosystem.

## Esforços decorrentes para melhorar o ecossistema da Yearn:

> > > > > > > ce18874... Add Portuguese version

- Podes encontrar os YIPs ativos [aqui](https://yips.yearn.finance/all-yip).

<br>

# User Interface

## Posso usar as dApps da yearn no meu celular?

- Sim, podes usar o browser da Metamask.

<br>

# Suporte Técnico

## Fiz uma transação de ETH mas aparece como pendente. Como é que eu resolvo isso?

- Deves sempre confirmar que escolheste um preço por gwei adequado se queres que a tua transação execute rapidamente. Podes verificar os preços de gas atuais em [ethgasstation.info](https://ethgasstation.info/) ou em [gasnow.org](https://gasnow.org).
- Se estás a usar o MetaMask e enviaste a transacção mas está a demorar mais tempo do que o que desejas, podes acelerar a tua transação clicando em `Speed Up` abaixo da transação pendente, no separador Activity da MetaMask.
- Se já tentastes acelerar a transação mas continua pendente, podes resolver esse problema enviando uma transação para a nonce da transação pendente, escolhendo um preço por gwei superior de forma a substituir a transação pendente. [Podes encontrar instruções sobre como fazer isto neste artigo](https://ethgasstation.info/blog/stuck-transaction-guide/#:~:text=Select).

## Porque é que a taxa de retirada do depósito (withdrawal fee) é tão alta?

- Se a taxa que observas quando tentas retirar o teu depósito é excessivamente alta, é possível que a ethereum esteja altamente congestionada e os preços de gas estejam muito altos. Confirme os preços de gas em [ethgasstation.info](https://ethgasstation.info/). Nesse caso, a única coisa que podes fazer é esperar que os preços baixem ou pagar uma taxa alta para teres os teus fundos disponíveis no momento.
- Se o preço da transação for absurdamente alto, é possível que exista um erro e que a transação não possa sequer ser processada. Por exemplo, podes estar a tentar depositar um ativo que não tens ou a tentar comprar um seguro em [yinsure.finance](http://yinsure.finance/) quando não existe cobertura disponível.

<<<<<<< HEAD

- If you're seeing higher than normal fees while using the yearn ecosystem then it may be due to Ethereum congestion and abnormally high gas costs. Check [Ethgasstation](https://ethgasstation.info/). Your options are to wait until gas prices drop or spend the money to process your transaction now.
- # If the gas prices are crazy high, that means there is an error and the transaction will not be able to process. For instance if you are trying to deposit a token you don't have or if there is no cover available for a contract at [http://yinsure.finance/](http://yinsure.finance/).
<br>
>>>>>>> ce18874... Add Portuguese version

# Projetos Relacionados

## [Curve](https://curve.fi)

- A Curve é uma exchange/'pool' de liquidez no ethereum (tipo [Uniswap](https://app.uniswap.org/#/)) cujo objetivo é permitir (1) trocas altamente eficientes entre diferentes stablecoins e (2) obtenção de um retorno suplemental de baixo risco para fornecedores de liquidez, sem custos de oportunidade. A Curve permite a utilizadores (e também outros contratos como a 1inch, Parawap, Totle e Dex.ag) passarem de DAI para USDC com uma derrapagem baixíssima, pagando apenas 0.04% em taxas. Para além disso, os ativos depositados na pool também são fornecidos a plataformas de crédito como a compound e a yearn.finance, gerando assim rendimentos adicionais via juros recebidos.
- [FAQ da Curve](https://www.curve.fi/rootfaq)

## [Aave](https://app.aave.com/home)

- A Aave é um protocolo open source e não-custodial que permite a criação de mercados de crédito.
- Usuários podem tanto depositar ativos e receber juros, tal como pedir determinados ativos emprestados.

## Recursos

<<<<<<< HEAD

### Where can I learn more about yearn?

=======

### Onde é que eu posso aprender mais sobre a yearn?

> > > > > > > ce18874... Add Portuguese version

- [Learn Yearn](https://www.learnyearn.finance/)
- [Medium.com/iearn](https://medium.com/iearn)
- [yCosystem](https://ycosystem.info/)

### Lista de Smart Contracts

- https://gov.yearn.finance/t/yearn-contracts/1951
- https://etherscan.io/accounts/label/yearn-finance
  - Exige sign-in
- [Delegated controller](https://etherscan.io/address/0x2be5d998c95de70d9a38b3d78e49751f10f9e88b#readContract)
- [StrategyVaultTUSD](https://etherscan.io/address/0x35CEE4c61B7619956e0B2015B5411F93CBba817A#code)
- [yLINK token](https://etherscan.io/address/0x881b06da56bb5675c54e4ed311c21e54c5025298#code)
- [yaLINK token](https://etherscan.io/address/0x29e240cfd7946ba20895a7a02edb25c210f9f324#readContract)
- [StrategyMStableSavingsTUSD](https://etherscan.io/address/0xd6214317bf66921154d78e3074bada013a4de8e8#readContract)
- [yTUSD](https://etherscan.io/address/0x37d19d1c4e1fa9dc47bd1ea12f742a0887eda74a)
- [yTokenRebalance](https://etherscan.io/address/0x19b6424C58aFcee6D0cb954D4B8d44B9b5e9cC09#code)
- [CollateralVaultProxy](https://etherscan.io/address/0xf0988322b8392245d6232e520bf3cdf912b043c4)
- [USDC strategy for LINK](https://etherscan.io/address/0x25fAcA21dd2Ad7eDB3a027d543e617496820d8d6)
- [Strategy for USDC vault](https://etherscan.io/address/0xA30d1D98C502378ad61Fe71BcDc3a808CF60b897)
- [DAI vault](https://etherscan.io/address/0xACd43E627e64355f1861cEC6d3a6688B31a6F952)

### Registo de tokens e contratos de utilidade

- https://docs.yearn.finance/yearn.finance/yearn-1

## Referência direta dos Vaults

- https://vaults.finance/

## Estatísticas

- [yieldfarming.info](https://yieldfarming.info/)
- [Calculadora de ROI dos yVaults](https://py-earn.herokuapp.com/)
- [stats.finance/yearn](https://stats.finance/yearn)
- [Feel The Yearn](https://feel-the-yearn.vercel.app/)
- Distribuição inicial da Yearn - [Dune Dashboard](https://explore.duneanalytics.com/dashboard/yearn)
- Estatísticas de Voto - [Dune Dashboard](https://explore.duneanalytics.com/public/dashboards/Lqnxzm7fa8NVhKC4kc37DDFPZgqXryaIjyLRYAYp)

## Últimas notícias relacionadas à yearn

- [yearn.finance - Twitter oficial da Yearn](https://twitter.com/iearnfinance)
- [AndreCronjeTech](https://twitter.com/AndreCronjeTech)
- [Yearn Finance - Blog oficial](https://medium.com/iearn)

## Podcasts

- [Andre Cronje and the Philosophy of Yearn Finance](https://anchor.fm/hasu-research/episodes/6-Andre-Cronje-and-the-Philosophy-of-Yearn-Finance-ei4vds)
- [The FTX Podcast - Andre Cronje DeFI Architect](https://open.spotify.com/episode/6d14TJtQU7eB69azelpdeh)
- [Zapper Community Call - With Andre](https://www.youtube.com/watch?v=venoiaiVZ-U)
- [In DeFi My Money is Actually Mine. Its a Beautiful Concept But it Comes With Responsibilities - Andre Cronje](https://anchor.fm/camila-russo/episodes/In-DeFi-My-Money-is-Actually-Mine--Its-a-Beautiful-Concept-But-it-Comes-With-Responsibilities-Andre-Cronje-ehs3op)
- [YFI: Farming the Farmers | Andre Cronje](http://podcast.banklesshq.com/25-king-of-the-yield-farmers-andre-cronje)

## Blogs

- [Yearn Finance - Blog oficial](https://medium.com/iearn)
  - [Yinsure.finance: A new insurance primitive](https://medium.com/iearn/yinsure-finance-a-new-insurance-primitive-77d5d4217896)
  - [Explicação dos Delegated Vaults](https://medium.com/iearn/delegated-vaults-explained-fa81f1c3fce2)
  - [Yearn.finance v2](https://medium.com/iearn/yearn-finance-v2-af2c6a6a3613?source=---------3------------------)
  - [Forúns de Governância da Yearn](https://medium.com/iearn/yearn-governance-forum-7b7c9d0300ac?source=collection_home---6------2-----------------------)
  - [YFI rewards pool](https://medium.com/iearn/yfi-rewards-pool-810ef9256ec6)
  - [YFI](https://medium.com/iearn/yfi-df84573db81)

## Logotipos

- Podes vê-los no discord em [#media-resources](https://discord.com/channels/734804446353031319/736132884443955242/740325105904779326)
