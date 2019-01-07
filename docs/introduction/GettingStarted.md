# Começando com o Redux

Redux é um container de estado previsível para apps em JavaScript.

Ele ajuda que você escreva aplicações que se comportem de forma consistente, que funcionem em diferentes ambientes (cliente, servidor, e nativo), e que sejam fáceis de testar. Além disso, ele fornece uma grande experiência de desenvolvedor, tais como [edição de código em tempo real combinado com um 'time traveling debugger'](https://github.com/reduxjs/redux-devtools).

Você pode usar o Redux em conjunto com o [React](https://reactjs.org), ou qualquer outra biblioteca de view. Ele é minúsculo (2kB, incluindo dependências), mas tem um grande ecossistema de addons disponíveis.

## Instalação

O Redux está disponível como um pacote NPM para uso com um module bundler ou em uma aplicação Node:

```bash
npm install --save redux
```

Ele também está disponível como um pacote UMD pré-compilado que define uma variábel global `window.Redux`. O pacote UMD pode ser usado com uma [tag `<script>`](https://unpkg.com/redux/dist/redux.js) diretamente.

Para maiores detalhes, veja a página de [Instalação](Installation.md).

## Pacote de Iniciante do Redux

Redux é pequeno e sem uma opinião definida. Nós também possuímos um pacote separado chamado de **[redux-starter-kit](https://redux-starter-kit.js.org/)**,
que incluem alguns padrões baseados em opinião que ajudarão você a usar o Redux de uma forma mais eficiente.

Isto ajuda a simplificar vários casos de uso comuns, incluindo [configuração da store](https://redux-starter-kit.js.org/api/configureStore),
[criação de reducers e escrita de lógica de atualização imutável](https://redux-starter-kit.js.org/api/createreducer),
e mesmo [criação de "fatias" inteiras de estado de uma vez](https://redux-starter-kit.js.org/api/createslice).

Independentemente se você é um novo usuário de Redux configurando seu primeiro projeto ou alguém já experiente desejando simplificar uma aplicação existente, o **[redux-starter-kit](https://redux-starter-kit.js.org/)** pode te ajudar a melhorar seu código do Redux.

## Exemplo básico

Todo o estado da sua aplicação está em uma árvore de objetos dentro de uma única _store_.  
A única forma de alterar a árvore de estado é emitir uma _action_, um objeto descrevendo o que ocorreu.  
Para especificar como as ações transformam a árvore de estado, você escreve os _reducers_.

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

## Exemplos

O repositório do Redux contém vários exemploes de projetos demonstrando vários aspectos de como usar o Redux. Quase todos os exemplos têm um sandbox do CodeSandbox. Isto é uma versão interativa do código que você pode "brincar" online.

- [**Counter Vanilla**](/introduction/examples#counter-vanilla): [Source](https://github.com/reduxjs/redux/tree/master/examples/counter-vanilla)
- [**Counter**](/introduction/examples#counter): [Source](https://github.com/reduxjs/redux/tree/master/examples/counter) | [Sandbox](https://codesandbox.io/s/github/reduxjs/redux/tree/master/examples/counter)
- [**Todos**](/introduction/examples#todos): [Source](https://github.com/reduxjs/redux/tree/master/examples/todos) | [Sandbox](https://codesandbox.io/s/github/reduxjs/redux/tree/master/examples/todos)
- [**Todos with Undo**](/introduction/examples#todos-with-undo): [Source](https://github.com/reduxjs/redux/tree/master/examples/todos-with-undo) | [Sandbox](https://codesandbox.io/s/github/reduxjs/redux/tree/master/examples/todos-with-undo)
- [**TodoMVC**](/introduction/examples#todomvc): [Source](https://github.com/reduxjs/redux/tree/master/examples/todomvc) | [Sandbox](https://codesandbox.io/s/github/reduxjs/redux/tree/master/examples/todomvc)
- [**Shopping Cart**](/introduction/examples#shopping-cart): [Source](https://github.com/reduxjs/redux/tree/master/examples/shopping-cart) | [Sandbox](https://codesandbox.io/s/github/reduxjs/redux/tree/master/examples/shopping-cart)
- [**Tree View**](/introduction/examples#tree-view): [Source](https://github.com/reduxjs/redux/tree/master/examples/tree-view) | [Sandbox](https://codesandbox.io/s/github/reduxjs/redux/tree/master/examples/tree-view)
- [**Async**](/introduction/examples#async): [Source](https://github.com/reduxjs/redux/tree/master/examples/async) | [Sandbox](https://codesandbox.io/s/github/reduxjs/redux/tree/master/examples/async)
- [**Universal**](/introduction/examples#universal): [Source](https://github.com/reduxjs/redux/tree/master/examples/universal)
- [**Real World**](/introduction/examples#real-world): [Source](https://github.com/reduxjs/redux/tree/master/examples/real-world) | [Sandbox](https://codesandbox.io/s/github/reduxjs/redux/tree/master/examples/real-world)

## Aprenda Redux

Nós temos uma variedade de recursos para ajudar você a aprender Redux, não importa qual seja o seu background ou estilo de aprendizagem.

### Apenas o Básico

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
  - O tutorial [DevGuides: Introduction to Redux](http://devguides.io/redux/) tutorial covers several aspects of Redux, including actions, reducers, usage with React, and middleware.

### Conceitos intermediários

Depois de ter aprendido as noções básicas de como trabalhar com actions, reducers e store, você pode ter perguntas sobre tópicos tais como trabalhar com lógica assíncrona e solicitações AJAX, conectar uma estrutura de interface do usuário como React ao seu armazenamento Redux e configurar um aplicativo para usar o Redux:

- A **["seção da documentação de conceitos Avançados](../advanced/README.md)** abrange detalhes sobre como trabalhar com lógica assíncrona, middleware e rotas.
- A página de documentação do Redux **["Recursos de Aprendizagem"](./LearningResources.md)** aponta para artigos recomendados sobre uma variedade de tópicos relacionados ao Redux.
- A série em 8 partes de Sophie DeBenedetto **Criando um aplicativo CRUD simples com React + Redux](http://www.thegreatcodeadventure.com/building-a-simple-crud-app-with-react-redux-part-1/)** mostra como montar um aplicativo CRUD básico a partir do zero.

### Real-World Usage

Going from a TodoMVC app to a real production application can be a big jump, but we've got plenty of resources to help:

- Redux creator Dan Abramov's **[free "Building React Applications with Idiomatic Redux" video series](https://egghead.io/courses/building-react-applications-with-idiomatic-redux)** builds on his first video series and covers topics like middleware, routing, and persistence.
- The **[Redux FAQ](../FAQ.md)** answers many common questions about how to use Redux, and the **["Recipes" docs section](../recipes/README.md)** has information on handling derived data, testing, structuring reducer logic, and reducing boilerplate.
- Redux co-maintainer Mark Erikson's **["Practical Redux" tutorial series](http://blog.isquaredsoftware.com/series/practical-redux/)** demonstrates real-world intermediate and advanced techniques for working with React and Redux (also available as **[an interactive course on Educative.io](https://www.educative.io/collection/5687753853370368/5707702298738688)**).
- The **[React/Redux links list](https://github.com/markerikson/react-redux-links)** has categorized articles on working with [reducers and selectors](https://github.com/markerikson/react-redux-links/blob/master/redux-reducers-selectors.md), [managing side effects](https://github.com/markerikson/react-redux-links/blob/master/redux-side-effects.md), [Redux architecture and best practices](https://github.com/markerikson/react-redux-links/blob/master/redux-architecture.md), and more.
- Our community has created thousands of Redux-related libraries, addons, and tools. The **["Ecosystem" docs page](./Ecosystem.md)** lists our recommendations, and there's a complete listing available in the **[Redux addons catalog](https://github.com/markerikson/redux-ecosystem-links)**.
- If you're looking to learn from actual application codebases, the addons catalog also has a list of **[purpose-built examples and real-world applications](https://github.com/markerikson/redux-ecosystem-links/blob/master/apps-and-examples.md)**.

## Ajuda e Discussão

O **[canal #redux](https://discord.gg/0ZcbPKXt5bZ6au5t)** da **[comunidade Reactiflux no Discord](http://www.reactiflux.com)** é nosso recurso oficial para todas as questões relacionadas com aprender e usar o Redux. Reactiflux é um ótimo lugar para sair, fazer perguntas e aprender - venha se juntar a nós!

You can also ask questions on [Stack Overflow](https://stackoverflow.com) using the **[#redux tag](https://stackoverflow.com/questions/tagged/redux)**.

## Você deve usar o Redux?

O Redux é uma ferramenta valiosa para organizar seu estado, mas você também deve considerar se é apropriado para sua situação. ** Não use o Redux só porque alguém disse que você deveria - tire um tempo para entender os potenciais benefícios e desvantagens de usá-lo **.

Aqui estão algumas sugestões sobre quando faz sentido usar o Redux:

- Você tem quantidades razoáveis ​​de dados mudando ao longo do tempo
- Você precisa de uma única fonte de verdade para o seu estado
- Você acha que manter todo o seu estado em um componente de nível superior não é mais suficiente

Sim, essas diretrizes são subjetivas e vagas, mas isso é por um bom motivo. O momento em que você deve integrar o Redux em seu aplicativo é diferente para cada usuário e diferente para cada aplicativo.

> **Para mais pensamentos sobre como o Redux deve ser usado, veja:**<br>
>
> - **[Redux FAQ: Quando eu devo usar o Redux?](../faq/General.md#when-should-i-use-redux)**
> - **[Talvez você não precise do Redux](https://medium.com/@dan_abramov/you-might-not-need-redux-be46360cf367)**<br>
> - **[O Tao do Redux, Parte 1 - Implementação e Intenção](http://blog.isquaredsoftware.com/2017/05/idiomatic-redux-tao-of-redux-part-1/)**<br>
> - **[The Tao of Redux, Parte 2 - Prática e Filosofia](http://blog.isquaredsoftware.com/2017/05/idiomatic-redux-tao-of-redux-part-2/)**
> - **[Redux FAQ](../FAQ.md)**
