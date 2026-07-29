# Estado atual do projeto

**Atualizado em:** 29/07/2026

**Fase:** 0 — descoberta e validação

**Status geral:** decisões iniciais e operacionais registradas; D0 parcialmente concluída; preparação da coleta pendente; produto ainda não validado

## 1. Resumo

O repositório oficial foi definido e a base inicial foi auditada na etapa `EO-DISC-001`.

A auditoria concluiu que a proposta é coerente para iniciar descoberta, mas não está pronta para fechar MVP ou iniciar implementação. Nenhuma hipótese `H-01` a `H-07` possui evidência externa suficiente.

Na etapa `EO-DISC-002`, Bruno aprovou em 29/07/2026 as quatro decisões iniciais de produto (`DISC-001` a `DISC-004`), a matriz de hipóteses foi congelada e a pendência documental `DOC-001` a `DOC-003` foi sanada — as decisões foram movidas para confirmadas em razão do merge do PR #1. As hipóteses `H-01` a `H-07` seguem não validadas.

O próximo gate é preparar, para aprovação de Bruno, os instrumentos e as regras de coleta responsável — critérios de recrutamento, consentimento, registro e eventual gravação, anonimização, local de armazenamento, controle de acesso e prazo de retenção e descarte — e obter autorização específica antes de qualquer contato com participantes.

## 2. Decisões confirmadas

| ID | Decisão | Origem |
| --- | --- | --- |
| GOV-001 | ChatGPT organizará, documentará e orquestrará o desenvolvimento | Bruno |
| GOV-002 | Claude Code e Antigravity serão ferramentas/agentes de desenvolvimento | Bruno |
| GOV-003 | GitHub será usado para versionamento | Bruno |
| GOV-004 | Bruno mantém aprovação final de decisões e ações sensíveis | Governança adotada |
| GOV-005 | Commit, push, PR, migration e mudança sensível exigem autorização explícita | Governança adotada |
| GOV-006 | `BrunoMNoronha/escambo-online` é o repositório oficial | Bruno |
| DISC-001 | Descoberta testa exclusivamente troca de bens sem complemento financeiro | Bruno (29/07/2026) |
| DISC-002 | Regiões candidatas Cruzeiro/DF e Guará/DF; unidade pública = Região Administrativa | Bruno (29/07/2026) |
| DISC-003 | Público, três categorias candidatas e exclusões como recorte de descoberta | Bruno (29/07/2026) |
| DISC-004 | Critérios da matriz aprovados e congelados; hipóteses seguem não validadas | Bruno (29/07/2026) |
| DOC-001 | Organizar documentos por área (`produto`, `descoberta`, `arquitetura`, `qualidade`, `governanca`) | Merge do PR #1 (29/07/2026) |
| DOC-002 | Manter `README.md` e `AGENTS.md` na raiz | Merge do PR #1 (29/07/2026) |
| DOC-003 | Usar o registro de decisões como fonte primária das decisões confirmadas | Merge do PR #1 (29/07/2026) |
| GOV-007 | GitHub Actions e scripts Python autorizados quando diretamente úteis a uma etapa, gratuitos, determinísticos, documentados e seguros; sem conceder deploy, push, PR, migration ou mudança sensível | Bruno (29/07/2026) |
| GOV-008 | Ferramentas gratuitas ou já incluídas de Claude/Anthropic, OpenAI e GitHub autorizadas com custo incremental zero e menor privilégio | Bruno (29/07/2026) |
| INFRA-001 | Vercel como hospedagem preferencial sob custo zero; sem deploy nesta etapa; detalhamento no `ADR-008` | Bruno (29/07/2026) |
| DOC-004 | Higiene contínua e controlada do repositório; remoção somente com evidência registrada | Bruno (29/07/2026) |
| DOC-005 | Sincronização canônica da base do Projeto ChatGPT (procedimento manual, espelhando a `main`); complementa `DOC-004` | Bruno (29/07/2026) |

A fonte primária dessas decisões é o [registro de decisões](REGISTRO_DECISOES.md).

## 3. Propostas ainda não homologadas

| ID | Proposta |
| --- | --- |
| PROD-001 | MVP de troca de bens sem pagamento ou complemento financeiro |
| PROD-002 | Operação inicial regional e encontro presencial |
| PROD-003 | Um ou mais anúncios por lado da proposta |
| PROD-004 | Chat vinculado à negociação |
| PROD-005 | Reputação após conclusão |
| PROD-006 | Moderação administrativa mínima |
| TECH-001 | Aplicação web responsiva |
| TECH-002 | Monólito modular em monorepo TypeScript |
| TECH-003 | Next.js + NestJS + PostgreSQL + Prisma |
| TECH-004 | Storage compatível com S3 para imagens |
| TECH-005 | Docker Compose local e GitHub Actions |

Nenhuma proposta desta seção autoriza implementação.

## 4. Hipóteses críticas

| Hipótese | Estado | Efeito se falsa |
| --- | --- | --- |
| H-01 — demanda recorrente por troca sem dinheiro | Não validada | inviabiliza a tese |
| H-02 — liquidez regional suficiente | Não validada | inviabiliza marketplace aberto |
| H-03 — disposição para cadastrar item próprio | Não validada | altera o mecanismo de proposta |
| H-04 — chat e reputação aumentam confiança | Não validada | altera o pacote de confiança |
| H-05 — encontro presencial é suficiente | Não validada | bloqueia operação sem logística |
| H-06 — vários itens são compreensíveis | Não validada | recomenda simplificação |
| H-07 — moderação manual suporta o piloto | Não validada | bloqueia piloto seguro |

`H-01`, `H-02`, `H-05` e `H-07` são gates de viabilidade. Os critérios de decisão da [matriz de hipóteses](../descoberta/MATRIZ_HIPOTESES_V1.md) foram aprovados e **congelados em 29/07/2026** (`DISC-004`); nenhuma hipótese foi validada, mantida, alterada ou rejeitada.

## 5. Decisões pendentes priorizadas

| Prioridade | Decisão | Quando | Status |
| ---: | --- | --- | --- |
| 1 | Fronteira da tese e complemento financeiro | antes da pesquisa | Respondida 29/07/2026 (`DISC-001`) |
| 2 | Regiões candidatas e unidade de liquidez | antes da pesquisa | Respondida 29/07/2026 (`DISC-002`) |
| 3 | Público, categorias e itens excluídos | antes da pesquisa | Respondida 29/07/2026 (`DISC-003`) |
| 4 | Critérios para manter, alterar ou rejeitar hipóteses | antes da pesquisa | Respondida 29/07/2026 (`DISC-004`) |
| 5 | Composição 1:1, 1:N ou N:N | antes do protótipo | Pendente |
| 6 | Presencial, raio e compartilhamento progressivo | pesquisa e antes do piloto | Pendente |
| 7 | Momento do chat e controles de abuso | antes do protótipo/piloto | Pendente |
| 8 | Expiração, cancelamento e concorrência | antes do modelo de estados | Pendente |
| 9 | Conclusão, problema, disputa e reputação | antes do piloto | Pendente |
| 10 | Elegibilidade, moderação e gates do piloto | antes de usuários reais | Pendente |

Detalhes: [Decisões para Bruno V1](../descoberta/DECISOES_PARA_BRUNO_V1.md).

## 6. Artefatos concluídos

### Base inicial

- instruções do Projeto ChatGPT;
- fonte-mestra v0.1;
- escopo e regras propostas;
- jornadas, histórias e critérios;
- modelo conceitual;
- arquitetura proposta;
- requisitos de qualidade, segurança e privacidade;
- roadmap;
- governança de agentes e GitHub;
- templates de prompt, relatório e auditoria.

### EO-DISC-001

- [Relatório de auditoria V1](../descoberta/RELATORIO_AUDITORIA_PRODUTO_V1.md);
- [Plano de descoberta V1](../descoberta/PLANO_DESCOBERTA_V1.md);
- [Roteiro de entrevistas V1](../descoberta/ROTEIRO_ENTREVISTAS_V1.md);
- [Matriz de hipóteses V1](../descoberta/MATRIZ_HIPOTESES_V1.md);
- [Decisões para Bruno V1](../descoberta/DECISOES_PARA_BRUNO_V1.md).

### EO-DISC-002

- decisões `DISC-001` a `DISC-004` registradas em [Registro de decisões](REGISTRO_DECISOES.md);
- pendência documental `DOC-001` a `DOC-003` sanada (movidas para decisões confirmadas em razão do merge do PR #1);
- matriz de hipóteses aprovada e congelada;
- fonte-mestra, escopo, plano de descoberta e índices atualizados com o recorte de descoberta;
- decisões 1–4 marcadas como respondidas; 5–10 mantidas pendentes.

### EO-GOV-001

- decisões operacionais `GOV-007`, `GOV-008`, `INFRA-001` e `DOC-004` registradas em [Registro de decisões](REGISTRO_DECISOES.md);
- governança (`09`), templates (`10`), instruções dos agentes (`AGENTS.md`), arquitetura (`06`) e roadmap (`08`) sincronizados com os novos limites;
- etapa exclusivamente de consolidação documental; nenhuma Action, script persistente, aplicação ou configuração Vercel criada; nenhum deploy;
- **PR #2** (`agent/registrar-decisoes-iniciais`, draft, conflitante) analisada em modo somente leitura e registrada como pendência operacional candidata a encerramento — **não** encerrada nesta etapa.

### EO-REPO-003

- auditoria somente leitura da PR #2 concluída; modelagem de decisões classificada como superada/divergente da `main`;
- conteúdo residual útil identificado e preservado: procedimento de sincronização da base de conhecimento e correção de hierarquia do `01`;
- `12_BASE_CONHECIMENTO_CHATGPT.md` reautorado contra o estado canônico atual; hierarquia de verdade do `01_INSTRUCOES` alinhada ao `README.md`; índice atualizado;
- decisão `DOC-005` registrada em [Registro de decisões](REGISTRO_DECISOES.md);
- **PR #5** publicada com essas três alterações e **aguardando merge**; **não mesclada** nesta etapa;
- **PR #2** permanece aberta, aguardando **encerramento posterior** (após o merge da PR #5), com o conteúdo residual útil já preservado;
- **pendência operacional:** a sincronização manual dos anexos e das instruções do Projeto ChatGPT (`DOC-005`) **ainda não foi executada** — documentar o procedimento não é executá-lo.

### EO-REPO-004 — situação consolidada

Estado autoritativo após o encerramento das PRs (supera as menções "aguardando merge/encerramento" das etapas anteriores):

- **PR #5** (`docs/eo-repo-003`) **integrada** à `main` em `main@b4411eb28143a46669e494e80195d294daa5b439` (merge commit da PR #5); branch remota **preservada**;
- **PR #2** (`agent/registrar-decisoes-iniciais`) **encerrada como superada, sem merge**; branch remota **preservada** para rastreabilidade histórica;
- o conteúdo residual útil da PR #2 (procedimento canônico da base de conhecimento e alinhamento da hierarquia documental) permanece **preservado pela PR #5**;
- **pendência operacional:** a sincronização manual da base de conhecimento do Projeto ChatGPT (`DOC-005`) foi **executada em 29/07/2026** (ver bloco `EO-REPO-005`);
- produto e `H-01` a `H-07` seguem **não validados**; decisões 5–10 seguem **pendentes**; próximo gate de produto permanece a **preparação da coleta responsável** (inalterado).

### EO-REPO-005 — sincronização DOC-005 executada

- **`DOC-005` executada em 29/07/2026** por Bruno, manualmente, no Projeto ChatGPT;
- origem do pacote: `main@7a7d49f5474f2ff57a27f3cf479cbb0a6df19c65`;
- campo de instruções substituído pela versão de `01_INSTRUCOES_PROJETO_CHATGPT.md` desse commit;
- base com **exatamente 18 anexos**, incluindo `README.md` e `AGENTS.md`, sem duplicados nem renomeados;
- `01_INSTRUCOES_PROJETO_CHATGPT.md` (campo de instruções), `docs/README.md` e `12_BASE_CONHECIMENTO_CHATGPT.md` **não** anexados;
- checklist pós-substituição concluído sem divergências; **pendência operacional de `DOC-005` encerrada**;
- registro aceito com ressalva de evidência: a composição dos anexos foi comprovada; a substituição do campo de instruções é aceita pelo registro operacional de Bruno, sem comparação independente neste contexto entre o campo e o blob do commit;
- o repositório permanece a **fonte prevalente**; nenhuma decisão de produto, segurança ou implementação foi alterada.

## 7. Não iniciado

- recrutamento ou entrevistas;
- validação de mercado;
- análise jurídica;
- protótipo;
- landing page;
- coleta de dados;
- nome e marca definitivos;
- ADRs homologados;
- scaffold ou implementação;
- schema ou migration;
- CI/CD e infraestrutura;
- GitHub Actions ou scripts Python persistentes (autorizados por `GOV-007`, mas não criados);
- configuração de conta, projeto ou integração Vercel (`INFRA-001` registra a direção, sem ativação);
- deploy de preview, staging ou produção.

## 8. Riscos abertos

- demanda insuficiente;
- ausência de liquidez regional;
- fraude e itens proibidos;
- insegurança em encontro presencial;
- assédio e exposição no chat;
- complexidade de trocas com vários itens;
- capacidade de moderação;
- retenção e tratamento de dados;
- coleta iniciada antes de consentimento, anonimização e retenção aprovados (mitigado pelo gate atual);
- viés retrospectivo caso os critérios congelados sejam alterados após ver resultados;
- crescimento de escopo antes da validação;
- custo não previsto ou conversão automática ao usar plataformas gratuitas (mitigado por `GOV-008` e `INFRA-001`, custo incremental zero exigido);
- lock-in de fornecedor de hospedagem (mitigado pelos critérios de portabilidade de `INFRA-001`);
- ampliação indevida de permissões, tokens ou integrações (mitigado pela exigência de menor privilégio e interrupção);
- vazamento de segredos ou dados pessoais em prompts, logs, artefatos ou Actions (proibido por `GOV-007`/`GOV-008`);
- acúmulo ou obsolescência documental sem higiene controlada (mitigado por `DOC-004`).

## 9. Próximo passo recomendado

As decisões 1–4 foram respondidas e registradas. O próximo gate é preparar e submeter à aprovação de Bruno:

1. critérios de recrutamento;
2. consentimento e forma de registro (e eventual gravação);
3. anonimização, local de armazenamento, controle de acesso, prazo de retenção e descarte;
4. revisão e aprovação do roteiro aplicável;
5. autorização explícita antes de contatar participantes.

As decisões 5–10 continuam pendentes nos momentos definidos, mas **não** são o próximo gate imediato. Nada de recrutamento, entrevista, contato ou implementação está autorizado nesta etapa.

## 10. Histórico

### 29/07/2026 — Base inicial

- documentação original criada;
- produto mantido como hipótese;
- nenhuma implementação autorizada.

### 29/07/2026 — EO-DISC-001

- auditoria documental concluída;
- inconsistências e lacunas registradas;
- H-01 a H-07 avaliadas como não validadas;
- plano, roteiro, matriz e decisões prioritárias produzidos;
- repositório oficial confirmado por Bruno;
- nenhuma decisão de produto foi presumida.

### 29/07/2026 — EO-DISC-002

- baseline `EO-REPO-001` aceita com ressalvas antes desta etapa;
- decisões 1–4 aprovadas por Bruno e registradas como `DISC-001` a `DISC-004`;
- pendência documental `DOC-001` a `DOC-003` movida para decisões confirmadas (em vigor com o merge do PR #1);
- matriz de hipóteses aprovada e congelada; `H-01` a `H-07` mantidas não validadas;
- fonte-mestra, escopo, plano de descoberta, índices e este estado atualizados;
- roteiro de entrevistas lido e verificado, sem alteração (permanece proposta, não aprovado);
- nenhuma pesquisa, recrutamento, contato ou implementação autorizado;
- etapa exclusivamente documental, sem commit, push ou PR.

### 29/07/2026 — EO-GOV-001

- consolidação documental das decisões operacionais recentes de Bruno;
- `GOV-007`, `GOV-008`, `INFRA-001` e `DOC-004` registrados como decisões confirmadas;
- governança, templates, `AGENTS.md`, arquitetura e roadmap sincronizados sem ampliar autorizações;
- Vercel registrada como direção de hospedagem preferencial sob custo zero, sem configuração nem deploy;
- auditoria de obsolescência e links executada em modo somente leitura; nenhuma remoção necessária;
- produto mantido não validado; `H-01` a `H-07` mantidas não validadas; próximo gate de descoberta inalterado;
- PR #2 classificada como candidata a encerramento, sem alteração remota;
- etapa exclusivamente documental, sem commit, push, PR, merge ou deploy.

### 29/07/2026 — EO-REPO-003

- auditoria somente leitura da PR #2 concluída; modelagem de decisões classificada como superada/divergente (a `main` já traz `DISC-001..004` com Cruzeiro/Guará escolhidos);
- conteúdo residual útil identificado; `12_BASE_CONHECIMENTO_CHATGPT.md` reautorado contra a `main` atual;
- hierarquia de verdade do `01_INSTRUCOES` alinhada ao `README.md`; índice atualizado;
- decisão `DOC-005` registrada (procedimento de sincronização manual da base de conhecimento);
- PR #5 publicada e **aguardando merge**; PR #2 ainda aberta e **aguardando encerramento** posterior;
- sincronização manual da base de conhecimento permanece **pendente** (não executada);
- produto mantido não validado; `H-01` a `H-07` mantidas não validadas; decisões 5–10 pendentes; próximo gate de descoberta inalterado;
- correção de rastreabilidade `EO-REPO-003-COR-01` sem commit, push, PR, merge ou deploy.

### 29/07/2026 — EO-REPO-004

- consolidação documental do estado após o encerramento das PRs;
- **PR #5 integrada** à `main` (`main@b4411eb`); branch `docs/eo-repo-003` preservada;
- **PR #2 encerrada como superada, sem merge**; branch `agent/registrar-decisoes-iniciais` preservada; comentário de encerramento publicado antes do fechamento;
- conteúdo residual útil da PR #2 preservado pela PR #5;
- sincronização manual da base de conhecimento (`DOC-005`) permanece **pendente**;
- produto e `H-01` a `H-07` mantidos não validados; decisões 5–10 pendentes; próximo gate de descoberta inalterado;
- etapa exclusivamente documental (`11_ESTADO_ATUAL_PROJETO.md`); sem nova decisão (`REGISTRO_DECISOES.md` inalterado); sem merge nesta etapa.

### 29/07/2026 — EO-REPO-005

- **`DOC-005` executada**: sincronização manual da base de conhecimento do Projeto ChatGPT concluída por Bruno;
- pacote obtido de `main@7a7d49f`; campo de instruções substituído pela versão de `01_INSTRUCOES_PROJETO_CHATGPT.md`;
- base com exatamente **18 anexos** (incluindo `README.md` e `AGENTS.md`), sem duplicados; `01_INSTRUCOES`, `docs/README.md` e `12_BASE` fora dos anexos;
- checklist pós-substituição sem divergências; **pendência operacional de `DOC-005` encerrada**;
- aceito com ressalva de evidência (sem comparação independente do campo de instruções contra o blob do commit);
- produto e `H-01` a `H-07` mantidos não validados; decisões 5–10 pendentes; próximo gate de produto continua a preparação da coleta responsável;
- etapa exclusivamente documental; sem nova decisão (`REGISTRO_DECISOES.md` inalterado).

## 11. Modelo para próxima atualização

```markdown
## Atualização [data] — [ID da etapa]

- Veredito:
- Entregáveis aceitos:
- Decisões aprovadas:
- Documentos atualizados:
- Riscos novos/encerrados:
- Pendências:
- Próxima etapa:
- Autorização concedida:
```
