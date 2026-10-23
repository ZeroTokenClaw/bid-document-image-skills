---
name: bid-product-render
description: Designs one product, robot, or equipment render at a time for bid documents from 招标文件, 投标文件, or 技术方案. Use for 产品效果图, 机器人产品图, 设备白底图, 包装图, and transparent cutouts. Generates through the imagegen skill. Do not use for architecture, flowchart, topology, deployment, or scene-wide illustrations.
---

# 招投标产品效果图

只设计原文中的一件产品、一台机器人或一套明确组合。先摘录外观、组成和数量，再按 `.cursor/skills/imagegen/SKILL.md` 生成。用例使用 `product-mockup`。

## 构图

每张图只放一个主体。按用途选择一种，不与场景图或架构图共用布局：

- 目录图：四分之三视角，主体居中，背景使用 `#F7F8F6`。
- 结构展示：正视，只显示原文列出的可见部件。
- 白底抠图：用例 `background-extraction`，主体完整，边缘不被裁切。
- 包装图：只在原文要求包装时制作，包装文字只用已确认的产品名。

默认 `aspect_ratio` 为 `1:1`。需要与文字并排时用 `4:3`，主体偏向一侧并留出空白。

项目里已有该产品照片时，把照片作为参考图。提示词要求保持参考中的外形和比例，只调整背景、视角或光线。没有照片时，不补充品牌标志和未记载的传感器、屏幕、轮组或机械臂。

## 禁止

虚构性能数字、接口名和认证标志。一张图排列多个无关产品。使用霓虹、粒子和发光地面。把产品图画成系统架构或大屏界面。

## 校验

对照原文核对产品类型、部件数量和朝向。文字只能是已确认的短名称，错字则重做这一张。提示词写入 `bid_images/prompts/`，成图写入 `bid_images/generated/`。
