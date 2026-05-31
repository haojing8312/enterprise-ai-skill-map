# 行政/运营场景

## 场景问题

行政运营类 Skill 看起来不像“高科技”，但往往最容易碰到账号、日志、文件和内部流程。真正的重点不是能不能自动化，而是谁授权、谁复核、出了错谁能回滚。

## 典型岗位/数字员工
- [AI 平台工程师](../roles/ai-platform.md)：11 个 Skill
- [工作流架构师](../roles/workflow-architecture.md)：10 个 Skill
- [开发工程师](../roles/engineering.md)：8 个 Skill
- [运营自动化负责人](../roles/operations-automation.md)：7 个 Skill
- [基础设施/运维负责人](../roles/infra-ops.md)：6 个 Skill
- [成本治理负责人](../roles/cost-governance.md)：5 个 Skill
- [研发平台/GitHub 管理员](../roles/engineering-platform.md)：3 个 Skill
- [运营/行政/流程管理员](../roles/operations-admin.md)：3 个 Skill
- [内容/市场运营负责人](../roles/content-marketing.md)：2 个 Skill
- [内容研究助理](../roles/content-research.md)：2 个 Skill
- [数字员工架构师](../roles/digital-employee-architect.md)：2 个 Skill
- [数字员工/Skill 设计师](../roles/digital-employee-designer.md)：2 个 Skill
- [技术负责人/研发效能负责人](../roles/engineering-management.md)：2 个 Skill
- [知识库运营](../roles/knowledge-ops.md)：2 个 Skill
- [QA/测试负责人](../roles/qa-testing.md)：2 个 Skill
- [Skill 观察研究员](../roles/skill-research.md)：2 个 Skill
- [AI 应用工程师](../roles/ai-application.md)：1 个 Skill
- [客服/客户成功负责人](../roles/customer-success.md)：1 个 Skill
- [法务/合规负责人](../roles/legal-compliance.md)：1 个 Skill
- [产品经理](../roles/product-manager.md)：1 个 Skill
- [策略/行业研究员](../roles/strategy-research.md)：1 个 Skill

## 当前可用 Skill（25）
|Skill|行业|岗位|风险|推荐用法|
|---|---|---|---|---|
|[browser-use/browser-use](https://github.com/browser-use/browser-use)|[软件/互联网/研发组织](../industries/software-internet.md)<br>[零售/电商/客服密集型](../industries/retail-ecommerce.md)<br>[通用企业/内部运营](../industries/general-enterprise.md)|[运营自动化负责人](../roles/operations-automation.md)<br>[开发工程师](../roles/engineering.md)<br>[QA/测试负责人](../roles/qa-testing.md)|medium|给网页流程自动化团队用，适合做采集、登录后操作和表单流转；生产账号、Cookie 和页面数据必须单独隔离。|
|[PrefectHQ/fastmcp](https://github.com/PrefectHQ/fastmcp)|[软件/互联网/研发组织](../industries/software-internet.md)<br>[AI/数据基础设施团队](../industries/ai-infrastructure.md)<br>[专业服务：法律/咨询/研究](../industries/professional-services.md)|[开发工程师](../roles/engineering.md)<br>[AI 平台工程师](../roles/ai-platform.md)<br>[工作流架构师](../roles/workflow-architecture.md)|medium|给 Python 团队用，适合把 MCP server、client 从 demo 做成可维护工程；工具层能连内网资源时，权限设计要先行。|
|[vllm-project/vllm](https://github.com/vllm-project/vllm)|[AI/数据基础设施团队](../industries/ai-infrastructure.md)<br>[软件/互联网/研发组织](../industries/software-internet.md)|[AI 平台工程师](../roles/ai-platform.md)<br>[基础设施/运维负责人](../roles/infra-ops.md)<br>[成本治理负责人](../roles/cost-governance.md)|medium|给多模型和高吞吐场景的 AI 平台、运维团队用，适合统一推理服务和看 GPU 利用率；没有运维能力时别把它当一键托管平台。|
|[punkpeye/awesome-mcp-servers](https://github.com/punkpeye/awesome-mcp-servers)|[通用企业/内部运营](../industries/general-enterprise.md)<br>[AI/数据基础设施团队](../industries/ai-infrastructure.md)<br>[软件/互联网/研发组织](../industries/software-internet.md)|[AI 平台工程师](../roles/ai-platform.md)<br>[工作流架构师](../roles/workflow-architecture.md)<br>[Skill 观察研究员](../roles/skill-research.md)|medium|给做选型长名单的人用，适合快速摸清 MCP 生态里有哪些连接器；它是目录，不是生产可用清单。|
|[ggml-org/llama.cpp](https://github.com/ggml-org/llama.cpp)|[AI/数据基础设施团队](../industries/ai-infrastructure.md)<br>[政企/国企/内网场景](../industries/government-stateowned.md)<br>[软件/互联网/研发组织](../industries/software-internet.md)|[AI 平台工程师](../roles/ai-platform.md)<br>[基础设施/运维负责人](../roles/infra-ops.md)|medium|给内网或成本敏感的 AI 平台团队用，适合先把模型跑在自己机器上验证可行性；它解决推理，不替你解决业务流程和模型许可。|
|[apify/crawlee](https://github.com/apify/crawlee)|[零售/电商/客服密集型](../industries/retail-ecommerce.md)<br>[通用企业/内部运营](../industries/general-enterprise.md)<br>[内容/媒体/营销服务](../industries/content-media.md)|[运营自动化负责人](../roles/operations-automation.md)<br>[开发工程师](../roles/engineering.md)<br>[内容研究助理](../roles/content-research.md)|medium|给采集和站点监测团队用，适合抓公开网页、盯页面变化、给 RAG 准备原料；robots、条款和隐私边界不能越。|
|[modelcontextprotocol/servers](https://github.com/modelcontextprotocol/servers)|[通用企业/内部运营](../industries/general-enterprise.md)<br>[软件/互联网/研发组织](../industries/software-internet.md)<br>[AI/数据基础设施团队](../industries/ai-infrastructure.md)|[AI 平台工程师](../roles/ai-platform.md)<br>[数字员工架构师](../roles/digital-employee-architect.md)<br>[运营/行政/流程管理员](../roles/operations-admin.md)|medium|给数字员工架构师和 AI 平台团队用，适合梳理文件、浏览器、GitHub 这类工具接入；每接一个 server 都要单独收权限。|
|[googleapis/mcp-toolbox](https://github.com/googleapis/mcp-toolbox)|[通用企业/内部运营](../industries/general-enterprise.md)<br>[AI/数据基础设施团队](../industries/ai-infrastructure.md)<br>[软件/互联网/研发组织](../industries/software-internet.md)|[AI 平台工程师](../roles/ai-platform.md)<br>[运营/行政/流程管理员](../roles/operations-admin.md)<br>[工作流架构师](../roles/workflow-architecture.md)|medium|给要把数据库接进 AI 助手的开发和分析团队用，适合做查询、发现和 schema 理解；谁能查、谁能写，必须先分层。|
|[triggerdotdev/trigger.dev](https://github.com/triggerdotdev/trigger.dev)|[软件/互联网/研发组织](../industries/software-internet.md)<br>[AI/数据基础设施团队](../industries/ai-infrastructure.md)<br>[通用企业/内部运营](../industries/general-enterprise.md)|[研发平台/GitHub 管理员](../roles/engineering-platform.md)<br>[运营自动化负责人](../roles/operations-automation.md)<br>[工作流架构师](../roles/workflow-architecture.md)|medium|给做长任务和事件驱动产品的团队用，适合追踪 AI workflow 和后台任务；secret 管理和失败补偿没设计好时别急着接业务系统。|
|[BerriAI/litellm](https://github.com/BerriAI/litellm)|[AI/数据基础设施团队](../industries/ai-infrastructure.md)<br>[软件/互联网/研发组织](../industries/software-internet.md)|[AI 平台工程师](../roles/ai-platform.md)<br>[成本治理负责人](../roles/cost-governance.md)<br>[基础设施/运维负责人](../roles/infra-ops.md)|medium|给多模型接入的 AI 平台团队用，适合统一路由、日志和预算；密钥会更集中，所以权限和审计要更严。|
|[mlflow/mlflow](https://github.com/mlflow/mlflow)|[AI/数据基础设施团队](../industries/ai-infrastructure.md)<br>[软件/互联网/研发组织](../industries/software-internet.md)<br>[通用企业/内部运营](../industries/general-enterprise.md)|[AI 平台工程师](../roles/ai-platform.md)<br>[成本治理负责人](../roles/cost-governance.md)<br>[策略/行业研究员](../roles/strategy-research.md)|medium|给做模型、agent 实验和评估的团队用，适合把实验记录、指标和治理放到同一条交付链路；平台装好了，不代表评估口径自然就有。|
|[apify/crawlee-python](https://github.com/apify/crawlee-python)|[零售/电商/客服密集型](../industries/retail-ecommerce.md)<br>[通用企业/内部运营](../industries/general-enterprise.md)<br>[内容/媒体/营销服务](../industries/content-media.md)|[运营自动化负责人](../roles/operations-automation.md)<br>[开发工程师](../roles/engineering.md)<br>[内容研究助理](../roles/content-research.md)|medium|给 Python 技术栈的采集团队用，适合做公开网页抓取和浏览器执行；碰登录态或受限页面时要先补审计和权限。|
|[github/github-mcp-server](https://github.com/github/github-mcp-server)|[软件/互联网/研发组织](../industries/software-internet.md)|[研发平台/GitHub 管理员](../roles/engineering-platform.md)<br>[运营/行政/流程管理员](../roles/operations-admin.md)<br>[技术负责人/研发效能负责人](../roles/engineering-management.md)|medium|给 GitHub 为核心的研发平台团队用，适合把 issue、PR、review 接进数字员工流程；token scope 和写权限不清时先别自动化。|
|[microsoft/playwright-mcp](https://github.com/microsoft/playwright-mcp)|[软件/互联网/研发组织](../industries/software-internet.md)<br>[零售/电商/客服密集型](../industries/retail-ecommerce.md)<br>[内容/媒体/营销服务](../industries/content-media.md)|[QA/测试负责人](../roles/qa-testing.md)<br>[运营自动化负责人](../roles/operations-automation.md)<br>[开发工程师](../roles/engineering.md)|medium|给 QA 和网页运营自动化团队用，适合真实打开页面做回归和流程检查；凡是会点到真系统的动作都要隔离账号、保留审批。|
|[tensorzero/tensorzero](https://github.com/tensorzero/tensorzero)|[AI/数据基础设施团队](../industries/ai-infrastructure.md)<br>[软件/互联网/研发组织](../industries/software-internet.md)<br>[通用企业/内部运营](../industries/general-enterprise.md)|[AI 平台工程师](../roles/ai-platform.md)<br>[成本治理负责人](../roles/cost-governance.md)<br>[工作流架构师](../roles/workflow-architecture.md)|medium|给想把模型调用、评估和优化放进一套平台的 AI 团队用，适合做 LLMOps 底座；中心化之后治理责任更重，别只看功能不看权限。|
|[casdoor/casdoor](https://github.com/casdoor/casdoor)|[通用企业/内部运营](../industries/general-enterprise.md)<br>[AI/数据基础设施团队](../industries/ai-infrastructure.md)<br>[政企/国企/内网场景](../industries/government-stateowned.md)|[AI 平台工程师](../roles/ai-platform.md)<br>[法务/合规负责人](../roles/legal-compliance.md)<br>[基础设施/运维负责人](../roles/infra-ops.md)|medium|给做统一身份认证的 AI 平台团队用，适合补齐数字员工接入后的 IAM 视角；组织、角色、权限模型没梳清前别急着上。|
|[openai/openai-agents-python](https://github.com/openai/openai-agents-python)|[软件/互联网/研发组织](../industries/software-internet.md)<br>[AI/数据基础设施团队](../industries/ai-infrastructure.md)<br>[咨询/培训/知识服务](../industries/consulting-training.md)|[AI 应用工程师](../roles/ai-application.md)<br>[工作流架构师](../roles/workflow-architecture.md)<br>[数字员工架构师](../roles/digital-employee-architect.md)|medium|给要自己编排多角色代理的产品和工程团队用，适合做 handoff 和工具调用原型；它是 SDK，不是现成业务系统。|
|[mem0ai/mem0](https://github.com/mem0ai/mem0)|[通用企业/内部运营](../industries/general-enterprise.md)<br>[零售/电商/客服密集型](../industries/retail-ecommerce.md)|[客服/客户成功负责人](../roles/customer-success.md)<br>[产品经理](../roles/product-manager.md)<br>[知识库运营](../roles/knowledge-ops.md)|medium|给客服、助理和产品团队用，适合让助手记住上下文和用户偏好；没定保留期、删除和纠错机制前别随便存用户记忆。|
|[nanobrowser/nanobrowser](https://github.com/nanobrowser/nanobrowser)|[通用企业/内部运营](../industries/general-enterprise.md)<br>[零售/电商/客服密集型](../industries/retail-ecommerce.md)<br>[内容/媒体/营销服务](../industries/content-media.md)|[运营自动化负责人](../roles/operations-automation.md)<br>[开发工程师](../roles/engineering.md)<br>[内容/市场运营负责人](../roles/content-marketing.md)|medium|给一线运营和增长试点团队用，适合验证浏览器扩展形态的 AI 自动化；它依然会碰账号、页面和 API key，别当低风险玩具。|
|[apache/airflow](https://github.com/apache/airflow)|[通用企业/内部运营](../industries/general-enterprise.md)<br>[AI/数据基础设施团队](../industries/ai-infrastructure.md)<br>[专业服务：法律/咨询/研究](../industries/professional-services.md)|[基础设施/运维负责人](../roles/infra-ops.md)<br>[运营自动化负责人](../roles/operations-automation.md)<br>[工作流架构师](../roles/workflow-architecture.md)|medium|给已经有调度体系的企业运维和流程架构团队用，适合把 AI 任务纳入定时和依赖编排；如果只是轻量自动化，别先上重平台。|
|[openlit/openlit](https://github.com/openlit/openlit)|[AI/数据基础设施团队](../industries/ai-infrastructure.md)<br>[通用企业/内部运营](../industries/general-enterprise.md)<br>[软件/互联网/研发组织](../industries/software-internet.md)|[AI 平台工程师](../roles/ai-platform.md)<br>[基础设施/运维负责人](../roles/infra-ops.md)<br>[成本治理负责人](../roles/cost-governance.md)|medium|给 AI 平台和成本治理团队用，适合看调用链路、日志和花费；只有看板没有治理动作，观测价值会很快打折。|
|[alirezarezvani/claude-skills](https://github.com/alirezarezvani/claude-skills)|[通用企业/内部运营](../industries/general-enterprise.md)<br>[内容/媒体/营销服务](../industries/content-media.md)<br>[咨询/培训/知识服务](../industries/consulting-training.md)|[知识库运营](../roles/knowledge-ops.md)<br>[数字员工/Skill 设计师](../roles/digital-employee-designer.md)<br>[工作流架构师](../roles/workflow-architecture.md)|medium|给搭内部 skill 库的人用，适合研究 skill 怎么分层和分发；不要整仓照搬，不然上下文和维护成本一起失控。|
|[spring-ai-community/spring-ai-agent-utils](https://github.com/spring-ai-community/spring-ai-agent-utils)|[软件/互联网/研发组织](../industries/software-internet.md)<br>[AI/数据基础设施团队](../industries/ai-infrastructure.md)<br>[专业服务：法律/咨询/研究](../industries/professional-services.md)|[开发工程师](../roles/engineering.md)<br>[研发平台/GitHub 管理员](../roles/engineering-platform.md)<br>[工作流架构师](../roles/workflow-architecture.md)|medium|给 Java、Spring 团队用，适合把 skill、tool、handoff 封装进企业应用；没有安全评审前别把工具接口直接暴露出去。|
|[JimLiu/baoyu-skills](https://github.com/JimLiu/baoyu-skills)|[内容/媒体/营销服务](../industries/content-media.md)<br>[咨询/培训/知识服务](../industries/consulting-training.md)|[内容/市场运营负责人](../roles/content-marketing.md)<br>[Skill 观察研究员](../roles/skill-research.md)<br>[数字员工/Skill 设计师](../roles/digital-employee-designer.md)|high|给内容型 skill 设计观察用，适合研究 packaging 写法；许可没讲清前不要进企业库，也别对外分发。|
|[obra/superpowers](https://github.com/obra/superpowers)|[软件/互联网/研发组织](../industries/software-internet.md)<br>[咨询/培训/知识服务](../industries/consulting-training.md)|[技术负责人/研发效能负责人](../roles/engineering-management.md)<br>[开发工程师](../roles/engineering.md)<br>[工作流架构师](../roles/workflow-architecture.md)|low|给技术负责人和 AI 编码流程设计者用，适合把 spec、测试、验收提前到写码前面；前提是团队本来就愿意做评审和回滚。|

## 推荐工作流
- 先把账号、权限、日志和平台边界梳清，再接流程自动化。
- 高频但可回滚的后台操作优先，先不要碰高敏写操作。
- 任何能触达生产系统、模型 key 或客户数据的动作都要留审批链。

## 风险边界
- 后台、账号和权限动作默认高风险。
- 能写生产系统的能力必须有审批和回滚。
- 日志、token 和密钥不能随意暴露。
