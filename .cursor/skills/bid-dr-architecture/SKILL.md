---
name: bid-dr-architecture
description: Designs one disaster-recovery or backup diagram at a time from 招标文件, 投标文件, or 技术方案. Use for 容灾, 备份, 两地三中心, RPO, and RTO. Draws with SVG. Do not invent recovery metrics or replace the deployment diagram.
---

# 招投标容灾备份图

一张图只表达一套备份或容灾关系。生产、同城和异地只保留原文出现的站点。复制方向用箭头表示，RPO、RTO 和切换时间只标注原文给出的值。

生产站点与备份站点分成明确区域。区域内只列原文点名的系统和数据。没有指标时标“待确认”，不填行业常用值。

日常部署交给 `bid-deployment-diagram`。切换步骤交给 `bid-migration-plan`。

用 SVG 绘制并导出 PNG。不用图像模型。禁止虚构双活、两地三中心和存储品牌。说明写入 `bid_images/prompts/`，PNG 写入 `bid_images/generated/`。
