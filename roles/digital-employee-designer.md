# 岗位｜数字员工/Skill 设计师

把可复用能力包装成可分发、可维护的 Skill 或模板。

## 适用行业

- [内容/媒体/营销服务](../industries/content-media.md)：2 个 Skill
- [咨询/培训/知识服务](../industries/consulting-training.md)：2 个 Skill
- [通用企业/内部运营](../industries/general-enterprise.md)：1 个 Skill

## 当前可用 Skill

|Skill|行业|场景|风险|一句话用法|
|---|---|---|---|---|
|[alirezarezvani/claude-skills](https://github.com/alirezarezvani/claude-skills)|通用企业/内部运营<br>内容/媒体/营销服务<br>咨询/培训/知识服务|r-and-d<br>marketing-content<br>operations-admin|medium|适合拿来研究企业内部 skill 库怎么分层、怎么裁剪。别整仓搬进来，不然上下文很快失控。|
|[JimLiu/baoyu-skills](https://github.com/JimLiu/baoyu-skills)|内容/媒体/营销服务<br>咨询/培训/知识服务|marketing-content<br>operations-admin|high|这个仓库更适合当观察样本，不适合直接拿去商用复用。现在最大的卡点不是能力，而是许可边界没讲清。|

## 岗位使用建议

- 把 Skill 当成工作流组件，不要当成完整岗位替代。
- 先写清输入、输出、审批人和失败回退方式。
- 能触达代码、账号、客户数据、合同或财务数据的能力，默认提高一个风险等级管理。
