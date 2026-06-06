# 2026-06-07 视觉套图 watchdog 修复记录

- 日期：2026-06-07
- 岗位：AI 亚马逊评论洞察员 / AI Amazon Review Insights Agent
- slug：ai-amazon-review-insights-agent
- 修复对象：Card 05｜能力模块 + 工具栈 + 第一周试点

## 问题

watchdog 复核发现 Card 05 旧图中第 03 能力模块存在高风险错字/近形字问题，不能作为视觉 PASS 交付。

## 修复动作

- 已通过 visual-agent profile 的 image_gen 原生生成重做版 Card 05。
- 未重新选题，未改动前 4 张卡片。
- 未使用 HTML / Canvas / PIL / SVG / 程序化截图 / 本地拉伸裁切。
- 已将工作区修复版同步至 GitHub repo：`visual/ai-amazon-review-insights-agent/ai-amazon-review-insights-agent-05-toolkit-pilot.png`。

## 修复后验收

| 项目 | 结果 |
|---|---|
| 尺寸 | 1152×2048 |
| 比例 | 9:16 PASS |
| Card 01 首页结构 | PASS：含岗位名、岗位职责、核心技能、业务作用 |
| Card 05 文案 | PASS：能力模块、ASIN 运营看板、工具栈、试点验收可读 |
| 错字/乱码/遮挡 | PASS：未见明显错字、乱码或遮挡 |
| 底部署名 | PASS：郝朋友的AI进化论可读 |
| final_message | PASS：含 5 行 MEDIA |

## 结论

watchdog 修复后：短文案 PASS；5 图 9:16 PASS；GitHub 本期文件待 commit/push。
