# Instruções para agentes

Estas regras se aplicam a qualquer agente que analise ou altere este repositório.

## Estado do projeto

- Fase atual: **0 — descoberta e validação**.
- Produto, MVP e arquitetura ainda não estão homologados.
- Não existe autorização geral para aplicação, schema, migration, API ou infraestrutura.
- O estado vigente está em `docs/governanca/11_ESTADO_ATUAL_PROJETO.md`.

## Leitura mínima

Antes de qualquer atividade, leia:

1. `README.md`;
2. `docs/governanca/11_ESTADO_ATUAL_PROJETO.md`;
3. `docs/governanca/REGISTRO_DECISOES.md`;
4. as fontes específicas indicadas no prompt.

Para produto, leia também:

- `docs/produto/02_FONTE_MESTRA_PRODUTO.md`;
- `docs/produto/03_ESCOPO_MVP_REGRAS_NEGOCIO.md`;
- `docs/descoberta/MATRIZ_HIPOTESES_V1.md`;
- `docs/descoberta/DECISOES_PARA_BRUNO_V1.md`.

## Regras de análise

- Separe explicitamente **fato**, **inferência**, **hipótese**, **recomendação** e **decisão**.
- Não declare hipótese validada sem evidência coletada pelo método aprovado.
- Não invente execução, pesquisa, métricas observadas ou autorização.
- Preserve evidência contrária e riscos residuais.
- Em conflito, siga a hierarquia de verdade do `README.md`.
- Interrompa quando uma pendência de Bruno puder alterar materialmente o resultado.

## Limites de alteração

Sem autorização explícita e presente na etapa, não:

- altere visão, público, escopo ou regra de negócio;
- homologue stack ou arquitetura;
- crie código, scaffold, schema, migration, API ou infraestrutura;
- adicione dependência ou serviço externo;
- trate dado pessoal real;
- realize comunicação externa;
- faça merge, release ou mudança em produção.

Uma autorização documental não autoriza implementação.

## Automações, ferramentas e hospedagem

Bruno autorizou em 29/07/2026 (`GOV-007`, `GOV-008`, `INFRA-001`, `DOC-004`; fonte primária: `docs/governanca/REGISTRO_DECISOES.md`, limites em `docs/governanca/09_GOVERNANCA_IA_GITHUB.md`):

- **GitHub Actions e scripts Python** podem ser criados quando diretamente úteis ao objetivo autorizado de uma etapa (verificação, validação, teste, qualidade, segurança, auditoria, desempenho, redução de trabalho e tokens). Autorização para criá-los **não** significa autorização para criá-los em qualquer etapa.
- **Ferramentas gratuitas ou já incluídas** de Claude/Anthropic, OpenAI e GitHub podem ser usadas com custo incremental zero e menor privilégio. Recursos pagos, trials com conversão e excedentes continuam bloqueados.
- Nenhuma automação pode, por si só, realizar deploy, mutation remota, migration ou alteração de dados/schema sem autorização específica (`GOV-005`).
- Pare e relate antes de OAuth, conta, token, instalação de app, cobrança ou ampliação de permissão não autorizada.
- **Vercel** é a hospedagem preferencial sob custo zero, mas **não está configurada** e não há autorização de deploy; configuração de conta/projeto/integração exige autorização posterior e específica (detalhe técnico no `ADR-008`).
- **Higiene do repositório é controlada**: remova arquivos apenas com evidência (referências, substituto, impacto e valor histórico verificados); registre toda remoção; não versione arquivos temporários ou gerados.
- Sincronize a documentação afetada na mesma etapa. Na dúvida, interrompa e relate.

## Documentação

- Atualize somente documentos afetados pela etapa.
- Mantenha links relativos válidos.
- Registre decisão confirmada em `docs/governanca/REGISTRO_DECISOES.md`.
- Atualize `docs/governanca/11_ESTADO_ATUAL_PROJETO.md` ao concluir uma etapa aceita.
- Decisão arquitetural futura deve usar ADR.
- Relatório não substitui fonte-mestra nem decisão.

## Git e entrega

- Preserve trabalho existente e inspecione o diff.
- Use branch curta e commit focado quando autorizado.
- Não use force-push nem reescreva histórico.
- Não inclua alteração não relacionada.
- Informe arquivos, validações, limitações e estado do Git.
- Se uma validação não foi executada, declare isso.
