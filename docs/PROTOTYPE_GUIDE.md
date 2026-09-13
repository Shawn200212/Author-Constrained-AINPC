# A guide to the restaurant prototype / 餐厅原型导览

[Overview / 项目首页](../README.md) · [中文首页](../README.zh-CN.md)

## Read the scene before the architecture

The restaurant makes the relationship between conversation and action visible. A seat can be occupied, two characters can address each other across a table, and a service character can share the same space. These situations motivate the research; an image of them does not demonstrate that every associated task is autonomous or complete.

| View | What to look for | What the image does not establish |
|---|---|---|
| [Dining room](media/ainpc-dining-room.jpg) | Characters, furniture and shared space in one setting | Reliable coordination across all characters |
| [Partner table](media/ainpc-partner-table.png) | Seated posture and a character's relation to the table | Successful seating for every character |
| [Across the table](media/ainpc-partner-exchange.png) | Orientation and the spatial setting for an exchange | Correct turn-taking or meaningful dialogue |
| [Table gestures](media/ainpc-table-gestures.png) | Visible bodily expression during a runtime moment | Speech synchronization or task completion |
| [Service character](media/ainpc-service-character.png) | The service character in the restaurant, in an editor view | A running service sequence |

## How the research question developed

The starting point was a character that could respond in natural language. Connecting those responses to a shared world introduced a different problem: a plausible sentence can still describe an action that the world cannot, or should not, perform.

I therefore separated the model's proposal from the engine's execution. The model supplies dialogue and high-level intentions. In implemented paths, the runtime checks the proposal against the scene and author-defined constraints, handles execution, and records the outcome. This division lets me ask what was proposed and what actually happened without treating them as the same event.

That distinction also changes the evaluation question. An action can satisfy an explicit rule while still conflicting with the author's understanding of the situation. The research examines that gap separately from execution success. The detailed evaluation instrument and its results are outside this public overview.

The next engineering step is to connect the existing local interactions into a sustained, embodied service sequence. That remains development work, not a demonstrated outcome of the images here.

## What is available to inspect

| Area | Publicly described status | Evidence boundary |
|---|---|---|
| Proposal and execution separation | Implemented in prototype paths and being extended | The diagram explains responsibilities; it is not source code or an exhaustive specification |
| Dialogue, captions, movement and seating | Present in development paths | Still images cannot establish timing, reliability or end-to-end success |
| Restaurant and character presentation | Shown in the curated media | Runtime stills and the static editor view are labelled separately |
| Ordering through payment | Full service sequence under development | No claim of complete autonomous service |
| Evaluation during play | Future work | No claim of established player benefit |

The [machine-readable image inventory](public-media.json) contains filenames, dimensions, captions and available date information. It is media metadata, not an experimental dataset or a set of performance measurements. The images and their rights are covered by the [rights notice](../RIGHTS_AND_CREDITS.md).

## 中文导览：先看情境，再看职责

餐厅让“说了什么”与“做了什么”的关系变得可见：座位可能被占用，同桌角色需要面向彼此，服务角色也要在共享空间中行动。这些情境说明研究问题从哪里来；画面本身不能证明相关任务已经全部自主完成。

研究最初从自然语言回应出发。把回应接入场景后，我遇到的关键问题变成了：一句听起来合理的话，是否对应一个世界能够执行、作者也愿意接受的动作？因此，我把模型提议和引擎执行分开。在已实现的路径中，模型提出台词与高层意图，运行时结合场景和作者约束检查提议、处理执行并记录结果。这样，提出动作与真正完成动作就可以分别检查。

随后，研究进一步区分了两种判断：动作是否满足明确规则，以及它是否符合作者对具体情境的理解。公开材料介绍这个问题与职责分工，不公开评估规则、研究数据或结果。

下一步是把已有局部交互连接成能够持续运行的具身服务流程。从点餐到结账的完整链条仍在开发，不能用几张静帧替代完成证据。图片清单中的日期、尺寸和说明只是媒体资料，不是实验数据。Partner 桌、同桌交流、手势和服务角色均已在首页单独展示，其中服务角色图片明确标为编辑器静态视图。
