---
name: bid-website-asset
description: Designs one website visual at a time for a bid or product site from 招标文件, 投标文件, or 技术方案. Use for 网站素材, 首屏图, banner, and page heroes. Generates through the imagegen skill with space reserved for real text. Do not use for architecture, flowchart, topology, deployment, or UI pages that require exact labels.
---

# 招投标网站素材

一张图只做一个网站位置，例如首屏、栏目横幅或功能配图。素材内容来自投标方案中已经写明的产品、场景或服务，不为主题另编功能。

## 构图

首屏和横幅使用 `16:9`。主体放在一侧，另一侧留出连续空白，方便网页标题和按钮用真实文字排版。栏目配图使用 `4:3`，只表现该栏目的一个对象。

生成执行 `.cursor/skills/imagegen/SKILL.md`。提示词写明 `no text, no logo, no watermark`，除非原文要求画面内出现已确认的短名称。不生成带小字导航的整页网站截图；精确页面使用 `bid-ui-mockup`。

已有产品照片时作为参考图，保持产品外形。没有照片时不添加品牌标志。

## 禁止

虚构界面数据和客户案例。一张横幅塞入多个栏目。使用霓虹粒子背景。把拓扑图或架构图栅格化后当作网站装饰。

## 校验

检查主体是否完整、留白是否可排版、画面有无乱码。每个文件只对应一个网页位置。提示词写入 `bid_images/prompts/`，成图写入 `bid_images/generated/`。
