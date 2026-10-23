---
name: bid-data-governance-diagram
description: Designs one bid-document data governance diagram at a time from 招标文件, 投标文件, or 技术方案. Use when the figure is a 数据治理图, 数据治理体系, 数据质量, 数据目录, or shows governance roles, control points, and the data lifecycle. Draws with SVG and exports PNG. Do not use for entity-relationship diagrams, system architecture, or business flowcharts.
---

# 招投标数据治理图

先阅读当前项目中该治理方案的原文，只设计这一张图。色彩和字体遵循 `.cursor/skills/bid-document-image-design/SKILL.md`。

## 表达边界

数据治理图表达治理对象、管理职责、处理链路和质量控制点。

- 实体、字段和系统间流向交给 `bid-data-relationship-diagram`。
- 平台功能分层交给 `bid-architecture-diagram`。
- 项目实施阶段交给 `bid-implementation-roadmap`。

## 从原文提取

- 治理对象：数据源、主数据、元数据、指标或原文列出的数据域。
- 链路：采集、标准化、质检、目录、共享、应用中原文实际包含的环节。
- 控制点：质量规则、对账、审核、安全或授权。只标注原文有措施的位置。
- 责任角色。原文未划分角色时不画组织架构。

缺失的制度名称不补成已有制度。

## 构图

主链路横向排列。治理对象放在链路上方或左侧，质量控制点放在对应环节下方，用同一标记符号表示，不换成另一套流程布局。

责任角色只作为环节下方的短标签，不做泳道流程图。若原文以组织职责为主、处理链路为辅，改为左职责、右对象的对照布局，仍然只做这一张图的一种构图。

## 绘制

用 SVG 绘制，再导出宽 2400px 的 PNG。环节名和控制点文字不小于 18px。控制点与主环节用细线连接，避免叠字。

## 禁止

用图像模型生成此图。虚构数据标准、质量分数、目录数量或监管平台。画成普通业务流程图或数据表关系图。

## 校验

每个环节和控制点都能指回原文。设计说明写入 `bid_images/prompts/IMG-编号.md`，PNG 写入 `bid_images/generated/`。
