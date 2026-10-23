---
name: bid-context-diagram
description: Designs one system context diagram at a time from 招标文件, 投标文件, or 技术方案. Use for 系统上下文, 系统边界, and external actors around one system. Draws with SVG. Do not use for internal architecture, interface catalogs, or sequence diagrams.
---

# 招投标系统上下文图

一张图只放一个被建系统。系统内部模块不展开。外部角色和外部系统只保留原文点名的对象。

被建系统放在中央。外部对象分布在四周，每条连线只标注原文中的交互名称。未写明的数据流不画箭头。

多个被建系统分别出图。用 SVG 绘制并导出宽 2400px 的 PNG，文字不小于 18px。不用图像模型。

禁止把上下文图画成分层架构、网络拓扑或接口清单。说明写入 `bid_images/prompts/`，PNG 写入 `bid_images/generated/`。
