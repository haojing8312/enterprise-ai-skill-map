# Skill 类型目录

这个页面参考 `awesome-claude-skills` 的“先看目录，再进细项”方式：先让读者知道仓库里有哪些 Skill 类型，再按业务路线或单个卡片深入。

> 口径：这里按“使用场景 / 能力类型”分组，不按内部 taxonomy。一个 Skill 只放到最主要的一类，避免目录膨胀。

## 1. AI 编码与研发流程（5 个）

适合：研发负责人、AI 编码流程设计者、测试负责人。

| Skill | 用途 | 风险提示 |
|---|---|---|
| [obra/superpowers](https://github.com/obra/superpowers) | 把 spec、测试、验收前置到 AI 编码流程 | 流程样本，不是万能自治员工 |
| [openai/codex](https://github.com/openai/codex) | 终端式 coding agent，读仓库、修 bug、补测试 | 需要评审与测试，不能直连生产 |
| [anomalyco/opencode](https://github.com/anomalyco/opencode) | 开源 AI 编码底座，可二次开发 | 需要沙箱、权限和回滚机制 |
| [google-gemini/gemini-cli](https://github.com/google-gemini/gemini-cli) | 大厂 CLI agent 的终端工作流样本 | 终端能力不等于审批权 |
| [mattpocock/skills](https://github.com/mattpocock/skills) | 工程团队如何组织可复用 skills 的样本 | 公开样本需裁剪后再进企业流程 |

## 2. Agent / 多智能体编排（5 个）

适合：数字员工架构师、工作流设计者、AI 应用工程师。

| Skill | 用途 | 风险提示 |
|---|---|---|
| [openai/openai-agents-python](https://github.com/openai/openai-agents-python) | 多角色 agent、handoff、工具调用 SDK | SDK 不是完整业务系统 |
| [revfactory/harness](https://github.com/revfactory/harness) | 岗位型 agent 团队和 skill 包设计样本 | 仍需人工定义边界和验收 |
| [spring-ai-community/spring-ai-agent-utils](https://github.com/spring-ai-community/spring-ai-agent-utils) | Java / Spring 体系的 agent 工具层封装 | 企业应用接入前要安全评审 |
| [triggerdotdev/trigger.dev](https://github.com/triggerdotdev/trigger.dev) | 长任务、事件驱动、AI workflow 编排 | secret 管理和失败补偿要先设计 |
| [apache/airflow](https://github.com/apache/airflow) | 定时、依赖、跨系统调度底座 | 对个人轻量自动化可能过重 |

## 3. MCP / 工具连接器（6 个）

适合：AI 平台、系统集成、数字员工连接层负责人。

| Skill | 用途 | 风险提示 |
|---|---|---|
| [modelcontextprotocol/servers](https://github.com/modelcontextprotocol/servers) | 官方 MCP server 参考目录 | 每个 server 的权限边界不同 |
| [github/github-mcp-server](https://github.com/github/github-mcp-server) | GitHub issue、PR、repo context 接入 | token scope 和写权限必须收紧 |
| [punkpeye/awesome-mcp-servers](https://github.com/punkpeye/awesome-mcp-servers) | MCP 生态长名单索引 | 目录不等于生产可用背书 |
| [PrefectHQ/fastmcp](https://github.com/PrefectHQ/fastmcp) | Python MCP server/client 工程底座 | 工具层连内网资源时要做认证审计 |
| [googleapis/mcp-toolbox](https://github.com/googleapis/mcp-toolbox) | 数据库工具通过 MCP 接入 IDE / agent | 谁能查、谁能写必须分层 |
| [GLips/Figma-Context-MCP](https://github.com/GLips/Figma-Context-MCP) | Figma 设计稿上下文接入编码流程 | 私有设计资产和访问凭证不能外放 |

## 4. 浏览器自动化 / 网页采集（5 个）

适合：运营自动化、QA、增长团队、公开数据采集团队。

| Skill | 用途 | 风险提示 |
|---|---|---|
| [microsoft/playwright-mcp](https://github.com/microsoft/playwright-mcp) | 真实打开页面做 QA、回归和流程检查 | 自动点击可能触发真实动作 |
| [browser-use/browser-use](https://github.com/browser-use/browser-use) | 网页采集、表单流转、登录后操作 | 生产账号、Cookie、页面数据需隔离 |
| [apify/crawlee](https://github.com/apify/crawlee) | JS 体系网页采集、站点监测、RAG 原料 | 不能越过 robots、条款和隐私边界 |
| [apify/crawlee-python](https://github.com/apify/crawlee-python) | Python 体系公开网页采集和浏览器执行 | 登录态和受限页面要先补审计 |
| [nanobrowser/nanobrowser](https://github.com/nanobrowser/nanobrowser) | 浏览器扩展形态的前台自动化 | 仍会接触账号、页面和 API key |

## 5. 内容研究 / 知识库 / 文档处理（5 个）

适合：研究员、内容团队、知识库运营、培训方案设计者。

| Skill | 用途 | 风险提示 |
|---|---|---|
| [langchain-ai/open_deep_research](https://github.com/langchain-ai/open_deep_research) | 资料检索、出处整理、研究初稿 | 不能跳过引用核查直接对外发布 |
| [microsoft/markitdown](https://github.com/microsoft/markitdown) | Office / PDF 转 Markdown，知识入库前清洗 | 转换稿不能当原件，敏感文件仍需脱敏 |
| [alirezarezvani/claude-skills](https://github.com/alirezarezvani/claude-skills) | 企业 skill library 分层与角色包样本 | 不要整仓照搬进企业上下文 |
| [K-Dense-AI/scientific-agent-skills](https://github.com/K-Dense-AI/scientific-agent-skills) | 垂直专业领域 skill 库组织样本 | 专业结论需要专家复核 |
| [JimLiu/baoyu-skills](https://github.com/JimLiu/baoyu-skills) | 内容型 skill packaging 观察样本 | 许可边界未清，当前只做观察，不建议商用复用 |

## 6. 出海营销 / 内容增长（5 个）

适合：出海公司、内容增长、营销 Ops、个人 IP / Newsletter 运营。

| Skill | 用途 | 风险提示 |
|---|---|---|
| [n8n](../skills/n8n.md) | 表单、CRM、邮件、提醒、报表流程编排 | 对外触达必须有人审规则和频率 |
| [Activepieces](../skills/activepieces.md) | 开源自动化连接层，适合 AI + SaaS 联动 | 客户名单、审批流、发布流要留人工节点 |
| [RSSHub](../skills/rsshub.md) | 公开信号订阅、竞品动态、趋势监控 | 公开订阅不等于可二次分发 |
| [Ghost](../skills/ghost.md) | 内容发布、订阅、newsletter、会员 | 标题、CTA、价格信息要编辑复核 |
| [Plausible Analytics](../skills/plausible-analytics.md) | 内容、落地页、newsletter 的访问与转化复盘 | 数据只辅助判断，归因口径要人工定 |

## 7. 模型基础设施 / 网关（4 个）

适合：AI 平台、推理服务、成本治理和模型网关负责人。

| Skill | 用途 | 风险提示 |
|---|---|---|
| [ggml-org/llama.cpp](https://github.com/ggml-org/llama.cpp) | 本地推理、边缘部署、内网验证 | 代码许可不等于模型权利也开放 |
| [vllm-project/vllm](https://github.com/vllm-project/vllm) | 高吞吐模型服务和 OpenAI-compatible API | 需要 GPU、运维和模型许可评估 |
| [BerriAI/litellm](https://github.com/BerriAI/litellm) | 多模型 provider 路由、日志、预算 | 密钥更集中，权限和审计要更严 |
| [tensorzero/tensorzero](https://github.com/tensorzero/tensorzero) | LLM gateway、观测、评估与优化 | 中心化之后治理责任更重 |

## 8. 企业 AI 治理 / 观测 / 安全（4 个）

适合：LLMOps、AI 平台治理、安全负责人、客服/助理产品经理。

| Skill | 用途 | 风险提示 |
|---|---|---|
| [mem0ai/mem0](https://github.com/mem0ai/mem0) | agent 记忆、用户偏好和上下文保持 | 长期记忆涉及 PII、保留期和删除机制 |
| [openlit/openlit](https://github.com/openlit/openlit) | LLM observability、trace、成本监控 | prompt、trace、调用数据要脱敏和留存管理 |
| [mlflow/mlflow](https://github.com/mlflow/mlflow) | 实验、评估、监控、治理平台 | 平台装好不代表评估口径自然存在 |
| [casdoor/casdoor](https://github.com/casdoor/casdoor) | agent-first IAM / gateway 身份访问控制 | IAM 配错影响面大，需分阶段接入 |

## 怎么继续找

- 按业务目标找：回到 [`tracks/`](../tracks/)
- 按外部应用找：看 [`app-automations/`](../app-automations/)
- 看结构化数据源：[`data/skills.yaml`](../data/skills.yaml)
