# Governança e Operações  

Desde que o [YIP-61: Governance 2.0](https://gov.yearn.finance/t/yip-61-governance-2-0/10460) passou no dia 25 de Abril de 2021, a yearn começou sua transição para uma estrutura **multi-DAO**, gerenciada por uma **delegação limitada**. Essa abordagem permite ao desenvolvimento do protocolo se manter flexível, evitando bloqueios burocráticos enquanto mantém um nível suficiente de descentralização.

Multi-DAO se refere ao número flexível de organizações autônomas descentralizadas (DAOs) que contribuem para o protocolo de formas únicas. Esses grupos independentes consistem de detentores de YFI, yTeams e as multi-assinaturas (Multisigs).

- **Detentores de YFI** votam nas mudanças no protocolo ou na estrutura de governança do protocolo
- **yTeams** focam em aspectos específicos do protocolo ou em operações relevantes
- Membros com **Multisigs** executam ou vetam decisões on-chain

Detentores do token têm a palavra final em relação a qual yTeams existem, quem faz parte do Multisig, e as limitações do controle operacional de cada grupo. O termo 'delegação limitada' provém dos detentores de tokens, delegando certas competências para vários grupos que desenvolvem e gerenciam a yearn.

Um processo de governança simplificado se assemelha ao seguinte:

    1. Detentores de YFi criam, desfazem e definem limitações nas yTeams
    2. A yTeam notifica a yTx sobre a decisão
    3. A yTx cria uma transação delegada e a envia para o Multsig
    4. O Multisig executa ou veta a transação

## Responsabilidades da DAO

![](https://i.imgur.com/IDysF5O.png)

### Detentores do Token

É dever dos detentores do [token YFI](https://docs.yearn.finance/governance/yfi) criar e votar em propostas que aprimorem o protocolo.

| Propostas | Descrições |
|-----------|--------------|
|Yearn Improvement Proposal (YIP)|Uma proposta para execução de qualquer poder delegado aos detentores de YFI, ou que está além do escopo dos poderes enumerados|
|Yearn Delegation Proposal (YDP)|Uma proposta para mudança de onde a tomada de decisão discreta deve ser delegada|
|Yearn Signaling Proposal (YSP)|Uma proposta livre de vínculos onde o sentimento da comunidade é sinalizado, alternativamente também serve para chamar atenção sobre algum problema|

Essas propostas permitem os detentores do token executar as seguintes mudanças:

| Poder | Descrição |
|-------|-------------|
|Gerenciamento de poderes|Detentores de YFI podem votar em criação, atribuição ou revogação de poderes discretos que vem ou que parte da yTeams|
|Modificar o contrato do token YFI|Qualquer interação com o contrato do token YFI, como emissão de YFI ou queima das chaves de emissão, continua sob o controle de detentores de YFI|
|Estabelecimento de Taxas|Estabelece o padrão de estrutura de taxas no protocolo da Yearn|
|Reeleger os signatários da Multi-assinatura|Como a multi-assinatura continua a reservar poderes críticos no curto prazo, apenas detentores de YFI tem o poder de eleger os signatários|
|Ratificar yTeams|Ratificar ou desratificar yTeams de forma formal, para controlar quais yTeams podem possuir poderes delegados|
|Mudar os signatários yOps|Como o yOps tem poder sobre a designação de signatários de outras yTeams, essa posição possui a função especial de modificar os signatários da yOps|
|Gasto de fundos do Tesouro|Gastar fundos do tesouro|
|Poder YIP|Detentores de YFI tem o poder de propor YIPs em qualquer coisa que não esteja atualmente delegada|

### yTeams

Cada yTeam tem objetivos e poderes que são definidos pelos detentores do token. Eles podem ser partilhados em pools de filiados, que são grupos aparte de contribuidores trabalhando em prol de fins semelhantes aos da equipe dominante. Além disso, uma pool de filiados podem pertencer a múltiplas yTeams.

| yTeam | Objetivo | Pool de Filiados |
|-------|-----------|-----------------|
|yGuard|Proteger as vaults|YFI Protocol Dev, YFI Strategists, YFI Mechanics, YFI Secret Admirers|
|yBrain|Gerenciar as estratégias|YFI Strategists|
|yDev|Gerenciar o protocol|YFI Protocol Dev|
|yPeople|Curar a equipe|YFI Compensation Working Group, YFI Advisors|
|yBudget|Gastar os fundos de forma apropriada|YFI Finances, YFI Advisors|
|yFarm|Crescer o Tesouro|YFI Secret Admirers, YFI Secret Entrance|
|yTx|Escrever transações|YFI Doers|
|yOps|Coordenação de contribuidores|YFI Ops|

Cada yTeam é atribuída com certos poderes de decisão, definidos pela YIP-61:

| yTeam | Poder | Descrição |
|-------|-------|-------------|
|yGuard|Poderes de Emergência|Intervenção imediata em caso de ataques ou bugs, paralisando ou executando rollbacks em estratégias ou vaults|
|yBrain|Gerenciamento de estratégias|Ativa, desativa, ajusta e mantem estratégias|
|yDev|Definição do Protocolo Yearn|Decide quais códigos são considerados parte da yearn e quais não são|
|yDev|Gerenciamento do Protocolo|Mantém e aprimora o Protocolo Yearn|
|yDev|Adição de Estratégias|Adiciona novas estratégias as vaults|
|yTx|Delegar Transações|Gera transações delegadas para o Multisg assinar e executar|
|yPeople|Pagamento da equipe|Gera, implanta, modifica ou termina pacotes de compensação da Yearn|
|yBudget|Definição de verba|Gera verbas para a coordinape, subsídios, contratações, operações e outros campos de atuação|
|yFarm|Farmar o Tesouro|Farma com o tesouro e faz decisões em relação a airdrops|
|yOps|Ratifica signatários da yTeam|Oficialmente aprova ou remove signatários para cada yTeam|

### Multisig

Decisões decretadas pelas yTeams serão executadas na blockchain pelo Multisig até que um sistema mais descentralizado for aprovado para implementação. No meio tempo, o [Multisig](https://docs.yearn.finance/resources/faq#who-is-on-the-multisig) controla o seguinte:


| Poder | Descrição |
|-------|-------------|
|Poder de execução|O poder de executar decisões feitas pelos detentores de YFI e pelas yTeams na blockchain|
|Poder de Veto|Esse poder permite ao Multsig vetar qualquer decisão, preferencialmente não será algo necessário|
|Poder Transicional|Um poder temporário que permite o Multisig operar sob o mandato do YIP-41 até o conjunto de poderes com tomada de decisão cubram todas as transações necessárias|


## Implementações Futuras

A Yearn continua pavimentando o caminho em direção de um balanço ideal entre produtividade e descentralização da DAO. A fase atual de empenhos implementam mudanças, em geral, na camada social, e no futuro estaremos migrando para uma implementação em software, tais como:

- Mecanismo de consenso Multisig que permite cada yTeam obter poder de execução
- Migrar a votação por meio de proxy para votação na blockchain
- tokenizar poderes de tomada de decisão como NFTs
- Utilizar o [Coordinape](https://coordinape.com/) para alocação de fundos e compensação
