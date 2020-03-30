# Vue 3 Deep Dive

RFCs Repo for breaking changes and new features (vue/rfc)

Vue.createApp
keeps vue stateless

```js
const app = Vue.createApp();
app.use();
app.mount("#app");
```

Render Functions

- `import { h } from vue`
- better for reusable components
- ability to wrap slots with html
- removes template code an uses JS - Similar to JSX
- lots of logic little markup
- React is all Render Fucntions and gives poor perfomance over vue

Template Compiler

- Better Optimazation
- Used with lots of Markup and little logic
- Content Heavy - better perfomance (React Lacks this)

Reactivity

- Proxies allow for reactivity of new object properties

Composition API

- Replaces Mixins
- Need to create a reactive refernce (ref)
- WatchEffect - watcher that runs onMounted and on changes to the data
  - Send a ref or a function into the API for watchEffect to work
- Replaces scoped slots
- Ability to pass desctructed values from one composition function into another

Fragments

- Multiple root nodes

Portals

- Use with modal and overlays

Suspense

- Async components to display all components are ready for render
- Add async to setup() to make a component Asyncronous

V-Model

- multiple v-model with different prop names on a component
- v-model modifiers - modify the data before syncing back up
- replace v-bind.sync - fundamentaly the same

Custom Render API

- Ability to render vue with webGL, nativescript and ....

Custom Compiler API

- Custom Transform - ability to transform elements at compile time
- Ability to solve issues at compile level with type support

Contributions

- Test Coverage
- Read .gitlab --> contributions.md
- Watch the RFC repo and provide feedback
- Provide help with community questions
