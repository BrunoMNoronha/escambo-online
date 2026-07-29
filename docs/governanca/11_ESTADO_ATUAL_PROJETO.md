# Estado atual do projeto

**Atualizado em:** 29/07/2026

**Fase:** 0 — descoberta e validação

**Status geral:** auditoria documental concluída; produto ainda não validado

## 1. Resumo

O repositório oficial foi definido e a base inicial foi auditada na etapa `EO-DISC-001`.

A auditoria concluiu que a proposta é coerente para iniciar descoberta, mas não está pronta para fechar MVP ou iniciar implementação. Nenhuma hipótese `H-01` a `H-07` possui evidência externa suficiente.

O próximo gate é Bruno decidir a fronteira da tese, as regiões, o público/categorias e os critérios prévios da pesquisa.

## 2. Decisões confirmadas

| ID | Decisão | Origem |
| --- | --- | --- |
| GOV-001 | ChatGPT organizará, documentará e orquestrará o desenvolvimento | Bruno |
| GOV-002 | Claude Code e Antigravity serão ferramentas/agentes de desenvolvimento | Bruno |
| GOV-003 | GitHub será usado para versionamento | Bruno |
| GOV-004 | Bruno mantém aprovação final de decisões e ações sensíveis | Governança adotada |
| GOV-005 | Commit, push, PR, migration e mudança sensível exigem autorização explícita | Governança adotada |
| GOV-006 | `BrunoMNoronha/escambo-online` é o repositório oficial | Bruno |

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

`H-01`, `H-02`, `H-05` e `H-07` são gates de viabilidade.

## 5. Decisões pendentes priorizadas

| Prioridade | Decisão | Quando |
| ---: | --- | --- |
| 1 | Fronteira da tese e complemento financeiro | antes da pesquisa |
| 2 | Regiões candidatas e unidade de liquidez | antes da pesquisa |
| 3 | Público, categorias e itens excluídos | antes da pesquisa |
| 4 | Critérios para manter, alterar ou rejeitar hipóteses | antes da pesquisa |
| 5 | Composição 1:1, 1:N ou N:N | antes do protótipo |
| 6 | Presencial, raio e compartilhamento progressivo | pesquisa e antes do piloto |
| 7 | Momento do chat e controles de abuso | antes do protótipo/piloto |
| 8 | Expiração, cancelamento e concorrência | antes do modelo de estados |
| 9 | Conclusão, problema, disputa e reputação | antes do piloto |
| 10 | Elegibilidade, moderação e gates do piloto | antes de usuários reais |

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
- CI/CD e infraestrutura.

## 8. Riscos abertos

- demanda insuficiente;
- ausência de liquidez regional;
- fraude e itens proibidos;
- insegurança em encontro presencial;
- assédio e exposição no chat;
- complexidade de trocas com vários itens;
- capacidade de moderação;
- retenção e tratamento de dados;
- crescimento de escopo antes da validação.

## 9. Próximo passo recomendado

Bruno deve responder às decisões 1 a 4 de [Decisões para Bruno V1](../descoberta/DECISOES_PARA_BRUNO_V1.md).

Depois:

1. registrar as decisões aprovadas;
2. ajustar e congelar critérios da matriz;
3. preparar recrutamento, consentimento e registro;
4. solicitar autorização específica antes de contatar participantes;
5. executar entrevistas antes de protótipo detalhado ou arquitetura.

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
