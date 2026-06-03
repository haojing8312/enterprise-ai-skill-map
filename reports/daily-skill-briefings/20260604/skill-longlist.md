# 2026-06-04 实用 Skill 技能早报候选长名单

主题重心：营销类、出海营销类、增长获客类 Skill / Agent / 开源工作流。

## 本轮信号覆盖
- GitHub Search：已按 `marketing ai agent`、`seo ai agent`、`claude skill marketing`、`claude skill seo`、`social media ai agent`、`outbound sales agent`、`growth agent ai` 等查询，并按 stars / recent pushed 过滤。
- GitHub Trending：已检查 daily trending；当日泛 AI/工具项较多，营销垂直强相关不足，仅作为辅助信号。
- 新项目 / star-growth：重点记录 2026 年仍在更新、近期 pushed 的营销 Skill 仓库；例如 `coreyhaines31/marketingskills`、`eracle/OpenOutreach`、`yaojingang/GEOFlow`、`LeoYeAI/openclaw-marketing-skills` 等均在 2026-06 附近仍有更新/传播。
- 开发者社交传播：Hacker News Algolia 命中 `Marketing Skills for Claude Code`、`AI Marketing Skills for Claude Code`、`Open-Source GTM Skills for Claude Code, Codex, and Cursor`、`Geo-lint` 等开发者发布信号。
- Product Hunt / Reddit：Product Hunt 公开搜索链路受反爬/登录限制，本轮未作为精确排名来源；Reddit JSON 搜索返回 403，被记录为不可用信号，不据此编造热度。
- 直接 repo 检查：对核心候选检查 README / skills 目录 / SKILL.md / license / 更新日期；安全上默认只推荐公开仓库，不推荐绕过平台规则、批量骚扰、凭据滥用类用法。

## 候选长名单（24）

| # | 候选 | URL | 类型 | 公开信号 | 用途 | 初筛安全判断 |
|---|---|---|---|---|---|---|
| 1 | coreyhaines31/marketingskills | https://github.com/coreyhaines31/marketingskills | Skill 库 | GitHub Search 强信号；2026-06-03 查询约 31.7k stars，MIT，skills 目录含 43 项；HN 有 Show HN/讨论记录 | CRO、文案、SEO、分析、增长工程的一揽子营销技能 | verified_public；注意不要把输出当合规承诺 |
| 2 | AgriciDaniel/claude-seo | https://github.com/AgriciDaniel/claude-seo | SEO Skill 套件 | GitHub Search SEO 类强信号；约 8k stars，MIT，25 个 skills | 技术 SEO、E-E-A-T、schema、GEO/AEO、报告 | verified_public；部分外部 API 可选，需提醒密钥自管 |
| 3 | zubair-trabzada/geo-seo-claude | https://github.com/zubair-trabzada/geo-seo-claude | GEO/SEO Skill | GitHub Search GEO/SEO 强信号；约 7.8k stars，MIT，skills 目录 | AI 搜索优化、citability、品牌权威、schema | verified_public；不要夸大 GEO 排名效果 |
| 4 | yaojingang/GEOFlow | https://github.com/yaojingang/GEOFlow | 开源工作流/Agent | GitHub Search SEO/GEO；约 2.4k stars，Apache-2.0，2026-06-03 pushed | GEO 内容工程、多站分发、RAG 语义分块、WordPress 发布 | verified_public；涉及自动发布需人工审核 |
| 5 | oaker-io/wewrite | https://github.com/oaker-io/wewrite | 内容生产 Skill | GitHub Search Claude SEO；约 2.1k stars，MIT，含 SKILL.md | 公众号热点抓取、选题、写作、SEO、视觉、排版、草稿箱 | verified_public；不应替代事实核查/版权审核 |
| 6 | eracle/OpenOutreach | https://github.com/eracle/OpenOutreach | Outbound Agent | GitHub Search marketing；约 2k stars，2026-06-02 pushed | 描述产品和目标市场后寻找 LinkedIn leads | watchlist；LinkedIn 自动化/群发存在平台规则和骚扰风险，需边界说明 |
| 7 | aaron-he-zhu/seo-geo-claude-skills | https://github.com/aaron-he-zhu/seo-geo-claude-skills | SEO/GEO Skill 库 | GitHub Search marketing/seo；约 1.9k stars，Apache-2.0 | 关键词研究、内容写作、技术审计、排名跟踪 | verified_public；外部工具与排名数据需用户自行合规接入 |
| 8 | Eronred/aso-skills | https://github.com/Eronred/aso-skills | ASO Skill 库 | GitHub Search growth/marketing；约 1.45k stars，MIT，skills 目录 40+ | App Store 优化、关键词、元数据、竞品分析、应用增长 | verified_public；应用商店规则需人工复核 |
| 9 | LeoYeAI/openclaw-marketing-skills | https://github.com/LeoYeAI/openclaw-marketing-skills | OpenClaw Marketing Skill | GitHub Search marketing/growth；约 1.27k stars，含 SKILL.md 和 30+ skills | 广告创意、AI SEO、分析追踪、留存、增长技能 | watchlist；license 为 NOASSERTION，入库时标注许可待确认 |
| 10 | onvoyage-ai/gtm-engineer-skills | https://github.com/onvoyage-ai/gtm-engineer-skills | GTM/GEO Skill | GitHub Search SEO；约 1.1k stars，MIT，2026-06-02 pushed | 网站 AEO/GEO 16 项基础检查、6 维智能诊断 | verified_public；适合站点自查，不保证排名结果 |
| 11 | AgriciDaniel/claude-blog | https://github.com/AgriciDaniel/claude-blog | Blog Skill 套件 | GitHub Search marketing/seo；约 960 stars | 博客交付流程、Google 排名、AI citation 优化 | verified_public；内容事实核查仍需人工 |
| 12 | kostja94/marketing-skills | https://github.com/kostja94/marketing-skills | Marketing Skill 库 | GitHub Search claude skill marketing；约 574 stars，2026-06-01 pushed | SEO、社交、Influencer、页面类型、付费广告 | watchlist；未完成本轮 API 复核，需二次检查 license/目录 |
| 13 | aitytech/agentkits-marketing | https://github.com/aitytech/agentkits-marketing | Agent Kits | GitHub Search marketing；约 525 stars | 企业级营销自动化、Claude/Cursor/GitHub Copilot 等 | watchlist；需确认可复现路径与许可 |
| 14 | JeffLi1993/seo-audit-skill | https://github.com/JeffLi1993/seo-audit-skill | SEO Audit Skill | GitHub Search SEO；约 445 stars，2026-06-03 pushed | 生成基础/高级技术 SEO 报告 | watchlist；需确认 license 和报告来源边界 |
| 15 | Affitor/affiliate-skills | https://github.com/Affitor/affiliate-skills | Affiliate Marketing Skill | GitHub Search marketing；约 430 stars | 联盟营销内容研究、数据帖、信息图、落地页 | watchlist；联盟营销合规与广告披露需提醒 |
| 16 | blacktwist/social-media-skills | https://github.com/blacktwist/social-media-skills | Social Media Skill | GitHub Search social media；约 213 stars | 社交内容策略、创作与分析 | watchlist；需二次复核 license/安全 |
| 17 | superamped/ai-marketing-skills | https://github.com/superamped/ai-marketing-skills | AI Marketing Skills | HN Show HN 命中；GitHub Search growth 约 42 stars | SEO、文案、竞品研究、广告、营销策略 | watchlist；低 star 但有开发者发布信号 |
| 18 | getaero-io/gtm-eng-skills | https://github.com/getaero-io/gtm-eng-skills | GTM Engineering Skill | GitHub Search outbound；约 25 stars，2026-06-03 pushed；HN 命中 Open-Source GTM Skills | 邮箱补全、TAM、信号发现、职位变动、Outbound | watchlist；GTM 数据供应商/个人数据边界需严格标注 |
| 19 | apify/apify-mcp-server | https://github.com/apify/apify-mcp-server | MCP Server / 数据采集工具 | GitHub Search social media；约 1.3k stars，2026-06-03 pushed | 给 AI agent 接入公开网页/社交/地图/电商采集能力 | watchlist；只能采公开数据，禁止绕过权限/抓取隐私 |
| 20 | enescingoz/awesome-n8n-templates | https://github.com/enescingoz/awesome-n8n-templates | 工作流模板库 | GitHub Search social media；约 22k stars | 邮件、社媒、聊天机器人、自动化模板 | verified_public；模板质量需逐条检查 |
| 21 | postiz-app/postiz-app | https://github.com/gitroomhq/postiz-app | 开源社媒排程工具 | 已知开源增长工具；需二次 GH API 复核 | 社媒内容排程、团队协作、可能含 AI 辅助 | watchlist；平台授权和发布审批需明确 |
| 22 | mendableai/firecrawl | https://github.com/mendableai/firecrawl | 爬取/内容采集底座 | 已知开源 LLM 爬取工具，常用于市场/竞品研究 | 把网页转成 LLM 可用数据，用于竞品、内容、线索研究 | watchlist；遵守 robots、版权和访问权限 |
| 23 | ScrapeGraphAI/Scrapegraph-ai | https://github.com/ScrapeGraphAI/Scrapegraph-ai | LLM 采集工作流 | 已知开源 scraping + LLM 项目 | 结构化抓取网页数据，服务竞品/内容研究 | watchlist；同样需公开数据边界 |
| 24 | browser-use/browser-use | https://github.com/browser-use/browser-use | 浏览器 Agent | 已知热门浏览器自动化 agent | 自动浏览网页，可用于市场调研/竞品检查 | watchlist；登录、Cookie、真实提交动作需隔离 |

## 初筛建议
- 优先进入今日早报：`marketingskills`、`seo-geo-claude-skills`、`aso-skills`、`gtm-engineer-skills`、`GEOFlow`。
- 适合放 watchlist、不宜直接强推：`OpenOutreach`、`gtm-eng-skills`、`apify-mcp-server`、`browser-use`，原因是触达个人数据、自动化动作或第三方平台规则风险更高。
- 今日不编造 Product Hunt/Reddit 排名；只能写 GitHub/HN/直接 repo 证据。
