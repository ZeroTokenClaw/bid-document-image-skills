---
name: bid-quality-system
description: Designs one quality-management diagram at a time from 招标文件, 投标文件, or 技术方案. Use for 质量管理, 质量门禁, reviews, and QA activities. Draws with SVG. Do not use for test strategy, acceptance flow, or implementation roadmaps.
---

# 招投标质量管理图

一张图只表达一套质量活动。评审、检查单、缺陷关闭和质量门禁以质量方案为准。未规定的门禁不补。

活动按实施顺序横向排列。每个门禁写明进入条件和原文中的责任岗位。不把测试用例层级画进本图。

测试范围交给 `bid-test-strategy`。验收结论交给 `bid-acceptance`。项目阶段交给 `bid-implementation-roadmap`。

用 SVG 绘制并导出 PNG。不用图像模型。禁止虚构合格率和缺陷密度。说明写入 `bid_images/prompts/`，PNG 写入 `bid_images/generated/`。
