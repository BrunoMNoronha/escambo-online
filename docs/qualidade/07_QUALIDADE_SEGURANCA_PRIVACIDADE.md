# Qualidade, segurança e privacidade

**Versão:** 0.1  
**Status:** requisitos mínimos iniciais

## 1. Estratégia de qualidade

Qualidade não é uma fase final. Cada etapa deve incluir critérios funcionais, técnicos, de segurança e observabilidade proporcionais ao risco.

### Pirâmide proposta

| Nível | Foco |
| --- | --- |
| Unidade | regras de domínio, validações e casos de uso |
| Integração | banco, autorização, transações, storage e contratos |
| Contrato/API | schemas, erros, paginação e compatibilidade |
| E2E | jornadas críticas do usuário |
| Manual exploratório | usabilidade, acessibilidade e cenários não roteirizados |

### Casos mínimos

- happy path;
- vazio, nulo, limite mínimo e máximo;
- dado inválido;
- não autenticado e sem permissão;
- recurso inexistente;
- repetição/idempotência;
- concorrência;
- alto volume quando pertinente;
- falha e recuperação de dependência externa.

## 2. Pipeline mínimo

Em toda mudança de código:

1. formatação;
2. lint;
3. typecheck;
4. testes unitários e de integração afetados;
5. testes E2E aplicáveis;
6. build;
7. análise de dependências e segredos conforme tooling aprovado.

O relatório deve listar cada comando, código de saída e resumo do resultado.

## 3. Jornadas críticas para E2E

1. criar conta e autenticar;
2. publicar anúncio;
3. buscar anúncio;
4. enviar proposta;
5. fazer contraproposta;
6. aceitar com reserva atômica;
7. impedir aceite concorrente;
8. conversar;
9. concluir e avaliar;
10. denunciar e moderar.

## 4. Requisitos não funcionais iniciais

- experiência responsiva a partir de smartphone;
- navegação principal acessível por teclado;
- feedback claro de carregamento, erro e sucesso;
- paginação para coleções;
- uploads com limites;
- endpoints críticos protegidos contra abuso;
- transações consistentes;
- recuperação de falha sem duplicar comandos;
- logs sem credenciais e dados pessoais desnecessários;
- backup e restauração testados antes de produção.

Metas numéricas de latência, disponibilidade e volume devem ser definidas após o piloto e o orçamento.

## 5. Segurança por área

### Identidade

- armazenamento seguro de credenciais;
- proteção contra enumeração e força bruta;
- recuperação com token temporário;
- revogação de sessão;
- elevação de privilégio controlada;
- MFA para perfis administrativos, se viável para o lançamento.

### Autorização

- negar por padrão;
- validar papel e propriedade no backend;
- testes específicos para acesso horizontal e vertical;
- não confiar em IDs, flags ou estado vindos do cliente.

### Entrada e saída

- schemas estritos;
- consultas parametrizadas;
- encode/sanitize conforme o contexto;
- política de conteúdo para rich text, links e imagens;
- limites de tamanho, quantidade e frequência.

### Operações críticas

- idempotência;
- transação;
- auditoria;
- confirmação explícita;
- tratamento de concorrência;
- mensagens de erro sem detalhes internos.

### Dependências e segredos

- lockfile versionado;
- dependências mínimas;
- verificação de vulnerabilidades;
- nenhum segredo em repositório, prompt, screenshot ou relatório;
- rotação e separação por ambiente.

## 6. Ameaças específicas do produto

| Risco | Controle inicial |
| --- | --- |
| Anúncio fraudulento | denúncia, moderação, histórico e limites |
| Item proibido | política, categorias, detecção e revisão |
| Conta falsa | verificação progressiva, rate limit e sinais de abuso |
| Assédio no chat | bloqueio, denúncia, moderação e retenção controlada |
| Exposição de endereço | região aproximada e compartilhamento progressivo |
| Aceite duplo | transação, restrição e lock |
| Manipulação de avaliação | vínculo à troca, unicidade e moderação |
| Spam de propostas | rate limit, bloqueio e reputação |
| Upload malicioso | validação, processamento isolado e storage controlado |
| Abuso administrativo | RBAC, MFA, motivo e auditoria |

Usar modelagem de ameaças antes de autenticação, upload, chat, aceite e administração.

## 7. Privacidade

Princípios:

- coletar somente o necessário;
- definir finalidade antes do campo;
- separar dado público, privado e administrativo;
- reduzir exposição por padrão;
- definir retenção e descarte;
- permitir exercício de direitos conforme política aplicável;
- registrar acesso administrativo sensível;
- revisar fornecedores que processem dados.

Antes da produção, criar uma matriz:

`dado → finalidade → base/política aplicável → visibilidade → retenção → compartilhamento → controle`.

### 7.1 Matriz de privacidade da coleta de descoberta

Instância aprovada para o **primeiro ciclo de entrevistas** (`DISC-005` a `DISC-012`; detalhe no [Protocolo de coleta responsável V1](../descoberta/PROTOCOLO_COLETA_RESPONSAVEL_V1.md)). É proposta operacional, **não** parecer jurídico; nenhuma base legal está homologada.

| Dado | Finalidade | Base/política aplicável | Visibilidade | Acesso | Retenção | Descarte | Compartilhamento | Controles |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Contato do participante | agendamento e eventual exclusão | decisão operacional `DISC-005`/`DISC-006`; avaliação jurídica futura | privada, arquivo separado | só Bruno | até 30 dias após a última entrevista do ciclo | exclusão segura (arquivo, lixeira, cópias) | não compartilhado; nunca a IA | MFA; separação de arquivos; sem link público; fora do GitHub |
| Chave `contato ↔ código` | localizar dados para exclusão/reagendamento | decisão operacional `DISC-008`; avaliação jurídica futura | privada | só Bruno | eliminada com os contatos (≤30 dias) | exclusão segura | não compartilhado | MFA; arquivo separado; fora do GitHub; nunca a IA |
| Registro de consentimento | comprovar consentimento verbal | decisão operacional `DISC-006`; avaliação jurídica futura | privado | só Bruno | mesmo prazo da respectiva nota | com a nota | não compartilhado | MFA; fora do GitHub |
| Notas pseudonimizadas (só código) | evidência das hipóteses | decisão operacional `DISC-007`/`DISC-011`; avaliação jurídica futura | pseudonimizada (só código) | só Bruno inicialmente | o que ocorrer primeiro: 90 dias após a decisão final de D6 ou 12 meses após a entrevista | exclusão segura | só sínteses desidentificadas a IA | MFA; só código; fora do GitHub; restrição de IA |
| Sínteses agregadas desidentificadas | análise e documentação | decisão operacional `DISC-010`/`DISC-011` | desidentificada | equipe do projeto | podem permanecer na documentação | conforme documentação | IA apenas após desidentificação revisada por Bruno | desidentificação revisada antes de qualquer uso por IA |
| Áudio/vídeo | — | não aplicável no 1º ciclo (`DISC-007`) | — | — | não aplicável no 1º ciclo | — | — | — |

Controles transversais: nenhum dado pessoal no GitHub; nenhum arquivo bruto enviado a IA; armazenamento em Google Drive privado de Bruno com MFA e sem compartilhamento público (`DISC-009`); exclusão em até 7 dias corridos mediante código e fluxo mínimo de incidente com aviso a Bruno no mesmo dia (`DISC-012`).

## 8. Moderação e segurança presencial

O produto deve:

- exibir orientação de encontro em local público;
- evitar sugerir residência como ponto de encontro;
- permitir bloqueio e denúncia;
- mostrar que a plataforma não inspecionou o item, salvo processo real;
- definir resposta a ameaça, fraude e item ilícito;
- ter procedimento interno para escalonamento.

## 9. Gate jurídico e de políticas

Antes do piloto com usuários reais, revisar:

- termos de uso;
- política de privacidade;
- política de itens proibidos;
- regras de moderação e recurso;
- orientação de segurança;
- idade mínima;
- retenção e exclusão;
- responsabilidade por encontros e bens;
- mecanismo de contato para solicitações.

Este documento é requisito de produto e engenharia, não parecer jurídico.

## 10. Evidência exigida por etapa

Uma conclusão técnica deve trazer:

- diff ou lista exata de arquivos;
- comandos executados;
- resultados e quantidade de testes;
- cenários não testados e motivo;
- riscos residuais;
- impacto em documentação;
- screenshots para alteração visual;
- evidência de migration e rollback quando autorizados;
- confirmação de que segredos não foram incluídos.
