# Reading the prototype / 原型导览

[English overview](../README.md) · [中文首页](../README.zh-CN.md)

## Reading the work

AINPC examines how authors can shape improvisation by game characters and inspect the relation between a proposed action and its outcome. The restaurant brings shared objects, bodily actions and social expectations together in an observable scene.

YUISIU ZHANG is responsible for the research framework, interaction design, UE prototype integration and development verification. The prototype combines this work with Unreal Engine, MetaHuman, speech and language-model services, and third-party character, animation and environment assets. Development verification does not establish independently evaluated effectiveness.

## Responsibilities in the design

| Responsibility | What it does | What it does not establish |
|---|---|---|
| Upper layer: model | Proposes dialogue, intent and high-level action at decision points | A proposal is not a command or a completed action |
| Author-constraint boundary | Checks fit; may accept, adjust and recheck, request a new proposal or decline | Not a guarantee that every proposal can be repaired |
| Lower layer: UE | Rechecks live conditions, runs native tasks and confirms outcomes | An animation or spoken claim alone does not prove completion |
| Separate records | Retain proposals, check decisions and outcomes for review | Records do not control actions or establish effectiveness |

The next decision uses actual world state. Treating model output as executable instructions is a conceptual counterexample, not a mode or experimental condition used by this prototype. The conceptual diagrams describe responsibilities; some paths remain in development.

## What the new images show

| View | Development stage | What the image supports | Limit |
|---|---|---|---|
| [Menu-grip pose](media/menu-pose-20260917.png), 17 Sep 2026 | Editor pose candidate | A proposed hand and menu arrangement | Does not demonstrate runtime grasping |
| [Child seating adaptation](media/child-seat-study-20260917.png), 17 Sep 2026 | Pose-adaptation candidate | A candidate child pose in relation to a chair and table | Does not demonstrate a complete seating action |
| [Menu on the table](media/menu-table-test-20260915.png), 15 Sep 2026 | Controlled development run with a test setup | The visible menu position at one point in the test | Does not establish autonomous service or an uninterrupted task sequence |

The [image inventory](public-media.json) describes all nine current gallery images. Six earlier stills provide scene, posture and gesture context. Dates and dimensions are media metadata, not experimental measurements. Three earlier environmental views have left the current gallery; already-public files and Git snapshots remain available as historical material.

## Work still in progress

Partial paths exist for dialogue, captions and speech, movement, seating, object interaction and service tasks. The three new images document specific development work, not a completed integration of those paths. Connecting them into sustained interaction remains unfinished. Ordering through payment is incomplete; formal gameplay evaluation has not begun. Execution reliability, character understanding and player experience need separate investigation.

Actual JSON schemas, prompts, author rules, repair selection, evaluation materials and findings remain outside the public overview.

## 中文：如何阅读这项工作

AINPC 关注作者如何约束游戏角色的即兴行动，以及如何检查行动提议与实际结果之间的关系。餐厅把共享物件、身体行动和社会期待放在同一个可观察的场景中。

张睿潇负责研究框架、交互设计、UE 原型集成与开发验证。原型同时使用 Unreal Engine、MetaHuman、语音与语言模型服务，以及第三方角色、动画和环境资产。开发过程中的验证不等于效果已获得独立评估。

上层模型提出台词、意图和高层动作，作者约束检查提议是否合适，下层 UE 复核现场条件、执行任务并确认结果。方案允许接受、调整后重查、要求新提议或不执行；部分路径仍在开发。提议、检查和结果另行记录，供事后复核，不参与动作选择。把模型输出直接当作执行指令只是说明问题的概念反例，不是本原型采用的模式或实验组。

9 月 17 日新增展示的三张图片具有不同性质：

- 菜单握持图是编辑器姿势候选，不证明运行时抓取。
- 儿童坐姿图是适配候选，不证明完整落座动作。
- 9 月 15 日菜单位于桌面的图片来自带有测试安排的受控开发运行，只展示某一时刻的菜单位置，不证明自主服务或连续任务链。

当前图库共九张，另外六张早期静帧提供场景、坐姿和手势的背景。三张旧环境图不再用于当前图库，但原公开文件和历史快照保留。日期与尺寸只是媒体信息，不是实验测量。

对话、字幕与语音、移动、落座、物件交互和服务任务已有局部路径，把这些能力串成持续互动仍未完成。点餐至结账的完整流程尚未完成，正式游玩评估尚未开展。执行可靠性、角色理解与玩家体验仍需分别研究；具体协议、提示词、作者规则、修复选择、评估材料和结果不公开。
