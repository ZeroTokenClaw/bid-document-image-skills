---
name: bid-data-relationship-diagram
description: Designs one bid-document data relationship diagram at a time from 招标文件, 投标文件, or 技术方案. Use when the figure is a 数据关系图, 数据流图, 实体关系, 数据流向, or shows data sources, entities, and destinations. Draws with SVG or Mermaid and exports PNG. Do not use for data-governance lifecycles, system architecture, or business flowcharts.
---

# 招投标数据关系图

先阅读当前项目中该数据关系的原文，只设计这一张图。色彩和字体遵循 `.cursor/skills/bid-document-image-design/SKILL.md`。

## 表达边界

数据关系图只表达数据实体、来源、处理环节和去向。

- 数据标准、质量和目录治理交给 `bid-data-governance-diagram`。
- 系统模块分层交给 `bid-architecture-diagram`。
- 业务审批步骤交给 `bid-flowchart`。

## 从原文提取

- 数据对象或实体名称。
- 来源系统、处理系统、存储和消费方。
- 原文写明的字段、主键或关联。没有字段表时不编造字段。
- 流转方向：采集、交换、加工、查询或回写。

未确认的数据对象标“待确认”。

## 构图

来源放左侧，处理放中间，存储和去向放右侧。实体用矩形，系统用分组框，数据流用带标签的箭头。

若原文是实体关系而不是系统间数据流，改用实体框和关系线，关系名放在线上，不画系统分层。两种构图不得叠在同一张图里；原文同时要求时拆成两张。

## 绘制

系统间数据流用 SVG。实体关系可用 Mermaid `erDiagram`，再导出 PNG。默认横版，宽 2400px。字段列表过长时只保留原文点名的关键字段，其余在设计说明中记录，不缩小到不可读。

## 禁止

用图像模型生成此图。虚构数据表、字段、接口报文或交换频率。把数据治理流程画进关系图。

## 校验

每条箭头的起点和终点都能在原文找到。设计说明写入 `bid_images/prompts/IMG-编号.md`，PNG 写入 `bid_images/generated/`。
