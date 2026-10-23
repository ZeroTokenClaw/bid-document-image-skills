---
name: bid-state-diagram
description: Designs one state diagram at a time from 招标文件, 投标文件, or 技术方案. Use for 状态图, 状态流转, and lifecycle transitions. Draws with Mermaid stateDiagram-v2 and exports PNG. Do not use for business flowcharts or sequence diagrams.
---

# 招投标状态图

一张图只描述一个对象的状态生命周期。状态名和触发条件以原文为准。

每个状态只出现一次。转换标注触发条件，原文没有条件时不补。起点和终点只在原文存在初态、终态时画出。

业务流程中的人和审批交给 `bid-flowchart`。系统调用顺序交给 `bid-sequence-diagram`。

用 Mermaid `stateDiagram-v2` 绘制，再导出 PNG。不用图像模型。禁止虚构驳回、超时和归档状态。源稿写入 `bid_images/prompts/`，PNG 写入 `bid_images/generated/`。
