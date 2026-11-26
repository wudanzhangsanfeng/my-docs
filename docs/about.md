# 关于本项目

## 项目目标

实现从 Markdown 文档到公开网站的自动化发布：我只需要专心写内容，构建与上线全部交给流水线完成。

## 技术组成

| 工具 | 作用 |
| --- | --- |
| Markdown | 编写文档内容 |
| MkDocs Material | 将文档构建成静态网站 |
| GitHub Actions | 自动执行安装、构建和部署 |
| GitHub Pages | 托管并提供网站访问地址 |

## 工作原理

1. 我在本地编写 `docs/` 目录下的 Markdown 文件。
2. 推送到 `main` 分支后，GitHub Actions 读取工作流 `.github/workflows/deploy.yml`。
3. 流水线安装 Python 依赖并运行 `mkdocs build`，把静态站点生成到 `site/` 目录。
4. 官方 Pages Actions 把 `site/` 作为构建产物上传并发布。
5. 浏览器访问 `https://wudanzhangsanfeng.github.io/my-docs/` 即可看到最新内容。

## 数据流示意

```
docs/*.md  --(mkdocs build)-->  site/  --(GitHub Actions 上传)-->  GitHub Pages
```

## 一点体会

最大的感受是「关注点分离」：写文档和上线部署本来是两件完全不同的事，却能被一条 `git push` 串起来。这比过去手动打包、上传服务器的方式省心得多，而且每次发布都有记录、可以随时回滚。

想了解如何修改内容，请继续阅读 [使用指南](guide.md)。
