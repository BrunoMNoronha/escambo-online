# Escopo do MVP e regras de negócio

**Versão:** 0.1  
**Status:** proposta para validação  
**Dependência:** [02_FONTE_MESTRA_PRODUTO.md](02_FONTE_MESTRA_PRODUTO.md)

## 0. Recorte aprovado para a descoberta

Bruno aprovou em 29/07/2026 (`DISC-001` a `DISC-003`, ver [Registro de decisões](../governanca/REGISTRO_DECISOES.md)) o recorte abaixo **para a etapa de descoberta**. Ele delimita a amostra e a coleta; **não** é a política definitiva do MVP, do piloto ou da produção, nem parecer jurídico.

**Fronteira da tese:** troca exclusivamente de bens, **sem complemento financeiro** (`DISC-001`).

**Público:** pessoas com 18 anos ou mais; residentes no Cruzeiro ou no Guará; com pelo menos um item usado, em bom estado e sem uso recorrente; com interesse real em avaliar troca por outro bem; com disponibilidade para considerar encontro presencial em local público; sem depender de complemento financeiro para participar da tese testada.

**Categorias candidatas:**

1. livros, quadrinhos, jogos de tabuleiro e jogos eletrônicos em mídia física;
2. artigos de hobby, esporte e lazer de baixo ou médio valor;
3. pequenos itens para casa, decoração e organização, desde que transportáveis e passíveis de inspeção presencial.

**Exclusões imediatas da descoberta:** dinheiro, PIX, créditos, vales, cartões-presente ou complemento financeiro; serviços, trabalho ou promessa de prestação futura; armas, munições, explosivos e objetos perigosos; drogas, medicamentos, álcool, tabaco e substâncias controladas; alimentos, bebidas e produtos perecíveis; animais; veículos, imóveis e itens que dependam de transferência formal; documentos pessoais, contas, credenciais ou dados de acesso; produtos ilícitos, falsificados, furtados ou de procedência incerta; itens íntimos, de higiene pessoal ou com risco sanitário; itens sujeitos a licença, prescrição, autorização ou regulação específica; eletrônicos de alto valor ou cuja condição, autenticidade ou funcionamento sejam difíceis de verificar; joias, metais preciosos e objetos de alto risco de fraude; itens com defeitos graves não informados; qualquer item com risco relevante à integridade física, privacidade ou segurança dos participantes.

As categorias finais e a política de itens proibidos para piloto e produção, a elegibilidade futura e a revisão jurídica continuam pendentes.

## 1. Atores

| Ator | Responsabilidade |
| --- | --- |
| Visitante | Consultar anúncios públicos e iniciar cadastro |
| Usuário | Publicar itens, negociar, conversar, concluir e avaliar trocas |
| Moderador | Analisar denúncias e aplicar ações permitidas |
| Administrador | Gerenciar categorias, políticas, perfis administrativos e auditoria |

## 2. Capacidades do MVP proposto

### Conta e perfil

- cadastro e autenticação;
- confirmação do canal principal de acesso;
- recuperação de conta;
- nome público, foto opcional e região aproximada;
- bloqueio de outro usuário;
- desativação da própria conta, conforme política de retenção.

### Anúncio

- criar e editar rascunho;
- publicar com dados mínimos;
- anexar e ordenar fotos;
- pausar, reativar e remover;
- definir categoria e estado de conservação;
- descrever itens ou categorias de interesse;
- consultar situação e histórico essencial.

### Descoberta

- listagem paginada;
- busca textual;
- filtro por categoria, região aproximada e conservação;
- visualização do anúncio e do perfil público do anunciante.

### Negociação

- selecionar o anúncio desejado;
- oferecer um ou mais anúncios próprios elegíveis;
- incluir uma mensagem inicial;
- aceitar, rejeitar, cancelar ou fazer contraproposta;
- manter histórico imutável das revisões;
- conversar no contexto da negociação;
- reservar os itens em uma operação atômica após o aceite.

### Conclusão e confiança

- cada participante confirma a conclusão;
- avaliar a contraparte uma vez;
- denunciar anúncio, usuário, negociação ou mensagem;
- consultar situação das próprias denúncias, quando permitido pela política.

### Administração mínima

- consultar fila de denúncias;
- ocultar anúncio;
- suspender ou reativar conta;
- registrar motivo de toda ação;
- consultar eventos críticos de auditoria;
- manter categorias permitidas.

## 3. Estados propostos

### Anúncio

| Estado | Significado |
| --- | --- |
| `DRAFT` | Ainda não está visível |
| `ACTIVE` | Publicado e disponível para propostas |
| `RESERVED` | Vinculado a uma proposta aceita |
| `TRADED` | Troca concluída |
| `PAUSED` | Oculto temporariamente pelo dono |
| `REMOVED` | Removido pelo dono ou pela moderação |

Transições fora do fluxo definido devem ser rejeitadas pelo backend.

### Proposta de troca

| Estado | Significado |
| --- | --- |
| `SENT` | Enviada e aguardando resposta |
| `COUNTERED` | Nova revisão apresentada e aguardando resposta da outra parte |
| `ACCEPTED` | Acordo aceito e itens reservados |
| `REJECTED` | Recusada |
| `CANCELLED` | Cancelada por participante autorizado |
| `EXPIRED` | Encerrada por prazo |
| `COMPLETED` | Conclusão confirmada conforme regra vigente |
| `DISPUTED` | Um participante informou problema após aceite |

O prazo de expiração e a regra de conclusão unilateral são decisões pendentes.

## 4. Regras e invariantes

### Usuário e conta

1. Um usuário não pode negociar consigo mesmo.
2. Contas suspensas não podem publicar, enviar mensagens ou alterar negociações.
3. Operações sensíveis exigem autenticação válida e autorização no backend.
4. A elegibilidade etária inicial é uma hipótese a ser validada juridicamente.

### Anúncios

1. Somente o proprietário pode editar, pausar ou remover o anúncio, salvo ação administrativa autorizada.
2. Um anúncio público precisa de título, descrição, categoria, estado de conservação, região aproximada e ao menos uma imagem válida.
3. Localização residencial exata não pode aparecer publicamente.
4. Anúncios reservados ou trocados não aceitam nova proposta.
5. Itens proibidos pela política não podem ser publicados.
6. Exclusão física de anúncio com histórico de negociação não é permitida; usar remoção lógica e retenção controlada.

### Propostas

1. O alvo e todos os itens oferecidos devem estar ativos no momento do envio.
2. Todos os itens oferecidos precisam pertencer ao proponente.
3. Uma contraproposta cria nova revisão; não sobrescreve o acordo anterior.
4. Apenas a revisão atual pode ser aceita.
5. O aceite deve validar novamente disponibilidade e propriedade.
6. O aceite e a reserva de todos os itens ocorrem na mesma transação.
7. Se qualquer item estiver indisponível, nenhum item deve ser reservado.
8. Um anúncio não pode participar simultaneamente de duas propostas aceitas.
9. Propostas concorrentes afetadas por uma reserva devem ser encerradas ou invalidadas conforme política explícita.
10. Complemento financeiro não faz parte do MVP proposto.

### Chat

1. O chat existe somente entre participantes de uma negociação.
2. Mensagens não podem ser alteradas silenciosamente.
3. Bloqueio, denúncia, retenção e eventual exclusão devem respeitar a política do produto.
4. Telefones, endereços e outros dados sensíveis devem receber tratamento de privacidade e prevenção de abuso.
5. A administração só acessa conteúdo privado dentro de hipótese e permissão formalmente definidas.

### Conclusão, reputação e disputa

1. A avaliação só pode ocorrer após a condição definida para conclusão.
2. Cada participante avalia a outra parte uma única vez por troca.
3. A avaliação não pode ser editada livremente após publicada.
4. Um usuário não avalia a si próprio.
5. Denúncias e sanções registram motivo, autor administrativo e timestamp.
6. A plataforma não pode afirmar que verificou autenticidade, propriedade ou segurança de um item sem processo real que sustente essa afirmação.

## 5. Políticas mínimas antes do lançamento

- itens proibidos;
- conteúdo e comportamento aceitáveis;
- privacidade e retenção;
- denúncias e recursos;
- segurança em encontros;
- contas, suspensão e encerramento;
- avaliações;
- termos de uso;
- resposta a incidentes.

Os textos finais dessas políticas exigem revisão jurídica adequada antes de produção.

## 6. Critério macro de aceite do MVP proposto

O MVP proposto só estará funcionalmente completo quando um usuário puder:

1. criar uma conta;
2. publicar um item;
3. encontrar um item de outra pessoa;
4. enviar proposta com item próprio;
5. negociar e aceitar uma versão explícita;
6. ter todos os itens reservados de modo consistente;
7. conversar com a contraparte;
8. registrar a conclusão;
9. avaliar ou denunciar;
10. ter as operações críticas protegidas, testadas e auditáveis.

## 7. Decisões pendentes com impacto de escopo

O recorte de **descoberta** (região, público e categorias candidatas) foi decidido em `DISC-002`/`DISC-003` (ver seção 0). As pendências abaixo referem-se ao **piloto e à produção**:

- região e público do piloto (o recorte de descoberta não os define);
- idade mínima;
- uma ou várias unidades por lado da troca;
- momento de abertura do chat;
- prazo de expiração;
- regra de conclusão quando apenas uma parte confirma;
- tratamento de proposta concorrente;
- compartilhamento de contato e local após aceite;
- categorias e itens proibidos definitivos;
- necessidade de verificação de identidade;
- política de disputa;
- modelo de negócio futuro.
