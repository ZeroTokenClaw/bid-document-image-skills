---
name: bid-risk-matrix
description: Designs one risk matrix at a time from 招标文件, 投标文件, or 技术方案. Use for 风险矩阵, 概率影响, and named project risks. Draws an editable table with HTML. Do not invent probability, impact, or mitigations.
---

# 招投标风险矩阵

一张图只列入已经识别的风险。行是风险，列是原文给出的可能性、影响、责任人和应对。缺少的量化等级保持空白或标“待确认”，不按经验打分。

风险过多时按实施、技术、数据或供应拆成多张。组织汇报不画进矩阵。

责任岗位的汇报线交给 `bid-org-chart`。应急处置步骤交给 `bid-emergency-plan`。

用 HTML 表格绘制再导出 PNG，文字可阅读。不用图像模型。禁止用红黄绿暗示原文没有的等级。说明写入 `bid_images/prompts/`，PNG 写入 `bid_images/generated/`。
