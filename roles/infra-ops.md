# 岗位｜基础设施/运维负责人

内网部署、GPU、边缘设备、系统稳定性和权限隔离。

## 适用行业

- [AI/数据基础设施团队](../industries/ai-infrastructure.md)：3 个 Skill
- [软件/互联网/研发组织](../industries/software-internet.md)：3 个 Skill
- [政企/国企/内网场景](../industries/government-stateowned.md)：1 个 Skill

## 当前可用 Skill

|Skill|行业|场景|风险|一句话用法|
|---|---|---|---|---|
|[vllm-project/vllm](https://github.com/vllm-project/vllm)|AI/数据基础设施团队<br>软件/互联网/研发组织|r-and-d<br>operations-admin|medium|当团队开始同时接多模型、看吞吐和成本时，再考虑它更合适。别把它当成一键省心的 SaaS。|
|[ggml-org/llama.cpp](https://github.com/ggml-org/llama.cpp)|AI/数据基础设施团队<br>政企/国企/内网场景<br>软件/互联网/研发组织|r-and-d<br>operations-admin|medium|如果场景出不了网，或者想先把模型跑在自己机器上，它是个靠谱底座。但它解决的是推理，不是业务流程。|
|[BerriAI/litellm](https://github.com/BerriAI/litellm)|AI/数据基础设施团队<br>软件/互联网/研发组织|r-and-d<br>operations-admin|medium|当你手里不止一家模型供应商，还想统一路由、记日志、控预算时，它很实用。问题是密钥会更集中，所以平台权限要更严。|

## 岗位使用建议

- 把 Skill 当成工作流组件，不要当成完整岗位替代。
- 先写清输入、输出、审批人和失败回退方式。
- 能触达代码、账号、客户数据、合同或财务数据的能力，默认提高一个风险等级管理。
