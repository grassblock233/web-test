# web-test

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).

## 部署到 GitHub Pages

工作流位于 `.github/workflows/deploy.yml`，使用 Node.js 24 和 `npm ci` 安装依赖，
通过 lint 检查并构建后，将 `dist` 发布到 GitHub Pages。

1. 在 GitHub 仓库的 **Settings → Pages → Build and deployment → Source** 中选择 **GitHub Actions**。
2. 将代码推送到 `main` 分支即可自动部署，也可以在 **Actions → Deploy to GitHub Pages → Run workflow** 中手动触发。
3. 部署完成后，在工作流的 `github-pages` 环境中查看站点地址。

工作流使用仓库自带的 `GITHUB_TOKEN`，无需额外配置部署密钥。资源路径根据 Pages
配置自动设置，支持项目站点的仓库子路径、用户站点和自定义域名。本地开发默认使用 `/`。
如果修改默认分支名称，需要同步修改工作流的 `on.push.branches`。
