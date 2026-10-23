---
name: bid-gantt
description: Designs one schedule Gantt chart at a time from 招标文件, 投标文件, or 技术方案. Use for 甘特图, 进度计划, and dated tasks with dependencies. Draws from confirmed dates with Mermaid or SVG. Do not invent dates or replace the phase roadmap.
---

# 招投标甘特图

一张图只覆盖一份进度计划。任务、开始时间、结束时间和依赖以投标进度或招标工期为准。没有日期的任务不估算日历，只保留在阶段路线图中。

横轴是时间，纵轴是任务。条形长度对应工期。里程碑用单独标记。依赖只画原文写明的前后关系。任务很多时按阶段拆成多张，不缩小到不可读。

阶段、交付物和验收的总览交给 `bid-implementation-roadmap`。工作包分解交给 `bid-wbs`。

用 Mermaid `gantt` 或 SVG 绘制并导出 PNG。不用图像模型。禁止改写招标工期和虚构人月。源稿写入 `bid_images/prompts/`，PNG 写入 `bid_images/generated/`。
