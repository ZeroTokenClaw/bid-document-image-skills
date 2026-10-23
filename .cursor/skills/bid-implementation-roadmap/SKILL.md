---
name: bid-implementation-roadmap
description: Designs one bid-document implementation roadmap or timeline at a time from 招标文件, 投标文件, or 技术方案. Use when the figure is a 项目实施图, 实施路线, 时间轴, 里程碑, 进度计划, or shows phases, tasks, deliverables, and acceptance. Draws with SVG or HTML and exports PNG. Do not use for architecture, flowcharts, topology, or deployment.
---

# 招投标项目实施图

先阅读当前项目中该实施计划的原文，只设计这一张实施图或时间轴。色彩和字体遵循 `.cursor/skills/bid-document-image-design/SKILL.md`。

## 表达边界

实施图只表达阶段、任务、里程碑、交付物和验收节点。

- 系统分层交给 `bid-architecture-diagram`。
- 办理步骤和条件分支交给 `bid-flowchart`。
- 环境与服务部署位置交给 `bid-deployment-diagram`。

## 从原文提取

- 阶段名称、顺序和原文给出的时间。
- 每阶段的任务、交付物和责任方。
- 里程碑和验收节点。原文没有日期时保留阶段顺序，不编造日历。
- 招标文件要求的工期约束。投标响应不得改写这些约束。

未确认的日期标“待确认”。

## 构图

阶段沿水平时间轴从左到右排列。阶段用等宽区段，区内列出该阶段任务。交付物放在区段下方，里程碑和验收放在轴上，用两种不同标记区分。

阶段少于 4 个且任务很多时，改为纵向阶段带，每带内部再列任务和交付物。不得使用架构图的分层布局。

多条实施线，如软件、集成、培训，原文分开描述时拆成多张图，或在同一时间轴上分成少量平行轨道。轨道名称必须来自原文。

## 绘制

用 SVG 或 HTML 绘制，再导出宽 2400px 的 PNG。阶段名、交付物和验收文字不小于 18px。时间文本与阶段对齐，不重叠。

## 禁止

用图像模型生成实施图。虚构工期、人月、验收结论或招标文件没有的阶段。把实施计划画成技术架构。添加装饰性城市天际线或旗帜。

## 校验

阶段顺序、交付物和验收节点与投标进度计划及招标工期一致。设计说明写入 `bid_images/prompts/IMG-编号.md`，PNG 写入 `bid_images/generated/`。
