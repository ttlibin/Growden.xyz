# Growden.xyz 网站说明

本仓库为 Growden.xyz 的单页网站，围绕关键词“Growden.io”进行 SEO 优化，并在首页通过 iframe 嵌入在线游戏 `https://growden.io`。

## 预览与使用
- 本地预览：直接双击或用浏览器打开 `index.html` 即可。
- Canonical 域名：`https://growden.xyz/`
- 游戏源站：`https://growden.io`

## 技术栈
- 纯静态单页：`index.html`
- 样式：Tailwind CSS（CDN 版，支持 light/dark）
- SEO：Title/Description、Canonical、OG/Twitter、FAQ JSON‑LD 结构化数据
- 性能：`dns-prefetch` + `preconnect` 到游戏域；iframe 懒加载 + 骨架占位

## 文件结构
- `index.html`：主页面（Hero、Features、How to Play、Why、FAQ、iframe）
- `SEO_README.md`：英文 SEO 文案来源
- `README.md`：当前文档

## 自定义与开发
- 颜色方案：
  - 浅色（Fresh Garden）：`bg-slate-50` + `bg-green-600`
  - 深色（Frosty Night）：`dark:bg-slate-950` + 蓝/青点缀
- 深浅色切换：`<html class="dark">` + `localStorage.theme`；右上角按钮切换
- 锚点导航：`#play`、`#what-is`、`#features`、`#how-to-play`、`#why`、`#faq`
- 标题与图标：H2/H3 已居中并加入 Emoji 图标

## SEO 要点（已内置）
- Title/Description 含“Growden.io”，仅一个 H1，多组 H2/H3
- Canonical 指向 `https://growden.xyz/`
- Open Graph / Twitter Card 元信息
- FAQPage JSON‑LD（5 条问答）

## 性能注意
- iframe 内容不被搜索引擎索引，但能提升互动与转化
- 已加入 `dns-prefetch`、`preconnect` 与骨架占位，避免加载前空白
- 建议压缩 `og-image.jpg`

## 部署建议
- 作为静态站点托管（Vercel/Netlify/Cloudflare Pages/Nginx 等），根路径指向 `index.html`

## 后续可做
- 生成 `sitemap.xml` 与 `robots.txt`
- 替换/优化分享图 `og-image.jpg`
- 扩展更多图标/插画与内链模块
