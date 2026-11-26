# my-docs

我的技术文档网站，使用 [MkDocs](https://www.mkdocs.org/) + [Material 主题](https://squidfunk.github.io/mkdocs-material/) 编写，并通过 GitHub Actions 自动部署到 GitHub Pages。

- 网站链接：https://wudanzhangsanfeng.github.io/my-docs/
- 个人实验报告：[个人实验报告](report/README.md)
- 源码仓库：https://github.com/wudanzhangsanfeng/my-docs

## 项目结构

```
my-docs/
├── .github/workflows/deploy.yml   # 自动部署工作流
├── docs/                          # 网站源文件（四页文档）
├── report/                        # 作业过程报告与截图
├── mkdocs.yml                     # MkDocs 配置
├── requirements.txt               # Python 依赖
└── .gitignore
```

## 本地预览

```bash
# 创建并激活虚拟环境（Windows PowerShell）
py -3 -m venv .venv
.\.venv\Scripts\Activate.ps1

# 安装依赖
py -m pip install -r requirements.txt

# 本地预览，默认 http://127.0.0.1:8000/
py -m mkdocs serve

# 构建并严格检查警告
py -m mkdocs build --strict
```

## 自动部署

推送到 `main` 分支后，`.github/workflows/deploy.yml` 会自动安装依赖、构建站点并发布到 GitHub Pages。
