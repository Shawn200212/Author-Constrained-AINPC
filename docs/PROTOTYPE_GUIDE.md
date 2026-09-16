# Reading the prototype / 原型导览

[English overview](../README.md) · [中文首页](../README.zh-CN.md)

## Why the two layers matter

An occupied seat and a broken commitment are different problems. UE can check whether the seat is available. Author constraints add the character's goals, commitments, order of actions and priorities. A proposal must fit those boundaries before execution, and UE must still check whether it can actually be carried out.

| Responsibility | What it does | What it does not establish |
|---|---|---|
| Upper layer: model | Proposes dialogue, intent and high-level action at decision points | A proposal is not a command or a completed action |
| Author-constraint boundary | Checks fit; may accept, adjust and recheck, request a new proposal or decline | This is not a third brain or a guarantee that every proposal is repairable |
| Lower layer: UE | Rechecks live state, runs native tasks and confirms the outcome | An animation or spoken claim alone does not prove completion |
| Separate records | Retain proposals, check decisions and outcomes for review | Records do not control actions or prove effectiveness by themselves |

The next decision uses actual world state. Record-keeping is a separate, one-way review path. This distinction matters: the model's statement that something happened cannot become evidence that it did.

Treating model output as executable instructions is a conceptual counterexample, not an experimental condition or an alternative mode in this prototype. It does not imply that UE's basic runtime checks can be bypassed. The proposed benefit of author constraints still needs evaluation.

## What the images show

| View | Visible content | Boundary |
|---|---|---|
| [Waitress at the table](media/ainpc-table-service-20260915.png) | Service character beside a seated character, 15 Sep 2026 | Not a completed service sequence |
| [A view from the seat](media/ainpc-seated-scene-20260915.png) | Seated posture and surrounding space, 15 Sep 2026 | Not a seating-reliability test |
| [Partner table](media/ainpc-partner-table.png) | Partner's seated pose, 31 Aug 2026 | Not proof that every character can sit successfully |
| [Table gestures](media/ainpc-table-gestures.png) | Body poses during an exchange, 8 Sep 2026 | Not a continuous dialogue or speech-synchronization record |

The [image inventory](public-media.json) lists all nine current stills. Dates, dimensions and captions are media metadata, not experimental measurements. The two September 15 images replace an older table view and an editor close-up in the current presentation; earlier public Git snapshots remain historical.

## Current limits

Partial paths exist for dialogue, captions and speech, movement, seating, object interaction and service tasks. Connecting them into sustained service remains development work. Ordering through payment is incomplete; formal gameplay evaluation has not begun. Actual JSON schemas, author rules, repair selection, evaluation materials and findings remain outside this public overview.

## 中文：两层各自负责什么

座位被占用与角色违背承诺，是不同的问题。UE 可以检查座位是否空闲；作者约束则加入角色目标、承诺、行动顺序和优先关系。提议先要符合这些边界，执行时仍须接受 UE 对现场条件的复核。

上层模型在决策时提出台词、意图和高层动作，不直接控制身体。两层之间的检查可以接受提议、保留原意调整后重查、要求重新规划，或明确不执行。下层 UE 处理原生任务，由世界状态确认结果；未完成时回退或结束。部分路径仍在开发，不保证所有提议都能修复。

下一轮依据实际世界状态决策。提议、检查决定与执行结果另行记录，供事后复核，不参与动作选择。模型说“已经完成”，不能替代世界中的完成证据。

“模型直接驱动引擎”只是架构反例，不是当前原型的实验组或可切换模式，也不表示能绕过 UE 的基础运行时检查。作者约束的预期价值仍需验证。

本次用两张 9 月 15 日的运行静帧替换旧同桌视角和编辑器近景。九张现用图片的日期、尺寸与说明见[清单](public-media.json)；旧公开 Git 快照保留为历史记录。新图展示桌边关系与落座空间，不证明完整服务流程、语音同步或稳定成功。点餐至结账仍未完成，正式游玩评估尚未开展；具体协议、作者规则、修复选择与评估材料不公开。
