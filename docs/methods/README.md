# Method notes / 方法说明

[English overview](../../README.md) · [中文概览](../../README.zh-CN.md) · [Disclosure / 公开范围](../../DISCLOSURE.md)

Status: in development · rules and object descriptions not yet signed off by the author · not evaluated with players.

These dated, text-only notes explain what parts of the prototype do, what information they use and why they are designed that way. They are not development logs or results, and they contain no data, measurements, parameter values, field names, source code or asset names; see [Disclosure](../../DISCLOSURE.md) for the boundary.

状态：开发中 · 规则与物体描述尚未经作者最终确认 · 未经玩家评估。

这些按日期发布的纯文字说明解释原型各部分做什么、用什么信息、为什么这样设计。它们不是开发日志，也不是研究结果，不含数据、测量值、参数值、字段名、源码或资产名；边界见[公开范围](../../DISCLOSURE.md)。

## Notes by date / 按日期

Newest first. Each note is one dated method revision; later notes do not rewrite earlier ones.

按日期排列，新的在上。每篇是一次带日期的方法修订，后来的说明不改写先前的说明。

### 25 September 2026 · Serving several guests: shared objects and taking a seat

[English](2026-09-25-serving-several-guests.md) · [中文：服务多位客人：共享物件与入座](2026-09-25-serving-several-guests.zh-CN.md)

How availability is judged in one place, how table settings and the server's standing place are derived from the seat, how shared objects circulate among guests, and how a guest pulls out a chair and sits down.

有空与否只在一处判断；桌面布置与服务员站位由座位推出；共享物件在客人之间流转；客人如何拉开椅子并坐下。

### 24 September 2026 · Three-layer embedding and holding objects

[English](2026-09-24-three-layer-embedding.md) · [中文：三层 embedding 与持物](2026-09-24-three-layer-embedding.zh-CN.md)

What each embedding layer describes, how objects are described from their own geometry, and the general rules for holding and using everyday objects.

各层 embedding 描述什么、物体如何由自身几何描述，以及拿起和使用日常物件的通用规则。

## Revisions / 修订

| Date / 日期 | Note / 说明 | Public commit / 公开提交 | Private record / 私有记录 |
|---|---|---|---|
| 2026-09-25 | [Serving several guests: shared objects and taking a seat](2026-09-25-serving-several-guests.md) / [服务多位客人：共享物件与入座](2026-09-25-serving-several-guests.zh-CN.md) | `1c65386` → (filled in after commit / 提交后回填) | (filled in after commit / 提交后回填) |
| 2026-09-24 | [Three-layer embedding and holding objects](2026-09-24-three-layer-embedding.md) / [三层 embedding 与持物](2026-09-24-three-layer-embedding.zh-CN.md) | `e5e68de` → **`91c4c5e`** | `6da28a8` (private development record, not public / 私有开发记录，不公开) |

The private record column cites a private development record by commit id only; that record is not public.

“私有记录”一栏只以提交编号引用私有开发记录；该记录不公开。
