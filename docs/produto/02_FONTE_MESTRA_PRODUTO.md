# Fonte-mestra do produto — Escambo Online

**Versão:** 0.2

**Status:** hipótese inicial; fronteiras da descoberta decididas; produto ainda não validado

**Responsável final:** Bruno

**Última atualização:** 29/07/2026

> **Fronteiras aprovadas para a descoberta (29/07/2026):** a tese testada é exclusivamente troca de bens **sem complemento financeiro** (`DISC-001`); as regiões candidatas são **Cruzeiro/DF** e **Guará/DF**, com **Região Administrativa** como unidade pública de localização (`DISC-002`); o público inicial da descoberta está definido em `DISC-003`. Aprovar o teste **não** valida demanda, liquidez nem o MVP; `H-01` a `H-07` seguem não validadas. Fonte primária: [Registro de decisões](../governanca/REGISTRO_DECISOES.md).

## 1. Tese do produto

Criar uma plataforma digital que permita a pessoas anunciar bens disponíveis e negociar trocas de forma organizada, rastreável e mais segura do que conversas dispersas em redes sociais ou classificados genéricos.

A tese proposta prioriza **troca de bens entre pessoas**, sem pagamento processado pela plataforma no MVP. Para a descoberta, essa fronteira está decidida: testa-se exclusivamente troca de bens sem complemento financeiro (`DISC-001`). Menção espontânea de participantes à necessidade de complemento é registrada como evidência, sem alterar a tese durante a coleta; qualquer reconsideração futura exige nova decisão explícita de Bruno.

## 2. Problema

Hoje, quem deseja trocar um item costuma enfrentar:

- dificuldade para encontrar alguém que queira exatamente o que oferece;
- anúncios incompletos e baixa confiança entre desconhecidos;
- negociações espalhadas em mensagens sem estrutura;
- risco de combinar uma troca envolvendo item indisponível;
- ausência de histórico, reputação e mecanismos claros de denúncia;
- exposição prematura de telefone e localização exata.

## 3. Público inicial

Hipótese principal:

- pessoas maiores de idade;
- atuando inicialmente em uma cidade ou região delimitada;
- interessadas em trocar itens usados em bom estado;
- com preferência por encontro presencial em local combinado.

**Recorte aprovado para a descoberta (`DISC-002`, `DISC-003`):** pessoas com 18 anos ou mais, residentes no **Cruzeiro** ou no **Guará** (Região Administrativa como unidade pública), com pelo menos um item usado em bom estado e sem uso recorrente, com interesse real em avaliar troca por outro bem, com disponibilidade para considerar encontro presencial em local público, e sem depender de complemento financeiro para participar da tese testada. Cruzeiro e Guará são células **candidatas** para comparação, não mercados com liquidez comprovada.

Para a pesquisa inicial, trabalha-se somente com adultos por prudência. A elegibilidade do futuro piloto continua pendente de decisão e revisão apropriada.

Segmentos que podem ser avaliados depois:

- colecionadores;
- comunidades por categoria;
- pequenos negócios;
- instituições, grupos de doação ou economia circular.

## 4. Proposta de valor

“Encontre pessoas interessadas no que você tem, negocie uma troca estruturada e acompanhe o acordo com mais clareza e segurança.”

Diferenciais pretendidos:

- proposta de troca vinculada a anúncios reais;
- contraproposta e histórico das condições negociadas;
- reserva atômica dos itens ao aceitar um acordo;
- chat contextual à negociação;
- reputação após troca concluída;
- privacidade progressiva de localização e contato;
- denúncia, bloqueio e moderação.

## 5. Princípios do produto

1. **Troca antes de dinheiro:** o núcleo do MVP é escambo de bens.
2. **Confiança por desenho:** reputação, histórico e moderação são partes do produto.
3. **Privacidade progressiva:** dados sensíveis só aparecem quando necessários.
4. **Acordo explícito:** a condição aceita deve permanecer registrada.
5. **Simplicidade:** cada funcionalidade precisa provar valor para o MVP.
6. **Segurança sem falsa garantia:** a plataforma reduz riscos, mas não certifica os bens nem garante o encontro.
7. **Rastreabilidade:** operações críticas e mudanças de estado devem ser auditáveis.
8. **Acessibilidade e uso móvel:** a experiência principal deve funcionar bem em smartphones.

## 6. Hipótese de solução do MVP

O MVP proposto deverá permitir:

1. criar conta e perfil;
2. cadastrar anúncio com fotos, categoria, descrição, estado de conservação e localização aproximada;
3. informar o que o anunciante aceita ou deseja receber;
4. buscar e filtrar anúncios;
5. abrir uma proposta oferecendo um ou mais anúncios próprios;
6. aceitar, rejeitar, cancelar ou apresentar contraproposta;
7. conversar em um chat vinculado à proposta;
8. reservar os itens envolvidos quando houver aceite;
9. registrar conclusão ou problema;
10. avaliar a outra parte após a conclusão;
11. denunciar usuário, anúncio ou mensagem;
12. permitir moderação administrativa mínima.

Esses itens são hipóteses de escopo, não decisões homologadas.

A cardinalidade 1:1, 1:N ou N:N e o momento de abertura do chat continuam pendentes. A lista acima não homologa essas regras.

## 7. Fora do MVP proposto

- pagamento, carteira, PIX, escrow ou complemento financeiro;
- cálculo automático de equivalência de valor;
- compra e venda;
- leilão;
- logística, entrega integrada ou rastreamento de frete;
- seguro ou garantia da troca;
- aplicativo móvel nativo;
- múltiplos países, moedas ou idiomas;
- recomendação avançada por inteligência artificial;
- gamificação complexa;
- plano comercial para lojas;
- integrações sociais amplas;
- blockchain, token ou NFT.

## 8. Premissas que precisam ser validadas

| ID | Hipótese | Como validar |
| --- | --- | --- |
| H-01 | Existe demanda recorrente por troca sem dinheiro | Entrevistas e landing page |
| H-02 | Localização regional gera liquidez suficiente | Pesquisa por cidade e categorias |
| H-03 | Usuários aceitam cadastrar itens próprios para propor troca | Protótipo e teste de usabilidade |
| H-04 | Reputação e chat contextual aumentam confiança | Entrevistas e teste moderado |
| H-05 | Troca presencial é suficiente para o primeiro mercado | Entrevistas e análise operacional |
| H-06 | Um ou mais itens por lado é compreensível no MVP | Protótipo comparando fluxos |
| H-07 | Moderação manual suporta o volume inicial | Simulação de cenários e fila |

## 9. Indicadores iniciais

Métricas de produto propostas:

- percentual de usuários que publicam o primeiro anúncio;
- propostas enviadas por anúncio ativo;
- taxa de proposta aceita;
- taxa de troca concluída;
- tempo mediano entre anúncio e acordo;
- percentual de negociações abandonadas;
- denúncias por cem negociações;
- retenção de usuários que concluíram uma troca;
- tempo de resposta da moderação.

Não usar métricas de vaidade, como cadastros totais, isoladamente.

## 10. Riscos principais

- baixa liquidez: oferta e desejo não coincidem;
- fraude, itens proibidos ou descrição enganosa;
- assédio e exposição de dados no chat;
- encontro presencial inseguro;
- contas falsas e manipulação de reputação;
- disputas após o aceite;
- complexidade excessiva em trocas com vários itens;
- exigências jurídicas, de privacidade e moderação;
- custo de armazenamento de imagens;
- crescimento prematuro sem densidade regional.

## 11. Condição para alterar esta fonte

Uma alteração relevante exige:

1. proposta explícita;
2. motivo e evidência;
3. impactos no MVP, regras e arquitetura;
4. decisão de Bruno;
5. atualização dos documentos dependentes.
