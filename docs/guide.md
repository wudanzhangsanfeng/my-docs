# 使用指南

## 更新文档的流程

1. 修改 `docs/` 目录中的 Markdown 文件。
2. 在本地预览并检查页面及链接。
3. 提交修改并推送到 `main` 分支。
4. 在 Actions 页面查看构建与部署状态。
5. 打开网站检查内容是否更新。

## 常用命令

在项目根目录执行（本机使用 `py` 启动 Python）：

```bash
# 创建并激活虚拟环境（Windows PowerShell）
py -3 -m venv .venv
.\.venv\Scripts\Activate.ps1

# 安装依赖
py -m pip install -r requirements.txt

# 本地预览，默认 http://127.0.0.1:8000/
py -m mkdocs serve

# 构建并严格检查警告（与 CI 行为一致）
py -m mkdocs build --strict
```

## 目录约定

| 路径 | 说明 |
| --- | --- |
| `docs/` | 网站源文件，只放 Markdown 和图片 |
| `site/` | 构建产物，自动生成，已被 `.gitignore` 忽略 |
| `.github/workflows/deploy.yml` | 自动部署流水线 |
| `report/` | 本次作业的过程报告与截图 |

> 注意：`site/` 是生成目录，不要手动修改，也不要提交到仓库。

## 检查清单

- [ ] 四个页面都能正常打开
- [ ] 导航栏标题与顺序正确
- [ ] 表格、代码块显示正常
- [ ] 页面之间的链接可以点击跳转

可以回到 [首页](index.md) 或查看 [API 参考](api.md)。
