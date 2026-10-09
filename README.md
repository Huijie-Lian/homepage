# Huijie Lian — Academic CV

当前网站使用官方 [HugoBlox Academic CV](https://github.com/HugoBlox/hugo-theme-academic-cv) 模板。网站源码位于 `academic-site/`，项目根目录的旧 PaperMod 文件保留用于回溯。

## 更新资料

- `academic-site/data/authors/me-zh.json`：中文姓名、身份、教育经历及链接。
- `academic-site/data/authors/me-en.json`：英文个人资料。
- `academic-site/content/zh/`、`academic-site/content/en/`：双语首页、关于我及论文。
- `academic-site/assets/media/authors/`：个人照片。
- `academic-site/assets/css/custom.css`：照片比例和少量样式定制。

## 构建

需要 Hugo Extended 0.166.0、Node.js 22 和 Go。依赖版本由 `package-lock.json` 和 `go.sum` 固定。

```powershell
cd academic-site
npm ci
hugo --destination ../.academic-public
cd ..
./scripts/export-academic-preview.ps1
```

离线预览入口为 `web-preview/zh/index.html` 和 `web-preview/en/index.html`。本地服务器可以使用 `hugo server --source academic-site`。

Netlify 和 GitHub Pages 的构建配置均指向新模板目录。推送到 main 分支后，GitHub Actions 会自动构建并部署 GitHub Pages。

## 模板与资料

HugoBlox 模板的许可证保留在 `academic-site/LICENSE.md`，页面保留官方署名。
论文核对记录见 `PUBLICATIONS_REVIEW.md`。获奖信息、研究方向与兴趣照片已根据本人提供的资料加入；未确认的研究项目、导师和简历未加入新模板。
