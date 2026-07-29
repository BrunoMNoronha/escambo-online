# Base de conhecimento do Projeto ChatGPT

**Projeto:** Escambo Online

**Status:** procedimento operacional para sincronizar a base de conhecimento do Projeto ChatGPT com o repositório oficial

**Última atualização:** 29/07/2026 (etapa `EO-REPO-003`)

## 1. Objetivo

Este documento define como manter a base de conhecimento do Projeto ChatGPT alinhada ao repositório `BrunoMNoronha/escambo-online`, evitando que versões antigas, cópias atualizadas e regras divergentes coexistam no contexto do orquestrador.

Substituir a base de conhecimento **não** autoriza pesquisa de campo, contato com participantes, implementação, schema, infraestrutura, deploy ou operação Git adicional. É apenas higiene de contexto (`DOC-004`).

## 2. Fonte da verdade

A ordem de precedência é a mesma do [`README.md`](../../README.md) e do [`01_INSTRUCOES_PROJETO_CHATGPT.md`](01_INSTRUCOES_PROJETO_CHATGPT.md):

1. decisão explícita e mais recente de Bruno;
2. [registro de decisões](REGISTRO_DECISOES.md);
3. [fonte-mestra do produto](../produto/02_FONTE_MESTRA_PRODUTO.md);
4. escopo e regras de negócio;
5. documentos técnicos e de qualidade (incluindo ADRs formalizados);
6. roadmap, prompts e relatórios;
7. implementação existente.

A base de conhecimento do Projeto ChatGPT é um **espelho** dessas fontes, nunca uma fonte concorrente. Em qualquer divergência, prevalece o repositório.

## 3. Procedimento de substituição

1. Aguardar o merge da revisão documental relevante na `main`.
2. No Projeto ChatGPT, remover todos os arquivos atualmente anexados à base de conhecimento.
3. Substituir integralmente o texto de **Instruções do projeto** pelo conteúdo completo de `01_INSTRUCOES_PROJETO_CHATGPT.md` (versão mergeada na `main`).
4. Anexar somente os arquivos canônicos listados na seção 4, obtidos da `main` já mergeada.
5. Não anexar `01_INSTRUCOES_PROJETO_CHATGPT.md` como arquivo: seu conteúdo já estará no campo de instruções.
6. Não manter cópias com sufixos como "original", "novo", "atualizado" ou "cópia".
7. Executar a verificação da seção 5 antes de usar a base.

Remover arquivos antigos do Projeto ChatGPT não apaga histórico: versões anteriores permanecem recuperáveis no Git.

## 4. Arquivos canônicos a anexar

Obtidos sempre da `main`. `README.md`, `AGENTS.md`, `docs/README.md` e este manifesto permanecem no repositório como navegação/procedimento e **não** precisam ser anexados.

### Produto

1. [`02_FONTE_MESTRA_PRODUTO.md`](../produto/02_FONTE_MESTRA_PRODUTO.md)
2. [`03_ESCOPO_MVP_REGRAS_NEGOCIO.md`](../produto/03_ESCOPO_MVP_REGRAS_NEGOCIO.md)
3. [`04_JORNADAS_HISTORIAS_CRITERIOS.md`](../produto/04_JORNADAS_HISTORIAS_CRITERIOS.md)
4. [`08_ROADMAP_BACKLOG.md`](../produto/08_ROADMAP_BACKLOG.md)

### Descoberta

5. [`RELATORIO_AUDITORIA_PRODUTO_V1.md`](../descoberta/RELATORIO_AUDITORIA_PRODUTO_V1.md)
6. [`PLANO_DESCOBERTA_V1.md`](../descoberta/PLANO_DESCOBERTA_V1.md)
7. [`ROTEIRO_ENTREVISTAS_V1.md`](../descoberta/ROTEIRO_ENTREVISTAS_V1.md)
8. [`MATRIZ_HIPOTESES_V1.md`](../descoberta/MATRIZ_HIPOTESES_V1.md)
9. [`DECISOES_PARA_BRUNO_V1.md`](../descoberta/DECISOES_PARA_BRUNO_V1.md)

### Arquitetura e qualidade

10. [`05_MODELO_DOMINIO_DADOS.md`](../arquitetura/05_MODELO_DOMINIO_DADOS.md)
11. [`06_ARQUITETURA_TECNICA_INICIAL.md`](../arquitetura/06_ARQUITETURA_TECNICA_INICIAL.md)
12. [`07_QUALIDADE_SEGURANCA_PRIVACIDADE.md`](../qualidade/07_QUALIDADE_SEGURANCA_PRIVACIDADE.md)

### Governança

13. [`09_GOVERNANCA_IA_GITHUB.md`](09_GOVERNANCA_IA_GITHUB.md)
14. [`10_TEMPLATES_PROMPTS_RELATORIOS.md`](10_TEMPLATES_PROMPTS_RELATORIOS.md)
15. [`11_ESTADO_ATUAL_PROJETO.md`](11_ESTADO_ATUAL_PROJETO.md)
16. [`REGISTRO_DECISOES.md`](REGISTRO_DECISOES.md)

São **16 arquivos**. Este manifesto (`12`) não é anexado.

## 5. Verificação após a substituição

Confirmar no Projeto ChatGPT, sempre contra o estado atual da `main`:

- existem exatamente 16 arquivos de conhecimento, sem duplicados nem versões antigas;
- a instrução menciona **troca exclusivamente de bens, sem complemento financeiro** (`DISC-001`);
- as regiões candidatas são **Cruzeiro/DF** e **Guará/DF**, com **Região Administrativa** como unidade pública (`DISC-002`) — já escolhidas, não pendentes;
- o público e os três grupos de categorias candidatas constam como recorte de descoberta (`DISC-003`), não como taxonomia final;
- `MATRIZ_HIPOTESES_V1.md` informa critérios **aprovados e congelados** (`DISC-004`) e hipóteses **não validadas**;
- `H-01` a `H-07` continuam não validadas; decisões 5–10 continuam pendentes;
- o registro contém as decisões operacionais `GOV-007`, `GOV-008`, `INFRA-001` e `DOC-004`;
- a Vercel consta como hospedagem preferencial sob custo zero, **sem configuração nem deploy** (`INFRA-001`);
- `11_ESTADO_ATUAL_PROJETO.md` aponta como próximo gate a **preparação das regras de coleta responsável**, não a escolha de regiões;
- nenhuma fonte declara autorização para implementação ou contato externo.

Se qualquer verificação falhar, não iniciar a próxima etapa: corrigir a base e repetir a checagem.

## 6. Primeiro uso recomendado

Após a substituição, iniciar uma nova conversa no Projeto ChatGPT com:

> Leia integralmente a base de conhecimento vigente. Resuma somente as decisões confirmadas, as hipóteses ainda não validadas e os bloqueios atuais. Em seguida, apresente a Bruno o próximo gate — a preparação das regras de coleta responsável (recrutamento, consentimento, registro, anonimização, armazenamento, acesso e retenção) — explicando o que precisa ser aprovado e o impacto de adiar. Não pesquise pessoas, não contate participantes e não implemente nada.

O resultado esperado é uma verificação de consistência e a preparação da próxima decisão, não execução de campo.

## 7. Controle de versão

- A fonte oficial dos arquivos é o repositório `BrunoMNoronha/escambo-online`.
- Alterações futuras ocorrem no Git, são revisadas e só então substituem os arquivos correspondentes no Projeto ChatGPT.
- O campo de instruções é atualizado sempre que `01_INSTRUCOES_PROJETO_CHATGPT.md` mudar.
- A troca de arquivo na base preserva o mesmo nome canônico.
- Decisão nova exige atualização mínima de `REGISTRO_DECISOES.md` e `11_ESTADO_ATUAL_PROJETO.md`, além das fontes afetadas (`DOC-004`).

## 8. Limitação operacional

Este repositório prepara e versiona o pacote, mas não altera automaticamente os anexos ou as instruções do Projeto ChatGPT. A remoção dos originais e a inclusão dos 16 arquivos atualizados são executadas no próprio Projeto ChatGPT, manualmente, depois do merge.
