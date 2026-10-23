---
name: bid-sla-service
description: Designs one service-level diagram at a time from 招标文件, 投标文件, or 技术方案. Use for SLA, 服务等级, response time, and service windows. Draws with SVG or HTML from confirmed values. Do not invent service targets.
---

# 招投标服务等级图

一张图只列出一类服务的等级承诺。服务项、响应时限、恢复时限和服务窗口以招标要求或投标承诺为准。没有数值时标“待确认”，不填写常见的 7×24 或四小时到场。

服务项按严重程度或服务类型排列，只使用原文中的分级。升级路径另见应急图，不在本图展开步骤。

应急步骤交给 `bid-emergency-plan`。日常运维环节交给 `bid-ops-architecture`。

用 SVG 或 HTML 绘制并导出 PNG。不用图像模型。禁止改写招标工期和服务罚款条件。说明写入 `bid_images/prompts/`，PNG 写入 `bid_images/generated/`。
