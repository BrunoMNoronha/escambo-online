# Governança de IA, execução e GitHub

**Versão:** 0.1  
**Status:** regra operacional do projeto

## 1. Papéis

| Papel | Responsabilidades | Não pode decidir sozinho |
| --- | --- | --- |
| Bruno | Aprovar produto, escopo, arquitetura, custos, mudanças sensíveis e releases | — |
| ChatGPT | Manter contexto, planejar, gerar prompts, auditar relatórios e recomendar próximos passos | Não inventa execução nem concede autorização em nome de Bruno |
| Claude Code | Analisar e implementar a etapa autorizada no repositório | Não amplia escopo nem publica sem autorização |
| Antigravity | Analisar, prototipar, implementar ou validar a etapa autorizada | Não amplia escopo nem publica sem autorização |
| GitHub | Versionar código, documentos, issues, PRs e checks | Não substitui a decisão de produto |

## 2. Regra de um responsável por etapa

Cada prompt de execução tem um agente principal. Dois agentes não devem alterar simultaneamente os mesmos arquivos.

O segundo agente pode atuar como revisor independente depois que a execução principal terminar. A revisão deve ter escopo somente leitura, salvo prompt corretivo posterior.

## 3. Fluxo padrão

1. Bruno apresenta objetivo ou relatório.
2. ChatGPT consulta as fontes e identifica o estado real.
3. ChatGPT define uma etapa curta.
4. Bruno aprova quando houver gate.
5. ChatGPT gera o prompt.
6. Um agente executa e devolve relatório.
7. ChatGPT audita escopo e evidências.
8. Se necessário, gera correção.
9. A documentação de estado e decisões é atualizada.
10. ChatGPT propõe a próxima etapa.

## 4. Gates que exigem autorização explícita

- mudança de visão, público ou escopo;
- regra de negócio relevante;
- arquitetura-base ou stack;
- nova dependência ou serviço externo relevante;
- custo recorrente;
- schema e migration;
- dados pessoais adicionais;
- autenticação, autorização ou criptografia;
- remoção ou transformação de dados;
- commit, push, PR, merge e release;
- acesso ou mudança em produção;
- comunicação externa em nome do projeto.

Na dúvida, o agente interrompe, relata e espera.

## 5. Anatomia de uma etapa

Uma etapa deve:

- ter um objetivo principal;
- caber em uma revisão;
- declarar não escopo;
- ter arquivos previstos;
- listar critérios de aceite;
- exigir validações;
- definir o que fazer em caso de bloqueio;
- terminar com relatório padronizado.

Não usar prompts como “implemente todo o MVP”.

## 6. Regras para Claude Code e Antigravity

Antes de alterar:

- ler instruções do repositório e documentos indicados;
- inspecionar estado e alterações existentes;
- preservar trabalho do usuário;
- registrar divergências;
- confirmar que a etapa não depende de decisão bloqueadora.

Durante:

- editar somente o necessário;
- não reformatar arquivos não relacionados;
- não ocultar erro;
- não usar dados reais;
- manter contratos e testes coerentes;
- interromper em caso de risco ou permissão ausente.

Depois:

- executar validações;
- revisar o próprio diff;
- verificar segredos e arquivos acidentais;
- entregar relatório completo;
- não criar commit, push ou PR sem autorização presente no prompt.

## 7. Estratégia Git proposta

Após ativação formal:

- branch principal protegida;
- branch por tarefa: `feat/...`, `fix/...`, `docs/...`, `chore/...`;
- commits convencionais e focados;
- PR pequena, revisável e vinculada à issue;
- checks obrigatórios;
- sem push direto na principal;
- sem force-push;
- squash ou merge definido por ADR de contribuição;
- tags e releases apenas após gate.

## 8. Conteúdo mínimo de PR

- contexto e problema;
- solução implementada;
- itens fora do escopo;
- arquivos ou módulos afetados;
- evidências de testes;
- screenshots ou vídeo para UI;
- impacto em banco e migration;
- segurança e privacidade;
- compatibilidade e rollback;
- riscos e pendências;
- documentação atualizada.

## 9. Auditoria de relatório

O ChatGPT deve verificar:

| Pergunta | Evidência esperada |
| --- | --- |
| O objetivo foi atendido? | correspondência com critérios |
| Houve ampliação de escopo? | lista de arquivos e diff |
| Testes passaram? | comandos e resultados |
| Erros foram ocultados? | ausência de skips/supressões indevidas |
| Regras foram preservadas? | referência às fontes |
| Dados/schema mudaram? | migration e aprovação |
| Segurança foi afetada? | análise e testes |
| Documentos ficaram coerentes? | arquivos atualizados |
| Há risco residual? | seção explícita no relatório |

## 10. Classificação final da etapa

- **Aprovado:** critérios e evidências completos.
- **Aprovado com ressalvas:** objetivo cumprido, pendências não bloqueadoras registradas.
- **Correção necessária:** falha corrigível dentro do mesmo escopo.
- **Bloqueado:** depende de decisão, acesso, risco ou mudança de escopo.

## 11. Atualização documental

Ao final de uma etapa:

- decisão de produto atualiza a fonte-mestra e o escopo;
- decisão técnica cria ou altera ADR;
- implementação atualiza documentação técnica;
- mudança de prioridade atualiza backlog;
- conclusão atualiza estado atual;
- comportamento lançado atualiza changelog.

## 12. Princípio de prestação de contas

Relatório é evidência, não cerimônia. Se uma ação não foi executada, deve constar como não executada. Se um teste falhou, o resultado deve ser preservado no relatório. Se houver incerteza, ela deve ser explicitada.
