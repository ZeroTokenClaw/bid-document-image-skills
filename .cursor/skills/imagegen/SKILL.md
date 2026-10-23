---
name: imagegen
description: Generates or edits one raster image at a time with Cursor's built-in GenerateImage tool, following the OpenAI imagegen workflow. Use for 文生图, 参考图编辑, 产品效果图, 机器人产品图, UI 氛围稿, 海报, 网站素材, 信息图视觉, and 数字孪生大屏氛围图. Do not use for 架构图, 流程图, 拓扑图, 部署图, or other precise labeled diagrams; those use the bid vector skills. The built-in tool needs no API key. Switch to an external image CLI only when the user explicitly asks.
---

# 图像生成

栅格配图使用 Cursor 内置 `GenerateImage`。这是 OpenAI 官方 `imagegen` 的默认路径：内置图像工具，不配置 `OPENAI_API_KEY`。官方说明见 [openai/skills imagegen](https://github.com/openai/skills/blob/main/skills/.system/imagegen/SKILL.md)。

精确文字和结构不走本技能。总表中用 SVG、HTML 或 Mermaid 的类型，分别使用对应的 `.cursor/skills/bid-*` 技能。已有图片的局部修改先执行 `bid-image-edit`。

## 选择方式

- 新建画面，或参考图只提供风格、构图、主体外观：`generate`。
- 修改已有画面并保留其余部分：`edit`。参考图放入 `reference_image_paths`，提示词写明只改什么、必须保持什么。
- 一次调用只生成一张。多张图多次调用，不把多张需求写进同一次生成。

## 调用

使用 `GenerateImage`：

- `description`：下面的结构化提示词，不少于具体主体、构图和禁止项。
- `aspect_ratio`：正文和网站横图 `16:9`，普通配图 `4:3`，方形产品图 `1:1`，竖版海报 `3:4` 或 `9:16`。
- `reference_image_paths`：参考图或被编辑的原图。有真实设备或界面参考时必须传入。
- `filename`：只写文件名，如 `IMG-001_机器人产品.png`。

招投标成图在生成后放入当前项目 `bid_images/generated/`。提示词原文放入 `bid_images/prompts/IMG-编号.md`。不覆盖已有文件；修改版使用新的版本名。

生成后检查主体、构图、文字、裁切和禁止项。不合格时只改一个问题并重新生成这一张。

## 提示词

提示词已经具体时，只整理结构，不追加新物体、品牌、口号或指标。提示词笼统时，只补充构图、用途和光效强度。

```text
Use case: <product-mockup | ui-mockup | photorealistic-natural | stylized-concept | infographic-diagram | logo-brand | illustration-story | text-localization | identity-preserve | precise-object-edit | lighting-weather | background-extraction | style-transfer | compositing | sketch-to-render>
Asset type: <标书插图 | 网站首屏 | 海报 | 产品图 | 界面氛围 | 大屏氛围>
Primary request: <这一张图的目的>
Input images: <图1：参考外观；图2：编辑对象>
Scene/backdrop: <场景>
Subject: <主体、数量、视角>
Style/medium: <摄影 | 产品渲染 | 简洁界面>
Composition/framing: <横版、主体位置、留白>
Lighting/mood: <克制棚拍或现场光>
Color palette: <主色 #1F3A4D，背景 #F7F8F6>
Text (verbatim): "<必须出现的短文字>"
Constraints: <必须保留的外观或布局>
Avoid: <乱码、水印、霓虹、粒子、虚构指标、未提及的设备>
```

参考图要保持同一台设备或同一个人时，写明使用参考图中的身份，不要另画一个相似主体。编辑时每轮都重复“只修改 X，保持 Y 不变”。

图像模型不稳定。大段中文、菜单、模块名、接口和性能指标不要放进画面；这些文字用矢量图或文档排版。画面里只保留必要的短标题，并逐字核对，错字则重做或改回矢量。

## 外部模型

内置工具失败时，告诉用户失败原因并停止。不自动改用 API、CLI 或其他模型。

只有用户明确要求切换外部模型时才使用：

- 多供应商切换或批量提示词文件：[baoyu-image-gen](https://github.com/guanyang/open-agent-hub/tree/main/skills/baoyu-image-gen)，支持 OpenAI、Google、OpenRouter、通义万象、智谱、即梦、Seedream 等，需要用户自己配置密钥。
- 科研概念图和视觉素材：[K-Dense generate-image](https://github.com/K-Dense-AI/scientific-agent-skills/tree/main/skills/generate-image)，通过 OpenRouter 调用，技术结构图仍用矢量技能。

不把上述仓库的脚本复制进本项目，也不在对话中索取完整密钥。
