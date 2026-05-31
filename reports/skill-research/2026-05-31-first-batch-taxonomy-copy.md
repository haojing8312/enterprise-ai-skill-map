# 2026-05-31 首批 Skill taxonomy 与企业推荐语

## 结论
- 本批共看 34 条候选：verified_public 33 条，blocked 1 条。
- 行业和岗位 taxonomy 这轮先不扩。现有 industry / role_group 足够把首批样本装进去，盲目加类目只会把导航做散。
- 真缺口在 scenario 层。建议下一轮补两个候选场景：`identity-access`（身份、权限、token、目录接入）和 `observability-evaluation`（trace、评测、成本、回放）。
- `finance-tax`、`healthcare`、`manufacturing`、`education` 继续保留行业占位，但当前还没有够硬的公开样本，不建议先写成可卖方案。

## 这轮怎么分
- industry：站在老板或业务线视角，看这类 Skill 最先会在哪种组织里落地。
- role_group：看谁真正负责接、管、验收，不按“谁会用一下”乱贴。
- scenario：看首个可落地流程，而不是功能名。
- copy：统一写成“谁该用、解决什么具体问题、边界在哪”。

## 分类面板

### 行业覆盖（verified_public）
| 行业 | 条数 |
|---|---:|
| 软件/互联网/研发组织 | 24 |
| 通用企业/内部运营 | 18 |
| AI/数据基础设施团队 | 16 |
| 咨询/培训/知识服务 | 8 |
| 内容/媒体/营销服务 | 8 |
| 专业服务：法律/咨询/研究 | 7 |
| 零售/电商/客服密集型 | 6 |
| 政企/国企/内网场景 | 2 |

### 岗位覆盖（Top 10）
| 岗位 | 条数 |
|---|---:|
| 开发工程师 | 13 |
| 工作流架构师 | 12 |
| AI 平台工程师 | 11 |
| 运营自动化负责人 | 7 |
| 技术负责人/研发效能负责人 | 6 |
| 基础设施/运维负责人 | 6 |
| 成本治理负责人 | 5 |
| 知识库运营 | 5 |
| QA/测试负责人 | 4 |
| 研发平台/GitHub 管理员 | 4 |

### 场景覆盖（verified_public）
| 场景 | 条数 |
|---|---:|
| 研发/产品 | 27 |
| 行政/运营 | 25 |
| 办公协同 | 11 |
| 市场/内容 | 10 |
| 客服/交付 | 4 |
| 法务合规 | 1 |

## taxonomy 缺口判断
1. 暂不新增行业。现在新增行业只会把“样本稀薄”伪装成“版图很大”。四个占位行业先留空比乱塞更诚实。
2. 暂不新增岗位。像设计协作、IAM、安全治理都只出现了 1–2 个样本，还不够独立成稳定岗位入口。
3. 建议下一轮优先补 scenario，而不是补行业：
   - `identity-access`：casdoor、github-mcp-server、mcp-servers、mcp-toolbox 现在被分散到 operations-admin / office / r-and-d，读起来不够准。
   - `observability-evaluation`：openlit、mlflow、tensorzero、litellm、trigger.dev 都在讲 trace、评测、成本和回放，继续塞进 r-and-d 会把“治理”这一层埋掉。
4. `industry-solutions` 先保留轻用法。现在它更适合放在报告和咨询包装里，不适合回填到太多单体 Skill。

## 34 条候选的分类与推荐语

### 一、编码与 agent 开发

- obra/superpowers（verified_public）
  - industry: 软件/互联网/研发组织 / 咨询/培训/知识服务
  - role_group: 技术负责人/研发效能负责人 / 开发工程师 / 工作流架构师
  - scenario: 研发/产品 / 行政/运营
  - 推荐语: 给技术负责人和 AI 编码流程设计者用，适合把 spec、测试、验收提前到写码前面；前提是团队本来就愿意做评审和回滚。

- openai/codex（verified_public）
  - industry: 软件/互联网/研发组织
  - role_group: 开发工程师 / 技术负责人/研发效能负责人 / QA/测试负责人
  - scenario: 研发/产品
  - 推荐语: 给会看代码的开发和测试负责人用，适合读仓库、修小 bug、补测试；别拿它跳过评审直接动生产。

- anomalyco/opencode（verified_public）
  - industry: 软件/互联网/研发组织 / AI/数据基础设施团队
  - role_group: 开发工程师 / 研发平台/GitHub 管理员 / 技术负责人/研发效能负责人
  - scenario: 研发/产品
  - 推荐语: 给想自建开源 AI 编码底座的研发团队用，适合做可二次开发的 coding agent 流程；没有沙箱和权限控制时别往生产环境放。

- github/github-mcp-server（verified_public）
  - industry: 软件/互联网/研发组织
  - role_group: 研发平台/GitHub 管理员 / 运营/行政/流程管理员 / 技术负责人/研发效能负责人
  - scenario: 研发/产品 / 行政/运营
  - 推荐语: 给 GitHub 为核心的研发平台团队用，适合把 issue、PR、review 接进数字员工流程；token scope 和写权限不清时先别自动化。

- openai/openai-agents-python（verified_public）
  - industry: 软件/互联网/研发组织 / AI/数据基础设施团队 / 咨询/培训/知识服务
  - role_group: AI 应用工程师 / 工作流架构师 / 数字员工架构师
  - scenario: 研发/产品 / 行政/运营
  - 推荐语: 给要自己编排多角色代理的产品和工程团队用，适合做 handoff 和工具调用原型；它是 SDK，不是现成业务系统。

- google-gemini/gemini-cli（verified_public）
  - industry: 软件/互联网/研发组织 / 通用企业/内部运营
  - role_group: 开发工程师 / 技术负责人/研发效能负责人 / 知识库运营
  - scenario: 研发/产品 / 办公协同
  - 推荐语: 给想比较不同 CLI agent 的研发和知识工作团队用，适合放进终端工作流试用；终端能执行命令，不等于它有审批权。

- spring-ai-community/spring-ai-agent-utils（verified_public）
  - industry: 软件/互联网/研发组织 / AI/数据基础设施团队 / 专业服务：法律/咨询/研究
  - role_group: 开发工程师 / 研发平台/GitHub 管理员 / 工作流架构师
  - scenario: 研发/产品 / 行政/运营
  - 推荐语: 给 Java、Spring 团队用，适合把 skill、tool、handoff 封装进企业应用；没有安全评审前别把工具接口直接暴露出去。

- PrefectHQ/fastmcp（verified_public）
  - industry: 软件/互联网/研发组织 / AI/数据基础设施团队 / 专业服务：法律/咨询/研究
  - role_group: 开发工程师 / AI 平台工程师 / 工作流架构师
  - scenario: 研发/产品 / 行政/运营
  - 推荐语: 给 Python 团队用，适合把 MCP server、client 从 demo 做成可维护工程；工具层能连内网资源时，权限设计要先行。

- GLips/Figma-Context-MCP（verified_public）
  - industry: 软件/互联网/研发组织 / 专业服务：法律/咨询/研究
  - role_group: 数字员工/Skill 设计师 / 产品经理 / 开发工程师
  - scenario: 研发/产品 / 市场/内容
  - 推荐语: 给产品、设计系统和前端协作团队用，适合把设计稿上下文接到编码流程里；私有设计资产和 token 不能默认外放。

### 二、模型服务、接入与平台治理

- ggml-org/llama.cpp（verified_public）
  - industry: AI/数据基础设施团队 / 政企/国企/内网场景 / 软件/互联网/研发组织
  - role_group: AI 平台工程师 / 基础设施/运维负责人
  - scenario: 研发/产品 / 行政/运营
  - 推荐语: 给内网或成本敏感的 AI 平台团队用，适合先把模型跑在自己机器上验证可行性；它解决推理，不替你解决业务流程和模型许可。

- vllm-project/vllm（verified_public）
  - industry: AI/数据基础设施团队 / 软件/互联网/研发组织
  - role_group: AI 平台工程师 / 基础设施/运维负责人 / 成本治理负责人
  - scenario: 研发/产品 / 行政/运营
  - 推荐语: 给多模型和高吞吐场景的 AI 平台、运维团队用，适合统一推理服务和看 GPU 利用率；没有运维能力时别把它当一键托管平台。

- modelcontextprotocol/servers（verified_public）
  - industry: 通用企业/内部运营 / 软件/互联网/研发组织 / AI/数据基础设施团队
  - role_group: AI 平台工程师 / 数字员工架构师 / 运营/行政/流程管理员
  - scenario: 研发/产品 / 办公协同 / 行政/运营
  - 推荐语: 给数字员工架构师和 AI 平台团队用，适合梳理文件、浏览器、GitHub 这类工具接入；每接一个 server 都要单独收权限。

- BerriAI/litellm（verified_public）
  - industry: AI/数据基础设施团队 / 软件/互联网/研发组织
  - role_group: AI 平台工程师 / 成本治理负责人 / 基础设施/运维负责人
  - scenario: 研发/产品 / 行政/运营
  - 推荐语: 给多模型接入的 AI 平台团队用，适合统一路由、日志和预算；密钥会更集中，所以权限和审计要更严。

- googleapis/mcp-toolbox（verified_public）
  - industry: 通用企业/内部运营 / AI/数据基础设施团队 / 软件/互联网/研发组织
  - role_group: AI 平台工程师 / 运营/行政/流程管理员 / 工作流架构师
  - scenario: 行政/运营 / 办公协同 / 研发/产品
  - 推荐语: 给要把数据库接进 AI 助手的开发和分析团队用，适合做查询、发现和 schema 理解；谁能查、谁能写，必须先分层。

- casdoor/casdoor（verified_public）
  - industry: 通用企业/内部运营 / AI/数据基础设施团队 / 政企/国企/内网场景
  - role_group: AI 平台工程师 / 法务/合规负责人 / 基础设施/运维负责人
  - scenario: 行政/运营 / 办公协同 / 客服/交付
  - 推荐语: 给做统一身份认证的 AI 平台团队用，适合补齐数字员工接入后的 IAM 视角；组织、角色、权限模型没梳清前别急着上。

- openlit/openlit（verified_public）
  - industry: AI/数据基础设施团队 / 通用企业/内部运营 / 软件/互联网/研发组织
  - role_group: AI 平台工程师 / 基础设施/运维负责人 / 成本治理负责人
  - scenario: 行政/运营 / 研发/产品
  - 推荐语: 给 AI 平台和成本治理团队用，适合看调用链路、日志和花费；只有看板没有治理动作，观测价值会很快打折。

- mlflow/mlflow（verified_public）
  - industry: AI/数据基础设施团队 / 软件/互联网/研发组织 / 通用企业/内部运营
  - role_group: AI 平台工程师 / 成本治理负责人 / 策略/行业研究员
  - scenario: 研发/产品 / 行政/运营
  - 推荐语: 给做模型、agent 实验和评估的团队用，适合把实验记录、指标和治理放到同一条交付链路；平台装好了，不代表评估口径自然就有。

- tensorzero/tensorzero（verified_public）
  - industry: AI/数据基础设施团队 / 软件/互联网/研发组织 / 通用企业/内部运营
  - role_group: AI 平台工程师 / 成本治理负责人 / 工作流架构师
  - scenario: 研发/产品 / 行政/运营
  - 推荐语: 给想把模型调用、评估和优化放进一套平台的 AI 团队用，适合做 LLMOps 底座；中心化之后治理责任更重，别只看功能不看权限。

### 三、浏览器执行与网页采集

- microsoft/playwright-mcp（verified_public）
  - industry: 软件/互联网/研发组织 / 零售/电商/客服密集型 / 内容/媒体/营销服务
  - role_group: QA/测试负责人 / 运营自动化负责人 / 开发工程师
  - scenario: 研发/产品 / 市场/内容 / 行政/运营
  - 推荐语: 给 QA 和网页运营自动化团队用，适合真实打开页面做回归和流程检查；凡是会点到真系统的动作都要隔离账号、保留审批。

- browser-use/browser-use（verified_public）
  - industry: 软件/互联网/研发组织 / 零售/电商/客服密集型 / 通用企业/内部运营
  - role_group: 运营自动化负责人 / 开发工程师 / QA/测试负责人
  - scenario: 行政/运营 / 市场/内容 / 客服/交付
  - 推荐语: 给网页流程自动化团队用，适合做采集、登录后操作和表单流转；生产账号、Cookie 和页面数据必须单独隔离。

- apify/crawlee（verified_public）
  - industry: 零售/电商/客服密集型 / 通用企业/内部运营 / 内容/媒体/营销服务
  - role_group: 运营自动化负责人 / 开发工程师 / 内容研究助理
  - scenario: 行政/运营 / 市场/内容 / 客服/交付
  - 推荐语: 给采集和站点监测团队用，适合抓公开网页、盯页面变化、给 RAG 准备原料；robots、条款和隐私边界不能越。

- apify/crawlee-python（verified_public）
  - industry: 零售/电商/客服密集型 / 通用企业/内部运营 / 内容/媒体/营销服务
  - role_group: 运营自动化负责人 / 开发工程师 / 内容研究助理
  - scenario: 行政/运营 / 市场/内容 / 研发/产品
  - 推荐语: 给 Python 技术栈的采集团队用，适合做公开网页抓取和浏览器执行；碰登录态或受限页面时要先补审计和权限。

- nanobrowser/nanobrowser（verified_public）
  - industry: 通用企业/内部运营 / 零售/电商/客服密集型 / 内容/媒体/营销服务
  - role_group: 运营自动化负责人 / 开发工程师 / 内容/市场运营负责人
  - scenario: 行政/运营 / 市场/内容 / 办公协同
  - 推荐语: 给一线运营和增长试点团队用，适合验证浏览器扩展形态的 AI 自动化；它依然会碰账号、页面和 API key，别当低风险玩具。

### 四、文档、研究与知识记忆

- langchain-ai/open_deep_research（verified_public）
  - industry: 通用企业/内部运营 / 内容/媒体/营销服务 / 咨询/培训/知识服务 / 专业服务：法律/咨询/研究
  - role_group: 策略/行业研究员 / 内容研究助理 / 内容/市场运营负责人
  - scenario: 研发/产品 / 市场/内容
  - 推荐语: 给研究员和内容团队用，适合先把资料、出处、分歧拉出来；核查没做完前别直接变成可发结论。

- microsoft/markitdown（verified_public）
  - industry: 通用企业/内部运营 / 专业服务：法律/咨询/研究 / 内容/媒体/营销服务
  - role_group: 文档处理专员 / 知识库运营 / 法务/合规负责人
  - scenario: 办公协同 / 市场/内容 / 法务合规
  - 推荐语: 给知识库和文档处理团队用，适合把 PDF、PPT、Word 先转成能喂给 AI 的文本；转换稿不能当原件，敏感文件照样要脱敏。

- mem0ai/mem0（verified_public）
  - industry: 通用企业/内部运营 / 零售/电商/客服密集型
  - role_group: 客服/客户成功负责人 / 产品经理 / 知识库运营
  - scenario: 办公协同 / 客服/交付 / 行政/运营
  - 推荐语: 给客服、助理和产品团队用，适合让助手记住上下文和用户偏好；没定保留期、删除和纠错机制前别随便存用户记忆。

- K-Dense-AI/scientific-agent-skills（verified_public）
  - industry: 专业服务：法律/咨询/研究 / 咨询/培训/知识服务 / 软件/互联网/研发组织
  - role_group: 策略/行业研究员 / Skill 观察研究员 / 知识库运营
  - scenario: 研发/产品 / 办公协同
  - 推荐语: 给做垂直知识库或培训方案的人用，适合研究专业领域 skill 怎么围绕数据源组织；专业结论仍要让行业专家复核。

### 五、Skill 库、生态目录与方案包装

- alirezarezvani/claude-skills（verified_public）
  - industry: 通用企业/内部运营 / 内容/媒体/营销服务 / 咨询/培训/知识服务
  - role_group: 知识库运营 / 数字员工/Skill 设计师 / 工作流架构师
  - scenario: 研发/产品 / 市场/内容 / 行政/运营
  - 推荐语: 给搭内部 skill 库的人用，适合研究 skill 怎么分层和分发；不要整仓照搬，不然上下文和维护成本一起失控。

- mattpocock/skills（verified_public）
  - industry: 软件/互联网/研发组织 / 咨询/培训/知识服务
  - role_group: 开发工程师 / QA/测试负责人 / 工作流架构师
  - scenario: 研发/产品
  - 推荐语: 给工程团队搭 skills 模板库用，适合看什么 skill 真会被开发者反复调用；公开样本要先裁剪，再变成企业标准。

- revfactory/harness（verified_public）
  - industry: 软件/互联网/研发组织 / 咨询/培训/知识服务
  - role_group: 技术负责人/研发效能负责人 / 工作流架构师 / Skill 观察研究员
  - scenario: 研发/产品 / 办公协同
  - 推荐语: 给咨询交付和数字员工设计团队用，适合把一个岗位拆成 agent 团队加 skill 包；它更像方法样本，不是接上就能上岗的员工。

- punkpeye/awesome-mcp-servers（verified_public）
  - industry: 通用企业/内部运营 / AI/数据基础设施团队 / 软件/互联网/研发组织
  - role_group: AI 平台工程师 / 工作流架构师 / Skill 观察研究员
  - scenario: 研发/产品 / 行政/运营 / 办公协同
  - 推荐语: 给做选型长名单的人用，适合快速摸清 MCP 生态里有哪些连接器；它是目录，不是生产可用清单。

### 六、编排与后台任务

- apache/airflow（verified_public）
  - industry: 通用企业/内部运营 / AI/数据基础设施团队 / 专业服务：法律/咨询/研究
  - role_group: 基础设施/运维负责人 / 运营自动化负责人 / 工作流架构师
  - scenario: 行政/运营 / 办公协同 / 研发/产品
  - 推荐语: 给已经有调度体系的企业运维和流程架构团队用，适合把 AI 任务纳入定时和依赖编排；如果只是轻量自动化，别先上重平台。

- triggerdotdev/trigger.dev（verified_public）
  - industry: 软件/互联网/研发组织 / AI/数据基础设施团队 / 通用企业/内部运营
  - role_group: 研发平台/GitHub 管理员 / 运营自动化负责人 / 工作流架构师
  - scenario: 行政/运营 / 研发/产品
  - 推荐语: 给做长任务和事件驱动产品的团队用，适合追踪 AI workflow 和后台任务；secret 管理和失败补偿没设计好时别急着接业务系统。

### 七、暂不入库，只保留观察位

- JimLiu/baoyu-skills（blocked）
  - industry: 内容/媒体/营销服务 / 咨询/培训/知识服务
  - role_group: 内容/市场运营负责人 / Skill 观察研究员 / 数字员工/Skill 设计师
  - scenario: 市场/内容 / 行政/运营
  - 推荐语: 给内容型 skill 设计观察用，适合研究 packaging 写法；许可没讲清前不要进企业库，也别对外分发。

## 对 data/skills.yaml 的处理
- 已为全部 34 条条目补 `copy` 字段，写法统一为一句人话推荐语。
- `copy` 不替代 `value_summary`：前者给老板和岗位负责人快速判断，后者保留更完整的说明口径。
- 若后续正式引入 `identity-access` / `observability-evaluation` 两个 scenario，再统一回填到相关条目。

## 给内容团队的使用建议
- 对外写推荐时，先说岗位和问题，再说工具名字。
- 遇到“会写、会爬、会点、会接库、会记忆”的 Skill，边界要写在同一句里，不要放到脚注。
- 对 blocked / watchlist 条目，宁可写“先观察”，也不要包装成可直接商用。
