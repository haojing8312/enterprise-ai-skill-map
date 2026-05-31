# 法务合规场景

## 场景问题

法务合规最怕两件事：一是把格式整理当成法律判断，二是把机器给的提示当成免责依据。这里的 Skill 只能做前处理和风险提示。

## 典型岗位/数字员工
- [文档处理专员](../roles/document-ops.md)：1 个 Skill
- [知识库运营](../roles/knowledge-ops.md)：1 个 Skill
- [法务/合规负责人](../roles/legal-compliance.md)：1 个 Skill

## 当前可用 Skill（1）
|Skill|行业|岗位|风险|推荐用法|
|---|---|---|---|---|
|[microsoft/markitdown](https://github.com/microsoft/markitdown)|[通用企业/内部运营](../industries/general-enterprise.md)<br>[专业服务：法律/咨询/研究](../industries/professional-services.md)<br>[内容/媒体/营销服务](../industries/content-media.md)|[文档处理专员](../roles/document-ops.md)<br>[知识库运营](../roles/knowledge-ops.md)<br>[法务/合规负责人](../roles/legal-compliance.md)|low|给知识库和文档处理团队用，适合把 PDF、PPT、Word 先转成能喂给 AI 的文本；转换稿不能当原件，敏感文件照样要脱敏。|

## 推荐工作流
- 只做文档前处理和信息整理，不替代法律判断。
- 先把原件、转换稿和风险提示分层，再交给人工复核。
- 涉及合同、隐私、权限和对外承诺时，必须保留人工拍板。

## 风险边界
- 这里只能做前处理和风险提示，不能把机器输出当法律结论。
- 合同、隐私、权限和对外承诺必须人工复核。
- 原件与摘要、建议与结论要严格分层。
