1 初始化 package.json

```
npm init
```

2 安装插件

```
npm install 
  webpack webpack-dev-server 
  vue-loader vue-html-loader css-loader vue-style-loader vue-hot-reload-api 
  babel-loader babel-core babel-plugin-transform-runtime babel-preset-es2015 
  babel-runtime@5 
  --save-dev
npm install vue --save
```

3 配置文件

```
// webpack.config.js
module.exports = {
  // entry point of our application
  entry: './main.js',
  // where to place the compiled bundle
  output: {
    path: __dirname,
    filename: 'build.js'
  },
  module: {
    // `loaders` is an array of loaders to use.
    // here we are only configuring vue-loader
    loaders: [
      {
        test: /\.vue$/, // a regex for matching all files that end in `.vue`
        loader: 'vue'   // loader to use for matched files
      }
    ]
  }
}
```

4 创建文件 

+ main.js

```
// main.js
var Vue = require('vue')
// require a *.vue component
var App = require('./components/App.vue')

// mount a root Vue instance
new Vue({
  el: 'body',
  components: {
    // include the required component
    // in the options
    app: App
  }
})
```

+ component/App.vue

```
<template>
  <div class="app">
    <component-a></component-a>
    <component-b></component-b>
  </div>
</template>

<script>
import ComponentA from './ComponentA.vue'
import ComponentB from './ComponentB.vue'

export default {
  components: {
    ComponentA,
    ComponentB
  }
}
</script>
```

+ index.html

```
<!-- index.html -->
<body>
  <app></app>
  <script src="build.js"></script>
</body>
```

5 启动

```
"scripts": {
  "dev": "webpack-dev-server --inline --hot",
  "build": "webpack -p"
}
```