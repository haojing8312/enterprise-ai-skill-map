# 2026-06-02｜Skill 验证与评分

评分：ranking/growth 30 + practical usefulness 30 + reproducibility 15 + safety 15 + communication 10。低于 70 不进早报；安全问题未解决一律 blocked。

## Firecrawl｜87 分

- URL：https://github.com/firecrawl/firecrawl
- License：AGPL-3.0
- 状态：verified_public；风险：medium-high
- 用途：把公开网页和搜索结果变成 LLM 更好读的 Markdown/结构化数据，适合做 GEO/SEO 研究、竞品页面整理和内容差距分析。
- 证据：公开 GitHub 仓库；README 展示 Search、Scrape、Crawl/Interact/Agent 等能力；主许可证 AGPL-3.0。; 2026-06-02 raw README/LICENSE 已抽检；研究分 87。
- 安全边界：网页抓取需遵守 robots.txt、网站 ToS、隐私政策和当地法规；AGPL-3.0 对网络服务与衍生部署有强 copyleft 义务；大规模抓取可能触发封禁、法律或品牌风险
- 评分：ranking/growth 29 / usefulness 27 / reproducibility 13 / safety 9 / communication 9 / total 87

## Postiz｜85 分

- URL：https://github.com/gitroomhq/postiz-app
- License：AGPL-3.0
- 状态：verified_public；风险：medium
- 用途：开源/自托管的社媒排期和内容日历工具，适合把 AI 草稿接到人工审核后的发布队列里。
- 证据：公开 GitHub 仓库；README/仓库定位为 agentic social media scheduling tool；许可证 AGPL-3.0。; 公开 HN / GitHub Search 信号显示开发者传播明显；2026-06-02 研究分 85。
- 安全边界：社媒平台 API/ToS 经常变化，自动化发布要控制频率和权限；AGPL-3.0 对网络部署和衍生服务有披露义务；内容合规、品牌安全、版权与虚假宣传需人工审核
- 评分：ranking/growth 27 / usefulness 26 / reproducibility 13 / safety 10 / communication 9 / total 85

## Twenty｜84 分

- URL：https://github.com/twentyhq/twenty
- License：GPL with Enterprise-marked files / commercial-license exceptions
- 状态：verified_public；风险：medium
- 用途：开源 CRM 候选，适合把海外线索、客户资料和跟进记录放进可控系统里，再给 AI 销售助手提供结构化上下文。
- 证据：公开 GitHub 仓库；README 标题为 The #1 Open-Source CRM；License 提到 GPL 主体与 Enterprise 标记文件。; 2026-06-02 raw README/LICENSE 已抽检；研究分 84。
- 安全边界：CRM 涉及联系人、公司、沟通记录等 PII/商业敏感数据，需权限、加密、备份和保留策略；LICENSE 提示部分 Enterprise 标记文件不在 GPL 类许可内；自托管需要数据库、备份、升级和安全运维
- 评分：ranking/growth 27 / usefulness 27 / reproducibility 12 / safety 10 / communication 8 / total 84

## Mautic｜82 分

- URL：https://github.com/mautic/mautic
- License：GPL-3.0-or-later
- 状态：verified_public；风险：medium
- 用途：成熟的开源营销自动化软件，适合邮件培育、线索评分、活动流程和自托管 MarTech 栈。
- 证据：公开 GitHub 仓库；README 写明 Open Source Marketing Automation Software；许可证 GPL-3.0-or-later。; 2026-06-02 raw README/LICENSE 已抽检；研究分 82。
- 安全边界：邮件营销必须遵守同意、退订、发件人身份、GDPR/CAN-SPAM/当地隐私法规；README 提醒 GitHub 源码更适合开发/测试，生产建议 Composer 或打包版本；营销数据涉及 PII，需要权限、审计和数据保留策略
- 评分：ranking/growth 26 / usefulness 27 / reproducibility 10 / safety 11 / communication 8 / total 82

## GrowthBook｜83 分

- URL：https://github.com/growthbook/growthbook
- License：MIT + GrowthBook Enterprise License for marked portions
- 状态：verified_public；风险：medium
- 用途：把增长假设放进可跟踪的实验系统里：Feature Flag、A/B 测试和结果分析适合用来验证落地页、功能和转化路径。
- 证据：公开 GitHub 仓库；README 写 Open Source Feature Flags, Experimentation, and Product Analytics；LICENSE 含 Enterprise 目录说明。; GitHub Search/HN 显示增长实验方向公开传播；2026-06-02 评分 83。
- 安全边界：实验需要样本量、统计口径和伦理边界，不能把结果当绝对真相；涉及用户行为数据时需隐私告知、权限和保留策略；部分目录采用 GrowthBook Enterprise License，商用集成需审查
- 评分：ranking/growth 26 / usefulness 27 / reproducibility 12 / safety 10 / communication 8 / total 83

## Watchlist / blocked

- n8n：已在 2026-06-01 入库；本轮可在策略里作为“增长自动化底座”参照，不重复新增。
- Marketing Skills for AI Agents / AI Marketing Skills：传播信号强，但需要逐项审 outbound、ads、lead-gen 模块后再进正式早报。
- OpenOutreach / auto-like / view-generator bot：blocked，涉及平台规避、骚扰式外联或刷量风险。
