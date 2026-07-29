# Roadmap e backlog inicial

**Versão:** 0.1  
**Status:** proposta orientada a gates

## 1. Estratégia

O roadmap é organizado por redução de risco, não apenas por telas. Cada fase termina com um gate explícito. A fase seguinte só começa quando bloqueios relevantes estiverem resolvidos.

## 2. Fases

### Fase 0 — Descoberta e validação

Objetivos:

- validar problema, público e região inicial;
- entrevistar potenciais usuários;
- testar proposta de valor;
- decidir as regras pendentes do MVP;
- mapear riscos jurídicos, operacionais e de moderação;
- estabelecer indicadores do piloto.

Entregáveis:

- relatório de descoberta;
- mapa de hipóteses;
- decisões de produto;
- PRD v1;
- backlog revisado;
- critérios de sucesso e cancelamento.

Gate:

- problema e público aprovados;
- escopo do MVP fechado;
- hipóteses críticas com plano de validação;
- riscos impeditivos identificados.

### Fase 1 — UX e arquitetura

Objetivos:

- prototipar jornadas críticas;
- testar compreensão de proposta e contraproposta;
- aprovar modelo de domínio;
- registrar ADRs;
- definir segurança, privacidade e moderação iniciais.

Entregáveis:

- fluxos e protótipo;
- relatório de usabilidade;
- arquitetura homologada;
- modelo de dados conceitual aprovado;
- contrato inicial de API;
- threat model inicial.

Gate:

- fluxo principal compreendido por usuários de teste;
- ADRs bloqueadores aprovados;
- hospedagem e limites do plano gratuito definidos no gate arquitetural (`INFRA-001`, detalhados no `ADR-008`);
- sem pendência crítica de regra.

### Fase 2 — Fundação do repositório

Objetivos:

- criar monorepo;
- configurar frontend, backend, banco local e CI;
- estabelecer padrões, testes e documentação;
- consolidar automações e verificações reutilizáveis do repositório (`GOV-007`), sem ativar recurso pago silenciosamente.

Entregáveis:

- scaffold mínimo;
- ambiente local reproduzível;
- lint, typecheck, testes e build no CI;
- templates de issue e PR;
- guias de contribuição e execução.

Gate:

- clone limpo sobe conforme README;
- pipeline verde;
- nenhuma funcionalidade de negócio implementada indevidamente.

### Fase 3 — Identidade, perfil e catálogo

Objetivos:

- autenticação e autorização;
- perfil;
- categorias;
- anúncios e imagens;
- descoberta básica.

Gate:

- usuário publica e encontra anúncio;
- controles de segurança e privacidade testados;
- moderação mínima de anúncio definida.

### Fase 4 — Negociação

Objetivos:

- proposta;
- revisões e contraproposta;
- aceite transacional;
- reserva;
- concorrência e idempotência.

Gate:

- nenhuma simulação de corrida permite reserva dupla;
- versão aceita é rastreável;
- testes de autorização e integração passam.

### Fase 5 — Comunicação e confiança

Objetivos:

- chat;
- notificações essenciais;
- conclusão;
- avaliações;
- denúncia, bloqueio e moderação.

Gate:

- jornada ponta a ponta completa;
- abuso básico pode ser reportado e tratado;
- dados sensíveis não são expostos indevidamente.

### Fase 6 — Hardening e homologação

Objetivos:

- segurança;
- acessibilidade;
- performance;
- observabilidade;
- backup e restauração;
- testes exploratórios;
- políticas e operação.

Gate:

- checklist de release aprovado;
- riscos críticos resolvidos;
- rollback ensaiado;
- portabilidade, limites de execução e custos de hospedagem validados antes do piloto, sem excedente ou recurso pago ativado silenciosamente;
- documentação operacional disponível.

### Fase 7 — Piloto controlado

Objetivos:

- operar com público e região limitados;
- acompanhar liquidez, abuso e suporte;
- medir hipóteses;
- corrigir problemas antes da expansão.

Gate:

- métricas e feedback justificam continuar, pivotar ou encerrar.

### Fase 8 — Evolução

Possíveis temas, somente com evidência:

- expansão regional;
- melhorias de matching;
- novos canais de notificação;
- PWA avançada ou app nativo;
- verificação adicional;
- modelo de negócio.

## 3. Backlog inicial priorizado

### P0 — Bloqueadores de descoberta

- definir região do piloto;
- definir público e categorias iniciais;
- decidir uma ou várias ofertas por lado;
- decidir chat e compartilhamento de contato;
- decidir expiração, cancelamento e conclusão;
- elaborar política inicial de itens proibidos;
- definir sinais de sucesso do piloto;
- validar proposta com usuários.

### P1 — Fundação do produto

- conta e sessão;
- perfil e região aproximada;
- categorias;
- anúncio e imagens;
- busca e filtros;
- proposta e revisões;
- aceite e reserva;
- chat;
- conclusão e avaliação;
- denúncia, bloqueio e moderação;
- auditoria.

### P2 — Qualidade operacional

- notificações por e-mail ou canal aprovado;
- painel administrativo;
- observabilidade;
- backup/restauração;
- exportação e exclusão de dados;
- acessibilidade;
- testes de carga dos fluxos críticos.

### P3 — Após validação

- recomendação/matching;
- favoritos;
- lista de desejos estruturada;
- reputação mais sofisticada;
- verificação adicional;
- novos mercados e categorias.

## 4. Critérios de priorização

Pontuar cada item por:

- valor para a jornada principal;
- redução de risco;
- dependência desbloqueada;
- esforço;
- custo operacional;
- risco de segurança e privacidade;
- evidência disponível.

Não priorizar apenas por entusiasmo técnico.

## 5. Gestão de mudanças

Uma nova ideia deve ser classificada:

- requisito do MVP;
- experimento da Fase 0;
- melhoria pós-MVP;
- fora da tese;
- decisão pendente.

Itens não aprovados não entram silenciosamente em prompts de implementação.
