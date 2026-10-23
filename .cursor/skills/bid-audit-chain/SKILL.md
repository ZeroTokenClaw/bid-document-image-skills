---
name: bid-audit-chain
description: Designs one audit and logging chain at a time from 招标文件, 投标文件, or 技术方案. Use for 审计链路, 日志采集, retention, and evidence flow. Draws with SVG. Do not invent retention periods or replace security architecture.
---

# 招投标审计链路图

一张图只表达一类日志或审计证据的路径。来源、采集、存储、查询和留存期限以安全或运维方案为准。没有期限时标“待确认”。

来源在左，审计查询在右。每个节点写明原文中的系统名。告警处置不展开成应急流程。

安全域交给 `bid-security-architecture`。日常运维环节交给 `bid-ops-architecture`。

用 SVG 绘制并导出宽 2400px 的 PNG。不用图像模型。禁止虚构不可篡改、区块链和保存年限。说明写入 `bid_images/prompts/`，PNG 写入 `bid_images/generated/`。
