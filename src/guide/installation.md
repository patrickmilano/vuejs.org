---
title: Instalação
type: guide
order: 0
vue_version: 1.0.24
dev_size: "264.56"
min_size: "74.51"
gz_size: "25.79"
---

### Notas de Compatibilidade

Vue.js **não** suporta o IE8 e versões anteriores, pois o Vue.js trabalha com características do ECMAScript 5, que não são suportadas no IE8. Entretanto o Vue.js suporta todos os [navegadores compatíveis com ECMAScript](http://caniuse.com/#feat=es5).

### Notas de Lançamento

Notas de lançamento mais detalhadas para cada versão estão disponíveis em [GitHub](https://github.com/vuejs/vue/releases).

## Standalone

Simplesmente faça o download e inclua uma tag script. `Vue` será registrado como uma variável global. **Dica importante: não use a versão reduzida durante o desenvolvimento. Você perderá todos os avisos de erros comuns.**

<div id="downloads">
<a class="button" href="/js/vue.js" download>Versão de Desenvolvimento</a><span class="light info">Com alertas e modo debug</span>

<a class="button" href="/js/vue.min.js" download>Versão de Produção</a><span class="light info">Arquivo despojado, {{gz_size}}kb min+gzip</span>
</div>

### CDN

Disponível em [jsdelivr](//cdn.jsdelivr.net/vue/{{vue_version}}/vue.min.js) ou [cdnjs](//cdnjs.cloudflare.com/ajax/libs/vue/{{vue_version}}/vue.min.js) (tire algum tempo para sincronizar, pois a última versão poderá não estar disponível no momento).

Também disponível em [npmcdn](https://npmcdn.com/vue/dist/vue.min.js), que será convertida para a última versão assim que ela for publicada no npm. Você também pode pesquisar o fonte do pacote no npm em [npmcdn.com/vue/](https://npmcdn.com/vue/).

### CSP - compilação compatível

Alguns ambientes, tal como o Google Chrome Apps, forçam uma Política de Segurança de Conteúdo (CSP) e não permitem o uso do `new Function()` para expressões calculáveis. Em casos como esse, você pode usar o [CSP - compilação compatível](https://github.com/vuejs/vue/tree/csp/dist) como alternativa.

## NPM

NPM é o método recomendado de instalção quando se trata de um desenvolvimento em grande escala com aplicações Vue.js. Eles funcionam muito bem com o módulo CommonJS, tal como [Webpack](http://webpack.github.io/) ou [Browserify](http://browserify.org/). O Vue.js também fornece ferramentas de acompanhamento para autoria de [Componentes em um único arquivo](application.html#componentes-em-um-unico-arquivo).

``` bash
# versão estável mais recente
$ npm install vue
# versão estável mais recente + CSP-compliant
$ npm install vue@csp
```

## CLI

Vue.js provides an official CLI for quickly scaffolding ambitious Single Page Applications. It provides battery-included build setups for a modern frontend workflow. It takes only a few minutes to get up and running with hot-reload, lint-on-save and production-ready builds:
O Vue.js fornece uma [CLI oficial](https://github.com/vuejs/vue-cli) para um rápido __scaffolding__ de uma Aplicação de Página Única. Isso proporciona uma configuração carregada com modernos fluxos de trabalho __frontend__. Leva alguns minutos para "subir" e funciona com arquiteturas __hot-reload__, __lint-on-save__ e __production-ready__.

``` bash
# instalar vue-cli
$ npm install -g vue-cli
# criar um novo projeto usando o clichê "pacote web" 
$ vue init webpack my-project
# instalar as dependências e mandar ver!
$ cd my-project
$ npm install
$ npm run dev
```

## Dev Build

**Importante**: o pacote CommonJS distribuído no NPM (`vue.common.js`) é ativado apenas durante __releases__ na __branch__ `master`, então o arquivo na __branch__ `dev` é o mesmo da última __release__ estável. Para usar a última versão do código fonte no GitHub, você mesmo deverá fazer o __build__!

``` bash
git clone https://github.com/vuejs/vue.git node_modules/vue
cd node_modules/vue
npm install
npm run build
```

## Bower

``` bash
# última versão estável
$ bower install vue
```

## AMD Module Loaders

The standalone downloads or versions installed via Bower are wrapped with UMD so they can be used directly as an AMD module.
Os downloads isolados ou versões instaladas via __Bower__ são envolvidas com UMD, então eles podem ser usados diretamente como um módulo AMD.
