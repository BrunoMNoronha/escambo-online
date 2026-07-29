# Índice da documentação

Este diretório organiza a fonte de conhecimento oficial por responsabilidade. A numeração original dos documentos foi preservada para manter rastreabilidade.

## Estado dos termos

| Termo | Significado |
| --- | --- |
| Confirmado | decisão explícita de Bruno ou regra operacional aprovada |
| Proposta | opção documentada que ainda depende de aprovação |
| Hipótese | afirmação que depende de evidência |
| Recomendação | caminho sugerido para decisão |
| Evidência | resultado observável de método executado |

## Ordem de leitura

1. [Estado atual](governanca/11_ESTADO_ATUAL_PROJETO.md)
2. [Registro de decisões](governanca/REGISTRO_DECISOES.md)
3. [Fonte-mestra](produto/02_FONTE_MESTRA_PRODUTO.md)
4. [Relatório de auditoria](descoberta/RELATORIO_AUDITORIA_PRODUTO_V1.md)
5. [Decisões para Bruno](descoberta/DECISOES_PARA_BRUNO_V1.md)
6. Demais documentos conforme a etapa.

## Produto

| Documento | Finalidade | Estado |
| --- | --- | --- |
| [02 — Fonte-mestra](produto/02_FONTE_MESTRA_PRODUTO.md) | tese, público, proposta de valor, hipóteses e riscos | Fronteiras da descoberta decididas; produto não validado |
| [03 — Escopo e regras](produto/03_ESCOPO_MVP_REGRAS_NEGOCIO.md) | capacidades, estados e invariantes | Proposta |
| [04 — Jornadas e histórias](produto/04_JORNADAS_HISTORIAS_CRITERIOS.md) | jornadas, backlog funcional e critérios | Requer refinamento |
| [08 — Roadmap](produto/08_ROADMAP_BACKLOG.md) | fases, gates e prioridades | Proposta |

## Descoberta

| Documento | Finalidade | Estado |
| --- | --- | --- |
| [Relatório de auditoria V1](descoberta/RELATORIO_AUDITORIA_PRODUTO_V1.md) | coerência, lacunas e inconsistências | Auditoria concluída |
| [Plano de descoberta V1](descoberta/PLANO_DESCOBERTA_V1.md) | método, amostra, evidência e sequência | D0 parcialmente aprovado; preparação pendente |
| [Roteiro de entrevistas V1](descoberta/ROTEIRO_ENTREVISTAS_V1.md) | entrevista não indutiva e teste de protótipo | Proposta |
| [Matriz de hipóteses V1](descoberta/MATRIZ_HIPOTESES_V1.md) | critérios para H-01 a H-07 | Pré-registro aprovado e congelado; nenhuma hipótese validada |
| [Decisões para Bruno V1](descoberta/DECISOES_PARA_BRUNO_V1.md) | dez decisões priorizadas | Decisões 1–4 respondidas; 5–10 pendentes |

## Arquitetura

| Documento | Finalidade | Estado |
| --- | --- | --- |
| [05 — Modelo conceitual](arquitetura/05_MODELO_DOMINIO_DADOS.md) | linguagem de domínio e invariantes conceituais | Não autoriza schema |
| [06 — Arquitetura inicial](arquitetura/06_ARQUITETURA_TECNICA_INICIAL.md) | direção técnica e ADRs futuros | Proposta |

## Qualidade

| Documento | Finalidade | Estado |
| --- | --- | --- |
| [07 — Qualidade, segurança e privacidade](qualidade/07_QUALIDADE_SEGURANCA_PRIVACIDADE.md) | requisitos, ameaças e gates | Requisitos iniciais |

## Governança

| Documento | Finalidade | Estado |
| --- | --- | --- |
| [01 — Instruções do Projeto ChatGPT](governanca/01_INSTRUCOES_PROJETO_CHATGPT.md) | orientação do orquestrador | Regra operacional |
| [09 — Governança de IA e GitHub](governanca/09_GOVERNANCA_IA_GITHUB.md) | papéis, limites e fluxo | Regra operacional |
| [10 — Templates](governanca/10_TEMPLATES_PROMPTS_RELATORIOS.md) | prompts, relatórios e auditoria | Modelo |
| [11 — Estado atual](governanca/11_ESTADO_ATUAL_PROJETO.md) | estágio, pendências e próximo gate | Registro vivo |
| [Registro de decisões](governanca/REGISTRO_DECISOES.md) | decisões confirmadas e propostas formais | Registro vivo |

## Regra de manutenção

- Decisão de produto: atualizar registro de decisões, fonte-mestra, escopo e estado quando aplicável.
- Decisão técnica: criar ADR e atualizar arquitetura após autorização.
- Descoberta executada: preservar instrumento, evidência, síntese e limitações.
- Mudança de prioridade: atualizar roadmap e estado.
- Implementação futura: atualizar documentação técnica e relatório da etapa.

Não duplicar uma decisão em vários documentos sem definir qual é a fonte primária.
