# Serving several guests: shared objects and taking a seat

Method note, 25 September 2026 · wording corrected the same day · [中文](2026-09-25-serving-several-guests.zh-CN.md) · [All method notes](README.md) · [Disclosure](../../DISCLOSURE.md)

## Status

This is work in development. Its rules have not been signed off by the author, and nothing has been evaluated with players. The sessions behind this note are development diagnostic runs, not study runs. The note explains methods and design intent, not results.

## Why

With a single guest, a restaurant can hide many assumptions: a menu is always free, the server always has somewhere to stand, and a chair only ever moves for one person. With several guests at several tables these assumptions break, and the world state does not show why. One guest waits for a menu that another guest still holds, a server cannot reach the side of the table where an object was placed, or a guest walks through the chair they have just pulled out. This note describes the general rules that replace those single-guest assumptions. Like the [note on holding objects](2026-09-24-three-layer-embedding.md), it concerns the execution side described in the [overview](../../README.md).

## In brief

The rules cover judging whether a character is available, deriving where objects sit on a table and where the server stands to reach them, circulating shared objects among guests, and taking a seat. Each rule is written for every seat, guest and object rather than for one table, and most can be switched off in development to restore the earlier behavior for comparison.

## One judgment of availability

Whether a guest or a member of staff is busy is decided in one place, and every judgment of busy carries its reason, such as talking, speaking, having tasks queued, carrying out an action or holding a seat. Idle behavior that only passes time never counts as busy, for guests and staff alike, so a character who is merely idling does not hold up service.

## Table settings derived from the seat

Where the menu, plate, cutlery and bill go is derived from the seat: the chair's tucked-in position, the table edge and what the seated body can reach. The same rule serves every adult guest. A place only needs to be within reach of the table: a setting is refused when the table edge lies beyond a straight arm from the seat, and a place farther in is kept, with the lean it implies reported rather than hidden. When something does not fit, cannot be reached or leaves the server nowhere to stand, the rule refuses instead of guessing. Children are not given derived settings yet; an adult at the table chooses for them.

## Where the server stands

A standing place counts only if the server can actually stand there and walk to it. The choice of which side of a guest the menu goes on is therefore made where all of these constraints are known. If the first side leaves the server nowhere to stand, the same rule tries the other side and checks it against the neighboring settings, and if neither side works, both reasons are reported. A standing place written for an object is used only when it lies on walkable ground; otherwise, where a character stands to fetch the object follows where the object currently rests. Arriving at an object and touching it use the same reach check.

## Shared objects circulate

An object borrowed for a step goes back to where it came from when that step is complete: a menu returns to its rack once the order is taken, so the next guest can use it. The return is bounded in time; if it cannot finish, the order still proceeds and the abandoned return is recorded instead of stalling service. Whether a session has stalled is judged from the progress of the whole restaurant, not of one guest, because with several guests some waiting for a shared object is normal.

## Taking a seat

The rules for taking a seat follow how people handle a chair. A guest stands beside the chair, not behind it, to pull it out, and then walks into the space between chair and table from the side, never through the chair. Before pulling, the guest turns toward the table and places the hand nearer the chair on the top of the backrest, guided by inverse kinematics, then moves back together with the chair and lets go once it is out. Each chair rests tucked in at its own table, and pushing in mirrors pulling out, at a slow and steady pace. When movement is checked for collisions, a seated body may overlap its own table, including every part of it, but nothing else.

## Evaluation principles

These are the evaluation rules the work has adopted; the current checks do not yet meet all of them.

- Most new rules have a development switch that restores the previous behavior, so a run with the rule can be compared with a run without it.
- The timing and pace of motion phases come from the engine's own record of the motion, not from the clock of a sampling script, which slows down under load.
- When the search for a standing place fails, every reason for rejection is counted and reported, not only the last one.
- A check that a path is clear uses the same shape and height as the movement it checks.
- Results are checked against rendered frames taken from viewpoints that walls and fittings do not block.

## Rules that generalize

- Make a choice at the layer that knows every constraint on it, or pass those constraints down to where the choice is made.
- Keep a single implementation of each physical rule; with two copies, a fix reaches one and misses the other.
- Before giving a task a preferred worker, check that the preference expires; one that never expires acts as exclusive ownership.
- Standing beside an object uses the width of the body, not the wider envelope used for walking.
- State which part of a movement must avoid an object and which part belongs to the object's own contract, such as the space in front of a seat where a guest is meant to stand.

## Not claimed

- The hand reaches the backrest only at a point; the fingers do not yet close around it, and there is no stepping-back motion, so the feet slide while the chair moves.
- Some seats still use the earlier approach, because nearby scenery blocks the new standing place.
- Reaching farther than a straight arm implies a lean that is not animated.
- Seated characters can still pass slightly into chairs and the floor.
- When several guests are served at once, a complete autonomous service does not yet finish for every guest.
- The current build does not yet follow every rule in this note.
- The rules have run only in development diagnostic sessions.

## Not disclosed

This note gives no data, numbers, parameter values, field names, source code or images, and names no assets, clips, animation sources, characters or runs; development records stay private, as set out in [Disclosure](../../DISCLOSURE.md).
