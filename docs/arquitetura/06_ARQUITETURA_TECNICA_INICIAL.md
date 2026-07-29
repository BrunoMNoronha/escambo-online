# Arquitetura técnica inicial

**Versão:** 0.1  
**Status:** proposta; requer ADR e aprovação antes da implementação

## 1. Direção recomendada

Aplicação web responsiva, organizada como monólito modular e monorepo TypeScript. Essa direção reduz custo operacional e mantém separação suficiente para evoluir sem introduzir microserviços prematuramente.

## 2. Stack proposta

| Camada | Proposta | Observação |
| --- | --- | --- |
| Frontend | Next.js + TypeScript | Interface responsiva e aplicação web |
| Backend | NestJS + TypeScript | API e módulos de negócio |
| Banco | PostgreSQL | Transações e restrições importantes para reservas |
| ORM | Prisma | Produtividade, migrations e tipagem |
| Estilos | Tailwind CSS | Consistência e velocidade no MVP |
| API | REST + OpenAPI | Contratos explícitos e integração simples |
| Arquivos | Storage S3-compatible | Imagens fora do banco |
| Ambiente local | Docker Compose | Banco e dependências reproduzíveis |
| Testes | Jest + Playwright | Unidade/integração e E2E |
| CI | GitHub Actions | Checks de qualidade e build |

A versão do Node.js e de cada dependência deve ser fixada somente no kickoff técnico, usando uma versão suportada e compatível. Não copiar versões antigas de outros projetos sem validar suporte.

## 3. Estrutura

A documentação atual está organizada por responsabilidade:

```text
/
├── README.md
├── AGENTS.md
└── docs/
    ├── produto/
    ├── descoberta/
    ├── arquitetura/
    ├── qualidade/
    └── governanca/
```

Após os gates de produto e arquitetura, a estrutura técnica proposta é:

```text
/
├── apps/
│   ├── web/
│   └── api/
├── packages/
│   ├── contracts/
│   ├── config/
│   └── test-utils/
├── docs/
│   ├── produto/
│   ├── descoberta/
│   ├── arquitetura/
│   ├── qualidade/
│   ├── governanca/
│   ├── adr/
│   ├── operacao/
│   └── relatorios/
├── infra/
├── .github/
└── package.json
```

Usar workspaces nativos inicialmente. Adicionar ferramenta de build de monorepo apenas se houver ganho mensurável.

## 4. Módulos de backend

Proposta inicial:

- `auth`;
- `users`;
- `profiles`;
- `categories`;
- `listings`;
- `media`;
- `search`;
- `trade-proposals`;
- `conversations`;
- `notifications`;
- `ratings`;
- `reports`;
- `moderation`;
- `audit`;
- `health`.

Cada módulo deve separar:

- transporte/controller;
- casos de uso/application;
- domínio e regras;
- persistência/infraestrutura;
- contratos e validação.

Evitar uma Clean Architecture cerimonial. A separação deve proteger regras, testes e substituição de infraestrutura, sem multiplicar arquivos vazios.

## 5. Frontend

Áreas propostas:

- pública: descoberta e detalhes do anúncio;
- acesso: cadastro, login e recuperação;
- autenticada: perfil, meus anúncios, propostas, chat e avaliações;
- administrativa: denúncias, categorias, usuários e auditoria.

Regras:

- autorização real permanece no backend;
- Server Components e Client Components devem ser escolhidos conscientemente;
- estado local, estado remoto e formulário não devem ser misturados;
- formulários usam schema compartilhável quando isso não acoplar indevidamente as camadas;
- acessibilidade e mobile são critérios desde o primeiro componente.

## 6. API e contratos

- versionar a API quando houver contrato público que justifique;
- gerar e manter OpenAPI;
- respostas de erro com código estável e correlação;
- paginação consistente;
- idempotência nos comandos críticos;
- validação de payload no limite da aplicação;
- DTO público não expõe entidade de persistência;
- horários e enums possuem representação única.

## 7. Autenticação e autorização

Decisão pendente entre implementação própria controlada e provedor gerenciado. A decisão deve comparar:

- custo;
- complexidade;
- recuperação e verificação;
- revogação de sessões;
- dependência de fornecedor;
- requisitos de privacidade;
- suporte ao ambiente de desenvolvimento.

Independentemente da opção:

- senha com algoritmo apropriado, quando houver senha;
- sessão protegida;
- CSRF, XSS e rate limiting avaliados;
- RBAC para funções administrativas;
- autorização por propriedade para recursos de usuário;
- trilha de auditoria para ação administrativa.

## 8. Imagens

Fluxo proposto:

1. validar tipo, tamanho e quantidade;
2. gerar identificador não previsível;
3. enviar ao storage por fluxo controlado;
4. processar dimensões e remover metadados desnecessários;
5. armazenar apenas metadados e referência no banco;
6. servir por URL controlada;
7. remover órfãos por rotina segura.

Antivírus, moderação de imagem e CDN devem ser decididos conforme risco e volume.

## 9. Chat e notificações

Começar pelo mecanismo mais simples que satisfaça a experiência. Comparar formalmente:

- atualização periódica via API;
- Server-Sent Events;
- WebSocket.

Não adicionar Redis ou broker somente por expectativa futura. Notificações assíncronas precisam ser desacopladas da transação principal e tolerar repetição.

## 10. Observabilidade

Mínimo por ambiente:

- logs estruturados sem segredos;
- identificador de correlação;
- métricas de erro, latência e filas;
- rastreamento de ações administrativas;
- healthcheck e readiness;
- alerta para falhas críticas;
- política de retenção.

Ferramenta externa de monitoramento exige análise de custo e privacidade.

## 11. Ambientes

- `local`: desenvolvimento reproduzível;
- `test`: testes automatizados;
- `staging`: homologação próxima de produção;
- `production`: acesso restrito e mudanças controladas.

Configuração segue doze fatores quando aplicável. Segredos ficam fora do repositório. Dados reais não são copiados para desenvolvimento.

## 12. Decisões arquiteturais obrigatórias antes do scaffold

| ADR | Decisão |
| --- | --- |
| ADR-001 | Arquitetura e monorepo |
| ADR-002 | Stack e versões suportadas |
| ADR-003 | Autenticação e sessão |
| ADR-004 | Estratégia de upload e storage |
| ADR-005 | Modelo de chat |
| ADR-006 | Reserva, concorrência e idempotência |
| ADR-007 | Notificações |
| ADR-008 | Ambientes e hospedagem |

## 13. Não objetivos arquiteturais do MVP

- microserviços;
- Kubernetes;
- event sourcing;
- CQRS amplo;
- GraphQL sem caso de uso comprovado;
- múltiplos bancos;
- busca externa antes de medir limitação do PostgreSQL;
- infraestrutura multi-região;
- abstrações para fornecedores ainda inexistentes.

## 14. Gate de aprovação

Nenhum scaffold deve ser criado antes de:

- validar o escopo funcional;
- decidir as questões bloqueadoras da Fase 0;
- aprovar a arquitetura por ADR;
- definir critérios de sucesso e piloto;
- definir licença e política de contribuição no repositório oficial.
