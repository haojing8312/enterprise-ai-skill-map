# Taxonomy｜分类体系

这份分类不是按“工具炫不炫”来分，而是按企业里 **哪个行业会用、哪个岗位负责、落在哪个流程、风险由谁承担** 来分。

当前主导航从原来的“场景优先”调整为：

```text
行业 industry → 岗位 role → 场景 scenario → Skill → 风险边界 → 工作流组合
```

当前已收录 Skill：34 个。

## 一级：行业 Industry

| ID | 行业 | 当前 Skill | 说明 |
|---|---|---:|---|
| general-enterprise | [通用企业/内部运营](industries/general-enterprise.md) | 18 | 不绑定单一行业，重点在文档、知识库、客服、流程、权限和内部协作。 |
| software-internet | [软件/互联网/研发组织](industries/software-internet.md) | 24 | 研发、测试、DevOps、AI 应用工程、平台工程最先落地的一组场景。 |
| ai-infrastructure | [AI/数据基础设施团队](industries/ai-infrastructure.md) | 16 | 模型服务、推理网关、本地部署、成本治理和工具接入。 |
| content-media | [内容/媒体/营销服务](industries/content-media.md) | 8 | 选题、研究、写作、视觉、分发、复盘，以及内容团队自己的 Skill 库。 |
| consulting-training | [咨询/培训/知识服务](industries/consulting-training.md) | 8 | 把 Skill 变成课程、咨询交付、企业内训、工作坊和方案库。 |
| professional-services | [专业服务：法律/咨询/研究](industries/professional-services.md) | 7 | 合同、资料、报告、尽调、研究支持等高审校要求场景。 |
| government-stateowned | [政企/国企/内网场景](industries/government-stateowned.md) | 2 | 重视内网、权限、审计、国产化/本地化部署和流程留痕。 |
| retail-ecommerce | [零售/电商/客服密集型](industries/retail-ecommerce.md) | 6 | 客服、运营、网页巡检、FAQ、用户记忆和活动支持。 |
| finance-tax | [金融/财税](industries/finance-tax.md) | 0 | 预算、报销、成本、税务材料、金融合规。当前先占位，等待可公开复核样本。 |
| healthcare | [医疗健康](industries/healthcare.md) | 0 | 医疗知识、院内流程、培训、客服、文档辅助。当前先占位，后续必须强化隐私和合规边界。 |
| manufacturing | [制造业](industries/manufacturing.md) | 0 | 工艺文档、设备巡检、质检、培训、售后支持。当前先占位，等待行业流程样本。 |
| education | [教育/培训机构](industries/education.md) | 0 | 课程设计、教案、作业反馈、知识库和培训运营。 |

## 二级：岗位 Role Group

| ID | 岗位组 | 当前 Skill | 说明 |
|---|---|---:|---|
| executive-management | [老板/高管/业务负责人](roles/executive-management.md) | 0 | 看方向、定边界、决定先在哪个流程试点。 |
| strategy-research | [策略/行业研究员](roles/strategy-research.md) | 3 | 负责资料检索、竞品研究、行业分析和决策前材料。 |
| engineering | [开发工程师](roles/engineering.md) | 13 | 读代码、改 bug、写测试、做小范围实现。 |
| engineering-management | [技术负责人/研发效能负责人](roles/engineering-management.md) | 6 | 设计 AI 编码流程、验收标准、代码审查和发布边界。 |
| engineering-platform | [研发平台/GitHub 管理员](roles/engineering-platform.md) | 4 | 负责代码协作平台、Issue/PR 自动化、仓库权限和审计。 |
| qa-testing | [QA/测试负责人](roles/qa-testing.md) | 4 | 网页回归、测试执行、验收检查和质量门禁。 |
| ai-platform | [AI 平台工程师](roles/ai-platform.md) | 11 | 模型服务、网关、推理平台、MCP/Agent 工具接入。 |
| infra-ops | [基础设施/运维负责人](roles/infra-ops.md) | 6 | 内网部署、GPU、边缘设备、系统稳定性和权限隔离。 |
| cost-governance | [成本治理负责人](roles/cost-governance.md) | 5 | 模型调用、GPU 资源、网关计费和成本透明化。 |
| ai-application | [AI 应用工程师](roles/ai-application.md) | 1 | 把 Agent SDK、工具调用和业务流程做成可测试应用。 |
| workflow-architecture | [工作流架构师](roles/workflow-architecture.md) | 12 | 设计多代理交接、状态流转、异常处理和可观察性。 |
| digital-employee-architect | [数字员工架构师](roles/digital-employee-architect.md) | 2 | 从组织能力出发，定义角色、工具、权限、交接和验收。 |
| digital-employee-designer | [数字员工/Skill 设计师](roles/digital-employee-designer.md) | 3 | 把可复用能力包装成可分发、可维护的 Skill 或模板。 |
| content-marketing | [内容/市场运营负责人](roles/content-marketing.md) | 3 | 选题、写作、图文、渠道分发、数据复盘。 |
| content-research | [内容研究助理](roles/content-research.md) | 3 | 为长文、短内容、课程和方案准备材料与出处。 |
| knowledge-ops | [知识库运营](roles/knowledge-ops.md) | 5 | 整理文档、沉淀经验、维护可检索的知识资产。 |
| document-ops | [文档处理专员](roles/document-ops.md) | 1 | 格式转换、资料清洗、文档归档、引用准备。 |
| legal-compliance | [法务/合规负责人](roles/legal-compliance.md) | 2 | 合同、隐私、权限、数据使用和对外表述风险提示。 |
| operations-admin | [运营/行政/流程管理员](roles/operations-admin.md) | 3 | 账号、权限、平台接入、制度、巡检和流程协调。 |
| operations-automation | [运营自动化负责人](roles/operations-automation.md) | 7 | 把网页、后台、表单、报表等重复操作半自动化。 |
| customer-success | [客服/客户成功负责人](roles/customer-success.md) | 1 | FAQ、工单、用户记忆、实施手册和交付复盘。 |
| product-manager | [产品经理](roles/product-manager.md) | 2 | 定义需求、验收口径、用户记忆和体验边界。 |
| solution-delivery | [解决方案/交付架构师](roles/solution-delivery.md) | 0 | 把 Skill 组合成可交付的行业方案、课程或咨询包。 |
| hr-training | [人力/培训运营](roles/hr-training.md) | 0 | 招聘、培训、课程、员工手册和能力评估。 |
| finance-tax | [财务/税务/报销负责人](roles/finance-tax.md) | 0 | 预算、报销、成本和税务材料准备；当前需要更多公开样本。 |
| skill-research | [Skill 观察研究员](roles/skill-research.md) | 4 | 发现、验证、记录外部 Skill 和社区工作流。 |

## 三级：场景 Scenario

场景仍然保留，但不再作为唯一入口。它回答的是“这个岗位在企业流程里具体怎么用”。

| ID | 场景 | 默认边界 |
|---|---|---|
| office | 办公协同 | 先管原文件权限、记忆保留期、谁能看到什么 |
| finance-tax | 财税 | 没有复核链路时，不要让代理直接生成对外承诺或税务结论 |
| legal-compliance | 法务合规 | 只能做辅助整理和提示，不能替代律师或合规负责人拍板 |
| sales-growth | 销售增长 | 不要擅自对客户承诺价格、周期、能力 |
| customer-service | 客服/交付 | 核心风险是记错用户信息、把历史脏数据继续放大 |
| hr-training | 人力/培训 | 涉及候选人和员工数据时，先讲清留存、权限和偏见风险 |
| r-and-d | 研发/产品 | 不要神化为“自己写自己发”，spec、测试、review 还得有人扛 |
| marketing-content | 市场/内容 | 内容类最怕像模板稿，先保留人的判断，再谈批量生成 |
| operations-admin | 行政/运营 | 多数工具都能碰账号、日志、文件，默认按高权限风险管理 |
| industry-solutions | 行业方案 | 没有行业数据和流程细节时，不要空喊“通用解决方案” |

## 收录字段要求

`data/skills.yaml` 中每个条目都要有三组标签：

```yaml
industries: []   # 行业入口，比如 software-internet / content-media
role_groups: []  # 岗位入口，比如 engineering / ai-platform / content-marketing
scenarios: []    # 具体使用场景，比如 r-and-d / office / customer-service
```

## 默认判断

1. 能直接碰文件、仓库、浏览器、密钥的 Skill，默认比“只会写字”的 Skill 风险高一档。
2. 看上去最省人的，不一定最适合先落地；企业更适合先上“有人审、可回滚、可追责”的半自动链路。
3. 内容类 Skill 先看有没有人味和事实核查；平台类 Skill 先看权限和审计；记忆类 Skill 先看 retention 和删除机制。
4. 行业页不等于行业方案。没有真实流程、数据边界和验收角色时，只能写“候选方向”，不能写成完整解决方案。
