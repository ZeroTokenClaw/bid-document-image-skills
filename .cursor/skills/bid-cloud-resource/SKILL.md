---
name: bid-cloud-resource
description: Designs one cloud-resource diagram at a time from 招标文件, 投标文件, or 技术方案. Use for 云资源, accounts, VPC, and resource boundaries. Draws with SVG. Do not invent cloud products or replace network topology and deployment diagrams.
---

# 招投标云资源图

一张图只表达一组账号、资源边界和资源类型。云厂商、区域、专有网络和资源名称以部署方案为准。未选型时使用“云资源待确认”，不填写具体产品。

账号或订阅作为外框，资源按网络、计算、存储、安全和运维分组。组内只列原文点名的资源。链路带宽和交换机不作为主体。

网络链路交给 `bid-topology-diagram`。服务落点交给 `bid-deployment-diagram`。

用 SVG 绘制并导出 PNG。不用图像模型。禁止虚构可用区数量和费用。说明写入 `bid_images/prompts/`，PNG 写入 `bid_images/generated/`。
