# Kit inicial — Projeto Escambo Online

**Versão:** 0.1  
**Data:** 29/07/2026  
**Status:** base inicial para descoberta e planejamento  
**Nome do produto:** “Escambo Online” é provisório

## Objetivo deste kit

Este conjunto de arquivos estabelece a base de conhecimento usada pelo ChatGPT para organizar, documentar e orquestrar o desenvolvimento do produto.

O modelo operacional definido é:

1. Bruno atua como responsável final pelas decisões e aprovações.
2. O ChatGPT mantém o contexto, organiza o backlog, propõe as próximas etapas, elabora prompts e audita os relatórios.
3. Claude Code e Antigravity executam análises e atividades de desenvolvimento autorizadas.
4. O GitHub mantém o histórico do código, da documentação e das decisões.

## Ordem recomendada para adicionar ao Projeto do ChatGPT

1. Cole o conteúdo de `01_INSTRUCOES_PROJETO_CHATGPT.md` no campo **Instruções do projeto**.
2. Adicione os demais arquivos `.md` como fontes da base de conhecimento.
3. Inicie uma conversa no projeto usando o prompt “Fase 0”, disponível em `10_TEMPLATES_PROMPTS_RELATORIOS.md`.
4. Atualize `11_ESTADO_ATUAL_PROJETO.md` ao concluir cada etapa.

## Documentos

| Arquivo | Função |
| --- | --- |
| `01_INSTRUCOES_PROJETO_CHATGPT.md` | Instrução pronta para o Projeto do ChatGPT |
| `02_FONTE_MESTRA_PRODUTO.md` | Visão, problema, público, princípios e hipóteses do MVP |
| `03_ESCOPO_MVP_REGRAS_NEGOCIO.md` | Escopo funcional, estados, regras e invariantes |
| `04_JORNADAS_HISTORIAS_CRITERIOS.md` | Jornadas, épicos, histórias e critérios de aceite |
| `05_MODELO_DOMINIO_DADOS.md` | Modelo conceitual de domínio e requisitos de dados |
| `06_ARQUITETURA_TECNICA_INICIAL.md` | Arquitetura proposta e decisões que ainda exigem validação |
| `07_QUALIDADE_SEGURANCA_PRIVACIDADE.md` | Estratégias mínimas de qualidade, segurança e privacidade |
| `08_ROADMAP_BACKLOG.md` | Fases, gates e backlog inicial priorizado |
| `09_GOVERNANCA_IA_GITHUB.md` | Papéis, fluxo entre agentes, GitHub e limites de autonomia |
| `10_TEMPLATES_PROMPTS_RELATORIOS.md` | Modelos de prompt, relatório e auditoria |
| `11_ESTADO_ATUAL_PROJETO.md` | Registro vivo do estágio, decisões e próximo passo |

## Hierarquia das fontes

Quando houver divergência, prevalece esta ordem:

1. decisão explícita e mais recente de Bruno;
2. `02_FONTE_MESTRA_PRODUTO.md`;
3. decisões formalizadas no registro de decisões do projeto;
4. `03_ESCOPO_MVP_REGRAS_NEGOCIO.md`;
5. arquitetura e demais documentos técnicos;
6. backlog, prompts e relatórios;
7. código atual.

O código não altera uma regra de negócio por si só. Uma divergência entre código e documentação deve ser registrada e submetida à decisão.

## Convenções de manutenção

- Documentos textuais usam Markdown e ficam versionados junto ao projeto.
- Toda mudança relevante informa data, motivo, impacto e responsável pela aprovação.
- Decisões arquiteturais relevantes usam ADR.
- Relatórios de agentes registram comandos executados e resultados observados.
- Nenhum relatório pode declarar sucesso sem evidência reproduzível.
- Regras provisórias permanecem identificadas como hipóteses até aprovação explícita.

## Situação inicial

Este kit não representa validação de mercado, parecer jurídico ou arquitetura homologada. Ele transforma a ideia inicial em uma base controlada para executar a Fase 0 de descoberta.
