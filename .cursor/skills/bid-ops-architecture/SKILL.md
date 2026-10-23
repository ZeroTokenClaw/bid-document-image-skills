---
name: bid-ops-architecture
description: Designs one operations architecture diagram at a time from 招标文件, 投标文件, or 技术方案. Use for 运维体系, 监控告警, 服务台, and operations handover. Draws with SVG. Do not use for deployment, security architecture, or emergency flowcharts.
---

# 招投标运维体系图

一张图只表达运维对象、值班或服务流程和原文写明的工具。监控、告警、事件、变更、巡检只保留方案中实际包含的环节。

对象放在左侧，处理环节横向排列，工具或岗位作为环节下方的短标签。不画机房平面，不展开安全域。

部署位置交给 `bid-deployment-diagram`。安全控制交给 `bid-security-architecture`。故障升级步骤交给 `bid-emergency-plan`。

用 SVG 绘制并导出宽 2400px 的 PNG。不用图像模型。禁止虚构监控平台、告警阈值和服务等级数值。说明写入 `bid_images/prompts/`，PNG 写入 `bid_images/generated/`。
