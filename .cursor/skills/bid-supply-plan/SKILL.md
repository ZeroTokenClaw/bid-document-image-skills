---
name: bid-supply-plan
description: Designs one supply and delivery diagram at a time from 招标文件, 投标文件, or 技术方案. Use for 供货计划, 到货, warehousing, and on-site handover. Draws with SVG. Do not invent lead times, brands, or quantities.
---

# 招投标供货到货图

一张图只覆盖一批或一类物资。采购、生产、运输、到货验收和安装交接以供货方案为准。数量、品牌和周期没有原文时标“待确认”。

环节从左到右排列。每个环节写明责任方和交付凭证。设备外观和机柜位置不在本图展开。

现场点位交给 `bid-site-layout`。安装后的部署交给 `bid-deployment-diagram`。项目总进度交给 `bid-gantt`。

用 SVG 绘制并导出 PNG。不用图像模型。禁止虚构物流时效和库存。说明写入 `bid_images/prompts/`，PNG 写入 `bid_images/generated/`。
