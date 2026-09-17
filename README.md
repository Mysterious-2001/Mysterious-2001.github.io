# Mysterious-2001 的个人博客

一个以长期写作为核心的 Hexo 博客，发布地址为：

<https://mysterious-2001.github.io>

## 本地运行

```bash
npm install
npm run dev
```

浏览器打开 <http://localhost:4000>。

## 写一篇新文章

```bash
npm run new -- "文章标题"
```

然后编辑 `source/_posts/` 中生成的 Markdown 文件。完成后运行：

```bash
npm run build
```

生成的网站位于 `public/`，该目录不需要提交。

## 添加 Notion 外链

公开 Notion 页面后，编辑 `themes/ink/_config.yml`：

```yaml
notion_url: "https://your-name.notion.site/your-page"
```

填写后，网站顶部会自动出现 `Notion ↗` 导航。

## 发布到 GitHub Pages

1. 在 GitHub 新建公开仓库 `Mysterious-2001.github.io`。
2. 将本项目推送到仓库的 `main` 分支。
3. 进入仓库的 **Settings → Pages**，将 **Source** 设为 **GitHub Actions**。
4. 等待 Actions 完成，访问 <https://mysterious-2001.github.io>。

以后每次推送到 `main`，博客都会自动重新发布。
