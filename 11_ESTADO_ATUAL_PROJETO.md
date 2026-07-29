# Estado atual do projeto

**Atualizado em:** 29/07/2026  
**Fase:** 0 — descoberta e validação  
**Status geral:** base inicial criada; produto ainda não validado

## 1. Decisões confirmadas

| ID | Decisão | Origem |
| --- | --- | --- |
| GOV-001 | ChatGPT organizará, documentará e orquestrará o desenvolvimento | Bruno |
| GOV-002 | Claude Code e Antigravity serão ferramentas/agentes de desenvolvimento | Bruno |
| GOV-003 | GitHub será usado para versionamento | Bruno |
| GOV-004 | Bruno mantém aprovação final de decisões e ações sensíveis | Governança adotada |
| GOV-005 | Commit, push, PR, migration e mudança sensível exigem autorização explícita | Governança adotada |

## 2. Propostas ainda não homologadas

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
| TECH-004 | Storage S3-compatible para imagens |
| TECH-005 | Docker Compose local e GitHub Actions |

Nenhuma proposta desta seção autoriza implementação.

## 3. Decisões pendentes prioritárias

| Prioridade | Decisão | Impacto |
| ---: | --- | --- |
| 1 | Região e público do piloto | Liquidez, operação e pesquisa |
| 2 | Categorias iniciais e itens proibidos | Risco e foco |
| 3 | Troca 1:1 ou N:N | UX, domínio e transação |
| 4 | Complemento financeiro | Tese, risco e complexidade |
| 5 | Momento do chat e compartilhamento de contato | Segurança e conversão |
| 6 | Expiração, cancelamento e conclusão | Estados e automações |
| 7 | Tratamento de propostas concorrentes | Consistência e experiência |
| 8 | Idade mínima e verificação | Jurídico e confiança |
| 9 | Política de disputa e moderação | Operação e responsabilidade |
| 10 | Critérios de sucesso do piloto | Decisão de continuar ou pivotar |

## 4. Artefatos concluídos

- instrução inicial do Projeto ChatGPT;
- fonte-mestra v0.1;
- escopo e regras propostas;
- jornadas, histórias e critérios;
- modelo conceitual;
- arquitetura proposta;
- requisitos de qualidade, segurança e privacidade;
- roadmap;
- governança de agentes e GitHub;
- templates de prompt, relatório e auditoria.

## 5. Não iniciado

- pesquisa com usuários;
- validação de mercado;
- análise jurídica;
- nome e marca definitivos;
- protótipo;
- ADRs homologados;
- repositório;
- scaffold;
- implementação;
- CI/CD;
- infraestrutura.

## 6. Riscos abertos

- liquidez insuficiente;
- fraude e itens proibidos;
- insegurança em encontro presencial;
- assédio e exposição no chat;
- custo e abuso de imagens;
- complexidade de trocas N:N;
- operação de moderação;
- retenção e tratamento de dados;
- escopo crescer antes da validação.

## 7. Próximo passo recomendado

Executar `EO-DISC-001 — Auditoria da base e plano de descoberta`, disponível em `10_TEMPLATES_PROMPTS_RELATORIOS.md`.

Após o relatório:

1. ChatGPT audita evidências e incoerências.
2. Bruno responde apenas às decisões prioritárias realmente necessárias.
3. Atualizar fonte-mestra, escopo e estado.
4. Executar entrevistas e teste de proposta.
5. Somente então iniciar UX e arquitetura.

## 8. Modelo para próxima atualização

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
