# Vue & Nuxt

- Introdução ao VueJS e NuxtJS | Teoria e prática - Cataline
- Com o Nuxt.js você produz muito com extrema elegância em muito pouco tempo

## Configuração da compilação

```bash
# instala dependências
$ npm install

# serve com hot reload em localhost:3000
$ npm run dev

# build para produção e servidor de lançamento
$ npm run build
$ npm run start

# gera projeto estático
$ npm run generate
```

Para uma explicação detalhada de como as coisas funcionam, confira a [documentação](https://nuxtjs.org).

## Diretórios especiais

Você pode criar os seguintes diretórios extras, alguns dos quais possuem comportamentos especiais. Somente `pages` é necessário; você pode excluí-los se não quiser usar sua funcionalidade.

### `assets`

O diretório de recursos contém seus recursos não compilados, como arquivos Stylus ou Sass, imagens ou fontes.

Mais informações sobre o uso deste diretório na [documentação](https://nuxtjs.org/docs/2.x/directory-structure/assets).

### `componentes`

O diretório de componentes contém seus componentes Vue.js. Os componentes compõem as diferentes partes da sua página e podem ser reutilizados e importados para suas páginas, layouts e até mesmo outros componentes.

Mais informações sobre o uso deste diretório na [documentação](https://nuxtjs.org/docs/2.x/directory-structure/components).

### `pages`

Esse diretório contém as exibições e rotas do aplicativo. O Nuxt lerá todos os arquivos `*.vue` dentro deste diretório e configurará o Vue Router automaticamente.

Mais informações sobre o uso deste diretório na [documentação](https://nuxtjs.org/docs/2.x/get-started/routing).

### `plugins`

O diretório plugins contém plugins JavaScript que você deseja executar antes de instanciar o aplicativo Vue.js raiz. Este é o lugar para adicionar plugins Vue e injetar funções ou constantes. Toda vez que você precisar usar `Vue.use()`, você deve criar um arquivo em `plugins/` e adicionar seu caminho para plugins em `nuxt.config.js`.

Mais informações sobre o uso deste diretório na [documentação](https://nuxtjs.org/docs/2.x/directory-structure/plugins).

### `static`

Este diretório contém seus arquivos estáticos. Cada arquivo dentro deste diretório é mapeado para `/`.

Exemplo: `/static/robots.txt` é mapeado como `/robots.txt`.

Mais informações sobre o uso deste diretório na [documentação](https://nuxtjs.org/docs/2.x/directory-structure/static).
