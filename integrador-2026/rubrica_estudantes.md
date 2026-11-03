# Rubrica do trabalho integrador — Curadoria do repertório

**Versão de entrega · 20/10/2026.**
**Programação III · IFSul — Campus Passo Fundo · Professor Élder F. F. Bernardi**
**Tutor da atividade:** Prof. Leonardo Constantin  

Os critérios abaixo descrevem as evidências que serão observadas no núcleo do trabalho. O núcleo bem executado e compreendido permite nota máxima, com ou sem base de retomada, Vue ou funcionalidades extras. Não há desconto pelo apoio recebido nem avaliação por quantidade de código ou commits.

## Pesos e cálculo da pontuação

**Valor total: 4,0 pontos. Tutor da atividade: Prof. Leonardo Constantin.**

| Critério | Origem da evidência | Peso | Valor máximo |
|---|---|---|---|
| C1 — Integração e funcionamento | Dupla | 30% | 1,2 ponto |
| C2 — Persistência e publicação | Dupla | 20% | 0,8 ponto |
| C3 — Qualidade proporcional ao ensino | Dupla | 10% | 0,4 ponto |
| C4 — Compreensão | Individual | 30% | 1,2 ponto |
| C5 — Processo e comunicação | Dupla, com participação de ambos | 10% | 0,4 ponto |

Para cada critério, multiplicar o valor máximo pelo fator do nível: Excelente = 1; Bom = 0,75; Regular = 0,50; Insuficiente = 0,25. A pontuação de cada estudante soma os quatro critérios da dupla (até 2,8 pontos) ao seu C4 individual (até 1,2 ponto). Evidência ausente ou impedida fica pendente de verificação equivalente, sem inferir desconhecimento automaticamente.

Uma falha externa ou ausência de evidência exige encaminhamento e nova conferência; não equivale automaticamente a desconhecimento.

### C1 — Integração e funcionamento · R1–R4, R6

| Nível | Evidência observável |
|---|---|
| **Excelente** | Consulta, cadastro, edição no mesmo ID e exclusão funcionam pela interface com dados coerentes; cancelamento preserva registro; player do seed funciona e música sem partes tem estado claro, sem tentativa inválida de reprodução. |
| **Bom** | Percurso CRUD é demonstrável e preserva os dados corretos; há falha pontual de seleção/atualização visual ou estado do player, identificada e corrigível sem reconstruir o fluxo. |
| **Regular** | Demonstra leitura e ao menos uma escrita integrada; uma ou mais operações dependem de requisição manual, ou a interface diverge da API sem que a dupla consiga completar a conferência. |
| **Insuficiente** | Não apresenta leitura e escrita integradas verificáveis; alteração existe só na tela ou as ações indicam sucesso sem executar o percurso correspondente. |

**Observar:** CRUD cotidiano acontece na interface. Chamadas manuais são apoio
de diagnóstico, não substituem a integração. Preservar amostra para o player.

### C2 — Persistência e publicação · R2–R4, R7

| Nível | Evidência observável |
|---|---|
| **Excelente** | Na URL pública, a dupla cria, consulta, edita e exclui com banco; identifica o mesmo ID antes/depois de reiniciar o serviço e explica onde os dados ficam. Configuração é reproduzível, com segredos somente no servidor. |
| **Bom** | CRUD público com banco e persistência são demonstrados; falta um registro de conferência ou há ajuste pontual de configuração que a dupla identifica e conclui com orientação breve. |
| **Regular** | Banco funciona localmente, mas publicação ou teste após reinício ainda não é verificável; a dupla identifica parte da configuração e precisa de apoio para concluir a prova de persistência. |
| **Insuficiente** | A única evidência é dado em memória/lista local ou aplicação pública sem integração verificável ao banco; não distingue esses estados mesmo com consulta orientada. |

**Impedimento externo:** indisponibilidade não equivale a nível insuficiente.
Registrar o impedimento, evidência local com banco e evidências anteriores;
deixar a verificação impedida pendente, conforme encaminhamento docente.
O objetivo de publicação com banco permanece, sem criar prazo/penalidade novos.

### C3 — Qualidade proporcional ao ensino · R5, R8

| Nível | Evidência observável |
|---|---|
| **Excelente** | Entradas vazias não geram cadastro válido; sucesso depende da resposta; falha controlada gera mensagem útil sem esconder problema. Campos e ações são identificáveis e responsabilidades de tela, rota e DAO permanecem reconhecíveis. |
| **Bom** | Validação e distinção entre sucesso/erro funcionam; uma mensagem ou estado exige ajuste pequeno, sem impedir a pessoa de completar a operação e conferir o resultado. |
| **Regular** | Trata apenas parte das entradas/falhas; mensagem genérica ou lista desatualizada dificulta conferir resultado. Precisa de apoio para localizar onde validar ou tratar resposta. |
| **Insuficiente** | Aceita entradas obrigatórias inválidas ou anuncia sucesso na falha, impedindo verificar operações; não consegue localizar o tratamento nem acompanhar uma correção orientada. |

Não cobrar estética elaborada, biblioteca nova, relatório ou técnica de
responsividade não confirmada. A análise limita-se a uso legível e feedback.

### C4 — Compreensão individual · R8 e fluxo associado

| Nível | Evidência observável de cada pessoa |
|---|---|
| **Excelente** | Com consulta, acompanha um fluxo real tela → rota → DAO → banco → retorno e realiza ou prevê uma pequena intervenção equivalente já exemplificada, conferindo o efeito e distinguindo estado da tela de persistência. |
| **Bom** | Acompanha o fluxo e demonstra a intervenção, precisando de indicação pontual de arquivo/campo; depois explica o efeito e o teste com coerência. |
| **Regular** | Localiza parte do percurso e executa trecho com apoio frequente; ainda confunde função da rota/DAO, formato enviado/recebido ou evidência de persistência. Precisa de nova oportunidade equivalente. |
| **Insuficiente** | Mesmo com consulta e retomada orientada, não relaciona a operação demonstrada ao próprio código nem prevê seu efeito; evidência de domínio ainda não foi produzida. |

Registrar separadamente por estudante. Ausência, ansiedade ou falta de tempo
não comprovam desconhecimento: coletar outra evidência equivalente.
Aceitar fala, percurso apontado no código ou anotação/desenho com demonstração;
não pontuar rapidez, memória, quantidade de fala ou contribuição por commits.

### C5 — Processo e comunicação técnica · R8

| Nível | Evidência observável |
|---|---|
| **Excelente** | README permite instalar/executar sem segredo e informa URL, variáveis e decisão. Registros breves mostram teste, resultado e retomada; ambos participam de interface e API/DAO e conseguem localizar suas evidências. |
| **Bom** | Instruções e registros permitem conferir o trabalho; há uma omissão pequena, suprida pela dupla sem inviabilizar execução ou compreensão do processo. |
| **Regular** | Código é localizável, mas faltam instruções de execução ou evidências de teste; participação nas camadas e decisões exigem reconstrução com ajuda do professor. |
| **Insuficiente** | Não há instrução nem registro suficiente para reproduzir/verificar o trabalho; a dupla não consegue reconstruir execução e processo mesmo com apoio. |

