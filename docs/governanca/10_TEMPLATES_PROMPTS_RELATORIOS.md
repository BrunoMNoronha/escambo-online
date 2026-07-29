# Templates de prompts, relatórios e auditoria

**Versão:** 0.2
**Uso:** copiar, preencher e enviar ao agente escolhido

## 1. Template principal de prompt de execução

```markdown
# [ID] — [Título da etapa]

## Papel
Atue como [papel técnico] responsável exclusivamente por esta etapa.

## Contexto
[Estado atual comprovado do projeto.]

## Fontes obrigatórias
Leia antes de agir:
- [arquivo/fonte 1]
- [arquivo/fonte 2]

Em caso de conflito, interrompa e relate a divergência.

## Objetivo único
[Resultado verificável.]

## Escopo
- [item incluído]
- [item incluído]

## Não escopo
- [item excluído]
- [item excluído]

## Regras a preservar
- [regra/decisão]
- [limite técnico]

## Arquivos esperados
- [arquivo ou diretório]

Não altere arquivos não relacionados.

## Sequência obrigatória
1. Inspecione o estado atual e alterações existentes.
2. Relate bloqueio antes de improvisar.
3. Execute a menor alteração necessária.
4. Atualize testes e documentação aplicáveis.
5. Execute as validações.
6. Revise o diff.
7. Entregue o relatório no formato solicitado.

## Critérios de aceite
- [critério observável]
- [critério observável]

## Validações obrigatórias
- `[comando]`
- `[comando]`

Se algum comando não puder ser executado, informe o motivo; não declare sucesso.

## Git e autonomia
- Não faça commit, push, merge, rebase, force-push ou PR.
- Não crie nem execute migration.
- Não adicione dependência ou serviço externo.
- Não altere regra de negócio, autenticação ou autorização.
- Para qualquer necessidade fora desses limites, pare e solicite decisão.

## Relatório final obrigatório
Use exatamente:
1. Resumo executivo
2. Estado inicial observado
3. Ações realizadas
4. Arquivos criados, alterados e removidos
5. Decisões e justificativas
6. Comandos executados e resultados
7. Critérios de aceite: aprovado/reprovado por item
8. Riscos, limitações e dívida técnica
9. Divergências ou bloqueios
10. Git status e confirmação de que não houve commit/push/PR
11. Próxima ação recomendada
```

## 2. Template de relatório do agente

```markdown
# Relatório [ID] — [Título]

## 1. Resumo executivo
[O que foi realizado e resultado.]

## 2. Estado inicial observado
- Branch:
- Commit base:
- Worktree:
- Dependências relevantes:

## 3. Ações realizadas
1. ...

## 4. Arquivos
| Arquivo | Ação | Motivo |
| --- | --- | --- |
| ... | criado/alterado/removido | ... |

## 5. Decisões
| Decisão | Motivo | Impacto |
| --- | --- | --- |
| ... | ... | ... |

## 6. Validações
| Comando | Código de saída | Resultado |
| --- | ---: | --- |
| ... | 0 | ... |

## 7. Critérios de aceite
| Critério | Status | Evidência |
| --- | --- | --- |
| ... | aprovado/reprovado | ... |

## 8. Riscos e limitações
- ...

## 9. Divergências ou bloqueios
- ...

## 10. Estado do Git
- `git status --short`:
- Commit criado: não
- Push realizado: não
- PR criada: não

## 11. Próxima ação recomendada
[Uma ação objetiva, sem executá-la.]
```

## 3. Template do ChatGPT para auditar relatório

```markdown
Analise o relatório abaixo contra o prompt original e as fontes do Projeto Escambo Online.

Não presuma que algo foi executado sem evidência. Verifique:
- correspondência entre objetivo, escopo e resultado;
- itens fora do escopo;
- arquivos afetados;
- comandos, códigos de saída e testes;
- critérios de aceite;
- impacto em regra de negócio, dados, segurança e documentação;
- uso indevido de migration, dependência, commit, push ou PR;
- riscos e inconsistências.

Entregue:
1. veredito: aprovado, aprovado com ressalvas, correção necessária ou bloqueado;
2. evidências que sustentam o veredito;
3. falhas ou lacunas;
4. impacto e risco;
5. prompt corretivo completo, se necessário;
6. próxima etapa recomendada apenas se a atual estiver aprovada.

PROMPT ORIGINAL:
[colar]

RELATÓRIO:
[colar]
```

## 4. Prompt executado — EO-DISC-001

**Executado em:** 29/07/2026

**Resultado:** consulte `docs/descoberta/`.

Preservado como histórico e modelo. Este prompt não autoriza implementação nem deve ser executado novamente sem uma finalidade nova.

```markdown
# EO-DISC-001 — Auditoria da base e plano de descoberta

## Papel
Atue como Product Manager e Analista de Negócios Sênior, com experiência em marketplaces, confiança e segurança.

## Contexto
Estamos iniciando o projeto provisoriamente chamado “Escambo Online”. O ChatGPT orquestra o trabalho; Bruno decide; Claude Code e Antigravity executam etapas; `BrunoMNoronha/escambo-online` é o repositório oficial. Ainda não existe autorização para criar aplicação, schema, infraestrutura ou código.

## Fontes obrigatórias
Leia integralmente:
- README.md
- docs/produto/02_FONTE_MESTRA_PRODUTO.md
- docs/produto/03_ESCOPO_MVP_REGRAS_NEGOCIO.md
- docs/produto/04_JORNADAS_HISTORIAS_CRITERIOS.md
- docs/arquitetura/05_MODELO_DOMINIO_DADOS.md
- docs/qualidade/07_QUALIDADE_SEGURANCA_PRIVACIDADE.md
- docs/produto/08_ROADMAP_BACKLOG.md
- docs/governanca/09_GOVERNANCA_IA_GITHUB.md
- docs/governanca/11_ESTADO_ATUAL_PROJETO.md

## Objetivo único
Auditar a coerência da proposta inicial e produzir um plano de descoberta capaz de validar as hipóteses que mais podem inviabilizar ou alterar o MVP.

## Escopo
- identificar contradições e lacunas;
- separar decisões confirmadas, propostas e perguntas pendentes;
- priorizar hipóteses por impacto e incerteza;
- definir público e amostra recomendada para pesquisa;
- elaborar roteiro de entrevistas sem perguntas indutivas;
- propor teste de protótipo e/ou landing page;
- definir evidências e critérios para manter, alterar ou rejeitar cada hipótese;
- recomendar a sequência das decisões de produto.

## Não escopo
- implementar código;
- criar repositório ou scaffold;
- escolher versões de framework;
- criar schema, migration ou API;
- criar identidade visual;
- declarar hipótese como validada sem evidência;
- pesquisar dados pessoais ou contatar participantes.

## Entregáveis esperados
Produza em Markdown:
1. `docs/descoberta/RELATORIO_AUDITORIA_PRODUTO_V1.md`
2. `docs/descoberta/PLANO_DESCOBERTA_V1.md`
3. `docs/descoberta/ROTEIRO_ENTREVISTAS_V1.md`
4. `docs/descoberta/MATRIZ_HIPOTESES_V1.md`
5. `docs/descoberta/DECISOES_PARA_BRUNO_V1.md`

Se o ambiente não permitir criar arquivos, devolva cada documento em bloco separado e integral.

## Regras
- Não modificar as fontes originais.
- Não inventar pesquisa, concorrentes, métricas ou respostas.
- Distinguir explicitamente fato, inferência, hipótese e recomendação.
- Evitar overengineering e expansão do MVP.
- Considerar liquidez regional, fraude, moderação, privacidade e segurança presencial.
- Para cada pergunta a Bruno, explicar o impacto de não decidi-la.

## Critérios de aceite
- todas as hipóteses H-01 a H-07 foram avaliadas;
- inconsistências entre documentos foram listadas;
- as dez decisões mais importantes estão priorizadas;
- o plano contém método, amostra, evidência, critério e ordem;
- o roteiro evita perguntas que induzam a solução;
- nenhuma implementação foi realizada.

## Git e autonomia
Não faça commit, push, PR, alteração de código, migration ou contato externo.

## Relatório final
Informe:
1. resumo;
2. fontes lidas;
3. arquivos produzidos;
4. principais lacunas;
5. decisões prioritárias;
6. limitações;
7. confirmação de ausência de implementação e operações Git;
8. próximo passo recomendado.
```

## 5. Prompt de correção

```markdown
# [ID]-FIX-01 — Correção do relatório/implementação

O resultado anterior foi classificado como **correção necessária**.

Corrija somente os itens abaixo:
1. [falha objetiva]
2. [falha objetiva]

Preserve todo o restante que já atende aos critérios. Não amplie o escopo.

Evidências obrigatórias:
- [evidência]
- [comando]

Restrições:
- [repetir limites relevantes]

Entregue novamente o relatório completo, destacando o que mudou desde a tentativa anterior.
```

## 6. Prompt de revisão independente

```markdown
Atue como revisor independente, em modo somente leitura.

Compare:
- prompt autorizado;
- documentos-fonte;
- relatório do executor;
- diff e resultados de testes disponíveis.

Procure especialmente:
- alteração fora do escopo;
- regra de negócio quebrada;
- falha de autorização;
- concorrência;
- teste frágil ou ausente;
- migration ou dependência não autorizada;
- divergência entre relatório e código.

Não altere arquivos. Entregue achados classificados em crítico, alto, médio e baixo, sempre com evidência verificável.
```
