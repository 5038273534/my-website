---
sidebar_position: 3
---

前提：
1. 安装nodejs 参照[]


### 常用命令
```bash
// 安装脚手架
npm install -g @vue/cli / cnpm install -g @vue/cli

// 更新脚手架
npm update -g @vue/cli / npm i -g @vue/cli

// 查询版本
vue --version / vue -V
@vue/cli 5.0.8

// 创建项目
vue create vue-project

// 启动项目
npm run serve
```


### 项目目录说明
```
```


### 配置
1. 项目运行自动打开浏览器。`package.json`，增加 **--open**
```json
  "scripts": {
    "serve": "vue-cli-service serve --open",
    "build": "vue-cli-service build",
    "lint": "vue-cli-service lint"
  },
```
2. 关闭eslint校验功能 (要是声明了变量没使用就会报错)。`vue.config.js`，增加 **lintOnSave: false**
```js
module.exports = defineConfig({
  transpileDependencies: true,
  lintOnSave: false
})
```



