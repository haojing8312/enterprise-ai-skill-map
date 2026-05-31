# 2026-06-01 营销 / 出海增长 Skill 验证筛选

任务：T2 验证筛选：营销增长 Skill 5–8 个候选
负责人：@research-writer
上游长名单：`reports/daily-skill-briefings/2026-06-01-marketing-skill-longlist.md`

## 结论快照

本轮验证 8 个候选，建议入选早报 5 个：

1. n8n — 91
2. Activepieces — 83
3. Plausible Analytics — 82
4. Ghost — 81
5. RSSHub — 75

watchlist：
- AI Marketing Skills — 71
- GTM Agents — 62
- Owkus Content Brief Generator — 58

说明：
- 70 分以下不进早报。
- 即使总分超过 70，若包含明显越界模块，也只建议“限模块使用”，不建议整体无差别推广。
- 本轮未新增“整仓 blocked”对象；高风险群发/采集/黑帽类项目继续沿用 T1 直接排除结论。

## 验证方法

证据源以公开、可复核材料为主：
- GitHub 仓库主页公开信息（stars、项目描述）
- README 原文
- `commits/<branch>.atom` 最近提交时间
- LICENSE 文件首段或仓库内 license 声明

评分模型（100 分）：
- 排名 / 增长：30
- 实用性：30
- 可复现：15
- 安全：15
- 传播价值：10

本轮 GitHub API 出现匿名限流，后续改用公开 HTML + raw README + commits atom 交叉验证，不影响结论可复核性。

## 建议入选对象（5）

| 排名 | 候选 | 分数 | 入选理由 | 主要边界 |
|---|---|---:|---|---|
| 1 | n8n | 91 | 增长自动化底座最成熟；400+ integrations、900+ workflow templates，适合表单→CRM→邮件→报表链路 | fair-code / 非纯 OSI；外部二次分发前需法务复核；禁止把它包装成自动骚扰引擎 |
| 2 | Activepieces | 83 | 更偏“可控 AI 自动化 + MCP 连接层”；README 明确有 Human in the Loop / approval | 混合许可；优先内部运营与连接层，不直接外放“自治式营销代理”叙事 |
| 3 | Plausible Analytics | 82 | 隐私优先、cookie-free、GDPR/CCPA/PECR 友好，适合内容增长与落地页复盘 | AGPL 边界要写清；事件埋点与权限管理需人工治理 |
| 4 | Ghost | 81 | 内容发布、Newsletter、membership 一体化，和 OPC 内容增长系统贴合度高 | 需要编辑审核，不能把 AI 草稿直接当成发布成品 |
| 5 | RSSHub | 75 | 适合竞品监控、行业情报、内容选题雷达，是内容增长前置情报层 | 仅限公开路由 / 公开来源；不要触达私有、登录后、未授权数据 |

---

### 1) n8n

- 仓库：`n8n-io/n8n`
- 公开信号：190,471★；最近提交 2026-05-31
- README 关键信息：
  - “Secure Workflow Automation for Technical Teams”
  - “400+ integrations”
  - “900+ ready-to-use templates”
- License / 使用边界：`LICENSE.md` 显示 fair-code / 非纯开源边界，且部分目录不按同一许可开放。
- 安装 / 使用路径：README 给出 `npx` 快速启动；也支持 Docker 部署。
- 企业营销场景价值：
  - 表单 / CRM / 邮件 / 社媒 / 分析报表串联
  - 用于 lead routing、内容分发、周报自动化、归因数据搬运
- 人工审核点：
  - 所有 outbound / 邮件 / 私信动作都要先过 consent / 频控 / 黑名单
  - 自动生成的分群规则、评分阈值、发送文案要人工抽检
- 风险边界：
  - 只推荐“合规自动化编排”，不推荐大规模冷启动骚扰、绕平台风控、批量抓取个人隐私数据
- 评分拆解：排名增长 29 / 实用性 28 / 可复现 12 / 安全 13 / 传播价值 9 = 91

### 2) Activepieces

- 仓库：`activepieces/activepieces`
- 公开信号：22,492★；最近提交 2026-05-31
- README 关键信息：
  - “An open source replacement for Zapier”
  - “Largest open source MCP toolkit”
  - 明确写有 “Human in the Loop” 和 “require approval”
- License / 使用边界：根 LICENSE 为混合许可，ee 目录单独受限；适合内部采用，不宜直接模糊成“完全自由复用”。
- 安装 / 使用路径：README 指向官方 install docs；生态基于 npm / TypeScript pieces。
- 企业营销场景价值：
  - 很适合做“AI 员工 + SaaS 工具”的连接层
  - 可把 RSS / 表单 / Google Sheets / OpenAI / Discord 等节点串成营销运营流程
- 人工审核点：
  - 涉及客户名单、审批流、发布流时，优先启用 approval / human input interface
  - 分发前要校验文案、受众、触发条件是否误伤
- 风险边界：
  - 推荐作为内部流程编排层，不推荐直接承诺“无人值守增长代理”
- 评分拆解：排名增长 24 / 实用性 26 / 可复现 12 / 安全 13 / 传播价值 8 = 83

### 3) Plausible Analytics

- 仓库：`plausible/analytics`
- 公开信号：26,649★；最近提交 2026-05-28
- README 关键信息：
  - “privacy-first web analytics”
  - “cookie-free alternative to Google Analytics”
  - 明确标注 GDPR、CCPA、PECR compliant
- License / 使用边界：核心 CE 为 AGPLv3；tracker 另有 MIT 许可，使用时需区分。
- 安装 / 使用路径：可直接用 managed cloud，也可自托管 CE。
- 企业营销场景价值：
  - 适合内容团队做落地页、newsletter、渠道流量与转化复盘
  - 适合对“隐私合规”敏感的出海项目
- 人工审核点：
  - 事件设计、归因口径、共享权限需要人工定义
  - 读数只能辅助决策，不能替代对渠道质量的人工判断
- 风险边界：
  - 不适合被包装成“全自动增长决策器”；更适合做分析层
- 评分拆解：排名增长 22 / 实用性 24 / 可复现 13 / 安全 15 / 传播价值 8 = 82

### 4) Ghost

- 仓库：`TryGhost/Ghost`
- 公开信号：53,747★；最近提交 2026-05-29
- README 关键信息：
  - “modern publishing, memberships, subscriptions and newsletters”
- License / 使用边界：MIT。
- 安装 / 使用路径：README 提供 `npm install ghost-cli -g` 与 `ghost install local` 快速启动路径。
- 企业营销场景价值：
  - 适合把内容生产、订阅转化、newsletter、会员体系放进同一内容资产平台
  - 对“个人 IP + 内容产品化”路线尤其贴合
- 人工审核点：
  - 标题、摘要、CTA、会员权益、价格页信息必须人工校对
  - AI 草稿需经过编辑审核再发布
- 风险边界：
  - 平台本身低风险，但内容真实性、版权、医学/财务等高风险领域仍要人工把关
- 评分拆解：排名增长 22 / 实用性 25 / 可复现 12 / 安全 14 / 传播价值 8 = 81

### 5) RSSHub

- 仓库：`DIYgod/RSSHub`
- 公开信号：44,393★；最近提交 2026-05-30
- README 关键信息：
  - “Everything is RSSible”
  - “world's largest RSS network, consisting of over 5,000 global instances”
  - README 直接给出 Quick Start / Deployment 文档
- License / 使用边界：AGPL-3.0。
- 安装 / 使用路径：文档给出 Quick Start 与部署路径，也有 Docker / npm 分发信号。
- 企业营销场景价值：
  - 可做竞品动态监控、行业信号聚合、选题雷达、内容情报底座
  - 很适合接到 n8n / Activepieces 前面作为触发器
- 人工审核点：
  - 路由质量、数据噪音、重复源、订阅优先级要人工治理
  - 抓到的线索要二次验证，不直接当事实发布
- 风险边界：
  - 仅使用公开、授权、可复核来源；不碰登录后页面、私域信息、未授权采集
- 评分拆解：排名增长 18 / 实用性 23 / 可复现 13 / 安全 13 / 传播价值 8 = 75

## watchlist

### 6) AI Marketing Skills — 71

- 仓库：`ericosiu/ai-marketing-skills`
- 公开信号：2,517★；最近提交 2026-05-28；MIT
- 正向价值：
  - README 结构清晰，覆盖 `growth-engine`、`content-ops`、`seo-ops`、`x-longform-post` 等，内容团队可直接借鉴工作流设计
  - 明确有 privacy / security 说明与 sanitizer 脚本
- 为什么先放 watchlist：
  - 同仓库也包含 `outbound-engine`、`sales-pipeline` 这类更敏感模块
  - 适合作为“内容工作流模板库”选读，不适合整仓打包推荐给所有团队
- 建议使用边界：
  - 可优先采用：content-ops、SEO ops、X long-form humanizer
  - 暂不推荐：冷外联、匿名访客转线索、自动化外呼/邮件序列
- 评分拆解：排名增长 17 / 实用性 22 / 可复现 14 / 安全 10 / 传播价值 8 = 71

### 7) GTM Agents — 62

- 仓库：`gtmagents/gtm-agents`
- 公开信号：259★；最近提交 2026-04-03；Apache-2.0
- 正向价值：
  - 覆盖 content marketing、social、SEO、growth experiments 等插件，营销叙事完整
  - README 也写了维护节奏与治理文档
- 为什么先放 watchlist：
  - 社区验证与维护活跃度信号仍偏弱
  - 仓库含 prospecting / sales sequence / ABM orchestration 等高敏感模块，默认推广风险较高
- 建议使用边界：
  - 仅把它当“GTM 插件地图”参考，不作为默认推荐工具包
- 评分拆解：排名增长 12 / 实用性 20 / 可复现 13 / 安全 10 / 传播价值 7 = 62

### 8) Owkus Content Brief Generator — 58

- 仓库：`owkusweb/owkus-brief-generator`
- 公开信号：0★；最近提交 2026-04-08；MIT
- 正向价值：
  - 单点场景清晰：SEO 内容 brief，输出 H2/H3、关键词变体、meta 建议
  - 零 API key、Python 本地可跑，复现门槛低
- 为什么先放 watchlist：
  - 社区信号极弱，维护可信度不足
  - 更像单功能脚本，而不是可持续复用的营销增长基础设施
- 建议使用边界：
  - 可内部试跑做 brief 初稿，但必须人工做 SERP 复核、事实核验、品牌语气校正
- 评分拆解：排名增长 8 / 实用性 18 / 可复现 14 / 安全 13 / 传播价值 5 = 58

## 模块级 blocked 提醒（不是整仓封禁，属使用边界）

以下内容即使来自 watchlist/可用仓库，也不建议进入早报“推荐动作”：

- AI Marketing Skills 的 `outbound-engine`、`sales-pipeline` 中任何未经 consent 校验的自动外联动作
- GTM Agents 中 prospecting / sales sequence / ABM automation 里可能触发冷触达、批量个性化骚扰的流程
- 一切把抓取、群发、自动评论、规避平台限制包装成“增长”的模块

## 对早报的编辑建议

如果只放 3–5 个对象，建议顺序：
1. n8n
2. Activepieces
3. Plausible Analytics
4. Ghost
5. RSSHub

推荐写法：
- 前 2 个写“营销自动化连接层”
- 中间 2 个写“内容资产与增长分析底座”
- 最后 1 个写“内容情报雷达”

这样更符合 OPC 内容作战室的真实使用路径：先拿情报，再做内容与分发，最后回收分析数据。