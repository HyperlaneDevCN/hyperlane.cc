# Hyperlane 文档

本网站使用 [Docusaurus 3](https://docusaurus.io/) 构建，这是一个现代化的静态网站生成器。

## 生成的内容

`static` 目录包含生成的内容。

大部分内容只是从 `@hyperlane-xyz` NPM 包序列化的内容的中文化（参见 `devDependencies`）。最终这应该成为构建过程的一部分。

### 安装

```
pnpm install
```

### 本地开发

```
pnpm start
```

此命令启动本地开发服务器并打开浏览器窗口。大多数更改无需重启服务器即可实时显示。

### 构建

```
pnpm build
```

此命令将静态内容生成到 `build` 目录中，可以使用任何内容托管服务进行部署。

**重要提示：** 在推送更改之前，请确保构建成功完成。构建失败会中断部署过程。使用 `pnpm build` 在本地验证一切按预期工作。

### 部署

使用 GitHub Pages 部署网站。该操作在每次推送到 `main` 分支时触发。

## 贡献指南

感谢您有兴趣为改进文档做出贡献！

您可以做出两种类型的贡献：

- 修复错误或为当前文档内容添加新页面。
- 修复文档网站的错误或引入新功能（在 Docusaurus 代码库中）。

### 内容贡献

文档内容以 MDX 格式编写，位于 `docs` 文件夹中。

- MDX 文件：将 Markdown 与 React 结合。在 [Docusaurus 文档](https://docusaurus.io/docs/markdown-features/react) 中了解更多信息。
- Markdown 基础：如果您不熟悉 Markdown，请参考此 [指南](https://guides.github.com/features/mastering-markdown/) 或此 [速查表](https://www.markdownguide.org/cheat-sheet/) 开始使用。

#### 现有内容

如果您发现现有文档中有任何令人困惑或可以改进的地方，可以点击页面底部的**"编辑此页面"**，这将重定向到该文档的 GitHub 编辑表单。提交包含您更改的拉取请求（PR）。

#### 新内容

添加新页面时：

1. Fork 仓库。
2. 创建新分支并在您的仓库中进行更改。
3. 向 Hyperlane 中文社区文档仓库提交拉取请求（PR）。
   - 确保您的 PR 包含清晰的标题和对更改的描述。

### 配置

- `docusaurus.config.js` - 此文件包含 Docusaurus 配置。在这里，您可以管理站点元数据、页眉和页脚中的链接以及主题配置。您可以访问 [Docusaurus 文档](https://docusaurus.io/docs/configuration) 了解更多关于 Docusaurus 设置的信息。
- `sidebars.js` - 这指定了文档的侧边栏。如果您添加新页面，请确保将其包含在侧边栏中。

  有关此文件的完整文档，请访问 [Docusaurus 网站](https://docusaurus.io/docs/sidebar)。

如果本 `README.md` 中有任何遗漏或说明不清楚的地方，请记住您也可以贡献改进它。**Fork、修改并向我们的仓库提交 PR！**

欢迎所有贡献！
