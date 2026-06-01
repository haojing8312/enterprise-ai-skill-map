# Enterprise AI Skill Map

帮企业、出海团队和超级个体快速找到可落地的 AI Skill / Agent / 自动化工作流。

这个仓库不追求“把所有工具都列出来”，而是帮你回答一个更实际的问题：

> 我现在有一个业务目标，应该先用哪些 Skill？怎么组合？风险在哪里？

## 5 秒开始

| 你现在的目标 | 直接看这里 |
|---|---|
| 我是出海公司，要做 GEO / SEO / 内容增长 | [`tracks/overseas-geo-marketing.md`](tracks/overseas-geo-marketing.md) |
| 我要做营销自动化和线索获取 | [`tracks/marketing-automation.md`](tracks/marketing-automation.md) |
| 我要搭内容生产与分发系统 | [`tracks/content-engine.md`](tracks/content-engine.md) |
| 我要给研发团队上 AI 编码流程 | [`tracks/ai-coding-workflow.md`](tracks/ai-coding-workflow.md) |
| 我要连接 Gmail / Slack / Apollo / GSC 等应用 | [`app-automations/README.md`](app-automations/README.md) |
| 我第一次来，只想看推荐路线 | [`START_HERE.md`](START_HERE.md) |

## 推荐路线

1. **出海 GEO / SEO 内容增长**：公开信号监控、竞品内容、搜索表现、Newsletter、内容阵地。  
   → [`tracks/overseas-geo-marketing.md`](tracks/overseas-geo-marketing.md)

2. **营销自动化与线索获取**：表单、CRM、邮件、社媒、报表、审批流。  
   → [`tracks/marketing-automation.md`](tracks/marketing-automation.md)

3. **内容生产与分发系统**：选题、研究、写作、发布、复盘。  
   → [`tracks/content-engine.md`](tracks/content-engine.md)

4. **AI 编码与研发效能**：AI 写码、测试、审查、排障、发布检查。  
   → [`tracks/ai-coding-workflow.md`](tracks/ai-coding-workflow.md)

## 核心入口

```text
tracks/            按业务目标找：出海增长、营销自动化、内容系统、AI 编码
categories/        按能力找：增长、内容/GEO、自动化、研究监控、研发等
app-automations/   按外部应用找：Gmail、Slack、Apollo、GSC、LinkedIn、X 等
skills/            单个 Skill 人话卡片：适合谁、解决什么、风险边界
data/              机器可读 YAML 数据源
reports/           每日 Skill 早报和研究归档
```

## 热门 Skill 卡片

- [`n8n`](skills/n8n.md)：营销 Ops / 增长流程编排
- [`Activepieces`](skills/activepieces.md)：开源自动化连接层
- [`RSSHub`](skills/rsshub.md)：公开信号订阅与竞品监控
- [`Ghost`](skills/ghost.md)：内容阵地、Newsletter、会员
- [`Plausible Analytics`](skills/plausible-analytics.md)：隐私友好的网站分析

## Skill 卡片怎么看

每张卡片只回答 6 件事：

1. 适合谁
2. 解决什么问题
3. 推荐用法
4. 不适合什么
5. 风险边界
6. 来源 / License / 验证状态

## 收录原则

只收录公开、可验证、能落地的 Skill / Agent / Workflow。  
不收录需要泄露密钥、Cookie、客户数据、私有仓库，或明显用于骚扰、刷量、绕过平台限制、数据窃取的方案。

## 给维护者

- 原 README 已备份到 [`docs/legacy-readme-before-route-navigation.md`](docs/legacy-readme-before-route-navigation.md)
- 重构说明见 [`docs/repo-structure-redesign.md`](docs/repo-structure-redesign.md)
- 结构化数据见 [`data/skills.yaml`](data/skills.yaml)
- 分类说明保留在 [`taxonomy.md`](taxonomy.md)
