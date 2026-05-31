# 行业｜AI/数据基础设施团队

模型服务、推理网关、本地部署、成本治理和工具接入。

## 先看哪些岗位

- [AI 平台工程师](../roles/ai-platform.md)：4 个 Skill
- [基础设施/运维负责人](../roles/infra-ops.md)：3 个 Skill
- [成本治理负责人](../roles/cost-governance.md)：2 个 Skill
- [数字员工架构师](../roles/digital-employee-architect.md)：2 个 Skill
- [AI 应用工程师](../roles/ai-application.md)：1 个 Skill
- [工作流架构师](../roles/workflow-architecture.md)：1 个 Skill
- [开发工程师](../roles/engineering.md)：1 个 Skill
- [技术负责人/研发效能负责人](../roles/engineering-management.md)：1 个 Skill
- [研发平台/GitHub 管理员](../roles/engineering-platform.md)：1 个 Skill
- [运营/行政/流程管理员](../roles/operations-admin.md)：1 个 Skill

## 当前可用 Skill

|Skill|岗位|场景|风险|一句话用法|
|---|---|---|---|---|
|[anomalyco/opencode](https://github.com/anomalyco/opencode)|开发工程师<br>研发平台/GitHub 管理员<br>技术负责人/研发效能负责人|r-and-d|medium|想自己掌控 AI 编码流程，而不是全押某个闭源产品，可以拿它做开源底座。别把“能改代码”理解成“能自己交付”。|
|[vllm-project/vllm](https://github.com/vllm-project/vllm)|AI 平台工程师<br>基础设施/运维负责人<br>成本治理负责人|r-and-d<br>operations-admin|medium|当团队开始同时接多模型、看吞吐和成本时，再考虑它更合适。别把它当成一键省心的 SaaS。|
|[ggml-org/llama.cpp](https://github.com/ggml-org/llama.cpp)|AI 平台工程师<br>基础设施/运维负责人|r-and-d<br>operations-admin|medium|如果场景出不了网，或者想先把模型跑在自己机器上，它是个靠谱底座。但它解决的是推理，不是业务流程。|
|[modelcontextprotocol/servers](https://github.com/modelcontextprotocol/servers)|AI 平台工程师<br>数字员工架构师<br>运营/行政/流程管理员|r-and-d<br>office<br>operations-admin|medium|它的价值不是“更聪明”，而是把文件、浏览器、GitHub 这些工具接进来，让数字员工真的能干活。前提是权限要一项一项收紧。|
|[BerriAI/litellm](https://github.com/BerriAI/litellm)|AI 平台工程师<br>成本治理负责人<br>基础设施/运维负责人|r-and-d<br>operations-admin|medium|当你手里不止一家模型供应商，还想统一路由、记日志、控预算时，它很实用。问题是密钥会更集中，所以平台权限要更严。|
|[openai/openai-agents-python](https://github.com/openai/openai-agents-python)|AI 应用工程师<br>工作流架构师<br>数字员工架构师|r-and-d<br>operations-admin|medium|适合自己搭一套有人设、有交接、有工具调用的数字员工原型。它是 SDK，不是现成业务系统。|

## 使用边界

- 先从低风险、有人审的流程开始。
- 涉及客户数据、账号权限、合同、价格、医疗/金融/政务等高敏信息时，必须增加人工确认。
- 这个页只做行业入口，不替代具体项目方案。
