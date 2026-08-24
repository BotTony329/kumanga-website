# Kumanga 站外可见度行动清单 — 2026-08-24

代码层面的 SEO/GEO 优化已经完成（canonical、robots.txt、sitemap、结构化数据、FAQ、llms.txt）。
以下是**代码做不了、需要你本人执行**的事项，按优先级排序。对一个独立开源项目来说，
这些站外动作往往比代码改动更能决定被搜到、被 AI 推荐的程度。

## 本周做一次（合计约 2–3 小时）

### 1. 注册 Google Search Console + Bing Webmaster Tools（最高优先级）
- 访问 [search.google.com/search-console](https://search.google.com/search-console)，添加资源
  `https://kumanga-website.vercel.app/`，验证后提交 `sitemap.xml`。
- 这是你能看到"哪些词搜到了你、排名多少、AI/搜索爬虫抓取是否正常"的唯一官方入口。
- Bing 站长工具同理（[bing.com/webmasters](https://www.bing.com/webmasters)），Bing 还 feeding ChatGPT 的搜索结果。

### 2. 处理旧部署域名（消除重复内容）
- `kumanga-website-personal-b90d.vercel.app` 和正式域名同时在线提供相同内容。
  页面已加 canonical 标签指向正式域名，能兜底；但更干净的做法是在 Vercel 项目设置里
  把旧域名删除，或配置 301 跳转到 `kumanga-website.vercel.app`。
- og:image 已改为正式域名，此项已修复。

### 3. 打磨 GitHub 仓库（AI 引擎 heavily 参考的权威源）
- `BotTony329/mangaharness` 的 description 目前只有 "a manga harness"。改成含关键词的完整描述，
  例如：`Kumanga — an open-source, local-first AI manga harness. Reusable characters, non-destructive editor, natural-language Manga Agent. BYOK, no account.`
- 添加 Topics：`ai-manga` `manga-creator` `comic-generator` `local-first` `byok` `open-source` `webtoon` `ai-agent`。
- 在仓库 About 里填 Website 链接指向 `https://kumanga-website.vercel.app/`，README 顶部也加上。
- 官网页脚已链接仓库，形成双向权威闭环。

### 4. 优化两个 YouTube 演示视频的标题和描述
- 标题带关键词（如 "Kumanga Demo — Reusable Character Relations (Open-Source AI Manga Studio)"）。
- 描述里放官网链接、GitHub 链接和一句话项目简介；加标签 ai manga / manga studio / webtoon。
- YouTube 是第二大搜索引擎，且越来越多被 AI 答案直接引用。

## 每月习惯（每次 30–60 分钟）

### 5. 手动检查 AI 引用情况
- 向 ChatGPT、Perplexity、Gemini、Claude 问这些目标查询，记录 Kumanga 是否被提及、描述是否准确：
  - "open source AI manga creator"
  - "AI manga generator that runs locally"
  - "local-first AI comic maker"
  - "AI manga tool with reusable characters"
  - "what is Kumanga"
- 描述有误通常能追溯到某个过时的目录/仓库字段——回到源头修。

### 6. 社区存在感（GEO 的核心输入）
- AI 引擎非常看重跨独立来源的品牌提及（甚至无链接的提及）。每月至少 1–2 次：
  在 Reddit（r/manga、r/aiArt、r/SideProject、r/webtoons）、Hacker News（Show HN）、
  相关 Discord 社区以创作者身份回答问题、分享进展。
- 规则：只做真实分享，不发垃圾推广——被社区惩罚的损失远大于收益。

### 7. 监测 AI 引荐流量
- 如果装了 GA4：添加自定义细分，过滤引荐来源 `chatgpt.com`、`perplexity.ai`、
  `gemini.google.com`、`claude.ai`，每月看一次趋势。

## 有空再做（Nice to have）

### 8. 注册独立域名
- `vercel.app` 子域名可用但品牌可信度弱于自有域名（如 `kumanga.dev` / `kumangastudio.com`）。
  注册后迁移时：Vercel 里加新域名、全站 URL/sitemap/canonical/llms.txt 同步替换、旧域名 301。

### 9. 精选 3–5 个高质量目录（不买批量提交包）
- 候选：Product Hunt（Kickstarter 上线时首发效果最好）、AlternativeTo、
  面向创作者的 AI 工具目录。只选有真实流量的，拒绝 bulk directory。

### 10. 写一篇"原创数据/过程"文章
- 例如 "How we made AI characters stay consistent across 3 manga pages"，
  放在官网新开 /blog 或 dev.to / Medium。原创方法论和一手数据是 AI 答案中
  被引用最多的内容类型，也给搜索提供长尾入口。

### 11. Kickstarter 上线时的传播包
- 上线当天：Show HN、相关 Subreddit、漫画创作者 YouTuber/newsletter 私信合作。
- 提前准备一页 press kit（logo、海报、两句简介、链接）。

---

**预期管理**：搜索排名和 AI 引用的变化以**周/月**计，不会立刻生效。新站被索引
通常需要几天到几周；AI 助手开始引用一个新品牌通常需要它先在多个独立来源出现。
第 1、3、4 项做完后，基础信号就齐了。
