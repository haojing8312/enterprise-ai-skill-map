# Skill 仓库结构重设计方案

> 目标：把 `enterprise-ai-skill-map` 从“企业分类体系仓库”改成“业务人员能快速按索引找到可用 Skill 的目录型仓库”。
>
> 典型用户问题：我是一个出海公司，要做 GEO / SEO / 内容增长，应该从哪里开始？

## 1. 参考的高赞 Skill / Agent 聚合仓库

| 仓库 | Star 信号 | 结构特点 | 可借鉴点 |
|---|---:|---|---|
| `ComposioHQ/awesome-claude-skills` | 6w+ | README 顶部强 CTA + Quickstart；正文是精选分类清单；仓库里同时保留 28 个顶层 Skill 和 800+ `composio-skills/*-automation` 应用自动化 Skill | 最值得参考：**首页像 Awesome List，目录像 Skill Marketplace，应用自动化单独成大类**；不把所有条目塞进 taxonomy |
| `wshobson/agents` | 3w+ | README 先给 Quick start，再给插件市场、分类、文档地图；真实内容放在 `plugins/` 下 | 首页只保留入口和安装/使用路径；复杂说明放 docs |
| `VoltAgent/awesome-claude-code-subagents` | 2w+ | `categories/01-core-development` 这种编号目录；README 直接列分类和条目 | 分类编号清晰，读者不需要理解完整 taxonomy |
| `contains-studio/agents` | 1w+ | 按部门分：engineering / marketing / design / product / operations | 用“团队/岗位语言”组织，比抽象技术标签更好找 |
| `abubakarsiddik31/claude-skills-collection` | 600+ | Overview → Popular Picks → Categories → Getting Started → Template | 首页要有“热门推荐”和“怎么用”，不要只有文件树 |
| `helloianneo/awesome-claude-code-skills` | 100+ | 中文 README，Top 10 + 场景分类 + 怎么选 Skill | 中文用户友好；用“必装/场景/选择指南”降低门槛 |

结论：高赞仓库不是 taxonomy 最完整，而是 **首页入口简单、分类稳定、热门条目靠前、每个目录都能直接回答“我该点哪里”**。Composio 的额外启发是：当 Skill 数量很大时，不要试图让用户浏览全量列表，而要把“精选路线 / 能力分类 / 应用自动化目录 / 单个 Skill 卡片”分层。

## 2. 当前仓库的问题

当前结构：

```text
industries/  # 行业
roles/       # 岗位
scenarios/   # 场景
data/        # 结构化数据
reports/     # 每日早报/研究报告
workflows/   # 工作流样板
```

主要问题：

1. **入口太多**：行业、岗位、场景并列，用户不知道先点哪个。
2. **目录像内部咨询 taxonomy**：适合我们做沉淀，不适合外部用户快速找答案。
3. **高频需求没有独立路径**：例如“出海公司 / GEO 营销”要跨 `content-media`、`retail-ecommerce`、`content-marketing`、`sales-growth` 才能拼出来。
4. **Skill 卡片隐藏在 YAML 里**：人可以读 README，但很难直接浏览单个 Skill 的使用边界。
5. **日报和长期索引混在一起**：`reports/` 有价值，但不应该干扰主导航。

## 3. 新结构原则

### 一句话原则

把公开仓库设计成：

```text
先按“我是谁/我要做什么”进入，再看到“推荐路线”，最后才看单个 Skill。
```

### 保留但降级的东西

- `data/skills.yaml`：继续作为机器可读数据源。
- 原来的 industries / roles / scenarios：不再作为首页主入口，可迁移到 `archive/legacy-taxonomy/` 或保留为辅助索引。
- `reports/`：保留每日早报归档，但从 README 主导航降级。

## 4. 推荐的新目录结构

```text
enterprise-ai-skill-map/
├── README.md                         # 首页：5 秒找到入口
├── START_HERE.md                     # 新手选择指南：按业务目标选路线
├── tracks/                           # 最重要：按业务目标组织的“路线图”
│   ├── overseas-geo-marketing.md     # 出海公司：GEO / SEO / 内容增长
│   ├── overseas-social-growth.md     # 出海社媒增长 / KOL / 社群
│   ├── b2b-lead-generation.md        # B2B 线索获取
│   ├── content-engine.md             # 内容生产与分发
│   ├── marketing-automation.md       # 营销自动化
│   ├── customer-support.md           # 客服 / FAQ / 工单
│   ├── internal-knowledge-base.md    # 企业知识库
│   └── ai-coding-workflow.md         # AI 编码与研发效能
├── categories/                       # 二级：稳定能力分类
│   ├── 01-marketing-growth.md
│   ├── 02-content-seo-geo.md
│   ├── 03-automation-integration.md
│   ├── 04-research-monitoring.md
│   ├── 05-customer-success.md
│   ├── 06-knowledge-docs.md
│   ├── 07-ai-coding-devtools.md
│   ├── 08-ai-infra-model-ops.md
│   └── 09-governance-security.md
├── skills/                           # 单个精选 Skill 卡片，人可读；类似 Composio 顶层精选 Skill
│   ├── n8n.md
│   ├── activepieces.md
│   ├── rsshub.md
│   ├── ghost.md
│   ├── plausible-analytics.md
│   └── ...
├── app-automations/                  # 应用自动化目录；借鉴 Composio 的 composio-skills/*-automation
│   ├── README.md                     # 按应用/业务场景列 Gmail、Slack、Apollo、GSC、LinkedIn 等连接能力
│   ├── marketing-sales.md            # Apollo、HubSpot、LinkedIn、Google Search Console、Mailchimp...
│   ├── content-social.md             # X/Twitter、YouTube、Reddit、Instagram、Webflow、Ghost...
│   └── analytics-data.md             # GA、Plausible、PostHog、BigQuery、Sheets...
├── indexes/                          # 辅助索引，不放首页太靠前
│   ├── by-business.md                # 按业务类型：出海公司/B2B SaaS/电商/内容团队...
│   ├── by-role.md                    # 按负责人：市场/运营/研发/客服/老板...
│   ├── by-risk.md                    # 按风险等级：low/medium/high
│   └── by-source.md                  # 按来源：GitHub repo/MCP/Claude Skill/Agent...
├── playbooks/                        # 可复制的组合方案
│   ├── geo-marketing-stack.md        # GEO 营销组合方案
│   ├── ai-content-monitoring-stack.md
│   └── lead-gen-automation-stack.md
├── data/                             # 机器可读，继续保留
│   ├── skills.yaml
│   ├── classification.yaml
│   └── sources.yaml
├── reports/                          # 每日早报和调研归档，降级为历史记录
├── templates/
└── archive/legacy-taxonomy/           # 原 industries/roles/scenarios 可迁入
```

## 5. 首页应该怎么改

README 不再解释复杂分类，改成 4 个入口：

```markdown
# Enterprise AI Skill Map

帮企业和超级个体快速找到可落地的 AI Skill / Agent / 自动化工作流。

## 我想快速开始

- 我是出海公司，要做 GEO / SEO / 内容增长 → tracks/overseas-geo-marketing.md
- 我要搭内容生产和分发系统 → tracks/content-engine.md
- 我要做营销自动化和线索获取 → tracks/marketing-automation.md
- 我要连接 Gmail / Slack / Apollo / Google Search Console 等应用 → app-automations/README.md
- 我要给研发团队上 AI 编码流程 → tracks/ai-coding-workflow.md
- 我只想看最推荐的 Top Skills → START_HERE.md

## 热门路线

1. 出海 GEO 营销路线
2. 内容增长路线
3. 营销自动化路线
4. AI 编码路线
5. 企业知识库路线

## Skill 卡片怎么看

每个 Skill 只回答 6 件事：
- 适合谁
- 解决什么问题
- 推荐用法
- 不适合什么
- 风险边界
- 链接 / License / 验证状态
```

## 6. 示例路径：出海公司做 GEO 营销

用户从 README 点击：

```text
README → tracks/overseas-geo-marketing.md → playbooks/geo-marketing-stack.md → skills/*.md
```

`tracks/overseas-geo-marketing.md` 示例结构：

```markdown
# 出海公司：GEO / SEO / 内容增长 Skill 路线

适合：B2B SaaS、独立站、工具型产品、AI 产品、跨境服务商。

## 你可能要解决的问题

1. 持续监控海外行业/KOL/竞品内容
2. 把信号转成英文/多语言内容选题
3. 建站、博客、Newsletter、帮助中心
4. 自动分发到社媒、邮件、社区
5. 监控自然流量、转化和内容效果

## 推荐 Skill 组合

| 阶段 | 推荐 Skill | 用法 | 风险 |
|---|---|---|---|
| 监控 | RSSHub / Crawlee | 监控竞品、博客、社区、RSS | 注意来源权限和抓取频率 |
| 自动化 | n8n / Activepieces | 把 RSS、表格、邮件、社媒串成流程 | 不要把密钥写进公开流程 |
| 内容阵地 | Ghost | 搭博客、Newsletter、内容中心 | 对外发布需人工复核 |
| 数据分析 | Plausible | 看页面、来源、转化趋势 | 不替代完整归因系统 |
| 浏览器任务 | Browser-use / Playwright MCP | 巡检网页、采集公开页面结构 | 不处理账号 Cookie 和私密后台 |

## 第一周建议

- Day 1：用 RSSHub 建 10 个公开信号源
- Day 2：用 n8n / Activepieces 做每日候选选题流
- Day 3：用 Ghost 建内容落地页/博客草稿
- Day 4：用 Plausible 看基础访问数据
- Day 5：复盘哪些内容信号值得长期监控
```

## 7. 单个 Skill 卡片模板

`skills/n8n.md` 示例：

```markdown
# n8n

一句话：开源自动化工作流工具，适合把内容监控、表格、邮件、社媒、CRM 等动作串起来。

## 适合谁
- 出海市场/增长负责人
- 内容运营
- 营销自动化负责人

## 解决什么问题
- 每天自动收集公开内容信号
- 把候选选题写入表格或知识库
- 触发邮件、Slack/飞书、社媒草稿等流程

## 推荐场景
- GEO / SEO 内容监控
- Newsletter 选题池
- 线索收集和初筛

## 不适合
- 没有权限设计就直接接生产账号
- 批量骚扰、刷量、绕过平台规则

## 风险边界
- API Key / Cookie 不得写入公开仓库
- 对外发送消息必须有人审

## 来源
- GitHub: https://github.com/n8n-io/n8n
- License: Sustainable Use License / Enterprise License 相关条款需复核
- 状态：verified_public
```

## 8. 数据字段调整建议

继续保留 `data/skills.yaml`，但新增更适合导航的字段：

```yaml
- id: n8n
  name: n8n-io/n8n
  url: https://github.com/n8n-io/n8n
  status: verified_public
  primary_category: automation-integration
  business_tags:
    - overseas-company
    - b2b-saas
    - ecommerce
  goal_tags:
    - geo-marketing
    - seo-content
    - lead-generation
    - workflow-automation
  role_tags:
    - marketing
    - growth
    - operations
  recommended_tracks:
    - overseas-geo-marketing
    - marketing-automation
  risk_level: medium
  card_summary: ...
```

这样 README 和 track 页面可以自动生成，不再靠人工维护多套目录。

## 9. 迁移步骤

### Phase 1：不破坏现有仓库，先加新入口

1. 新增 `START_HERE.md`。
2. 新增 `tracks/`，先做 4 条高频路线：
   - `overseas-geo-marketing.md`
   - `content-engine.md`
   - `marketing-automation.md`
   - `ai-coding-workflow.md`
3. 新增 `categories/`，把现有 Skill 归入 8–9 个稳定能力分类。
4. 新增 `skills/`，先为每日 Skill 早报入库的条目自动生成人可读卡片。
5. 新增 `app-automations/`，借鉴 Composio，把“连接外部应用做动作”的 Skill 单独放一层；首批只做出海营销常用应用：Google Search Console、Google Analytics/Plausible、Apollo、LinkedIn、X/Twitter、YouTube、Reddit、Mailchimp/ConvertKit、Gmail、Slack/飞书。
6. README 改成“5 秒导航页”。

### Phase 2：把旧 taxonomy 降级

1. `industries/roles/scenarios` 暂时保留，但 README 不再主推。
2. 等新入口稳定后，迁到 `archive/legacy-taxonomy/`。
3. `taxonomy.md` 改名为 `docs/data-taxonomy.md`，只给维护者看。

### Phase 3：自动化生成

1. 每日 Skill 早报入库时，新增/更新 `skills/{id}.md`。
2. 根据 `recommended_tracks` 自动更新 `tracks/*.md`。
3. 根据 `primary_category` 自动更新 `categories/*.md`。
4. YAML 校验 + 链接校验 + 去重后再 commit。

## 10. 验收标准

这次重构是否成功，看 5 个问题：

1. 用户打开 README，是否 5 秒内知道该点哪里？
2. “出海公司做 GEO 营销”是否能一跳进入对应路线？
3. 每个 Skill 是否有人话说明，而不是只能读 YAML？
4. 日报归档是否不干扰主导航？
5. 新 Skill 入库后，是否能自动出现在对应路线和分类页？

## 11. 推荐先落地的最小版本

先不要大改全仓库。建议下一步只做：

```text
README.md 重写
START_HERE.md 新增
tracks/overseas-geo-marketing.md 新增
tracks/marketing-automation.md 新增
categories/01-marketing-growth.md 新增
app-automations/README.md 新增
app-automations/marketing-sales.md 新增
skills/n8n.md / activepieces.md / rsshub.md / ghost.md / plausible-analytics.md 新增
```

这样可以立刻满足“出海公司做 GEO 营销快速找到 Skill”的需求，同时不破坏现有数据。