# 客服/交付场景

## 场景问题

客服和交付场景不是缺回答速度，而是怕上下文断掉、用户历史丢掉、错误信息反复被引用。记忆层要先管“记什么、记多久、怎么删”。

## 典型岗位/数字员工
- [开发工程师](../roles/engineering.md)：2 个 Skill
- [运营自动化负责人](../roles/operations-automation.md)：2 个 Skill
- [AI 平台工程师](../roles/ai-platform.md)：1 个 Skill
- [内容研究助理](../roles/content-research.md)：1 个 Skill
- [客服/客户成功负责人](../roles/customer-success.md)：1 个 Skill
- [基础设施/运维负责人](../roles/infra-ops.md)：1 个 Skill
- [知识库运营](../roles/knowledge-ops.md)：1 个 Skill
- [法务/合规负责人](../roles/legal-compliance.md)：1 个 Skill
- [产品经理](../roles/product-manager.md)：1 个 Skill
- [QA/测试负责人](../roles/qa-testing.md)：1 个 Skill

## 当前可用 Skill（4）
|Skill|行业|岗位|风险|推荐用法|
|---|---|---|---|---|
|[browser-use/browser-use](https://github.com/browser-use/browser-use)|[软件/互联网/研发组织](../industries/software-internet.md)<br>[零售/电商/客服密集型](../industries/retail-ecommerce.md)<br>[通用企业/内部运营](../industries/general-enterprise.md)|[运营自动化负责人](../roles/operations-automation.md)<br>[开发工程师](../roles/engineering.md)<br>[QA/测试负责人](../roles/qa-testing.md)|medium|给网页流程自动化团队用，适合做采集、登录后操作和表单流转；生产账号、Cookie 和页面数据必须单独隔离。|
|[apify/crawlee](https://github.com/apify/crawlee)|[零售/电商/客服密集型](../industries/retail-ecommerce.md)<br>[通用企业/内部运营](../industries/general-enterprise.md)<br>[内容/媒体/营销服务](../industries/content-media.md)|[运营自动化负责人](../roles/operations-automation.md)<br>[开发工程师](../roles/engineering.md)<br>[内容研究助理](../roles/content-research.md)|medium|给采集和站点监测团队用，适合抓公开网页、盯页面变化、给 RAG 准备原料；robots、条款和隐私边界不能越。|
|[casdoor/casdoor](https://github.com/casdoor/casdoor)|[通用企业/内部运营](../industries/general-enterprise.md)<br>[AI/数据基础设施团队](../industries/ai-infrastructure.md)<br>[政企/国企/内网场景](../industries/government-stateowned.md)|[AI 平台工程师](../roles/ai-platform.md)<br>[法务/合规负责人](../roles/legal-compliance.md)<br>[基础设施/运维负责人](../roles/infra-ops.md)|medium|给做统一身份认证的 AI 平台团队用，适合补齐数字员工接入后的 IAM 视角；组织、角色、权限模型没梳清前别急着上。|
|[mem0ai/mem0](https://github.com/mem0ai/mem0)|[通用企业/内部运营](../industries/general-enterprise.md)<br>[零售/电商/客服密集型](../industries/retail-ecommerce.md)|[客服/客户成功负责人](../roles/customer-success.md)<br>[产品经理](../roles/product-manager.md)<br>[知识库运营](../roles/knowledge-ops.md)|medium|给客服、助理和产品团队用，适合让助手记住上下文和用户偏好；没定保留期、删除和纠错机制前别随便存用户记忆。|

## 推荐工作流
- 先把用户记忆、FAQ 和工单上下文串起来，再让浏览器/采集类 Skill 帮忙补信息。
- 用户数据要明确 retention、删除和纠错机制，避免把错误记忆继续放大。
- 适合从内部客服或低风险问答场景开始试点。

## 风险边界
- 用户记忆和工单上下文包含 PII，保留期与删除规则必须明确。
- 错误记忆会直接污染后续回复。
- 对外答复不要超出已有知识和授权。
