# Website 网站

This website is built using [Docusaurus 2](https://docusaurus.io/), a modern static website generator.

本网站使用[Docusaurus 2](https://docusaurus.io/)构建，这是一个现代静态网站生成器。


### Local Development 本地开发

```bash
$ npm start
$ yarn start
```

This command starts a local development server and opens up a browser window. Most changes are reflected live without having to restart the server.

此命令启动本地开发服务器并打开浏览器窗口。大多数更改都是实时反映的，无需重新启动服务器。

### Build 构建

```bash
$ npm build
```

This command generates static content into the `build` directory and can be served using any static contents hosting service.

此命令将静态内容生成到“build”目录中，并可以使用任何静态内容托管服务提供。

### Deployment 部署

Using SSH:

```
$ USE_SSH=true yarn deploy
```

Not using SSH:

```
$ GIT_USER=<Your GitHub username> yarn deploy
```

If you are using GitHub pages for hosting, this command is a convenient way to build the website and push to the `gh-pages` branch.

如果您正在使用GitHub页面进行托管，则此命令是构建网站并推送到“gh pages”分支的便捷方法。
