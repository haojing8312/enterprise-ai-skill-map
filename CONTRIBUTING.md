# Contributing

欢迎提交公开、安全、可验证的企业级 AI Skill / Agent Workflow。

## 提交前请确认

- 来源公开可访问
- License 或使用边界清楚
- 不包含密钥、Cookie、私有仓库、客户信息、内部路径
- 不鼓励绕过平台限制、滥用账号、抓取隐私数据
- 推荐理由落到企业场景，不写成泛泛的工具夸奖
- 至少补齐 `industries`、`role_groups`、`scenarios` 三组标签

## 推荐新增方式

1. 复制 `templates/skill-card-template.md`
2. 补充结构化字段
3. 在 `data/skills.yaml` 增加条目
4. 在对应 `industries/*.md` 添加引用或重新生成行业页
5. 在对应 `roles/*.md` 添加引用或重新生成岗位页
6. 必要时再更新 `scenarios/*.md` 和 `workflows/*.md`

## 审核标准

我们会按 `data/scoring-rules.md` 评分。安全风险未解决的条目不会合并。

新增分类时，先更新 `data/classification.yaml`，再更新 `taxonomy.md` 和对应页面。
