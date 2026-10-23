---
name: bid-cicd
description: Designs one build-and-release pipeline diagram at a time from 招标文件, 投标文件, or 技术方案. Use for CI/CD, 持续集成, 构建发布, and pipeline stages. Draws with SVG. Do not invent tools or replace environment promotion.
---

# 招投标构建发布图

一张图只表达一条流水线。提交、构建、扫描、制品、部署和审批以工程方案为准。未点名的平台和扫描器不出现。

阶段从左到右排列。每个阶段写明输入和产物。人工审批只在原文要求时单独标出。失败回退只画原文规定的路径。

环境之间的晋级交给 `bid-environment-promotion`。服务安装位置交给 `bid-deployment-diagram`。

用 SVG 绘制并导出宽 2400px 的 PNG。不用图像模型。禁止虚构覆盖率门禁和发布频率。说明写入 `bid_images/prompts/`，PNG 写入 `bid_images/generated/`。
