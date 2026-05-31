# 2026-06-01 营销 / 出海增长 Skill 归档草稿

任务：T5 归档草稿：营销 Skill 早报知识库沉淀 2026-06-01
负责人：@publisher-analytics-agent
上游输入：`reports/daily-skill-briefings/2026-06-01-marketing-skill-verification.md`、`reports/daily-skill-briefings/2026-06-01-marketing-skill-copy.md`、`reports/daily-skill-briefings/2026-06-01-marketing-skill-longlist.md`
状态：draft / not published

## 结论

本次只把公开、可复核、且安全边界清晰的 5 个对象沉淀进归档草稿；watchlist 和模块级 blocked 内容不进入正式推荐入口。

推荐对象：n8n、Activepieces、Plausible Analytics、Ghost、RSSHub。

## 归档摘要

- T2 已完成公开证据验证，5 个入选项均超过 70 分。
- T3 已完成去 AI 味与人话改写，适合直接做早报文案底稿。
- 本稿只做 repo 候选归档，不做对外正式发布；外部发布仍待郝敬确认。

## 推荐对象一览

| Skill | 推荐场景 | 安全边界 | 验证状态 | Source |
|---|---|---|---|---|
| n8n | 表单 → CRM → 邮件 → 报表链路，营销 Ops 编排 | 对外发送、分群规则、触发条件要人工抽检，不能做骚扰式外联 | verified_public | https://github.com/n8n-io/n8n |
| Activepieces | AI 助手与 SaaS 工具连接层，保留审批节点 | 客户名单、发布流、审批流要有人盯，别写成“自动获客机器” | verified_public | https://github.com/activepieces/activepieces |
| Plausible Analytics | 内容、落地页、newsletter 访问与转化复盘 | 事件口径、权限、归因解释要人工定，读数只作辅助判断 | verified_public | https://github.com/plausible/analytics |
| Ghost | 内容发布、订阅、newsletter、会员一体化 | 标题、摘要、CTA、价格页要编辑复核，AI 草稿不能直接发 | verified_public | https://github.com/TryGhost/Ghost |
| RSSHub | 公开情报雷达、竞品动态、选题信号聚合 | 只看公开/授权/可复核来源，不碰私域、登录后页面、未授权数据 | verified_public | https://github.com/DIYgod/RSSHub |

## 适合进 repo 的候选草稿写法

- n8n：写成“营销自动化连接层”样本，重点放在合规编排，而不是自动外联。
- Activepieces：写成“带审批的 AI 自动化连接层”，强调 Human in the Loop。
- Plausible Analytics：写成“隐私优先的增长分析底座”，强调复盘而不是自动决策。
- Ghost：写成“内容资产 + 订阅转化一体化”样本，强调编辑审核。
- RSSHub：写成“内容情报雷达”样本，强调公开信号聚合与二次核验。

## 模块级 blocked 提醒（仅作边界，不进正式推荐）

以下内容即使来自 watchlist/可用仓库，也不建议进入早报推荐动作：

- AI Marketing Skills 的 `outbound-engine`、`sales-pipeline` 中任何未经 consent 校验的自动外联动作
- GTM Agents 中 prospecting / sales sequence / ABM automation 里可能触发冷触达、批量个性化骚扰的流程
- 一切把抓取、群发、自动评论、规避平台限制包装成“增长”的模块

## watchlist 仅保留观察位

- AI Marketing Skills — 71
- GTM Agents — 62
- Owkus Content Brief Generator — 58

这些对象不进入本次正式推荐入口；如后续要入库，需补齐边界说明或重新验证。

## data/skills.yaml 建议片段

以下仅是建议片段，尚未写入 `data/skills.yaml`。
字段只保留本轮最关键的：industries / role_groups / scenarios / source_url / risk_level / verification_status。

```yaml
- id: n8n
  industries: [software-internet, consulting-training, content-media]
  role_groups: [operations-automation, workflow-architecture, content-marketing]
  scenarios: [marketing-content, operations-admin]
  source_url: https://github.com/n8n-io/n8n
  risk_level: medium
  verification_status: verified_public

- id: activepieces
  industries: [software-internet, consulting-training, content-media]
  role_groups: [operations-automation, workflow-architecture, digital-employee-designer]
  scenarios: [marketing-content, operations-admin]
  source_url: https://github.com/activepieces/activepieces
  risk_level: medium
  verification_status: verified_public

- id: plausible-analytics
  industries: [software-internet, content-media]
  role_groups: [content-marketing, strategy-research, knowledge-ops]
  scenarios: [marketing-content, operations-admin]
  source_url: https://github.com/plausible/analytics
  risk_level: medium
  verification_status: verified_public

- id: ghost
  industries: [content-media, consulting-training, software-internet]
  role_groups: [content-marketing, knowledge-ops, product-manager]
  scenarios: [marketing-content, operations-admin]
  source_url: https://github.com/TryGhost/Ghost
  risk_level: low
  verification_status: verified_public

- id: rsshub
  industries: [content-media, software-internet, consulting-training]
  role_groups: [content-research, strategy-research, content-marketing]
  scenarios: [marketing-content, operations-admin]
  source_url: https://github.com/DIYgod/RSSHub
  risk_level: medium
  verification_status: verified_public
```

## 归档状态

- 可直接复用为日报底稿：是
- 可直接转成对外正式发布：否
- 是否需要郝敬最终确认：是
