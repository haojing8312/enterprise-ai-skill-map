# AI 编码与研发效能 Skill 路线

适合：开发工程师、技术负责人、研发效能负责人、QA。

## 推荐闭环

```text
需求/spec → AI 编码 → 测试 → Code Review → 发布检查 → 复盘沉淀
```

## 常见能力

- 读仓库、定位代码、补测试
- 小范围 bugfix 和重构
- PR Review、CI 检查、发布前清单
- 本地模型/Agent 工具链验证

## 安全边界

- 不直接让 AI 改生产系统。
- 不跳过测试和 code review。
- 会执行终端命令的 coding agent 默认中风险以上，需要沙箱和权限边界。

## 数据入口

更多研发类 Skill 可在 [`data/skills.yaml`](../data/skills.yaml) 中按 `role_groups: engineering` / `scenarios: r-and-d` 检索。
