# 出海公司：GEO / SEO / 内容增长 Skill 路线

适合：B2B SaaS、独立站、工具型产品、AI 产品、跨境服务商、海外内容团队。

## 你可能要解决的问题

1. 持续监控海外行业、KOL、竞品和社区动态
2. 把公开信号转成英文 / 多语言内容选题
3. 建站、博客、Newsletter、帮助中心和内容阵地
4. 自动分发到邮件、社媒、社区或内部表格
5. 监控自然流量、搜索词、转化和内容效果

## 第一套推荐组合

| 阶段 | 推荐 Skill / 工具 | 用法 | 风险边界 |
|---|---|---|---|
| 公开信号监控 | [`RSSHub`](../skills/rsshub.md) / Crawlee | 订阅竞品博客、社区、产品更新、KOL 动态 | 只采公开来源，不碰登录后页面和私域数据 |
| 流程编排 | [`n8n`](../skills/n8n.md) / [`Activepieces`](../skills/activepieces.md) | 把 RSS、表格、邮件、飞书/Slack、CRM 串起来 | 不把 API Key / Cookie 写进公开流程 |
| 内容阵地 | [`Ghost`](../skills/ghost.md) | 博客、Newsletter、内容中心、会员 | 标题、CTA、价格和承诺信息要人工复核 |
| 数据复盘 | [`Plausible`](../skills/plausible-analytics.md) / GSC | 看页面访问、来源、关键词和转化趋势 | 不把相关性误解成因果归因 |
| 应用连接 | [`app-automations`](../app-automations/README.md) | 连接 GSC、Apollo、LinkedIn、X、Mailchimp 等 | 外联和对外发布必须有人审 |

## 一周落地路径

- **Day 1：建公开信号源**  
  用 RSSHub / Crawlee 收集 10–20 个公开来源：竞品博客、更新日志、Reddit、YouTube、X、行业 Newsletter。

- **Day 2：做选题池自动化**  
  用 n8n / Activepieces 把信号写入表格或知识库，字段至少包括：来源、标题、链接、目标关键词、适合内容角度、风险备注。

- **Day 3：建内容阵地**  
  用 Ghost 或现有 CMS 建博客 / Newsletter 草稿区，先不自动发布。

- **Day 4：接数据复盘**  
  用 Plausible / Google Search Console 看页面访问、来源、关键词和转化。

- **Day 5：人工复盘**  
  判断哪些信号源值得长期监控，哪些内容能形成系列栏目。

## 不建议一开始就做

- 全自动抓取竞品全站并改写发布
- 无审批的邮件群发或 LinkedIn 私信外联
- 用 AI 生成价格、承诺、客户案例、法律条款
- 把 GEO / SEO 当成纯关键词堆砌

## 推荐下一步

如果你只想先跑一个最小闭环：

```text
RSSHub → n8n/Activepieces → 选题表 → Ghost 草稿 → Plausible/GSC 复盘
```

更完整的组合方案见：[`playbooks/geo-marketing-stack.md`](../playbooks/geo-marketing-stack.md)
