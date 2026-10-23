---
name: bid-emergency-plan
description: Designs one emergency-response diagram at a time from 招标文件, 投标文件, or 技术方案. Use for 应急预案, 故障升级, incident levels, and response loops. Draws with SVG. Do not invent severity levels or replace the operations architecture.
---

# 招投标应急响应图

一张图只覆盖一类应急场景。事件等级、触发条件、响应岗位和升级时限以预案原文为准。没有等级划分时不自行分成四级。

左侧是发现与定级，中间是处置，右侧是恢复和复盘。升级走独立通道。每个节点标明负责岗位。闭环只在原文要求复查时画回起点。

日常运维环节交给 `bid-ops-architecture`。普通业务审批交给 `bid-flowchart`。

用 SVG 绘制并导出 PNG。不用图像模型。禁止虚构响应时长、值班电话和演练结论。说明写入 `bid_images/prompts/`，PNG 写入 `bid_images/generated/`。
