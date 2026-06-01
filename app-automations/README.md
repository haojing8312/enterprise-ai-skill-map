# App Automations｜应用自动化目录

参考 `ComposioHQ/awesome-claude-skills` 的组织方式：

- 精选 Skill 放在 [`skills/`](../skills/)
- 大量“连接某个应用做动作”的能力单独放在这里

这样用户不用在复杂 taxonomy 里找，可以直接问：我要连哪个应用？它属于哪个业务场景？

## 按场景进入

| 场景 | 入口 | 常见应用 |
|---|---|---|
| 营销 / 销售 / 线索 | [`marketing-sales.md`](marketing-sales.md) | Apollo、HubSpot、LinkedIn、Gmail、Mailchimp、Google Search Console |
| 内容 / 社媒 / 分发 | [`content-social.md`](content-social.md) | X/Twitter、YouTube、Reddit、Instagram、Webflow、Ghost |
| 数据 / 分析 / 报表 | [`analytics-data.md`](analytics-data.md) | Plausible、GA、PostHog、BigQuery、Google Sheets |

## 使用原则

1. 先确认应用权限，再设计自动化。
2. 对外发送、群发、报价、承诺、客户信息默认人工审批。
3. API Key、Cookie、客户数据不写入公开仓库。
4. 自动化要有日志、失败提醒和人工回滚路径。
