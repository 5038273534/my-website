---
sidebar_position: 3
---

前提：
1. 安装nodejs：<https://nodejs.org/zh-cn>,学习nodejs`/docs/nodejs`
2. vue-cli官网：https://cli.vuejs.org/zh/guide


### 常用命令
```bash
// 安装脚手架
npm install -g @vue/cli / cnpm install -g @vue/cli

// 更新脚手架
npm update -g @vue/cli / npm i -g @vue/cli

// 查询版本
vue --version / vue -V
@vue/cli 5.0.8

// 脚手架创建项目
vue create vue-project

// 启动项目
npm run serve

// 项目要用到的依赖
cnpm install --save less less-loader@5
cnpm install --save vue-router


// ui界面创建项目
vue ui

```


### 项目目录说明
```
node_modules  ->项目依赖包
public
src
.gitignore
babel.config.js
jsconfig.json
package-lock.json
package.json
README.md
vue.config.js
```


### 配置
1. 项目运行自动打开浏览器。`package.json`，增加 **--open**
```json
  "scripts": {
    "serve": "vue-cli-service serve --open",
    "build": "vue-cli-service build",
    "lint": "vue-cli-service lint"
  },
  如果自动打开出现0.0.0.0:8080解决方法：
  vue.config.js文件里面添加：devServer
  const { defineConfig } = require("@vue/cli-service");
  module.exports = defineConfig({
    transpileDependencies: true,
    lintOnSave: false,
    devServer: {
      host: "localhost",
      port: 8080,
    },
});


```
2. 关闭eslint校验功能 (要是声明了变量没使用就会报错)。`vue.config.js`，增加 **lintOnSave: false**
```js
module.exports = defineConfig({
  transpileDependencies: true,
  lintOnSave: false
})
```



