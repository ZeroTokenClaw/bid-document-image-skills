---
name: bid-wbs
description: Designs one work breakdown structure at a time from 招标文件, 投标文件, or 技术方案. Use for WBS, 工作分解, and deliverable packages. Draws a tree with SVG. Do not use for function trees, organization charts, or Gantt charts.
---

# 招投标工作分解图

一张图只分解一个项目或一个标段的工作包。顶层是项目，下层是可交付的工作，而不是软件功能或岗位。

工作包名称使用实施计划原文。同一层级表示同一分解粒度。不在本图上画时间和责任人；时间交给 `bid-gantt`，责任交给 `bid-raci`，功能交给 `bid-function-tree`。

用 SVG 自上而下绘制并导出 PNG。不用图像模型。禁止虚构工作包和百分比。说明写入 `bid_images/prompts/`，PNG 写入 `bid_images/generated/`。
