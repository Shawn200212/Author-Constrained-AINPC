# Three-layer embedding and holding objects

Method note, 24 September 2026 · [中文](2026-09-24-three-layer-embedding.zh-CN.md) · [All method notes](README.md) · [Disclosure](../../DISCLOSURE.md)

## Status

This is work in development. Its rules and object descriptions have not yet been signed off by the author, and nothing has been evaluated with players. The note explains methods and design intent, not results.

## Why

The characters need to hold and use everyday objects, such as a spoon or a dish, believably. The animation library has plenty of whole-body motion, but finger motion is often missing or generic, and no clip knows what the hand is holding. The embedding work describes what a motion means, what a hand is doing and what an object affords, so that holding and using can follow general rules instead of fixes for each clip.

## In brief

Here an embedding is a compact description that places similar things close together, such as similar motions or hand shapes. Layer one, still only planned, is meant to map a situation to how a character presents itself; layer two describes whole-body motion, and layer three describes hand states. Object descriptions measured from geometry sit beside the layers, and runtime rules combine them when a character holds or uses something. All of this concerns how the engine carries out and presents an action, the execution side described in the [overview](../../README.md).

## Layer one: situation to presentation (planned, not built)

This layer is meant to map a character's situation and persona to posture, tone and expression. Nothing is learned yet. A learned mapping would replace today's behavior only if it does better.

## Layer two: whole-body motion meaning

Poses from each library clip are described relative to the character's own body and scale, then summarized per clip; fingers are left to layer three. A linear projection, a self-supervised contrastive encoder and a supervised metric encoder were compared as ways to place similar motions close together. The current build uses the linear projection; the learned encoders are not deployed, and the comparison remains open.

## Layer three: hand states (feet planned)

Hands are described with skeleton-independent measures of finger and palm posture. Only moments in which the fingers actually move are clustered, without labels, and clusters are named by rules on their measurements, so the names are measurement labels, not validated grasp types. Finger rotations come only from clips of the character's own skeleton family. Foot states are not built yet.

## Objects described from geometry

Each object is measured from its own mesh, using its main axes and a cross-section profile along its length. These give the working end, such as a spoon's bowl, and a region to hold; for objects that carry food or drink, they are also meant to identify the side that must face up. Handle thickness and overall shape suggest a rough kind of grip. These are geometric estimates that guide behavior, not ground truth, and none has been signed off by the author.

## Exchange with the world-generation project AIWG

AIWG, the author's world-generation project also shown on the project website, is meant to supply the same kind of object description for what it generates; this project owns the contract and uses the records at runtime. The contract covers records for objects, hand states and motion meanings, and each record states where it came from. It specifies that invalid records are refused one by one, that author approval can never be imported and is given only through the author's own tools, and that hand data applies only to the skeleton family it was measured on. Only the kinds of records and the rules for accepting them are described here; the contract itself stays private. No record produced by AIWG exists yet.

## Runtime behavior while holding and using

Each rule is written as a general rule, not per object or character. While a hand holds an object, its fingers blend toward a hand state from the same skeleton family, giving way when a carry with both hands takes over. A utensil's grip comes from its description and the posed hand: it lies along the index finger with its working end past the fingertips, and a utensil carrying food is meant to stay near level at the moment of use. At that moment, inverse kinematics brings the working end toward its use target: the mouth when eating, and the same rule is meant to cover drinking. When a character walks to an object, how close it must get to count as arrived is limited by how far its arm can reach from where it stands.

## Evaluation principles

These are the evaluation rules the work has adopted. When testing a motion embedding, hold out whole animation sources in turn, and hold out copies or retargets of one motion together. Fit normalization on training data only, and fix the protocol and deployment rule before a run. Compare learned models with simple baselines and across random seeds. At runtime, count whole-window statistics rather than the best sample, do not treat a geometric distance as contact, and check results against rendered frames. The current checks are weak, so the layer two comparison remains open.

## Rules that generalize

- Check rotation conventions against the engine's own functions before exporting joint rotations.
- Never transfer joint rotations between skeleton families; features for grouping can be shared, rotations cannot.
- Confirm what a geometry query returns on an object of known size before deriving tips or grip points from it.
- Never let a descriptive property double as a behavior trigger; behavior should follow how the object is meant to be used.

## Not claimed

- No claim is made that a utensil touches or enters the mouth; how it meets the face is unresolved.
- The current build does not yet follow every rule in this note.
- The runtime rules have run only in narrow development sessions.
- The situation layer and foot states are not built.

## Not disclosed

This note gives no data, numbers, parameter values, field names, source code or images, and names no assets, clips, animation sources, characters or runs; development records and corrections stay private, as set out in [Disclosure](../../DISCLOSURE.md).
