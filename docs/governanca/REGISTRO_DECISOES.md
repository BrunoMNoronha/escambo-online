# Registro de decisões

**Atualizado em:** 29/07/2026

**Responsável pela aprovação de produto:** Bruno

Este documento registra decisões explícitas. Propostas e recomendações não se tornam decisões apenas por estarem documentadas.

## Decisões confirmadas

| ID | Data | Decisão | Origem | Impacto |
| --- | --- | --- | --- | --- |
| GOV-001 | 29/07/2026 | ChatGPT organizará, documentará e orquestrará o desenvolvimento | Bruno | Define o orquestrador |
| GOV-002 | 29/07/2026 | Claude Code e Antigravity atuarão como agentes de execução autorizada | Bruno | Define executores |
| GOV-003 | 29/07/2026 | GitHub será usado para versionamento | Bruno | Define histórico oficial |
| GOV-004 | 29/07/2026 | Bruno mantém aprovação final de decisões e ações sensíveis | Governança adotada | Preserva decisão humana |
| GOV-005 | 29/07/2026 | Commit, push, PR, migration e mudança sensível exigem autorização explícita | Governança adotada | Define gates |
| GOV-006 | 29/07/2026 | `BrunoMNoronha/escambo-online` é o repositório oficial do projeto | Bruno | Centraliza documentação e futuro código |

## Decisões de desenho da descoberta

Aprovadas explicitamente por Bruno em 29/07/2026, encerrando o gate inicial de produto (decisões 1–4 de [Decisões para Bruno V1](../descoberta/DECISOES_PARA_BRUNO_V1.md)). Definem o teste da descoberta; **não validam** demanda, liquidez nem o MVP.

| ID | Data | Decisão | Origem | Impacto | Documentos afetados |
| --- | --- | --- | --- | --- | --- |
| DISC-001 | 29/07/2026 | A descoberta testa exclusivamente troca de bens sem complemento financeiro; menção espontânea a complemento é registrada como evidência e não altera a tese durante a coleta | Bruno | Fixa a fronteira da tese testada; reconsideração futura exige nova decisão de Bruno | `02_FONTE_MESTRA`, `03_ESCOPO`, `PLANO_DESCOBERTA_V1`, `MATRIZ_HIPOTESES_V1` |
| DISC-002 | 29/07/2026 | Regiões candidatas: Cruzeiro/DF e Guará/DF; unidade pública de localização é a Região Administrativa | Bruno | Define células de recrutamento e comparação; não presume liquidez; endereço exato permanece proibido | `02_FONTE_MESTRA`, `PLANO_DESCOBERTA_V1`, `MATRIZ_HIPOTESES_V1` |
| DISC-003 | 29/07/2026 | Público, três categorias candidatas e exclusões imediatas definidos como recorte de descoberta | Bruno | Delimita a amostra; não é política definitiva do MVP nem parecer jurídico | `02_FONTE_MESTRA`, `03_ESCOPO`, `PLANO_DESCOBERTA_V1` |
| DISC-004 | 29/07/2026 | Critérios de `MATRIZ_HIPOTESES_V1.md` aprovados sem alteração de conteúdo e congelados em 29/07/2026 | Bruno | Pré-registro; `H-01` a `H-07` seguem não validadas; falha de `H-01/H-02/H-05/H-07` pode interromper, restringir ou reformular o projeto | `MATRIZ_HIPOTESES_V1`, `PLANO_DESCOBERTA_V1` |

## Decisões documentais confirmadas

Propostas no PR #1 como `DOC-001` a `DOC-003` e **em vigor desde o merge do PR #1**, em 29/07/2026.

| ID | Data | Decisão | Origem | Impacto |
| --- | --- | --- | --- | --- |
| DOC-001 | 29/07/2026 | Organizar documentos por `produto`, `descoberta`, `arquitetura`, `qualidade` e `governanca` | Merge do PR #1 | Altera caminhos, não conteúdo de produto |
| DOC-002 | 29/07/2026 | Manter `README.md` e `AGENTS.md` na raiz | Merge do PR #1 | Padroniza leitura inicial de pessoas e agentes |
| DOC-003 | 29/07/2026 | Usar este registro como fonte primária das decisões confirmadas | Merge do PR #1 | Exige atualização após cada aprovação |

## Decisões operacionais confirmadas

Tomadas explicitamente por **Bruno em 29/07/2026**, na etapa `EO-GOV-001`. Autorizam **meios de trabalho** e a **direção de hospedagem**; não autorizam implementação do MVP, deploy, criação de automações persistentes, configuração da Vercel nem ativação de recurso pago. Os limites detalhados estão em [09 — Governança de IA e GitHub](09_GOVERNANCA_IA_GITHUB.md) e, para hospedagem, em [06 — Arquitetura técnica inicial](../arquitetura/06_ARQUITETURA_TECNICA_INICIAL.md). Cada decisão preserva os gates do [README.md](../../README.md) e do `09_GOVERNANCA_IA_GITHUB.md`.

| ID | Data | Decisão | Origem | Impacto | Documentos afetados |
| --- | --- | --- | --- | --- | --- |
| GOV-007 | 29/07/2026 | Autorizar GitHub Actions e scripts Python quando diretamente necessários ao escopo de uma etapa (verificações, validações, testes, qualidade, segurança, auditoria documental, desempenho, redução de trabalho repetitivo e economia de tempo/tokens), desde que gratuitos ou cobertos pela infraestrutura já aprovada, determinísticos, reproduzíveis, documentados e seguros | Bruno | Habilita automação interna sob demanda; **não** concede automaticamente commit, push, PR, deploy, migration, alteração de schema ou mudança sensível; autorização não vale para qualquer etapa | `09_GOVERNANCA`, `10_TEMPLATES`, `AGENTS.md`, `11_ESTADO_ATUAL` |
| GOV-008 | 29/07/2026 | Autorizar o uso de ferramentas e recursos gratuitos ou já incluídos das plataformas Claude/Anthropic, OpenAI e GitHub, sem cobrança adicional, desde que o custo incremental seja confirmado como zero, sem contratação, trial com conversão automática ou excedente pago, sem ampliar permissões, sem expor segredos ou dados pessoais e respeitando termos, cotas e limitações | Bruno | Permite reduzir trabalho e tokens com o que já está disponível; criação de conta, OAuth, token, instalação de app, aumento de permissão ou compartilhamento externo de dados exige interrupção e autorização específica | `09_GOVERNANCA`, `10_TEMPLATES`, `AGENTS.md`, `11_ESTADO_ATUAL` |
| INFRA-001 | 29/07/2026 | Registrar a **Vercel** como plataforma **preferencial** para hospedar o protótipo ou MVP sob restrição de custo zero, condicionada à elegibilidade do uso no plano gratuito vigente, à inexistência de cobrança/excedente/conversão automática, à confirmação dos limites antes da ativação, à preservação de portabilidade e a uma autorização posterior e específica para configurar conta, projeto, integração ou deploy | Bruno | Define direção de hospedagem, não homologa a stack proposta; **nenhum deploy nesta etapa**; detalhamento técnico permanece pendente no `ADR-008`; incompatibilidade do plano gratuito obriga a interromper e devolver a decisão a Bruno | `06_ARQUITETURA`, `08_ROADMAP`, `11_ESTADO_ATUAL`, `AGENTS.md` |
| DOC-004 | 29/07/2026 | Registrar a **higiene contínua do repositório**: documentos afetados atualizados na mesma etapa; arquivos obsoletos, duplicados ou desnecessários removidos apenas com evidência suficiente (referências, substituto, impacto em build/testes/links e valor histórico verificados antes); conteúdo relevante consolidado na fonte correta antes da exclusão; toda remoção registrada em relatório com motivo e evidência; histórico útil preservado no Git; arquivos temporários, gerados ou acidentais não versionados | Bruno | Torna a limpeza uma regra controlada; nenhuma exclusão por nome, idade ou aparente duplicidade; complementa `DOC-001` a `DOC-003` | `09_GOVERNANCA`, `10_TEMPLATES`, `AGENTS.md`, `11_ESTADO_ATUAL` |

Limites preservados por estas quatro decisões: continuam exigindo autorização explícita, salvo quando já concedida e sem ampliar permissões, todas as ações de `GOV-005` (commit, push, PR, merge, migration e mudança sensível), qualquer deploy, qualquer custo pago e qualquer tratamento de dado pessoal real.

## Decisão documental adicional

Tomada por **Bruno em 29/07/2026**, na etapa `EO-REPO-003`, ao decidir preservar o conteúdo residual útil da PR #2 — reautorando o procedimento contra a `main` atual e alinhando a hierarquia do `01`. Complementa `DOC-004`.

| ID | Data | Decisão | Origem | Impacto | Documentos afetados |
| --- | --- | --- | --- | --- | --- |
| DOC-005 | 29/07/2026 | Sincronização canônica da base do Projeto ChatGPT: a base de conhecimento deve espelhar as fontes canônicas da `main`; o campo de instruções usa o conteúdo integral de `01_INSTRUCOES_PROJETO_CHATGPT.md`; somente os 18 arquivos definidos em `12_BASE_CONHECIMENTO_CHATGPT.md` são anexados — incluindo `README.md` e `AGENTS.md`, para que a leitura mínima exigida por `AGENTS.md` seja cumprida sem acesso externo; arquivos antigos, duplicados ou renomeados não coexistem; o repositório prevalece em divergência; a substituição de anexos e instruções é **manual**; e a hierarquia de verdade do `01` permanece alinhada ao `README.md` | Bruno | Estabelece higiene da base de conhecimento e complementa `DOC-004`; **documentar o procedimento não significa que a sincronização foi executada**; não altera produto, escopo, hipóteses ou arquitetura; não concede autorização de pesquisa, implementação, infraestrutura, deploy ou tratamento de dados; permite encerrar a PR #2 após o merge da PR #5, com o conteúdo residual útil já preservado | `01_INSTRUCOES_PROJETO_CHATGPT`, `12_BASE_CONHECIMENTO_CHATGPT`, `docs/README.md`, `REGISTRO_DECISOES`, `11_ESTADO_ATUAL` |

## Decisão documental — base de conhecimento (`DOC-006`)

Tomada por **Bruno em 29/07/2026**, na etapa `EO-DOC-006`, após o merge da PR #8. Complementa `DOC-005`.

| ID | Data | Decisão | Origem | Impacto | Documentos afetados |
| --- | --- | --- | --- | --- | --- |
| DOC-006 | 29/07/2026 | A base de conhecimento do Projeto ChatGPT permanece com **exatamente 18 anexos**, substituindo `RELATORIO_AUDITORIA_PRODUTO_V1.md` por `PROTOCOLO_COLETA_RESPONSAVEL_V1.md` (item 7); o relatório de auditoria permanece no repositório como registro histórico, mas deixa de integrar os anexos canônicos; atualiza `12_BASE_CONHECIMENTO_CHATGPT.md` (lista, checklist e primeiro uso) ao estado posterior à `EO-DISC-005` | Bruno | Complementa `DOC-005`; **não** autoriza a substituição manual dos anexos, commit, push, PR, contato com participantes nem aprovação do roteiro | `12_BASE_CONHECIMENTO_CHATGPT`, `REGISTRO_DECISOES`, `11_ESTADO_ATUAL` |

## Decisões de coleta responsável

Aprovadas explicitamente por **Bruno em 29/07/2026**, na etapa `EO-DISC-005`, homologando o pacote `EO-DISC-004` (respostas PC-01 a PC-10). Definem as **regras de coleta do primeiro ciclo de entrevistas de descoberta**. **Não** aprovam o roteiro, **não** autorizam contato, recrutamento, entrevista ou coleta, e **não** declaram conformidade jurídica. Detalhamento operacional em [Protocolo de coleta responsável V1](../descoberta/PROTOCOLO_COLETA_RESPONSAVEL_V1.md).

| ID | Data | Decisão | Origem | Impacto | Documentos afetados |
| --- | --- | --- | --- | --- | --- |
| DISC-005 | 29/07/2026 | Recrutamento: smartphone é variável de perfil, não elegibilidade; critério obrigatório é ter decidido ou considerado o destino de um item nos últimos 12 meses; canais permitidos: indicação pessoal, grupos/associações locais somente com autorização do responsável/administrador e divulgação física em locais autorizados; proibidos: raspagem ou compra de listas, mensagens em massa não solicitadas, anúncios pagos sem orçamento aprovado e contato com menores | Bruno | Define recrutamento sem viés digital e sem coleta indevida de terceiros; não autoriza contato | `PROTOCOLO_COLETA_RESPONSAVEL_V1`, `PLANO_DESCOBERTA_V1`, `11_ESTADO_ATUAL` |
| DISC-006 | 29/07/2026 | Consentimento verbal registrado por checkbox na ficha com código, precedido de folha curta de informação (finalidade, voluntariedade, dados coletados, retenção, exclusão e canal de contato); sem assinatura ou documento; sem incentivo por padrão (incentivo futuro exige aprovação separada); participante recebe seu código para eventual solicitação de exclusão | Bruno | Consentimento com mínima coleta; base legal permanece questão jurídica futura | `PROTOCOLO_COLETA_RESPONSAVEL_V1`, `ROTEIRO_ENTREVISTAS_V1` |
| DISC-007 | 29/07/2026 | Primeiro ciclo registrado somente por notas, sem áudio e sem vídeo; gravação só reconsiderada em decisão específica, com consentimento e retenção próprios, se as notas se mostrarem insuficientes | Bruno | Reduz risco, armazenamento e complexidade; gravação é opção condicionada, não contradição | `PROTOCOLO_COLETA_RESPONSAVEL_V1`, `ROTEIRO_ENTREVISTAS_V1`, `PLANO_DESCOBERTA_V1` |
| DISC-008 | 29/07/2026 | Pseudonimização temporária: cada participante recebe um código (ex.: `P-CRU-01`); notas contêm somente o código; tabela `contato ↔ código` mantida separada, acesso exclusivo de Bruno, eliminada junto com os contatos | Bruno | Permite exclusão e reagendamento no ciclo sem manter identificadores nas notas | `PROTOCOLO_COLETA_RESPONSAVEL_V1`, `ROTEIRO_ENTREVISTAS_V1` |
| DISC-009 | 29/07/2026 | Armazenamento em pasta dedicada no Google Drive privado de Bruno, conta com MFA, sem link público ou compartilhamento externo; notas e contatos separados; acesso inicial exclusivo de Bruno; nenhuma nota de pesquisa no GitHub; nenhum arquivo bruto enviado a IA; sem sincronização automática adicional | Bruno | Define local, visibilidade e acesso antes da coleta; baixo custo e menor exposição | `PROTOCOLO_COLETA_RESPONSAVEL_V1`, `07_QUALIDADE` |
| DISC-010 | 29/07/2026 | Agentes de IA só analisam conteúdo previamente revisado e desidentificado por Bruno (remover nomes/contatos, locais específicos, datas exatas desnecessárias, nomes de terceiros, combinações raras identificáveis e citações literais identificáveis); notas brutas e listas de contato não podem ser enviadas a IA | Bruno | Habilita apoio de IA sem expor dados pessoais; coerente com `GOV-008` | `PROTOCOLO_COLETA_RESPONSAVEL_V1`, `09_GOVERNANCA` |
| DISC-011 | 29/07/2026 | Retenção por categoria: contatos e chave `contato ↔ código` até 30 dias após a última entrevista do ciclo; notas brutas pseudonimizadas até 90 dias após a decisão final da etapa D6, com limite absoluto de 12 meses após cada entrevista; registro do consentimento pelo mesmo prazo da nota; sínteses agregadas desidentificadas podem permanecer; áudio/vídeo não aplicável no 1º ciclo; descarte cobre arquivo principal, lixeira, cópias locais e exportações | Bruno | Proposta operacional conservadora, não obrigação legal; prazos podem ser ajustados após avaliação jurídica futura | `PROTOCOLO_COLETA_RESPONSAVEL_V1`, `07_QUALIDADE`, `PLANO_DESCOBERTA_V1` |
| DISC-012 | 29/07/2026 | Exclusão aceita enquanto a nota bruta existir, concluída em até 7 dias corridos mediante o código, registrando somente a execução (sem preservar o conteúdo eliminado); incidente ou coleta indevida: interromper, isolar o material, não enviar a GitHub/IA, registrar incidente mínimo sem copiar o dado, comunicar Bruno no mesmo dia e decidir depois sobre comunicação ao participante e apoio jurídico conforme a gravidade | Bruno | Garante direito de exclusão e resposta a incidente na descoberta | `PROTOCOLO_COLETA_RESPONSAVEL_V1`, `07_QUALIDADE` |
| DISC-013 | 29/07/2026 | O roteiro NÃO é aprovado nesta etapa e permanece proposta; sequência: (1) registrar as regras; (2) executar etapa documental; (3) incorporar consentimento, código, exclusão e registro somente por notas; (4) auditar o diff; (5) só então Bruno aprova a versão resultante | Bruno | Evita estado ambíguo de roteiro "aprovado mas inadequado"; aprovação fica para etapa posterior | `ROTEIRO_ENTREVISTAS_V1`, `PLANO_DESCOBERTA_V1`, `11_ESTADO_ATUAL` |
| DISC-014 | 29/07/2026 | Nenhum contato, recrutamento ou entrevista autorizado; autorização dependerá de decisões registradas, protocolo criado, roteiro atualizado, documentos sincronizados, revisão final e simulação interna do fluxo com dados fictícios | Bruno | Mantém o bloqueio de contato vigente; contato é gate separado | `PROTOCOLO_COLETA_RESPONSAVEL_V1`, `11_ESTADO_ATUAL` |

Limites preservados: `DISC-005` a `DISC-014` não validam nem alteram `H-01` a `H-07`, não alteram `DISC-001` a `DISC-004` nem o recorte congelado, não aprovam o roteiro e não autorizam contato ou coleta. Continuam exigindo autorização explícita todas as ações de `GOV-005` (commit, push, PR, merge, migration e mudança sensível).

## Pendências de produto

As decisões 1–4 (fronteira da tese, regiões, público/categorias e critérios da matriz) foram respondidas em 29/07/2026 e estão registradas acima como `DISC-001` a `DISC-004`. As decisões 5–10 permanecem pendentes nos momentos previstos. A lista priorizada, as alternativas e o impacto de não decidir estão em:

- [Decisões para Bruno V1](../descoberta/DECISOES_PARA_BRUNO_V1.md)

Nenhuma recomendação da auditoria foi convertida automaticamente em decisão de produto; `DISC-001` a `DISC-004` decorrem de decisão explícita de Bruno, não de recomendação.

## Template

```markdown
| [ID] | [data] | [decisão objetiva] | Bruno | [impacto] |
```

Ao registrar uma decisão:

1. citar a evidência ou o motivo;
2. indicar documentos afetados;
3. atualizar o estado atual;
4. não apagar decisões anteriores; marcar substituição quando aplicável.
