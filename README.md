# Escambo Online

Base oficial de produto, descoberta e governança do projeto provisoriamente chamado **Escambo Online**.

> O produto está na **Fase 0 — descoberta e validação**. Não há MVP homologado, aplicação, schema ou infraestrutura autorizados.

## Situação atual

- Bruno é o responsável final por decisões e autorizações.
- ChatGPT organiza o trabalho, mantém contexto e audita resultados.
- Claude Code e Antigravity executam etapas autorizadas.
- Este repositório é a fonte versionada oficial do projeto.
- A auditoria documental `EO-DISC-001` foi concluída.
- Nenhuma hipótese `H-01` a `H-07` foi validada por pesquisa.
- O próximo gate é Bruno responder às quatro decisões necessárias antes da coleta.

Consulte o [estado atual do projeto](docs/governanca/11_ESTADO_ATUAL_PROJETO.md) antes de iniciar qualquer etapa.

## Próxima decisão

As quatro decisões imediatas são:

1. confirmar se complemento financeiro permanece fora da tese inicial;
2. escolher as regiões candidatas;
3. delimitar público, categorias e exclusões;
4. aprovar ou ajustar os critérios de decisão das hipóteses.

O contexto, as alternativas e o impacto de não decidir estão em [Decisões para Bruno V1](docs/descoberta/DECISOES_PARA_BRUNO_V1.md).

## Documentação

| Área | Conteúdo |
| --- | --- |
| [Produto](docs/produto/) | fonte-mestra, escopo, jornadas e roadmap |
| [Descoberta](docs/descoberta/) | auditoria, plano, roteiro, hipóteses e decisões pendentes |
| [Arquitetura](docs/arquitetura/) | modelo conceitual e proposta técnica ainda não homologada |
| [Qualidade](docs/qualidade/) | qualidade, segurança, privacidade e gates |
| [Governança](docs/governanca/) | instruções, papéis, templates, decisões e estado atual |

O [índice completo](docs/README.md) apresenta ordem de leitura, finalidade e estado de cada documento.

## Hierarquia de verdade

Em caso de divergência, prevalece:

1. decisão explícita e mais recente de Bruno;
2. [registro de decisões](docs/governanca/REGISTRO_DECISOES.md);
3. [fonte-mestra do produto](docs/produto/02_FONTE_MESTRA_PRODUTO.md);
4. [escopo e regras de negócio](docs/produto/03_ESCOPO_MVP_REGRAS_NEGOCIO.md);
5. documentos técnicos e de qualidade;
6. roadmap, prompts e relatórios;
7. implementação existente.

Código não homologa regra de negócio. Divergências devem ser registradas e submetidas à decisão.

## Organização do repositório

```text
/
├── README.md
├── AGENTS.md
└── docs/
    ├── README.md
    ├── produto/
    ├── descoberta/
    ├── arquitetura/
    ├── qualidade/
    └── governanca/
```

Diretórios de aplicação, infraestrutura, ADRs e relatórios técnicos só serão adicionados quando seus gates forem autorizados.

## Regras para contribuir

- Leia [AGENTS.md](AGENTS.md) e as fontes obrigatórias da etapa.
- Trabalhe em uma branch curta e mantenha alterações relacionadas.
- Separe fato, inferência, hipótese, recomendação e decisão.
- Não transforme proposta técnica ou de produto em decisão.
- Não implemente código, schema, migration ou infraestrutura sem autorização explícita.
- Não use dados pessoais reais ou segredos.
- PRs devem informar escopo, evidências, riscos, pendências e impacto documental.

## Limites desta base

Esta documentação não representa validação de mercado, parecer jurídico, garantia de segurança ou arquitetura homologada. O objetivo atual é reduzir incerteza antes de investir em implementação.
