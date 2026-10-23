---
name: bid-business-architecture
description: Designs one business architecture diagram at a time from 招标文件, 投标文件, or 技术方案. Use for 业务架构, 业务能力, 业务域, and user groups. Draws with SVG. Do not use for technical layers, function trees, or flowcharts.
---

# 招投标业务架构图

一张图只表达业务域、业务能力和使用对象。技术组件、服务器和接口不放进本图。

按原文中的业务域分栏。栏内只放该域已经列出的能力。使用对象放在对应能力外侧，连线表示原文写明的服务关系。没有的域不补。

不得套用技术架构的上下五层。用 SVG 导出宽 2400px 的 PNG。不用图像模型。

禁止虚构业务中台、共享能力和组织部门。说明写入 `bid_images/prompts/`，PNG 写入 `bid_images/generated/`。
