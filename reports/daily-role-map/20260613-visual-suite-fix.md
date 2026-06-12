# 2026-06-13｜视觉套图 Watchdog 补救记录

## 对象

- 系列：每天认识一个出海 AI 员工
- 岗位：AI 独立站页面健康巡检员 / AI Website Health Auditor
- slug：`ai-website-health-auditor`
- 工作区：`/mnt/f/code/work/公众号文章/crossborder-digital-employee-series/20260613-ai-website-health-auditor/`

## 触发原因

03:00 主任务文本已完成，但视觉被标记为 `blocked / partial`：原视觉生成轮次连续输出 1024×1536（2:3），不满足硬性 9:16 门槛，因此未保存为合格候选图，也未向 final_message 写入 5 行 MEDIA。

## 补救动作

04:10 watchdog 读取：

- `visual/visual_prompt.md`
- `draft/role-map-copy.md`
- `draft/short-platform-copy.md`
- `review/chief_review.md`

并调用 visual-agent profile 原生 image_gen 重新生成 5 张 PNG。补救过程遵守：

- 禁止 HTML / Canvas / PIL / SVG / 程序化截图 / 模板渲染。
- 禁止本地拉伸、裁切、扩图把 2:3 冒充 9:16。
- PIL 仅用于尺寸校验。
- 每张底部署名：`郝朋友的AI进化论`。
- Card 01 必须是系列首页 / 今日岗位封面，含岗位名、岗位职责、核心技能、业务作用。

## 结果

5 张图均为 1152×2048，严格 9:16：

| 卡片 | 文件 | 尺寸 | 质检 |
|---|---|---:|---|
| 01 | `visual/ai-website-health-auditor/ai-website-health-auditor-01-cover.png` | 1152×2048 | PASS：今日岗位封面；岗位职责/核心技能/业务作用清晰；署名存在 |
| 02 | `visual/ai-website-health-auditor/ai-website-health-auditor-02-pain.png` | 1152×2048 | PASS：广告扣费与坏页面痛点清楚；署名存在 |
| 03 | `visual/ai-website-health-auditor/ai-website-health-auditor-03-compare.png` | 1152×2048 | PASS：旧方法 vs AI 页面巡检员对比清楚；署名存在 |
| 04 | `visual/ai-website-health-auditor/ai-website-health-auditor-04-workflow-prompts.png` | 1152×2048 | PASS：流程、工具与提示词可读；署名存在 |
| 05 | `visual/ai-website-health-auditor/ai-website-health-auditor-05-toolkit-pilot.png` | 1152×2048 | PASS：第一周试点、工具栈、边界清楚；署名存在 |

## GitHub 入库文件

- `reports/daily-role-map/20260613.md`
- `reports/daily-role-map/20260613-visual-suite-fix.md`
- `visual/ai-website-health-auditor/ai-website-health-auditor-01-cover.png`
- `visual/ai-website-health-auditor/ai-website-health-auditor-02-pain.png`
- `visual/ai-website-health-auditor/ai-website-health-auditor-03-compare.png`
- `visual/ai-website-health-auditor/ai-website-health-auditor-04-workflow-prompts.png`
- `visual/ai-website-health-auditor/ai-website-health-auditor-05-toolkit-pilot.png`

## 最终状态

`watchdog visual fix PASS`：短文案 PASS；5 图 9:16 PASS；Card 01 首页结构 PASS；final_message 已补 5 行 MEDIA；GitHub 本期视觉补救文件已完成 commit + push。
