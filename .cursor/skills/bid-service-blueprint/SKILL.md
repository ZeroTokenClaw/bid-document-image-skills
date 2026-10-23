---
name: bid-service-blueprint
description: Designs one service blueprint at a time from 招标文件, 投标文件, or 技术方案. Use for 服务蓝图, frontstage and backstage actions, and support processes. Draws swim lanes with SVG. Do not use for system sequence diagrams or organization charts.
---

# 招投标服务蓝图

一张蓝图只覆盖一条服务。横向是原文中的服务步骤，纵向只保留原文能够区分的层，例如用户动作、前台、后台和支持系统。没有证据的层不画。

每个格子只放该步在该层的一个动作。层与层之间的依赖用短连线，不改成系统调用时序。

系统消息顺序交给 `bid-sequence-diagram`。岗位汇报交给 `bid-org-chart`。

用 SVG 绘制并导出 PNG。不用图像模型。禁止虚构接触点和等待时间。说明写入 `bid_images/prompts/`，PNG 写入 `bid_images/generated/`。
