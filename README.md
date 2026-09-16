# AINPC: Author-Constrained Improvisation

[中文](README.zh-CN.md) · [Project page](https://ruixiaozhang.com/index_EN#work-ainpc)

The model proposes an action, author constraints check whether it fits, and Unreal Engine executes and confirms the result. AINPC explores how characters can improvise while the author retains control over what they can do.

Public overview updated **16 September 2026**. This is a research prototype, not a runnable software release or a complete research artifact.

## Speaking is not acting

In the restaurant prototype, saying “I'm seated” does not make it so: the world must confirm that the character has sat down. Treating a model's response as an engine command could target an occupied seat, request an unsupported action or report success from outdated information. That direct connection is an architectural counterexample, not a mode used by this prototype.

UE's checks still matter, but an executable action can be wrong for the situation. A character might use an available object while overlooking a commitment or the intended order of actions. Author constraints address that difference between **can execute** and **fits the author's intent**.

## Two layers, with a boundary between them

The upper layer proposes. At decision points, the model reads the situation and available interactions, then returns dialogue, intent, a high-level action and a target reference as a structured proposal. It does not move the body frame by frame or choose animations.

An author-constraint check sits between the layers. Locally defined goals, objects, action order and priorities are not the model's to rewrite. The design allows acceptance, an intent-preserving adjustment followed by another check, a request for a new proposal, or an explicit refusal to act. This check is a responsibility boundary, not a third “brain”. Some paths remain in development; successful repair is not guaranteed.

The lower layer runs in UE. It rechecks live state and resources, carries out native movement and interaction tasks, and confirms completion from the world. An incomplete task rolls back or ends explicitly. The next decision reads the actual outcome, not a claim of success. Proposals, checks and outcomes are also recorded separately for review; those records do not select actions.

![Two-layer architecture: context feeds model proposals; author constraints gate execution; UE confirms world outcomes. Separate paths handle replanning, refusal, world feedback and read-only records.](docs/media/public-interaction-overview.svg)

[Open the full-size diagram](docs/media/public-interaction-overview.svg). It shows responsibilities and information categories, not actual JSON fields, prompts, author rules or repair algorithms.

## Where the prototype stands

Dialogue, captions and speech, movement, seating, object interaction and service tasks have partial runtime paths. Work is connecting these into a longer sequence. The ordering-to-payment flow is incomplete, and formal gameplay evaluation has not begun.

The research will examine whether system judgments reflect the author's requirements in a given situation. Execution reliability, character understanding and player experience need separate validation. Evaluation rules, data and findings remain private.

## Inside the restaurant

These nine development stills from August and September 2026 show characters, seating and gestures. Some retain debug rings, and the visuals are unfinished. A still does not verify continuous dialogue, synchronized speech or a completed service task.

### Waitress at the table

![Waitress standing beside a seated character](docs/media/ainpc-table-service-20260915.png)

15 Sep 2026 · Runtime still: Waitress and a seated character share the table setting.

### A view from the seat

![A seated foreground character in the restaurant](docs/media/ainpc-seated-scene-20260915.png)

15 Sep 2026 · Runtime still: seated posture, orientation and surrounding space.

### A shared restaurant

![Characters and tables in the shared restaurant](docs/media/ainpc-dining-room.jpg)

Characters, tables and walkways form the setting for action.

### A seated conversation

![A character seated in the conversation setting](docs/media/ainpc-conversation.jpg)

Seating and orientation give the conversation a place in the scene.

### Furniture as interaction

![Seats and tables in the restaurant booth](docs/media/ainpc-booth.jpg)

Tables and chairs are objects to find and use, not just scenery.

### Seated together

![Partner character seated at the table](docs/media/ainpc-partner-table.png)

31 Aug 2026 · Runtime still: the Partner character's seated pose and table position.

### Table gestures

![Character poses during a table exchange](docs/media/ainpc-table-gestures.png)

8 Sep 2026 · Runtime still: character poses during a table exchange.

### Further views

![Another view of the restaurant prototype](docs/media/ainpc-arrival.jpg)

![A further view of the shared scene](docs/media/ainpc-stairs.jpg)

[Prototype guide](docs/PROTOTYPE_GUIDE.md) · [Image inventory](docs/public-media.json) · [Version scope](docs/VERSION_SCOPE.md) · [Disclosure](DISCLOSURE.md) · [Rights and credits](RIGHTS_AND_CREDITS.md)
