# Fonte-mestra do produto — Escambo Online

**Versão:** 0.2
**Status:** fronteira da tese aprovada para descoberta; hipóteses de valor ainda não validadas
**Responsável final:** Bruno  
**Última atualização:** 29/07/2026

## 1. Tese do produto

Criar uma plataforma digital que permita a pessoas anunciar bens disponíveis e negociar trocas de forma organizada, rastreável e mais segura do que conversas dispersas em redes sociais ou classificados genéricos.

A tese inicial é **troca exclusivamente de bens entre pessoas, sem pagamento ou complemento financeiro**.

Essa fronteira foi confirmada por Bruno para a descoberta e para o MVP inicial. A decisão não valida a existência de demanda.

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
- atuando inicialmente no Distrito Federal;
- interessadas em trocar itens usados em bom estado;
- com preferência por encontro presencial em local combinado.

Para a pesquisa inicial, recomenda-se trabalhar somente com adultos por prudência. A elegibilidade do futuro piloto continua pendente de decisão e revisão apropriada.

O Distrito Federal é o mercado macro. A Região Administrativa será a unidade territorial de análise, e duas RAs ainda precisam ser escolhidas antes do recrutamento.

### Agrupamentos candidatos da descoberta

1. livros, histórias em quadrinhos e jogos de tabuleiro;
2. itens portáteis e não elétricos de casa e decoração;
3. itens portáteis e não motorizados de esporte e lazer.

Esses agrupamentos servem para comparar sinais de demanda e liquidez. Não constituem taxonomia final do produto.

Excluir da descoberta itens:

- ilícitos ou regulados;
- de procedência incerta;
- perigosos;
- íntimos ou com risco relevante de higiene;
- de alto risco;
- que dependam de garantia especializada.

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

- pagamento, carteira, PIX, escrow ou complemento financeiro, por decisão confirmada;
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
| H-02 | Duas Regiões Administrativas do Distrito Federal geram liquidez suficiente no recorte escolhido | Pesquisa por RA e agrupamento de categoria |
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

## 12. Decisões relacionadas

- `PROD-001`: troca exclusivamente de bens, sem complemento financeiro.
- `DISC-001`: Distrito Federal como mercado macro.
- `DISC-002`: Região Administrativa como unidade de análise.
- `DISC-003`: três agrupamentos candidatos da descoberta.
- `DISC-004`: exclusões iniciais de risco.
- `DISC-005`: critérios H-01 a H-07 aprovados.

Consulte `docs/governanca/REGISTRO_DECISOES.md` para a formulação oficial.
