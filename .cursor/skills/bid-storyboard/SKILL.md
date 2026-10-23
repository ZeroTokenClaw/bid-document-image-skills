---
name: bid-storyboard
description: Designs one visual storyboard at a time from 招标文件, 投标文件, or 技术方案. Use for 场景分镜, 操作分镜, and multi-panel application scenes. Each panel shows one confirmed action and is generated through the imagegen skill. Do not use for flowcharts, implementation timelines, or technical diagrams.
---

# 招投标场景分镜

一张分镜只讲一个场景。面板数量和每格动作以原文中的操作顺序为准，通常三到四格。业务判断、退回和角色泳道交给 `bid-flowchart`。

## 构图

面板等大，按从左到右或从上到下排列，并标注顺序号。每格只放一个动作、原文中的使用者和必要设备。格与格之间留白，不画流程箭头。

不在画面中写步骤说明。步骤名称放在面板外的可编辑标题中。

## 生成

每一格单独按 `.cursor/skills/imagegen/SKILL.md` 生成，用例 `illustration-story` 或 `photorealistic-natural`。全组分镜保持同一主体、同一地点和同一光线。有设备参考图时每格都传入，并保持外形。

## 禁止

增加原文没有的动作。在一格中放入多个场景。使用漫画夸张、对话气泡和虚构界面数据。用分镜代替流程图。

## 校验

核对格数、顺序、人物角色和设备是否与原文一致。各格提示词写入 `bid_images/prompts/`，成图写入 `bid_images/generated/`。
