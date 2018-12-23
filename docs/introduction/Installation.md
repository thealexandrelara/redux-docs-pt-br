# Installation

Para instalar a versão estável:

```bash
npm install --save redux
```

Este exemplo assume que você está usando o [npm](https://www.npmjs.com/) como o seu gerenciador de pacotes.

Caso contrário, você pode [acessar estes arquivos no unpkg](https://unpkg.com/redux/), baixá-los, ou configurar o seu gerenciador de pacotes para apontar para eles.

Geralmente, as pessoas utilizam o Redux como uma coleção de módulos [CommonJS](http://webpack.github.io/docs/commonjs.html). Estes módulos são os que você recebe quando você importa o `redux` em um [Webpack](https://webpack.js.org/), [Browserify](http://browserify.org/), ou em um ambiente Node. Caso você goste de viver no limite e usa [Rollup](https://rollupjs.org), nós suportamos ele também.

Se você não usa um 'module bundler', também não há problema. O pacote npm do `redux` inclui builds [UMD](https://github.com/umdjs/umd) pré-compiladas para produção e desenvolvimento localizadas na [pasta `dist`](https://unpkg.com/redux/dist/). Elas podem ser utilizadas diretamente sem um bundler e por conta disso são compatíveis com muitos ambientes e 'module loaders' do JavaScript. Por exemplo, você pode utilizar uma build UMD com uma [tag `<script>`](https://unpkg.com/redux/dist/redux.js) na página, ou [instalar com o Bower](https://github.com/reduxjs/redux/pull/1181#issuecomment-167361975). As builds UMD permitem que o Redux fique disponível como uma variável global `window.Redux`.

O código fonte do Redux é escrito em ES2015 mas nós pré-compilamos com o CommonJS e builds UMD para o ES5, então ele funciona em [qualquer navegador moderno](http://caniuse.com/#feat=es5). Você não precisa usar o Babel ou qualquer 'module bundle' para [começar a usar o Redux](https://redux.js.org/introduction/examples#counter-vanilla).

## Pacotes Complementares

Most likely, you'll also need [the React bindings](https://github.com/reduxjs/react-redux) and [the developer tools](https://github.com/reduxjs/redux-devtools).

```bash
npm install --save react-redux
npm install --save-dev redux-devtools
```

Note that unlike Redux itself, many packages in the Redux ecosystem don't provide UMD builds, so we recommend using CommonJS module bundlers like [Webpack](https://webpack.js.org/) and [Browserify](http://browserify.org/) for the most comfortable development experience.
