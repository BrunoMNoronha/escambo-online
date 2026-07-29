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
