---
name: bid-function-tree
description: Designs one function decomposition tree at a time from 招标文件, 投标文件, or 技术方案. Use for 功能结构图, 功能分解, and module trees. Draws with SVG. Do not use for organization charts, WBS, or business flowcharts.
---

# 招投标功能结构图

一张图只分解一个系统或一个子系统的功能。上级功能在上，下级功能在下，同级横向对齐。功能名称与需求或方案原文一致。

只展开原文已经分层的功能。叶子功能不再自行拆成按钮或接口。多个子系统分别出图。

组织岗位交给 `bid-org-chart`。项目工作包交给 `bid-wbs`。操作步骤交给 `bid-flowchart`。

用 SVG 绘制并导出 PNG，功能名不小于 18px。不用图像模型。禁止虚构功能和创新点。说明写入 `bid_images/prompts/`，PNG 写入 `bid_images/generated/`。
