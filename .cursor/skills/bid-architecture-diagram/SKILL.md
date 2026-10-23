---
name: bid-architecture-diagram
description: Designs one bid-document architecture diagram at a time from 招标文件, 投标文件, or 技术方案. Use when the figure is a 架构图, 总体架构, 技术架构, 应用架构, 业务架构, or logical system layers and module dependencies. Draws with SVG or HTML and exports PNG. Do not use for network topology, deployment, or step-by-step flows.
---

# 招投标架构图

先阅读当前项目中该图对应的招标文件、投标文件或技术方案，只设计这一张架构图。色彩和字体遵循 `.cursor/skills/bid-document-image-design/SKILL.md`。

## 表达边界

架构图只表达逻辑分层、模块和依赖。

- 网络区域、链路和安全域交给 `bid-topology-diagram`。
- 服务器、容器、机房和部署单元交给 `bid-deployment-diagram`。
- 步骤、判断和循环交给 `bid-flowchart`。

## 从原文提取

只记录原文写明的内容：

- 图题、章节、这张图要回答的问题。
- 层次或分区。原文没有的层次不补。
- 每个模块的名称，与原文一致。
- 原文写明的调用、依赖或数据传递。未写明的关系不画箭头。
- 需要在图中出现的接口名称。没有接口字段时不编造。

## 构图

按这张图的内容选一种构图，不得每张架构图都用同一套五层横条。

- 分层架构：展示、应用、服务、数据、基础自上而下，只保留原文存在的层。
- 中心架构：核心平台居中，周边子系统按业务分列。
- 分区架构：按业务域分栏，栏内再放模块。
- 对照架构：仅当原文要求现状与目标、或招标要求与投标响应对照。

同层模块对齐，层名放在层的左侧或顶部。依赖用直角折线，箭头指向被调用方。跨层调用集中走层间通道，避免斜线交叉。

## 绘制

用 SVG 或 HTML 绘制，再导出 PNG。默认横版，宽 2400px，四周留白不少于 64px。模块文字不小于 18px。标题放在图内上方。

图内只保留标题、层名、模块名、原文中的关系标签和图例。图例仅在存在两种以上关系时出现。

## 禁止

虚构微服务、中间件、数据库或性能指标。把多张架构画进一张。使用光效、3D 机柜、无意义图标或英文占位符。用图像模型直接生成这张文字架构图。

## 校验

逐项对照原文模块清单。多出的模块、缺失的模块、标错的依赖都要改这张图后重新导出。设计说明写入 `bid_images/prompts/IMG-编号.md`，PNG 写入 `bid_images/generated/`。
