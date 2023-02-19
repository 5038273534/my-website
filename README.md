# Website 网站

This website is built using [Docusaurus 2](https://docusaurus.io/), a modern static website generator.

本网站使用[Docusaurus 2](https://docusaurus.io/)构建，这是一个现代静态网站生成器。


### Local Development

```bash
$ npm start
$ yarn start
```

This command starts a local development server and opens up a browser window. Most changes are reflected live without having to restart the server.

### Build

```bash
$ npm build
```

This command generates static content into the `build` directory and can be served using any static contents hosting service.

### Deployment

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
