# Visão Geral

## O que são yVaults?

[yVaults](https://yearn.finance/vaults) são como contas de poupança para seus cripto ativos. Elas aceitam o seu depósito, e o encaminham por estratégias que buscam os maiores rendimentos disponíveis em DeFi.

![](https://i.imgur.com/yXnJqsn.png)
*yVaults no site yearn.finance*

## Zapeando qualquer ativo

Graças à [Zapper](https://zapper.fi/), yVaults possuem depósitos bastante acessíveis. Contanto que você tenha qualquer token que possa ser trocado no Uniswap com menos de 1% de derrapagem, a vault vai aceitar o token, converter para o que é necessário para a vault, e depositar ele tudo em uma transação.

Quanto ao saque, usuários podem zapear de volta em um dos seguintes tokens:
- ETH, WETH, DAI, USDT, USDC, WBTC

## Estrutura de taxas da yVault

|Versão da yVault |Taxa de Saque|Taxa de Desempenho|Taxa de Administração|
|--------------|:-----------:|:-------------:|:------------:|
|v1|0.5%|5%|-|
|v2|-|20%|2%|

- Taxa de Saque: Taxa cobrada unicamente no saque
- Performance Fee: Percentual deduzido do rendimento
- Taxa de Administração: Percentual deduzido pelo balanço total anual.

## Melhorias das yVaults v2

- **Até 20 estratégias por vault:** Isso permite maior flexibilidade para gerenciar capital de forma mais eficiente durante diferentes cenários de mercado. Cada estratégia tem um teto capital. Isso é útil para impedir excesso de alocação de fundos em uma estratégia que não pode mais aumentar seu APY.
- **Guardiões e Estrategistas são os novos controladores:** O conceito de controlador não existe mais nas yVaults v2, e agora a função é dada aos guardiões e criadores de estratégias (estrategistas). Esses dois atores orientam a performance da estratégia e são encarregados de tomar ação para aprimorar o gerenciamento capital ou agir em situações críticas.
- **Automatização de tarefas domésticas das Vaults (Rede Keep3r):** As chamadas `harvest()` e `earn()` são automatizadas por meio da rede de bots Keep3r. Essas duas funções de chamada são usadas para compra de novos colaterais subjacentes vendendo os tokens farmados enquanto move os lucros de volta para a vault e mais tarde para estratégias. A rede keep3r se responsabiliza por executar essa tarefa exaustiva e lidar com os custos de gas em troca de tokens keep3r. Essa abordagem remove o trabalho humano dessas tarefas domésticas.
- **Lista de Seguranças e Convidados:** A Yearn criou um processo de desenvolvimento único para criação de novas vaults. Todas as vaults são lançadas como vaults de teste \(tyvToken\) no início. Vaults de testes tem um limite, assim como suas estratégias. Além disso, os Seguranças possuem uma lista de carteiras convidadas cujo são autorizadas a interagir com as Test Vaults em forma de depósito e retirada de fundos. Esse método previne usuários desinformados de potencialmente perderem fundos em um produto que não está em estágio de lançamento.
