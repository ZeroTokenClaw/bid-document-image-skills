---
name: bid-infographic
description: Designs one bid-document infographic at a time from 招标文件, 投标文件, or 技术方案. Use for 信息图, 图解, 指标对照, and visual summaries. Structured text and numbers use SVG or HTML; short-title visuals use the imagegen skill. Do not use for architecture, flowchart, topology, deployment, or data-governance diagrams.
---

# 招投标信息图

一张信息图只说明一个问题，例如一组对照、一个组成关系或一条已确认结论。数字、名称和结论必须能在招标文件、投标文件或技术方案中找到。

## 绘制方式

信息图以文字和关系为主，默认用 SVG 或 HTML 绘制，再导出 PNG。不把精确指标交给图像模型。

只有画面主体是实物或场景、标题不超过一句时，才按 `.cursor/skills/imagegen/SKILL.md` 生成视觉底图，用例 `infographic-diagram`。标题逐字写入提示词；生成后核对，错字则改为矢量文字重做。

## 构图

按内容选择一种，不重复架构图的分层横条：

- 对照：左右或上下两栏，栏题使用原文分组名。
- 组成：中心主题，周围不超过原文列出的分项。
- 结论：上方一句结论，下方按阅读顺序排列依据。

每栏只放该栏的事实。没有单位或口径的数字标“待确认”，不估算。默认横版 2400px；条目很多时改为纵向，不缩小到不可读。

## 禁止

虚构百分比、排名和增长。把流程图、数据治理链路或实施时间轴改画成信息图。使用装饰性大数字和无关图标。多张信息图合并成一张海报。

## 校验

每个可见事实都能指回原文出处。设计说明写入 `bid_images/prompts/`，PNG 写入 `bid_images/generated/`。
