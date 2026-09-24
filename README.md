# Hanxiao Wu — academic website prototype

独立的新网站项目：Quarto + custom CSS，五个英文页面，附带已生成的离线预览。
旧网站未修改，也没有发布或推送到任何远程仓库。

## 立即预览

打开 `_site/index.html` 即可浏览，页面导航、照片、PDF 都使用相对路径，无需联网。
当前会话另有本地预览：http://127.0.0.1:8765/ 。本地服务关闭后请打开 HTML，或重新启动预览。

## 修改与重新生成

安装 [Quarto](https://quarto.org/docs/download/)，然后在本目录执行：

```sh
quarto preview
```

生成可发布的文件：

```sh
quarto render
```

本项目已用 Quarto 1.9.38 实际渲染。系统字体无需下载，照片和 CV 均保存在项目内。

## 文件说明

- `index.qmd`：首页、研究概览、现场照片、精选论文。
- `research.qmd`：三个研究方向，顺序为 Antarctic / Continental / Computational。
- `publications.qmd`：已发表论文、在审稿件、会议报告。
- `fieldwork.qmd`：六张南极照片与 Kenya 经历。
- `cv.qmd`：网页版简历。
- `styles.css`：颜色、字体、布局和手机适配。
- `site-template.html`：所有页面共用导航和页脚。
- `assets/photos/`：经过网页尺寸优化的用户照片；没有生成或替代任何现场照片。
- `assets/documents/CV_Hanxiao.pdf`：用户上传的原始 PDF，内容未修改。
- `_site/`：已经渲染的完整网站，可直接浏览。

为了精确控制第一版版式，页面内容写在 `.qmd` 中的 HTML 区块里；修改正文时直接编辑标签之间的英文。公共导航只需改模板，颜色和间距只需改 CSS。Quarto 负责统一渲染与资源输出。

## 设计

- 冰雪白 `#ffffff`、深灰蓝 `#192c36`、冷蓝 `#204e64`、浅冰蓝 `#edf3f5`、帐篷红 `#a33730`。
- Georgia 衬线标题 + 系统无衬线正文。
- 宽幅摄影首页；研究页用分栏叙述；论文用清晰书目列表；照片页保留竖图。
- 手机布局采用单栏和始终可见的导航；包含键盘焦点、跳过导航链接、图片替代文本。

## 内容来源与编辑边界

身份、学历、研究经历、野外经历、在审稿件、报告、教学、奖项与技术背景来自本次提供的 `CV_Hanxiao.pdf`。
预计 Ph.D. 毕业年份为 2027，保留 expected 标记。Science 和 SRL 稿件按 CV 标为 under review，不呈现为已发表。

2024 论文 DOI 已核实：https://doi.org/10.1029/2023JB027952 。作者保留 CV 的缩写格式；未凭空补全在审稿件作者名单或添加未提供的论文 PDF。

照片对应：

| 文件 | 原始文件前缀 | 用途 |
|---|---|---|
| tent.jpg | 5872151A | 首页主图，红色物体是帐篷 |
| halo.jpg | 603E7356 | 光晕与帐篷，Fieldwork 开篇 |
| deployment.jpg | BEFFBCDF | Research 和 Fieldwork |
| team.jpg | 13A8B6C1 | South Pole Camp 合影 |
| fieldwork.jpg | 9757AB7A | 现场工作 |
| vault.jpg | 2F6BB644 | 雪坑 / broadband station 作业 |

未把具体照片绑定到未经确认的单一野外季节；未假定照片中的人物身份。光晕照片 480×360，团队合影 640×359，后续如有高清原图可替换同名文件。

参考网站：
- https://igppweb.ucsd.edu/~yanyang/ — 克制的信息层级和清晰的论文列表。
- https://me.seisman.info/ — 以研究主题组织内容。

未复制参考网站的文字、代码或照片。没有使用未提供的科研图或在审数据。

## 后续发布到 GitHub Pages

这是发布准备，不会自动改动旧网站。建议新建独立仓库，例如 `hanxiao-website-prototype`。

1. 将本目录源码提交到新的仓库；不要覆盖旧网站仓库。`_site/` 是构建结果，Git 忽略它。
2. 在仓库 Settings → Pages 中将 Source 选为 GitHub Actions。
3. 在 Actions 中手动运行 “Publish Quarto website”。工作流会重新渲染并部署 `_site/`。
4. 验证新版满意后，再决定正式网址与旧站迁移。

工作流只接受手动触发，初次提交不会自动发布。所有内部链接与资源路径均为相对路径，适用于 GitHub Pages 项目子路径。

发布方式参考：https://quarto.org/docs/publishing/github-pages.html 。

## 本轮内容修订

首页以 Seismologist 为主要身份，覆盖 continental 和 polar environments；将 composition、porosity、physical state 写成从地震观测进一步推断的研究问题，而非已实现的通用能力。Seismic–radar integration 明确为未来方向。新增用户提供的 2025 Brown University Geophysics Lunch Bunch 受邀报告；原始 CV PDF 未修改。
