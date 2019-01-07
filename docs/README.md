# <a href='http://redux.js.org'><img src='https://camo.githubusercontent.com/f28b5bc7822f1b7bb28a96d8d09e7d79169248fc/687474703a2f2f692e696d6775722e636f6d2f4a65567164514d2e706e67' height='60' alt='Redux Logo' aria-label='redux.js.org' /></a>

O Redux é um contêiner de estado previsível para aplicativos JavaScript.
(Não confundir com um framework WordPress - [Redux Framework](https://reduxframework.com/).)

Ele ajuda você a escrever aplicativos que se comportam de maneira consistente, executados em diferentes ambientes (cliente, servidor e nativo) e são fáceis de testar. Além disso, oferece uma ótima experiência de desenvolvedor, como [edição de código ao vivo combinada com um depurador de viagem no tempo](https://github.com/reduxjs/redux-devtools).

Você pode usar o Redux junto com o [React](https://reactjs.org), ou com qualquer outra biblioteca de view.
É minúsculo (2kB, incluindo dependências).

> ** Nota **: No momento, estamos planejando uma reescrita da documentação do Redux. Reserve um tempo para ** [preencher esta pesquisa sobre qual conteúdo é mais importante em um site de documentação](https://docs.google.com/forms/d/e/1FAIpQLSfzIkY3fXZ8PrQKScYMK0YoEgALfAK2qQ0mOj1_ibKv2qDTuQ/viewform) **. Obrigado!

[![build status](https://img.shields.io/travis/reduxjs/redux/master.svg?style=flat-square)](https://travis-ci.org/reduxjs/redux)

[![npm version](https://img.shields.io/npm/v/redux.svg?style=flat-square)](https://www.npmjs.com/package/redux)

[![npm downloads](https://img.shields.io/npm/dm/redux.svg?style=flat-square)](https://www.npmjs.com/package/redux)

[![redux channel on discord](https://img.shields.io/badge/discord-%23redux%20%40%20reactiflux-61dafb.svg?style=flat-square)](https://discord.gg/0ZcbPKXt5bZ6au5t)

[![Changelog #187](https://img.shields.io/badge/changelog-%23187-lightgrey.svg?style=flat-square)](https://changelog.com/187)

## Aprenda Redux

emos uma variedade de recursos disponíveis para ajudá-lo a aprender Redux, não importa qual seja o seu background ou estilo de aprendizado.

### Apenas o básico

Se você é novato no Redux e quer entender os conceitos básicos, veja:

- A **[Motivação](./Motivation.md)** por trás da construção do Redux, os **[Conceitos Principais](./CoreConcepts.md)**, e os **[Três Princípios](./ThreePrinciples.md)**.
- O **[tutorial básico na documentação do Redux](../basics/README.md)**
- **[Série de vídeos "Getting Started with Redux"](https://egghead.io/series/getting-started-with-redux)** grátis no Egghead.io do criador do Redux, Dan Abramov
- **[O slideshow "Redux Fundamentals"](http://blog.isquaredsoftware.com/2018/03/presentation-reactathon-redux-fundamentals/)** e a **[lista de recursos sugeridos para aprender Redux](http://blog.isquaredsoftware.com/2017/12/blogged-answers-learn-redux/)** do co-mantenedor do Redux, Mark Erikson
- Se você aprende melhor olhando o código e "brincando" com ele, cheque nossa lista de **[exemplos de aplicações Redux](./Examples.md)**, disponíveis como projetos separados no repositório do Redux, e também como exemplos online interativos no CodeSandbox.
- A seção **[Tutoriais do Redux](https://github.com/markerikson/react-redux-links/blob/master/redux-tutorials.md)** da **[lista de links React/Redux](https://github.com/markerikson/react-redux-links)**. Aqui está uma lista dos nossos tutoriais recomendados:
  - Os posts de Dave Ceddia: [What Does Redux Do? (and when should you use it?)](https://daveceddia.com/what-does-redux-do/) e [How Redux Works: A Counter-Example](https://daveceddia.com/how-does-redux-work/) são uma grande introdução para o básico de Redux e como usar ele com React, como este post [React and Redux: An Introduction](http://jakesidsmith.com/blog/post/2017-11-18-redux-and-react-an-introduction/).
  - O post de Valentino Gagliardi: [React Redux Tutorial for Beginners: Learning Redux in 2018](https://www.valentinog.com/blog/react-redux-tutorial-beginners/) é uma excelente introdução mais extensa sobre muitos aspectos de uso do Redux.
  - O artigo do CSS Tricks [Leveling Up with React: Redux](https://css-tricks.com/learning-react-redux/) abrange bem o básico de Redux.
  - O tutorial [DevGuides: Introduction to Redux](http://devguides.io/redux/) aborda vários aspectos do Redux, incluindo actions, reducers, uso com o React e middleware.

### Conceitos intermediários

Depois de ter aprendido as noções básicas de como trabalhar com actions, reducers e store, você pode ter perguntas sobre tópicos tais como trabalhar com lógica assíncrona e solicitações AJAX, conectar uma estrutura de interface do usuário como React ao seu armazenamento Redux e configurar um aplicativo para usar o Redux:

- A **["seção da documentação de conceitos Avançados](../advanced/README.md)** abrange detalhes sobre como trabalhar com lógica assíncrona, middleware e rotas.
- A página de documentação do Redux **["Recursos de Aprendizagem"](./LearningResources.md)** aponta para artigos recomendados sobre uma variedade de tópicos relacionados ao Redux.
- A série em 8 partes de Sophie DeBenedetto **Criando um aplicativo CRUD simples com React + Redux](http://www.thegreatcodeadventure.com/building-a-simple-crud-app-with-react-redux-part-1/)** mostra como montar um aplicativo CRUD básico a partir do zero.

### Uso no Mundo Real

Going from a TodoMVC app to a real production application can be a big jump, but we've got plenty of resources to help:

- Redux creator Dan Abramov's **[free "Building React Applications with Idiomatic Redux" video series](https://egghead.io/courses/building-react-applications-with-idiomatic-redux)** builds on his first video series and covers topics like middleware, routing, and persistence.
- The **[Redux FAQ](https://redux.js.org/faq)** answers many common questions about how to use Redux, and the **["Recipes" docs section](https://redux.js.org/recipes)** has information on handling derived data, testing, structuring reducer logic, and reducing boilerplate.
- Redux co-maintainer Mark Erikson's **["Practical Redux" tutorial series](http://blog.isquaredsoftware.com/series/practical-redux/)** demonstrates real-world intermediate and advanced techniques for working with React and Redux (also available as **[an interactive course on Educative.io](https://www.educative.io/collection/5687753853370368/5707702298738688)**).
- The **[React/Redux links list](https://github.com/markerikson/react-redux-links)** has categorized articles on working with [reducers and selectors](https://github.com/markerikson/react-redux-links/blob/master/redux-reducers-selectors.md), [managing side effects](https://github.com/markerikson/react-redux-links/blob/master/redux-side-effects.md), [Redux architecture and best practices](https://github.com/markerikson/react-redux-links/blob/master/redux-architecture.md), and more.
- Our community has created thousands of Redux-related libraries, addons, and tools. The **["Ecosystem" docs page](https://redux.js.org/introduction/ecosystem)** lists our recommendations, and there's a complete listing available in the **[Redux addons catalog](https://github.com/markerikson/redux-ecosystem-links)**.
- If you're looking to learn from actual application codebases, the addons catalog also has a list of **[purpose-built examples and real-world applications](https://github.com/markerikson/redux-ecosystem-links/blob/master/apps-and-examples.md)**.

Finally, Mark Erikson is teaching a series of **[Redux workshops through Workshop.me](#redux-workshops)**. Check the [workshop schedule](https://workshop.me/?a=mark) for upcoming dates and locations.

## Ajuda e Discussão

O **[canal #redux](https://discord.gg/0ZcbPKXt5bZ6au5t)** da **[comunidade Reactiflux no Discord](http://www.reactiflux.com)** é nosso recurso oficial para todas as questões relacionadas com aprender e usar o Redux. Reactiflux é um ótimo lugar para sair, fazer perguntas e aprender - venha se juntar a nós!

You can also ask questions on [Stack Overflow](https://stackoverflow.com) using the **[#redux tag](https://stackoverflow.com/questions/tagged/redux)**.

## Antes de prosseguir

O Redux é uma ferramenta valiosa para organizar seu estado, mas você também deve considerar se é apropriado para sua situação. ** Não use o Redux só porque alguém disse que você deveria - tire um tempo para entender os potenciais benefícios e desvantagens de usá-lo **.

Aqui estão algumas sugestões sobre quando faz sentido usar o Redux:

- Você tem quantidades razoáveis ​​de dados mudando ao longo do tempo
- Você precisa de uma única fonte de verdade para o seu estado
- Você acha que manter todo o seu estado em um componente de nível superior não é mais suficiente

Sim, essas diretrizes são subjetivas e vagas, mas isso é por um bom motivo. O momento em que você deve integrar o Redux em seu aplicativo é diferente para cada usuário e diferente para cada aplicativo.

> **For more thoughts on how Redux is meant to be used, see:**<br>
>
> - **[You Might Not Need Redux](https://medium.com/@dan_abramov/you-might-not-need-redux-be46360cf367)**<br>
> - **[The Tao of Redux, Part 1 - Implementation and Intent](http://blog.isquaredsoftware.com/2017/05/idiomatic-redux-tao-of-redux-part-1/)**<br>
> - **[The Tao of Redux, Part 2 - Practice and Philosophy](http://blog.isquaredsoftware.com/2017/05/idiomatic-redux-tao-of-redux-part-2/)**
> - **[Redux FAQ](https://redux.js.org/faq)**

## Experiência do desenvolvedor

Dan Abramov (autor do Redux) escreveu Redux enquanto trabalhava em sua palestra na React Europe chamada ["Hot Reloading with Time Travel"](https://www.youtube.com/watch?v=xsSnOQynTHs). Seu objetivo era criar uma biblioteca de gerenciamento de estado com uma API mínima, mas um comportamento completamente previsível. O Redux possibilita a implementação de logging, hot reloading, time travel, aplicativos universais, gravação e reprodução, sem qualquer participação do desenvolvedor.

## Influências

O Redux desenvolve as idéias do [Flux](http://facebook.github.io/flux/), mas evita sua complexidade pegando sugestões do [Elm] (https://github.com/evancz/elm-architecture-tutorial /).
Mesmo se você nunca usou Flux ou Elm, o Redux leva apenas alguns minutos para começar.

## Instalação

Para instalar a versão estável:

`` `sh npm install --save redux `` `

Isso pressupõe que você está usando [npm](https://www.npmjs.com/) como seu gerenciador de pacotes.

Se não estiver, você pode [acessar esses arquivos no unpkg](https://unpkg.com/redux/), baixá-los ou apontar seu gerenciador de pacotes para eles.

Geralmente, as pessoas consomem o Redux como uma coleção de módulos [CommonJS](https://github.com/webpack/docs/wiki/commonjs). Estes módulos são o que você obtém quando importa o `redux` em um [Webpack](https://webpack.js.org/), [Browserify](http://browserify.org/) ou um ambiente Node. Se você gosta de viver no limite e usar o [Rollup](https://rollupjs.org), também damos suporte a isso.

Se você não usa um module bundler, também está tranquilo. O pacote npm do `redux` inclui builds de produção e desenvolvimento pré-compilados [UMD](https://github.com/umdjs/umd) na pasta [`dist`](https://unpkg.com/redux/dist/) . Eles podem ser usados ​​diretamente sem um bundler e, portanto, são compatíveis com muitos module loaders e ambientes JavaScript populares. Por exemplo, você pode usar uma build UMD como uma tag [`<script>`](https://unpkg.com/redux/dist/redux.js) na página, ou [pedir ao Bower para instalá-la] (https : //github.com/reduxjs/redux/pull/1181#issuecomment-167361975). As builds do UMD tornam o Redux disponível como uma variável global `window.Redux`.

O código-fonte do Redux é escrito no ES2015, mas nós pré-compilamos o CommonJS e o UMD para o ES5 para que funcionem em [qualquer navegador moderno](http://caniuse.com/#feat=es5). Você não precisa usar o Babel ou um module bundler para [começar com o Redux](https://github.com/reduxjs/redux/blob/master/examples/counter-vanilla/index.html).

### Pacotes Complementares

Provavelmente, você também precisará dos [bindings do React](https://github.com/reduxjs/react-redux) e [as ferramentas do desenvolvedor](https://github.com/reduxjs/redux-devtools).

```sh
npm install --save react-redux
npm install --save-dev redux-devtools
```

Note que, diferentemente do próprio Redux, muitos pacotes no ecossistema Redux não fornecem builds UMD, então recomendamos o uso de module bundlers do CommonJS tipo [Webpack](https://webpack.js.org/) e [Browserify] (http: / /browserify.org/) para a experiência de desenvolvimento mais confortável.

## A Essência

Todo o estado do seu aplicativo é armazenado em uma árvore de objetos dentro de uma única _store_.

A única maneira de alterar a árvore de estados é emitir um _action_, um objeto descrevendo o que aconteceu.

Para especificar como as ações transformam a árvore de estados, você escreve _reducers_.

E é isso!

```js
import { createStore } from "redux";

/**
 * Este é um reducer, uma função pura com a assinatura (state, action) => state.
 * Ela descreve como uma ação transforma o estado atual em um novo estado.
 *
 * A forma do estado depende de você: ele pode ser um valor primitivo, um array, um objeto ou mesmo uma estrutura de dados do Immutable.js. A única parte importante é que você nunca deve
 * mutar o objeto do estado, mas sim, retornar um novo objeto se o estado mudar.
 *
 * Neste exemplo, nós usaremos o  `switch` e strings, mas você pode usar um helper que
 * segue uma convenção diferente (por exemplo, funções de mapeamento) se fizer sentido para o seu projeto
 *
 */
function counter(state = 0, action) {
  switch (action.type) {
    case "INCREMENT":
      return state + 1;
    case "DECREMENT":
      return state - 1;
    default:
      return state;
  }
}

// Crie uma store do Redux que manterá o estado do seu App.
// A API dela é { subscribe, dispatch, getState }.
let store = createStore(counter);

// Você pode usar o subscribe() para atualizar a UI em resposta à mudanças no estado.
// Normalmente, você usaria uma biblioteca de binding na view (e.g. React Redux) ao invés de usar o subscribe() diretamente.
// Entretanto, isto pode ser útil para persistir o estado atual no localStorage.

store.subscribe(() => console.log(store.getState()));

// A única forma de mutar o estado interno é através do dispatch de uma ação.
// As ações podem ser serializadas, colocadas em log ou armazenadas e posteriormente reexecutadas.
store.dispatch({ type: "INCREMENT" });
// 1
store.dispatch({ type: "INCREMENT" });
// 2
store.dispatch({ type: "DECREMENT" });
// 1
```

Ao invés de mutar o estado diretamente, você especifica as mutações que você quer que ocorra com objetos planos chamados _actions_. Então você escreve uma função especial chamadaThen _reducer_ para decidir como cada action transforma o estado inteiro da aplicação.

Em um app típico usando Redux, há somente uma única store com uma única função redutora. Porém, à medida que seu app cresce, você irá dividir o seu reducer raíz em reducers menores que irão operar independentemente e em diferentes partes da árvore de estado. Isto é exatamente da mesma forma em que há apenas um componente raiz em um aplicativo React, mas ele é composto de muitos componentes pequenos.

Essa arquitetura pode parecer um exagero para um aplicativo criado somente com um contador, mas a beleza desse padrão é como ele é escalável para aplicativos grandes e complexos. Ele também permite ferramentas de desenvolvedor muito poderosas, porque é possível rastrear cada mutação para a ação que ocasionou ela. Você pode gravar sessões do usuário e reproduzi-las apenas reproduzindo cada ação.

## Aprenda Redux por seus Autores

### Tutoriais em Vídeo de Redux por Dan Abramov

#### Getting Started with Redux

**[Getting Started with Redux](https://egghead.io/series/getting-started-with-redux)** é um curso em vídeo composto por 30 vídeos narrados por [Dan Abramov](https://twitter.com/dan_abramov), autor de Redux. Ele foi desenvolvido para complementar a parte “Básica” da documentação, trazendo insights adicionais sobre imutabilidade, testes, melhores práticas do Redux e usando o Redux com o React. **Este curso é e sempre será gratuito.**

> [“Great course on egghead.io by @dan_abramov - instead of just showing you how to use #redux, it also shows how and why redux was built!”](https://twitter.com/sandrinodm/status/670548531422326785)  
> Sandrino Di Mattia

> [“Plowing through @dan_abramov 'Getting Started with Redux' - its amazing how much simpler concepts get with video.”](https://twitter.com/chrisdhanaraj/status/670328025553219584)  
> Chris Dhanaraj

> [“This video series on Redux by @dan_abramov on @eggheadio is spectacular!”](https://twitter.com/eddiezane/status/670333133242408960)  
> Eddie Zaneski

> [“Come for the name hype. Stay for the rock solid fundamentals. (Thanks, and great job @dan_abramov and @eggheadio!)”](https://twitter.com/danott/status/669909126554607617)  
> Dan

> [“This series of videos on Redux by @dan_abramov is repeatedly blowing my mind - gunna do some serious refactoring”](https://twitter.com/gelatindesign/status/669658358643892224)  
> Laurence Roberts

Então, o que você está esperando?

#### [Assista à série de vídeos gratuita "Getting Started with Redux"](https://egghead.io/series/getting-started-with-redux)

> Nota: Se você gostou do curso de Dan, considere apoiar o Egghead [fazendo uma assinatura](https://egghead.io/pricing). Os inscritos têm acesso ao código-fonte de todos os exemplos em meus vídeos e muitas lições avançadas sobre outros tópicos, incluindo JavaScript em profundidade, Reaçt, Angular e muito mais. Muitos [instrutores de Egghead](https://egghead.io/instructors) também são autores de bibliotecas de código aberto, portanto, fazer uma assinatura é uma boa maneira de agradecer-lhes pelo trabalho que fizeram.

#### Building React Applications with Idiomatic Redux

O curso **[Building React Applications with Idiomatic Redux](https://egghead.io/courses/building-react-applications-with-idiomatic-redux)**
é uma segunda série de vídeos gratuitos de Dan Abramov. Ele começa de onde a primeira série parou e abrange técnicas prontas para serem usadas em produção para a construção de suas aplicações React e Redux: gerenciamento avançado de estado, middleware, integração com o React Router e outros problemas comuns que você provavelmente encontrará ao criar aplicativos para seus clientes. Como na primeira série, ** este curso será sempre gratuito **.

#### [Assista a série de vídeos grátis "Idiomatic Redux"](https://egghead.io/courses/building-react-applications-with-idiomatic-redux)

### Practical Redux course

**[Redux na Prática](https://www.educative.io/collection/5687753853370368/5707702298738688/) ** é um curso interativo pago pelo co-mantenedor do Redux [Mark Erikson](https://twitter.com/acemarke). O curso foi desenvolvido para mostrar como aplicar os conceitos básicos do Redux para construir algo maior que um aplicativo TodoMVC. Inclui tópicos do mundo real como:

- Adicionando o Redux a um novo projeto Create-React-App e configurando o Hot Module Replacement para um desenvolvimento mais rápido
- Controlando o comportamento da interface do usuário com o Redux
- Usando a biblioteca Redux-ORM para gerenciar dados relacionais em sua store
- Construindo uma view principal/de detalhe para exibir e editar dados
- Escrevendo lógica avançada do reducer para resolver problemas específicos
- Otimizando o desempenho de entradas de formulário conectadas ao Redux

E muito mais!

### Redux Fundamentals Workshop

O co-mantenedor do Redux [Mark Erikson](https://twitter.com/acemarke) montou um [**Redux Fundamentals workshop**, e os slides estão disponíveis aqui](https://blog.isquaredsoftware.com/2018/06/redux-fundamentos-oficina-slides/). Eles cobrem:

- A história e propósito do Redux
- Reducers e actions, e trabalhando com uma store do Redux
- Usando Redux com React
- Usando e escrevendo o middleware Redux
- Trabalhando com chamadas AJAX e outros efeitos colaterais
- Teste de unidade de aplicativos Redux
- Estrutura e desenvolvimento de aplicativos do Redux no mundo real

## Documentação

- [Introdução](http://redux.js.org/introduction/index.html)
- [Básico](http://redux.js.org/basics/index.html)
- [Avançado](http://redux.js.org/advanced/index.html)
- [Recipes](http://redux.js.org/recipes/index.html)
- [FAQ](http://redux.js.org/FAQ.html)
- [Solução de problemas](http://redux.js.org/Troubleshooting.html)
- [Glossário](http://redux.js.org/Glossary.html)
- [Referências da API](http://redux.js.org/api/index.html)

Para exportações em PDF, ePub e MOBI para leitura off-line e instruções sobre como criá-las, consulte: [paulkogel / redux-offline-docs](https://github.com/paulkogel/redux-offline-docs).

Para a documentação off-line, consulte: [devdocs][devdocs](http://devdocs.io/redux/)

## Exemplos

Quase todos os exemplos têm uma sandbox do CodeSandbox. Isto é uma versão interativa do código que você pode "brincar" online.

- [**Counter Vanilla**](https://redux.js.org/introduction/examples#counter-vanilla): [Source](https://github.com/reduxjs/redux/tree/master/examples/counter-vanilla)
- [**Counter**](https://redux.js.org/introduction/examples#counter): [Source](https://github.com/reduxjs/redux/tree/master/examples/counter) | [Sandbox](https://codesandbox.io/s/github/reduxjs/redux/tree/master/examples/counter)
- [**Todos**](https://redux.js.org/introduction/examples#todos): [Source](https://github.com/reduxjs/redux/tree/master/examples/todos) | [Sandbox](https://codesandbox.io/s/github/reduxjs/redux/tree/master/examples/todos)
- [**Todos with Undo**](https://redux.js.org/introduction/examples#todos-with-undo): [Source](https://github.com/reduxjs/redux/tree/master/examples/todos-with-undo) | [Sandbox](https://codesandbox.io/s/github/reduxjs/redux/tree/master/examples/todos-with-undo)
- [**Todos w/ Flow**](https://redux.js.org/introduction/examples#todos-flow): [Source](https://github.com/reduxjs/redux/tree/master/examples/todos-flow)
- [**TodoMVC**](https://redux.js.org/introduction/examples#todomvc): [Source](https://github.com/reduxjs/redux/tree/master/examples/todomvc) | [Sandbox](https://codesandbox.io/s/github/reduxjs/redux/tree/master/examples/todomvc)
- [**Shopping Cart**](https://redux.js.org/introduction/examples#shopping-cart): [Source](https://github.com/reduxjs/redux/tree/master/examples/shopping-cart) | [Sandbox](https://codesandbox.io/s/github/reduxjs/redux/tree/master/examples/shopping-cart)
- [**Tree View**](https://redux.js.org/introduction/examples#tree-view): [Source](https://github.com/reduxjs/redux/tree/master/examples/tree-view) | [Sandbox](https://codesandbox.io/s/github/reduxjs/redux/tree/master/examples/tree-view)
- [**Async**](https://redux.js.org/introduction/examples#async): [Source](https://github.com/reduxjs/redux/tree/master/examples/async) | [Sandbox](https://codesandbox.io/s/github/reduxjs/redux/tree/master/examples/async)
- [**Universal**](https://redux.js.org/introduction/examples#universal): [Source](https://github.com/reduxjs/redux/tree/master/examples/universal)
- [**Real World**](https://redux.js.org/introduction/examples#real-world): [Source](https://github.com/reduxjs/redux/tree/master/examples/real-world) | [Sandbox](https://codesandbox.io/s/github/reduxjs/redux/tree/master/examples/real-world)

Se você é novo no ecossistema NPM e tem problemas para fazer um projeto funcionar, ou não sabe onde colá-lo, confira [simplest-redux-example] (https://github.com/jackielii / simplest-redux-example) que usa o Redux junto com o React e o Browserify.

## Depoimentos

> [“Love what you're doing with Redux”](https://twitter.com/jingc/status/616608251463909376)  
> Jing Chen, creator of Flux

> [“I asked for comments on Redux in FB's internal JS discussion group, and it was universally praised. Really awesome work.”](https://twitter.com/fisherwebdev/status/616286955693682688)  
> Bill Fisher, author of Flux documentation

> [“It's cool that you are inventing a better Flux by not doing Flux at all.”](https://twitter.com/andrestaltz/status/616271392930201604)  
> André Staltz, creator of Cycle

## Obrigado

- [The Elm Architecture](https://github.com/evancz/elm-architecture-tutorial) for a great intro to modeling state updates with reducers;
- [Turning the database inside-out](https://www.confluent.io/blog/turning-the-database-inside-out-with-apache-samza/) for blowing my mind;
- [Developing ClojureScript with Figwheel](https://www.youtube.com/watch?v=j-kj2qwJa_E) for convincing me that re-evaluation should “just work”;
- [Webpack](https://webpack.js.org/concepts/hot-module-replacement/) for Hot Module Replacement;
- [Flummox](https://github.com/acdlite/flummox) for teaching me to approach Flux without boilerplate or singletons;
- [disto](https://github.com/threepointone/disto) for a proof of concept of hot reloadable Stores;
- [NuclearJS](https://github.com/optimizely/nuclear-js) for proving this architecture can be performant;
- [Om](https://github.com/omcljs/om) for popularizing the idea of a single state atom;
- [Cycle](https://github.com/cyclejs/cycle-core) for showing how often a function is the best tool;
- [React](https://github.com/facebook/react) for the pragmatic innovation.

Special thanks to [Jamie Paton](http://jdpaton.github.io) for handing over the `redux` NPM package name.

## Logo

Você pode encontrar o logotipo oficial [no GitHub](https://github.com/reduxjs/redux/tree/master/logo).

## Change Log

Este projeto adere à [Semantic Versioning](http://semver.org/).

Cada versão, juntamente com as instruções de migração, está documentada na página do GitHub [Releases](https://github.com/reduxjs/redux/releases).

## Patrons

O trabalho no Redux foi [financiado pela comunidade](https://www.patreon.com/reactdx).
Conheça algumas das empresas de destaque que tornaram isso possível:

- [Webflow](https://github.com/webflow)
- [Ximedes](https://www.ximedes.com/)

[See the full list of Redux patrons](PATRONS.md), as well as the always-growing list of [people and companies that use Redux](https://github.com/reduxjs/redux/issues/310).

## License

MIT
