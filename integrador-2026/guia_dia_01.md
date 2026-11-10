# Guia do dia 1 — Repositório, Supabase e Render

**Trabalho integrador 2026 — O repertório da turma · Programação III**  
**IFSul — Campus Passo Fundo · Ensino Médio Integrado — Técnico em Informática**  
**Professor:** Élder F. F. Bernardi · **Tutor da atividade:** Prof. Leonardo Constantin

Este guia é a lista do que fazer **hoje**, na ordem. Ele não substitui os guias: cada item aponta a seção do documento que explica o passo em detalhe. Abram o link quando precisarem do passo a passo; se o item já está feito, marquem e sigam.

Hoje vocês **não programam** o CRUD. O objetivo é deixar o terreno pronto:

- o projeto rodando no computador e guardado no repositório da dupla, com as duas pessoas com acesso;
- o banco no Supabase conferido e ligado ao projeto;
- o serviço na Render criado, com a URL anotada (ou o impedimento registrado).

Isso corresponde ao **marco M1 — Abrir e compreender** ([Ficha de marcos](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/ficha_marcos.html#aceites-e-atividades-por-marco)).

## 0. Escolher o ponto de partida

Leiam [Enunciado → De onde partir](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/enunciado.html#de-onde-partir) e decidam em dupla:

| Situação da dupla | Caminho de hoje |
|---|---|
| O projeto de vocês roda, já está no GitHub e já fala (ou quase) com o Supabase | **Caminho A** — seguir com o repositório que vocês já têm |
| O projeto não roda, se perdeu, ou está muito atrás | **Caminho B** — base de retomada |

A base de retomada é opcional, **não reduz a nota** e permite chegar ao nível excelente. Em dúvida, perguntem ao professor antes de começar: trocar de caminho no meio do dia custa caro.

## 1. Conferir as ferramentas (as duas pessoas)

- ☐ `node --version` mostra 22 ou mais; `git --version` responde; `git config user.name` mostra o **seu** nome. → [Guia do Supabase, Etapa 0](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_supabase.html#etapa-0--antes-de-começar)
- ☐ Extensão **REST Client** instalada no VS Code. → [Etapa 0 → Ferramentas](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_supabase.html#ferramentas)
- ☐ Conseguem entrar no GitHub, no Supabase e na Render (os dois últimos com **Continue with GitHub**).
- ☐ O agente de IA está configurado como tutor, com o `AGENTS.md` do projeto. → [Etapa 0 → O agente como tutor](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_supabase.html#o-agente-como-tutor)

## 2A. Caminho A — o repositório que vocês já têm

- ☐ `git remote -v` mostra o endereço do **repositório da dupla**, não o da aula (`elderbernardiifsul/aula-nodejs-...`).
  - Mostra o da aula? → [Guia do Supabase, 1.5 O repositório da dupla no GitHub](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_supabase.html#15-o-repositório-da-dupla-no-github)
  - Não mostra nada? → [Guia de deploy, 3.5 O projeto ainda não está no GitHub](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_deploy_render.html#35-caso-especial-o-projeto-ainda-não-está-no-github)
- ☐ A outra pessoa foi convidada como colaboradora, aceitou o convite e clonou o repositório. → [1.5 (último parágrafo)](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_supabase.html#15-o-repositório-da-dupla-no-github) e [1.6 A outra pessoa da dupla](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_supabase.html#16-a-outra-pessoa-da-dupla)
- ☐ Nos dois computadores: `git pull`, `npm install` e `npm start` sem erro.
- ☐ Localizar em que etapa do Guia do Supabase o projeto de vocês está (DAO em memória? já com banco?). → [Guia do Supabase, Qual caminho seguir](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_supabase.html#qual-caminho-seguir) e [Sumário](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_supabase.html#sumário)
- ☐ O `.gitignore` tem `node_modules` e `.env`. → [Guia do Supabase, 5.1](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_supabase.html#51-proteger-o-env-antes-de-criá-lo)
- ☐ Os arquivos que vocês usam estão no lugar esperado (`require` com o caminho certo). → [Guia do Supabase, Anexo — Correspondência de estruturas](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_supabase.html#anexo--correspondência-de-estruturas)

## 2B. Caminho B — a base de retomada

- ☐ Baixar e descompactar a [base_retomada.zip](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/downloads/base_retomada.zip); abrir a pasta `base_retomada` no VS Code e ler o `README.md`.
- ☐ Criar o repositório da dupla no GitHub (vazio, sem README) e enviar a base. → [Guia de deploy, 3.5](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_deploy_render.html#35-caso-especial-o-projeto-ainda-não-está-no-github)
  - Antes do `git add .`, confiram que ainda **não existe** `.env` na pasta, ou que `git status` não o lista. A base já traz o `.gitignore` certo.
- ☐ Convidar a outra pessoa como colaboradora; ela aceita, clona o repositório da dupla e roda `npm ci`. → [Guia do Supabase, 1.5](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_supabase.html#15-o-repositório-da-dupla-no-github) e [1.6](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_supabase.html#16-a-outra-pessoa-da-dupla)
- ☐ `npm ci` sem erro nos dois computadores. → [Roteiro de retomada, 1. Preparar e executar](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/roteiro_retomada.html#1-preparar-e-executar)
- ☐ Vieram do repositório da aula? Vejam onde cada arquivo foi parar na base. → [Roteiro, Se vocês vieram do repositório da aula](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/roteiro_retomada.html#se-vocês-vieram-do-repositório-da-aula)

O `npm start` da base só funciona depois do `.env` preenchido (item 3).

## 3. Supabase — banco conferido e ligado ao projeto

- ☐ Abrir o painel do projeto da Unidade 3. Está pausado? Cliquem em **Restore** e esperem o status **Healthy**. → [Guia do Supabase, 4.4](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_supabase.html#44-caminho-4b--projeto-da-unidade-3)
- ☐ Escolher **4A** (projeto novo) ou **4B** (projeto da Unidade 3). Em dúvida, 4A. → [4.2 Qual caminho seguir](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_supabase.html#42-qual-caminho-seguir)
- ☐ Rodar os SQL no **SQL Editor**, na ordem do caminho escolhido. Os arquivos estão na pasta `sql/` do projeto e nos [Downloads da página do trabalho](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/index.html#downloads).
  - **4A:** `schema.sql` → `seed.sql` → consulta de conferência → `diagnostico.sql` com 20 linhas `ok`. → [4.3](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_supabase.html#43-caminho-4a--projeto-novo)
  - **4B:** `diagnostico.sql` → se houver `ajustar`, `ajustes.sql` → `diagnostico.sql` de novo → `seed.sql`. **Não** rodem o `schema.sql` num banco que já tem as tabelas. → [4.4](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_supabase.html#44-caminho-4b--projeto-da-unidade-3)
- ☐ No **Table Editor**: tabelas `artistas`, `musicas` e `partes`, e a música `Encontro da turma`. → [4.5](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_supabase.html#45-conferir-no-table-editor)
- ☐ Criar o `.env` a partir do `.env.example` e preencher `SUPABASE_URL` e `SUPABASE_SECRET_KEY`. → [5.3](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_supabase.html#53-o-arquivo-envexample), [5.4 Onde achar a URL e a secret key](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_supabase.html#54-onde-achar-a-url-e-a-secret-key) e [5.5](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_supabase.html#55-preencher-o-env)
- ☐ `git status` **não** lista o `.env`.
- ☐ Testar a conexão:
  - **Base de retomada:** `npm start`, abrir `http://localhost:3000` e ver a lista com `Encontro da turma`; selecionar e tocar. → [Roteiro, 1. Preparar e executar, passo 6](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/roteiro_retomada.html#1-preparar-e-executar)
  - **Projeto próprio:** `node testes/teste_conexao.js` (se ainda não existe, ele está na [5.7](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_supabase.html#57-o-teste-de-conexão)) e depois `npm start`.
- ☐ Deu erro? → [Guia do Supabase, Socorro — erros comuns](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_supabase.html#socorro--erros-comuns)

> **A secret key é segredo.** Ela não vai para o GitHub, para print, para o grupo da turma nem para a conversa com o agente. Se vazar, troquem a chave: [Guia do Supabase, 5.5 (quadro "Cuidado")](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_supabase.html#55-preencher-o-env).

## 4. Render — o serviço criado e a URL anotada

**Antes de publicar, no código:**

- ☐ `package.json` com script `start`; `engines` com `"node": ">=22"`; `app.js` lendo a porta de `process.env.PORT`. → [Guia de deploy, Etapa 1](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_deploy_render.html#etapa-1--conferindo-o-projeto-antes-de-publicar) e [Etapa 2](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_deploy_render.html#etapa-2--duas-mudanças-no-código)
  - Na base de retomada esses três itens **já estão prontos**: só confiram.
- ☐ Tudo commitado e enviado (`git push`). No GitHub, o `.env` **não** aparece. → [Etapa 3.3 A conferência que salva a nota](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_deploy_render.html#33-a-conferência-que-salva-a-nota)

**Na Render:**

- ☐ Conta criada com o GitHub e e-mail confirmado. → [Etapa 4](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_deploy_render.html#etapa-4--criando-a-conta-na-render)
- ☐ Novo **Web Service** apontando para o repositório **da dupla**. → [Etapa 5.1](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_deploy_render.html#51-começando)
- ☐ Formulário conferido campo a campo. → [Etapa 5.2](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_deploy_render.html#52-preenchendo-o-formulário)
  - **Build Command:** `npm ci` (base) ou `npm install` (projeto próprio).
  - **Start Command:** `npm start` (apaguem o `node index.js` que a Render sugere).
  - **Region:** Ohio.
- ☐ Plano **$0 / month** selecionado. Se pedir cartão, parem e chamem o professor. → [Etapa 5.3](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_deploy_render.html#53-escolhendo-o-plano)
- ☐ **Exatamente duas** variáveis de ambiente: `SUPABASE_URL` e `SUPABASE_SECRET_KEY`, com os valores do `.env`. **Sem** `PORT`. → [Etapa 6.2](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_deploy_render.html#62-como-resolver) e [6.3 Cuidados](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_deploy_render.html#63-cuidados)
- ☐ Acompanhar os logs até `Your service is live`. → [Etapa 7](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_deploy_render.html#etapa-7--acompanhando-o-primeiro-deploy)
- ☐ Abrir a URL pública e ver a lista de músicas. → [Etapa 8.1](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_deploy_render.html#81-a-página-do-karaokê)
- ☐ Deploy falhou? → [Etapa 10 — Socorro](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_deploy_render.html#etapa-10--socorro-erros-mais-comuns). Três falhas seguidas com erro fora da tabela: chamem o professor.

**Já tinham um serviço na Render?** Confiram que ele aponta para o repositório e a branch certos, que as duas variáveis batem com o `.env` de hoje (se trocaram de projeto no Supabase, elas mudaram) e que o último deploy ficou **Live**. → [Etapa 6.2, "Depois que o serviço existe"](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_deploy_render.html#62-como-resolver) e [Etapa 9.1](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_deploy_render.html#91-publicação-automática)

## 5. Antes de sair — fechamento do dia

- ☐ As duas pessoas sabem apontar o caminho **tela → rota → DAO → banco** no código. → [Roteiro, 2. Encontrar cada responsabilidade](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/roteiro_retomada.html#2-encontrar-cada-responsabilidade) ou [Guia do Supabase, 1.4 Quem importa quem](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_supabase.html#14-quem-importa-quem)
- ☐ O README da dupla tem: como executar, a URL pública (ou o impedimento) e o caminho escolhido (A ou B).
- ☐ Ficha de marcos preenchida: identificação da dupla, repositório, URL, base usada e diagnóstico inicial. → [Ficha de marcos, Identificação da dupla](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/ficha_marcos.html#identificação-da-dupla)
- ☐ Algo travou? Registrem no README a data, a etapa, o erro (sem segredos) e o que tentaram. → [Enunciado, Se houver impedimento técnico](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/enunciado.html#se-houver-impedimento-técnico)
- ☐ Último `git push` do dia feito.

**Extraclasse (até 60 min):** revisar o mapa dos arquivos, completar as instruções de execução no README e anotar a próxima dúvida. → [Ficha de marcos, Aceites e atividades por marco (M1)](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/ficha_marcos.html#aceites-e-atividades-por-marco)

**Próximo encontro:** cadastro pela tela (R2 e R5). → [Roteiro, 4. Integrar cadastro](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/roteiro_retomada.html#4-integrar-cadastro--r2-e-r5) e [Guia de interface — CRUD na tela com fetch](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_interface_crud.html)

> **Pergunte ao agente** citando o documento e a seção, com o endereço do `.md`. Exemplo: "Estou no item 3 do Guia do dia 1 (https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_dia_01.md). O diagnóstico mostrou `ajustar` em `partes → musicas`. O que isso quer dizer?"
