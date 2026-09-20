# Ray思世界

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

然后编辑 `source/_posts/` 中生成的 Markdown 文件，并为文章选择分类。

每篇文章只使用一个一级分类：

```yaml
categories:
  - 生活思考
```

或：

```yaml
categories:
  - 专业知识
```

这两个分类会分别出现在 `/categories/life/` 和 `/categories/knowledge/` 页面。

完成后运行：

```bash
npm run build
```

生成的网站位于 `public/`，该目录不需要提交。

## 本机草稿

```bash
npm run new -- draft "文章标题"
npm run draft
```

草稿保存在 `source/_drafts/`，只通过本机的 <http://127.0.0.1:4000> 预览。该目录不会提交到 Git；常规 `npm run build` 也不会生成草稿页面。写完后运行 `npx hexo publish "文章标题"`，文章会移到 `source/_posts/`，之后便可按正常流程发布。

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
