---
name: bid-knowledge-transfer
description: Designs one knowledge-transfer diagram at a time from 招标文件, 投标文件, or 技术方案. Use for 知识转移, handover materials, shadowing, and operations takeover. Draws with SVG. Do not invent courses or replace the training plan.
---

# 招投标知识转移图

一张图只表达一次移交。移交物、移交对象、陪产或跟岗、签收和未完成项以移交方案为准。

移交物放在左侧，接收岗位放在右侧，中间写移交方式。培训课程和考核不展开。

课程体系交给 `bid-training-plan`。运维接管后的日常流程交给 `bid-ops-architecture`。

用 SVG 绘制并导出 PNG。不用图像模型。禁止虚构文档册数和独立运维日期。说明写入 `bid_images/prompts/`，PNG 写入 `bid_images/generated/`。
