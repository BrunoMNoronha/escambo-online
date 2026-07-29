# EO-DISC-001 — Relatório de auditoria do produto V1

**Projeto:** Escambo Online

**Data-base:** 29/07/2026

**Natureza:** auditoria documental

**Status:** concluído para decisão de Bruno; não representa validação de mercado

## 1. Convenções de leitura

- **Fato:** consta explicitamente nas fontes ou descreve o estado documental observado.
- **Inferência:** conclusão analítica derivada da combinação das fontes.
- **Hipótese:** afirmação ainda dependente de evidência externa ou teste.
- **Recomendação:** curso de ação sugerido; depende de aprovação de Bruno.

Não foram realizadas entrevistas, pesquisa de mercado, análise de concorrentes, contato com participantes ou coleta de dados. Portanto, nenhuma hipótese de produto está validada.

## 2. Resumo executivo

**Fato:** a base apresenta uma tese coerente para um marketplace regional de troca de bens entre pessoas, sem intermediação financeira, com negociação estruturada, privacidade progressiva e controles de confiança e segurança.

**Fato:** além das decisões de governança, Bruno confirmou após a auditoria a tese de troca exclusivamente de bens, o Distrito Federal como mercado macro, os recortes iniciais de categoria e os critérios de decisão da matriz. Essas decisões delimitam a descoberta; não validam demanda, liquidez ou segurança.

**Inferência:** a proposta é suficientemente estruturada para iniciar descoberta, mas não para fechar PRD, arquitetura ou backlog de implementação. O fluxo funcional está mais detalhado do que a evidência disponível sobre problema, liquidez e operação.

**Hipótese:** a maior ameaça à viabilidade não é técnica. É formar, em uma região e janela de tempo úteis, pares compatíveis de pessoas, itens e interesses, com confiança suficiente para que a troca presencial aconteça.

**Decisão confirmada:** `H-01`, `H-02`, `H-05` e `H-07` são hipóteses de gate. Se demanda, liquidez regional, viabilidade presencial ou capacidade de moderação falharem nos critérios aprovados, o MVP deverá ser estreitado, reformulado ou suspenso antes de qualquer implementação.

## 3. Fontes lidas integralmente

1. `README.md`
2. `02_FONTE_MESTRA_PRODUTO.md`
3. `03_ESCOPO_MVP_REGRAS_NEGOCIO.md`
4. `04_JORNADAS_HISTORIAS_CRITERIOS.md`
5. `05_MODELO_DOMINIO_DADOS.md`
6. `07_QUALIDADE_SEGURANCA_PRIVACIDADE.md`
7. `08_ROADMAP_BACKLOG.md`
8. `09_GOVERNANCA_IA_GITHUB.md`
9. `11_ESTADO_ATUAL_PROJETO.md`

## 4. Avaliação geral de coerência

### 4.1 Pontos coerentes e bem alinhados

| Tema | Constatação | Classificação |
| --- | --- | --- |
| Governança | Bruno decide; ChatGPT orquestra; agentes executam somente etapas autorizadas | Fato |
| Estado do produto | Produto está na Fase 0 e não foi validado | Fato |
| Núcleo da proposta | Troca de bens, negociação estruturada e ausência de pagamento processado no MVP proposto | Fato |
| Segurança | A plataforma reduz riscos, mas não garante autenticidade do item nem segurança do encontro | Fato |
| Privacidade | Localização pública aproximada e exposição progressiva de contato | Fato |
| Consistência | Aceite e reserva de todos os itens são tratados como operação atômica | Fato |
| Rastreabilidade | Revisões de proposta, estados críticos, moderação e auditoria devem preservar histórico | Fato |
| Roadmap | Descoberta precede UX, arquitetura, repositório e implementação | Fato |
| Escopo | Pagamento, escrow, frete integrado, app nativo e matching avançado estão fora do MVP proposto | Fato |
| Prudência | Documentos técnicos declaram explicitamente que não autorizam schema ou migration | Fato |

### 4.2 Veredito

**Inferência:** existe coerência de princípios, mas não existe ainda coerência decisória suficiente para implementar. Algumas jornadas e entidades estão descritas como se o comportamento já estivesse escolhido, enquanto o documento de estado corretamente mantém essas escolhas como propostas.

**Recomendação:** usar as jornadas, estados e entidades apenas como material de teste. O resultado da descoberta deve simplificar ou alterar esses artefatos antes de qualquer especificação técnica.

## 5. Inconsistências e ambiguidades entre documentos

| ID | Tema | Evidência documental | Consequência | Tratamento recomendado |
| --- | --- | --- | --- | --- |
| INC-01 | Complemento financeiro | `02` e `03` o colocam fora do MVP; `11` o mantém como decisão pendente prioritária | A fronteira central da tese não está formalmente homologada | Bruno deve decidir se “sem complemento” é uma hipótese a testar ou uma restrição já aprovada |
| INC-02 | Idade mínima | `02` define público maior de idade; `03`, `07` e `11` tratam idade como pendência jurídica | Público de pesquisa, cadastro e política ficam indefinidos | Adotar somente adultos na pesquisa inicial por prudência; decidir elegibilidade do piloto após revisão apropriada |
| INC-03 | Cardinalidade da troca | `02` fala em um ou mais itens oferecidos; `03` e `04` partem de um anúncio-alvo e vários itens próprios; `05` descreve um ou mais itens em cada lado se N:N for aprovado; `11` cita “um ou mais anúncios por lado” | Não está claro se a alternativa é 1:1, 1:N ou N:N | Testar primeiro 1:1 contra 1:N; não assumir N:N sem evidência de necessidade e compreensão |
| INC-04 | Momento do chat | `02`, `03` e `04` incluem chat na negociação; `03` e `11` registram o momento de abertura como pendente | Segurança, moderação, conversão e domínio da conversa dependem dessa regra | Comparar chat após proposta versus após aceite; mensagem inicial estruturada pode existir sem chat livre |
| INC-05 | Notificações | `04` contém história de aviso; `05` contém `Notification`; `08` posiciona notificações essenciais na Fase 5 e e-mail em P2 | Não está claro o mínimo necessário para a jornada nem o canal | Definir eventos essenciais e deixar canal/sofisticação fora até validar a jornada |
| INC-06 | Problema, disputa e conclusão | `02` prevê “registrar conclusão ou problema”; `03` tem `DISPUTED`, mas política e conclusão unilateral estão pendentes; `04` liga avaliação à conclusão | Estados e direitos das partes não têm regra operacional | Separar “relatar problema”, “disputa operacional” e “denúncia”; decidir efeito sobre conclusão e avaliação |
| INC-07 | Status do MVP | `02` usa “o MVP deverá permitir” e `03` descreve “capacidades do MVP”, embora ambos e `11` mantenham os itens como hipóteses/propostas | O texto pode ser interpretado como aprovação inexistente | Padronizar a linguagem futura como “MVP proposto” até decisão de Bruno |
| INC-08 | Acesso administrativo ao chat | `03` condiciona acesso a hipótese e permissão formal; `04` e `07` exigem denúncia/moderação de mensagem | Moderação de assédio não funciona sem regra de acesso, evidência e retenção | Definir acesso por denúncia, escopo mínimo, logs, papéis e retenção antes do piloto |
| INC-09 | Estado do repositório | `11` lista “repositório” como não iniciado, embora Bruno tenha definido `BrunoMNoronha/escambo-online` como repositório oficial e a base já esteja versionada | O registro vivo não representa o estado real | Atualizar o estado e registrar formalmente o repositório oficial |
| INC-10 | Critérios do piloto | `08` exige indicadores e critérios de sucesso/cancelamento na Fase 0; `11` mantém esses critérios pendentes | Sem regra prévia, qualquer resultado pode ser racionalizado depois | Pré-registrar gates antes de entrevistas, protótipo e landing page |
| INC-11 | Compartilhamento de localização e contato | Todos defendem progressividade, mas momento, granularidade, consentimento e revogação não estão definidos | Pode haver exposição precoce ou bloqueio da logística | Testar o momento de revelação e definir dado mínimo por etapa |
| INC-12 | Operação de moderação | Moderação manual mínima aparece no MVP proposto, mas não há responsável, horário, capacidade, severidade ou recurso | H-07 não pode ser avaliada nem o piloto operado com segurança | Criar política provisória e simulação de fila antes do piloto |
| INC-13 | Bloqueio durante negociação | `UserBlock` e bloqueio fazem parte dos documentos, mas não há efeito definido sobre proposta aceita, chat, denúncia ou conclusão | Usuário pode ficar sem canal para concluir ou reportar risco | Definir comportamento por estado da negociação |
| INC-14 | Remoção e ocultação | `REMOVED` reúne remoção pelo dono e pela moderação; administração também “oculta” anúncio | Visibilidade, motivo e possibilidade de recurso podem ficar ambíguos | Diferenciar motivo/ator no histórico mesmo que o estado público permaneça simples |

### 5.1 Tratamento documental após a auditoria

- `INC-07`: linguagem ajustada para distinguir “MVP proposto” de decisão homologada.
- `INC-09`: estado atualizado com o repositório oficial.
- Organização documental: fontes separadas por responsabilidade e índice central criado.
- Demais inconsistências permanecem pendentes porque exigem evidência ou decisão de Bruno; não foram resolvidas por edição textual.

### 5.2 Decisões posteriores incorporadas

| Item | Situação em 29/07/2026 | Efeito |
| --- | --- | --- |
| `INC-01` | Resolvida como fronteira de tese | Troca exclusivamente de bens; complemento financeiro excluído |
| Recorte territorial | Parcialmente resolvido | Distrito Federal é o mercado macro; RA é a unidade de análise; duas RAs ainda devem ser escolhidas |
| Recorte de categorias | Resolvido para a descoberta | Três agrupamentos candidatos foram definidos; não são taxonomia definitiva |
| Itens excluídos | Resolvido para a descoberta | Aplicam-se as exclusões de risco registradas na fonte-mestra |
| `INC-10` | Resolvida para o pré-registro | Critérios da matriz aprovados, inclusive gates críticos |

Nenhuma dessas decisões muda o estado de `H-01` a `H-07`: todas continuam não validadas.

## 6. Decisões confirmadas, propostas e pendências

### 6.1 Confirmadas

| ID | Decisão | Fonte |
| --- | --- | --- |
| GOV-001 | ChatGPT organizará, documentará e orquestrará o trabalho | `11` |
| GOV-002 | Claude Code e Antigravity atuarão como executores autorizados | `11` |
| GOV-003 | GitHub será o mecanismo de versionamento | `11` |
| GOV-004 | Bruno mantém decisão final sobre produto e ações sensíveis | `09`, `11` |
| GOV-005 | Commit, push, PR, migration e mudanças sensíveis exigem autorização explícita | `09`, `11` |
| GOV-006 | `BrunoMNoronha/escambo-online` é o repositório oficial | registro vivo |
| PROD-001 | A tese testada é troca exclusivamente de bens, sem complemento financeiro | decisão de Bruno |
| DISC-001 | Distrito Federal é o mercado macro da descoberta | decisão de Bruno |
| DISC-002 | Região Administrativa é a unidade inicial de análise; duas RAs ainda serão escolhidas | decisão aplicada |
| DISC-003 | Três agrupamentos candidatos foram definidos para a pesquisa | decisão aplicada |
| DISC-004 | Itens de risco definidos ficam excluídos da descoberta | decisão de Bruno |
| DISC-005 | Critérios da matriz e gates críticos estão aprovados | decisão de Bruno |

### 6.2 Propostas, não decisões

| Área | Propostas atuais |
| --- | --- |
| Produto | encontro presencial; chat contextual; reputação; moderação mínima |
| Escopo | conta, anúncio, descoberta, proposta, contraproposta, reserva, conclusão, avaliação e denúncia |
| Canal | aplicação web responsiva/PWA |
| Tecnologia | monorepo TypeScript, Next.js, NestJS, PostgreSQL, Prisma, storage compatível com S3, Docker Compose e GitHub Actions |
| Operação | moderação manual inicial e piloto controlado |

### 6.3 Perguntas pendentes de maior impacto

1. Há comportamento recorrente de troca sem dinheiro ou apenas interesse declarado?
2. Quais duas RAs do Distrito Federal permitem recrutamento e comparação controlada?
3. Em qual célula RA × agrupamento se concentra oferta e demanda compatíveis?
4. 1:1 é suficiente ou existe necessidade comprovada de 1:N/N:N?
5. O encontro presencial cabe na distância, mobilidade e percepção de segurança do público?
6. Em que momento chat, telefone e local podem ser compartilhados?
7. Como expiração, cancelamento, concorrência, conclusão, problema e avaliação funcionam?
8. Qual nível de verificação e elegibilidade é proporcional ao risco?
9. Quem modera, com qual política, capacidade, prazo e mecanismo de recurso?
10. Quais evidências da descoberta justificam seguir, estreitar, reformular ou interromper?

## 7. Principais lacunas

### 7.1 Problema e comportamento

- Não há evidência de frequência real de tentativas de troca.
- Não se sabe quando a pessoa prefere vender, doar, guardar ou descartar.
- Não se sabe qual falha é mais relevante: encontrar contraparte, avaliar equivalência, confiar, negociar ou deslocar-se.
- A redação atual parte da solução “marketplace estruturado” antes de comprovar qual problema merece ser resolvido.

### 7.2 Liquidez regional

- As duas RAs, o raio, a densidade e os canais de aquisição ainda não estão definidos.
- Não há massa observada de itens disponíveis nem de desejos compatíveis.
- Não há critério para distinguir interesse unilateral de par de troca possível.
- O efeito “dupla coincidência de desejos” pode tornar a liquidez mais difícil do que em compra e venda.

### 7.3 Público e categorias

- “Pessoas maiores de idade em duas RAs” ainda precisa ser refinado por evidência, embora já permita preparar cotas.
- Existem três agrupamentos candidatos de pesquisa, mas a adequação de cada um ainda precisa de evidência.
- Há exclusões iniciais de risco; a política operacional completa de itens proibidos ainda não existe.
- Pequenos negócios e instituições aparecem como possíveis segmentos futuros, mas não devem contaminar a pesquisa do público inicial.

### 7.4 Confiança, fraude e reputação

- Chat e reputação são mecanismos pretendidos, não evidências de confiança.
- Não há definição de sinais de conta, histórico mínimo ou resistência a contas falsas.
- Reputação pós-troca não ajuda diretamente a primeira troca de um novo usuário.
- Não está definido o que a moderação pode verificar e o que deve apenas encaminhar ou remover.

### 7.5 Segurança presencial

- Não há raio aceitável, necessidade de transporte nem disponibilidade de pontos públicos.
- Não há fluxo para desistência segura, ameaça, coação, item diferente ou não comparecimento.
- Não há regra de exposição de telefone/local nem alternativas para quem não deseja compartilhá-los.
- Orientação de segurança é requisito, mas sua compreensão não foi testada.

### 7.6 Moderação

- Ausência de taxonomia de denúncias, severidade, SLA, escala, recurso e registro de decisão.
- Ausência de estimativa de volume por negociação, usuário ou anúncio.
- Ausência de responsável operacional e cobertura de incidentes críticos.
- Ausência de critério de capacidade para aceitar ou limitar o piloto.

### 7.7 Privacidade e aspectos jurídicos

- Idade mínima, bases/políticas aplicáveis, retenção, exclusão e acesso a mensagens estão pendentes.
- Não há matriz de dados por finalidade, visibilidade e retenção.
- Uma landing page com lista de espera exigirá finalidade, consentimento, retenção e canal de exclusão.
- A descoberta não substitui revisão jurídica antes do piloto real.

### 7.8 Métricas e decisão

- Os critérios da matriz foram aprovados, mas não há baseline nem resultado observado.
- Taxa de cadastro ou opinião positiva isolada não demonstra liquidez nem troca concluída.
- É necessário separar sinais de problema, compreensão, intenção, formação de pares e comportamento real.

## 8. Avaliação das hipóteses H-01 a H-07

| Hipótese | Impacto se falsa | Incerteza atual | Prioridade | Veredito documental |
| --- | --- | --- | --- | --- |
| H-01 — demanda recorrente por troca sem dinheiro | Inviabiliza a tese | Alta | Gate 1 | Não validada; não há evidência comportamental |
| H-02 — liquidez regional suficiente | Inviabiliza marketplace aberto | Muito alta | Gate 1 | Não validada; DF, RA e agrupamentos estão definidos, mas faltam as duas RAs e evidência bilateral |
| H-03 — disposição para cadastrar itens próprios | Pode quebrar o mecanismo de proposta | Alta | Gate 2 | Não validada; o fluxo pressupõe esse comportamento |
| H-04 — reputação e chat aumentam confiança | Pode exigir outro pacote de confiança | Alta | Gate 2 | Não validada; mede-se percepção antes do piloto e efeito real somente depois |
| H-05 — troca presencial é suficiente | Pode inviabilizar a operação sem logística | Alta | Gate 1 | Não validada; faltam raio, mobilidade e segurança |
| H-06 — vários itens por lado são compreensíveis | Pode ampliar desnecessariamente UX e domínio | Alta | Gate 2 | Não validada e descrita de forma inconsistente |
| H-07 — moderação manual suporta o volume inicial | Pode impedir piloto seguro | Muito alta | Gate 1 | Não validada; não há volume, capacidade ou política |

A matriz operacional completa está em `MATRIZ_HIPOTESES_V1.md`.

## 9. Recomendações da auditoria

1. Não homologar o escopo funcional atual como MVP.
2. Manter o produto na Fase 0.
3. Preservar os critérios aprovados e registrar qualquer alteração antes da pesquisa.
4. Começar por comportamento passado, não por opinião sobre a ideia.
5. Escolher duas RAs do Distrito Federal e manter os três agrupamentos candidatos como recorte de descoberta.
6. Testar 1:1 como referência simples antes de justificar 1:N ou N:N.
7. Tratar landing page como teste de intenção e composição de oferta/demanda, não como prova de mercado.
8. Tratar protótipo como teste de compreensão e confiança percebida, não como prova de troca real.
9. Simular moderação com casos sintéticos antes de aceitar usuários reais.
10. Submeter a Bruno somente decisões sustentadas pelas evidências coletadas.

## 10. Gate recomendado para a próxima fase

A Fase 1 só deve ser considerada quando:

- o problema aparecer em comportamentos recentes e repetidos de um segmento identificável;
- uma célula RA × agrupamento demonstrar sinal bilateral de oferta e procura;
- o fluxo mínimo de proposta for compreendido sem assistência relevante;
- o encontro presencial tiver condições práticas e de segurança aceitáveis;
- existir operação mínima de denúncia e moderação compatível com o piloto;
- as dez decisões prioritárias estiverem decididas ou explicitamente adiadas sem bloquear UX;
- critérios de sucesso, alteração e interrupção do piloto estiverem aprovados.

## 11. Limitações

- Auditoria restrita às nove fontes obrigatórias.
- Nenhuma fonte externa ou dado de mercado foi consultado.
- Nenhuma pessoa foi entrevistada.
- Nenhum protótipo ou landing page foi criado ou testado.
- Não houve validação jurídica.
- Os critérios quantitativos aprovados nos demais entregáveis são regras de pré-registro, não resultados nem benchmarks comprovados.

## 12. Confirmação de escopo

Nenhum código, aplicação, identidade visual, schema, migration, API ou infraestrutura foi criado por `EO-DISC-001`. As fontes originais não foram modificadas durante a auditoria. Não houve commit, push, PR, merge, contato externo ou coleta de dados pessoais naquela etapa.
