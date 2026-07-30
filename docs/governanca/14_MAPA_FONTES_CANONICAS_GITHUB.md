# Mapa de fontes canônicas do GitHub — Escambo Online

**Status:** regra operacional estável

**Natureza:** documento estável de navegação e protocolo de recuperação. Funciona como **índice** das fontes canônicas e como **protocolo** para consultar o estado vigente diretamente no GitHub. **Não** reproduz o conteúdo integral dos documentos evolutivos e **não** contém snapshot de estado, próximo gate, backlog, hipóteses específicas, decisões temporárias, SHAs, branches ou números de PR. Esses valores mudam e vivem **somente no GitHub**.

Este mapa acompanha a [Constituição operacional do Projeto ChatGPT](13_CONSTITUICAO_OPERACIONAL_CHATGPT.md): a constituição diz **como trabalhar**; este mapa diz **onde ler o que está decidido e em que estágio**.

## 1. Repositório e referência canônica

- Repositório oficial: **`BrunoMNoronha/escambo-online`**.
- Referência canônica vigente: o branch **`main`**.
- O GitHub é a fonte versionada oficial do produto, da descoberta, da arquitetura, da qualidade, da governança, das decisões, do roadmap e dos prompts, relatórios e evidências.
- Qualquer atividade dependente do estado do projeto deve ler as fontes vigentes na `main` **antes** de analisar, recomendar ou decidir.

## 2. Documentos mínimos obrigatórios

Antes de qualquer atividade cuja resposta, recomendação ou execução dependa do estado vigente do projeto, leia na versão atual da `main`:

1. [`README.md`](../../README.md) — entrada do projeto e hierarquia de verdade;
2. [`AGENTS.md`](../../AGENTS.md) — regras aplicáveis a qualquer agente;
3. [`11_ESTADO_ATUAL_PROJETO.md`](11_ESTADO_ATUAL_PROJETO.md) — estágio, pendências e próximo gate (registro vivo);
4. [`REGISTRO_DECISOES.md`](REGISTRO_DECISOES.md) — decisões confirmadas (fonte primária).

Esses quatro documentos determinam o estado, as autorizações vigentes e os bloqueios. A leitura é obrigatória antes de qualquer:

- análise dependente do estado atual;
- decisão ou recomendação operacional;
- criação de prompt para um agente;
- auditoria de relatório;
- autorização ou execução de etapa;
- avaliação de gate, pendência ou próximo passo.

Atividades que **não** dependem do estado vigente (por exemplo, correção de digitação, dúvida conceitual sobre uma regra estável ou formatação local) não exigem a releitura integral da base, **desde que não façam nenhuma afirmação** sobre:

- estado atual;
- decisões vigentes;
- autorizações;
- escopo vigente;
- pendências;
- conclusão de etapas;
- próximo gate.

Esta exceção **não** autoriza trabalhar com memória ou snapshot antigo quando o estado for material: no instante em que a tarefa passar a depender do estado, releia os quatro documentos antes de afirmar ou agir.

Esta dispensa aplica-se **somente à orquestração do Projeto ChatGPT**, quando a tarefa não analisa nem altera o repositório e não faz afirmações dependentes do estado. Agentes que analisem ou alterem o repositório continuam sujeitos à leitura mínima e às demais regras de [`README.md`](../../README.md) e [`AGENTS.md`](../../AGENTS.md), inclusive em alterações locais, editoriais ou aparentemente simples. Quando mais de uma regra se aplicar, prevalece a mais específica ou restritiva: esta dispensa não supera `README.md` nem `AGENTS.md`.

## 3. Sequência de leitura

Quando a consulta ao estado vigente for obrigatória, siga esta sequência:

1. `README.md`;
2. `AGENTS.md`;
3. `11_ESTADO_ATUAL_PROJETO.md`;
4. `REGISTRO_DECISOES.md`;
5. as fontes adicionais do assunto da etapa (seção 4);
6. os documentos adicionais citados pelas fontes acima, conforme necessário (seção 5).

## 4. Fontes adicionais por assunto

Quando a atividade dependente do estado exigir fontes adicionais, leia, além dos documentos mínimos, somente as fontes aplicáveis ao assunto da etapa. Consulte-as sempre na `main`.

### Produto e escopo

- [`02_FONTE_MESTRA_PRODUTO.md`](../produto/02_FONTE_MESTRA_PRODUTO.md);
- [`03_ESCOPO_MVP_REGRAS_NEGOCIO.md`](../produto/03_ESCOPO_MVP_REGRAS_NEGOCIO.md);
- [`04_JORNADAS_HISTORIAS_CRITERIOS.md`](../produto/04_JORNADAS_HISTORIAS_CRITERIOS.md);
- [`08_ROADMAP_BACKLOG.md`](../produto/08_ROADMAP_BACKLOG.md).

### Descoberta

- [`RELATORIO_AUDITORIA_PRODUTO_V1.md`](../descoberta/RELATORIO_AUDITORIA_PRODUTO_V1.md);
- [`PLANO_DESCOBERTA_V1.md`](../descoberta/PLANO_DESCOBERTA_V1.md);
- [`ROTEIRO_ENTREVISTAS_V1.md`](../descoberta/ROTEIRO_ENTREVISTAS_V1.md);
- [`PROTOCOLO_COLETA_RESPONSAVEL_V1.md`](../descoberta/PROTOCOLO_COLETA_RESPONSAVEL_V1.md);
- [`MATRIZ_HIPOTESES_V1.md`](../descoberta/MATRIZ_HIPOTESES_V1.md);
- [`DECISOES_PARA_BRUNO_V1.md`](../descoberta/DECISOES_PARA_BRUNO_V1.md).

### Arquitetura

- [`05_MODELO_DOMINIO_DADOS.md`](../arquitetura/05_MODELO_DOMINIO_DADOS.md);
- [`06_ARQUITETURA_TECNICA_INICIAL.md`](../arquitetura/06_ARQUITETURA_TECNICA_INICIAL.md).

### Qualidade, segurança e privacidade

- [`07_QUALIDADE_SEGURANCA_PRIVACIDADE.md`](../qualidade/07_QUALIDADE_SEGURANCA_PRIVACIDADE.md).

### Governança

- [`01_INSTRUCOES_PROJETO_CHATGPT.md`](01_INSTRUCOES_PROJETO_CHATGPT.md);
- [`09_GOVERNANCA_IA_GITHUB.md`](09_GOVERNANCA_IA_GITHUB.md);
- [`13_CONSTITUICAO_OPERACIONAL_CHATGPT.md`](13_CONSTITUICAO_OPERACIONAL_CHATGPT.md);
- este mapa (`14`);
- [`12_BASE_CONHECIMENTO_CHATGPT.md`](12_BASE_CONHECIMENTO_CHATGPT.md) — manifesto da base do Projeto ChatGPT.

### Prompts, relatórios e evidências

- [`10_TEMPLATES_PROMPTS_RELATORIOS.md`](10_TEMPLATES_PROMPTS_RELATORIOS.md);
- relatórios e evidências versionados nas respectivas áreas do repositório.

O [índice completo da documentação](../README.md) apresenta ordem de leitura, finalidade e estado de cada documento.

## 5. Documentos adicionais citados pelas fontes

Quando uma fonte lida citar outro documento necessário para entender ou executar a etapa, consulte também esse documento na `main`. Não presuma o conteúdo de um documento citado a partir do nome ou de memória: leia a versão vigente antes de usá-lo.

## 6. Verificação da fonte

Antes de confiar em qualquer fonte, confirme:

- que a leitura foi feita no branch **`main`** do repositório oficial;
- a **data** de atualização declarada no documento, quando houver;
- o **estado** informado (por exemplo: proposta, confirmado, hipótese, registro vivo);
- que a versão consultada é a **vigente**, não uma cópia, snapshot ou anexo desatualizado.

## 7. Não trabalhar com memória ou snapshot antigo

Não conduza análise, recomendação ou decisão dependente do estado usando apenas memória, contexto de conversa anterior ou uma versão antiga anexada. O estado do projeto muda no GitHub; a fonte válida é sempre a `main` vigente. Sempre que a atividade depender do estado atual, reconsulte os documentos mínimos obrigatórios antes de agir.

## 8. Comportamento quando o GitHub estiver indisponível

Se não for possível acessar a `main` ou validar a fonte vigente:

- **não presumir o estado** do projeto a partir de memória ou de versões antigas;
- **não afirmar autorizações** — nenhum gate se considera liberado sem confirmação na fonte vigente;
- **não aprovar nem executar etapa sensível** (qualquer item dos gates de autorização da constituição);
- **reportar claramente o bloqueio**, indicando que a fonte canônica não pôde ser consultada e que a etapa fica suspensa até o acesso ser restabelecido.

Indisponibilidade da fonte é motivo para parar e relatar, nunca para improvisar sobre o estado.
