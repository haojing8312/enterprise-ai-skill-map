# Marketing & Sales App Automations

适合：出海营销、B2B 线索获取、内容增长、销售运营。

## 推荐应用地图

| 应用 / 能力 | 适合做什么 | 风险边界 |
|---|---|---|
| Apollo | 公司搜索、联系人发现、线索补全 | 外联名单要人工复核，不做骚扰式群发 |
| LinkedIn | 公司/岗位/内容信号、社交触达 | 不绕过平台限制，不批量骚扰 |
| Google Search Console | 搜索词、页面表现、索引状态 | 需要站点权限；数据解释要人工判断 |
| Google Analytics / Plausible | 页面访问、来源、事件、转化 | 不把相关性当因果 |
| Gmail / Outlook | 邮件草稿、回复、跟进提醒 | 对外发送需人工确认 |
| Mailchimp / ConvertKit | Newsletter、订阅者、分组、活动数据 | 订阅许可和退订机制必须合规 |
| Slack / 飞书 | 内部提醒、审批、日报同步 | 不暴露客户数据和密钥 |

## 出海 GEO 营销中的典型组合

```text
Google Search Console → 关键词/页面表现
RSSHub/Crawlee → 竞品和行业公开信号
n8n/Activepieces → 写入选题池并提醒
Ghost/Webflow → 内容阵地草稿
Plausible/GA → 内容效果复盘
```

## 不建议

- 自动批量私信陌生人
- 未经许可抓取联系人
- 把邮件草稿直接自动发送
- 用 AI 生成报价、客户案例、法律条款并直接对外
