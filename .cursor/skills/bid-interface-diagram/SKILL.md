---
name: bid-interface-diagram
description: Designs one bid-document interface diagram at a time from 招标文件, 投标文件, or 技术方案. Use for 接口关系, 系统对接, 对接边界, and named external interfaces. Draws with SVG. Do not use for sequence messages, data entities, or deployment diagrams.
---

# 招投标接口关系图

一张图只表达一组对接边界。系统名、接口名、方向和协议以接口清单为准。没有接口清单时，只画原文点名的对接，其余标“待确认”。

## 表达边界

接口图强调系统之间的对接点。调用先后交给 `bid-sequence-diagram`。数据实体和字段交给 `bid-data-relationship-diagram`。服务部署位置交给 `bid-deployment-diagram`。

## 构图

本系统放在中间或左侧，外部系统按对接方分列。每条对接用一条带接口名称的连线，箭头表示原文写明的主方向。协议、频率和认证方式只标注原文已给出的项。

对接方很多时按业务域拆成多张，不交叉堆叠。

## 绘制

用 SVG 绘制，再导出宽 2400px 的 PNG。系统名和接口名不小于 18px。不用图像模型生成接口图。

## 禁止

虚构接口、报文和厂家系统。把接口图画成网络拓扑。用无名称箭头表示未确认对接。

## 校验

每条连线都能对应接口清单中的一条记录。说明写入 `bid_images/prompts/`，PNG 写入 `bid_images/generated/`。
