---
name: bid-scene-illustration
description: Designs one bid-document scene or concept illustration at a time from 招标文件, 投标文件, or 技术方案. Use when the figure is a 场景示意图, 应用场景, 设备示意图, 概念视觉图, or 氛围图. Generates through the imagegen skill. Product renders use bid-product-render. Do not use for architecture, flowchart, topology, deployment, UI mockups, or dashboards.
---

# 招投标场景与设备配图

先阅读当前项目中该配图对应的原文，只生成这一张场景、设备或概念图。全套色彩基调与 `.cursor/skills/bid-document-image-design/SKILL.md` 一致，但构图按本图场景单独设计。

## 表达边界

本技能处理应用场景、现场设备示意、概念视觉和氛围图。单一产品、机器人产品图和白底图使用 `bid-product-render`。

架构图、流程图、拓扑图、部署图、数据关系图、数据治理图和项目实施图必须使用对应的矢量技能。界面稿和大屏有精确文字时使用 `bid-ui-mockup` 或 `bid-dashboard-visual`。

## 从原文提取

- 场景地点、使用者和要说明的业务动作。
- 原文点名的设备、外观特征和数量。
- 允许出现在画面中的系统名称。只保留能看清的短标签。
- 不得出现的内容：未中标品牌、未提及的设备、性能数字和接口参数。

参数未确认时，画面不写该参数。

## 构图

每张配图只表现一个场景或一件设备。按原文选择：

- 设备示意图：单一设备或原文规定的组合，正视或四分之三视角，背景干净。
- 应用场景：使用现场、使用者和设备的位置关系清楚，不堆砌无关人群。
- 概念视觉：只表达原文中的一个主题，保留可阅读的标题。

横版用于方案正文，竖版仅在封面或展板要求时使用。画面留出文档裁切边距。

## 生成

按 `.cursor/skills/imagegen/SKILL.md` 逐张生成，用例使用 `photorealistic-natural` 或 `stylized-concept`。有现场或设备照片时作为参考图，并保持原有外观。提示词写入 `bid_images/prompts/IMG-编号.md`，PNG 写入 `bid_images/generated/`。

画面正式、克制、真实，不使用科技光效、粒子、霓虹和虚构大屏数据。

## 禁止

一张图塞入多个无关场景。生成带小字参数的架构图冒充技术图。画面中出现乱码、错品牌、原文没有的传感器或机器人。用同一提示词只改标题批量出图。

## 校验

核对设备种类、数量和场景是否与原文一致，并检查文字是否可读、主体是否被裁切。不合格则只改这张图的提示词并重新生成。
