# 2026-05-31 首批 Skill 候选验证与结构化结果

## 结论
- Verified Public：33 条（沿用已验证基线 14 条，本轮新增 19 条）。
- Blocked：3 条。
- Watchlist：6 条。
- 已回填 `data/skills.yaml` 中现有条目的 `source_url` / `verification_status`，并追加首批新增卡片，可直接合并使用。

## 验证规则
- 只保留公开、可复核、MIT/Apache 或边界明确的首批条目。
- License 不清、README 过于空泛、或安全/数据边界不明的条目不进入首批 Verified Public。
- 不把“AI 自治”夸大成事实；所有可执行/可接入项目均按“需权限、需审计、需人工验收”处理。

## Verified Public（沿用已验证基线）
### obra/superpowers
- repo/url: https://github.com/obra/superpowers
- 简介: 如果团队已经在用 AI 写码，但总要靠人最后收烂摊子，可以先看它怎么把 spec、测试、验收往前放。它更像流程样本，不是万能外挂。
- 核心能力: planning, testing, debugging, acceptance-review
- 安装/使用入口: 仓库 README / 官方 docs
- license: MIT
- 维护活跃度: 公开仓库，MIT 协议
- 企业可用场景: 研发团队建立 AI 编码工作流；数字员工任务分解与验收
- 安全风险: 不能夸大为全自动自治
- 推荐等级: B
- 证据链接: https://github.com/obra/superpowers

### openai/codex
- repo/url: https://github.com/openai/codex
- 简介: 适合给会看代码的人提速：读仓库、修小 bug、跑命令都顺手，但前提是有人审、有人测。
- 核心能力: planning, code-generation, debugging, terminal-execution, code-review
- 安装/使用入口: 仓库 README / 官方 docs
- license: Apache-2.0
- 维护活跃度: 公开 GitHub 仓库，Apache-2.0；2026-05-31 GitHub API 显示 87,167 stars，README 描述为 terminal coding agent。
- 企业可用场景: 研发团队做 bugfix、代码审阅、仓库导航；把 AI 编码能力纳入有人审的交付链路
- 安全风险: 会执行终端命令，若权限边界没控好可能误改代码或读取敏感文件；生成代码仍需人工测试与审阅
- 推荐等级: A
- 证据链接: https://github.com/openai/codex

### anomalyco/opencode
- repo/url: https://github.com/anomalyco/opencode
- 简介: 想自己掌控 AI 编码流程，而不是全押某个闭源产品，可以拿它做开源底座。别把“能改代码”理解成“能自己交付”。
- 核心能力: planning, code-generation, debugging, agent-workflow, terminal-execution
- 安装/使用入口: 仓库 README / 官方 docs
- license: MIT
- 维护活跃度: 公开 GitHub 仓库，MIT；2026-05-31 GitHub API 显示 167,573 stars，官网为 opencode.ai。
- 企业可用场景: 想搭建可二次开发的 AI 编码流程；研究开源 coding agent 的企业接入方式
- 安全风险: 同样具备执行命令和改仓库能力，需要沙箱与审批边界；开源可扩展性强，但也意味着接入方要自担运维和安全设计
- 推荐等级: A
- 证据链接: https://github.com/anomalyco/opencode

### ggml-org/llama.cpp
- repo/url: https://github.com/ggml-org/llama.cpp
- 简介: 如果场景出不了网，或者想先把模型跑在自己机器上，它是个靠谱底座。但它解决的是推理，不是业务流程。
- 核心能力: local-inference, model-serving, quantization, edge-deployment
- 安装/使用入口: 仓库 README / 官方 docs
- license: MIT
- 维护活跃度: 公开 GitHub 仓库，MIT；2026-05-31 GitHub API 显示 113,893 stars，README 描述为 C/C++ LLM inference。
- 企业可用场景: 内网环境或成本敏感场景做本地模型验证；把模型推理能力嵌入私有工具链
- 安全风险: 仓库代码是 MIT，但模型权利仍取决于各模型许可证；本地部署会引入硬件、性能和维护成本
- 推荐等级: A-
- 证据链接: https://github.com/ggml-org/llama.cpp

### vllm-project/vllm
- repo/url: https://github.com/vllm-project/vllm
- 简介: 当团队开始同时接多模型、看吞吐和成本时，再考虑它更合适。别把它当成一键省心的 SaaS。
- 核心能力: high-throughput-serving, model-serving, inference-optimization, openai-compatible-api
- 安装/使用入口: 仓库 README / 官方 docs
- license: Apache-2.0
- 维护活跃度: 公开 GitHub 仓库，Apache-2.0；2026-05-31 GitHub API 显示 81,458 stars，主页为 vllm.ai。
- 企业可用场景: 多模型统一服务层；GPU 资源利用率和吞吐要求高的团队
- 安全风险: 需要 GPU/推理基础设施，实施门槛高于通用 SaaS；模型可用性与合规性不由 vLLM 仓库本身背书
- 推荐等级: A
- 证据链接: https://github.com/vllm-project/vllm

### modelcontextprotocol/servers
- repo/url: https://github.com/modelcontextprotocol/servers
- 简介: 它的价值不是“更聪明”，而是把文件、浏览器、GitHub 这些工具接进来，让数字员工真的能干活。前提是权限要一项一项收紧。
- 核心能力: tool-integration, system-connectors, agent-extensions, protocol-reference
- 安装/使用入口: 仓库 README / 官方 docs
- license: Apache-2.0 / MIT legacy / docs CC-BY-4.0
- 维护活跃度: 公开 GitHub 仓库；2026-05-31 GitHub API 显示 86,494 stars，LICENSE 首段明确处于 MIT→Apache-2.0 迁移期，文档为 CC-BY-4.0。
- 企业可用场景: 梳理企业工具接入清单；为数字员工补浏览器、文件、GitHub 等外部工具接口
- 安全风险: 不同 server 能触达不同系统，安全边界取决于具体接入项；LICENSE 正在从 MIT 过渡到 Apache-2.0，需要记录复合许可边界
- 推荐等级: A-
- 证据链接: https://github.com/modelcontextprotocol/servers

### github/github-mcp-server
- repo/url: https://github.com/github/github-mcp-server
- 简介: 如果团队已经把 issue、PR、review 都放在 GitHub，这个 server 很适合接给开发型数字员工。先管好 token，再谈自动化。
- 核心能力: github-integration, issue-pr-ops, repo-context, agent-tooling
- 安装/使用入口: 仓库 README / 官方 docs
- license: MIT
- 维护活跃度: 公开 GitHub 仓库，MIT；2026-05-31 GitHub API 显示 30,299 stars，README 描述为 GitHub official MCP server。
- 企业可用场景: 研发协作自动化；代码库与工单系统一体化
- 安全风险: 风险主要集中在 GitHub token scope 和写权限控制；需要明确哪些代理只能读、哪些代理能写或发评论
- 推荐等级: B+
- 证据链接: https://github.com/github/github-mcp-server

### microsoft/playwright-mcp
- repo/url: https://github.com/microsoft/playwright-mcp
- 简介: 凡是需要“真的打开网页点一遍”的场景，它比纯文本 agent 靠谱。但它点的是真系统，所以账号隔离和审批不能省。
- 核心能力: browser-automation, web-testing, ui-regression, agent-tooling
- 安装/使用入口: 仓库 README / 官方 docs
- license: Apache-2.0
- 维护活跃度: 公开 GitHub 仓库，Apache-2.0；2026-05-31 GitHub API 显示 33,246 stars，npm 包名为 @playwright/mcp。
- 企业可用场景: 网页回归测试与可视化 QA；需要浏览器执行能力的数字员工
- 安全风险: 浏览器会接触会话、Cookie、后台页面，必须隔离凭证与账号；自动点击可能触发真实外部动作，需要审批边界
- 推荐等级: B+
- 证据链接: https://github.com/microsoft/playwright-mcp

### alirezarezvani/claude-skills
- repo/url: https://github.com/alirezarezvani/claude-skills
- 简介: 适合拿来研究企业内部 skill 库怎么分层、怎么裁剪。别整仓搬进来，不然上下文很快失控。
- 核心能力: skill-library, agent-prompts, workflow-templates, role-packaging
- 安装/使用入口: 仓库 README / 官方 docs
- license: MIT
- 维护活跃度: 公开 GitHub 仓库，MIT；2026-05-31 GitHub API 显示 16,646 stars，README 声称覆盖 300+ skills/agents/plugins。
- 企业可用场景: 搭建企业内部 skill library；给不同代理角色分发可复用技能包
- 安全风险: 社区 skill 质量参差，需要二次验证和删改；一次性装太多 skill 会明显增加上下文负担
- 推荐等级: B+
- 证据链接: https://github.com/alirezarezvani/claude-skills

### langchain-ai/open_deep_research
- repo/url: https://github.com/langchain-ai/open_deep_research
- 简介: 需要先把资料捞全、把出处和分歧摆出来时，它很有用。别让它跳过核查直接变成可发观点。
- 核心能力: deep-research, source-synthesis, web-retrieval, report-drafting
- 安装/使用入口: 仓库 README / 官方 docs
- license: MIT
- 维护活跃度: 公开 GitHub 仓库，MIT；2026-05-31 GitHub API 显示 11,535 stars，由 langchain-ai 维护。
- 企业可用场景: 行业研究、竞品研究、内容资料初稿；给研究型数字员工提供基线 workflow
- 安全风险: 研究链路可能继承网页噪音与错误引用，需要事实核验；更适合作为研究初稿引擎，不是最终审校者
- 推荐等级: B+
- 证据链接: https://github.com/langchain-ai/open_deep_research

### openai/openai-agents-python
- repo/url: https://github.com/openai/openai-agents-python
- 简介: 适合自己搭一套有人设、有交接、有工具调用的数字员工原型。它是 SDK，不是现成业务系统。
- 核心能力: multi-agent-workflow, handoffs, tool-calling, workflow-sdk
- 安装/使用入口: 仓库 README / 官方 docs
- license: MIT
- 维护活跃度: 公开 GitHub 仓库，MIT；2026-05-31 GitHub API 显示 26,779 stars，官方文档站为 openai.github.io/openai-agents-python。
- 企业可用场景: 需要程序化编排 agent handoff 的团队；把多个角色代理组织成可测试流程
- 安全风险: 框架只提供编排能力，业务边界和安全仍由接入方负责；若没有 tracing/审计，流程复杂后难排障
- 推荐等级: B+
- 证据链接: https://github.com/openai/openai-agents-python

### microsoft/markitdown
- repo/url: https://github.com/microsoft/markitdown
- 简介: 企业里一堆 PDF、PPT、Word 进不了 AI 流程时，它能先把格式摊平。别把转换后的 Markdown 当原件。
- 核心能力: document-conversion, markdown-normalization, file-ingestion, knowledge-prep
- 安装/使用入口: 仓库 README / 官方 docs
- license: MIT
- 维护活跃度: 公开 GitHub 仓库，MIT；2026-05-31 GitHub API 显示 132,964 stars，README 描述为 Office/PDF to Markdown 工具。
- 企业可用场景: 知识库入库前的文档清洗；把 Office/PDF 内容接进研究或写作链路
- 安全风险: 处理的是原始文件，若包含敏感信息仍需脱敏和访问控制；格式转换会有信息损失或结构偏差，需要人工抽检
- 推荐等级: A-
- 证据链接: https://github.com/microsoft/markitdown

### BerriAI/litellm
- repo/url: https://github.com/BerriAI/litellm
- 简介: 当你手里不止一家模型供应商，还想统一路由、记日志、控预算时，它很实用。问题是密钥会更集中，所以平台权限要更严。
- 核心能力: llm-gateway, provider-routing, cost-tracking, guardrails, logging
- 安装/使用入口: 仓库 README / 官方 docs
- license: MIT core; enterprise/ directory separately licensed
- 维护活跃度: 公开 GitHub 仓库；2026-05-31 GitHub API 显示 48,799 stars，根 LICENSE 前言写明 core 为 MIT，enterprise/ 目录单独授权。
- 企业可用场景: 多模型供应商接入统一出口；需要做路由、日志、预算和策略控制的团队
- 安全风险: 会集中管理 API key、日志与路由策略，平台权限必须严格控制；根 LICENSE 明确 enterprise/ 目录另有许可证，复用时不能一概按 MIT 理解
- 推荐等级: A-
- 证据链接: https://github.com/BerriAI/litellm

### mem0ai/mem0
- repo/url: https://github.com/mem0ai/mem0
- 简介: 如果你的助手老是前后失忆，或者客服每轮都像第一次接触用户，可以研究它。但记得先把保留期、删除和纠错机制想清楚。
- 核心能力: agent-memory, profile-memory, state-management, knowledge-recall
- 安装/使用入口: 仓库 README / 官方 docs
- license: Apache-2.0
- 维护活跃度: 公开 GitHub 仓库，Apache-2.0；2026-05-31 GitHub API 显示 57,170 stars，README 描述为 AI agents 的 universal memory layer。
- 企业可用场景: 客服/助理型代理的上下文保持；需要多轮连续性和偏好记忆的内部助手
- 安全风险: 长期记忆天然涉及 PII、偏好和历史行为，需要 retention 与删除机制；记错或过期记忆会直接污染后续输出
- 推荐等级: B+
- 证据链接: https://github.com/mem0ai/mem0

## Verified Public（本轮新增）
### revfactory/harness
- repo/url: https://github.com/revfactory/harness
- 简介: 适合拿来研究“怎么把一个岗位拆成 agent 团队 + skill 包”。更像方法样本，不是接上就能自治的员工。
- 核心能力: multi-agent-workflow, role-packaging, workflow-templates, planning
- 安装/使用入口: README Installation + 官方文档站点 https://revfactory.github.io/harness/
- license: Apache-2.0
- 维护活跃度: 2026-05-29 仍有代码推送；GitHub API 记录 4,391 stars。
- 企业可用场景: 设计企业内部专岗 agent 团队；把 skill 模板沉淀成培训/咨询交付件
- 安全风险: 容易被误包装成“自动生成团队就能落地”，实际仍需人工定义边界和验收
- 推荐等级: A-
- 证据链接: https://github.com/revfactory/harness | https://github.com/revfactory/harness/blob/main/README.md | https://revfactory.github.io/harness/

### browser-use/browser-use
- repo/url: https://github.com/browser-use/browser-use
- 简介: 适合把网页采集、登录后操作、表单流转做成企业数字员工流程，但必须先控好账号、数据和审计边界。
- 核心能力: browser-automation, web-retrieval, tool-calling, web-testing
- 安装/使用入口: README 的 LLM Quickstart + docs.browser-use.com。
- license: MIT
- 维护活跃度: 2026-05-26 仍有代码推送；GitHub API 记录 96,367 stars。
- 企业可用场景: 网页采集与表单操作自动化；需要浏览器级执行的测试/运营流程
- 安全风险: 涉及登录态、Cookie、页面数据时必须配审计与最小权限；浏览器自动化容易被误用成“代替人类审核”
- 推荐等级: A
- 证据链接: https://github.com/browser-use/browser-use | https://github.com/browser-use/browser-use/blob/main/README.md | https://browser-use.com

### google-gemini/gemini-cli
- repo/url: https://github.com/google-gemini/gemini-cli
- 简介: 适合观察“大厂 CLI agent 如何落到终端工作流”。能提速，但不应被当成默认可信的生产执行者。
- 核心能力: terminal-execution, repo-context, tool-calling, planning
- 安装/使用入口: README Installation 指向 https://www.geminicli.com/docs/get-started/installation 。
- license: Apache-2.0
- 维护活跃度: 2026-05-30 仍有代码推送；GitHub API 记录 104,774 stars。
- 企业可用场景: 终端式研发助手与办公助手研究；对比不同 CLI agent 的接入方式
- 安全风险: 终端执行与上下文读取需要权限隔离；外部模型调用要明确数据出境与留存边界
- 推荐等级: A
- 证据链接: https://github.com/google-gemini/gemini-cli | https://github.com/google-gemini/gemini-cli/blob/main/README.md | https://www.geminicli.com/docs/get-started/installation

### mattpocock/skills
- repo/url: https://github.com/mattpocock/skills
- 简介: 是高传播度的 skills 样本库，适合拆解“一个工程团队会愿意复用什么 skill、怎么落到 setup 流程里”。
- 核心能力: skill-library, testing, debugging, code-review
- 安装/使用入口: README Quickstart：npx skills@latest add mattpocock/skills。
- license: MIT
- 维护活跃度: 2026-05-31 当天仍有代码推送；GitHub API 记录 112,648 stars。
- 企业可用场景: 整理工程类 skill 模板；研究 skills 安装与激活流程
- 安全风险: 公开 skill 模板质量不一，需要二次裁剪和本地化审校
- 推荐等级: A
- 证据链接: https://github.com/mattpocock/skills | https://github.com/mattpocock/skills/blob/main/README.md

### K-Dense-AI/scientific-agent-skills
- repo/url: https://github.com/K-Dense-AI/scientific-agent-skills
- 简介: 适合观察“垂直领域技能库如何围绕科学研究组织能力与数据源”。对企业咨询/培训也有借鉴价值。
- 核心能力: skill-library, deep-research, source-synthesis, knowledge-prep
- 安装/使用入口: README Getting Started。
- license: MIT
- 维护活跃度: 2026-05-28 仍有代码推送；GitHub API 记录 26,687 stars。
- 企业可用场景: 垂直领域 skill 库样本研究；方法论课程里展示行业化 skill 打包方式
- 安全风险: 专业领域技能需要行业专家复核，不能只靠 README 宣传口径
- 推荐等级: B+
- 证据链接: https://github.com/K-Dense-AI/scientific-agent-skills | https://github.com/K-Dense-AI/scientific-agent-skills/blob/main/README.md | https://k-dense.ai

### spring-ai-community/spring-ai-agent-utils
- repo/url: https://github.com/spring-ai-community/spring-ai-agent-utils
- 简介: 适合 Java / Spring 体系团队参考怎么把 skill、tool、handoff 封装进企业应用。
- 核心能力: agent-tooling, tool-integration, workflow-sdk, handoffs
- 安装/使用入口: README Quick Start（Maven BOM 依赖导入）。
- license: Apache-2.0
- 维护活跃度: 2026-05-25 仍有代码推送；GitHub API 记录 465 stars。
- 企业可用场景: Spring 生态做 agent 工具层接入；企业内部 Java 系统接 AI 能力
- 安全风险: 企业应用集成一旦连到内部系统，必须先划清工具访问权限和日志策略
- 推荐等级: B+
- 证据链接: https://github.com/spring-ai-community/spring-ai-agent-utils | https://github.com/spring-ai-community/spring-ai-agent-utils/blob/main/README.md | https://spring-ai-community.github.io/spring-ai-agent-utils

### punkpeye/awesome-mcp-servers
- repo/url: https://github.com/punkpeye/awesome-mcp-servers
- 简介: 适合作为 MCP 生态总目录，用来快速找连接器样本和常见系统接入方向。它是目录，不是企业级背书清单。
- 核心能力: protocol-reference, system-connectors, tool-integration, skill-library
- 安装/使用入口: README 目录页；更适合选型，不是安装型产品。
- license: MIT
- 维护活跃度: 2026-05-27 仍有更新；GitHub API 记录 88,223 stars。
- 企业可用场景: 搭建 MCP 选型长名单；培训中展示连接层生态全貌
- 安全风险: 收录项目质量参差不齐，必须逐项复核权限边界、维护状态和许可证
- 推荐等级: A-
- 证据链接: https://github.com/punkpeye/awesome-mcp-servers | https://github.com/punkpeye/awesome-mcp-servers/blob/main/README.md | https://glama.ai/mcp/servers

### PrefectHQ/fastmcp
- repo/url: https://github.com/PrefectHQ/fastmcp
- 简介: 适合 Python 团队搭 MCP server/client 的工程底座，能让连接层从 demo 走向可维护工程。
- 核心能力: tool-integration, workflow-sdk, protocol-reference, tool-calling
- 安装/使用入口: README + https://gofastmcp.com 。
- license: Apache-2.0
- 维护活跃度: 2026-05-30 仍有代码推送；GitHub API 记录 25,410 stars。
- 企业可用场景: 企业内部快速搭 MCP server/client；把工具封装成可维护 Python 服务
- 安全风险: 工具服务一旦连到内部系统，必须补齐认证、审计和最小权限设计
- 推荐等级: A
- 证据链接: https://github.com/PrefectHQ/fastmcp | https://github.com/PrefectHQ/fastmcp/blob/main/README.md | https://gofastmcp.com

### googleapis/mcp-toolbox
- repo/url: https://github.com/googleapis/mcp-toolbox
- 简介: 适合把数据库能力通过 MCP 提供给 IDE/agent，但也意味着要先想清楚谁能查什么、能不能改写。
- 核心能力: system-connectors, tool-integration, protocol-reference, tool-calling
- 安装/使用入口: README Quick Start: Prebuilt Tools + 官方文档站。
- license: Apache-2.0
- 维护活跃度: 2026-05-29 仍有代码推送；GitHub API 记录 15,397 stars。
- 企业可用场景: 数据库接 AI 助手的查询/发现流程；面向开发与分析团队的 MCP 数据访问层
- 安全风险: 数据库连接器涉及敏感数据和写权限，必须先做权限、审计和脱敏策略
- 推荐等级: A-
- 证据链接: https://github.com/googleapis/mcp-toolbox | https://github.com/googleapis/mcp-toolbox/blob/main/README.md | https://mcp-toolbox.dev/documentation/introduction/

### GLips/Figma-Context-MCP
- repo/url: https://github.com/GLips/Figma-Context-MCP
- 简介: 适合设计稿到代码协作链路，但前提是 Figma token、设计资产权限和输出范围要先控住。
- 核心能力: system-connectors, tool-integration, tool-calling, repo-context
- 安装/使用入口: README Getting Started（需 Figma access token）。
- license: MIT
- 维护活跃度: 2026-05-27 仍有代码推送；GitHub API 记录 14,925 stars。
- 企业可用场景: 设计稿信息接入 AI 编码流程；设计系统到前端协作演示
- 安全风险: 依赖 Figma access token，设计资产和客户界面稿可能包含未公开信息
- 推荐等级: B+
- 证据链接: https://github.com/GLips/Figma-Context-MCP | https://github.com/GLips/Figma-Context-MCP/blob/main/README.md | https://www.framelink.ai/

### casdoor/casdoor
- repo/url: https://github.com/casdoor/casdoor
- 简介: 适合做“agent-first IAM / gateway”样本，补齐企业数字员工接入后的身份与访问控制视角。
- 核心能力: system-connectors, guardrails, llm-gateway, tool-integration
- 安装/使用入口: README Quick start + 官方站点 https://casdoor.ai 。
- license: Apache-2.0
- 维护活跃度: 2026-05-31 当天仍有代码推送；GitHub API 记录 13,692 stars。
- 企业可用场景: AI 平台统一身份认证与访问控制；需要 OAuth/OIDC/SAML/LDAP 的企业接入场景
- 安全风险: IAM 一旦配置错误，影响面远大于普通工具；必须经过安全评审与分阶段接入
- 推荐等级: A-
- 证据链接: https://github.com/casdoor/casdoor | https://github.com/casdoor/casdoor/blob/master/README.md | https://casdoor.ai

### apify/crawlee
- repo/url: https://github.com/apify/crawlee
- 简介: 适合做网页采集、站点监测、RAG 原始数据获取底座，但不能越过 robots、条款和隐私边界。
- 核心能力: browser-automation, web-retrieval, file-ingestion, tool-integration
- 安装/使用入口: README Installation + Crawlee JS docs。
- license: Apache-2.0
- 维护活跃度: 2026-05-30 仍有代码推送；GitHub API 记录 23,576 stars。
- 企业可用场景: 网站数据采集与变更监测；RAG/研究流程的网页原料获取
- 安全风险: 网页抓取涉及目标站点条款、代理使用和个人信息处理边界
- 推荐等级: A
- 证据链接: https://github.com/apify/crawlee | https://github.com/apify/crawlee/blob/master/README.md | https://crawlee.dev/js/docs/introduction

### apify/crawlee-python
- repo/url: https://github.com/apify/crawlee-python
- 简介: 适合 Python 技术栈团队做采集/监测/浏览器自动化，不必为 Node-only 工具链让路。
- 核心能力: browser-automation, web-retrieval, file-ingestion, tool-integration
- 安装/使用入口: README Installation + Crawlee Python docs。
- license: Apache-2.0
- 维护活跃度: 2026-05-29 仍有代码推送；GitHub API 记录 9,127 stars。
- 企业可用场景: Python 团队做公开网页采集；研究型/数据型流程接浏览器执行
- 安全风险: 同样涉及网页抓取合规、代理、登录态和数据留存边界
- 推荐等级: A-
- 证据链接: https://github.com/apify/crawlee-python | https://github.com/apify/crawlee-python/blob/master/README.md | https://crawlee.dev/python/docs/introduction

### nanobrowser/nanobrowser
- repo/url: https://github.com/nanobrowser/nanobrowser
- 简介: 适合展示“浏览器扩展形态的 AI 自动化”怎么进入一线业务，但要强调它仍然吃账号、页面和 API key 边界。
- 核心能力: browser-automation, multi-agent-workflow, web-retrieval, tool-calling
- 安装/使用入口: README Quick Start（Chrome Web Store 或开发版安装）。
- license: Apache-2.0
- 维护活跃度: 2025-11-24 最近一次推送；GitHub API 记录 13,060 stars。
- 企业可用场景: Chrome 扩展形态的网页流程自动化；对比 browser-use / crawlee 的一线使用体验
- 安全风险: 依赖浏览器扩展和自带 API key，存在页面数据暴露和操作误触风险
- 推荐等级: B+
- 证据链接: https://github.com/nanobrowser/nanobrowser | https://github.com/nanobrowser/nanobrowser/blob/master/README.md | https://nanobrowser.ai

### openlit/openlit
- repo/url: https://github.com/openlit/openlit
- 简介: 适合补齐“AI 员工不是只会干活，还要可观测、可评估、可控成本”这一层。
- 核心能力: logging, cost-tracking, guardrails, state-management
- 安装/使用入口: README Getting Started with LLM Observability + docs.openlit.io。
- license: Apache-2.0
- 维护活跃度: 2026-05-29 仍有代码推送；GitHub API 记录 2,479 stars。
- 企业可用场景: LLM observability / tracing / cost monitoring；企业内部 AI 平台的观测与评估基座
- 安全风险: 观测平台会汇集 prompt、trace、调用数据，必须处理脱敏与留存策略
- 推荐等级: A-
- 证据链接: https://github.com/openlit/openlit | https://github.com/openlit/openlit/blob/main/README.md | https://docs.openlit.io

### apache/airflow
- repo/url: https://github.com/apache/airflow
- 简介: 虽然不是新项目，但它仍是企业工作流编排的公开强样本，适合补齐“AI 员工要落在什么调度底座上”。
- 核心能力: workflow-templates, state-management, logging, workflow-sdk
- 安装/使用入口: README Getting started + 官方安装文档。
- license: Apache-2.0
- 维护活跃度: 2026-05-31 当天仍有代码推送；GitHub API 记录 45,626 stars。
- 企业可用场景: 跨系统定时/依赖式流程编排；把 AI 任务纳入已有企业调度体系
- 安全风险: 调度平台常掌握大量连接器与凭证，需要独立做密钥与任务权限治理
- 推荐等级: A
- 证据链接: https://github.com/apache/airflow | https://github.com/apache/airflow/blob/main/README.md | https://airflow.apache.org/docs/apache-airflow/stable/start.html

### triggerdotdev/trigger.dev
- repo/url: https://github.com/triggerdotdev/trigger.dev
- 简介: 适合做 AI workflow / background jobs 平台样本，特别是需要看任务执行链路与可视化时。
- 核心能力: workflow-sdk, logging, handoffs, multi-agent-workflow
- 安装/使用入口: README / changelog / docs 入口。
- license: Apache-2.0
- 维护活跃度: 2026-05-30 仍有代码推送；GitHub API 记录 15,161 stars。
- 企业可用场景: 长任务、事件驱动与 AI workflow 编排；需要任务可视化与运行追踪的产品团队
- 安全风险: 工作流平台通常持有回调、API key、任务上下文，必须做环境隔离与审计
- 推荐等级: A-
- 证据链接: https://github.com/triggerdotdev/trigger.dev | https://github.com/triggerdotdev/trigger.dev/blob/main/README.md | https://trigger.dev/changelog

### mlflow/mlflow
- repo/url: https://github.com/mlflow/mlflow
- 简介: 适合把实验、评估、监控和成本治理放进同一条企业 AI 交付链路，不该被误读成“训练框架而已”。
- 核心能力: logging, cost-tracking, guardrails, state-management
- 安装/使用入口: 仓库 README + https://mlflow.org 。
- license: Apache-2.0
- 维护活跃度: 2026-05-31 当天仍有代码推送；GitHub API 记录 26,210 stars。
- 企业可用场景: 模型/agent 实验追踪与评估；企业 AI 交付过程的可观测与治理
- 安全风险: 治理平台会汇总模型、数据、实验结果，需要明确访问控制和数据分类
- 推荐等级: A
- 证据链接: https://github.com/mlflow/mlflow | https://github.com/mlflow/mlflow/blob/master/README.md | https://mlflow.org

### tensorzero/tensorzero
- repo/url: https://github.com/tensorzero/tensorzero
- 简介: 适合把模型调用层、评估层、实验层收敛在一套 LLMOps 平台里，但也意味着平台治理责任更重。
- 核心能力: llm-gateway, logging, guardrails, openai-compatible-api
- 安装/使用入口: README Usage Example（先部署 gateway container）。
- license: Apache-2.0
- 维护活跃度: 2026-05-29 仍有代码推送；GitHub API 记录 11,422 stars。
- 企业可用场景: 统一 LLM gateway 与观测层；把模型优化与实验纳入平台治理
- 安全风险: 网关型平台会集中承载 prompt、路由、模型配置和日志，必须明确访问控制和留存策略
- 推荐等级: A-
- 证据链接: https://github.com/tensorzero/tensorzero | https://github.com/tensorzero/tensorzero/blob/main/README.md | https://tensorzero.com

## Blocked
- JimLiu/baoyu-skills — GitHub API 未返回 license，仓库根目录无明确 LICENSE，复用/再分发边界不清。
  - 证据链接: https://github.com/JimLiu/baoyu-skills
- anthropics/claude-code — 公开仓库但 GitHub license 字段为空，README 还写明会收集反馈/使用数据；默认不进入企业可复用公开条目池。
  - 证据链接: https://github.com/anthropics/claude-code | https://github.com/anthropics/claude-code/blob/main/README.md
- cursor/plugins — GitHub license 字段为空，README/边界信息不足，不满足“license 清晰 + README 不空泛”的首批标准。
  - 证据链接: https://github.com/cursor/plugins

## Watchlist
- ComposioHQ/awesome-claude-skills — 长名单已标 NOASSERTION/边界待复核；保留观察，不进首批。
  - 证据链接: https://github.com/ComposioHQ/awesome-claude-skills
- modelcontextprotocol/inspector — 长名单已标 NOASSERTION/边界待复核；适合作为工具链观察样本。
  - 证据链接: https://github.com/modelcontextprotocol/inspector
- lightpanda-io/browser — AGPL 边界较重，企业复用前需法务/合规确认。
  - 证据链接: https://github.com/lightpanda-io/browser
- Skyvern-AI/skyvern — AGPL 项目；浏览器自动化能力强，但首批不默认收录进企业可复用池。
  - 证据链接: https://github.com/Skyvern-AI/skyvern
- openobserve/openobserve — AGPL 边界较重，适合作为观测平台观察项，不进入首批复用池。
  - 证据链接: https://github.com/openobserve/openobserve
- thedivergentai/gd-agentic-skills — LGPL 项目，复用/再分发边界要先过法务；先观察。
  - 证据链接: https://github.com/thedivergentai/gd-agentic-skills

## 合并说明
- `data/skills.yaml` 已直接追加本轮 19 条 Verified Public 卡片。
- 对既有条目已回填 `source_url` 与 `verification_status` 字段，满足首批结构化复核需要。
- 若后续要继续扩展，可优先从 watchlist 里二次复核许可证/安全边界，再决定是否升级。

## 本轮新增条目清单
- harness — revfactory/harness
- browser-use — browser-use/browser-use
- gemini-cli — google-gemini/gemini-cli
- mattpocock-skills — mattpocock/skills
- scientific-agent-skills — K-Dense-AI/scientific-agent-skills
- spring-ai-agent-utils — spring-ai-community/spring-ai-agent-utils
- awesome-mcp-servers — punkpeye/awesome-mcp-servers
- fastmcp — PrefectHQ/fastmcp
- mcp-toolbox — googleapis/mcp-toolbox
- figma-context-mcp — GLips/Figma-Context-MCP
- casdoor — casdoor/casdoor
- crawlee — apify/crawlee
- crawlee-python — apify/crawlee-python
- nanobrowser — nanobrowser/nanobrowser
- openlit — openlit/openlit
- airflow — apache/airflow
- trigger-dev — triggerdotdev/trigger.dev
- mlflow — mlflow/mlflow
- tensorzero — tensorzero/tensorzero
