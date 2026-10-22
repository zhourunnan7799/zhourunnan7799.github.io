# 周润楠 个人主页（Runnan Zhou's Homepage）

仿照导师 [Xinjie Yao](https://yxjdarren.github.io/) 的学术主页做的同款站点 ——
两边用的是同一套主题 [Minimal Light](https://github.com/yaoyao-liu/minimal-light)（CC0 公共领域，可自由使用）。
本站是**纯静态 HTML**，不需要 Jekyll、不需要装任何环境，上传到 GitHub 就能用。

- 页面地址（建好仓库后）：`https://zhourunnan7799.github.io/`
- 本地预览：双击 `index.html`，用浏览器打开就是最终效果。

---

## 一、文件结构

```
zhourunnan7799.github.io/
├── index.html                      ← 唯一需要经常改的文件（所有文字内容都在这）
├── .nojekyll                       ← 告诉 GitHub Pages 不要用 Jekyll 处理，别删
├── README.md                       ← 本说明
├── assets/
│   ├── css/
│   │   ├── style.css               ← 主题主样式（一般不动）
│   │   ├── publications.css        ← 论文列表样式（一般不动）
│   │   ├── font.css                ← 正文字体：衬线版（当前使用）
│   │   ├── font_sans_serif.css     ← 正文字体：无衬线版（备选）
│   │   └── custom.css              ← 我加的样式：头像、图标、目录、占位文字，改这里
│   └── img/
│       ├── avatar.png              ← 头像（占位图，记得换成自己的照片）
│       ├── favicon.png             ← 标签页小图标（浅色模式）
│       └── favicon-dark.png        ← 标签页小图标（深色模式）
└── _preview/                       ← 我截图核对版式用的，可以整个删掉
```

---

## 二、部署到 GitHub（5 分钟）

1. 打开 <https://github.com/new>，**Repository name** 填 `zhourunnan7799.github.io`（必须和用户名完全一致，一个字母都不能差）。
2. 选 **Public**，不要勾 "Add a README file"，点 **Create repository**。
3. 在新建的空仓库页面点 **uploading an existing file**（或 `Add file → Upload files`）。
4. 把本文件夹里的**所有内容**（`index.html`、`assets/` 文件夹、`.nojekyll`）一起拖进去，点 **Commit changes**。
   - 注意：要拖 `index.html` 本身，不要拖外层文件夹，否则网址会变成 `.../zhourunnan7799.github.io/` 再加一层目录。
   - `.nojekyll` 是隐藏文件，网页上传框里可能看不到；如果拖不上去，就在仓库里手动新建文件，文件名填 `.nojekyll`，内容留空即可。
5. 进仓库 **Settings → Pages**，`Source` 选 **Deploy from a branch**，`Branch` 选 **main** + **/(root)**，点 **Save**。
6. 等 1–2 分钟，访问 <https://zhourunnan7799.github.io/>。第一次可能显示 404，多刷几次或等 5 分钟。

> 以后改完内容，重新上传 `index.html` 覆盖，等 1 分钟刷新页面即可。

---

## 三、日常怎么改（都在 index.html 里）

文件里每一段都有中文注释，搜索关键词就能定位：

| 想改什么 | 搜索这个 |
| --- | --- |
| 姓名（大字） | `<h1>` |
| 身份（如 M.S. Student） | `<position>` |
| 学校 / 学院 | `class="affil"` |
| 邮箱（显示和链接两处都要改） | `2513556598` |
| 社交图标 | `class="social-icons"` |
| 左侧目录 | `class="nav"` |
| 自我介绍 | `id="about-me"` |
| 研究方向 | `id="research-interests"` |
| 教育经历 | `id="education"` |
| 动态 / 论文录用消息 | `id="news"` |
| 论文列表 | `id="publications"`（里面有一条注释掉的模板） |
| 项目 | `id="projects"`（同样有注释模板） |
| 技能 | `id="skills"` |
| 页脚更新时间 | `Last updated` |

### 换头像

把新的正方形照片命名为 `avatar.png`，覆盖 `assets/img/avatar.png`。
建议 800×800 以上，正方形（不是正方形会被裁成圆形，人像居中即可）。

### 加论文

`index.html` 的 `id="publications"` 段里有一段被 `<!-- -->` 注释掉的模板：

1. 把 `<!--` 和 `-->` 删掉（保留里面的 `<li>...</li>`）；
2. 改题目、作者、期刊会议、链接；
3. 缩略图（论文里的 teaser 图）存成 `assets/img/xxx.png`，建议横向 540×246 左右；
4. 有了论文之后，把上面那行 `Coming soon.` 删掉。

`hust` 那行 `<abbr class="badge">CVPR</abbr>` 就是缩略图左上角的会议标签。

### 加动态 / 项目

`id="news"` 和 `id="projects"` 里都有注释掉的示例，照抄一行改内容即可，最新的放最上面。

---

## 四、还需要你补充的内容

现在页面上这几处是占位或偏简，等有内容了告诉我，我帮你写得更充实：

- [ ] **2020–2026 之间的经历**：现在按你的选择只写了本科毕业年份（2020），没展开这段。
- [ ] **项目 / 科研经历**：`Projects` 现在是 `Coming soon.`，有实践项目、课程项目、实习都可以放 1–2 条。
- [ ] **技能**：现在只有 `Python, C++`，可以加 PyTorch、Linux、Git、LaTeX、MATLAB 等。
- [ ] **Google Scholar 主页**：建好后把 `index.html` 里 scholar 图标的注释打开（现在有邮箱和 GitHub 两个图标）。
- [ ] **论文**：暂无，有录用后立刻可以加。
- [ ] **CV / 简历 PDF**：如果有，放到 `assets/files/curriculum_vitae.pdf`，我再帮你加一个 CV 图标。

---

## 五、小技巧

- **字体**：现在是衬线（Georgia / 宋体系，和导师页面一致的学术风）。想换成无衬线，把 `index.html` 里
  `<link rel="stylesheet" href="./assets/css/font.css">` 改成 `font_sans_serif.css` 即可。
- **深色模式**：系统开了深色模式时页面会自动变深蓝底，不用管。
- **图标**：用的是内联 SVG，不依赖任何 CDN，国内加载也正常；不需要联网也能显示。
- **改坏了的急救**：`index.html` 里删掉一个 `<div>` 或 `</div>` 会让版面错乱，改前先在 GitHub 网页上留个旧版本，或者本地备份一份。
- **`_preview/` 文件夹**：我用来截图核对的，不影响网站，可以删。

---

主题：Minimal Light by [Yaoyao Liu](https://github.com/yaoyao-liu/minimal-light)，CC0-1.0（公共领域），无需署名，此处保留只为说明出处。
