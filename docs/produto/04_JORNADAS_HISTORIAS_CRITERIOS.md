# Jornadas, histórias e critérios de aceite

**Versão:** 0.1  
**Status:** backlog funcional inicial; requer refinamento

## 1. Personas hipotéticas

Estas personas orientam a descoberta; não substituem pesquisa com usuários.

### Pessoa que quer desapegar

Possui itens utilizáveis, não quer vender ou descartar e procura algo útil em troca. Precisa publicar rapidamente e receber propostas compreensíveis.

### Pessoa que procura um item

Busca uma categoria ou item específico e quer descobrir o que pode oferecer ao anunciante. Precisa filtrar por região e negociar sem expor dados pessoais cedo demais.

### Moderador

Precisa analisar denúncias com contexto suficiente, agir de forma consistente e manter rastreabilidade.

## 2. Jornada principal

### Publicar

1. Usuário cria conta.
2. Completa o perfil mínimo.
3. Cria anúncio em rascunho.
4. Adiciona informações e fotos.
5. Informa preferências de troca.
6. Publica.

Resultado esperado: anúncio ativo, pesquisável e sem exposição de localização exata.

### Encontrar e propor

1. Usuário pesquisa ou filtra anúncios.
2. Abre um anúncio.
3. Seleciona um ou mais itens próprios elegíveis.
4. Revê a composição.
5. Envia proposta com mensagem.

Resultado esperado: proposta versionada, notificável e visível apenas às partes autorizadas.

### Negociar

1. Dono recebe e consulta a proposta.
2. Aceita, rejeita ou faz contraproposta.
3. Participantes conversam dentro da negociação.
4. Uma revisão é aceita.

Resultado esperado: todos os itens envolvidos ficam reservados atomicamente e a versão aceita permanece registrada.

### Concluir

1. Participantes combinam o encontro.
2. Cada parte inspeciona o item.
3. Confirmam a conclusão ou informam problema.
4. Avaliam a contraparte.

Resultado esperado: itens trocados, reputação atualizada e histórico protegido.

## 3. Épicos e histórias prioritárias

### E-01 — Conta e acesso

**US-001 — Criar conta**  
Como visitante, quero criar uma conta para publicar e negociar itens.

Critérios de aceite:

- campos obrigatórios são validados no cliente e no servidor;
- credencial nunca é armazenada em texto puro;
- e-mail ou canal adotado não pode duplicar outra conta ativa;
- erro não revela informações desnecessárias;
- consentimentos aplicáveis ficam registrados.

**US-002 — Entrar e sair**  
Como usuário, quero iniciar e encerrar uma sessão com segurança.

Critérios de aceite:

- credenciais inválidas não autenticam;
- sessão expirada não autoriza operação;
- logout invalida ou encerra a sessão conforme estratégia aprovada;
- tentativa excessiva recebe proteção definida.

**US-003 — Recuperar acesso**  
Como usuário, quero recuperar minha conta sem depender de um administrador.

Critérios de aceite:

- token é temporário, de uso único e não aparece em logs;
- resposta não confirma existência de conta indevidamente;
- redefinição invalida sessões conforme decisão de segurança.

### E-02 — Anúncios

**US-010 — Criar rascunho**  
Como usuário, quero salvar um anúncio incompleto e terminá-lo depois.

Critérios de aceite:

- rascunho não aparece publicamente;
- somente o dono e perfis administrativos autorizados podem acessá-lo;
- salvamento parcial não contorna validações da publicação.

**US-011 — Publicar anúncio**  
Como usuário, quero publicar um item para receber propostas.

Critérios de aceite:

- todos os campos mínimos são obrigatórios;
- pelo menos uma imagem válida está associada;
- estado inicial público é `ACTIVE`;
- localização exibida é aproximada;
- tentativa com categoria ou conteúdo proibido segue a política definida.

**US-012 — Pausar anúncio**  
Como anunciante, quero interromper novas propostas sem perder o cadastro.

Critérios de aceite:

- anúncio pausado sai da descoberta pública;
- proposta aceita não pode ser invalidada por pausa indevida;
- reativação valida novamente a elegibilidade.

### E-03 — Descoberta

**US-020 — Buscar anúncios**  
Como usuário, quero buscar por texto para encontrar itens relevantes.

Critérios de aceite:

- somente anúncios públicos elegíveis são retornados;
- resultado é paginado;
- consulta vazia segue comportamento definido;
- dados privados do anunciante não são expostos.

**US-021 — Filtrar anúncios**  
Como usuário, quero filtrar por categoria, conservação e região aproximada.

Critérios de aceite:

- filtros podem ser combinados;
- URL ou estado de navegação permite retornar ao resultado;
- nenhum filtro permite inferir endereço exato.

### E-04 — Propostas e contrapropostas

**US-030 — Enviar proposta**  
Como usuário, quero oferecer itens meus por um anúncio de outra pessoa.

Critérios de aceite:

- usuário não propõe ao próprio anúncio;
- todos os anúncios são revalidados no servidor;
- proposta registra a composição e mensagem originais;
- repetição idempotente não cria duplicação indevida.

**US-031 — Fazer contraproposta**  
Como participante, quero alterar a composição da troca sem apagar o histórico.

Critérios de aceite:

- nova revisão aponta para a proposta;
- revisão anterior permanece imutável;
- somente a parte que deve responder pode aceitar;
- itens da nova composição são revalidados.

**US-032 — Aceitar proposta**  
Como participante, quero aceitar uma versão específica da negociação.

Critérios de aceite:

- somente a revisão atual pode ser aceita;
- disponibilidade e propriedade são revalidadas;
- aceite e reservas ocorrem na mesma transação;
- falha em um item desfaz toda a operação;
- propostas concorrentes recebem o tratamento aprovado.

### E-05 — Conversa e notificação

**US-040 — Conversar na negociação**  
Como participante, quero conversar sem sair do contexto da proposta.

Critérios de aceite:

- somente participantes autorizados acessam as mensagens;
- mensagens ficam ordenadas e vinculadas à negociação;
- conteúdo pode ser denunciado;
- informações sensíveis recebem controles definidos.

**US-041 — Receber aviso relevante**  
Como usuário, quero ser avisado sobre mudança em uma proposta.

Critérios de aceite:

- eventos não geram notificações duplicadas indevidas;
- preferências do usuário são respeitadas;
- falha de notificação não reverte a transação de negócio;
- dados sensíveis não aparecem em canal inadequado.

### E-06 — Conclusão e reputação

**US-050 — Confirmar troca**  
Como participante, quero registrar que a troca ocorreu.

Critérios de aceite:

- somente participantes podem confirmar;
- confirmação é idempotente;
- estado final segue a regra de confirmação aprovada;
- itens envolvidos recebem estado coerente.

**US-051 — Avaliar contraparte**  
Como participante, quero avaliar a experiência após a troca.

Critérios de aceite:

- avaliação só é permitida após a condição definida;
- existe uma avaliação por autor e negociação;
- autor não avalia a si mesmo;
- abuso pode ser denunciado e moderado.

### E-07 — Segurança e moderação

**US-060 — Denunciar conteúdo ou conduta**  
Como usuário, quero denunciar uma situação inadequada.

Critérios de aceite:

- denúncia exige categoria e contexto mínimo;
- denunciante não acessa dados internos da análise;
- moderação recebe evidência e referência corretas;
- operação é auditada.

**US-061 — Moderar denúncia**  
Como moderador, quero analisar e registrar uma decisão.

Critérios de aceite:

- acesso depende de permissão;
- ação exige motivo;
- histórico não pode ser apagado silenciosamente;
- usuário afetado recebe comunicação conforme política;
- sanções críticas permitem revisão administrativa.

## 4. Cenários transversais obrigatórios

Cada história deve considerar, quando aplicável:

- sucesso;
- dados vazios, ausentes e limites;
- recurso inexistente;
- usuário não autenticado;
- usuário autenticado sem permissão;
- concorrência e repetição da requisição;
- recurso alterado entre leitura e gravação;
- alto volume;
- falha de serviço externo;
- auditoria;
- acessibilidade;
- responsividade móvel.

## 5. Definition of Ready

Uma história está pronta para implementação quando:

- objetivo e valor estão claros;
- regra correspondente está identificada;
- critérios são observáveis;
- dependências e não escopo estão registrados;
- interface ou contrato necessário está definido;
- impacto em dados e segurança foi avaliado;
- dúvidas bloqueadoras foram decididas.

## 6. Definition of Done

Uma história está concluída quando:

- critérios de aceite estão atendidos;
- código relevante foi revisado;
- testes aplicáveis foram criados e passaram;
- lint, typecheck e build passaram;
- segurança e autorização foram verificadas;
- documentação e contrato foram atualizados;
- migration, quando autorizada, foi validada em ambiente limpo;
- não há erro conhecido ocultado;
- relatório traz evidências reproduzíveis;
- Bruno aprovou os gates que exigem decisão humana.
