---
name: bid-data-model
description: Designs one data model diagram at a time from 招标文件, 投标文件, or 技术方案. Use for 概念模型, 逻辑模型, entities, and keys. Draws with SVG or Mermaid erDiagram. Do not invent fields or replace system data-flow diagrams.
---

# 招投标数据模型图

一张图只表达一个主题域的实体和关系。实体名、主键和关系以数据设计原文为准。没有字段清单时只画实体和已写明的关系，不补字段。

概念模型不写物理表名。逻辑模型只保留原文中的关键字段。一张图不同时混画概念、逻辑和物理三层。

系统间流向交给 `bid-data-relationship-diagram`。治理环节交给 `bid-data-governance-diagram`。

用 SVG 或 Mermaid `erDiagram` 绘制并导出 PNG。不用图像模型。禁止虚构表和枚举。源稿写入 `bid_images/prompts/`，PNG 写入 `bid_images/generated/`。
