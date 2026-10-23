---
name: bid-sequence-diagram
description: Designs one bid-document sequence diagram at a time from 招标文件, 投标文件, or 技术方案. Use for 时序图, 调用顺序, 接口交互, and message order between systems. Draws with Mermaid sequenceDiagram and exports PNG. Do not use for business flowcharts, architecture layers, or data-relationship diagrams.
---

# 招投标时序图

一张图只表达一次交互。参与方、消息名称和先后顺序以接口或流程原文为准。

## 表达边界

时序图强调谁先调用谁，以及返回发生在哪一步。业务判断和长流程交给 `bid-flowchart`。系统分层交给 `bid-architecture-diagram`。数据实体交给 `bid-data-relationship-diagram`。

## 构图

参与方沿顶部横向排列，调用方在左，被调用方在右。生命线向下。同步调用用实线箭头，返回用虚线箭头。原文中的可选步骤或循环单独成组，并使用原文中的条件，不补充超时和重试，除非原文写明。

消息文字使用接口或动作原名。没有原名时标“待确认”，不编造字段。

## 绘制

用 Mermaid `sequenceDiagram` 绘制，导出 SVG 后再导出 PNG。参与方较多时拆成多张交互，不压缩到不可读。

## 禁止

虚构参与系统和报文。把时序图画成泳道流程图。用图像模型生成消息文字。

## 校验

从上到下核对每一条消息的发送方、接收方和顺序。源稿写入 `bid_images/prompts/`，PNG 写入 `bid_images/generated/`。
