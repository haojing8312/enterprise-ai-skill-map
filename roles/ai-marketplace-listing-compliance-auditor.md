# AI 平台 Listing 合规巡检员 / AI Marketplace Listing Compliance Auditor

> 替跨境老板在商品上架前先看一遍：哪些词会惹麻烦，哪些图不能直接用，哪些承诺必须等人确认。

## 适合谁

- Amazon、Walmart、eBay、TikTok Shop、Shopee、Lazada、Temu 等多平台卖家。
- DTC 品牌和独立站团队，准备把商品同步到 Google Merchant Center / Meta Commerce。
- 有高风险品类的团队：儿童用品、电池、化妆品、食品接触材料、保健、宠物、安全防护、带认证声明的工业品。
- SKU 多、上新快、运营经验不均、平台警告经常压到老板桌面的团队。

## 老板痛点

爆品最怕突然被拒登、下架、广告停投。标题里用了竞品品牌词，五点里写了 `guaranteed`、`best`、`medical`，主图放了证书但后台没有材料，A+ 里写了夸大功效，包装图和详情页对不上。运营看着像小毛病，平台邮件一来，老板面对的是库存压着、广告断了、排名掉了、客服还要解释。

## 这个数字员工每天干什么

**输入：** SKU 清单、目标平台、类目、Listing 草稿、标题、五点、A+、图片文字、属性、变体、后台搜索词、平台公开政策、商品数据规范、禁限售规则、图片要求、认证材料、驳回/警告邮件。

**输出：** Listing 风险表、`PASS / REWRITE / BLOCK` 三类结果、证据截图/规则链接、建议改法、负责人、老板日报/周报。

## 可接手任务

1. Listing 草稿体检：检查标题、五点、描述、A+、图片文字、属性、变体和目标平台。
2. 高风险词扫描：标出医疗/保健功效、环保、儿童安全、食品接触、电池、认证、官方授权、极限词、竞品品牌词。
3. 图片风险检查：主图背景、文字水印、证书 logo、前后对比、儿童/医疗场景、包装图和页面描述是否冲突。
4. 属性完整性检查：品牌、GTIN、材质、尺寸、年龄段、危险品信息、能效、颜色、尺码、包装数量。
5. 多平台差异提醒：同一商品在不同平台是否需要删词、补属性、换图、拆变体、改类目。
6. 平台驳回归因：把拒登、下架、警告邮件拆成可执行整改项。
7. 规则更新后复检：平台政策或品类要求变化后，筛出受影响 SKU。
8. 改后复查：保留修改前后版本，确认 P0/P1 是否消失。

## 能力模块

| 模块 | 老板听得懂的作用 | 公开工具 / 工作流 | 风险边界 |
|---|---|---|---|
| 平台规则源 | 把平台要求变成检查项 | Amazon SP-API docs、Google Merchant Center、eBay、Meta policies | 保留原文链接和日期；AI 摘要不替代官方通知 |
| Listing 数据读取 | 拉 SKU、标题、描述、属性、图片、状态 | Amazon SP-API、Google Merchant feed/API、平台 CSV 导出 | 只读权限优先；token 不进提示词 |
| 风险分级 | 告诉老板“能上、要改、先别上” | PASS / REWRITE / BLOCK 表格 | P0/P1 必须人工确认 |
| 规则测试 | 用踩坑案例测试巡检质量 | promptfoo、OpenAI Evals、自建 eval | 样本脱敏；高风险判断抽查 |
| 页面截图证据 | 给每个风险留位置 | Playwright | 不绕登录、验证码、反爬或平台限制 |
| 巡检台账 | 管处理人、截止日、改前改后、复检 | NocoDB、Sheets、Metabase | 看板限权；不放客户 PII、账号密钥、合同报价 |

## 工作机理

```text
SKU 清单 / Listing 草稿 / 平台规则摘要 / 证书材料 / 驳回邮件
→ 读取标题、五点、A+、图片、属性、变体、类目、后台搜索词
→ 对照禁限售、品牌词、认证词、功效词、图片要求、必填字段
→ 输出 PASS / REWRITE / BLOCK + 证据位置 + 建议改法
→ 运营改低风险项，合规/老板确认 P0/P1
→ 复检改后版本，沉淀风险词表和规则清单
```

## 可复制提示词

```text
你是跨境平台 Listing 合规巡检员。请审查以下 Listing 草稿。
输出表格：平台、SKU、风险等级P0/P1/P2、问题字段、风险说明、可引用证据、建议修改、需人工确认人。
规则：不要承诺平台一定通过；证据不足时标记“需人工确认”。
目标平台：{{marketplace}}
类目：{{category}}
Listing草稿：{{title_bullets_description_attributes_images_text}}
可用证据：{{certificates_test_reports_public_specs}}
平台规则摘要：{{policy_excerpt_with_url}}
```

```text
请扫描以下商品文案中的高风险声明。
重点检查：医疗/保健功效、环保、儿童安全、食品接触、电池、认证、官方授权、极限词、竞品贬低、商标侵权。
输出：原文、风险类型、为什么有风险、是否需要证据、建议替代表述、是否建议暂停上架。
文案：{{listing_copy}}
目标国家/平台：{{country_marketplace}}
```

```text
同一商品准备同步到多个平台。请比较不同平台下 Listing 是否需要改写。
输出：平台、必须删除的内容、需补属性、图片风险、证据要求、人工确认项。
商品资料：{{product_spec}}
当前Amazon文案：{{amazon_listing}}
计划平台：{{target_platforms}}
平台规则摘要：{{platform_policy_notes}}
```

```text
请分析以下平台驳回/警告信息，归因到可执行整改项。
输出：原因分类、涉及SKU、需改字段、建议动作、优先级、需谁确认、复检方法。
不要猜测平台未说明的处罚原因；不确定就写“需登录后台查看原始通知”。
平台通知：{{marketplace_notice}}
相关Listing：{{listing_snapshot}}
```

## 人类主管验收

- 老板看：P0/P1 是否影响正在投广告、库存高、主推 SKU；是否有负责人和截止时间。
- 运营看：问题字段、证据位置、建议改法是否能直接处理。
- 合规/品控看：认证、功效、安全、儿童、食品接触、电池等高风险项是否有材料支撑。
- 数据负责人看：导入数据是否只读、脱敏、无账号密钥。
- 每天抽查 5–10 个 `PASS` SKU，防止 AI 漏报；每周复盘误报和漏报。

## 不能自动化的事

- 不自动发布、删除、下架商品；AI 只给建议，平台操作由授权人员完成。
- 不自动承诺认证、测试报告、质保、医疗/安全功效、环保属性、适用年龄或法定合规状态。
- 不替代律师、认证机构、检测实验室、平台审核团队或税务顾问。
- 不绕过平台风控、验证码、登录限制、抓取限制或账号权限。
- 不使用未脱敏客户投诉、订单、地址、电话、邮箱做公开测试样本。
- 不把商标证书、测试报告、供应商合同、API token、账号密码放进提示词或公共仓库。
- 不把 AI 判断当作“平台一定通过”的保证；高风险项必须由运营和合规负责人确认。

## 第一周试点

- **Day 1：** 选 1 个平台 + 1 个品类 + 20–50 个 SKU，优先正在投广告、库存高、刚改过页面、差评敏感的商品。
- **Day 2：** 整理平台规则清单、禁词、品牌词、认证词、功效词、图片风险项。
- **Day 3：** 查标题、五点、A+、后台搜索词、属性、类目和变体。
- **Day 4：** 查主图、包装图、证书图、对比图、使用场景图。
- **Day 5：** 输出 `PASS / REWRITE / BLOCK` 清单，老板和合规确认 P0/P1。
- **Day 6：** 运营按建议改 5–10 个最高风险 SKU，保留改前改后版本。
- **Day 7：** 复查并定模板：以后上架前先过这张表。

## 相关 Skill / 工具栈

- **Amazon SP-API Listings / Product Type Definitions / Listings Restrictions**：适合 Amazon 卖家做只读字段、品类属性、上架限制核对；风险是 API 权限和 token 绝不能进提示词或公开仓库。
- **Google Merchant Center 商品数据规范与 Shopping Ads Policies**：适合独立站商品 feed、Google Shopping、广告商品审核前自查；风险是政策解释必须保留原文链接。
- **promptfoo / OpenAI Evals**：适合把历史踩坑案例做成固定测试题，检查 AI 是否漏掉高风险词；风险是测试样本要脱敏。
- **Playwright**：适合打开公开页面、截图、定位图片文字和页面显示问题；风险是不绕过登录、验证码、反爬或平台限制。
- **NocoDB / Metabase / Sheets**：适合做 SKU 风险表、负责人、截止日和老板看板；风险是只展示必要字段，限制访问权限。

## 公开资料

- https://developer-docs.amazon.com/sp-api/docs/listings-items-api-v2021-08-01-reference
- https://developer-docs.amazon.com/sp-api/docs/product-type-definitions-api-v2020-09-01-reference
- https://developer-docs.amazon.com/sp-api/docs/listings-restrictions-api-v2021-08-01-reference
- https://support.google.com/merchants/answer/7052112?hl=en
- https://support.google.com/merchants/answer/6149970?hl=en
- https://www.ebay.com/help/policies/prohibited-restricted-items/prohibited-restricted-items?id=4207
- https://www.facebook.com/policies_center/commerce
- https://github.com/promptfoo/promptfoo
- https://github.com/openai/evals
- https://github.com/microsoft/playwright
- https://github.com/nocodb/nocodb
- https://github.com/metabase/metabase
