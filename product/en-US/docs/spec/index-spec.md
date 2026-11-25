---
id: index-spec
updated: "2026-11-23"
recheck: Changes to index fields, directory hierarchy, governance adoption, shared use, migration paths, stable IDs, section keys, source resolution, protection, or reading
---

# Index and reading specification

## 1. Responsibilities and entries <a name="entry"></a>

- Root INDEX locates root files, D and enabled data layers. D and layer indexes own their entries; leaf content stays in its branch. D identity follows #bindings.
- INDEX owns location, object identity, reading instructions, and necessary byte counts. Config owns choices and official sources. HANDOFF records the actual situation, lifecycle, tasks, and consumption. Indexing grants no permission to write, go online, communicate, or execute.
- Follow the root and owning indexes. Use root startup rules to check governance, config, charter and actual workspace before reading protected specs.
- “Root” means the actual workspace root confirmed by the user, recorded as `HANDOFF.root` once the charter is active. A root path does not grant root identity. At the material stage, use what the user actually opened, rather than guessing a root from an unset field.
- Use the index directory as the base for entry links. See #refs for stable references across files. Resolve any required physical tool paths through the owning index.

## 2. Index models <a name="model"></a>

### 2.1 Root INDEX: six columns <a name="root"></a>

| Field | Meaning |
|---|---|
| # | Consecutive display and reading order, not persistent identity |
| ID | Stable identity, unique in its index |
| Name | Short human-readable name in the instance language |
| Type | Actual object type, such as file, directory, or index |
| Entry | Actual target path, as a clickable link with a short label |
| How to use it | Starting point, reading scope, and how to navigate further |

Keep actual purposes such as governance, handoff, config, projects, docs, and T in the root index. Docs is the sole D entry; do not add a separate D row or `rule-*` alias table. Register K, R, and M only when selected. The minimal layout is root plus D and T. Projects is for business work, and D is local documentation; neither creates a data layer repository.

Root `fieldcase_version` mirrors the authoritative config field. Check it when adopting a charter or finishing a core upgrade. Ordinary customization does not change source version. Investigate discrepancies rather than choosing the larger number. Do not duplicate `locale`, `governance_adoption`, or a path map in the root INDEX. Use config for adoption direction; the shape of entries does not decide it.

### 2.2 Local INDEX: seven columns <a name="local"></a>

D, K/R/M/T, and necessary subordinate indexes use the root's six columns plus Size between Entry and How to use it.

This example shows fields, not an active object:

```markdown
| # | ID | Name | Type | Entry | Size | How to use it |
|---|---|---|---|---|---|---|
| 1 | example | Example object | File | [Example](example.md) | Actual B | Read in full, or specify the search entry and limits |
```

- Use actual UTF-8 file bytes. Character counts, lines, or estimated KB do not replace an actual protected file's byte count.
- Use “—” when size does not apply, such as a directory. Do not recursively size dynamic directories. Protected directories still need complete per-file records.
- Put full-reading permission, shard sizes, query commands, and result limits in How to use it rather than adding a separate column. Permission to read one whole file or shard does not extend to its directory.
- Start each table at 1 and continue numbering across tables of the same index. Renumber after reordering, while using stable IDs for persistent references.
- Resolve local paths after a file entry relative to its containing directory and after a directory entry relative to that directory. A different basis explicitly given in reading instructions takes precedence.
- For local K, R, M, and T, recommend starting with top-level categories by purpose or ownership. Put content in the corresponding branch and subdivide it as needed. In M, `media/images/covers/` illustrates a media category, an image subcategory, and a cover collection. A small, easy-to-search collection can stay shallow. Choose names and depth to suit the work.
- The top-level INDEX for each of these layers lists actual top-level categories and approved governance and entry files at the layer root. Within ordinary branches, use directory paths or local indexes to navigate one level at a time. Find individual items through their owning branch. Dedicated indexes follow their approved protocols.

When reusing a parent shared layer, retain its approved index protocol rather than converting, for example, eight columns to seven. The adoption plan maps IDs, entries, per-file bytes, reading scope, and ownership by column and verifies every active reference. New local indexes use this specification. Originals and local navigation are not the shared layer's active registration.

### 2.3 Layer content identity <a name="identity"></a>

A newly created local K, R, or M records these fields in its own INDEX. Record content versions and fixed references from the actual scope of management and source. A reused shared layer keeps its actual existing identity. Do not invent a baseline, branch, or version; record the source and protocol differences in local HANDOFF. D and T have no separate navigation version.

| Field | Meaning and values |
|---|---|
| layer_version | Exact content version for this INDEX and its contents |
| content_state | `development` for current work; `baseline` for an explicitly approved and reliably fixed consumption baseline; `released` for content actually released. These are separate from workspace lifecycle |
| development_branch | Actual development branch, or `null` when none applies |
| stable_ref | Fixed tag or reference of the confirmed stable baseline, or `null` if none can be verified |

Pack versions and identities are defaults for materials only. Maintain adopted layers against the approved charter and actual contents. A new layer without a reliable fixed baseline is `development` with `stable_ref=null`. Writing a charter, Ready to start, or a first commit does not set a baseline. A fixed consumption baseline needs complete contents, approval, and a reliable reference. It is not a normal version release. Read older originals and history under their actual fixed identities.

Development INDEX entries, membership, and byte counts describe the development source. Use the old version's own INDEX for old released content. Do not record consumers or the index's own commit ID in the layer index. A candidate trial does not change the layer's original `development` identity.

## 3. Stable IDs and path resolution <a name="refs"></a>

### 3.1 ID rules <a name="keys"></a>

- Keep short, identifiable IDs unique within their indexes. An object's ID survives renaming, moving, or reordering. Do not recycle withdrawn IDs.
- D, K, R, M, and T prefixes locate documents; they are not drive letters or executable commands. Resolve paths before passing them to tools.
- For `D:<id>`, use the local root docs entry and the D index. For K, R, M, or T, enter the corresponding actual registered layer. Do not add D to data layer configuration or interchange scopes. D works without K.
- Resolve the same prefix in different workspaces through each bound root and source. Bind the owning workspace before interpreting cross-workspace documents or replies. Do not resolve a parent D/K reference as local to the reader. References do not change identity, ownership, or authorization.
- D:agent-guide locates the guide, D:upstream the retained originals, and D:backups actual file recovery snapshots. Originals, history, and recovery material are not active rules because they are in D; do not reread them in full.
- A reference may append `#<local-key>`. A numeric suffix on a file denotes lines or a line range; use the reading instructions for other local keys. For example, D:index-spec#1-6 refers to the first six lines, and T:audit#my-project/ locates that authorized project in audit. Treat numeric lines separately from section keys; a previous section number is not a line number.
- Use `D:<spec-id>#<key>` for active local specs. Data and provider specs retain their own prefixes. Use `#<key>` within a specification. End a real heading with `<a name="<id>"></a>`, locate the actual file first, then the matching anchor. Do not give keys to example headings, pre-create design specs, or guess a key from a similar section number.
- Begin IDs with a lowercase letter and use short words or clear abbreviations. Digits and hyphens are allowed. Use unique keys within a file rather than full title text. Keep them stable across numbering, title, or order changes. If an ID changes, update all effective references together without reusing its former meaning.
- Table rows do not automatically create Markdown anchors. For direct links, maintain actual anchors or existing heading anchors. A missing `#id` is not a working link.

### 3.2 Path boundaries <a name="paths"></a>

- The entry link is the sole record of the actual entry path. Navigate from the parent through a registered directory or subordinate index. The owning index records each file's path and size once.
- New local files, repositories, and migrated current content stay in the target root by default. An approved complete adoption plan can reference an existing external shared layer from the root INDEX. Do not use `../`, absolute paths, or symlinks to bypass authorization.
- For shared adoption, verify the actual source layer, maintainer, INDEX, protocol, fixed source, and read and write boundaries. Check every cited section key; handle missing keys under #read, and protected membership and bytes under #guard. Derive physical configuration from confirmed entries.
- Direction 1 takes local management from active D specs and root rules. Shared specification keys keep their actual scope. Mapping index fields only resolves external references. The adopting workspace handles conflicts with applicable parent rules under root §1.6.
- External shared layers stay in place under their maintainers. Do not copy their roots, create repositories for them, or edit their indexes. Put temporary or contribution artifacts only in the authorized local scope of that shared layer, without creating a second active T.
- For an existing workspace, normally copy listed content, align governance under the chosen direction, and initialize the repository at the target as applicable. Preserve source root, repository, and previous rules for tracing. Verify target results independently against the approved list; do not reuse source state, a former `initialized` field, or an ancestor repository.
- Move an original instance only when explicitly required and specially authorized. Verify root, actual repository root, and affected physical config. Do not repeat completed files, copies, or repository creation. A session change alone does not rerun first adoption or rebuild the target.
- Copying, modifying an index, or connecting shared content does not switch the source repository layout. Names and depth can vary within scope; check objects, entries, permission, and derived configuration together.
- Prefer stable references in rules. Use necessary physical paths for fixed startup files, the rule's authority location, approved migration lists, and tools that cannot resolve IDs.

### 3.3 D navigation and active specifications <a name="bindings"></a>

Root docs resolves D. Its location can vary. D INDEX owns unique local entries, types, bytes and reading scope. D follows local approval and the root repository; no layer_version, content_state, development_branch, stable_ref or pin.

| D ID | Role and applicability |
|---|---|
| index-spec | Local indexes, sources, and protection; required for direction 1 and during adoption |
| handoff-spec | Handoff, lifecycle, versions, and resuming; required for direction 1 and during adoption |
| design-spec | DESIGN organization and maintenance; required for direction 1 and during adoption |
| cache-spec | Method for the adopted knowledge acquisition module; do not install if unselected |
| contract-spec | Method for the adopted cross-workspace module; do not install if unselected |

Put specifications in the workspace's dedicated D spec directory, normally `docs/spec/`, regardless of local or external K. Do not maintain parallel local rule sets in K/spec and D/spec. The root registers only docs, without a `rule-*` alias table or additional path or binding fields in config.

When resolving D:handoff-spec#state, keep the section key, use the docs entry to find the row, actual file, and bytes, then find `state`. For a directory entry, keep resolving local coordinates as registered rather than reinterpreting them from root or guessing an old path. Keep anchors clickable.

Read active D rules from the workspace's approved current set. A data source pin does not change local governance. Applicable parent rules retain their authoritative sources. K can hold technical or provider rules; their placement does not remove authority. Originals and recovery snapshots are not active rules.

For direction 2, use the approved local implementation and single adoption record. A missing D or renamed directory does not establish autonomy. When upgrading an older instance, migrate the active specifications, references, directory protection, and index together. Keep originals, fixed sources, and history in their original structure. Do not keep two independent alias sets.

## 4. Fix a source for the work <a name="source"></a>

- Get the default from `config.consumption.default_strategy` and record actual sources and resume facts in the consuming HANDOFF. Changing a default does not rewrite current work.
- `shared-development`: at a new task or explicit update, fix one approved committed development revision. Use that commit's INDEX, membership, and text throughout the task.
- `stable`: use the recorded formal fixed baseline. Comparison does not switch the dependency. For an actual trial, state the layer, candidate revision, applied scope, and old formal dependency in the same record.
- On interruption, session change, or context change, restore the same source. Update only by explicit selection, not by following dev or main on resume.
- Resolve each source from its actual owning repository. When the root INDEX, relevant layer indexes, and bodies are tracked in the same repository, read them and resolve paths from the same fixed commit. Verify different sources separately. A branch helps locate a commit; a movable branch name is not a fixed snapshot.
- Read files directly at a known commit without switching the maintainer's working directory. Expand into T only when needed for manual review; do not pre-create historical copies.
- No local repository does not imply a source lacks Git. Use verified fixed commits or copies at external sources. If a source lacks reliable historical identity, record its local state and reading scope without claiming commit snapshots, historical pins, or isolation. Recheck affected material after changes.
- Only the INDEX from the selected commit describes its tree. Do not use an older index to check the current tree or assume a fixed commit is unreadable because a maintainer has uncommitted work.

## 5. Protected object checks <a name="guard"></a>

### 5.1 Resolve the scope <a name="targets"></a>

List only adopted K, R, and M layers in `config.index_guard.layers`. Do not put D there. Always check active D specifications and the dedicated directory under #core-guard. Both `layers` and `targets` may be empty with no data layers or additional targets; D protection remains.

Retain approved custom protection. A `file` or `directory` in `targets` may name a registered active D working file, dedicated directory, or data object. A `pattern` expands within selected data layers by default. These entries do not turn D core protection on or off. An additional D target needs a real entry, type, bytes, or complete membership. Do not automatically treat all docs, originals, history, and recovery batches as active rules. Without data layers but with extra D targets, leave `layers` empty and list actual `targets`.

Generate `file`, `pattern`, and `directory` targets from the actual adopted governance, specs, and specification directories, retaining approved custom entries. The target list may be empty only if no applicable data protection objects exist, with the reason in the plan. Do not accept omission, unclear layer identity, or invalid references as empty protection. Do not assume an unregistered provider entry such as K:specs.

| Target type | Actual scope |
|---|---|
| pattern | Tracked files matching the name pattern at a selected layer's fixed source |
| file | The precise file resolved from a stable reference |
| directory | An actual directory ID, or the containing directory and complete subtree of a registered file followed by #./ |

Only a `directory` target interprets `#./` as the named file's directory, such as K:index-spec#./. Find the actual index-spec file from the same source before taking its parent. It is not a section key, line number, or layer INDEX directory, and it does not support arbitrary `#../` traversal. Resolve ordinary chapters as `#<key>`.

A derived directory must stay within the approved D or layer boundary. Obtain its complete same-source tree or another reliable directory record. Every protected member needs an actual owning index entry and its bytes. A few files cannot demonstrate directory coverage. Do not infer scope from chapter numbers, common folder names, or aggregate size.

When approving a charter or changing protection, list adopted specs and directories and generate the existing target types. Keep custom approved targets. If a provider has no directory ID but has a real spec file and full tree, use `#./` without adding an ID to its index. Protect a standalone root governance or design file as a `file`; do not treat its entire data root as a spec directory.

Deduplicate matches for the same object and source. Newly appearing provider content does not expand permission or change config. Handle membership, source, or byte gaps under #errors.

### 5.2 Required checks <a name="checks"></a>

Apply the following fixed-source checks to data objects. Check additional active D objects against local approved sources, actual D entries, and actual files using #core-guard as appropriate. No D content pin is needed. Record their sources separately and do not deduplicate across sources.

1. The fixed source exists, and its identity and content version agree with the consumption record.
2. The layer entry, type, target reference, and actual directory resolve.
3. The owning index locates all members of a protected directory. Additions, removals, renames, and moves agree with registration. Reuse existing indexes rather than adding one per directory.
4. Each protected file's actual bytes match that source's registration.
5. While checking, read the file list, types, and necessary byte information only. After a pass, read all governance and specifications when a root reread is triggered; read other bodies within task and registered scope. Do not read entire libraries for protection checks.

For fixed Git sources, take the tracked membership from that commit's tree. Uncommitted or untracked files do not enter the snapshot. Without Git, verify the current confirmed file scope. Explain exclusions for system or repository items, without silently ignoring new content as system files.

Do not verify file hashes for index protection. Matching bytes confirm length only, not unchanged content, approval, source identity, or version control. Check the index after content changes. If size and registration are unchanged, do not invent an index diff, serial, or timestamp.

### 5.3 Mismatches <a name="errors"></a>

| Code | Condition |
|---|---|
| SOURCE_REF_INVALID | The fixed source is missing or does not match the recorded identity |
| INDEX_ENTRY_MISMATCH | Missing registration, missing entry, wrong type, or mismatched membership or location |
| INDEX_BYTES_MISMATCH | Actual bytes at the selected source do not match registration |

Report code, layer and ID, fixed source, actual entry, registered and actual values, blocked task, and who should investigate. With normal `enforce` enabled, stop access to the layer and stop the current task. Preserve the situation and do not continue implementing from the affected specification.

A consumer does not adjust B to hide an error. The root or owning maintainer determines whether the index is stale, an object moved, or an edit lacks approval. Propose and implement authorized repair. After the repair commit, the consumer explicitly adopts that source and checks it again.

`enforce=false` removes only approved enforced index mismatch stops under root rules. Continue light checks and report differences. Unverifiable source, unavailable necessary files, broken config, and missing authorization remain gaps. `never-ask` controls only the prompt to resume after repair, not reading or writing rights.

### 5.4 Instance specification protection <a name="core-guard"></a>

Always protect the dedicated directory of D:index-spec, D:handoff-spec, D:design-spec, and actually adopted module specs. Removing index rows, omitting K, or clearing layer or module config cannot remove the three core specs from scope. D is not another data layer and does not add a switch. Use existing `enforce`, `restore_prompt`, and repair permissions.

- Check root docs, actual D spec entries, types, rights, sources, per-file B and complete membership under root §1.3 before reading. All core specs must be reachable in that spec directory. Without Git use the approved candidate, inventory and observed guarantees. Do not invent commits or use an old data INDEX for active specs.

Compare actual membership with the owning index's registration, not a temporary list generated from the same tree. Report missing core entries, missing files, loops, escapes, or unregistered members through the existing errors. Matching B does not establish unchanged content; do not add hash verification.

Check rules and task data by their actual source and use. Deduplicate only matches for the same source and object. Check other objects separately, without using data copies as governance. External data follows #guard and its protocol.

After approval, the local maintainer updates the body, D byte count, directory membership, and necessary references together. Readers do not fix counts automatically. For removals or moves, resolve active references and protection under the approved plan before stating an upgrade, removal, or adoption is complete.

## 6. Progressive reading and structural differences <a name="read"></a>

- Start at the owning layer's top-level INDEX and follow the branch through directory entries or local indexes. Search large collections by title, stable key, path, or a bounded tool query, then read matching bodies. Do not infer full-reading permission from a filename.
- If a library still has a large number of entries after its directories are organized, shard its local index as needed and read only the shards needed for the task.
- Report an unregistered ID rather than guessing an old path. Report a missing specification key rather than guessing by chapter number. If a match has no body, report it rather than substituting a search summary or unread material.
- Check consumable partitions and spec entries along layer roots and registered paths. Repository and system items or ordinary content changes within a registered partition are not new governance partitions.
- For T, check only registered categories. Projects, tasks, and batches inside them do not create shared categories. Read originals, recovery batches, and history in D progressively through their entries. A new batch does not require a full scan. Update registration along with actual changes to active specs and their directory.
- Stop current work and report when a consumable partition or spec entry is added, missing, renamed, or moved without corresponding registration. Do not repair the index or move files before a decision.
- Read historical volumes, old adopted originals, and upgrade backups by their entries as needed. Exclude them from current governance rereading and protection scans. Interpret historical paths as they were; do not rewrite them in bulk.

## 7. Maintenance and migration <a name="maint"></a>

- The root maintainer owns its root, D, and local T indexes. External shared T and other layers retain their own maintainers. Consumers read only. Access, issue discovery, or tooling does not grant editing permission.
- Draft the registration and necessary migration for a new object or changed entry. Once authorized, update the object, index, and derived configuration together and verify references.
- If D moves without an internal change, update the root docs entry. If a guide moves within D, update the D index. Use similar ownership for layer entries and local objects instead of duplicating dynamic paths in text.
- Do not store a second `paths` map in config. Derive and check physical config from final entries for Git ignores, tool parameters, and other tools that cannot resolve IDs.
- Verify unique index IDs and specification keys, actual types, reachable entries and sections, registered membership, bytes, reading limits, and cross-document references before marking a pass.
- Index edits do not change admission. Respect the owning rules for K production, R snapshots, and M materials. Register optional modules as active only after actual adoption and support verification.

## 8. Authority and review <a name="auth"></a>

D:index-spec is the local authority on this subject. The root docs entry leads to the D index, which holds actual paths and bytes. Root rules define authorization and minimum startup checks. The guide explains procedures without a second model. Draft, approve, and implement changes with applicable references. Review triggers are in the metadata.
