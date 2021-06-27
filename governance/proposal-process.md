# Processo de Proposta

O ecossistema da Yearn é controlado por detentores de YFI que apresentam e votam em propostas na blockchain que governam o ecossistema. Propostas que possuírem apoio da maioria (>50% dos votos) são implementadas por uma carteira multi-assinatura de 9 membros.

Mudanças precisam ser assinadas por 6 dos 9 signatários para serem implementadas. Os [membros da carteira multi-assinatura](https://docs.yearn.finance/resources/faq#who-is-on-the-multisig) foram eleitos por detentores de YFI e estão sujeitos a mudanças em futuras votações.

# Discussão

Discussão relativas a mudanças no protocolo acontecem em várias plataformas, algumas sendo:

 - [Fórum de Governança](https://gov.yearn.finance/)
 - [Discord](https://discord.yearn.finance)
 - [Telegram](https://t.me/yearnfinance)

É ideal que se colete o máximo de feedback possível dos vários canais de comunicação antes de introduzir uma proposta formal. O fórum e o servidor do discord possuem canais dedicados para tópicos específicos.

# Proposta

## Tipos de Proposta

**Yearn Improvement Proposals** (YIPs) são veículos abrangentes para exerção dos poderes que os detentores do token possuem. Após o [YIP-61](https://gov.yearn.finance/t/yip-61-governance-2-0/10460), foram introduzidas as **Yearn Delegation Proposals** (YDPs), que permite detentores dos tokens executarem uma realocação de onde o poder de tomada de decisão é delegado.


![](https://i.imgur.com/ZRNp2Zq.png)

### Previous and current proposals Propostas atuais e anteriores
- Anteriores: [Repositório de Propostas](https://docs.yearn.finance/governance/proposal-repository)
- Atuais: [Snapshot](https://snapshot.page/#/yearn)

### Requisitos para aprovação de propostas
- Discussões de 3 dias no [fórum](https://gov.yearn.finance/)
    - Mínimo de 25% de votos a favor à mudança
- 1 YFI em possessão para submeter o snapshot
- [Snapshot](https://snapshot.org/#/ybaby.eth) de 5 dias com mais de 50% de votos a favor

## Making a proposal Criando uma proposta

Qualquer pessoa pode postar uma proposta no fórum para ser discutida com a comunidade. Se for promovida a votação off-chain (via [Snapshot](https://snapshot.page/#/yearn)), apenas aqueles que detém no mínimo 1 YFI podem submeter ao snapshot. Caso sua proposta seja promovida e você não possua YFI o bastante, os moderadores irão te ajudar.

O formulário padrão para propostas pode ser encontrado no [Github](https://github.com/yearn/YIPS/blob/master/yip-X.md) e no [fórum](https://gov.yearn.finance), se você fizer um post na aba de propostas ou discussões ele será auto preenchido no formulário.

**Recursos**:
- [Como criar propostas](https://gov.yearn.finance/t/proposal-how-to/106)
- [YIP 0: Propósito e Diretrizes para YIPs](https://yips.yearn.finance/YIPS/yip-0)
- [YIP 44: Aprimorar Categorias de YIPs](https://yips.yearn.finance/YIPS/yip-44)
- [YIP 55: Formalizar a Introdução ao YIP e o Processo de Votação](https://gov.yearn.finance/t/yip-55-formalize-the-yip-process/7959)

# Votação

## Como eu voto?

- Detentores ou usuários fazendo staking com YFI podem votar na página do [Snapshot](https://snapshot.page/#/yearn) da Yearn nos seguintes locais:
    - Sua carteira
    - yVault YFI V2 (o equivalente de possuir tokens yvYFI)
    - tokens de YFI/WETH LP do Balancer
    - tokens de YFI/WETH LP do Uniswap
  - tokens de YFI/WETH LP do Sushiswap em staking no MasterChef
  - Colateral MakerDAO YFI
  - Colateral YFI do Unit Protocol
    - Bancor

## Qual é a diferença entre votação na enquente do fórum e votação off-chain?

- Uma enquente apenas agaria o sentimento da comunidade em relação à proposta enquanto uma votação off-chain (via [Snapshot](https://snapshot.page/#/yearn)) é vinculativa e entra em efeito assim que passar.

# Implementação

Uma vez que uma votação de uma Snapshot for aprovada, mudanças serão implementadas pelo protocolo da Yearn ou pela equipe de operações e será assinado pelo multi-sig, se necessário.
