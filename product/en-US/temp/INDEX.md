# Temporary layer index

Paths are relative to this index. Reach it from the T entry in the root index. The root maintainer owns this index; each artifact is maintained by its assigned workspace or task. Use D:index-spec for references and root rules §1–§2 for identity and authorization.

## 1. Storage, permission, and reading

- Category directories are shared entry points. Store artifacts under the workspace, task, library, or batch path listed below. The category parent is not freely writable.
- Use the confirmed owner name for `<workspace>` and a recognizable name for `<task>` or `<batch>`. Use an existing authorized location with the same purpose. Report unclear ownership instead of moving or removing anything without authorization.
- Index entries only provide navigation. They do not authorize reading all temporary material or changing files owned by others. Follow user permission, task scope, and the row's reading instructions. A directory sized “—” is not for full reading or recursive size measurement.
- Create only categories and artifacts needed for the approved charter, selected capabilities, and actual task. The table permits uses; it does not require empty categories, task directories, or indexes. A directory does not prove completion.
- Registering temporary material does not make it authoritative. Distinguish review material, fixed candidates, and formal knowledge. Only resources admitted through the proper process can be used as rules in force.
- With Git, exclude T artifacts and track the locally owned T index as a governance file in the root repository. A worktree under T belongs to its original repository. T does not have a repository of its own.
- When reusing a parent T, this is a template original. Follow that layer's active entries and authorized ownership. Do not create another active T or edit the parent index on its behalf.
- The docs index locates retained adoption originals, migration source copies, and upgrade recovery snapshots for comparison or recovery. Do not treat them as disposable cache or copy them into T recursively.

## 2. Category entries

| # | ID | Name | Type | Entry | Size | How to use it |
|---|---|---|---|---|---|---|
| 1 | <a id="cache"></a>cache | Rebuildable cache and material awaiting placement | Directory | [Cache](cache/) | — | Raw inputs, tools, inventories, and material awaiting placement. Read only what the task needs. See §2.1 for staging and placement |
| 2 | <a id="audit"></a>audit | Review and validation | Directory | [Review](audit/) | — | `<workspace>/<task-or-candidate>/`. Reports, evidence, and fixed review copies. Read named objects; self-check is not user acceptance |
| 3 | <a id="publish"></a>publish | Delivery candidates | Directory | [Delivery](publish/) | — | `<workspace>/<version-or-batch>/`. Approved packs and their usage entry. A candidate is not a public publication |
| 4 | <a id="backup"></a>backup | Version and operation backups | Directory | [Backups](backup/) | — | `<workspace>/<version-or-batch>/`. Save and verify within scope. Matching snapshots for official upgrades are under the docs backups entry |
| 5 | <a id="generated"></a>generated | Generated and intermediate materials | Directory | [Generated materials](generated_contents/) | — | `<workspace>/<task>/`. Use this location for workspace production materials, intermediate artifacts, and their records. Keep audit evidence under T:audit and recovery material at its designated recovery entry |
| 6 | <a id="distribution"></a>distribution | Fixed distribution resources | Directory | [Distribution](distribution/) | — | Read `fieldcase/INDEX.md` if present. Find fixed local language, layer, and module materials. Do not mark unused materials as installed |
| 7 | <a id="archived"></a>archived | Global archive | Directory | [Global archive](_archived/) | — | Retain approved T archives. Record ownership, source, and archive location for targeted lookup. Use the existing contract archive for contracts |

A missing directory shows only that the corresponding artifacts are absent. Do not claim a review copy, backup, or distribution material exists. If a needed entry has not been created, a session with permission can create and check it in the approved location. If official material is missing, follow the guide instead of constructing a false source.

### 2.1 Staging and placement

- For a workspace that owns its T, resolve a known final destination relative to the destination workspace root. When it is under a top-level directory, preserve that directory's actual name and the rest of the relative path under the actual T:cache entry. For example, stage `materials/media/logo.png` in `cache/materials/media/logo.png`. Use the actual names of custom layer directories and create the paths needed for the task.
- Stage root-level files under the authorized workspace owner path. For example, stage `HANDOFF.md` in `cache/<workspace>/HANDOFF.md`. When reusing a parent T, use its registered cache entry and authorized owner path, and show how staged paths map to their destinations in the plan. Store raw inputs and acquisition tools using the actual T entry and the adopted method.
- Confirm the destination, scope, and write authorization. Place the approved material, update the affected indexes and references under the destination layer's protocol, and check the files and entries. Keep material in staging within the current authorization while the destination is undecided.

## 3. Reference and maintenance

- Resolve a reference such as `T:audit#<workspace>/<task>/` by entering this index through the root T entry, then following the matching category and relative subpath. IDs stay stable across renames. Move actual files, update the index and tool parameters, and check references together.
- Before reorganizing existing categories or moving registered artifacts, draft the current path, actual purpose and retention requirements, proposed category and destination, and affected indexes, references, and Git-tracked paths. After the plan is approved and execution is authorized, move the files and update the entries together within that scope, then verify that they match.
- Add a child index only when local navigation requires one, and link to it from its parent index. Reuse an existing batch inventory or report when it already locates the material.
- Register a distribution cache index only after acquiring complete resources. Record module purpose, exact source, compatibility baseline, dependencies, supporting changes, and entry. Downloading is not adoption; `config.modules` records only completed integration.
- Record exact source and purpose for worktrees, copies, or temporary instances created on demand. Do not pre-create directories for every historical version. Stable consumption uses a development worktree with common history in the same repository.
- Cache cleanup does not authorize removing adopted official originals, current config, another session's files, material awaiting placement, fixed review copies, unique evidence, or recovery material. Follow the actual authorization and retention conditions.
- Draft changes to shared categories, owners, or reading rules first. Adding or removing a normal task batch under an existing category is not adding a layer or granting permission to write in the parent.

Authority: this index owns T categories, ownership, and storage. The root T entry identifies its actual location. Review it when categories, ownership, reading, tracking, or cleanup rules change.
