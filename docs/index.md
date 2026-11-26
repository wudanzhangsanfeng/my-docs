# 我的技术文档

欢迎访问我的个人文档网站。本网站使用 **MkDocs + Material** 构建，通过 **GitHub Actions** 自动部署到 **GitHub Pages**。

> 自动部署验证：这是我第二次推送后更新的内容。

- 作者：wudanzhangsanfeng
- 实践主题：静态文档自动部署

## 快速导航

- [关于本项目](about.md)
- [使用指南](guide.md)
- [API 参考](api.md)

## 这个网站讲什么

这是一个用于演示「从 Markdown 到公开网站」自动化发布流程的小型文档站。全部内容由四个 Markdown 页面组成：修改任意页面并推送到 `main` 分支后，GitHub Actions 会自动重新构建并部署，整个过程无需手动上传任何文件。

## 站点信息一览

| 项目 | 内容 |
| --- | --- |
| 构建工具 | MkDocs + Material 主题 |
| 部署方式 | GitHub Actions 自动部署 |
| 托管平台 | GitHub Pages |
| 源码仓库 | [wudanzhangsanfeng/my-docs](https://github.com/wudanzhangsanfeng/my-docs) |

## 本地预览命令

```bash
py -m mkdocs serve
```

执行后打开终端提示的地址（通常为 `http://127.0.0.1:8000/`）即可在本地查看网站。

## 我为什么做这个练习

在学习这门课程之前，我一直以为「发布网站」必须购买服务器、配置域名并手动上传文件。这次实践让我第一次完整走通了 **写文档 → 构建 → 自动部署 → 网页更新** 的链路，也真正理解了版本控制与持续交付是怎样配合工作的。
