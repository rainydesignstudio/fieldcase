# D documentation index

Resolve paths relative to this index. Find D through the docs entry in the root index and resolve `D:<id>` here. D is maintained with the workspace and does not have a separate layer version, repository, or source pin. D:index-spec provides index rules; the root rules govern identity and permissions.

## 1. Current documents and specifications

| # | ID | Name | Type | Entry | Size | How to use it |
|---|---|---|---|---|---|---|
| 1 | <a id="agent-guide"></a>agent-guide | Agent Guide | Guide | [Guide](AGENT-GUIDE.md) | 78546 B | Read fully or by chapter for procedures; it does not grant authority |
| 2 | <a id="index-spec"></a>index-spec | Index and reading specification | Specification | [Index specification](spec/index-spec.md) | 26345 B | After the root startup checks, reread as an active rule; D/K/R/M/T, source, protection, and resolution |
| 3 | <a id="handoff-spec"></a>handoff-spec | Handoff and lifecycle specification | Specification | [Handoff specification](spec/handoff-spec.md) | 40974 B | After the root startup checks, reread as an active rule; lifecycle, versions, items, history, and resuming |
| 4 | <a id="design-spec"></a>design-spec | Design documentation specification | Specification | [Design specification](spec/design-spec.md) | 9339 B | After the root startup checks, reread as an active rule; roles, placement, and maintenance, without a particular style |

The three core specs are required. Put active module specs in the same spec directory and register them here. Do not install or register unselected material as active. Protect the full directory and its member specs; disabling optional data layers or clearing extra config targets does not remove this protection.

## 2. Entries to add when needed

This table describes conditions, not existing originals, snapshots, history, or material. When an entry is actually created, append its real ID, type, path, size, and reading scope to §1 and continue the row numbering.

| Object | Creation and registration |
|---|---|
| cache-spec / contract-spec | On module adoption, install from the fixed original into local `spec`, verify its full supporting changes, and register the active D specification |
| upstream | Register actual retained adoption or comparison originals. Default: `upstream/fieldcase/`. Separate exact versions or candidate batches; verify language, saved scope, and pack-relative structure. Maintain current adoption as specified in §3 |
| migration | Register actual source copies, copy inventories, or validation material. Do not pre-create permanent logs or substitute old originals for active rules |
| distribution | If shared T has no distribution category and the workspace actually retains fixed pack materials, register their resource index here. Do not create a shared category |
| backups | Register the default `backups/<date>/<upgrade-batch>/` only for actual necessary snapshots. Put the batch index outside `snapshot`, with the actual structure and scope. Do not require the directory when Git covers recovery |
| handoff-history | Register when archiving actual stages or versions. Reach root L1 through `HANDOFF.history` and locate the index and volume by version |
| handoff-pending | Use a stable ID to locate actual unscheduled details. Do not create an empty file |
| pitfalls | Establish for actual issues and evidence. Match the number to its B-section entry and read only the needed items |

## 3. Maintenance and reading

D does not represent all applicable rules. Reread all rules and specifications actually in force. Take the guide as needed; refer to adopted originals, history, and recovery batches as directed. Do not apply startup protection to all of docs recursively.

This table owns the physical paths and byte sizes of guides and specs. Update the root docs entry if D moves. Do not duplicate root `rule-*` aliases or a config path map. Keep `*-spec.md` names, stable IDs, and section keys. Check active references, protection, and supporting changes when moving files.

D:upstream supplies originals for three-way comparison. After adoption, only the upstream row's reading instructions record the exact current original for the core and each adopted module. Distinguish modules by ID. Resolve paths relative to that row's entry directory; a fixed pack inventory may locate individual objects. Distinguish batches sharing a version by the pack batch in the pack README, verified under D:agent-guide §5.1. Supporting material origins do not identify the pack batch. Config records source versions; this index records the original's entry. Keep comparison originals alongside current ones. Change current entries only after adoption, upgrade, or removal has completed and been verified.

D:backups locates actual file snapshots only. The root rules §6 govern recovery evidence and inventories. If Git is sufficient and no snapshot is made, keep the recovery pointer and inventory in the existing plan or HANDOFF.

Clean up originals, unique evidence, and recovery sources only within authorization. Renaming a path, having Git, or downloading a new version does not authorize deleting old items. Authority and permissions come from the applicable rules, not the D prefix or filename.
