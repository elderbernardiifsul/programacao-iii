# Guia do dia 1 — Repositório, Supabase e Render

**Trabalho integrador 2026 — O repertório da turma · Programação III**  
**Professor:** Élder F. F. Bernardi · **Tutor da atividade:** Prof. Leonardo Constantin

Hoje vocês **não vão programar**. Hoje é só deixar tudo funcionando:

1. o projeto no computador e no GitHub da dupla;
2. o banco de dados (Supabase);
3. o site no ar (Render).

**Como usar este guia**

- Façam **um passo por vez**, na ordem. Marquem o ☐ quando terminar.
- Travou? Cliquem no link **Ajuda** do passo. Ele abre a explicação completa.
- Continua travado depois de 10 minutos? **Chamem o professor.** Não fiquem parados.

---

## Parte 1 — O projeto

### ☐ Passo 1 — Conferir o Node

No terminal do VS Code:

```bash
node --version
```

**Deu certo se:** aparece `v22` ou um número maior.  
**Ajuda:** [Guia do Supabase, Etapa 0](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_supabase.html#etapa-0--antes-de-começar)

### ☐ Passo 2 — O projeto de vocês roda?

Abram a pasta do projeto no VS Code e rodem:

```bash
npm install
npm start
```

Abram `http://localhost:3000` no navegador.

- **Abriu a página do karaokê?** Ótimo. Vão para o passo 3.
- **Deu erro, ou vocês não acham o projeto?** Usem a **base de retomada**. Ela é um projeto pronto para começar, e **não tira nota**:
  1. Baixem a [base_retomada.zip](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/downloads/base_retomada.zip) e descompactem.
  2. Abram a pasta `base_retomada` no VS Code.
  3. Rodem `npm ci` no terminal.
  4. A base só abre no navegador depois da Parte 2. Sigam para o passo 3.

**Ajuda:** [Roteiro de retomada, 1. Preparar e executar](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/roteiro_retomada.html#1-preparar-e-executar)

### ☐ Passo 3 — O projeto está no GitHub da dupla?

```bash
git remote -v
```

Olhem o endereço que aparece:

| O que apareceu | O que fazer |
|---|---|
| Um endereço com o **usuário de vocês** | Está certo. Vão para o passo 4. |
| Um endereço com `elderbernardiifsul` | É o repositório da aula. Troquem para o de vocês: [Ajuda](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_supabase.html#15-o-repositório-da-dupla-no-github) |
| Nada, ou um erro | O projeto ainda não está no GitHub. Criem o repositório: [Ajuda](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_deploy_render.html#35-caso-especial-o-projeto-ainda-não-está-no-github) |

### ☐ Passo 4 — Os dois têm acesso?

1. Quem criou o repositório abre ele no GitHub: **Settings → Collaborators → Add people** e adiciona o colega.
2. O colega aceita o convite (chega por e-mail).
3. O colega baixa o projeto no computador dele com `git clone`.

**Deu certo se:** os dois abrem o projeto no próprio computador.  
**Ajuda:** [Guia do Supabase, 1.5](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_supabase.html#15-o-repositório-da-dupla-no-github) e [1.6](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_supabase.html#16-a-outra-pessoa-da-dupla)

---

## Parte 2 — O banco (Supabase)

### ☐ Passo 5 — Abrir o projeto no Supabase

Entrem em [supabase.com/dashboard](https://supabase.com/dashboard) com a conta do GitHub.

| O que vocês veem | O que fazer |
|---|---|
| O projeto da Unidade 3, funcionando | Vão para o passo 6. |
| O projeto está **pausado** | Cliquem em **Restore** e esperem alguns minutos. |
| Não tem projeto nenhum | Criem um novo: [Ajuda](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_supabase.html#43-caminho-4a--projeto-novo) |

### ☐ Passo 6 — Preparar as tabelas

No Supabase, abram o **SQL Editor**. Os arquivos estão na pasta `sql/` do projeto (ou nos [Downloads](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/index.html#downloads)). Para cada arquivo: copiem tudo, colem no editor e cliquem em **Run**.

**Projeto novo** (criado hoje):

1. `schema.sql`
2. `seed.sql`

**Projeto antigo** (da Unidade 3):

1. `diagnostico.sql` — olhem a coluna `situacao`.
2. Apareceu `ajustar`? Rodem o `ajustes.sql` e depois o `diagnostico.sql` de novo.
3. Apareceu `criar`? **Chamem o professor.**
4. `seed.sql`

**Atenção:** no projeto antigo, **não** rodem o `schema.sql`.

**Ajuda:** [projeto novo](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_supabase.html#43-caminho-4a--projeto-novo) · [projeto antigo](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_supabase.html#44-caminho-4b--projeto-da-unidade-3)

### ☐ Passo 7 — Conferir a música de exemplo

No Supabase, abram o **Table Editor** e cliquem na tabela `musicas`.

**Deu certo se:** aparece a música `Encontro da turma`.  
**Ajuda:** [Guia do Supabase, 4.5](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_supabase.html#45-conferir-no-table-editor)

### ☐ Passo 8 — Criar o arquivo `.env`

O `.env` guarda o endereço e a senha do banco.

1. No VS Code, façam uma cópia do arquivo `.env.example` e deem o nome `.env`.
2. No Supabase, cliquem no botão verde **Connect** e copiem a `SUPABASE_URL` e a `SUPABASE_SECRET_KEY`.
3. Colem os dois valores no `.env` e salvem.

> **A secret key é como uma senha.** Não mandem para ninguém: nem no grupo, nem em print, nem para a IA.

**Ajuda:** [onde achar a URL e a chave](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_supabase.html#54-onde-achar-a-url-e-a-secret-key) · [como preencher](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_supabase.html#55-preencher-o-env)

### ☐ Passo 9 — Testar

```bash
npm start
```

Abram `http://localhost:3000`.

**Deu certo se:** a música `Encontro da turma` aparece na lista.  
**Não apareceu?** Vejam os [erros comuns](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_supabase.html#socorro--erros-comuns) ou chamem o professor. Se o projeto de vocês ainda não usa o banco, é normal: mostrem ao professor em que etapa do [Guia do Supabase](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_supabase.html#sumário) vocês pararam.

---

## Parte 3 — O site no ar (Render)

### ☐ Passo 10 — Enviar o projeto para o GitHub

```bash
git add .
git commit -m "Projeto pronto para publicar"
git push
```

Depois, abram o repositório no site do GitHub.

**Deu certo se:** os arquivos estão lá e o `.env` **não** aparece.  
**O `.env` apareceu?** Parem e chamem o professor.  
**Ajuda:** [Guia de deploy, Etapa 3.3](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_deploy_render.html#33-a-conferência-que-salva-a-nota)

### ☐ Passo 11 — Entrar na Render

Entrem em [render.com](https://render.com) e escolham entrar **com o GitHub**.

**Pediu cartão de crédito?** Parem e chamem o professor. O trabalho é gratuito.  
**Ajuda:** [Guia de deploy, Etapa 4](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_deploy_render.html#etapa-4--criando-a-conta-na-render)

### ☐ Passo 12 — Criar o serviço

Cliquem em **+ New → Web Service** e escolham o repositório **da dupla**. Preencham assim:

| Campo | O que colocar |
|---|---|
| **Build Command** | `npm install` |
| **Start Command** | `npm start` |
| **Plano** | **$0 / month** |

**Ainda não cliquem no botão final.** Façam antes o passo 13.

**Ajuda:** [Guia de deploy, Etapa 5.2](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_deploy_render.html#52-preenchendo-o-formulário)

### ☐ Passo 13 — Colocar a URL e a chave do banco

No fim do mesmo formulário, em **Environment Variables**, criem **duas** variáveis. Os valores são os mesmos do `.env`:

| Key | Value |
|---|---|
| `SUPABASE_URL` | o valor que está no `.env` |
| `SUPABASE_SECRET_KEY` | o valor que está no `.env` |

Só essas duas. Não criem `PORT`.

**Ajuda:** [Guia de deploy, Etapa 6.2](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_deploy_render.html#62-como-resolver)

### ☐ Passo 14 — Publicar e testar

1. Cliquem em **Deploy web service**.
2. Esperem de 2 a 5 minutos, até aparecer `Your service is live`.
3. Cliquem no endereço que termina em `.onrender.com`.

**Deu certo se:** a página abre e mostra a lista de músicas.  
**Deu erro?** Vejam a [tabela de erros](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_deploy_render.html#etapa-10--socorro-erros-mais-comuns). Se o projeto não é a base de retomada, confiram também a [Etapa 2 do guia de deploy](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_deploy_render.html#etapa-2--duas-mudanças-no-código).

### ☐ Passo 15 — Guardar o endereço

Colem o endereço do site no `README.md` do projeto e enviem:

```bash
git add .
git commit -m "Endereço do site no README"
git push
```

---

## Antes de sair

- ☐ O projeto abre no computador dos dois.
- ☐ A música `Encontro da turma` aparece em `localhost:3000`.
- ☐ O site abre no endereço da Render.
- ☐ O endereço está no README.

**Não deu tempo de terminar?** Tudo bem. Anotem no README em qual passo pararam e qual foi o erro, e avisem o professor. No próximo encontro vocês continuam desse passo.

**Próximo encontro:** cadastrar uma música pela tela. Quem quiser adiantar a leitura: [Guia de interface — CRUD na tela com fetch](https://elderbernardiifsul.github.io/programacao-iii/integrador-2026/guia_interface_crud.html).
