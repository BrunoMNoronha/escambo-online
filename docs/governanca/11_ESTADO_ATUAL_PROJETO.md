# Estado atual do projeto

**Atualizado em:** 29/07/2026

**Fase:** 0 — descoberta e validação

**Status geral:** decisões iniciais incorporadas à base v0.2; produto ainda não validado

## 1. Resumo

O repositório oficial foi definido, a base inicial foi auditada na etapa `EO-DISC-001` e as quatro primeiras decisões de descoberta foram respondidas por Bruno.

A tese inicial é troca exclusivamente de bens, sem complemento financeiro. O Distrito Federal é o mercado macro, Região Administrativa é a unidade de análise e três agrupamentos candidatos delimitam a pesquisa. Os critérios de `H-01` a `H-07` foram aprovados, mas nenhuma hipótese possui evidência externa suficiente.

O próximo gate é Bruno escolher duas RAs e aprovar os instrumentos operacionais antes de qualquer recrutamento ou contato externo.

## 2. Decisões confirmadas

| ID | Decisão | Origem |
| --- | --- | --- |
| GOV-001 | ChatGPT organizará, documentará e orquestrará o desenvolvimento | Bruno |
| GOV-002 | Claude Code e Antigravity serão ferramentas/agentes de desenvolvimento | Bruno |
| GOV-003 | GitHub será usado para versionamento | Bruno |
| GOV-004 | Bruno mantém aprovação final de decisões e ações sensíveis | Governança adotada |
| GOV-005 | Commit, push, PR, migration e mudança sensível exigem autorização explícita | Governança adotada |
| GOV-006 | `BrunoMNoronha/escambo-online` é o repositório oficial | Bruno |
| PROD-001 | A tese testada é troca exclusivamente de bens, sem complemento financeiro | Bruno |
| DISC-001 | Distrito Federal é o mercado macro da descoberta | Bruno |
| DISC-002 | Região Administrativa é a unidade inicial de análise; duas RAs ainda serão escolhidas | decisão aplicada |
| DISC-003 | Três agrupamentos candidatos delimitam a pesquisa inicial | decisão aplicada |
| DISC-004 | Itens ilícitos, regulados, de procedência incerta, perigosos, íntimos, de alto risco ou que exijam garantia especializada ficam excluídos da descoberta | Bruno |
| DISC-005 | Os critérios de `MATRIZ_HIPOTESES_V1.md` estão aprovados, inclusive os gates críticos | Bruno |

A fonte primária dessas decisões é o [registro de decisões](REGISTRO_DECISOES.md).

## 3. Propostas ainda não homologadas

| ID | Proposta |
| --- | --- |
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

`H-01`, `H-02`, `H-05` e `H-07` são gates de viabilidade aprovados. Falha nesses gates pode estreitar, reformular ou interromper o projeto.

## 5. Decisões pendentes priorizadas

| Prioridade | Decisão | Quando |
| ---: | --- | --- |
| 1 | Escolher as duas RAs do Distrito Federal | antes do recrutamento |
| 2 | Aprovar recrutamento, consentimento, registro, retenção e responsável pelos dados | antes de qualquer contato |
| 3 | Composição 1:1, 1:N ou N:N | depois das entrevistas e antes do protótipo |
| 4 | Presencial, raio e compartilhamento progressivo | pesquisa e antes do piloto |
| 5 | Momento do chat e controles de abuso | antes do protótipo/piloto |
| 6 | Expiração, cancelamento e concorrência | antes do modelo de estados |
| 7 | Conclusão, problema, disputa e reputação | antes do piloto |
| 8 | Elegibilidade, moderação e gates do piloto | antes de usuários reais |

Detalhes: [Decisões para Bruno V1](../descoberta/DECISOES_PARA_BRUNO_V1.md).

## 6. Artefatos concluídos

### Base inicial

- instruções do Projeto ChatGPT;
- fonte-mestra v0.2;
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

### Base de conhecimento

- instrução do Projeto ChatGPT revisada;
- manifesto de substituição da base antiga pelos arquivos canônicos v0.2;
- decisões `PROD-001` e `DISC-001` a `DISC-005` rastreadas no registro vivo.

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

1. Bruno escolhe duas RAs do Distrito Federal com acesso real para recrutamento e possível piloto.
2. A equipe prepara critérios de recrutamento, consentimento, registro e retenção.
3. Bruno aprova os instrumentos e concede autorização específica para contato.
4. Somente então são executadas entrevistas, antes de protótipo detalhado ou arquitetura.

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

### 29/07/2026 — Decisões iniciais da descoberta

- troca exclusivamente de bens, sem complemento financeiro, confirmada;
- Distrito Federal definido como mercado macro e RA como unidade de análise;
- três agrupamentos candidatos e exclusões de risco incorporados;
- critérios de `H-01` a `H-07` aprovados;
- nenhuma hipótese promovida a validada;
- duas RAs mantidas como próximo gate.

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
