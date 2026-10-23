---
name: bid-org-chart
description: Designs one bid-document organization chart at a time from 招标文件, 投标文件, or 技术方案. Use for 组织架构, 项目组织, 岗位职责, and reporting lines. Draws with SVG. Do not use for system architecture, flowcharts, or implementation timelines.
---

# 招投标组织架构图

一张图只表达一套汇报关系。单位、岗位和分组名称以投标组织方案为准，不补充未任命的人员姓名。

## 构图

上级在上，下级在下。同一层级横向对齐。岗位放在矩形内，汇报用竖向直角连线。需要展示职责时，职责用不超过两行的文字放在岗位下方，不另做流程图。

招标人组织与投标人组织在原文中分开时，分成两张图。左右对照只在原文要求对照双方接口人时使用。

## 绘制

用 SVG 绘制，再导出宽 2400px 的 PNG。岗位名不小于 18px。不用图像模型生成组织图。

## 禁止

虚构部门、人员和资质。把系统模块画成岗位。使用头像、装饰旗帜和照片墙。

## 校验

每个岗位和汇报线都能指回组织方案。说明写入 `bid_images/prompts/`，PNG 写入 `bid_images/generated/`。
