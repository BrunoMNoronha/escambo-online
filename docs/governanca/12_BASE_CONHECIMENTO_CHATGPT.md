# Base de conhecimento do Projeto ChatGPT

**Projeto:** Escambo Online

**Versão do pacote:** 0.2

**Data:** 29/07/2026

**Status:** conjunto canônico preparado para substituir integralmente a base anterior após merge

## 1. Objetivo

Este documento define a instrução e os arquivos que devem compor a base de conhecimento do Projeto ChatGPT. O procedimento evita que versões originais, cópias atualizadas e regras divergentes coexistam no contexto.

A substituição da base não autoriza pesquisa de campo, contato com participantes, implementação, schema, infraestrutura ou operação Git adicional.

## 2. Procedimento de substituição

1. Aguardar o merge da revisão documental que contém este manifesto.
2. No Projeto ChatGPT, remover todos os arquivos atualmente anexados à base de conhecimento do projeto.
3. Substituir integralmente o texto existente em **Instruções do projeto** pelo conteúdo completo de `01_INSTRUCOES_PROJETO_CHATGPT.md`.
4. Anexar somente os 16 arquivos listados na seção 3, obtidos da revisão já mergeada.
5. Não anexar `01_INSTRUCOES_PROJETO_CHATGPT.md` como arquivo: seu conteúdo já estará no campo de instruções.
6. Não manter cópias com sufixos como “original”, “novo”, “atualizado” ou “cópia”.
7. Executar a verificação da seção 4 antes de usar a base.

Remover os arquivos antigos do Projeto ChatGPT não apaga o histórico: versões anteriores permanecem recuperáveis no Git.

## 3. Arquivos canônicos a anexar

### Produto

1. [`02_FONTE_MESTRA_PRODUTO.md`](../produto/02_FONTE_MESTRA_PRODUTO.md)
2. [`03_ESCOPO_MVP_REGRAS_NEGOCIO.md`](../produto/03_ESCOPO_MVP_REGRAS_NEGOCIO.md)
3. [`04_JORNADAS_HISTORIAS_CRITERIOS.md`](../produto/04_JORNADAS_HISTORIAS_CRITERIOS.md)
4. [`08_ROADMAP_BACKLOG.md`](../produto/08_ROADMAP_BACKLOG.md)

### Descoberta

5. [`RELATORIO_AUDITORIA_PRODUTO_V1.md`](../descoberta/RELATORIO_AUDITORIA_PRODUTO_V1.md)
6. [`PLANO_DESCOBERTA_V1.md`](../descoberta/PLANO_DESCOBERTA_V1.md)
7. [`ROTEIRO_ENTREVISTAS_V1.md`](../descoberta/ROTEIRO_ENTREVISTAS_V1.md)
8. [`MATRIZ_HIPOTESES_V1.md`](../descoberta/MATRIZ_HIPOTESES_V1.md)
9. [`DECISOES_PARA_BRUNO_V1.md`](../descoberta/DECISOES_PARA_BRUNO_V1.md)

### Arquitetura e qualidade

10. [`05_MODELO_DOMINIO_DADOS.md`](../arquitetura/05_MODELO_DOMINIO_DADOS.md)
11. [`06_ARQUITETURA_TECNICA_INICIAL.md`](../arquitetura/06_ARQUITETURA_TECNICA_INICIAL.md)
12. [`07_QUALIDADE_SEGURANCA_PRIVACIDADE.md`](../qualidade/07_QUALIDADE_SEGURANCA_PRIVACIDADE.md)

### Governança

13. [`09_GOVERNANCA_IA_GITHUB.md`](09_GOVERNANCA_IA_GITHUB.md)
14. [`10_TEMPLATES_PROMPTS_RELATORIOS.md`](10_TEMPLATES_PROMPTS_RELATORIOS.md)
15. [`11_ESTADO_ATUAL_PROJETO.md`](11_ESTADO_ATUAL_PROJETO.md)
16. [`REGISTRO_DECISOES.md`](REGISTRO_DECISOES.md)

`README.md`, `AGENTS.md`, `docs/README.md` e este manifesto permanecem no repositório como navegação e procedimento. Não precisam ser anexados, pois duplicariam conteúdo operacional.

## 4. Verificação após a substituição

Confirmar no Projeto ChatGPT:

- existem exatamente 16 arquivos de conhecimento;
- não existe arquivo antigo ou duplicado;
- a instrução menciona troca exclusivamente de bens, sem complemento financeiro;
- a fonte-mestra está na versão 0.2;
- Distrito Federal consta como mercado macro e RA como unidade de análise;
- as duas RAs aparecem como pendência, não como escolha presumida;
- os três agrupamentos candidatos aparecem como recortes de pesquisa, não como taxonomia final;
- `MATRIZ_HIPOTESES_V1.md` informa critérios aprovados e hipóteses não validadas;
- `11_ESTADO_ATUAL_PROJETO.md` aponta a escolha das duas RAs como próximo gate;
- nenhuma fonte declara autorização para implementação ou contato externo.

Se qualquer verificação falhar, não iniciar a próxima etapa. Corrigir a base e repetir a checagem.

## 5. Primeiro uso recomendado

Após a substituição, iniciar uma nova conversa no Projeto ChatGPT com:

> Leia integralmente a base de conhecimento vigente. Resuma somente as decisões confirmadas, as hipóteses ainda não validadas e os bloqueios atuais. Em seguida, apresente a Bruno a decisão necessária sobre as duas Regiões Administrativas do Distrito Federal, explicando os critérios de escolha e o impacto de adiar. Não pesquise pessoas, não contate participantes e não implemente nada.

O resultado esperado é uma verificação de consistência e a preparação da próxima decisão, não uma execução de campo.

## 6. Controle de versão

- A fonte oficial dos arquivos é o repositório `BrunoMNoronha/escambo-online`.
- Alterações futuras devem ocorrer no Git, ser revisadas e somente depois substituir os arquivos correspondentes no Projeto ChatGPT.
- O campo de instruções deve ser atualizado sempre que `01_INSTRUCOES_PROJETO_CHATGPT.md` mudar.
- A troca de arquivo na base deve preservar o mesmo nome canônico.
- Decisão nova exige atualização mínima de `REGISTRO_DECISOES.md` e `11_ESTADO_ATUAL_PROJETO.md`, além das fontes afetadas.

## 7. Limitação operacional

Este repositório prepara e versiona o pacote, mas não altera automaticamente os anexos ou as instruções do Projeto ChatGPT. A remoção dos originais e a inclusão dos 16 arquivos atualizados devem ser executadas no próprio Projeto ChatGPT depois do merge.
