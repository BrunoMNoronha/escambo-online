# Registro de decisões

**Atualizado em:** 29/07/2026

**Responsável pela aprovação de produto:** Bruno

Este documento registra decisões explícitas. Propostas e recomendações não se tornam decisões apenas por estarem documentadas.

## Decisões confirmadas

| ID | Data | Decisão | Origem | Impacto |
| --- | --- | --- | --- | --- |
| GOV-001 | 29/07/2026 | ChatGPT organizará, documentará e orquestrará o desenvolvimento | Bruno | Define o orquestrador |
| GOV-002 | 29/07/2026 | Claude Code e Antigravity atuarão como agentes de execução autorizada | Bruno | Define executores |
| GOV-003 | 29/07/2026 | GitHub será usado para versionamento | Bruno | Define histórico oficial |
| GOV-004 | 29/07/2026 | Bruno mantém aprovação final de decisões e ações sensíveis | Governança adotada | Preserva decisão humana |
| GOV-005 | 29/07/2026 | Commit, push, PR, migration e mudança sensível exigem autorização explícita | Governança adotada | Define gates |
| GOV-006 | 29/07/2026 | `BrunoMNoronha/escambo-online` é o repositório oficial do projeto | Bruno | Centraliza documentação e futuro código |

## Decisões documentais propostas neste PR

Estas decisões entram em vigor com a aprovação e o merge do PR correspondente.

| ID | Proposta | Motivo | Impacto |
| --- | --- | --- | --- |
| DOC-001 | Organizar documentos por `produto`, `descoberta`, `arquitetura`, `qualidade` e `governanca` | Facilitar navegação e responsabilidade | Altera caminhos, não conteúdo de produto |
| DOC-002 | Manter `README.md` e `AGENTS.md` na raiz | Dar entrada clara a pessoas e agentes | Padroniza leitura inicial |
| DOC-003 | Usar este registro como fonte primária das decisões confirmadas | Evitar decisões dispersas | Exige atualização após cada aprovação |

## Pendências de produto

As decisões de produto continuam pendentes. A lista priorizada, as alternativas e o impacto de não decidir estão em:

- [Decisões para Bruno V1](../descoberta/DECISOES_PARA_BRUNO_V1.md)

Nenhuma recomendação da auditoria foi convertida automaticamente em decisão de produto.

## Template

```markdown
| [ID] | [data] | [decisão objetiva] | Bruno | [impacto] |
```

Ao registrar uma decisão:

1. citar a evidência ou o motivo;
2. indicar documentos afetados;
3. atualizar o estado atual;
4. não apagar decisões anteriores; marcar substituição quando aplicável.
