# 市场/内容运营场景

## 场景问题

内容团队用 AI 最大的问题不是产量，而是容易写成模板稿：像汇报、像通稿、没有现场感。先把资料、角度、人味和审核链路搭起来，再谈批量化。

## 典型岗位/数字员工
- [开发工程师](../roles/engineering.md)：6 个 Skill
- [运营自动化负责人](../roles/operations-automation.md)：5 个 Skill
- [内容/市场运营负责人](../roles/content-marketing.md)：3 个 Skill
- [内容研究助理](../roles/content-research.md)：3 个 Skill
- [数字员工/Skill 设计师](../roles/digital-employee-designer.md)：3 个 Skill
- [知识库运营](../roles/knowledge-ops.md)：2 个 Skill
- [QA/测试负责人](../roles/qa-testing.md)：2 个 Skill
- [文档处理专员](../roles/document-ops.md)：1 个 Skill
- [法务/合规负责人](../roles/legal-compliance.md)：1 个 Skill
- [产品经理](../roles/product-manager.md)：1 个 Skill
- [Skill 观察研究员](../roles/skill-research.md)：1 个 Skill
- [策略/行业研究员](../roles/strategy-research.md)：1 个 Skill
- [工作流架构师](../roles/workflow-architecture.md)：1 个 Skill

## 当前可用 Skill（10）
|Skill|行业|岗位|风险|推荐用法|
|---|---|---|---|---|
|[browser-use/browser-use](https://github.com/browser-use/browser-use)|[软件/互联网/研发组织](../industries/software-internet.md)<br>[零售/电商/客服密集型](../industries/retail-ecommerce.md)<br>[通用企业/内部运营](../industries/general-enterprise.md)|[运营自动化负责人](../roles/operations-automation.md)<br>[开发工程师](../roles/engineering.md)<br>[QA/测试负责人](../roles/qa-testing.md)|medium|给网页流程自动化团队用，适合做采集、登录后操作和表单流转；生产账号、Cookie 和页面数据必须单独隔离。|
|[apify/crawlee](https://github.com/apify/crawlee)|[零售/电商/客服密集型](../industries/retail-ecommerce.md)<br>[通用企业/内部运营](../industries/general-enterprise.md)<br>[内容/媒体/营销服务](../industries/content-media.md)|[运营自动化负责人](../roles/operations-automation.md)<br>[开发工程师](../roles/engineering.md)<br>[内容研究助理](../roles/content-research.md)|medium|给采集和站点监测团队用，适合抓公开网页、盯页面变化、给 RAG 准备原料；robots、条款和隐私边界不能越。|
|[microsoft/markitdown](https://github.com/microsoft/markitdown)|[通用企业/内部运营](../industries/general-enterprise.md)<br>[专业服务：法律/咨询/研究](../industries/professional-services.md)<br>[内容/媒体/营销服务](../industries/content-media.md)|[文档处理专员](../roles/document-ops.md)<br>[知识库运营](../roles/knowledge-ops.md)<br>[法务/合规负责人](../roles/legal-compliance.md)|low|给知识库和文档处理团队用，适合把 PDF、PPT、Word 先转成能喂给 AI 的文本；转换稿不能当原件，敏感文件照样要脱敏。|
|[apify/crawlee-python](https://github.com/apify/crawlee-python)|[零售/电商/客服密集型](../industries/retail-ecommerce.md)<br>[通用企业/内部运营](../industries/general-enterprise.md)<br>[内容/媒体/营销服务](../industries/content-media.md)|[运营自动化负责人](../roles/operations-automation.md)<br>[开发工程师](../roles/engineering.md)<br>[内容研究助理](../roles/content-research.md)|medium|给 Python 技术栈的采集团队用，适合做公开网页抓取和浏览器执行；碰登录态或受限页面时要先补审计和权限。|
|[GLips/Figma-Context-MCP](https://github.com/GLips/Figma-Context-MCP)|[软件/互联网/研发组织](../industries/software-internet.md)<br>[专业服务：法律/咨询/研究](../industries/professional-services.md)|[数字员工/Skill 设计师](../roles/digital-employee-designer.md)<br>[产品经理](../roles/product-manager.md)<br>[开发工程师](../roles/engineering.md)|medium|给产品、设计系统和前端协作团队用，适合把设计稿上下文接到编码流程里；私有设计资产和 token 不能默认外放。|
|[microsoft/playwright-mcp](https://github.com/microsoft/playwright-mcp)|[软件/互联网/研发组织](../industries/software-internet.md)<br>[零售/电商/客服密集型](../industries/retail-ecommerce.md)<br>[内容/媒体/营销服务](../industries/content-media.md)|[QA/测试负责人](../roles/qa-testing.md)<br>[运营自动化负责人](../roles/operations-automation.md)<br>[开发工程师](../roles/engineering.md)|medium|给 QA 和网页运营自动化团队用，适合真实打开页面做回归和流程检查；凡是会点到真系统的动作都要隔离账号、保留审批。|
|[nanobrowser/nanobrowser](https://github.com/nanobrowser/nanobrowser)|[通用企业/内部运营](../industries/general-enterprise.md)<br>[零售/电商/客服密集型](../industries/retail-ecommerce.md)<br>[内容/媒体/营销服务](../industries/content-media.md)|[运营自动化负责人](../roles/operations-automation.md)<br>[开发工程师](../roles/engineering.md)<br>[内容/市场运营负责人](../roles/content-marketing.md)|medium|给一线运营和增长试点团队用，适合验证浏览器扩展形态的 AI 自动化；它依然会碰账号、页面和 API key，别当低风险玩具。|
|[langchain-ai/open_deep_research](https://github.com/langchain-ai/open_deep_research)|[通用企业/内部运营](../industries/general-enterprise.md)<br>[内容/媒体/营销服务](../industries/content-media.md)<br>[咨询/培训/知识服务](../industries/consulting-training.md)<br>[专业服务：法律/咨询/研究](../industries/professional-services.md)|[策略/行业研究员](../roles/strategy-research.md)<br>[内容研究助理](../roles/content-research.md)<br>[内容/市场运营负责人](../roles/content-marketing.md)|medium|给研究员和内容团队用，适合先把资料、出处、分歧拉出来；核查没做完前别直接变成可发结论。|
|[alirezarezvani/claude-skills](https://github.com/alirezarezvani/claude-skills)|[通用企业/内部运营](../industries/general-enterprise.md)<br>[内容/媒体/营销服务](../industries/content-media.md)<br>[咨询/培训/知识服务](../industries/consulting-training.md)|[知识库运营](../roles/knowledge-ops.md)<br>[数字员工/Skill 设计师](../roles/digital-employee-designer.md)<br>[工作流架构师](../roles/workflow-architecture.md)|medium|给搭内部 skill 库的人用，适合研究 skill 怎么分层和分发；不要整仓照搬，不然上下文和维护成本一起失控。|
|[JimLiu/baoyu-skills](https://github.com/JimLiu/baoyu-skills)|[内容/媒体/营销服务](../industries/content-media.md)<br>[咨询/培训/知识服务](../industries/consulting-training.md)|[内容/市场运营负责人](../roles/content-marketing.md)<br>[Skill 观察研究员](../roles/skill-research.md)<br>[数字员工/Skill 设计师](../roles/digital-employee-designer.md)|high|给内容型 skill 设计观察用，适合研究 packaging 写法；许可没讲清前不要进企业库，也别对外分发。|

## 推荐工作流
- 先做资料收集和事实核查，再进入写作、视觉和发布。
- 图文内容要先去 AI 味，再进入出图/排版流程。
- 涉及外部发布、版权、授权和账号权限时，必须保留人工审核。

## 风险边界
- 内容发布前必须有人审，尤其是事实、版权和品牌语气。
- 采集和浏览器自动化会接触账号和页面，会话隔离不能省。
- 公开传播前要先过许可与授权边界。
