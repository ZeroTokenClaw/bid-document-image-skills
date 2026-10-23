---
name: bid-user-journey
description: Designs one user journey map at a time from 招标文件, 投标文件, or 技术方案. Use for 用户旅程, 使用阶段, 触点, and experience stages. Draws with SVG. Do not use for service blueprints, flowcharts, or storyboards.
---

# 招投标用户旅程图

一张图只跟随一类用户。阶段、行为和触点以原文为准。痛点和机会只写方案里已经确认的内容。

阶段横向排列。每一阶段下列行为、触点和系统支持。不画前台后台分层，也不画判断菱形。

服务分层交给 `bid-service-blueprint`。操作步骤交给 `bid-flowchart`。现场分镜交给 `bid-storyboard`。

用 SVG 绘制并导出宽 2400px 的 PNG。不用图像模型。禁止虚构情绪分数和未写明的触点。说明写入 `bid_images/prompts/`，PNG 写入 `bid_images/generated/`。
