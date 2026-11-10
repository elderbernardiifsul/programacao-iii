# Rubrica dos estudantes — Trabalho integrador: O repertório da turma

**Versão 3 · 10/11/2026.** Substitui a versão de entrega de 20/10/2026.  
**Programação III · IFSul — Campus Passo Fundo · Professor Élder F. F. Bernardi**  
**Tutor da atividade:** Prof. Leonardo Constantin  

[Página do trabalho](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/) · [Enunciado](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/enunciado.html)

> **O que mudou na versão 3**
>
> - **Nenhum critério mudou.** Os pesos, os valores e as tabelas de níveis são os mesmos da versão de 20/10/2026.
> - O título passou a usar o nome do trabalho: "O repertório da turma".
> - Há uma seção nova, "Como ler esta rubrica", e um glossário no fim.
> - As observações de cada critério foram reescritas em listas.

## Como ler esta rubrica

A rubrica diz como o professor transforma o que observa em pontos.

1. O trabalho tem cinco critérios: C1, C2, C3, C4 e C5.
2. Cada critério tem uma tabela com quatro níveis: Excelente, Bom, Regular e Insuficiente.
3. Cada nível descreve o que o professor observa no projeto.
4. Para se preparar, leiam o nível **Excelente** de cada critério. Depois, confiram se o projeto de vocês mostra o que está escrito ali.

O que vale para todos os critérios:

- Os critérios descrevem as evidências que serão observadas no núcleo do trabalho.
- O núcleo bem executado e compreendido permite nota máxima, com ou sem base de retomada, Vue ou funcionalidades extras.
- Não há desconto pelo apoio recebido.
- Não há avaliação por quantidade de código ou commits.

## Pesos e cálculo da pontuação

**Valor total: 4,0 pontos. Tutor da atividade: Prof. Leonardo Constantin.**

| Critério | Origem da evidência | Peso | Valor máximo |
|---|---|---|---|
| C1 — Integração e funcionamento | Dupla | 30% | 1,2 ponto |
| C2 — Persistência e publicação | Dupla | 20% | 0,8 ponto |
| C3 — Qualidade proporcional ao ensino | Dupla | 10% | 0,4 ponto |
| C4 — Compreensão | Individual | 30% | 1,2 ponto |
| C5 — Processo e comunicação | Dupla, com participação de ambos | 10% | 0,4 ponto |

**Como calcular:**

1. Em cada critério, o professor escolhe o nível que descreve o que observou.
2. Cada nível tem um fator: Excelente = 1; Bom = 0,75; Regular = 0,50; Insuficiente = 0,25.
3. A pontuação do critério é o valor máximo multiplicado pelo fator do nível.
4. A pontuação de cada estudante soma os quatro critérios da dupla (até 2,8 pontos) ao seu C4 individual (até 1,2 ponto).

Exemplo: nível Bom em C1 corresponde a `1,2 × 0,75 = 0,9 ponto`.

**Quando falta uma evidência:**

- Evidência ausente ou impedida fica pendente de verificação equivalente. O professor não conclui automaticamente que a pessoa não sabe.
- Uma falha externa ou ausência de evidência exige encaminhamento e nova conferência. Ela não equivale automaticamente a desconhecimento.

## Os cinco critérios

### C1 — Integração e funcionamento · R1–R4, R6

| Nível | Evidência observável |
|---|---|
| **Excelente** | Consulta, cadastro, edição no mesmo ID e exclusão funcionam pela interface com dados coerentes; cancelamento preserva registro; player do seed funciona e música sem partes tem estado claro, sem tentativa inválida de reprodução. |
| **Bom** | Percurso CRUD é demonstrável e preserva os dados corretos; há falha pontual de seleção/atualização visual ou estado do player, identificada e corrigível sem reconstruir o fluxo. |
| **Regular** | Demonstra leitura e ao menos uma escrita integrada; uma ou mais operações dependem de requisição manual, ou a interface diverge da API sem que a dupla consiga completar a conferência. |
| **Insuficiente** | Não apresenta leitura e escrita integradas verificáveis; alteração existe só na tela ou as ações indicam sucesso sem executar o percurso correspondente. |

**Observações sobre o C1:**

- O CRUD cotidiano acontece na interface.
- Chamadas manuais à API são apoio de diagnóstico. Elas não substituem a integração.
- Preservem a amostra para o player.

### C2 — Persistência e publicação · R2–R4, R7

| Nível | Evidência observável |
|---|---|
| **Excelente** | Na URL pública, a dupla cria, consulta, edita e exclui com banco; identifica o mesmo ID antes/depois de reiniciar o serviço e explica onde os dados ficam. Configuração é reproduzível, com segredos somente no servidor. |
| **Bom** | CRUD público com banco e persistência são demonstrados; falta um registro de conferência ou há ajuste pontual de configuração que a dupla identifica e conclui com orientação breve. |
| **Regular** | Banco funciona localmente, mas publicação ou teste após reinício ainda não é verificável; a dupla identifica parte da configuração e precisa de apoio para concluir a prova de persistência. |
| **Insuficiente** | A única evidência é dado em memória/lista local ou aplicação pública sem integração verificável ao banco; não distingue esses estados mesmo com consulta orientada. |

**Impedimento externo no C2:**

- Indisponibilidade não equivale a nível insuficiente.
- Registrem o impedimento, a evidência local com banco e as evidências anteriores.
- A verificação impedida fica pendente, conforme encaminhamento do professor.
- O objetivo de publicação com banco permanece. O impedimento não cria prazo novo nem penalidade nova.

### C3 — Qualidade proporcional ao ensino · R5, R8

| Nível | Evidência observável |
|---|---|
| **Excelente** | Entradas vazias não geram cadastro válido; sucesso depende da resposta; falha controlada gera mensagem útil sem esconder problema. Campos e ações são identificáveis e responsabilidades de tela, rota e DAO permanecem reconhecíveis. |
| **Bom** | Validação e distinção entre sucesso/erro funcionam; uma mensagem ou estado exige ajuste pequeno, sem impedir a pessoa de completar a operação e conferir o resultado. |
| **Regular** | Trata apenas parte das entradas/falhas; mensagem genérica ou lista desatualizada dificulta conferir resultado. Precisa de apoio para localizar onde validar ou tratar resposta. |
| **Insuficiente** | Aceita entradas obrigatórias inválidas ou anuncia sucesso na falha, impedindo verificar operações; não consegue localizar o tratamento nem acompanhar uma correção orientada. |

**Observações sobre o C3:**

- Este critério não cobra estética elaborada, biblioteca nova, relatório ou técnica de responsividade não confirmada.
- A análise limita-se a uso legível e feedback.

### C4 — Compreensão individual · R8 e fluxo associado

| Nível | Evidência observável de cada pessoa |
|---|---|
| **Excelente** | Com consulta, acompanha um fluxo real tela → rota → DAO → banco → retorno e realiza ou prevê uma pequena intervenção equivalente já exemplificada, conferindo o efeito e distinguindo estado da tela de persistência. |
| **Bom** | Acompanha o fluxo e demonstra a intervenção, precisando de indicação pontual de arquivo/campo; depois explica o efeito e o teste com coerência. |
| **Regular** | Localiza parte do percurso e executa trecho com apoio frequente; ainda confunde função da rota/DAO, formato enviado/recebido ou evidência de persistência. Precisa de nova oportunidade equivalente. |
| **Insuficiente** | Mesmo com consulta e retomada orientada, não relaciona a operação demonstrada ao próprio código nem prevê seu efeito; evidência de domínio ainda não foi produzida. |

**Observações sobre o C4:**

- O professor registra este critério separadamente por estudante.
- Ausência, ansiedade ou falta de tempo não comprovam desconhecimento. Nesses casos, o professor coleta outra evidência equivalente.
- Formas de resposta aceitas: fala, percurso apontado no código, ou anotação ou desenho com demonstração.
- Não são pontuados: rapidez, memória, quantidade de fala ou contribuição por commits.

### C5 — Processo e comunicação técnica · R8

| Nível | Evidência observável |
|---|---|
| **Excelente** | README permite instalar/executar sem segredo e informa URL, variáveis e decisão. Registros breves mostram teste, resultado e retomada; ambos participam de interface e API/DAO e conseguem localizar suas evidências. |
| **Bom** | Instruções e registros permitem conferir o trabalho; há uma omissão pequena, suprida pela dupla sem inviabilizar execução ou compreensão do processo. |
| **Regular** | Código é localizável, mas faltam instruções de execução ou evidências de teste; participação nas camadas e decisões exigem reconstrução com ajuda do professor. |
| **Insuficiente** | Não há instrução nem registro suficiente para reproduzir/verificar o trabalho; a dupla não consegue reconstruir execução e processo mesmo com apoio. |

## Glossário

As explicações abaixo valem para esta rubrica. O [Enunciado](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/enunciado.html) tem um glossário maior.

| Palavra | O que significa nesta rubrica |
|---|---|
| **Amostra** ou **seed** | A música com partes do repertório inicial, usada para demonstrar o player. O arquivo `seed.sql` inclui a música de exemplo. |
| **Com consulta** | A pessoa pode olhar o próprio código e os materiais de apoio enquanto responde. Não é o mesmo que consultar uma música na API. |
| **Evidência** | O que mostra que algo funciona ou foi compreendido. Exemplos: uma demonstração observada, um registro curto de teste, uma explicação. |
| **Fluxo** | O caminho tela → rota → DAO → banco → retorno. |
| **Intervenção** | Uma pequena mudança ou tarefa, de um dos tipos listados no Enunciado, na seção "O que cada integrante precisa compreender". |
| **Percurso CRUD** | A sequência de consultar, cadastrar, editar e excluir pela interface. |
| **Requisição manual** | Uma chamada à API feita fora da interface da aplicação. |
| **R1 a R8** | Os oito requisitos do núcleo. Estão no Enunciado, na seção "Núcleo do trabalho — R1 a R8". |
