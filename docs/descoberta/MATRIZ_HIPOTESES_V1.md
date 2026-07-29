# EO-DISC-001 — Matriz de hipóteses V1

**Projeto:** Escambo Online

**Data-base:** 29/07/2026

**Status:** pré-registro proposto; nenhuma hipótese validada

## 1. Como usar

Esta matriz distingue o estado documental da evidência futura.

- **Manter:** preservar a hipótese no MVP proposto e avançar para o próximo teste.
- **Alterar:** restringir público, região, categoria ou fluxo; uma hipótese alterada volta a ser testada.
- **Rejeitar:** retirar a hipótese do MVP ou impedir avanço enquanto não houver alternativa segura.

Os limiares numéricos são critérios de decisão sugeridos para aprovação de Bruno antes da pesquisa. Não são resultados, benchmarks de mercado ou garantia estatística.

## 2. Priorização

| Ordem | Hipótese | Impacto | Incerteza | Classe |
| ---: | --- | --- | --- | --- |
| 1 | H-01 — demanda recorrente por troca sem dinheiro | Crítico | Alta | Gate de tese |
| 2 | H-02 — liquidez regional suficiente | Crítico | Muito alta | Gate de marketplace |
| 3 | H-05 — encontro presencial suficiente | Crítico | Alta | Gate operacional e de segurança |
| 4 | H-07 — moderação manual suficiente | Crítico | Muito alta | Gate de piloto |
| 5 | H-03 — cadastro de item próprio é aceitável | Alto | Alta | Gate de mecanismo |
| 6 | H-06 — vários itens por lado são compreensíveis | Alto | Alta | Gate de complexidade |
| 7 | H-04 — reputação e chat aumentam confiança | Alto | Alta | Gate de confiança |

`H-04` aparece por último na ordem de teste decisório porque o efeito comportamental real de reputação exige uso no piloto. Isso não reduz a importância de segurança, chat e moderação.

## 3. Visão consolidada

| ID | Hipótese | Evidência atual | Método principal | Amostra | Decisão possível |
| --- | --- | --- | --- | --- | --- |
| H-01 | Existe demanda recorrente por troca sem dinheiro | Nenhuma externa | Entrevistas + landing | 24 entrevistas + tráfego pré-registrado | manter, nichar ou rejeitar tese |
| H-02 | Operação regional gera liquidez suficiente | Nenhuma externa | Landing bilateral + matriz de pares | duas regiões candidatas | escolher célula, estreitar ou não lançar marketplace |
| H-03 | Usuário aceita cadastrar item próprio antes de propor | Fluxo apenas documentado | Protótipo | 12 testes | manter cadastro, simplificar ou trocar mecanismo |
| H-04 | Reputação e chat contextual aumentam confiança | Princípio, não evidência | Entrevista + protótipo; piloto depois | 24 + 12 | manter pacote mínimo, alterar momento ou retirar mecanismo ineficaz |
| H-05 | Encontro presencial basta no mercado inicial | Premissa documental | Entrevista + tarefa de encontro | 24 + 12 | manter recorte, reduzir raio ou rejeitar presencial exclusivo |
| H-06 | Um ou mais itens por lado é compreensível | Documentos divergentes | Protótipo 1:1 versus 1:N | 12 testes | 1:1, 1:N ou adiar N:N |
| H-07 | Moderação manual suporta o volume inicial | Nenhuma capacidade definida | Simulação de fila | 40 casos sintéticos, duas rodadas | manter, limitar piloto ou bloquear lançamento |

## 4. H-01 — Demanda recorrente por troca sem dinheiro

### Formulação

**Hipótese:** existe um segmento identificável que tenta trocar bens sem dinheiro com frequência suficiente para justificar um produto dedicado.

### Base atual

- **Fato:** as fontes descrevem problemas plausíveis de busca, confiança, negociação e disponibilidade.
- **Fato:** não há entrevista, dado de comportamento ou sinal de demanda registrado.
- **Inferência:** o documento presume que a troca é desejada; ainda não se sabe se vender, doar, guardar ou descartar resolve melhor.

### Risco se falsa

O produto pode organizar um comportamento raro, de baixo valor ou facilmente substituído.

### Método

1. Entrevistar 24 pessoas nos perfis definidos.
2. Explorar decisões dos últimos 12 meses antes de apresentar a solução.
3. Executar landing page honesta com ação de alto compromisso.
4. Cruzar relato de comportamento, recência, repetição e intenção.

### Evidência favorável

- múltiplas tentativas concretas e recentes;
- repetição do problema em mais de um participante do mesmo segmento;
- perda percebida relevante ao falhar;
- alternativas atuais consideradas inadequadas por razões que a proposta pode atacar;
- ação na landing compatível com o lado “tenho” ou “procuro”.

### Evidência contrária

- troca aparece apenas como ideia simpática;
- pessoas sistematicamente preferem dinheiro, doação ou descarte;
- itens ficam guardados por baixa urgência, não por falta de canal;
- frequência é excepcional;
- CTA recebe curiosidade, mas não registro de oferta/procura.

### Critério

- **Manter:** comportamento recente e recorrente aparece em pelo menos metade dos 12 participantes com experiência de tentativa, em um segmento reconhecível, e o sinal da landing é coerente com esse comportamento.
- **Alterar:** comportamento existe, mas concentra-se em uma categoria, comunidade, ocasião ou região; reformular o público e repetir o teste.
- **Rejeitar:** menos de um terço dos participantes com experiência apresenta recorrência ou dor relevante, e a landing não gera intenção bilateral.

### Limitação

Entrevista e landing validam problema e intenção, não retenção nem troca concluída.

## 5. H-02 — Liquidez regional suficiente

### Formulação

**Hipótese:** dentro de uma região e intervalo de tempo úteis, há oferta e procura compatíveis suficientes para formar trocas.

### Base atual

- **Fato:** nenhuma região, raio ou categoria foi aprovada.
- **Fato:** a troca exige coincidência entre o que cada parte oferece e aceita.
- **Inferência:** esse é o risco estrutural mais específico do marketplace.

### Risco se falsa

Mesmo com muitos interessados, cada pessoa pode não encontrar contraparte compatível.

### Método

1. Escolher duas regiões candidatas e até três agrupamentos de categoria.
2. Coletar na landing: região ampla, “tenho/procuro” e categoria.
3. Construir matriz agregada de oferta e procura.
4. Aplicar regras simples de compatibilidade e raio aceito.
5. Não aproximar pessoas nesta etapa.

### Evidência favorável

- oferta e procura na mesma célula região × categoria;
- desejos não excessivamente específicos;
- raio aceito compatível;
- formação repetida de pares plausíveis;
- uma célula claramente mais densa do que as demais.

### Evidência contrária

- muitas ofertas e quase nenhuma procura, ou o inverso;
- interesses espalhados demais;
- distância inviável;
- pares dependem de complemento financeiro não previsto;
- somente um item excepcional forma par.

### Critério

- **Manter:** formar pelo menos cinco pares plausíveis na mesma região durante o teste e confirmar nas entrevistas que raio e tempo são aceitáveis.
- **Alterar:** pares aparecem apenas em um recorte; reduzir região, categoria ou público e repetir.
- **Rejeitar:** não há bilateralidade mesmo após recorte, ou os pares dependem consistentemente de elemento fora da tese.

### Limitação

Par plausível não é proposta aceita. A hipótese continuará parcialmente aberta até um piloto controlado.

## 6. H-03 — Disposição para cadastrar itens próprios

### Formulação

**Hipótese:** o usuário aceita criar um anúncio próprio com informações mínimas antes de enviar proposta.

### Base atual

- **Fato:** esse passo está embutido nas jornadas e invariantes.
- **Fato:** nenhuma pessoa testou o fluxo.
- **Inferência:** a exigência melhora rastreabilidade, mas aumenta esforço antes do primeiro valor.

### Risco se falsa

Usuários podem abandonar antes de propor, reduzindo ainda mais a liquidez.

### Método

1. Protótipo de baixa fidelidade.
2. Tarefa sem explicação prévia para encontrar item e propor.
3. Observar se a pessoa entende a necessidade do próprio anúncio.
4. Perguntar qual informação considera aceitável e qual evita.

### Evidência favorável

- conclusão sem ajuda;
- compreensão de que o item precisa estar disponível e descrito;
- percepção de benefício para clareza/confiança;
- esforço considerado proporcional;
- ausência de tentativa recorrente de contornar o cadastro.

### Evidência contrária

- abandono;
- tentativa de enviar somente texto/foto no chat;
- resistência a publicar antes de receber interesse;
- confusão sobre visibilidade;
- dados mínimos vistos como excessivos.

### Critério

- **Manter:** pelo menos 9 de 12 participantes concluem e explicam o motivo do cadastro.
- **Alterar:** 6 a 8 concluem; reduzir campos, permitir rascunho rápido ou mudar a ordem, sem remover validações críticas.
- **Rejeitar:** menos de 6 concluem ou a resistência é estrutural; testar outro mecanismo de proposta antes de especificar o MVP.

### Limitação

Protótipo não mede esforço real de fotografar e manter inventário ao longo do tempo.

## 7. H-04 — Reputação e chat contextual aumentam confiança

### Formulação

**Hipótese:** acesso a histórico/reputação e uma conversa vinculada à proposta muda positivamente a decisão de prosseguir sem criar falsa sensação de garantia.

### Base atual

- **Fato:** chat, reputação, denúncia e bloqueio constam no MVP proposto.
- **Fato:** momento do chat e acesso administrativo estão pendentes.
- **Inferência:** esses recursos ajudam contexto, mas não comprovam identidade, propriedade ou autenticidade.

### Risco se falsa

O MVP pode assumir custo e risco de mensagens/moderação sem reduzir abandono ou fraude.

### Método

1. Entrevistas sobre sinais usados em experiências reais.
2. Protótipo com cenários de informação suficiente, insuficiente e conflitante.
3. Observar informação consultada e decisão tomada.
4. Comparar mensagem inicial estruturada, chat após proposta e chat após aceite.
5. Medir efeito real somente no piloto futuro.

### Evidência favorável

- participante consulta espontaneamente histórico contextual;
- altera decisão com base em evidência pertinente;
- entende limites da reputação;
- usa chat para esclarecer condição ou logística;
- identifica e usa bloqueio/denúncia em situação de abuso.

### Evidência contrária

- reputação é ignorada ou tratada como garantia;
- chat apenas acelera exposição de telefone/endereço;
- participante migra imediatamente para canal externo;
- histórico não resolve conta nova;
- custo de moderação supera valor percebido.

### Critério

- **Manter como pacote mínimo:** pelo menos 8 de 12 participantes usam um dos sinais para justificar decisão e explicam corretamente seus limites.
- **Alterar:** sinais ajudam, mas o momento do chat ou a apresentação induzem risco; restringir chat, contato ou reputação.
- **Rejeitar mecanismo específico:** recurso não afeta decisão, é mal compreendido ou cria falsa garantia. Não rejeitar segurança básica por ausência de preferência.

### Limitação

Confiança percebida não equivale a redução de fraude. A hipótese só pode ser plenamente avaliada com dados do piloto.

## 8. H-05 — Troca presencial suficiente

### Formulação

**Hipótese:** um piloto regional pode operar sem frete integrado, usando encontro combinado diretamente entre as partes.

### Base atual

- **Fato:** encontro presencial é premissa proposta e segurança em local público é requisito.
- **Fato:** não há região, raio, mobilidade ou pontos de encontro definidos.
- **Inferência:** o encontro pode reduzir logística técnica e aumentar risco físico e abandono.

### Risco se falsa

Sem alternativa logística, propostas podem não ser concluídas ou podem expor usuários.

### Método

1. Entrevistas sobre encontros e entregas reais.
2. Registrar raio/tempo aceitável como faixa, não endereço.
3. Tarefa de protótipo para combinar encontro.
4. Avaliar transporte, tamanho do item, horário, acompanhante e ponto público.

### Evidência favorável

- participantes relatam prática ou disposição ancorada em experiência;
- existe raio compatível com a região;
- pontos públicos e horários viáveis são identificados;
- pessoa sabe cancelar e evitar residência;
- categorias escolhidas são transportáveis.

### Evidência contrária

- dependência frequente de entrega;
- item incompatível com transporte;
- distância e custo anulam o valor;
- preocupação de segurança impede encontro;
- necessidade de endereço residencial.

### Critério

- **Manter:** pelo menos dois terços dos participantes do segmento prioritário descrevem uma forma prática e segura de concluir dentro do raio escolhido.
- **Alterar:** viável apenas para categorias, horários ou micro-regiões específicos; reduzir o piloto.
- **Rejeitar:** encontro é barreira dominante ou exige logística fora do MVP na maioria dos casos relevantes.

### Limitação

Resposta hipotética sobre segurança deve ser tratada com cautela; comportamento real precisa ser acompanhado no piloto.

## 9. H-06 — Um ou mais itens por lado é compreensível

### Formulação

**Hipótese:** permitir composição com múltiplos itens resolve casos relevantes sem causar erro de entendimento.

### Base atual

- **Fato:** os documentos alternam entre 1:N e N:N.
- **Fato:** vários itens aumentam estados, concorrência e risco de aceite incorreto.
- **Inferência:** 1:1 deve ser a referência; complexidade precisa provar valor.

### Risco se falsa

O MVP ganha complexidade de UX e consistência sem benefício proporcional.

### Método

1. Levantar casos reais nas entrevistas.
2. Testar primeiro 1:1 com seis participantes e 1:N com seis.
3. Pedir que expliquem a composição sem olhar para a tela.
4. Observar tentativa espontânea de incluir vários itens.
5. Não testar N:N completo se 1:N já falhar.

### Evidência favorável

- casos reais exigem compensação por vários itens;
- participante entende lados e revisão;
- nenhum aceite incorreto;
- ganho percebido supera esforço.

### Evidência contrária

- casos são raros ou hipotéticos;
- erro sobre quem recebe o quê;
- múltiplos itens são usados para simular valor monetário;
- reserva de vários itens causa receio;
- 1:1 resolve o problema inicial.

### Critério

- **Manter 1:N:** pelo menos 9 de 12 compreendem e ao menos um terço relata caso concreto de necessidade.
- **Alterar para 1:1:** compreensão abaixo do limiar ou necessidade pouco frequente.
- **Rejeitar N:N no MVP:** qualquer padrão de aceite incorreto com risco relevante, ou ausência de casos concretos; reavaliar depois do piloto.

### Limitação

O protótipo não testa concorrência transacional. Essa validação só será técnica após decisão de produto.

## 10. H-07 — Moderação manual suporta o volume inicial

### Formulação

**Hipótese:** uma operação humana definida consegue tratar anúncios, mensagens, usuários e recursos no volume do piloto.

### Base atual

- **Fato:** moderação mínima é proposta para o MVP.
- **Fato:** não há volume, responsável, horário, severidade, SLA ou política.
- **Inferência:** “manual” não significa simples; casos críticos exigem cobertura e decisão consistente.

### Risco se falsa

O piloto pode expor usuários a fraude, assédio, ameaça ou item ilícito sem resposta adequada.

### Método

1. Definir política provisória e papéis.
2. Criar 40 casos sintéticos com severidades variadas.
3. Executar duas rodadas de triagem e decisão.
4. Medir tempo, divergência, escalonamento e backlog.
5. Comparar capacidade disponível com volume exploratório.

### Evidência favorável

- casos críticos identificados;
- decisões consistentes e justificadas;
- acesso a evidência é mínimo e auditável;
- fila cabe nas horas disponíveis;
- recurso e escalonamento funcionam.

### Evidência contrária

- caso crítico é classificado como baixo;
- decisões semelhantes recebem sanções incompatíveis;
- acesso ao chat é excessivo;
- backlog cresce;
- não existe responsável durante janela crítica;
- política não permite ação necessária.

### Critério

- **Manter:** 100% dos casos críticos são corretamente identificados e escalonados no prazo definido, e o volume total cabe na capacidade aprovada.
- **Alterar:** limitar usuários/categorias, melhorar triagem, política ou cobertura e repetir a simulação.
- **Rejeitar para o piloto:** qualquer caso crítico fica sem resposta, não há acesso controlado ou a capacidade é estruturalmente insuficiente.

### Limitação

Casos sintéticos não reproduzem integralmente ambiguidade, pressão e volume real. A fila deve ser monitorada desde o primeiro dia do piloto.

## 11. Regras de síntese

1. Nenhuma hipótese passa com uma única fala ou método.
2. Resultado misto gera alteração ou novo teste, não aprovação automática.
3. Evidência contrária deve aparecer ao lado da favorável.
4. `H-01`, `H-02`, `H-05` e `H-07` bloqueiam o piloto se rejeitadas.
5. `H-03`, `H-04` e `H-06` podem simplificar o MVP sem abandonar a tese.
6. Toda alteração relevante exige decisão de Bruno e atualização posterior das fontes.
