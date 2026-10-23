---
name: bid-flowchart
description: Designs one bid-document flowchart at a time from 招标文件, 投标文件, or 技术方案. Use when the figure is a 流程图, 业务流程, 审批流程, 办理流程, or a sequence with decisions, branches, and loops. Draws with Mermaid or SVG and exports PNG. Do not use for architecture layers, network topology, or deployment.
---

# 招投标流程图

先阅读当前项目中该流程的原文，只设计这一张流程图。色彩和字体遵循 `.cursor/skills/bid-document-image-design/SKILL.md`。

## 表达边界

流程图只表达步骤、顺序、条件分支、并行和闭环。

- 系统分层和模块依赖交给 `bid-architecture-diagram`。
- 网络节点和链路交给 `bid-topology-diagram`。
- 阶段、里程碑和交付物交给 `bid-implementation-roadmap`。

## 从原文提取

- 起点、终点和每个步骤的原文名称。
- 判断条件，以及原文给出的每个分支去向。
- 并行步骤、退回、重试或闭环。
- 角色或部门。只有原文区分责任主体时才做泳道。
- 时限、表单或输出物。原文没有则不写进节点。

步骤顺序以原文为准。原文未写的审批节点不补。

## 构图

主流程保持一个方向。步骤少于 8 个用横向；步骤多或分支多用纵向。判断用菱形，普通步骤用圆角矩形，起止用胶囊形。

“是/否”或原文中的分支词写在对应箭头旁。退回和闭环走外侧通道，不穿过主步骤。泳道按角色横向排列，步骤落在责任泳道内。

多条业务线必须拆成多张流程图，不得挤在一张总流程图里。

## 绘制

优先用 Mermaid `flowchart`，节点文字和分支标签以原文为准；导出 SVG 后再导出宽 2400px 的 PNG。Mermaid 无法表达泳道或精确对齐时，改用 SVG。

节点内文字不小于 18px，箭头连续，不出现断开或重叠文字。

## 禁止

用图像模型生成流程图。把流程画成架构分层。添加原文没有的判断分支。使用装饰性背景和英文占位符。

## 校验

从起点沿每条分支走到终点或闭环，核对是否与原文一致。设计说明和 Mermaid 源稿写入 `bid_images/prompts/IMG-编号.md`，PNG 写入 `bid_images/generated/`。
