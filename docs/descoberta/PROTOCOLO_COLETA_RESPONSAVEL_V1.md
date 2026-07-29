# EO-DISC-005 — Protocolo de coleta responsável V1

**Projeto:** Escambo Online

**Versão:** 1.0

**Data-base:** 29/07/2026

**Responsável final:** Bruno

**Status:** regras aprovadas por Bruno (`DISC-005` a `DISC-014`); instrumentos operacionais (roteiro, folha de informação e ficha) **ainda não congelados**; **nenhum contato, recrutamento, entrevista ou coleta autorizado**

> Este protocolo consolida as decisões de coleta responsável aprovadas em 29/07/2026 e registradas em [Registro de decisões](../governanca/REGISTRO_DECISOES.md) como `DISC-005` a `DISC-014`. Ele **não** autoriza contato com participantes, **não** aprova o roteiro de entrevistas e **não** declara conformidade jurídica. A autorização para iniciar contato é um gate separado (ver seção 11).

## 0. Escopo e limites

- Aplica-se ao **primeiro ciclo de entrevistas de descoberta** (etapa D1 do [Plano de descoberta V1](PLANO_DESCOBERTA_V1.md)), com adultos, dentro do recorte congelado de `DISC-002`/`DISC-003`.
- **Não** cobre protótipo (D3), landing page (D4) nem piloto — cada um terá regras próprias no seu gate.
- As recomendações de retenção e descarte são **proposta operacional conservadora**, não obrigação legal; a avaliação jurídica permanece questão aberta futura, já reservada por [07 — Qualidade, segurança e privacidade](../qualidade/07_QUALIDADE_SEGURANCA_PRIVACIDADE.md) §9 para o piloto.
- Em divergência entre documentos, vale a hierarquia de verdade do [README.md](../../README.md); a fonte primária das decisões é o [Registro de decisões](../governanca/REGISTRO_DECISOES.md).
- Nenhum dado pessoal real, credencial ou segredo pode ser inserido neste ou em qualquer documento, prompt, log ou relatório.

## 1. Princípios

1. Coletar o mínimo necessário; nunca endereço residencial exato, documento, CPF ou item ilícito.
2. Separar dado de contato, registro de consentimento e notas de conteúdo.
3. Preferir a opção mais simples, reversível e de menor exposição.
4. Registrar fato, fala, observação e interpretação em campos distintos.
5. Nenhuma hipótese é validada ou alterada pela coleta; `DISC-001` a `DISC-004` e os critérios congelados de `H-01` a `H-07` permanecem intactos.

## 2. Recrutamento — critérios e canais (`DISC-005`)

### 2.1 Critérios de elegibilidade

Mantêm-se os critérios congelados do recorte de descoberta (`DISC-003`; ver [recorte](../produto/03_ESCOPO_MVP_REGRAS_NEGOCIO.md) §0 e [Plano](PLANO_DESCOBERTA_V1.md) §4.1). Acrescenta-se:

- **Critério obrigatório adicional:** ter **decidido ou considerado o destino de um item** (vender, doar, guardar, descartar ou trocar) **nos últimos 12 meses**.
- **Acesso a smartphone:** registrado apenas como **característica de perfil** para diversidade da amostra — **não** é critério de elegibilidade e **não** exclui ninguém.

### 2.2 Canais permitidos

- indicação pessoal;
- grupos comunitários e associações locais do Cruzeiro/DF e do Guará/DF, **somente com autorização do responsável ou administrador** do canal e respeitando as regras do grupo;
- divulgação física (ex.: cartaz de pesquisa) em locais **autorizados**.

### 2.3 Canais e práticas proibidos

- raspagem (scraping) ou compra de listas de contatos;
- mensagens em massa não solicitadas (spam);
- anúncios pagos sem orçamento previamente aprovado por Bruno;
- qualquer abordagem a menores de idade;
- uso de dados de terceiros sem consentimento.

### 2.4 Texto de abordagem inicial — pendência bloqueante

O **texto de abordagem inicial** de recrutamento **ainda precisa ser preparado e aprovado por Bruno antes de qualquer contato**. Este protocolo **não** redige a mensagem de abordagem; fazê-lo exige **nova decisão de Bruno**.

## 3. Consentimento e informação (`DISC-006`)

- Consentimento **verbal**, obtido antes de qualquer registro, sem assinatura, CPF ou documento.
- Registro do consentimento por **marcação (checkbox) na ficha da sessão**, associado ao código do participante.
- Antes do consentimento, apresentar a **folha de informação** (modelo na seção 3.1).
- **Sem incentivo** como padrão; qualquer incentivo futuro exige **aprovação separada** de Bruno.
- O participante **recebe o seu código de pesquisa** para eventual solicitação de exclusão (ver seção 9).

> **Pendência bloqueante — canal de contato/exclusão:** o canal operacional pelo qual o participante tira dúvidas e solicita exclusão **ainda não está definido**. Defini-lo é **pré-requisito para a aprovação do roteiro** (seção 10) e para qualquer contato (seção 11). Este protocolo **não** escolhe o canal; a escolha exige **nova decisão de Bruno**.

### 3.1 Modelo de folha de informação (texto operacional, não jurídico)

> Estamos pesquisando como as pessoas decidem o que fazer com bens que não usam mais. A participação é **voluntária**: você pode não responder ou encerrar a qualquer momento, sem prejuízo. Faremos apenas **anotações** — sem áudio e sem vídeo. Não preciso de endereço, documento, nome de outras pessoas ou detalhes sensíveis. Suas respostas serão usadas de forma **agrupada e sem identificação**. As anotações são guardadas por prazo limitado e depois descartadas. Você receberá um **código** e pode pedir a exclusão dos seus dados usando esse código pelo canal informado. Contato para dúvidas ou exclusão: _[canal pendente de decisão de Bruno — ver pendência bloqueante acima]_.

## 4. Registro da coleta (`DISC-007`)

- O **primeiro ciclo** é registrado **somente por notas** — **sem áudio e sem vídeo**.
- Gravação só poderá ser **reconsiderada** em decisão específica posterior, com consentimento próprio e política de retenção própria, e apenas se as notas se mostrarem insuficientes.
- A ficha da sessão registra o consentimento e usa apenas o **código** do participante (ver seção 5).

## 5. Pseudonimização e dados de contato (`DISC-008`)

- **Pseudonimização temporária:** cada participante recebe um **código** (exemplo de formato: `P-CRU-01`, `P-GUA-01`), sem significado identificável.
- As **notas contêm somente o código** — nunca nome, telefone ou endereço.
- Uma **tabela `contato ↔ código`** é mantida **separada** das notas, com **acesso exclusivo de Bruno**.
- A tabela de correspondência é **eliminada junto com os contatos** (ver seção 8), restando nas notas apenas o código sem chave de reidentificação.

## 6. Armazenamento e acesso (`DISC-009`)

- Armazenamento em **pasta dedicada no Google Drive privado de Bruno**.
- Conta protegida por **autenticação em dois fatores (MFA)**.
- **Sem** link público e **sem** compartilhamento externo.
- **Notas e contatos** em arquivos ou pastas **separados**.
- **Acesso inicial exclusivo de Bruno.**
- **Nenhuma** nota de pesquisa versionada no GitHub.
- **Nenhum** arquivo bruto enviado a agentes de IA (ver seção 7).
- **Sem** sincronização automática com ferramenta adicional.

## 7. Uso de agentes de IA (`DISC-010`)

- Agentes de IA só podem analisar conteúdo **previamente revisado e desidentificado por Bruno**.
- A desidentificação deve remover: nomes e contatos; locais específicos; datas exatas desnecessárias; nomes de terceiros; histórias ou combinações raras que permitam reconhecer a pessoa; citações literais potencialmente identificáveis.
- **Notas brutas e listas de contato não podem ser enviadas a IA** — coerente com [09 — Governança de IA e GitHub](../governanca/09_GOVERNANCA_IA_GITHUB.md) §13 (`GOV-008`).

## 8. Retenção e descarte (`DISC-011`)

Prazos objetivos por categoria (proposta operacional conservadora):

| Categoria | Prazo de retenção |
| --- | --- |
| Contatos e chave `contato ↔ código` | até **30 dias** após a última entrevista do ciclo |
| Notas brutas pseudonimizadas | descarte no **evento que ocorrer primeiro**: **90 dias** após a decisão final da etapa D6 **ou** **12 meses** após a entrevista |
| Registro do consentimento | mesmo prazo da respectiva nota |
| Sínteses agregadas e desidentificadas | podem permanecer na documentação do projeto |
| Áudio e vídeo | **não aplicável** no primeiro ciclo |

O **descarte** deve cobrir: arquivo principal; lixeira do serviço; cópias locais; exportações e duplicações controladas por Bruno.

## 9. Desistência, exclusão e incidentes (`DISC-012`)

### 9.1 Desistência e exclusão

- O participante recebe o seu **código** e pode solicitar exclusão **enquanto a nota bruta existir**.
- A exclusão é concluída em **até 7 dias corridos** mediante o código.
- Registra-se **somente a execução** da exclusão, **sem preservar o conteúdo eliminado**.

### 9.2 Incidente de privacidade ou coleta indevida

1. interromper a coleta ou o processamento;
2. isolar o material;
3. **não** enviar o dado ao GitHub ou a agentes de IA;
4. registrar um **incidente mínimo**, sem copiar o dado exposto;
5. comunicar Bruno **no mesmo dia**;
6. decidir posteriormente sobre comunicação ao participante e apoio jurídico, conforme a gravidade.

## 10. Aprovação do roteiro (`DISC-013`)

- O [Roteiro de entrevistas V1](ROTEIRO_ENTREVISTAS_V1.md) **não** é aprovado nesta etapa; permanece oficialmente como **proposta**.
- **Pré-requisitos bloqueantes para a aprovação:** o **canal de contato/exclusão** (seção 3) e o **texto de abordagem inicial** (seção 2.4) precisam estar definidos e aprovados por Bruno antes de o roteiro ser aprovado.
- Sequência aprovada (`DISC-013`): (1) registrar estas regras — feito; (2) executar a etapa documental — feito; (3) incorporar consentimento, código, exclusão e registro somente por notas ao roteiro — feito nesta etapa; (4) **auditar o diff**; (5) definir canal e abordagem; (6) só então Bruno aprova a versão resultante.

## 11. Autorização de contato (`DISC-014`)

**Nenhum contato, recrutamento ou entrevista está autorizado.** A autorização dependerá de:

1. decisões registradas;
2. protocolo criado;
3. roteiro atualizado;
4. documentos sincronizados;
5. revisão final concluída;
6. simulação interna do fluxo com **dados fictícios**.

## 12. Rastreabilidade decisão ↔ documento

| Decisão | Tema | Seção deste protocolo |
| --- | --- | --- |
| `DISC-005` | Recrutamento — critérios e canais | 2 |
| `DISC-006` | Consentimento e informação | 3 |
| `DISC-007` | Registro por notas | 4 |
| `DISC-008` | Pseudonimização e contatos | 5 |
| `DISC-009` | Armazenamento e acesso | 6 |
| `DISC-010` | Uso de agentes de IA | 7 |
| `DISC-011` | Retenção e descarte | 8 |
| `DISC-012` | Desistência, exclusão e incidentes | 9 |
| `DISC-013` | Aprovação do roteiro | 10 |
| `DISC-014` | Autorização de contato | 11 |

## 13. Condição para alterar este protocolo

Uma alteração relevante exige: proposta explícita; motivo; impacto na coleta e na privacidade; **nova decisão de Bruno**; e atualização dos documentos dependentes ([Plano](PLANO_DESCOBERTA_V1.md), [Roteiro](ROTEIRO_ENTREVISTAS_V1.md), [07 — Qualidade](../qualidade/07_QUALIDADE_SEGURANCA_PRIVACIDADE.md) e [Estado atual](../governanca/11_ESTADO_ATUAL_PROJETO.md)). Recomendações não se tornam decisão por estarem aqui.
