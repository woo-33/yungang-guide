# 云导览 · 看懂云冈石窟

面向普通游客的云冈石窟科普 H5(手机优先)。单文件网页,无需构建,无后端。

内容:45 窟总览(昙曜五窟与第 20 窟详细讲解)、佛像识别图鉴、佛的故事、名词虚线注释、简繁一键切换。

## 目录

```
index.html        # 全部页面与数据(数据在顶部 DATA 对象)
images/           # 洞窟照片,文件名 = 窟号(02.jpg、20.jpg…)
IMAGE_CREDITS.md  # 图片作者与授权(请补全)
.nojekyll
```

## 部署到 GitHub Pages

1. 新建仓库,上传本目录全部文件到仓库根目录。
2. Settings → Pages → Source 选 `Deploy from a branch`,分支选 `main`,目录选 `/ (root)`。
3. 几分钟后访问 `https://<用户名>.github.io/<仓库名>/`。

本地预览:用浏览器直接打开 `index.html` 即可。

## 如何修改

- **加图片**:把照片命名为窟号(如 `06.jpg`,建议宽度约 720px)放进 `images/`,并在 `index.html` 里的 `const IMGS={...}` 加一行 `6:"images/06.jpg"`。
- **改内容**:编辑 `DATA`(洞窟、佛像、故事)、`ALLN`(各窟简介)、`LK`(各窟看点)、`DATA.terms`(虚线名词)。
- **繁体转换**依赖 CDN 上的 opencc-js,联网时可用。

## 注意

- 洞窟数据、分期与部分描述为科普概述,不同资料说法有出入,发布前请对照权威资料校对;资料不足的洞窟已标注"待补充"。
- 照片来源于 Wikimedia Commons,请在 `IMAGE_CREDITS.md` 补全作者与授权,并遵守各自许可(如 CC BY-SA 的署名要求)。
