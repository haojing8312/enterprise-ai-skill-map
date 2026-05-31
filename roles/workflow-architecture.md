# 岗位｜工作流架构师

设计多代理交接、状态流转、异常处理和可观察性。

## 适用行业

- [咨询/培训/知识服务](../industries/consulting-training.md)：3 个 Skill
- [软件/互联网/研发组织](../industries/software-internet.md)：2 个 Skill
- [AI/数据基础设施团队](../industries/ai-infrastructure.md)：1 个 Skill
- [内容/媒体/营销服务](../industries/content-media.md)：1 个 Skill
- [通用企业/内部运营](../industries/general-enterprise.md)：1 个 Skill

## 当前可用 Skill

|Skill|行业|场景|风险|一句话用法|
|---|---|---|---|---|
|[openai/openai-agents-python](https://github.com/openai/openai-agents-python)|软件/互联网/研发组织<br>AI/数据基础设施团队<br>咨询/培训/知识服务|r-and-d<br>operations-admin|medium|适合自己搭一套有人设、有交接、有工具调用的数字员工原型。它是 SDK，不是现成业务系统。|
|[alirezarezvani/claude-skills](https://github.com/alirezarezvani/claude-skills)|通用企业/内部运营<br>内容/媒体/营销服务<br>咨询/培训/知识服务|r-and-d<br>marketing-content<br>operations-admin|medium|适合拿来研究企业内部 skill 库怎么分层、怎么裁剪。别整仓搬进来，不然上下文很快失控。|
|[obra/superpowers](https://github.com/obra/superpowers)|软件/互联网/研发组织<br>咨询/培训/知识服务|r-and-d<br>operations-admin|low|如果团队已经在用 AI 写码，但总要靠人最后收烂摊子，可以先看它怎么把 spec、测试、验收往前放。它更像流程样本，不是万能外挂。|

## 岗位使用建议

- 把 Skill 当成工作流组件，不要当成完整岗位替代。
- 先写清输入、输出、审批人和失败回退方式。
- 能触达代码、账号、客户数据、合同或财务数据的能力，默认提高一个风险等级管理。
