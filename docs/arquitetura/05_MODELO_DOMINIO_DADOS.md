# Modelo conceitual de domínio e dados

**Versão:** 0.1  
**Status:** conceitual; não autoriza criação de schema ou migration

## 1. Objetivo

Definir linguagem comum, responsabilidades e invariantes antes da modelagem física. Nomes, campos e cardinalidades podem mudar por ADR e aprovação.

## 2. Agregados principais

### Identidade e acesso

| Entidade | Responsabilidade |
| --- | --- |
| `User` | Identidade, estado da conta e referências de segurança |
| `Profile` | Nome público, foto, biografia curta e região aproximada |
| `Session` | Sessão ou dispositivo autenticado |
| `Role` / `Permission` | Autorizações administrativas |
| `UserBlock` | Bloqueio entre usuários |
| `ConsentRecord` | Evidência de consentimento ou aceite de política, quando aplicável |

### Catálogo e anúncio

| Entidade | Responsabilidade |
| --- | --- |
| `Category` | Taxonomia administrável |
| `Listing` | Item anunciado, proprietário, descrição, conservação e estado |
| `ListingImage` | Metadados e ordem das imagens |
| `ExchangePreference` | Texto, categorias ou itens desejados |
| `ApproximateLocation` | Região pública sem endereço residencial exato |
| `ListingStatusHistory` | Mudanças relevantes de estado |

### Negociação

| Entidade | Responsabilidade |
| --- | --- |
| `TradeProposal` | Negociação entre duas partes e estado atual |
| `ProposalRevision` | Versão imutável da composição proposta |
| `ProposalItem` | Anúncio presente em um lado de uma revisão |
| `ListingReservation` | Reserva exclusiva criada no aceite |
| `TradeConfirmation` | Confirmação de conclusão por participante |
| `Dispute` | Problema informado após o aceite |

### Comunicação e confiança

| Entidade | Responsabilidade |
| --- | --- |
| `Conversation` | Canal vinculado a uma negociação |
| `Message` | Conteúdo, autor e estado de moderação |
| `Notification` | Evento destinado ao usuário e status de entrega |
| `Rating` | Avaliação de uma parte pela outra |
| `Report` | Denúncia contra alvo permitido |
| `ModerationAction` | Decisão administrativa motivada |
| `AuditEvent` | Evento crítico para rastreabilidade |

## 3. Relações conceituais

- Um `User` possui um `Profile` e vários `Listing`.
- Um `Listing` pertence a uma `Category` e possui imagens.
- Um `TradeProposal` tem dois participantes e várias `ProposalRevision`.
- Cada `ProposalRevision` possui um ou mais `ProposalItem` em cada lado, se o modelo N:N for aprovado.
- Uma revisão aceita cria reservas para todos os anúncios envolvidos.
- Uma negociação possui no máximo uma `Conversation`.
- Uma negociação pode gerar confirmações, avaliações, denúncia e disputa.
- Uma ação de moderação aponta para o alvo e para o moderador responsável.

## 4. Invariantes de dados

1. Identificadores são imutáveis.
2. Datas de negócio usam timezone explícito e persistência padronizada.
3. Estados usam enum ou equivalente controlado, nunca texto livre.
4. Revisões de proposta aceitas não são editadas.
5. Reserva ativa é exclusiva por anúncio.
6. Relações de propriedade são validadas no servidor.
7. Avaliação possui unicidade por negociação, autor e avaliado.
8. Ação administrativa crítica exige motivo e auditoria.
9. Remoção lógica preserva referências exigidas pelo histórico.
10. Dados públicos e privados devem estar claramente separados nos contratos.

## 5. Concorrência e consistência

O aceite é o ponto de maior risco transacional. A implementação deve:

- iniciar transação;
- bloquear ou validar todos os anúncios participantes;
- confirmar propriedade e estado;
- impedir reserva concorrente;
- criar todas as reservas;
- atualizar proposta e anúncios;
- registrar evento de auditoria;
- confirmar a transação;
- disparar notificações fora do núcleo transacional, de forma confiável.

O mecanismo exato de locking e idempotência depende do banco e do ORM aprovados.

## 6. Dados sensíveis

Tratar como sensíveis, no mínimo:

- e-mail, telefone e credenciais;
- localização precisa;
- mensagens privadas;
- tokens e sessões;
- dados técnicos que permitam rastreamento indevido;
- denúncias, sanções e evidências;
- registros de recuperação de conta.

Evitar coletar CPF, documento, endereço completo ou biometria sem necessidade formalmente demonstrada e revisão de impacto.

## 7. Retenção e exclusão

Antes da produção, definir por categoria:

| Categoria | Decisão necessária |
| --- | --- |
| Conta e perfil | prazo após desativação |
| Anúncios e imagens | remoção pública e retenção técnica |
| Propostas e revisões | histórico mínimo necessário |
| Mensagens | prazo, acesso administrativo e exclusão |
| Auditoria | prazo e proteção contra alteração |
| Denúncias | prazo e acesso restrito |
| Sessões e logs | prazo operacional e de segurança |

Exclusão do usuário não pode corromper o histórico de uma troca. Aplicar anonimização ou retenção justificada conforme política aprovada.

## 8. Migrações

- Toda alteração de schema exige decisão explícita no prompt.
- O agente deve apresentar impacto, compatibilidade, rollback e plano de dados.
- Migration não pode ser criada nem executada sem autorização de Bruno.
- Mudanças destrutivas exigem backup e ensaio de restauração quando houver dados relevantes.

## 9. Próximo artefato técnico

Após aprovação do MVP e da arquitetura, gerar:

- diagrama de contexto;
- modelo entidade-relacionamento;
- catálogo de campos;
- matriz dado × finalidade × visibilidade × retenção;
- estratégia de índices;
- plano de migration inicial.
