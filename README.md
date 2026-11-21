# Antonio Ramos Mendes · Engenheiro de automação com IA

Construo automações com n8n, Python e SQL. Cada projeto abaixo vem com o teste contra um gabarito fixo e com o teste dos caminhos de falha.

## Projetos

**[contas-a-pagar-ia](https://github.com/PerseoAgencyAutomations/contas-a-pagar-ia)**
Nota fiscal ou boleto entra e vira lançamento validado no Postgres. O código lê o XML da NF-e. A IA lê PDF e foto e devolve, por campo, o valor, a confiança e o trecho de onde tirou. Campo duvidoso vai pra uma pessoa conferir.
Teste com 40 documentos: decisão certa em 39, nenhum lançamento errado sem revisão humana, 4 de 4 duplicatas barradas.

**[prospeccao-local-ia](https://github.com/PerseoAgencyAutomations/prospeccao-local-ia)**
Você digita nicho e cidade e recebe os negócios que valem uma ligação, cada um com o trecho do site ou da avaliação que justifica. O código confere o trecho na fonte e decide. O lead que você aprova vira empresa e tarefa no HubSpot, e o custo de cada chamada de IA fica gravado no Postgres.
Teste com 40 negócios reais: 39 certos, nenhum lead sem evidência. Uma injeção de prompt plantada numa avaliação não teve efeito.

**[business-case-automacao](https://github.com/PerseoAgencyAutomations/business-case-automacao)**
A anotação da call de descoberta vira um business case de uma página: horas liberadas, economia, preço e payback. A IA só encaixa as respostas no questionário. Toda conta roda em código.
Teste com 12 calls fictícias: conta igual à referência em Python nas 12, e 3.248 de 3.248 na checagem de paridade.

Também: [Perseo-Web](https://github.com/Eternorms/Perseo-Web), meu site em Next.js, no ar em [perseo-web.vercel.app](https://perseo-web.vercel.app).

## Como trabalho

- Antes de construir, mapeio o processo e estimo as horas liberadas pelo método PAT da UiPath. No business case, a conta deu "não vale automatizar" pra anotação livre, então mudei a entrada antes de construir.
- Código onde a regra é fixa, IA onde o texto não tem formato, aprovação humana onde o erro sai caro.

## Stack

n8n · Python · SQL (PostgreSQL, Supabase) · JavaScript · Claude e Claude Code · OpenRouter · HubSpot · Playwright

## Formação

Bacharelado em Ciência de Dados, Univesp, em andamento (conclusão prevista em 2027). SP, Brasil, GMT-3.

[LinkedIn](https://www.linkedin.com/in/antonio-ramos-731934432/)

*In English:* AI automation engineer (n8n, Python, SQL, Claude). Each repo ships with a fixed test set and failure-path tests, and each README ends with a short English summary.
