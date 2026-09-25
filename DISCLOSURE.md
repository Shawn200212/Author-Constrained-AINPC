# Public disclosure scope / 公开范围

This file sets out what this repository discloses, what it never discloses and what stays in private development records, followed by the limits of these boundaries. It was revised on 24 September 2026, when dated method notes were added.

## At a glance

Added on 25 September 2026. Each kind of material sits in exactly one column; the sections below give the detail.

| Material | Public in this repository | Private development records | Never published |
|---|---|---|---|
| Research question, approach and the author's role | Front page overview | Detailed plans | — |
| How parts of the prototype work | Dated, text-only method notes | Interface specifications, rule parameters and corrections | — |
| Scene images | Three curated development stills on the front page | Other development frames, reduced in size | Full-size original frames |
| Diagrams | One conceptual responsibility diagram per language | Figures and charts drawn from data | — |
| Numbers | Dates and commit ids only | Measurements, parameter values and counts, each tied to an exact commit | — |
| Names | Platforms, named generically | Assets, clips, characters, runs, fields and version labels | — |
| Code | None | Source code | Third-party source assets |
| Logs | None | Selected run records | Raw logs |
| Evaluation | Principles the work has adopted | Development diagnostics | Scoring instruments and anchors, individual ratings, participant information |
| Unpublished research | None | None | Manuscripts, review correspondence, unpublished findings |
| Credentials and local file paths | None | None | Always excluded |

Anything not listed is treated as private until it has been reviewed for disclosure. Nothing moves into the public column unless the author has approved the exact change.

## What this repository discloses

The front page mirrors the project website: the research question, restaurant context, author's contribution, a conceptual responsibility diagram and three scene images. They are not development logs or a complete research artifact.

The diagram describes information categories and responsibilities. It omits operational rules, actual JSON fields and payloads, prompts, thresholds and repair-selection algorithms. Some depicted paths remain in development. The screenshots show a prototype setting. They do not establish complete autonomous service, synchronized speech, execution reliability or player benefits.

Dated, text-only [method notes](docs/methods/README.md) supplement this overview. They describe what parts of the prototype do, what information they use and why they are designed that way, and they publish no data, numbers, parameters, field names, source code or asset names. They describe some runtime behavior in words, but never its parameter values or source code. Notes may state evaluation principles; protocols, evaluation details and results stay private. Each note is a dated method revision, not a development log, and states its status and what it does not claim. Contract behavior is described as specified intent, not as a demonstrated property.

## What this repository never discloses

Method notes never give parameter values, thresholds, formulas, numeric or training results, field names, schemas, file formats, prompts, repair-selection logic, source code or engineering version labels, and they never name assets, clips, animation sources, characters or runs.

No data, measurements, results, counts or data-derived charts are published, nor any trained model or anything extracted from third-party assets. Third-party assets are named only generically, and naming a platform implies no endorsement.

The public materials exclude scoring instruments and anchors, calibration examples, individual ratings, analysis tables, unpublished findings, manuscripts, review correspondence, participant information, credentials, Unreal project source and third-party source assets. Private correspondence is not permission to publish its contents. Raw logs and local file paths are not published either.

## What stays in private development records

Run records, measurements, parameter values, detailed interface specifications (names, fields and types), evidence frames, correction details, sign-off evidence and source code stay in private development records. General lessons may be stated as design rules without incident detail. Detailed debugging and per-action progress belong in private development records, outside both public channels. A method note's revision table may cite such a record by commit id only; the record itself is not public.

## Limits of these boundaries

These boundaries reduce exposure of implementation and research materials; they cannot prevent others from imitating a publicly described idea. Attribution and rights notices do not make public information confidential. Previous public commits and tags remain accessible: removing a file from the current presentation does not retract its earlier disclosure.

---

本文件说明本仓公开什么、始终不公开什么、哪些内容留在私有开发记录中，最后说明这些边界的限度。2026 年 9 月 24 日补充方法说明时修订。

## 一览

2026 年 9 月 25 日补充。每一类材料只落在一栏；细则见下面各节。

| 材料 | 本仓公开 | 私有开发记录 | 永不公开 |
|---|---|---|---|
| 研究问题、思路与本人贡献 | 首页概览 | 详细计划 | — |
| 原型各部分如何工作 | 按日期发布的纯文字方法说明 | 接口规格、规则参数与更正 | — |
| 场景图片 | 首页三张精选开发静帧 | 其余开发画面（缩小后） | 全尺寸原图 |
| 图示 | 每种语言一张概念职责图 | 由数据画出的图与图表 | — |
| 数字 | 只有日期与提交编号 | 测量值、参数值与计数，逐一绑定确切提交 | — |
| 名称 | 平台，只作泛称 | 资产、片段、角色、运行、字段与版本号 | — |
| 代码 | 无 | 源码 | 第三方源资产 |
| 日志 | 无 | 选定的运行记录 | 原始日志 |
| 评估 | 已采纳的评估原则 | 开发诊断 | 评分工具与锚点、逐条评分、参与者资料 |
| 未公开的研究材料 | 无 | 无 | 稿件及相关往来、未公开结果 |
| 凭据与本机文件路径 | 无 | 无 | 一律排除 |

未列出的材料在完成披露审查之前一律按私有处理。任何内容都要经作者核准确切改动，才会进入“本仓公开”一栏。

## 本仓公开的内容

首页概览与项目网页一致：研究问题、餐厅情境、本人贡献、概念职责图和三张场景图，不作为开发日志或完整研究材料。

公开图只解释信息类别与职责，不提供可复现实现的规则、字段、提示词、阈值或修复选择算法；部分路径仍在开发。截图呈现原型场景，不证明完整自主服务、语音同步、执行可靠性或玩家收益。

按日期发布的纯文字[方法说明](docs/methods/README.md)另作补充。方法说明只讲各部分做什么、用什么信息、为什么这样设计；不公开数据、数值、参数、字段、源码与资产名。部分运行时行为用文字描述，但不给出参数值或源码。方法说明可以陈述评估原则；具体协议、评估细节与结果不公开。每篇说明是一次带日期的方法修订，不是开发日志，并写明状态与不声称的内容；约定行为按“规定的意图”描述，不代表已被证明。

## 本仓始终不公开的内容

方法说明不给出参数值、阈值、公式、数值或训练结果、字段名、数据结构、文件格式、提示词、修复选择逻辑、源码或工程版本号，也不点名资产、片段、动画来源、角色或运行。

不发布任何数据、测量值、结果、计数或由数据生成的图表，也不发布训练得到的模型或从第三方资产提取的任何内容。第三方资产只以泛称提及，提及某个平台不代表其背书。

评分工具与锚点、校准案例、逐条数据、分析表、未公开结果、论文、审稿往来、参与者资料、凭据及工程源码均不纳入展示。私下交流过的资料也不自动获得公开授权。第三方源资产、原始日志与本机文件路径同样不公开。

## 留在私有开发记录中的内容

运行记录、测量值、参数值、详细接口规格（名称、字段与类型）、证据画面、更正细节、验收证据与源码都留在私有开发记录中。可推广的经验只以设计规则陈述，不附事件经过。局部动作验收与调试过程留在私有开发记录。方法说明的修订表最多以提交编号引用这类记录，记录本身不公开。

## 边界的限度

控制披露深度可以减少研究细节外露，但不能保证公开概念不被模仿；署名与权利声明也不能让已公开的信息变回保密。当前展示移除的旧图仍可能通过历史提交和标签访问，不能宣称已经撤回。
