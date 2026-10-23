---
name: bid-deployment-diagram
description: Designs one bid-document deployment diagram at a time from 招标文件, 投标文件, or 技术方案. Use when the figure is a 部署图, 部署架构, 系统部署, or shows hosts, environments, services, and deployment boundaries. Draws with SVG and exports PNG. Do not use for logical architecture, network topology, or business flowcharts.
---

# 招投标部署图

先阅读当前项目中该部署方案的原文，只设计这一张部署图。色彩和字体遵循 `.cursor/skills/bid-document-image-design/SKILL.md`。

## 表达边界

部署图只表达运行环境、部署边界，以及服务或组件落在何处。

- 逻辑模块分层交给 `bid-architecture-diagram`。
- 网络设备和链路交给 `bid-topology-diagram`。
- 上线阶段和里程碑交给 `bid-implementation-roadmap`。

## 从原文提取

- 环境：开发、测试、生产，或原文中的云、机房、边端。只保留原文出现的环境。
- 部署单元：物理机、虚拟机、容器、终端、专有设备。
- 每个单元上的服务、组件或中间件，名称与原文一致。
- 访问方向和部署边界，如负载入口、数据库区、管理区。
- 数量、规格和可用部署方式。原文没有的规格写“待确认”，不填具体数字。

## 构图

按环境或机房分成大区，大区从左到右或从上到下对应访问路径。区内用分组框表示主机或集群，框内列出该主机上的服务。

服务与主机是包含关系，不用箭头表示“安装在”。箭头只表示原文写明的访问或同步方向。同一服务的主备或集群仅在原文说明时画出，并标注角色。

逻辑架构和部署图不得共用上下五层布局。

## 绘制

用 SVG 绘制，再导出宽 2400px 的 PNG。主机框、服务名和边界名称不小于 18px。规格用小字附在对应单元下方，不单独做装饰数据牌。

## 禁止

用图像模型生成部署图。虚构服务器数量、CPU、内存、中间件和高可用。把网络拓扑的交换机链路画成部署图主体。多环境挤成无法区分的一张图时，按环境拆图。

## 校验

每个服务都能指回原文中的部署位置。没有位置依据的服务不得出现。设计说明写入 `bid_images/prompts/IMG-编号.md`，PNG 写入 `bid_images/generated/`。
