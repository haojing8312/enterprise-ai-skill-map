# 2026-06-01 营销 / 出海增长 Skill 候选长名单

任务：T1 信号雷达：营销 / 出海增长 Skill 候选长名单
负责人：@trend-scout

## 方法说明

- 采样源：GitHub API + README 直读、GitHub 搜索结果、HN Algolia（Show HN / 新闻）、Product Hunt 交叉线索（因 Product Hunt 直连受 Cloudflare 阻断，本轮用 HN 发帖里明确带出的 PH 链接/launch 线索补位）。
- 判定原则：只保留公开、可复核、和营销 / 出海 / 增长相关的候选；对高风险、黑产或明显越界项直接排除或不进验证池。
- 评价字段：来源证据、适用场景、初步安全判断、是否进入验证池。

## 结论快照

- 公开候选：30 个
- 进入验证池：29 个
- 暂不进池 / 排除：6 个（长名单内 1 个中风险项 + 5 个额外高风险项）
- 来源覆盖：GitHub 搜索+README、Skill/Workflow 目录、HN 传播线、Product Hunt 交叉线索

## A. GitHub：增长自动化 / 触达 / 发布 / 分析底座

1. Mautic — https://github.com/mautic/mautic
   - 证据：GitHub 描述 + README 标题“Open Source Marketing Automation Software”；约 9,773★；最近更新 2026-05-29。
   - 适用场景：生命周期邮件、线索评分、营销旅程、再营销自动化。
   - 安全判断：低风险（偏合规营销自动化）。
   - 验证池：是。

2. n8n — https://github.com/n8n-io/n8n
   - 证据：GitHub 描述“workflow automation platform ... 400+ integrations”；约 190,470★；最近更新 2026-05-31。
   - 适用场景：营销 Ops 编排、表单→CRM→邮件→报表链路。
   - 安全判断：低风险（通用自动化底座）。
   - 验证池：是。

3. Activepieces — https://github.com/activepieces/activepieces
   - 证据：GitHub 描述强调 AI Workflow Automation / AI Agents / MCP；约 22,492★。
   - 适用场景：营销流程自动化、内容分发、跨工具联动。
   - 安全判断：低风险。
   - 验证池：是。

4. Postiz — https://github.com/gitroomhq/postiz-app
   - 证据：GitHub 描述“ultimate agentic social media scheduling tool”；约 31,288★；README 显示社媒调度与品牌侧能力。
   - 适用场景：多平台发帖、内容排期、品牌语气一致性。
   - 安全判断：低风险。
   - 验证池：是。

5. Ghost — https://github.com/TryGhost/Ghost
   - 证据：GitHub 描述“publishing, memberships, subscriptions and newsletters”；约 53,747★。
   - 适用场景：内容订阅、Newsletter、会员转化。
   - 安全判断：低风险。
   - 验证池：是。

6. Notifuse — https://github.com/Notifuse/notifuse
   - 证据：GitHub 描述“modern emailing platform”；README 为现代邮件平台。
   - 适用场景：邮件活动、触达编排、增长通知。
   - 安全判断：低风险。
   - 验证池：是。

7. Dittofeed — https://github.com/dittofeed/dittofeed
   - 证据：GitHub 描述“customer engagement ... email, SMS, mobile push, WhatsApp, Slack, and more”；README 为 open-source customer engagement。
   - 适用场景：全渠道触达、产品激活、留存提醒。
   - 安全判断：低风险。
   - 验证池：是。

8. Sendportal — https://github.com/mettle/sendportal
   - 证据：GitHub 描述“self-hosted email marketing”；README 写明“Modern open-source self-hosted email marketing”。
   - 适用场景：newsletter 发送、订阅者管理、活动分析。
   - 安全判断：低风险。
   - 验证池：是。

9. phpList — https://github.com/phpList/phplist3
   - 证据：GitHub 描述“email marketing manager”；README 为功能完整的开源邮件营销管理器。
   - 适用场景：活动发送、名单管理、campaign 分析。
   - 安全判断：低风险。
   - 验证池：是。

10. Camp — https://github.com/codersgyan/camp
    - 证据：GitHub 描述“open source email marketing platform”；README 说明轻量、自托管替代 Mailchimp。
    - 适用场景：轻量 newsletter / EDM / 联系人分段。
    - 安全判断：低风险。
    - 验证池：是。

11. OpenPanel — https://github.com/Openpanel-dev/openpanel
    - 证据：GitHub 描述“web and product analytics platform ... alternative to Mixpanel”；约 5,877★。
    - 适用场景：产品增长看板、转化漏斗、事件分析。
    - 安全判断：低风险。
    - 验证池：是。

12. Plausible Analytics — https://github.com/plausible/analytics
    - 证据：GitHub 描述“privacy-first web analytics”；README 标题即为 Plausible Analytics；约 26,649★。
    - 适用场景：营销归因、流量监控、内容/落地页效果复盘。
    - 安全判断：低风险。
    - 验证池：是。

13. Umami — https://github.com/umami-software/umami
    - 证据：GitHub 描述“privacy-focused analytics platform”；README 为 Google Analytics 替代；约 36,942★。
    - 适用场景：站点分析、渠道评估、落地页 A/B 观察。
    - 安全判断：低风险。
    - 验证池：是。

14. RSSHub — https://github.com/diygod/RSSHub
    - 证据：GitHub 描述“Everything is RSSible”；README 明确是 RSS 路由/聚合基础设施；约 44,393★。
    - 适用场景：竞品监控、行业情报、内容聚合、选题雷达。
    - 安全判断：低风险。
    - 验证池：是。

## B. GitHub：Skill / Agent / Workflow 目录

15. OpenClaudia/openclaudia-skills — https://github.com/OpenClaudia/openclaudia-skills
    - 证据：README 自述“The open-source marketing toolkit for AI coding agents”；63+ 模块化 skills。
    - 适用场景：营销 SOP 模板化、AI 编码助手的增长工作流封装。
    - 安全判断：低风险。
    - 验证池：是。

16. GTM Agents — https://github.com/gtmagents/gtm-agents
    - 证据：GitHub 描述“GTM agents and specialized skills ... sales, marketing, customer success, and revenue ops”；README 直接写“Save 15+ Hours Per Week”。
    - 适用场景：GTM 自动化、线索研究、内容草稿、客户成功流程。
    - 安全判断：低风险。
    - 验证池：是。

17. AI Marketing Skills — https://github.com/ericosiu/ai-marketing-skills
    - 证据：GitHub 描述“growth experiments, sales pipeline, content ops, outbound, SEO, and finance automation”；README 开头即为 Open-source Claude Code skills for marketing and sales teams。
    - 适用场景：增长实验、销售漏斗、内容运营、SEO、财务自动化。
    - 安全判断：低风险。
    - 验证池：是。

18. AI Workflow — https://github.com/nicepkg/ai-workflow
    - 证据：GitHub 描述“170+ pre-built skills ... Marketing, SEO ... workflows included”；README 为 pre-built skill collections。
    - 适用场景：营销 / SEO / 视频 / PM 的通用技能包。
    - 安全判断：低风险。
    - 验证池：是。

19. BMad Marketing Growth — https://github.com/MatthiasMRC/bmad-marketing-growth
    - 证据：GitHub 描述“14 AI agents + 6 workflows for complete SaaS marketing”；README 写明 Marketing Growth Suite。
    - 适用场景：SaaS 增长编排、营销团队代理化。
    - 安全判断：低风险。
    - 验证池：是。

20. Awesome Claude Skills — https://github.com/ComposioHQ/awesome-claude-skills
    - 证据：GitHub 描述“curated list of awesome Claude Skills”；README 为 skills/resources/tools 目录。
    - 适用场景：作为技能目录入口，做增长技能选型与拆解。
    - 安全判断：低风险。
    - 验证池：是。

21. listmonk — https://github.com/knadh/listmonk
   - 证据：README 写明“High performance, self-hosted, newsletter and mailing list manager with a modern dashboard. Single binary app.”
   - 适用场景：newsletter / mailing list 管理、批量发送、订阅管理。
   - 安全判断：低风险。
   - 验证池：是。

22. Owkus Content Brief Generator — https://github.com/owkusweb/owkus-brief-generator
    - 证据：GitHub 描述“content brief generator for SEO”；README 写明生成结构化 Markdown briefs、关键词变体、H2/H3。
    - 适用场景：SEO 内容 brief、外包写作交付、内容生产标准化。
    - 安全判断：低风险。
    - 验证池：是。

23. Universal YouTube Video SEO Suite — https://github.com/manulanirwan/universal-youtube-seo-suite
    - 证据：GitHub 描述“client-side YouTube Video SEO Package Generator”；README 说明完全客户端、零外部依赖。
    - 适用场景：YouTube 选题、标题/描述/标签包生成、视频增长。
    - 安全判断：低风险。
    - 验证池：是。

## C. HN / Product Hunt 传播信号（Product Hunt 直连受阻，本轮以 HN 跨贴为证据）

24. Copysmith — HN story: “Copysmith – an AI-powered marketing tool that feels like magic”
    - 证据：HN Algolia 记录：2020-11-03，3 points；story text 明确写“launched publicly on Product Hunt this week”且提到“most upvoted product all week”。
    - 适用场景：广告文案、SEO meta、产品卖点生成。
    - 安全判断：低风险。
    - 验证池：是。

25. Brewly.ai — HN story: “Show HN: Brewly – AI newsletter creator for any topics you want to deep dive in”
    - 证据：HN 记录：2024-03-26，10 points / 3 comments；story 详细描述自动浏览、筛选可信来源、生成个性化 newsletter。
    - 适用场景：主题新闻简报、行业研究 newsletter、内容聚合。
    - 安全判断：低风险。
    - 验证池：是。

26. Zyler.ai — HN story: “Show HN: Zyler – AI agent for marketing data that doesn't hallucinate”
    - 证据：HN 记录：2025-06-24，7 points / 4 comments；story 提到 Product Hunt top 10、统一 GA/Ads/SEO/YouTube 数据。
    - 适用场景：营销归因、跨渠道报表、自然语言分析。
    - 安全判断：低风险。
    - 验证池：是。

27. PostPal — HN story: “AI-powered social media content scheduler with brand voice”
    - 证据：HN 记录：2025-06-02，3 points / 0 comments；story 描述 brand voice、multi-platform support、content studio。
    - 适用场景：社媒内容排期、品牌语气一致性、批量生产。
    - 安全判断：低风险。
    - 验证池：是。

28. Coso.ai — HN story: “AI Agent for social media that learns from branded content”
    - 证据：HN 记录：2025-05-28，1 point / 1 comment；story 明确写会 scrape website / social feed，并提到正在 Product Hunt 上线。
    - 适用场景：品牌社媒内容自动生成、品牌素材驱动的内容生产。
    - 安全判断：中低风险（注意数据来源与品牌授权边界）。
    - 验证池：是。

29. Mailmeteor AI writer for Gmail — HN story: “AI email assistant ... marketing campaigns”
    - 证据：HN 记录：2024-12-19，1 point；story 中有 Product Hunt launch link，且说明“privacy-first”“handles marketing campaigns”。
    - 适用场景：Gmail 内部邮件助手、跟进邮件、营销邮件草稿。
    - 安全判断：中风险（必须限制到合规/同意场景）。
    - 验证池：否（先补齐反滥用/同意控制）。

30. FluffFilter — HN story: “Content quality analysis that finds what SEO tools miss”
    - 证据：HN 记录：2025-10-27，1 point；story 明确说“Launching on Product Hunt today as well”。
    - 适用场景：内容质量审核、AI 内容去水、批量文稿审校。
    - 安全判断：低风险。
    - 验证池：是。

## D. 暂不进验证池 / 排除项（高风险或越界）

- BillionMail — https://github.com/Billionmail/BillionMail
  - 原因：虽然是开源邮件服务器 / Newsletter / Email Marketing，但 README 和仓库定位过于接近大规模群发；需要更强的反滥用、同意与退订控制后再考虑。
  - 安全判断：中高风险。
  - 验证池：否。

- UZonMail — https://github.com/uyoufu/UZonMail
  - 原因：描述包含“邮箱采集、邮件群发、多线程并发”等，明显有滥用/垃圾邮件风险。
  - 安全判断：高风险。
  - 验证池：否。

- Email Marketing AI Agent — https://github.com/theaifutureguy/email-marketing-ai-agent
  - 原因：自动化邮件序列与自动跟进虽有业务价值，但缺少清晰的 consent / opt-out / anti-spam 约束时，容易滑向黑灰产。
  - 安全判断：中高风险。
  - 验证池：否。

- LiftmyCV / auto-apply 类工具
  - 原因：与本任务营销/增长边界不符，且偏自动投递/求职流程，不纳入本次长名单。
  - 安全判断：不适用。
  - 验证池：否。

- Craigslist Posting Service / 批量发帖类项目
  - 原因：典型黑帽/垃圾信息方向，直接排除。
  - 安全判断：高风险。
  - 验证池：否。

## 建议下一步

- 先从“验证池：是”的候选里挑 3 条最强赛道做深挖：
  1) 内容/Newsletter 生产链：Ghost + Sendportal + Brief Generator
  2) 增长自动化底座：n8n + Activepieces + Dittofeed
  3) Skill 目录化：OpenClaudia + AI Marketing Skills + GTM Agents
- 下一轮可直接补一个“优先级排序版”，按“可复用性 / 合规性 / 与 OPC 内容作战室贴合度”打分。
