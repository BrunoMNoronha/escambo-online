# Base de conhecimento do Projeto ChatGPT

**Projeto:** Escambo Online

**Status:** manifesto operacional da base estável do Projeto ChatGPT

**Última atualização:** 29/07/2026 (etapa `EO-DOC-007`; decisão `DOC-007`)

## 1. Objetivo

Este documento define a composição **estável** da base de conhecimento do Projeto ChatGPT sob a decisão [`DOC-007`](REGISTRO_DECISOES.md). A base deixa de espelhar os documentos evolutivos do repositório: passa a conter apenas um campo de instruções estável e dois anexos estáveis, e obriga a consulta do estado atual diretamente na `main` do GitHub.

Substituir a base **não** autoriza pesquisa de campo, contato com participantes, implementação, schema, infraestrutura, deploy ou operação Git adicional. É apenas higiene de contexto (`DOC-004`).

## 2. Fonte da verdade

O GitHub (`BrunoMNoronha/escambo-online`, branch `main`) é a fonte versionada oficial e concentra estado atual, decisões, produto e escopo, descoberta e hipóteses, arquitetura, qualidade/segurança/privacidade, roadmap, prompts, relatórios e evidências.

A ordem de precedência é a do [`README.md`](../../README.md) e da [Constituição operacional](13_CONSTITUICAO_OPERACIONAL_CHATGPT.md):

1. decisão explícita e mais recente de Bruno;
2. [registro de decisões](REGISTRO_DECISOES.md);
3. [fonte-mestra do produto](../produto/02_FONTE_MESTRA_PRODUTO.md);
4. escopo e regras de negócio;
5. documentos técnicos e de qualidade (incluindo ADRs formalizados);
6. roadmap, prompts e relatórios;
7. implementação existente.

A base de conhecimento do Projeto ChatGPT é um apoio estável de método, nunca uma fonte concorrente de estado. Em qualquer divergência, prevalece o repositório.

## 3. Composição da base estável

Sob `DOC-007`, a base do Projeto ChatGPT tem exatamente três elementos:

### Campo de instruções

- Conteúdo integral de [`01_INSTRUCOES_PROJETO_CHATGPT.md`](01_INSTRUCOES_PROJETO_CHATGPT.md), na versão vigente da `main`.
- É **estável**: não contém snapshot de estado, backlog, decisões específicas nem próximo gate. Direciona as consultas de estado ao GitHub.
- `01_INSTRUCOES_PROJETO_CHATGPT.md` **não** é anexado como arquivo: seu conteúdo já está no campo de instruções.

### Dois anexos estáveis

1. [`13_CONSTITUICAO_OPERACIONAL_CHATGPT.md`](13_CONSTITUICAO_OPERACIONAL_CHATGPT.md) — papéis, hierarquia de verdade, ciclo de trabalho, limites de autonomia, gates de autorização e critérios de auditoria;
2. [`14_MAPA_FONTES_CANONICAS_GITHUB.md`](14_MAPA_FONTES_CANONICAS_GITHUB.md) — índice das fontes canônicas e protocolo obrigatório de consulta à `main`, incluindo o comportamento quando o GitHub estiver indisponível.

São **exatamente dois anexos**. Ambos são estáveis: não contêm snapshot de estado, próximo gate, SHA, PR, hipótese específica nem decisão temporária.

### Demais documentos

Todos os demais documentos do projeto (produto, descoberta, arquitetura, qualidade, governança restante, roadmap, prompts, relatórios e evidências) permanecem **somente no GitHub** e são consultados na `main` pelo protocolo do documento `14`. Não são anexados ao Projeto ChatGPT.

> **Nota histórica — `DOC-005` e `DOC-006` (política anterior superada).** Até `EO-DOC-006`, este manifesto exigia **18 anexos** que espelhavam os documentos evolutivos da `main` (incluindo `README.md` e `AGENTS.md`). Essa política foi definida por `DOC-005` (sincronização canônica) e ajustada por `DOC-006` (troca do item 7 para `PROTOCOLO_COLETA_RESPONSAVEL_V1.md`). A partir de `DOC-007` (29/07/2026), a lista operacional de 18 anexos **deixa de valer** e é substituída pelos dois anexos estáveis acima. `DOC-005` e `DOC-006` **não são apagadas**: permanecem registradas em [`REGISTRO_DECISOES.md`](REGISTRO_DECISOES.md) como histórico da política anterior, agora superada operacionalmente por `DOC-007`.

## 4. Procedimento de substituição manual

Executado **manualmente no Projeto ChatGPT**, após o merge desta atualização documental na `main` e mediante autorização específica de Bruno:

1. Aguardar o merge da revisão documental relevante na `main`.
2. No Projeto ChatGPT, remover todos os arquivos atualmente anexados à base de conhecimento (inclusive os 18 anexos da política anterior).
3. Substituir integralmente o texto de **Instruções do projeto** pelo conteúdo completo de `01_INSTRUCOES_PROJETO_CHATGPT.md` (versão mergeada na `main`).
4. Anexar somente os **dois** arquivos estáveis, obtidos da `main` já mergeada:
   1. `13_CONSTITUICAO_OPERACIONAL_CHATGPT.md`;
   2. `14_MAPA_FONTES_CANONICAS_GITHUB.md`.
5. Não anexar `01_INSTRUCOES_PROJETO_CHATGPT.md` como arquivo: seu conteúdo já está no campo de instruções.
6. Não anexar nenhum documento evolutivo: eles permanecem apenas no GitHub.
7. Não manter cópias com sufixos como "original", "novo", "atualizado" ou "cópia".
8. Executar o checklist da seção 5 antes de usar a base.

Remover arquivos antigos do Projeto ChatGPT não apaga histórico: versões anteriores permanecem recuperáveis no Git, e os documentos evolutivos continuam íntegros no repositório.

## 5. Checklist pós-substituição

Confirmar no Projeto ChatGPT, sempre contra o estado atual da `main`:

- o campo de instruções corresponde ao conteúdo vigente de `01_INSTRUCOES_PROJETO_CHATGPT.md`;
- existem **exatamente dois** anexos, sem duplicados nem versões antigas;
- os anexos são `13_CONSTITUICAO_OPERACIONAL_CHATGPT.md` e `14_MAPA_FONTES_CANONICAS_GITHUB.md`;
- **nenhum** documento evolutivo permanece anexado (produto, descoberta, arquitetura, qualidade, roadmap, prompts, relatórios ou o antigo conjunto de 18 anexos);
- `README.md` e `AGENTS.md` **não** estão mais anexados — passam a ser consultados na `main`, conforme o mapa de fontes;
- o campo de instruções direciona as consultas de estado ao GitHub e referencia os documentos `13` e `14`;
- os dois anexos não contêm snapshot de estado, próximo gate, SHA, PR, hipótese específica nem decisão temporária;
- o mapa (`14`) descreve o protocolo de leitura obrigatória da `main` e o comportamento quando o GitHub estiver indisponível.

Se qualquer verificação falhar, não iniciar a próxima etapa: corrigir a base e repetir a checagem.

## 6. Teste de primeira utilização

Após a substituição, iniciar uma nova conversa no Projeto ChatGPT com:

> Leia o campo de instruções e os dois anexos estáveis (Constituição operacional e Mapa de fontes canônicas do GitHub). Sem presumir o estado do projeto, descreva o protocolo obrigatório de consulta à `main` do repositório `BrunoMNoronha/escambo-online` e liste os documentos mínimos obrigatórios que você leria primeiro. Em seguida, explique o que faria se o GitHub estivesse indisponível. Não afirme decisões, autorizações, fase, hipóteses ou próximo gate sem antes consultar as fontes vigentes da `main`. Não pesquise pessoas, não contate participantes e não implemente nada.

O resultado esperado é a demonstração do método e do protocolo de recuperação, não a execução de campo nem a afirmação de estado a partir de memória.

## 7. Controle de versão

- A fonte oficial dos arquivos é o repositório `BrunoMNoronha/escambo-online`.
- Alterações futuras ocorrem no Git, são revisadas e só então substituem o campo de instruções ou os dois anexos correspondentes no Projeto ChatGPT.
- O campo de instruções é atualizado sempre que `01_INSTRUCOES_PROJETO_CHATGPT.md` mudar; cada anexo é atualizado sempre que `13` ou `14` mudarem.
- A troca de arquivo na base preserva o mesmo nome canônico.
- Decisão nova exige atualização mínima de `REGISTRO_DECISOES.md` e `11_ESTADO_ATUAL_PROJETO.md`, além das fontes afetadas (`DOC-004`).

## 8. Limitação operacional

Este repositório prepara e versiona a definição da base, mas **não altera automaticamente** os anexos ou as instruções do Projeto ChatGPT. A remoção dos originais, a substituição do campo de instruções e a inclusão dos dois anexos estáveis são executadas no próprio Projeto ChatGPT, **manualmente**, depois do merge.

A decisão `DOC-007` (29/07/2026) redefine a base para dois anexos estáveis, mas **a substituição manual dos anexos permanece pendente e ainda não autorizada** — depende de nova autorização explícita de Bruno, após o merge desta atualização documental. Atualizar esta documentação **não executa** a troca de anexos.
