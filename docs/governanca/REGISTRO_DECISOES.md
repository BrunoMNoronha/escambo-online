# Registro de decisões

**Atualizado em:** 29/07/2026

**Responsável pela aprovação de produto:** Bruno

Este documento é a fonte primária das decisões explícitas do projeto. Propostas e recomendações não se tornam decisões apenas por estarem documentadas.

## Decisões confirmadas

### Governança

| ID | Data | Decisão | Origem | Impacto |
| --- | --- | --- | --- | --- |
| GOV-001 | 29/07/2026 | ChatGPT organizará, documentará e orquestrará o desenvolvimento | Bruno | Define o orquestrador |
| GOV-002 | 29/07/2026 | Claude Code e Antigravity atuarão como agentes de execução autorizada | Bruno | Define executores |
| GOV-003 | 29/07/2026 | GitHub será usado para versionamento | Bruno | Define histórico oficial |
| GOV-004 | 29/07/2026 | Bruno mantém aprovação final de decisões e ações sensíveis | Governança adotada | Preserva decisão humana |
| GOV-005 | 29/07/2026 | Commit, push, PR, migration e mudança sensível exigem autorização explícita | Governança adotada | Define gates |
| GOV-006 | 29/07/2026 | `BrunoMNoronha/escambo-online` é o repositório oficial do projeto | Bruno | Centraliza documentação e futuro código |

### Organização documental

| ID | Data | Decisão | Origem | Impacto |
| --- | --- | --- | --- | --- |
| DOC-001 | 29/07/2026 | Organizar documentos por `produto`, `descoberta`, `arquitetura`, `qualidade` e `governanca` | PR #1 aprovado | Define responsabilidades documentais |
| DOC-002 | 29/07/2026 | Manter `README.md` e `AGENTS.md` na raiz | PR #1 aprovado | Padroniza entrada de pessoas e agentes |
| DOC-003 | 29/07/2026 | Usar este registro como fonte primária das decisões confirmadas | PR #1 aprovado | Evita decisões dispersas |

### Produto e descoberta

| ID | Data | Decisão | Origem | Impacto |
| --- | --- | --- | --- | --- |
| PROD-001 | 29/07/2026 | A tese inicial será troca exclusivamente de bens, sem complemento financeiro | Bruno | Fecha a fronteira do experimento e do MVP inicial |
| DISC-001 | 29/07/2026 | O Distrito Federal será o mercado macro da descoberta e do possível piloto | Bruno | Delimita recrutamento e análise de liquidez |
| DISC-002 | 29/07/2026 | A unidade territorial de análise será a Região Administrativa; duas RAs deverão ser escolhidas antes do recrutamento | Decisão operacional derivada de DISC-001 | Evita tratar o DF como uma única célula de liquidez |
| DISC-003 | 29/07/2026 | A descoberta começará com três agrupamentos candidatos: livros/HQs/jogos de tabuleiro; casa/decoração portátil não elétrica; esporte/lazer portátil não motorizado | Aplicação dos critérios definidos por Bruno | Cria recorte comparável sem homologar categorias finais |
| DISC-004 | 29/07/2026 | Excluir da descoberta itens ilícitos, regulados, de procedência incerta, perigosos, íntimos, de alto risco ou que exijam garantia especializada | Bruno | Reduz risco jurídico, físico e operacional |
| DISC-005 | 29/07/2026 | Aprovar os critérios da matriz H-01 a H-07, inclusive interromper ou estreitar o projeto se H-01, H-02, H-05 ou H-07 falharem | Bruno | Pré-registra os gates e reduz viés retrospectivo |

## Limites das decisões

- `PROD-001` confirma a fronteira sem dinheiro, mas não valida `H-01`.
- `DISC-001` confirma o DF como macroárea, mas não valida liquidez.
- `DISC-003` define agrupamentos para pesquisa, não a taxonomia final do produto.
- `DISC-004` é um filtro inicial; a política completa de itens proibidos ainda exige detalhamento e revisão apropriada.
- `DISC-005` aprova critérios de decisão, não resultados.

## Pendências imediatas

1. Escolher duas Regiões Administrativas do Distrito Federal para a primeira amostra.
2. Definir canais e capacidade de recrutamento nessas RAs.
3. Aprovar consentimento, registro e retenção das notas de pesquisa.
4. Autorizar separadamente o contato com participantes.

As demais decisões de produto permanecem em [Decisões para Bruno V1](../descoberta/DECISOES_PARA_BRUNO_V1.md).

## Template

```markdown
| [ID] | [data] | [decisão objetiva] | Bruno | [impacto] |
```

Ao registrar uma decisão:

1. citar a evidência ou o motivo;
2. indicar documentos afetados;
3. atualizar o estado atual;
4. não apagar decisões anteriores; marcar substituição quando aplicável.
