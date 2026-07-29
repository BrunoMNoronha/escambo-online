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

## Decisões de desenho da descoberta

Aprovadas explicitamente por Bruno em 29/07/2026, encerrando o gate inicial de produto (decisões 1–4 de [Decisões para Bruno V1](../descoberta/DECISOES_PARA_BRUNO_V1.md)). Definem o teste da descoberta; **não validam** demanda, liquidez nem o MVP.

| ID | Data | Decisão | Origem | Impacto | Documentos afetados |
| --- | --- | --- | --- | --- | --- |
| DISC-001 | 29/07/2026 | A descoberta testa exclusivamente troca de bens sem complemento financeiro; menção espontânea a complemento é registrada como evidência e não altera a tese durante a coleta | Bruno | Fixa a fronteira da tese testada; reconsideração futura exige nova decisão de Bruno | `02_FONTE_MESTRA`, `03_ESCOPO`, `PLANO_DESCOBERTA_V1`, `MATRIZ_HIPOTESES_V1` |
| DISC-002 | 29/07/2026 | Regiões candidatas: Cruzeiro/DF e Guará/DF; unidade pública de localização é a Região Administrativa | Bruno | Define células de recrutamento e comparação; não presume liquidez; endereço exato permanece proibido | `02_FONTE_MESTRA`, `PLANO_DESCOBERTA_V1`, `MATRIZ_HIPOTESES_V1` |
| DISC-003 | 29/07/2026 | Público, três categorias candidatas e exclusões imediatas definidos como recorte de descoberta | Bruno | Delimita a amostra; não é política definitiva do MVP nem parecer jurídico | `02_FONTE_MESTRA`, `03_ESCOPO`, `PLANO_DESCOBERTA_V1` |
| DISC-004 | 29/07/2026 | Critérios de `MATRIZ_HIPOTESES_V1.md` aprovados sem alteração de conteúdo e congelados em 29/07/2026 | Bruno | Pré-registro; `H-01` a `H-07` seguem não validadas; falha de `H-01/H-02/H-05/H-07` pode interromper, restringir ou reformular o projeto | `MATRIZ_HIPOTESES_V1`, `PLANO_DESCOBERTA_V1` |

## Decisões documentais confirmadas

Propostas no PR #1 como `DOC-001` a `DOC-003` e **em vigor desde o merge do PR #1**, em 29/07/2026.

| ID | Data | Decisão | Origem | Impacto |
| --- | --- | --- | --- | --- |
| DOC-001 | 29/07/2026 | Organizar documentos por `produto`, `descoberta`, `arquitetura`, `qualidade` e `governanca` | Merge do PR #1 | Altera caminhos, não conteúdo de produto |
| DOC-002 | 29/07/2026 | Manter `README.md` e `AGENTS.md` na raiz | Merge do PR #1 | Padroniza leitura inicial de pessoas e agentes |
| DOC-003 | 29/07/2026 | Usar este registro como fonte primária das decisões confirmadas | Merge do PR #1 | Exige atualização após cada aprovação |

## Pendências de produto

As decisões 1–4 (fronteira da tese, regiões, público/categorias e critérios da matriz) foram respondidas em 29/07/2026 e estão registradas acima como `DISC-001` a `DISC-004`. As decisões 5–10 permanecem pendentes nos momentos previstos. A lista priorizada, as alternativas e o impacto de não decidir estão em:

- [Decisões para Bruno V1](../descoberta/DECISOES_PARA_BRUNO_V1.md)

Nenhuma recomendação da auditoria foi convertida automaticamente em decisão de produto; `DISC-001` a `DISC-004` decorrem de decisão explícita de Bruno, não de recomendação.

## Template

```markdown
| [ID] | [data] | [decisão objetiva] | Bruno | [impacto] |
```

Ao registrar uma decisão:

1. citar a evidência ou o motivo;
2. indicar documentos afetados;
3. atualizar o estado atual;
4. não apagar decisões anteriores; marcar substituição quando aplicável.
