# 研发/产品场景

## 场景问题

AI 写码真正的风险，不是代码生成慢，而是没有 spec、没有测试、没有验收，最后把错误交给人肉兜底。研发类 Skill 应该被放进“有人审、可回滚、可追责”的交付链路里。

## 典型岗位/数字员工
- [工作流架构师](../roles/workflow-architecture.md)：12 个 Skill
- [AI 平台工程师](../roles/ai-platform.md)：10 个 Skill
- [开发工程师](../roles/engineering.md)：10 个 Skill
- [技术负责人/研发效能负责人](../roles/engineering-management.md)：6 个 Skill
- [成本治理负责人](../roles/cost-governance.md)：5 个 Skill
- [基础设施/运维负责人](../roles/infra-ops.md)：5 个 Skill
- [研发平台/GitHub 管理员](../roles/engineering-platform.md)：4 个 Skill
- [运营自动化负责人](../roles/operations-automation.md)：4 个 Skill
- [知识库运营](../roles/knowledge-ops.md)：3 个 Skill
- [运营/行政/流程管理员](../roles/operations-admin.md)：3 个 Skill
- [QA/测试负责人](../roles/qa-testing.md)：3 个 Skill
- [Skill 观察研究员](../roles/skill-research.md)：3 个 Skill
- [策略/行业研究员](../roles/strategy-research.md)：3 个 Skill
- [内容研究助理](../roles/content-research.md)：2 个 Skill
- [数字员工架构师](../roles/digital-employee-architect.md)：2 个 Skill
- [数字员工/Skill 设计师](../roles/digital-employee-designer.md)：2 个 Skill
- [AI 应用工程师](../roles/ai-application.md)：1 个 Skill
- [内容/市场运营负责人](../roles/content-marketing.md)：1 个 Skill
- [产品经理](../roles/product-manager.md)：1 个 Skill

## 当前可用 Skill（27）
|Skill|行业|岗位|风险|推荐用法|
|---|---|---|---|---|
|[mattpocock/skills](https://github.com/mattpocock/skills)|[软件/互联网/研发组织](../industries/software-internet.md)<br>[咨询/培训/知识服务](../industries/consulting-training.md)|[开发工程师](../roles/engineering.md)<br>[QA/测试负责人](../roles/qa-testing.md)<br>[工作流架构师](../roles/workflow-architecture.md)|low|给工程团队搭 skills 模板库用，适合看什么 skill 真会被开发者反复调用；公开样本要先裁剪，再变成企业标准。|
|[openai/codex](https://github.com/openai/codex)|[软件/互联网/研发组织](../industries/software-internet.md)|[开发工程师](../roles/engineering.md)<br>[技术负责人/研发效能负责人](../roles/engineering-management.md)<br>[QA/测试负责人](../roles/qa-testing.md)|medium|给会看代码的开发和测试负责人用，适合读仓库、修小 bug、补测试；别拿它跳过评审直接动生产。|
|[google-gemini/gemini-cli](https://github.com/google-gemini/gemini-cli)|[软件/互联网/研发组织](../industries/software-internet.md)<br>[通用企业/内部运营](../industries/general-enterprise.md)|[开发工程师](../roles/engineering.md)<br>[技术负责人/研发效能负责人](../roles/engineering-management.md)<br>[知识库运营](../roles/knowledge-ops.md)|medium|给想比较不同 CLI agent 的研发和知识工作团队用，适合放进终端工作流试用；终端能执行命令，不等于它有审批权。|
|[anomalyco/opencode](https://github.com/anomalyco/opencode)|[软件/互联网/研发组织](../industries/software-internet.md)<br>[AI/数据基础设施团队](../industries/ai-infrastructure.md)|[开发工程师](../roles/engineering.md)<br>[研发平台/GitHub 管理员](../roles/engineering-platform.md)<br>[技术负责人/研发效能负责人](../roles/engineering-management.md)|medium|给想自建开源 AI 编码底座的研发团队用，适合做可二次开发的 coding agent 流程；没有沙箱和权限控制时别往生产环境放。|
|[PrefectHQ/fastmcp](https://github.com/PrefectHQ/fastmcp)|[软件/互联网/研发组织](../industries/software-internet.md)<br>[AI/数据基础设施团队](../industries/ai-infrastructure.md)<br>[专业服务：法律/咨询/研究](../industries/professional-services.md)|[开发工程师](../roles/engineering.md)<br>[AI 平台工程师](../roles/ai-platform.md)<br>[工作流架构师](../roles/workflow-architecture.md)|medium|给 Python 团队用，适合把 MCP server、client 从 demo 做成可维护工程；工具层能连内网资源时，权限设计要先行。|
|[vllm-project/vllm](https://github.com/vllm-project/vllm)|[AI/数据基础设施团队](../industries/ai-infrastructure.md)<br>[软件/互联网/研发组织](../industries/software-internet.md)|[AI 平台工程师](../roles/ai-platform.md)<br>[基础设施/运维负责人](../roles/infra-ops.md)<br>[成本治理负责人](../roles/cost-governance.md)|medium|给多模型和高吞吐场景的 AI 平台、运维团队用，适合统一推理服务和看 GPU 利用率；没有运维能力时别把它当一键托管平台。|
|[punkpeye/awesome-mcp-servers](https://github.com/punkpeye/awesome-mcp-servers)|[通用企业/内部运营](../industries/general-enterprise.md)<br>[AI/数据基础设施团队](../industries/ai-infrastructure.md)<br>[软件/互联网/研发组织](../industries/software-internet.md)|[AI 平台工程师](../roles/ai-platform.md)<br>[工作流架构师](../roles/workflow-architecture.md)<br>[Skill 观察研究员](../roles/skill-research.md)|medium|给做选型长名单的人用，适合快速摸清 MCP 生态里有哪些连接器；它是目录，不是生产可用清单。|
|[ggml-org/llama.cpp](https://github.com/ggml-org/llama.cpp)|[AI/数据基础设施团队](../industries/ai-infrastructure.md)<br>[政企/国企/内网场景](../industries/government-stateowned.md)<br>[软件/互联网/研发组织](../industries/software-internet.md)|[AI 平台工程师](../roles/ai-platform.md)<br>[基础设施/运维负责人](../roles/infra-ops.md)|medium|给内网或成本敏感的 AI 平台团队用，适合先把模型跑在自己机器上验证可行性；它解决推理，不替你解决业务流程和模型许可。|
|[modelcontextprotocol/servers](https://github.com/modelcontextprotocol/servers)|[通用企业/内部运营](../industries/general-enterprise.md)<br>[软件/互联网/研发组织](../industries/software-internet.md)<br>[AI/数据基础设施团队](../industries/ai-infrastructure.md)|[AI 平台工程师](../roles/ai-platform.md)<br>[数字员工架构师](../roles/digital-employee-architect.md)<br>[运营/行政/流程管理员](../roles/operations-admin.md)|medium|给数字员工架构师和 AI 平台团队用，适合梳理文件、浏览器、GitHub 这类工具接入；每接一个 server 都要单独收权限。|
|[googleapis/mcp-toolbox](https://github.com/googleapis/mcp-toolbox)|[通用企业/内部运营](../industries/general-enterprise.md)<br>[AI/数据基础设施团队](../industries/ai-infrastructure.md)<br>[软件/互联网/研发组织](../industries/software-internet.md)|[AI 平台工程师](../roles/ai-platform.md)<br>[运营/行政/流程管理员](../roles/operations-admin.md)<br>[工作流架构师](../roles/workflow-architecture.md)|medium|给要把数据库接进 AI 助手的开发和分析团队用，适合做查询、发现和 schema 理解；谁能查、谁能写，必须先分层。|
|[triggerdotdev/trigger.dev](https://github.com/triggerdotdev/trigger.dev)|[软件/互联网/研发组织](../industries/software-internet.md)<br>[AI/数据基础设施团队](../industries/ai-infrastructure.md)<br>[通用企业/内部运营](../industries/general-enterprise.md)|[研发平台/GitHub 管理员](../roles/engineering-platform.md)<br>[运营自动化负责人](../roles/operations-automation.md)<br>[工作流架构师](../roles/workflow-architecture.md)|medium|给做长任务和事件驱动产品的团队用，适合追踪 AI workflow 和后台任务；secret 管理和失败补偿没设计好时别急着接业务系统。|
|[BerriAI/litellm](https://github.com/BerriAI/litellm)|[AI/数据基础设施团队](../industries/ai-infrastructure.md)<br>[软件/互联网/研发组织](../industries/software-internet.md)|[AI 平台工程师](../roles/ai-platform.md)<br>[成本治理负责人](../roles/cost-governance.md)<br>[基础设施/运维负责人](../roles/infra-ops.md)|medium|给多模型接入的 AI 平台团队用，适合统一路由、日志和预算；密钥会更集中，所以权限和审计要更严。|
|[mlflow/mlflow](https://github.com/mlflow/mlflow)|[AI/数据基础设施团队](../industries/ai-infrastructure.md)<br>[软件/互联网/研发组织](../industries/software-internet.md)<br>[通用企业/内部运营](../industries/general-enterprise.md)|[AI 平台工程师](../roles/ai-platform.md)<br>[成本治理负责人](../roles/cost-governance.md)<br>[策略/行业研究员](../roles/strategy-research.md)|medium|给做模型、agent 实验和评估的团队用，适合把实验记录、指标和治理放到同一条交付链路；平台装好了，不代表评估口径自然就有。|
|[apify/crawlee-python](https://github.com/apify/crawlee-python)|[零售/电商/客服密集型](../industries/retail-ecommerce.md)<br>[通用企业/内部运营](../industries/general-enterprise.md)<br>[内容/媒体/营销服务](../industries/content-media.md)|[运营自动化负责人](../roles/operations-automation.md)<br>[开发工程师](../roles/engineering.md)<br>[内容研究助理](../roles/content-research.md)|medium|给 Python 技术栈的采集团队用，适合做公开网页抓取和浏览器执行；碰登录态或受限页面时要先补审计和权限。|
|[GLips/Figma-Context-MCP](https://github.com/GLips/Figma-Context-MCP)|[软件/互联网/研发组织](../industries/software-internet.md)<br>[专业服务：法律/咨询/研究](../industries/professional-services.md)|[数字员工/Skill 设计师](../roles/digital-employee-designer.md)<br>[产品经理](../roles/product-manager.md)<br>[开发工程师](../roles/engineering.md)|medium|给产品、设计系统和前端协作团队用，适合把设计稿上下文接到编码流程里；私有设计资产和 token 不能默认外放。|
|[github/github-mcp-server](https://github.com/github/github-mcp-server)|[软件/互联网/研发组织](../industries/software-internet.md)|[研发平台/GitHub 管理员](../roles/engineering-platform.md)<br>[运营/行政/流程管理员](../roles/operations-admin.md)<br>[技术负责人/研发效能负责人](../roles/engineering-management.md)|medium|给 GitHub 为核心的研发平台团队用，适合把 issue、PR、review 接进数字员工流程；token scope 和写权限不清时先别自动化。|
|[revfactory/harness](https://github.com/revfactory/harness)|[软件/互联网/研发组织](../industries/software-internet.md)<br>[咨询/培训/知识服务](../industries/consulting-training.md)|[技术负责人/研发效能负责人](../roles/engineering-management.md)<br>[工作流架构师](../roles/workflow-architecture.md)<br>[Skill 观察研究员](../roles/skill-research.md)|low|给咨询交付和数字员工设计团队用，适合把一个岗位拆成 agent 团队加 skill 包；它更像方法样本，不是接上就能上岗的员工。|
|[microsoft/playwright-mcp](https://github.com/microsoft/playwright-mcp)|[软件/互联网/研发组织](../industries/software-internet.md)<br>[零售/电商/客服密集型](../industries/retail-ecommerce.md)<br>[内容/媒体/营销服务](../industries/content-media.md)|[QA/测试负责人](../roles/qa-testing.md)<br>[运营自动化负责人](../roles/operations-automation.md)<br>[开发工程师](../roles/engineering.md)|medium|给 QA 和网页运营自动化团队用，适合真实打开页面做回归和流程检查；凡是会点到真系统的动作都要隔离账号、保留审批。|
|[K-Dense-AI/scientific-agent-skills](https://github.com/K-Dense-AI/scientific-agent-skills)|[专业服务：法律/咨询/研究](../industries/professional-services.md)<br>[咨询/培训/知识服务](../industries/consulting-training.md)<br>[软件/互联网/研发组织](../industries/software-internet.md)|[策略/行业研究员](../roles/strategy-research.md)<br>[Skill 观察研究员](../roles/skill-research.md)<br>[知识库运营](../roles/knowledge-ops.md)|medium|给做垂直知识库或培训方案的人用，适合研究专业领域 skill 怎么围绕数据源组织；专业结论仍要让行业专家复核。|
|[tensorzero/tensorzero](https://github.com/tensorzero/tensorzero)|[AI/数据基础设施团队](../industries/ai-infrastructure.md)<br>[软件/互联网/研发组织](../industries/software-internet.md)<br>[通用企业/内部运营](../industries/general-enterprise.md)|[AI 平台工程师](../roles/ai-platform.md)<br>[成本治理负责人](../roles/cost-governance.md)<br>[工作流架构师](../roles/workflow-architecture.md)|medium|给想把模型调用、评估和优化放进一套平台的 AI 团队用，适合做 LLMOps 底座；中心化之后治理责任更重，别只看功能不看权限。|
|[openai/openai-agents-python](https://github.com/openai/openai-agents-python)|[软件/互联网/研发组织](../industries/software-internet.md)<br>[AI/数据基础设施团队](../industries/ai-infrastructure.md)<br>[咨询/培训/知识服务](../industries/consulting-training.md)|[AI 应用工程师](../roles/ai-application.md)<br>[工作流架构师](../roles/workflow-architecture.md)<br>[数字员工架构师](../roles/digital-employee-architect.md)|medium|给要自己编排多角色代理的产品和工程团队用，适合做 handoff 和工具调用原型；它是 SDK，不是现成业务系统。|
|[langchain-ai/open_deep_research](https://github.com/langchain-ai/open_deep_research)|[通用企业/内部运营](../industries/general-enterprise.md)<br>[内容/媒体/营销服务](../industries/content-media.md)<br>[咨询/培训/知识服务](../industries/consulting-training.md)<br>[专业服务：法律/咨询/研究](../industries/professional-services.md)|[策略/行业研究员](../roles/strategy-research.md)<br>[内容研究助理](../roles/content-research.md)<br>[内容/市场运营负责人](../roles/content-marketing.md)|medium|给研究员和内容团队用，适合先把资料、出处、分歧拉出来；核查没做完前别直接变成可发结论。|
|[apache/airflow](https://github.com/apache/airflow)|[通用企业/内部运营](../industries/general-enterprise.md)<br>[AI/数据基础设施团队](../industries/ai-infrastructure.md)<br>[专业服务：法律/咨询/研究](../industries/professional-services.md)|[基础设施/运维负责人](../roles/infra-ops.md)<br>[运营自动化负责人](../roles/operations-automation.md)<br>[工作流架构师](../roles/workflow-architecture.md)|medium|给已经有调度体系的企业运维和流程架构团队用，适合把 AI 任务纳入定时和依赖编排；如果只是轻量自动化，别先上重平台。|
|[openlit/openlit](https://github.com/openlit/openlit)|[AI/数据基础设施团队](../industries/ai-infrastructure.md)<br>[通用企业/内部运营](../industries/general-enterprise.md)<br>[软件/互联网/研发组织](../industries/software-internet.md)|[AI 平台工程师](../roles/ai-platform.md)<br>[基础设施/运维负责人](../roles/infra-ops.md)<br>[成本治理负责人](../roles/cost-governance.md)|medium|给 AI 平台和成本治理团队用，适合看调用链路、日志和花费；只有看板没有治理动作，观测价值会很快打折。|
|[alirezarezvani/claude-skills](https://github.com/alirezarezvani/claude-skills)|[通用企业/内部运营](../industries/general-enterprise.md)<br>[内容/媒体/营销服务](../industries/content-media.md)<br>[咨询/培训/知识服务](../industries/consulting-training.md)|[知识库运营](../roles/knowledge-ops.md)<br>[数字员工/Skill 设计师](../roles/digital-employee-designer.md)<br>[工作流架构师](../roles/workflow-architecture.md)|medium|给搭内部 skill 库的人用，适合研究 skill 怎么分层和分发；不要整仓照搬，不然上下文和维护成本一起失控。|
|[spring-ai-community/spring-ai-agent-utils](https://github.com/spring-ai-community/spring-ai-agent-utils)|[软件/互联网/研发组织](../industries/software-internet.md)<br>[AI/数据基础设施团队](../industries/ai-infrastructure.md)<br>[专业服务：法律/咨询/研究](../industries/professional-services.md)|[开发工程师](../roles/engineering.md)<br>[研发平台/GitHub 管理员](../roles/engineering-platform.md)<br>[工作流架构师](../roles/workflow-architecture.md)|medium|给 Java、Spring 团队用，适合把 skill、tool、handoff 封装进企业应用；没有安全评审前别把工具接口直接暴露出去。|
|[obra/superpowers](https://github.com/obra/superpowers)|[软件/互联网/研发组织](../industries/software-internet.md)<br>[咨询/培训/知识服务](../industries/consulting-training.md)|[技术负责人/研发效能负责人](../roles/engineering-management.md)<br>[开发工程师](../roles/engineering.md)<br>[工作流架构师](../roles/workflow-architecture.md)|low|给技术负责人和 AI 编码流程设计者用，适合把 spec、测试、验收提前到写码前面；前提是团队本来就愿意做评审和回滚。|

## 推荐工作流
- 先用 spec/验收标准把需求前置，再让编程型 Skill 做局部实现。
- 把测试、评审和发布检查放在生成之后，避免直接把代码输出当成最终答案。
- 涉及仓库写权限、CI、生产配置时，保留人工审批和回滚路径。

## 风险边界
- 代码、仓库、CI 和发布动作都属于可逆但高影响操作，需要审批和回滚。
- 自动生成不等于自动验收，测试与 review 不能省。
- 密钥、生产配置和私有仓库权限必须单独隔离。
