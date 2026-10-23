---
name: bid-topology-diagram
description: Designs one bid-document network or system topology diagram at a time from 招标文件, 投标文件, or 技术方案. Use when the figure is a 拓扑图, 网络拓扑, 系统拓扑, or shows zones, nodes, and links. Draws with SVG and exports PNG. Do not use for logical architecture layers, deployment inventories, or business flowcharts.
---

# 招投标拓扑图

先阅读当前项目中该拓扑的原文，只设计这一张拓扑图。色彩和字体遵循 `.cursor/skills/bid-document-image-design/SKILL.md`。

## 表达边界

拓扑图只表达节点、连接和区域边界。

- 逻辑分层和业务模块交给 `bid-architecture-diagram`。
- 软件部署到哪台主机交给 `bid-deployment-diagram`。
- 业务办理顺序交给 `bid-flowchart`。

## 从原文提取

- 区域：互联网、政务外网、专网、内网、安全域等，名称以原文为准。
- 节点：终端、网关、防火墙、交换机、服务器、平台和外部系统。
- 链路：谁与谁相连，链路类型或带宽仅在原文给出时标注。
- 安全控制点：防火墙、隔离、接入区，仅画原文点名的设备。

不补 IP、VLAN、端口或未出现的网络设备。未确认的节点标“待确认”，不写成既有设备。

## 构图

按网络区域分块，外部区域在上或在左，核心区域居中，受限区域单独成块。块用细线框加区域名，不使用立体机房。

节点在区域内对齐。链路用直线或直角折线，交叉处断开或绕行。链路标签短，放在线的一侧。一种线型只表示一种原文关系，并在图例中说明。

多张拓扑按网络层级或站点拆开，不得画成一张无法阅读的全网总图。

## 绘制

用 SVG 绘制，再导出宽 2400px 的 PNG。节点名不小于 18px。设备用统一线框符号区分终端、网络设备和服务器，不贴真实品牌商标，除非原文要求且已确认。

## 禁止

用图像模型生成拓扑图。虚构带宽、双机、安全设备或运营商链路。把部署清单或架构分层画进拓扑。使用光效和 3D 机柜墙。

## 校验

逐个区域核对节点是否来自原文，逐条链路核对两端是否写明。设计说明写入 `bid_images/prompts/IMG-编号.md`，PNG 写入 `bid_images/generated/`。
