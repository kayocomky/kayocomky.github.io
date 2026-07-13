# meu-blog

Blog estático feito com [Jekyll](https://jekyllrb.com/), pronto para publicar
de graça no [GitHub Pages](https://pages.github.com/).

## Estrutura

- `_config.yml` — configurações do site (título, descrição, autor).
- `index.md` — página inicial (lista os posts automaticamente).
- `about.md` — página "Sobre".
- `_posts/` — seus posts. Cada arquivo é `AAAA-MM-DD-titulo.md`.

## Como escrever um novo post

1. Crie um arquivo em `_posts/` chamado `AAAA-MM-DD-titulo-do-post.md`.
2. Copie o cabeçalho de um post existente (as linhas entre `---`).
3. Escreva o conteúdo em Markdown abaixo do cabeçalho.

## Como publicar de graça no GitHub Pages

### 1. Crie uma conta no GitHub (gratuita)

Acesse https://github.com/signup e crie sua conta, caso ainda não tenha uma.

### 2. Crie um repositório novo

- Clique em "New repository".
- Nome do repositório:
  - Se quiser o site em `https://SEU-USUARIO.github.io` (site pessoal),
    o nome do repositório **precisa ser exatamente** `SEU-USUARIO.github.io`.
  - Se preferir outro nome (ex: `meu-blog`), o site ficará em
    `https://SEU-USUARIO.github.io/meu-blog`.
- Deixe o repositório como **Public** (o GitHub Pages gratuito exige
  repositório público, a menos que você tenha GitHub Pro).
- Não adicione README/gitignore pelo GitHub (já temos aqui).

### 3. Envie este projeto para o repositório

Depois de criar o repositório, o GitHub vai te mostrar uma URL parecida com:
`https://github.com/SEU-USUARIO/NOME-DO-REPO.git`

Me avise o link do repositório (ou peça para eu rodar os comandos) que eu
preparo o `git init`, `commit` e `push` para você — só peço confirmação antes
de enviar (publicar) de fato.

Os comandos, para referência, são:

```bash
git init
git add .
git commit -m "Primeiro commit do blog"
git branch -M main
git remote add origin https://github.com/SEU-USUARIO/NOME-DO-REPO.git
git push -u origin main
```

### 4. Ative o GitHub Pages

- No repositório, vá em **Settings > Pages**.
- Em "Build and deployment", escolha **Deploy from a branch**.
- Branch: `main`, pasta: `/ (root)`. Salve.
- Aguarde 1-2 minutos. O link do site aparece na própria página de Pages.

### 5. Pronto!

Qualquer alteração que você fizer nos arquivos e enviar com `git push`
atualiza o blog automaticamente em alguns minutos. Não há custo nenhum
nesse processo.

## Visualizar no computador antes de publicar (opcional)

Isso exige instalar o [Ruby](https://www.ruby-lang.org/) — é opcional, só
serve para conferir como o site fica antes de publicar. Sem isso, você
também pode simplesmente publicar e conferir direto no link do GitHub Pages.

```bash
bundle install
bundle exec jekyll serve
```

Depois acesse http://localhost:4000 no navegador.
