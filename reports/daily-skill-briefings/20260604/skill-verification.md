# 2026-06-04 Skill 早报候选复核

复核范围：从长名单中抽查 8 个公开候选，优先营销 / 出海营销 / GEO / 增长。  
复核方法：
- 已读取上游长名单：`/mnt/f/code/work/公众号文章/skill-brief-daily/20260604/research/skill-longlist.md`。
- 逐项 shallow clone 公开 repo 到 `/tmp/skillverify-20260604/`，检查 README、LICENSE/LICENCE、SKILL.md 或核心目录、最近 commit。
- 通过 GitHub 页面 HTML 解析星标数；GitHub REST API 本轮返回 unauth rate limit，未用 API 数据硬填。
- 评分规则：ranking/growth 30，practical usefulness 30，reproducibility 15，safety 15，communication value 10。低于 70 不进早报；未解决安全风险为 blocked。

## 入选结论

今日建议进入早报 5 个：
1. `coreyhaines31/marketingskills` — 营销 Skill 大库，覆盖 CRO/文案/SEO/增长工程。
2. `AgriciDaniel/claude-seo` — SEO/GEO 全链路分析 Skill，证据和可复现结构最完整。
3. `zubair-trabzada/geo-seo-claude` — GEO-first 叙事清晰，适合讲 AI 搜索优化。
4. `yaojingang/GEOFlow` — 中文/多语言 GEO 内容工程 + 多站分发系统，适合出海内容资产流水线。
5. `Eronred/aso-skills` — App Store Optimization / 移动应用增长 Skill，垂直场景清晰。

未入选但可继续观察：`onvoyage-ai/gtm-engineer-skills`、`aaron-he-zhu/seo-geo-claude-skills`。  
不推荐：`eracle/OpenOutreach`，安全/平台规则风险未解决，列 blocked。

## 评分总览

| 候选 | URL | license | ranking/growth | usefulness | reproducibility | safety | comms | 总分 | 状态 | 今日 |
|---|---|---:|---:|---:|---:|---:|---:|---:|---|---|
| coreyhaines31/marketingskills | https://github.com/coreyhaines31/marketingskills | MIT | 30 | 29 | 14 | 12 | 10 | 95 | verified_public | 入选 |
| AgriciDaniel/claude-seo | https://github.com/AgriciDaniel/claude-seo | MIT | 27 | 29 | 15 | 13 | 9 | 93 | verified_public | 入选 |
| zubair-trabzada/geo-seo-claude | https://github.com/zubair-trabzada/geo-seo-claude | MIT | 26 | 27 | 13 | 12 | 10 | 88 | verified_public | 入选 |
| yaojingang/GEOFlow | https://github.com/yaojingang/GEOFlow | Apache-2.0 | 23 | 29 | 13 | 11 | 9 | 85 | verified_public | 入选 |
| Eronred/aso-skills | https://github.com/Eronred/aso-skills | MIT | 21 | 28 | 13 | 13 | 9 | 84 | verified_public | 入选 |
| onvoyage-ai/gtm-engineer-skills | https://github.com/onvoyage-ai/gtm-engineer-skills | MIT | 20 | 27 | 13 | 12 | 9 | 81 | watchlist | 不入选 |
| aaron-he-zhu/seo-geo-claude-skills | https://github.com/aaron-he-zhu/seo-geo-claude-skills | Apache-2.0 | 22 | 25 | 14 | 12 | 8 | 81 | watchlist | 不入选 |
| eracle/OpenOutreach | https://github.com/eracle/OpenOutreach | GPL-3.0 | 20 | 20 | 11 | 0 | 8 | 59 | blocked | 不入选 |

---

## 1. coreyhaines31/marketingskills

- URL: https://github.com/coreyhaines31/marketingskills
- License: MIT（根目录 `LICENSE`：MIT License, copyright Corey Haines）
- 用途: 给 Claude Code / Codex / Cursor / Windsurf 等 agent 使用的营销 Skill 库，覆盖 conversion optimization、copywriting、SEO、analytics、growth engineering、cold email、pricing、ASO 等。
- 公开证据:
  - GitHub HTML 解析星标：31,774。
  - shallow clone 成功，origin 为 `https://github.com/coreyhaines31/marketingskills.git`。
  - 最近 commit：`7f4af1e`，2026-05-29，`Merge pull request #343 from coreyhaines31/development`。
  - README 标题为 “Marketing Skills for AI Agents”，说明它是 “A collection of AI agent skills focused on marketing tasks”，并称适配 Claude Code、OpenAI Codex、Cursor、Windsurf 与 Agent Skills spec。
  - 文件复核：365 个文件；`skills/` 下检出 184 个 skill/references/evals 相关文件；样例包括 `skills/cro/SKILL.md`、`skills/copywriting/SKILL.md`、`skills/cold-email/SKILL.md`、`skills/aso/SKILL.md`。
  - `skills/product-marketing/SKILL.md` 明确会创建/维护 `.agents/product-marketing.md`，作为产品、受众、定位上下文；`skills/cold-email/SKILL.md` 包含 B2B cold email 和 follow-up sequence 工作流。
- 评分: 95 = ranking/growth 30 + usefulness 29 + reproducibility 14 + safety 12 + communication 10。
- 状态: verified_public。
- 安全边界: 只推荐作为营销研究、文案、CRO、SEO 和内部增长实验辅助；冷邮件/外联内容必须人工审核、合规退订、遵守当地反垃圾邮件规则；不得用于采集隐私、冒充身份、批量骚扰或绕过平台规则；输出不是合规/排名承诺。
- 入选理由: 星标和 repo 结构均为本轮最强，覆盖早报主题最广；“营销 Skill 大库”容易被读者立即理解和试用。

## 2. AgriciDaniel/claude-seo

- URL: https://github.com/AgriciDaniel/claude-seo
- License: MIT（根目录 `LICENSE`，各 skill 目录另有 `LICENSE.txt` 指向 MIT）
- 用途: Claude Code SEO 分析插件，覆盖技术 SEO、E-E-A-T、Schema、AI Overviews / ChatGPT / Perplexity 的 GEO、local/e-commerce/international SEO，以及可选外部数据扩展。
- 公开证据:
  - GitHub HTML 解析星标：8,063。
  - shallow clone 成功，origin 为 `https://github.com/AgriciDaniel/claude-seo.git`。
  - 最近 commit：`dabfc1a`，2026-05-25，`chore(public): rebrand marketplace to agricidaniel-claude-seo`。
  - README 写明 “Universal SEO skill for Claude Code. 25 sub-skills + 18 sub-agents”，并说明 “Every audit produces a prioritized action plan with falsifiable recommendations grounded in primary-source guidance from Google”。
  - 文件复核：362 个文件；`skills/` 与 `extensions/` 下检出 161 个 skill/references/license 相关文件；样例包括 `skills/seo/SKILL.md`、`skills/seo-geo/SKILL.md`、`skills/seo-technical/SKILL.md`。
  - `skills/seo/SKILL.md` 的 description 覆盖 crawlability、indexability、Core Web Vitals、schema、E-E-A-T、AI Overviews、GEO；`skills/seo-geo/SKILL.md` 明确覆盖 llms.txt、citability scoring、AI crawler accessibility。
- 评分: 93 = ranking/growth 27 + usefulness 29 + reproducibility 15 + safety 13 + communication 9。
- 状态: verified_public。
- 安全边界: 可选 Firecrawl/DataForSEO/Ahrefs 等外部扩展时，API key 需由用户自管；抓取和审计仅限有权访问的公开站点，遵守 robots/服务条款/版权；SEO/GEO 建议需人工核验，不承诺 Google 或 AI 搜索排名。
- 入选理由: SEO/GEO 主题刚需强，README、skill 数量、license、测试/CI 信号齐全，可复现性高。

## 3. zubair-trabzada/geo-seo-claude

- URL: https://github.com/zubair-trabzada/geo-seo-claude
- License: MIT（根目录 `LICENSE`）
- 用途: GEO-first SEO Skill，面向 ChatGPT、Claude、Perplexity、Gemini、Google AI Overviews 等 AI 搜索/回答引擎优化，覆盖 AI citability、llms.txt、schema、brand mentions、平台化 GEO 报告。
- 公开证据:
  - GitHub HTML 解析星标：7,850。
  - shallow clone 成功，origin 为 `https://github.com/zubair-trabzada/geo-seo-claude.git`。
  - 最近 commit：`9eec32f`，2026-05-26，`Move star history chart above Why GEO Matters section`。
  - README 首屏文案为 “GEO-first, SEO-supported. Optimize websites for AI-powered search engines”。
  - 文件复核：67 个文件；检出 16 个 Skill 文件，包括 `geo/SKILL.md`、`skills/geo-audit/SKILL.md`、`skills/geo-citability/SKILL.md`、`skills/geo-llmstxt/SKILL.md`、`skills/geo-report/SKILL.md`。
  - `geo/SKILL.md` 明确描述 full GEO audits、citability scoring、AI crawler analysis、llms.txt generation、brand mention scanning、schema markup、client-ready GEO report generation。
- 评分: 88 = ranking/growth 26 + usefulness 27 + reproducibility 13 + safety 12 + communication 10。
- 状态: verified_public。
- 安全边界: 作为 GEO/SEO 诊断和内容改写辅助；不要把 README 中市场/流量增长叙述包装成确定收益；Skill 声明可用 Bash/WebFetch/Write，运行时应限定在目标项目目录、避免写入生产站点；抓取只限公开且有权访问内容。
- 入选理由: GEO-first 叙事强，和“AI 搜索优化”热点高度贴合，读者一眼能理解差异化。

## 4. yaojingang/GEOFlow

- URL: https://github.com/yaojingang/GEOFlow
- License: Apache-2.0（根目录 `LICENSE`，README 中明确 Apache License 2.0，含商业使用说明）
- 用途: GEO 内容工程与多站点分发系统，把知识库、素材库、提示词、AI 生成任务、审核发布、数据分析、WordPress REST、通用 HTTP API、远端静态页面分发串成内容资产流水线。
- 公开证据:
  - GitHub HTML 解析星标：2,462。
  - shallow clone 成功，origin 为 `https://github.com/yaojingang/GEOFlow.git`。
  - 最近 commit：`2b175ea`，2026-06-03，`Harden OpenAI-compatible embedding handling`。
  - README 中文和英文版均存在；英文版写明 “open-source GEO content engineering and multi-site distribution system”。
  - 文件复核：658 个文件；存在 `docker-compose.yml`、`docker-compose.prod.yml`、`composer.json`、`package.json`、`docs/`、`deploy-scripts/`、`.env.example`、`.env.prod.example`，说明是完整应用而非单个提示词文件。
  - README 功能表明确包括多模型内容生成、知识库/RAG、素材与提示词体系、任务自动化、审核与文章管理、多站点分发管理。
- 评分: 85 = ranking/growth 23 + usefulness 29 + reproducibility 13 + safety 11 + communication 9。
- 状态: verified_public。
- 安全边界: 多站发布和 WordPress/HTTP API 发布必须启用人工审核、发布节奏和回滚流程；知识库素材需确认版权和事实来源；密钥放 `.env`，不要提交；生成内容不得自动发布到生产站或伪造来源/作者。
- 入选理由: 与“出海/GEO 内容资产流水线”强相关，且 2026-06-03 仍在更新；作为系统型项目能补足纯 Skill 库之外的应用场景。

## 5. Eronred/aso-skills

- URL: https://github.com/Eronred/aso-skills
- License: MIT（根目录 `LICENSE`）
- 用途: App Store Optimization 与移动应用营销 Skill 库，服务 indie developers、app marketers、growth teams，支持关键词研究、元数据优化、竞品分析、市场情报、转化/付费/留存相关增长。
- 公开证据:
  - GitHub HTML 解析星标：1,451。
  - shallow clone 成功，origin 为 `https://github.com/Eronred/aso-skills.git`。
  - 最近 commit：`dbb99d2`，2026-05-08，`Enhance README and REGISTRY with new skills and routing information`。
  - README 写明 “AI agent skills for App Store Optimization (ASO) and mobile app marketing”，并说明可在 Cursor、Claude Code 或 Agent Skills-compatible assistant 中使用。
  - 文件复核：60 个文件；检出 41 个 `skills/` 相关文件，样例包括 `skills/aso-audit/SKILL.md`、`skills/keyword-research/SKILL.md`、`skills/metadata-optimization/SKILL.md`、`skills/competitor-analysis/SKILL.md`、`skills/apple-search-ads/SKILL.md`、`skills/paywall-optimization/SKILL.md`。
  - `skills/aso-audit/SKILL.md` 要求 App ID、国家、平台，并在 Appeeky MCP/API 可用时拉取 metadata、keyword rankings、competitors；`keyword-research` 和 `competitor-analysis` 有清晰输入与流程。
- 评分: 84 = ranking/growth 21 + usefulness 28 + reproducibility 13 + safety 13 + communication 9。
- 状态: verified_public。
- 安全边界: Appeeky API / App Store 数据接入需用户授权和密钥自管；应用商店元数据、关键词、截图、广告素材要人工审核，遵守 Apple/Google Play 规则；不要用生成内容规避审核或夸大下载/收入效果。
- 入选理由: ASO 是增长垂直刚需，和 SEO/GEO 不完全重复，能扩展早报读者的“应用增长”视角。

## 6. onvoyage-ai/gtm-engineer-skills

- URL: https://github.com/onvoyage-ai/gtm-engineer-skills
- License: MIT（根目录 `LICENSE`）
- 用途: GTM / AEO / GEO 工作流 Skill，产出 brand DNA、关键词/GEO prompt cluster、内容架构、AI-citable charts、AEO audit、backlink/resource pages 等可审核 artifact。
- 公开证据:
  - GitHub HTML 解析星标：1,109。
  - shallow clone 成功，origin 为 `https://github.com/onvoyage-ai/gtm-engineer-skills.git`。
  - 最近 commit：`fbe9343`，2026-06-02，`Rewrite README intro and remove logo`。
  - README 写明 “Each skill is a focused agent workflow that ships a concrete GTM artifact”。
  - 文件复核：75 个文件；检出 12 个 Skill 文件，包括 `audit-website-aeo/SKILL.md`、`research-keywords/SKILL.md`、`geo-content-research/SKILL.md`、`reddit-opportunity-research/SKILL.md`、`build-backlinks/SKILL.md`、`improve-aeo-geo/SKILL.md`。
  - `audit-website-aeo/SKILL.md` 明确 16 个 deterministic checks + 6 维内容评价；`reddit-opportunity-research/SKILL.md` 明确 “for promotion through useful participation, not spam”。
- 评分: 81 = ranking/growth 20 + usefulness 27 + reproducibility 13 + safety 12 + communication 9。
- 状态: watchlist。
- 安全边界: Reddit 研究仅限公开讨论和有帮助参与，遵守 subreddit 规则，不建议批量发帖/软广；AEO 网站审计要限制 crawl depth/rate；backlink/resource page 建议不得演化为链接农场或垃圾外链。
- 不入选理由: 项目质量可用且主题贴合，但今日 5 个名额已覆盖营销大库、SEO/GEO、GEOFlow 和 ASO；此项与 GEO/SEO 内容 pipeline 有一定重叠，放 watchlist 留作后续 GTM 专题。

## 7. aaron-he-zhu/seo-geo-claude-skills

- URL: https://github.com/aaron-he-zhu/seo-geo-claude-skills
- License: Apache-2.0（根目录 `LICENSE`；各 `SKILL.md` front matter 标注 Apache-2.0）
- 用途: SEO & GEO Skills Library，20 个 skills / commands，用于关键词研究、SERP 分析、内容 gap、技术 SEO、GEO 内容优化、schema、rank tracking、AI response checks 等。
- 公开证据:
  - GitHub HTML 解析星标：1,977。
  - shallow clone 成功，origin 为 `https://github.com/aaron-he-zhu/seo-geo-claude-skills.git`。
  - 最近 commit：`b69ebc6`，2026-05-14，`v9.9.9: consolidated 9.x final`。
  - README 写明 “20 skills. 20 commands. Plan, audit, and monitor SEO/GEO work”，并列出 Claude Code、Cursor、Codex CLI、Gemini CLI、Qwen Code 等兼容目标。
  - 文件复核：221 个文件；检出 20 个 `SKILL.md`，包括 `research/keyword-research/SKILL.md`、`build/geo-content-optimizer/SKILL.md`、`monitor/rank-tracker/SKILL.md`、`optimize/technical-seo-checker/SKILL.md`、`build/schema-markup-generator/SKILL.md`。
  - `build/geo-content-optimizer/SKILL.md` 的 when_to_use 覆盖 ChatGPT、Perplexity、AI Overviews、Gemini、Claude / AI citation optimization；`monitor/rank-tracker` 包括 AI response checks。
- 评分: 81 = ranking/growth 22 + usefulness 25 + reproducibility 14 + safety 12 + communication 8。
- 状态: watchlist。
- 安全边界: 排名、流量、关键词难度等数据应来自用户提供的导出或合规连接工具，不得凭空编造；GEO/SEO 建议不等于排名保证；不要自动生成垃圾外链、关键词堆砌或误导性 schema。
- 不入选理由: 证据充分、可复现性较好，但与 `AgriciDaniel/claude-seo` 和 `zubair-trabzada/geo-seo-claude` 主题重合；今日早报需要降低同质化，故暂列 watchlist。

## 8. eracle/OpenOutreach

- URL: https://github.com/eracle/OpenOutreach
- License: GPL-3.0（根目录 `LICENCE.md` 为 GNU General Public License v3；README badge 也标 GPLv3）
- 用途: 自托管 LinkedIn 自动化 B2B lead generation 工具。用户描述产品和目标市场后，系统生成 LinkedIn 搜索、发现/筛选 profile，并可能联系目标人群。
- 公开证据:
  - GitHub HTML 解析星标：2,008。
  - shallow clone 成功，origin 为 `https://github.com/eracle/OpenOutreach.git`。
  - 最近 commit：`1a9628c`，2026-06-02，`Let user clear LinkedIn checkpoint in live browser before daemon exits; document noVNC 6080 viewer`。
  - README 写明 “self-hosted, open-source LinkedIn automation tool for B2B lead generation”，并说明会 autonomously discovers, qualifies, and contacts people。
  - 文件复核：181 个文件；存在 `crm/`、`linkedin/`、`chat/`、`compose/`、`requirements/`、`LEGAL_NOTICE.md`、`ARCHITECTURE.md`。
  - `LEGAL_NOTICE.md` 明确写到 LinkedIn automation is prohibited by LinkedIn，运行该软件 violates LinkedIn Terms of Service，可能导致账号限制/封禁/法律风险；还写到部分非 GDPR 等司法辖区首次运行会自动启用 newsletter subscription。
- 评分: 59 = ranking/growth 20 + usefulness 20 + reproducibility 11 + safety 0 + communication 8。
- 状态: blocked。
- 安全边界: 不推荐读者运行或用于实际触达；不应用个人 LinkedIn 凭据/会话做自动化登录、访问、消息、加好友或 profile 访问；不应自动订阅 newsletter；不应用于采集个人数据或绕过平台反自动化机制。
- 不入选理由: 虽有增长/外联场景和公开热度，但 repo 自身法律声明确认违反 LinkedIn ToS，并存在凭据/会话自动化和自动订阅问题；属于未解决安全风险，按规则 blocked，不进早报。

## 复核问题记录

- GitHub REST API 本轮返回 `HTTP Error 403: rate limit exceeded`；已改用公开 GitHub HTML、git shallow clone、README/LICENSE/SKILL.md 本地复核，不编造 API 数据。
- 未生成图片，未发布任何内容。
