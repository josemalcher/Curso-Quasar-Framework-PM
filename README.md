# Curso Quasar Framework PM

https://www.youtube.com/c/PatrickMonteiroEng/videos

## <a name="indice">Índice</a>

1. [Tópicos Iniciais](#parte1)
---

## <a name="parte1">1 - Tópicos Iniciais </a>

- Aula 01 - Preparando Ambiente para o Quasar

- [https://quasar.dev/quasar-cli/installation](https://quasar.dev/quasar-cli/installation)

```
yarn global add @quasar/cli


$ quasar -v
1.2.1

$ vue -V
@vue/cli 4.5.13

```

```
$ quasar dev

 Dev mode.......... spa
 Pkg quasar........ v2.0.4
 Pkg @quasar/app... v3.1.0
 Pkg webpack....... v5
 Debugging......... enabled

```


- Aula 02 - Conhecendo o quasar-cli

```
$ quasar info

Operating System - Windows_NT(10.0.22000) - win32/x64
NodeJs - 14.16.1

Global packages
  NPM - 6.14.12
  yarn - 1.22.10
  @quasar/cli - 1.2.1
  @quasar/icongenie - Not installed
  cordova - Not installed

Important local packages
  quasar - 2.0.4 -- Build high-performance VueJS user interfaces (SPA, PWA, SSR, Mobile and Desktop) in record time
  @quasar/app - 3.1.0 -- Quasar Framework local CLI
  @quasar/extras - 1.10.12 -- Quasar Framework fonts, icons and animations
  eslint-plugin-quasar - Not installed
  vue - 3.2.4 -- The progressive JavaScript framework for buiding modern web UI.
  vue-router - 4.0.11
  vuex - 4.0.2 -- state management for Vue.js
  electron - Not installed
  electron-packager - Not installed
  electron-builder - Not installed
  @babel/core - 7.15.5 -- Babel compiler core.
  webpack - 5.52.1 -- Packs CommonJs/AMD modules for the browser. Allows to split your codebase into multiple bundles, which can be loaded on demand. Support loaders to
 preprocess files, i.e. json, jsx, es7, css, less, ... and your custom stuff.
  webpack-dev-server - 4.0.0 -- Serves a webpack app. Updates the browser on changes.
  workbox-webpack-plugin - Not installed
  register-service-worker - 1.7.2 -- Script for registering service worker, with hooks
  typescript - 4.2.2 -- TypeScript is a language for application scale JavaScript development
  @capacitor/core - Not installed
  @capacitor/cli - Not installed
  @capacitor/android - Not installed
  @capacitor/ios - Not installed

Quasar App Extensions
  *None installed*

Networking
  Host - DESKTOP-J4KCU1C
  vEthernet (WSL) - 172.17.64.1
  Wi-Fi - 192.168.0.183

```

```
$ quasar dev -m electron

 Dev mode.......... electron
 Pkg quasar........ v2.0.4
 Pkg @quasar/app... v3.1.0
 Pkg webpack....... v5
 Debugging......... enabled

```

- Aula 03 - Estrutura de um projeto Quasar

- [blog01/quasar.conf.js](blog01/quasar.conf.js)


- Aula 04 - Espaçamento CSS

- [https://quasar.dev/style/spacing#introduction](https://quasar.dev/style/spacing#introduction)

- [blog01/src/pages/Index.vue](blog01/src/pages/Index.vue)

```vue
<template>
  <q-page>
<!--    <img
      alt="Quasar logo"
      src="~assets/quasar-logo-vertical.svg"
      style="width: 200px; height: 200px"
    >-->
    <div class="q-pa-sm border-black">q-pa-sm</div>
    <div class="q-ml-xl q-mr-xl q-mt-xl border-black">q-ml-xl</div>
    <div class="q-ml-sm q-mr-sm q-mt-sm border-black">q-ml-sm</div>
  </q-page>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'PageIndex'
})
</script>

<style scoped>
.border-black {
  border: 1px solid black;
}
</style>

```

- Aula 05 - Flex CSS

- [https://quasar.dev/layout/grid/introduction-to-flexbox](https://quasar.dev/layout/grid/introduction-to-flexbox)

```vue
<template>
  <q-page class="container">
    <div class="row justify-center q-gutter-lg">
      <div class="col-lg-3">
        <q-btn color="dark" class="full-width">Button</q-btn>
      </div>
      <div class="col-lg-5">
        <q-btn color="dark" class="full-width">Button</q-btn>
      </div>
      <div class="col-lg-1">
        <q-btn color="dark" class="full-width">Button</q-btn>
      </div>
    </div>
  </q-page>
</template>
```


- Aula 06 - Shadows e Visibility

- [https://quasar.dev/style/shadows](https://quasar.dev/style/shadows)

- [https://quasar.dev/style/visibility](https://quasar.dev/style/visibility)

- Aula 07 - Criando páginas e rotas

- [https://quasar.dev/vue-components/list-and-list-items](https://quasar.dev/vue-components/list-and-list-items)

- Aula 07.1 - Criando páginas com o Quasar-Cli

```
$ quasar new page NopaPagina
 App • Generated page: src\pages\NopaPagina.vue
 App • Make sure to reference it in src/router/routes.js

```

- [blog01/src/pages/NopaPagina.vue](blog01/src/pages/NopaPagina.vue)

```vue
<template>
  <q-page padding>
    <!-- content -->
  </q-page>
</template>

<script>
export default {
  // name: 'PageName',
}
</script>

```

- Aula 08 - Usando componente QCard

- Aula 09 - Consumindo API com plugin Axios

- Aula 10 - Utilizando Vuex

- Aula 10.1 - Vuex e Vue Router

- Aula 011 - Build SPA e deploy com surge

- Construindo uma aplicação multiplataforma com Quasar Framework.

[Voltar ao Índice](#indice)

---

