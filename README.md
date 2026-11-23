# Antonio Ramos Mendes · Engenheiro de automação com IA

Construo automações com n8n, Python e SQL. Cada projeto abaixo foi testado contra um conjunto fixo de casos, incluindo os caminhos de falha.

## Projetos

**[contas-a-pagar-ia](https://github.com/PerseoAgencyAutomations/contas-a-pagar-ia)**
Uma nota fiscal ou um boleto entra e vira um lançamento validado no Postgres. O código lê o XML da NF-e; a IA lê PDF e foto e devolve, para cada campo, o valor, a confiança e o trecho de onde o tirou. Campo duvidoso vai para uma pessoa conferir.
Teste com 40 documentos: decisão certa em 39, nenhum lançamento errado sem revisão humana e 4 de 4 duplicatas barradas.

**[prospeccao-local-ia](https://github.com/PerseoAgencyAutomations/prospeccao-local-ia)**
Você informa o nicho e a cidade e recebe os negócios que valem uma ligação, cada um com o trecho do site ou da avaliação que justifica a escolha. O código confere esse trecho na fonte e decide. O lead aprovado vira empresa e tarefa no HubSpot, e o custo de cada chamada de IA fica registrado no Postgres.
Teste com 40 negócios reais: 39 certos e nenhum lead sem evidência. Uma injeção de prompt plantada numa avaliação não teve efeito.

**[business-case-automacao](https://github.com/PerseoAgencyAutomations/business-case-automacao)**
A anotação da reunião de descoberta vira um business case de uma página, com horas liberadas, economia, preço e payback. A IA só encaixa as respostas no questionário; todas as contas são feitas em código.
Teste com 12 reuniões fictícias: resultado igual à referência em Python nas 12 e 3.248 de 3.248 casos certos na checagem de paridade.

**[n8n-nodes-jev-gate](https://github.com/PerseoAgencyAutomations/n8n-nodes-jev-gate)**
Nó da comunidade do n8n, publicado no npm, para o Jev, o modelo de decisão da TypeSafe. O Jev devolve uma probabilidade para cada opção; o nó segue só as respostas acima do limite de confiança e manda o restante para revisão. Também calibra esse limite com exemplos rotulados do próprio usuário.
Testes de setembro de 2026: agrupar 24 mensagens por chamada reduziu o custo por decisão à metade sem alterar as decisões confiantes e, com conteúdo que confundia o modelo, o limite de 0,95 segurou todos os erros.

Também:
- [doc-extract-gate](https://github.com/PerseoAgencyAutomations/doc-extract-gate): extração de nota fiscal em n8n que para e pergunta a uma pessoa o campo que a IA não leu com certeza.
- [ad-teardown-pipeline](https://github.com/PerseoAgencyAutomations/ad-teardown-pipeline): anúncios de concorrentes lidos por um modelo de visão e devolvidos com nota, em n8n.
- [btc-snapshot](https://github.com/PerseoAgencyAutomations/btc-snapshot): leitura diária do Bitcoin em Python puro, sem dependências.

## Vídeos

- [jev e n8n: uma probabilidade vira decisão](https://www.youtube.com/watch?v=0hxoySIlnyw) (vídeo em inglês)
- [O apresentador não é real: uma automação no n8n fez este vídeo](https://www.youtube.com/watch?v=VmfDzkwWi5k) (vídeo em inglês)

## Como trabalho

Antes de construir, desenho o processo e calculo quantas horas a automação vai economizar. Na construção, uso código quando a regra é fixa, IA quando o texto não tem formato e a aprovação de uma pessoa quando um erro sai caro.

## Stack

n8n · Python · SQL (PostgreSQL, Supabase) · JavaScript · TypeScript · Claude e Claude Code · OpenRouter · HubSpot · Playwright

## Formação

Bacharelado em Ciência de Dados na Univesp, em andamento (conclusão prevista para 2027). SP, Brasil, GMT-3.

[LinkedIn](https://www.linkedin.com/in/antonio-ramos-731934432/)
