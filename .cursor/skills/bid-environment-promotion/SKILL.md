---
name: bid-environment-promotion
description: Designs one environment-promotion diagram at a time from 招标文件, 投标文件, or 技术方案. Use for 环境晋级, 开发测试生产, and promotion gates. Draws with SVG. Do not invent environments or replace the deployment diagram.
---

# 招投标环境晋级图

一张图只表达制品从一个环境进入下一个环境的条件。开发、测试、预生产和生产只保留原文存在的环境。

环境从左到右排列。环境之间只写晋级条件、责任人和回退条件。环境内部的服务器和服务不展开。

流水线步骤交给 `bid-cicd`。运行位置交给 `bid-deployment-diagram`。

用 SVG 绘制并导出 PNG。不用图像模型。禁止虚构四套环境和自动发布能力。说明写入 `bid_images/prompts/`，PNG 写入 `bid_images/generated/`。
