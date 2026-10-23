---
name: bid-data-classification
description: Designs one data classification diagram at a time from 招标文件, 投标文件, or 技术方案. Use for 数据分级, 数据分类, sensitivity levels, and handling rules. Draws with SVG. Do not invent grades or replace the data governance flow.
---

# 招投标数据分级分类图

一张图只表达一套分级或分类规则。类别、级别和对应的使用限制以数据安全方案为准。原文没有四级时不自行分成公开、内部、敏感和机密。

类别按列或按层排列。每个级别下列原文中的示例数据和管理要求。共享路径不在本图展开。

治理流程交给 `bid-data-governance-diagram`。权限授予交给 `bid-permission-model`。

用 SVG 绘制并导出 PNG。不用图像模型。禁止虚构数据量和脱敏算法。说明写入 `bid_images/prompts/`，PNG 写入 `bid_images/generated/`。
