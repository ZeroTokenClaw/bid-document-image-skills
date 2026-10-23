---
name: bid-dashboard-visual
description: Designs one digital-twin or operations dashboard visual at a time from 招标文件, 投标文件, or 技术方案. Use for 数字孪生大屏, 监控大屏, and 可视化大屏. Exact panels use HTML; atmosphere views use the imagegen skill. Do not invent metrics or replace architecture, topology, and deployment diagrams.
---

# 招投标数字孪生大屏

一张图只表现一块大屏或一种大屏状态。区域、图层和指标名称以技术方案为准。原文没有的刷新频率、告警数和地图点位不补。

## 绘制方式

- 大屏需要准确显示面板名称、指标和布局：用 HTML 按 16:9 画布绘制，再导出宽 2400px 的 PNG。这是投标正文的默认方式。
- 只表现控制室或大屏现场氛围，且不读取具体数字：按 `.cursor/skills/imagegen/SKILL.md` 生成，用例 `ui-mockup` 或 `photorealistic-natural`，`aspect_ratio` 为 `16:9`。提示词要求屏幕内容不可读或无具体数字，避免伪造指标。

精确大屏和氛围照片是两种交付，不得互相替代。多个主题屏分别出图。

## 构图

精确大屏按原文分区：总览、地图或孪生场景、告警、设备状态。分区对齐，标题短。孪生场景只显示原文列出的对象。氛围图表现屏幕与环境的关系，不替代界面稿。

不使用架构图的上下分层，也不把网络拓扑画成大屏装饰。

## 禁止

虚构在线率、告警数量、轨迹和热力。用密集乱码模拟数据表格。添加粒子、霓虹边框和无关城市夜景。一张图拼接多块不同主题的大屏。

## 校验

面板名称和可见指标逐项对照原文。氛围图确认看不清伪造数字。说明写入 `bid_images/prompts/`，PNG 写入 `bid_images/generated/`。
