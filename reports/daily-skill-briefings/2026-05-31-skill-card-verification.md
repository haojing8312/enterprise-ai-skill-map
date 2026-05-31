# 2026-05-31 首批 Skill 卡片验证摘要

## 本次新增

已在 `data/skills.yaml` 新增 14 个首批候选条目，并保留原有 `superpowers` 条目。

### Verified Public（13）
- codex — openai/codex
- opencode — anomalyco/opencode
- llama-cpp — ggml-org/llama.cpp
- vllm — vllm-project/vllm
- mcp-servers — modelcontextprotocol/servers
- github-mcp-server — github/github-mcp-server
- playwright-mcp — microsoft/playwright-mcp
- claude-skills — alirezarezvani/claude-skills
- open-deep-research — langchain-ai/open_deep_research
- openai-agents-python — openai/openai-agents-python
- markitdown — microsoft/markitdown
- litellm — BerriAI/litellm
- mem0 — mem0ai/mem0

### Blocked（1）
- baoyu-skills — JimLiu/baoyu-skills
  - 原因：GitHub API `license` 接口返回 404，仓库根目录未发现明确 LICENSE，当前复用/再分发边界不清楚。

## 验证方法

- 以公开 GitHub 仓库为主证据源。
- 记录了 URL、License/使用边界、适用场景、风险等级、验证状态。
- 对 `modelcontextprotocol/servers`、`litellm` 这类复合许可仓库，已在 `license` 与 `review_notes` 中显式标注边界。
- 对 License 缺失或边界不清晰项，按规则直接标 `blocked`。

## 备注

- 评分为内容团队当前收录判断，不代表第三方官方评级。
- 这些条目更适合作为“企业数字员工能力底座 / 工作流样本 / 连接层样本”，不应被包装成“接上就能自治”的万能方案。
