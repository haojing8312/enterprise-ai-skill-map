# 办公协同场景

## 场景问题

办公协同里最常见的误判，是把“能处理文档”理解成“能理解业务责任”。这类 Skill 更适合做整理、接线、记忆和入库，不适合替人定结论。

## 典型岗位/数字员工
- [AI 平台工程师](../roles/ai-platform.md)：4 个 Skill
- [知识库运营](../roles/knowledge-ops.md)：4 个 Skill
- [工作流架构师](../roles/workflow-architecture.md)：4 个 Skill
- [Skill 观察研究员](../roles/skill-research.md)：3 个 Skill
- [开发工程师](../roles/engineering.md)：2 个 Skill
- [技术负责人/研发效能负责人](../roles/engineering-management.md)：2 个 Skill
- [基础设施/运维负责人](../roles/infra-ops.md)：2 个 Skill
- [法务/合规负责人](../roles/legal-compliance.md)：2 个 Skill
- [运营/行政/流程管理员](../roles/operations-admin.md)：2 个 Skill
- [运营自动化负责人](../roles/operations-automation.md)：2 个 Skill
- [内容/市场运营负责人](../roles/content-marketing.md)：1 个 Skill
- [客服/客户成功负责人](../roles/customer-success.md)：1 个 Skill
- [数字员工架构师](../roles/digital-employee-architect.md)：1 个 Skill
- [文档处理专员](../roles/document-ops.md)：1 个 Skill
- [产品经理](../roles/product-manager.md)：1 个 Skill
- [策略/行业研究员](../roles/strategy-research.md)：1 个 Skill

## 当前可用 Skill（11）
|Skill|行业|岗位|风险|推荐用法|
|---|---|---|---|---|
|[google-gemini/gemini-cli](https://github.com/google-gemini/gemini-cli)|[软件/互联网/研发组织](../industries/software-internet.md)<br>[通用企业/内部运营](../industries/general-enterprise.md)|[开发工程师](../roles/engineering.md)<br>[技术负责人/研发效能负责人](../roles/engineering-management.md)<br>[知识库运营](../roles/knowledge-ops.md)|medium|给想比较不同 CLI agent 的研发和知识工作团队用，适合放进终端工作流试用；终端能执行命令，不等于它有审批权。|
|[punkpeye/awesome-mcp-servers](https://github.com/punkpeye/awesome-mcp-servers)|[通用企业/内部运营](../industries/general-enterprise.md)<br>[AI/数据基础设施团队](../industries/ai-infrastructure.md)<br>[软件/互联网/研发组织](../industries/software-internet.md)|[AI 平台工程师](../roles/ai-platform.md)<br>[工作流架构师](../roles/workflow-architecture.md)<br>[Skill 观察研究员](../roles/skill-research.md)|medium|给做选型长名单的人用，适合快速摸清 MCP 生态里有哪些连接器；它是目录，不是生产可用清单。|
|[modelcontextprotocol/servers](https://github.com/modelcontextprotocol/servers)|[通用企业/内部运营](../industries/general-enterprise.md)<br>[软件/互联网/研发组织](../industries/software-internet.md)<br>[AI/数据基础设施团队](../industries/ai-infrastructure.md)|[AI 平台工程师](../roles/ai-platform.md)<br>[数字员工架构师](../roles/digital-employee-architect.md)<br>[运营/行政/流程管理员](../roles/operations-admin.md)|medium|给数字员工架构师和 AI 平台团队用，适合梳理文件、浏览器、GitHub 这类工具接入；每接一个 server 都要单独收权限。|
|[microsoft/markitdown](https://github.com/microsoft/markitdown)|[通用企业/内部运营](../industries/general-enterprise.md)<br>[专业服务：法律/咨询/研究](../industries/professional-services.md)<br>[内容/媒体/营销服务](../industries/content-media.md)|[文档处理专员](../roles/document-ops.md)<br>[知识库运营](../roles/knowledge-ops.md)<br>[法务/合规负责人](../roles/legal-compliance.md)|low|给知识库和文档处理团队用，适合把 PDF、PPT、Word 先转成能喂给 AI 的文本；转换稿不能当原件，敏感文件照样要脱敏。|
|[googleapis/mcp-toolbox](https://github.com/googleapis/mcp-toolbox)|[通用企业/内部运营](../industries/general-enterprise.md)<br>[AI/数据基础设施团队](../industries/ai-infrastructure.md)<br>[软件/互联网/研发组织](../industries/software-internet.md)|[AI 平台工程师](../roles/ai-platform.md)<br>[运营/行政/流程管理员](../roles/operations-admin.md)<br>[工作流架构师](../roles/workflow-architecture.md)|medium|给要把数据库接进 AI 助手的开发和分析团队用，适合做查询、发现和 schema 理解；谁能查、谁能写，必须先分层。|
|[revfactory/harness](https://github.com/revfactory/harness)|[软件/互联网/研发组织](../industries/software-internet.md)<br>[咨询/培训/知识服务](../industries/consulting-training.md)|[技术负责人/研发效能负责人](../roles/engineering-management.md)<br>[工作流架构师](../roles/workflow-architecture.md)<br>[Skill 观察研究员](../roles/skill-research.md)|low|给咨询交付和数字员工设计团队用，适合把一个岗位拆成 agent 团队加 skill 包；它更像方法样本，不是接上就能上岗的员工。|
|[K-Dense-AI/scientific-agent-skills](https://github.com/K-Dense-AI/scientific-agent-skills)|[专业服务：法律/咨询/研究](../industries/professional-services.md)<br>[咨询/培训/知识服务](../industries/consulting-training.md)<br>[软件/互联网/研发组织](../industries/software-internet.md)|[策略/行业研究员](../roles/strategy-research.md)<br>[Skill 观察研究员](../roles/skill-research.md)<br>[知识库运营](../roles/knowledge-ops.md)|medium|给做垂直知识库或培训方案的人用，适合研究专业领域 skill 怎么围绕数据源组织；专业结论仍要让行业专家复核。|
|[casdoor/casdoor](https://github.com/casdoor/casdoor)|[通用企业/内部运营](../industries/general-enterprise.md)<br>[AI/数据基础设施团队](../industries/ai-infrastructure.md)<br>[政企/国企/内网场景](../industries/government-stateowned.md)|[AI 平台工程师](../roles/ai-platform.md)<br>[法务/合规负责人](../roles/legal-compliance.md)<br>[基础设施/运维负责人](../roles/infra-ops.md)|medium|给做统一身份认证的 AI 平台团队用，适合补齐数字员工接入后的 IAM 视角；组织、角色、权限模型没梳清前别急着上。|
|[mem0ai/mem0](https://github.com/mem0ai/mem0)|[通用企业/内部运营](../industries/general-enterprise.md)<br>[零售/电商/客服密集型](../industries/retail-ecommerce.md)|[客服/客户成功负责人](../roles/customer-success.md)<br>[产品经理](../roles/product-manager.md)<br>[知识库运营](../roles/knowledge-ops.md)|medium|给客服、助理和产品团队用，适合让助手记住上下文和用户偏好；没定保留期、删除和纠错机制前别随便存用户记忆。|
|[nanobrowser/nanobrowser](https://github.com/nanobrowser/nanobrowser)|[通用企业/内部运营](../industries/general-enterprise.md)<br>[零售/电商/客服密集型](../industries/retail-ecommerce.md)<br>[内容/媒体/营销服务](../industries/content-media.md)|[运营自动化负责人](../roles/operations-automation.md)<br>[开发工程师](../roles/engineering.md)<br>[内容/市场运营负责人](../roles/content-marketing.md)|medium|给一线运营和增长试点团队用，适合验证浏览器扩展形态的 AI 自动化；它依然会碰账号、页面和 API key，别当低风险玩具。|
|[apache/airflow](https://github.com/apache/airflow)|[通用企业/内部运营](../industries/general-enterprise.md)<br>[AI/数据基础设施团队](../industries/ai-infrastructure.md)<br>[专业服务：法律/咨询/研究](../industries/professional-services.md)|[基础设施/运维负责人](../roles/infra-ops.md)<br>[运营自动化负责人](../roles/operations-automation.md)<br>[工作流架构师](../roles/workflow-architecture.md)|medium|给已经有调度体系的企业运维和流程架构团队用，适合把 AI 任务纳入定时和依赖编排；如果只是轻量自动化，别先上重平台。|

## 推荐工作流
- 先把文档格式、权限和知识保留规则定清，再接入整理/记忆/搜索类 Skill。
- 把“谁能看、谁能改、谁能删”写进流程，不要把办公助手当成无边界资料柜。
- 适合从低风险的归档、转换、检索开始，逐步扩到内部协作。

## 风险边界
- 文档和记忆类工具天然会碰到敏感信息，默认按权限隔离管理。
- 格式转换会有信息损失，不能把输出当原件。
- 需要明确 retention、删除和审计机制。
