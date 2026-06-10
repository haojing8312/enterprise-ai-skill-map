# AI KOL/红人开发助理 / AI Influencer Outreach Assistant

> 面向跨境贸易公司老板和高管的岗位地图。  
> 本岗位只使用公开资料、官方 API / marketplace 或企业明确授权资料；不抓私信、非公开联系方式、客户隐私、合同、报价、佣金细节或未公开产品信息。

## 1. 适合谁

- Shopify / DTC 品牌：消费电子、美妆个护、宠物、家居、户外、母婴等品类。
- Amazon / Walmart / Etsy / TikTok Shop 卖家：需要站外测评、联盟、短视频授权和直播合作。
- 1–5 人的出海市场团队：想先低成本建立 creator 候选池。
- B2B 外贸品牌化转型团队：想从展会、询盘，逐步补上社媒内容和达人合作。

## 2. 老板痛点

很多老板第一次做红人合作，卡住的地方不是“没人可找”，而是找来一堆账号后，没人说得清：谁值得先联系，谁只是粉丝数好看，谁已经报价，样品寄到哪，素材授权有没有谈清。

最常见的现场是：运营收藏了 80 个主页，市场同事发了 20 封邮件，老板只看到一个杂乱表格。过了两周，没人知道哪些人该追、哪些人不该碰、哪些合作有披露风险。

## 3. 岗位描述

**AI KOL/红人开发助理**每天接收产品信息、目标市场、平台范围、预算边界、公开 creator 主页、公开视频、媒体包、历史合作名单和品牌禁用表达。

它不替老板谈合作，也不替法务看合同。它负责把“散在各处的红人线索”整理成可筛选、可联系、可跟进、可复盘的合作队列。

它的输出包括：

- 红人候选表：平台、链接、国家、内容主题、互动数据来源、联系路径、评分、风险备注。
- Top creator 推荐清单：A/B/C 档优先级、推荐理由、人工复核问题。
- 触达草稿：邮件、DM、follow-up，等待人工批准后再发送。
- Creator brief 草稿：内容方向、shot list、披露提醒、授权边界。
- 跟进看板：未联系、已联系、已回复、谈价中、寄样中、已发布、待复盘。
- 周报：候选数、合格数、触达数、回复率、样品成本、发布链接、学习点。

## 4. 可接手任务

1. 把产品、国家、平台和预算转成搜索关键词、hashtag、竞品词、creator 类型。
2. 从官方 API、creator marketplace、公开主页、公开视频、公开媒体包中整理 50–100 个候选。
3. 合并同一 creator 的多平台账号，补充公开链接、联系方式来源和内容主题。
4. 按品类相关、受众地区、内容质量、互动质量、商业合作适配、品牌安全风险打分。
5. 为通过初筛的人生成首封邮件、DM、2–3 轮 follow-up 草稿。
6. 为已确认合作意向的 creator 生成 brief 草稿、shot list 和披露提醒。
7. 维护报价、样品、合同、授权、发布时间和下一步动作。
8. 发布后汇总公开链接、互动数据、UTM / 优惠码线索，沉淀 creator 库。

## 5. 能力模块

| 模块 | 作用 | 可对应的公开工具 / Skill / 工作流 | 风险边界 |
|---|---|---|---|
| 红人发现与公开资料采集 | 建立候选池 | YouTube Data API、Google Custom Search JSON API、TikTok Creator Marketplace、Shopify Collabs、Crawlee | 不绕过登录、验证码、权限限制；不采集私密数据 |
| 候选人评分与风险标注 | 做匹配度、互动质量、品牌安全初筛 | ChatGPT / Claude / Gemini、Google Sheets / Airtable、Modash API docs | AI 只能辅助判断，不公开指控刷粉或欺诈 |
| 个性化触达 | 生成首封邮件、DM、follow-up | ChatGPT / Claude / Gemini、Gmail / Outlook / HubSpot、Hunter API 文档 | 不编造熟人关系；不自动群发；必须人工批准 |
| 合作 brief 与披露合规 | 生成 creator brief 和披露提醒 | FTC Influencer Disclosures、YouTube paid promotions、TikTok Branded Content Policy、Instagram branded content | 不能替代法务；地区政策需人工确认 |
| 看板与复盘 | 跟进报价、寄样、授权、发布时间和效果 | Airtable / Baserow / NocoDB、Shopify Collabs、UTM、优惠码、公开发布链接 | ROI、GMV、佣金结算以后台和财务数据为准 |

## 6. 工作机理

```text
输入
  ├─ 产品：卖点、目标用户、禁用表达、预算、样品库存
  ├─ 市场：国家、语言、平台、合作方式
  ├─ 公开线索：主页、公开视频、hashtag、媒体包、creator marketplace
  ├─ 历史资料：已合作名单、黑名单、触达模板、brief、复盘
  └─ 安全规则：不抓私信/非公开数据，不自动群发，报价合同授权人审

处理
  ├─ 生成搜索词：品类词、场景词、竞品词、creator 类型
  ├─ 建候选池：记录公开链接、粉丝量、互动、内容主题、联系路径
  ├─ 打标签：国家、语言、品类、内容风格、商业合作密度
  ├─ 评分：相关性、受众匹配、内容质量、互动质量、品牌安全
  ├─ 出草稿：首封邮件、DM、follow-up、creator brief
  └─ 更新看板：状态、下一步、寄样、报价、授权、发布时间

输出
  ├─ A/B/C 分层候选名单
  ├─ 每个候选人的推荐理由和风险备注
  ├─ 可人工审核的触达草稿
  ├─ creator brief 与披露提醒
  ├─ 合作状态看板
  └─ 第一周复盘报告

人工验收
  ├─ 老板/市场负责人确认 Top 10–15 人
  ├─ 人工批准每封外联文案
  ├─ 报价、合同、佣金、样品和素材授权人工确认
  └─ 发布内容、披露标签和复盘结论人工确认
```

## 7. 真实任务示例 / 可复制提示词

### Prompt 1：生成红人搜索策略

```text
你是一个跨境电商品牌的 AI 红人开发助理。请根据以下信息，为我生成 TikTok、Instagram、YouTube 三个平台的红人搜索策略。

产品：便携式宠物饮水杯
目标市场：美国
目标用户：经常带狗出门、露营、徒步、开车旅行的宠物主人
合作类型：寄样测评 + 联盟佣金
预算：优先找中小型 creator，单人固定费用不超过 200 美元
禁用方向：不要找只做搞笑搬运、无宠物原创内容、争议性训练方式的账号

请输出：英文关键词列表、hashtag 列表、竞品/场景搜索词、适合的 creator 类型、不适合的 creator 类型、候选人表格字段、初筛评分标准。
要求：不要编造具体达人账号；只给搜索策略和筛选方法。
```

### Prompt 2：给候选 creator 打分

```text
你是 AI Influencer Outreach Assistant。请根据我提供的公开资料，对以下 creator 做初步合作评分。不要臆测未提供的数据；如果信息不足，请写“需人工补充”。

品牌：美国市场宠物出行用品 DTC 品牌
产品：便携式宠物饮水杯
合作目标：获取 TikTok / Instagram 短视频测评和可授权素材

候选人公开资料：平台、账号链接、简介、粉丝量、最近 10 条内容主题、平均点赞、平均评论、受众地区信息、商业合作痕迹、联系方式来源。

请按品类相关性、受众市场匹配、内容质量、互动质量、商业合作适配度打分，每项 0–5 分；再标注品牌安全风险和合规风险。最后输出总分、A/B/C 推荐等级、推荐理由和必须人工复核的问题。
```

### Prompt 3：写个性化首封触达邮件

```text
你是一个跨境品牌的红人开发助理。请根据以下资料，写一封英文 KOL 合作邀请邮件。语气自然、具体、不过度夸张，不要编造我没有提供的信息。

品牌：PawTrail
产品：portable dog water bottle for walks, hiking, road trips
目标市场：US
合作方式：free sample + affiliate commission；如果 creator 有 rate card，也欢迎回复报价
Creator 名字：Jessica
Creator 账号主题：她经常发布 golden retriever hiking、dog park routine、pet travel tips
最近一条相关内容：a weekend hiking vlog with her dog Max
我们喜欢她的点：真实户外场景、狗狗出镜自然、评论区有用户问出行装备
必须包含：说明为什么找她、产品适合她内容的原因、是否愿意了解合作、不承诺夸张收益、不要求隐藏赞助关系、结尾礼貌。

输出：3 个邮件标题、120–180 词正文、2 句 DM 简短版。
```

### Prompt 4：生成 creator brief

```text
请为一个宠物用品品牌生成 creator brief。这个 brief 会发给已经确认合作的美国 TikTok/Instagram creator。

产品：便携式宠物饮水杯
核心卖点：one-hand operation、leak-proof design、fits car cup holder、适合 walking / hiking / dog park / road trips
内容形式：30–45 秒短视频
必须出现：狗狗真实使用场景、如何装水/出水/回收未喝完的水、至少一个户外场景
不能出现：不能说 veterinarian approved，除非品牌提供证明；不能承诺治疗或健康效果；不能攻击竞品品牌
披露要求：清楚标注 paid partnership / ad / gifted product，按平台规则执行
交付：1 条 TikTok 或 Reel；允许品牌 30 天内 organic repost，付费投放需另谈

请输出 creator brief、shot list、key talking points、Do & Don’t、披露提醒、人工确认项。
```

## 8. 人类主管验收

- 每个候选人必须有公开来源 URL；信息不足写“需人工补充”。
- Top 20–30 必须有推荐理由、风险备注和 A/B/C 分层。
- 每封外联文案至少包含一个真实、可核验的个性化点。
- 赞助、寄样、佣金合作必须提醒 disclosure。
- 触达前必须确认真实品牌身份、联系方式和停止联系机制。
- 老板每天看：合格候选数、Top 10 待确认、触达草稿可用率、回复状态、样品状态、授权/披露风险。

## 9. 不能自动化的事

- 不能自动决定签约、付款、佣金、报价、素材授权、独家条款。
- 不能绕过平台限制、登录权限、验证码或 robots / ToS。
- 不能自动采集未公开个人联系方式，尤其是私人邮箱、手机号、地址。
- 不能冒充真人关系，不能编造“长期关注你”或“朋友推荐”。
- 不能替代法务判断；FTC、欧盟、英国和平台规则需要人工确认。
- 不能生成虚假背书或要求 creator 做未体验产品的正面评价。
- 不能自动群发骚扰信息。

## 10. 第一周试点方案

- **Day 1**：确认产品、目标市场、平台、合作方式、预算、禁用条件，建立候选表字段和评分标准。
- **Day 2**：生成关键词、hashtag、竞品词、场景词，记录 50–100 个公开候选。
- **Day 3**：清洗、去重、补公开链接，AI 辅助评分，人工抽查，筛出 Top 20–30。
- **Day 4**：老板/市场负责人确认 Top 10–15，生成个性化邮件/DM/follow-up，人工审核语气与合规。
- **Day 5**：小批量触达，只发给人工批准对象，记录发送渠道、时间和状态。
- **Day 6**：汇总回复，给感兴趣 creator 生成 brief 草案，确认样品、预算、授权范围。
- **Day 7**：复盘候选数、合格率、触达数、回复率，更新关键词库、评分标准和模板。

## 11. 相关 Skill / 工具栈

| 工具 / repo / workflow | 公开链接 | 适合谁 | 风险边界 |
|---|---|---|---|
| YouTube Data API | https://developers.google.com/youtube/v3/docs/search/list | 做 YouTube creator 公开搜索和频道初筛 | 遵守 API quota 和平台条款 |
| Google Custom Search JSON API | https://developers.google.com/custom-search/v1/overview | 搜公开 creator 主页、博客、媒体包 | 遵守搜索 API 和目标站点规则 |
| TikTok Creator Marketplace | https://creatormarketplace.tiktok.com/ | 找 TikTok creator 的品牌团队 | 不绕过平台规则 |
| Shopify Collabs | https://www.shopify.com/collabs | Shopify 品牌做 creator / affiliate 合作 | 条款、佣金、授权人工确认 |
| Crawlee | https://github.com/apify/crawlee | 构建可控的公开网页采集流程 | 技术可行不等于合规可行 |
| Modash API docs | https://docs.modash.io/ | 有预算做红人搜索和数据 API 的团队 | 数据评分不等于最终合作决策 |
| FTC Influencer Disclosures | https://www.ftc.gov/business-guidance/resources/disclosures-101-social-media-influencers | 美国市场赞助/寄样/佣金披露参考 | 不能替代律师意见 |
