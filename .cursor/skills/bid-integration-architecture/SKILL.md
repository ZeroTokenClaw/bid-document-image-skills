---
name: bid-integration-architecture
description: Designs one integration-architecture diagram at a time from 招标文件, 投标文件, or 技术方案. Use for 集成架构, API gateway, bus, and integration styles. Draws with SVG. Do not invent middleware or replace interface catalogs and sequence diagrams.
---

# 招投标集成架构图

一张图只表达一种集成方式。点对点、网关、总线或文件交换以集成方案为准。原文没有总线时不补企业服务总线。

接入方分列两侧，集成通道放在中间。通道上只标原文中的协议和集成模式。单个接口的报文和调用顺序不展开。

对接清单交给 `bid-interface-diagram`。一次调用交给 `bid-sequence-diagram`。

用 SVG 绘制并导出宽 2400px 的 PNG。不用图像模型。禁止虚构中台和适配器数量。说明写入 `bid_images/prompts/`，PNG 写入 `bid_images/generated/`。
