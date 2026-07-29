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

## 13. Automações internas e ferramentas externas (`GOV-007` e `GOV-008`)

Origem: Bruno, 29/07/2026. Fonte primária: [Registro de decisões](REGISTRO_DECISOES.md).

`GOV-007` autoriza criar **GitHub Actions** e **scripts Python** quando forem diretamente necessários ao escopo de uma etapa, para verificação, validação, teste, análise de qualidade e segurança, auditoria documental, melhoria de desempenho, redução de trabalho repetitivo e economia de tempo e tokens.

`GOV-008` autoriza usar **ferramentas e recursos gratuitos ou já incluídos** das plataformas Claude/Anthropic, OpenAI e GitHub.

Limites obrigatórios em ambos os casos:

- a autorização é condicional e por etapa: criar Action ou script só é permitido quando útil ao objetivo autorizado daquela etapa, nunca por antecipação;
- **menor privilégio**: solicitar e usar o mínimo de permissões necessário;
- **custo incremental zero**: proibido ativar plano pago, trial com conversão automática ou excedente; confirmar o custo antes de usar;
- proibido expor segredos ou dados pessoais em prompts, logs, artefatos, Actions ou relatórios;
- nenhuma automação pode, por si só, realizar commit, push, PR, merge, deploy, mutation remota, migration, alteração de schema ou de dados sem autorização específica (`GOV-005`);
- **interromper e relatar** antes de qualquer OAuth, criação de conta/token, instalação de aplicativo, cobrança ou ampliação de permissão não autorizada — salvo quando a conexão já estiver aprovada e a operação não ampliar permissões;
- informar no relatório: ferramenta, finalidade, dados ou arquivos transmitidos, permissões e autenticação utilizadas, cotas ou limitações aplicáveis e custo incremental.

Antes de criar uma nova automação, reutilizar automação equivalente já existente e justificar a criação.

## 14. Requisitos para futuras GitHub Actions

Toda Action criada sob `GOV-007` deve:

- declarar `permissions` mínimos e explícitos (negar por padrão, conceder só o necessário);
- fixar ações de terceiros em versão confiável (SHA ou tag verificada), sem referências móveis;
- definir `timeout` por job;
- prevenir execução desnecessária (filtros de path, evento e concorrência);
- não emitir segredos em logs;
- não mascarar falhas (código de saída coerente; sem `|| true` que oculte erro);
- ter comando equivalente executável localmente quando aplicável;
- ter consumo compatível com as cotas do plano gratuito;
- gerar artefatos e definir retenção somente quando necessários.

## 15. Requisitos para futuros scripts Python

Todo script criado sob `GOV-007` deve:

- documentar entrada e saída;
- executar de forma determinística e reproduzível;
- retornar código de saída coerente (zero em sucesso, diferente de zero em falha);
- emitir mensagens de erro úteis;
- evitar dependências desnecessárias (preferir biblioteca padrão);
- suportar uso local e em CI quando aplicável;
- não alterar arquivos ou dados silenciosamente;
- oferecer modo somente leitura para auditorias, quando pertinente.

## 16. Limpeza controlada de arquivos (`DOC-004`)

Origem: Bruno, 29/07/2026. A higiene do repositório é contínua e controlada:

- documentos afetados por uma etapa são atualizados na mesma etapa;
- arquivos obsoletos, duplicados ou desnecessários só são removidos com evidência suficiente;
- nenhuma exclusão ocorre apenas pelo nome, idade ou aparente duplicidade;
- antes de excluir, verificar referências, substitutos e impacto em build, testes, links e valor histórico;
- consolidar o conteúdo relevante na fonte correta antes de remover;
- registrar toda remoção no relatório, com motivo e evidência;
- preservar histórico útil de forma recuperável pelo Git;
- não versionar arquivos temporários, gerados ou acidentais.
