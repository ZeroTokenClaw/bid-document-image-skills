---
name: bid-storage-architecture
description: Designs one storage-architecture diagram at a time from 招标文件, 投标文件, or 技术方案. Use for 存储架构, hot and cold tiers, backup media, and data placement. Draws with SVG. Do not invent capacity or replace disaster-recovery diagrams.
---

# 招投标存储架构图

一张图只表达数据如何按层存放。在线、近线和归档只保留原文存在的层次。容量、副本数和介质只标注已经给出的值。

数据对象在左，存储层横向排列，访问方在对应层的上方。备份站点的复制关系不在本图展开。

容灾复制交给 `bid-dr-architecture`。数据实体交给 `bid-data-model`。

用 SVG 绘制并导出 PNG。不用图像模型。禁止虚构 TB 容量和存储品牌。说明写入 `bid_images/prompts/`，PNG 写入 `bid_images/generated/`。
