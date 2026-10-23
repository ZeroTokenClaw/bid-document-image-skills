---
name: bid-security-architecture
description: Designs one bid-document security architecture diagram at a time from 招标文件, 投标文件, or 技术方案. Use for 安全架构, 安全体系, 安全域, 等保控制, and protection measures. Draws with SVG. Do not use for network topology, system architecture, or deployment diagrams.
---

# 招投标安全架构图

一张图只表达一套安全边界和控制措施。区域、控制点和策略名称以安全方案或招标安全要求为准。

## 表达边界

安全架构图强调保护对象、安全域和控制措施。网络设备与链路交给 `bid-topology-diagram`。软件部署位置交给 `bid-deployment-diagram`。业务模块分层交给 `bid-architecture-diagram`。

## 构图

按安全域分块。外部访问放在外侧，核心资产放在内侧。控制点放在域边界上，并用短标签标出原文中的措施，如身份鉴别、访问控制、审计或传输保护。只画原文点名的措施。

多种控制关系用图例区分。不使用盾牌堆砌和放射状装饰。

## 绘制

用 SVG 绘制，再导出宽 2400px 的 PNG。域名和控制点文字不小于 18px。不用图像模型生成安全架构。

## 禁止

虚构等保级别、证书、防火墙型号和未提出的零信任能力。把安全图绘成城市或机房效果图。

## 校验

每个安全域和控制点都能指回原文。未确认的措施标“待确认”。说明写入 `bid_images/prompts/`，PNG 写入 `bid_images/generated/`。
