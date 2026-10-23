---
name: bid-document-image-design
description: Inventories bid figures from the current project's 招标文件, 投标文件, and 技术方案, then designs each figure separately by following the matching type skill. Use when this project needs 标书配图, 架构图, 流程图, 拓扑图, 部署图, 数据关系图, 数据治理图, 项目实施图, 产品效果图, 界面稿, 信息图, 海报, 网站素材, or 数字孪生大屏. Raster images also follow .cursor/skills/imagegen/SKILL.md. Do not design every figure from this workflow alone, merge figures, or invent technical facts.
---

# 模式：招投标文档图片设计与生成

## 项目范围

本技能位于当前项目 `.cursor/skills/bid-document-image-design/`。交付物只写入当前项目根目录的 `bid_images/`。

执行前必须在当前项目中查找并阅读：

- 招标文件
- 投标文件
- 技术方案
- 与上述文件配套的附件、图纸和已有配图

从这些资料中分别识别架构图、流程图、拓扑图、部署图和标书配图。每一张图单独建立清单记录，单独摘录原文依据（文件名、章节、原图名或原文要求），单独确定构图，单独生成，单独校验。

同一份资料里已经分开要求的图，不得合并。没有读到对应原文时，不得按通用招投标模板出图，也不得编造模块、设备、指标或接口。当前项目中找不到招标文件、投标文件或技术方案时，先列出已检索范围和缺失项，停止生成。

## 图形类型技能

判定每张图的类型后，必须先阅读并执行对应技能，再单独设计。不得只用本流程代替类型设计。一张图只选一个主类型；原文把架构和部署写成两张图时，拆成两张，分别走对应技能。

| 类型 | 技能路径 |
| --- | --- |
| 架构图 | `.cursor/skills/bid-architecture-diagram/SKILL.md` |
| 流程图 | `.cursor/skills/bid-flowchart/SKILL.md` |
| 拓扑图 | `.cursor/skills/bid-topology-diagram/SKILL.md` |
| 部署图 | `.cursor/skills/bid-deployment-diagram/SKILL.md` |
| 数据关系图 | `.cursor/skills/bid-data-relationship-diagram/SKILL.md` |
| 数据治理图 | `.cursor/skills/bid-data-governance-diagram/SKILL.md` |
| 项目实施图、时间轴 | `.cursor/skills/bid-implementation-roadmap/SKILL.md` |
| 场景、设备、概念配图 | `.cursor/skills/bid-scene-illustration/SKILL.md` |
| 产品效果、机器人产品、白底图 | `.cursor/skills/bid-product-render/SKILL.md` |
| 界面设计稿 | `.cursor/skills/bid-ui-mockup/SKILL.md` |
| 信息图 | `.cursor/skills/bid-infographic/SKILL.md` |
| 海报、封面 | `.cursor/skills/bid-poster/SKILL.md` |
| 网站素材 | `.cursor/skills/bid-website-asset/SKILL.md` |
| 数字孪生大屏 | `.cursor/skills/bid-dashboard-visual/SKILL.md` |
| 线框图 | `.cursor/skills/bid-wireframe/SKILL.md` |
| 标识 | `.cursor/skills/bid-logo/SKILL.md` |
| 图标 | `.cursor/skills/bid-icon/SKILL.md` |
| 组织架构 | `.cursor/skills/bid-org-chart/SKILL.md` |
| 时序图 | `.cursor/skills/bid-sequence-diagram/SKILL.md` |
| 安全架构 | `.cursor/skills/bid-security-architecture/SKILL.md` |
| 机房与机柜布置 | `.cursor/skills/bid-room-layout/SKILL.md` |
| 接口关系 | `.cursor/skills/bid-interface-diagram/SKILL.md` |
| 现状与目标对照 | `.cursor/skills/bid-comparison-diagram/SKILL.md` |
| 系统上下文 | `.cursor/skills/bid-context-diagram/SKILL.md` |
| 业务架构 | `.cursor/skills/bid-business-architecture/SKILL.md` |
| 功能结构 | `.cursor/skills/bid-function-tree/SKILL.md` |
| 状态图 | `.cursor/skills/bid-state-diagram/SKILL.md` |
| 用例图 | `.cursor/skills/bid-usecase-diagram/SKILL.md` |
| 甘特图 | `.cursor/skills/bid-gantt/SKILL.md` |
| 工作分解 | `.cursor/skills/bid-wbs/SKILL.md` |
| 责任矩阵 | `.cursor/skills/bid-raci/SKILL.md` |
| 运维体系 | `.cursor/skills/bid-ops-architecture/SKILL.md` |
| 容灾备份 | `.cursor/skills/bid-dr-architecture/SKILL.md` |
| 点位分布 | `.cursor/skills/bid-site-layout/SKILL.md` |
| 迁移切换 | `.cursor/skills/bid-migration-plan/SKILL.md` |
| 服务蓝图 | `.cursor/skills/bid-service-blueprint/SKILL.md` |
| 信息架构、菜单 | `.cursor/skills/bid-ia-sitemap/SKILL.md` |
| 应急响应 | `.cursor/skills/bid-emergency-plan/SKILL.md` |
| 培训体系 | `.cursor/skills/bid-training-plan/SKILL.md` |
| 用户旅程 | `.cursor/skills/bid-user-journey/SKILL.md` |
| 质量管理 | `.cursor/skills/bid-quality-system/SKILL.md` |
| 测试策略 | `.cursor/skills/bid-test-strategy/SKILL.md` |
| 验收 | `.cursor/skills/bid-acceptance/SKILL.md` |
| 风险矩阵 | `.cursor/skills/bid-risk-matrix/SKILL.md` |
| 构建发布 | `.cursor/skills/bid-cicd/SKILL.md` |
| 环境晋级 | `.cursor/skills/bid-environment-promotion/SKILL.md` |
| 数据模型 | `.cursor/skills/bid-data-model/SKILL.md` |
| 数据分级分类 | `.cursor/skills/bid-data-classification/SKILL.md` |
| 权限模型 | `.cursor/skills/bid-permission-model/SKILL.md` |
| 审计链路 | `.cursor/skills/bid-audit-chain/SKILL.md` |
| 云资源 | `.cursor/skills/bid-cloud-resource/SKILL.md` |
| 存储架构 | `.cursor/skills/bid-storage-architecture/SKILL.md` |
| 集成架构 | `.cursor/skills/bid-integration-architecture/SKILL.md` |
| 访问矩阵 | `.cursor/skills/bid-access-matrix/SKILL.md` |
| 服务等级 | `.cursor/skills/bid-sla-service/SKILL.md` |
| 人员进场 | `.cursor/skills/bid-staffing-plan/SKILL.md` |
| 知识转移 | `.cursor/skills/bid-knowledge-transfer/SKILL.md` |
| 供货到货 | `.cursor/skills/bid-supply-plan/SKILL.md` |
| 场景分镜 | `.cursor/skills/bid-storyboard/SKILL.md` |
| 已有图片的局部编辑 | `.cursor/skills/bid-image-edit/SKILL.md` |
| 栅格图生成 | `.cursor/skills/imagegen/SKILL.md` |

全套图片共用同一色彩，但布局必须按类型技能区分。背景 `#F7F8F6`，主色 `#1F3A4D`，层次色 `#2E5A73`、`#4E7C8A`、`#D6E2E6`，正文 `#1C1C1C`，连线 `#5C6B73`。字体使用微软雅黑或思源黑体。矢量结构图不使用光效、3D 和装饰性图标。产品、场景、海报和网站素材只使用克制的棚拍或现场光。栅格配图先按类型技能确定构图，再按 `imagegen` 调用内置生成工具。

## 一、任务目标

为招投标文件中的每一张图片单独进行专业设计，并生成可直接插入 Word、PPT、PDF 的高质量图片。

必须逐图设计、逐图生成、逐图校验。禁止将多张图合并为一张总图，禁止所有图片套用相同布局，禁止仅输出图片生成建议或提示词而不执行生成。

## 二、执行流程

1. 全面检查当前项目中的招标文件、投标文件、技术方案及现有附件，识别所有需要设计或优化的图片。架构图、流程图、拓扑图、部署图和标书配图各自单独列入清单。
2. 建立《图片设计清单》，为每张图片分配唯一编号，记录所属章节、图片名称、表达目的、核心内容、图形类型、设计方案、原文依据、生成状态及校验结果。
3. 根据每张图片的业务含义选定类型技能，按该技能单独编写设计说明或图像提示词。内容只使用该图自己的原文依据。
4. 逐张调用可用的图像生成或绘图工具完成设计，不得用一张图片代替多张图片。
5. 检查每张图片的内容准确性、视觉质量、文字可读性、布局完整性及与投标方案的一致性。
6. 对不合格图片单独修改并重新生成，直至满足验收标准。

## 三、图片设计原则

1. 业务准确：严格依据招标要求、投标方案和已确认的技术资料，不得编造功能、设备、性能指标、接口或技术能力。
2. 一图一设计：每张图片均须有独立的构图、视觉层次、布局和表达重点，根据内容决定采用架构图、流程图、拓扑图、数据关系图、时间轴、场景示意图或其他适当形式。
3. 专业美观：采用现代企业级信息可视化风格，布局清晰、对齐规范、层次明确、留白合理，符合大型项目招投标材料的正式、严谨风格。
4. 逻辑清晰：系统架构突出层级与依赖关系，业务流程突出步骤与分支，数据流突出来源、处理与去向，实施路线突出阶段、任务与交付物。
5. 内容可读：图片中的标题、模块名称、关键标签和注释应准确、清晰、完整，不得出现乱码、错别字、重叠文字、无意义字符或被裁切的内容。
6. 风格统一但不重复：全套图片统一色彩体系、字体风格、图标规范和视觉基调，但根据各图用途采用不同布局。
7. 适配文档：根据实际插入场景选择横版、竖版或其他合理比例，保证缩放后仍具备足够的阅读性。
8. 避免装饰过度：禁止无意义的科技光效、冗余装饰、虚假数据、无关图标及与项目无关的场景元素。

## 四、每张图片的独立设计要求

针对每张图片，必须分别完成以下工作：

- 明确图片要解决的问题及目标读者。
- 从招标文件、投标文件或技术方案中提取必须呈现的业务实体、模块、步骤、关系和关键数据，并记下出处。
- 选择最合适的图形类型与构图。架构图、流程图、拓扑图、部署图和标书配图不得共用同一布局。
- 确定标题、主视觉、内容分区、连接关系、色彩及视觉层级。
- 编写专属图像生成提示词，明确禁止出现的错误。
- 调用图像生成或绘图工具生成图片。
- 检查生成结果，并根据实际问题进行针对性修改。

不同类型图片应采用不同的设计策略。例如，技术架构图强调层次与模块关系；业务流程图强调流程方向、条件分支与闭环；系统部署图强调设备、网络、服务及部署边界；数据治理图强调数据来源、处理链路与质量控制；项目实施图强调阶段、里程碑、交付物和验收节点。

## 五、文字与技术图表要求

对于包含大量专业文字、精确模块名称、接口字段、技术参数、箭头关系或复杂拓扑的图片，优先采用可编辑的 SVG、HTML 或 Mermaid 等方式绘制，再导出高清 PNG；不要强制依赖图像生成模型直接绘制复杂文字和精确结构。

对于产品效果图、应用场景图、设备示意图、概念视觉图和氛围图，可使用图像生成模型生成。

涉及真实设备、系统模块、技术参数和招标指标时，必须以原始资料为准。对于尚未确认的信息，应明确标记待确认，不得自行补全为事实。

## 六、交付物

1. 图片设计清单：覆盖所有识别出的图片及其生成、校验状态。
2. 独立图片文件：每张图片单独保存，使用统一编号和有意义的文件名。
3. 图片提示词：每张图片对应一份独立提示词，便于复用和修改。
4. 图片索引：记录图片编号、图片名称、所属章节、文件路径及用途。
5. 校验报告：记录内容准确性、文字可读性、布局质量、修改记录及最终状态。

交付目录为当前项目根目录：

bid_images/
├── 01_图片设计清单.xlsx
├── 02_图片索引.md
├── prompts/
│   ├── IMG-001.md
│   ├── IMG-002.md
│   └── ...
├── generated/
│   ├── IMG-001_总体技术架构.png
│   ├── IMG-002_业务流程.png
│   └── ...
└── review/
    └── 图片校验报告.md

## 七、验收标准

- 图片数量与设计清单一致，不遗漏任何计划制作的图片。
- 每张图片均具有独立设计方案、原文依据和对应提示词。
- 图片表达准确，与招标文件和投标技术方案一致。
- 架构图、流程图、拓扑图、部署图和标书配图均按资料中的独立需求分别成图。
- 不存在明显乱码、错字、内容重叠、结构断裂或画面裁切。
- 图片风格统一、布局清晰，适合正式投标材料。
- 所有图片均有明确文件名、保存路径和校验状态。
- 未实际生成或未通过校验的图片必须明确标记，不得虚报完成。

## 八、执行约束

先盘点全部图片需求，再逐张设计与生成。优先完成最影响技术方案理解和评审判断的图片，随后按清单继续执行。允许分批处理，但必须持续更新清单，直至所有任务完成。

不得擅自修改项目技术方案，不得虚构技术能力，不得跳过图片设计直接批量套模板，不得在未实际执行的情况下声称图片已生成。
