---
id: handoff-spec
updated: "2026-11-25"
recheck: Changes to adoption direction, setup or migration states, status labels, shared access, handoff structure, item IDs, version classification, dependencies, size notices, placement, or history
---

# Handoff, versions, and resuming

## 1. Purpose and responsibilities <a name="goal"></a>

A handoff lets someone unfamiliar with the chat find the actual workspace, current state and work, decisions, authorization still needed, next verification, and necessary history.

- The root rules govern identity, authorization, and long-term boundaries. HANDOFF records the instance, current items and requirements, and facts needed to resume. INDEX owns actual entries, and config owns confirmed selections and official sources.
- One current HANDOFF contains one current version's work. An approved charter can hold a target version in Ready to start. Template placeholders are not an active version. Record unimplemented requirements as well; recording them does not authorize action.
- Record initialization, development, pending candidate review, user acceptance, version release, and public publication separately. A pass in one does not imply another.
- Restore actual data dependencies through #pin. D:index-spec governs indexing, protection, and reading fixed sources. Module rules apply only after actual adoption and support checks.
- Example versions, paths, and commits demonstrate formats. Confirm actual fields against files, repositories, and user decisions.

## 2. Files and entry points <a name="files"></a>

These are default locations. Resolve the actual docs entry from the root INDEX; the D index records paths within it. Root-relative handoff data uses each file's `root`. Markdown links resolve from their containing files.

| File | Default location | Content and lifecycle |
|---|---|---|
| Current handoff | Root HANDOFF.md | Current state, items, requirements, dependencies, and necessary entries; maintain as authorized |
| L1 generation overview | Root HANDOFF-HISTORY.md | One overview per generation and pointers to L2 and L3; append only |
| L2 version index | `docs/handoff/HANDOFF-HISTORY-INDEX-<generation>.md` | One actual released version per row for the generation |
| L3 stage and completion volume | `docs/handoff/history/HANDOFF-HISTORY-<start>[-<end>][-part-<n>].md` | Actual stage state and formal completion; open volumes append, sealed volumes are read-only |
| Deferred entries | `docs/handoff/HANDOFF-HISTORY-PENDING.md` | Unscheduled, held, or unauthorized work details; no volume split |
| Pitfalls appendix | `docs/handoff/pitfalls.md` | Reproducible environment issues and evidence; split by topic as needed |

Do not create a current handoff for every version. Create L1–L3, deferred records, or pitfalls only when there is actual content. Completing initialization does not create release history, backup, or empty volumes.

Register actual document entries in D. Until history exists, `HANDOFF.history` is `null`. Stage archiving may create L1 and a stage volume before the first formal L2 release row.

## 3. Metadata and workspace lifecycle <a name="meta"></a>

### 3.1 Current handoff metadata <a name="fields"></a>

```yaml
---
doc: handoff
workspace: null
root: null
version: null
status: "Ready to start"
branch: null
updated: null
history: null
---
```

This is a pack template, not a live instance. Discussion, clarification, and charter drafting stay in chat. Under document authorization following user approval, write the charter and necessary supporting files together. Its initial live state is Ready to start. Missing identity, root, or target version cannot establish an instance. Do not add uninitialized, initializing, or another preparatory state.

| Field | Sole responsibility |
|---|---|
| doc | `handoff` for the current handoff |
| workspace | User-confirmed workspace name; it need not match the directory |
| root | Actual absolute workspace root, for resolving paths; it grants no root role |
| version | Approved target version of the current work, recorded when the charter takes effect. Ready to start is not version completion. A pack template may use `null` |
| status | Workspace lifecycle under #state. Item state and work mode use their own rules |
| branch | Actual branch in the owning repository; `null` before creation or if unidentified; “—” when explicitly without Git. Do not enter a planned branch as fact |
| updated | Actual last maintenance date; an unused template may leave it `null` |
| history | Path within the root to the existing L1; `null` without history |

Do not use `initialized` or a substitute preparation flag. On takeover use user approval, actual root, charter, config, tasks, and observable state. Old fieldcase flags do not decide takeover, rebuilding, or implementation. Remove them from current files on the next authorized revision under this model. Do not change historical records or adopted originals. A same-named field independently defined and approved for autonomous governance follows its own authority.

Use config for `locale` and `governance_adoption`. The local `version` does not replace the official core or module sources. Record adoption route, source and target, copy list, actual work, and authorization in the snapshot and E. Do not create a separate initialization document, consumption log, or duplicate path map.

When actual parent requirements apply, add `shared_layer` and `root_governance` to local handoff metadata for the adopted parent specification baseline and inherited root governance generation. Parent rules determine omission at their own root. Verify values; do not copy examples, use local or official core versions as substitutes, or read private parent handoff without rights. Do not prefill deployment values in a generic template. Keep actual data sources in the data table. Records of the same governance basis must agree, and a data pin does not replace current management rules.

### 3.2 Three states and transitions <a name="state"></a>

Store the exact values below in English workspaces governed by this revision. Read existing labels under the instance's adopted specification. On upgrade, locate the former specification by exact source and batch in D:upstream. Approve the mapping of current fields and item labels before writing. Preserve the version, item IDs, actual state, conditions, originals, and history. Pause dependent work if the mapping is unclear. Resume an interrupted conversion from the approved mapping and actual progress under #init-resume.

| status | Scenario and transition |
|---|---|
| Ready to start | The approved charter and required files are written, but the current work has not started. Applies on first adoption or a later version |
| In development | Authorized concrete work has started but the version is not formally released. Environment setup, dependencies, copying, Git creation or commits, and implementation count as work |
| Released | Applicable acceptance and explicit release permission are established, and the required actual commit or fast-forward, backup, history, and closure steps have been met. Without Git, verify the approved alternative and state the actual limits |

```text
Type: state machine | Workspace lifecycle
Ready to start → In development → Released
      ↑                              │
      └─ Next approved round, no work ┘
```

After release, keep the actual version and Released until another round is decided. Once the next approved charter is written and before concrete work, it is Ready to start. If work starts immediately, record In development. Do not force a separate stop, revert, or duplicate state change just to show each state. An unfinished version remains In development during a pause, blocker, pending review, or discussion. Record remaining work in the item state and section D rather than hiding it by reverting to Ready to start.

Lifecycle grants no permission to work, commit, back up, or publish. With document permission alone, stop at Ready to start. If the same explicit permission also covers work, proceed within scope to In development without asking again. Coordinated writes are not atomic across files or repositories. A state value does not establish that files, copies, repositories, or verification are complete.

The suggested first version is 0.1.0.0, confirmed at charter approval. Setup and same-version tasks use the same target version, not a dedicated initialization version. For versions, branches, and first commits see #branch and #release. For layer identity see D:index-spec#identity. Workspace state does not create a fixed consumption baseline.

If an applicable parent uses the same `status` field with different semantics or values, resolve applicability first. Do not add another state field to bypass it or turn direction 1 into autonomy. Keep unresolved dependencies as gaps rather than claiming a real adoption pass.

### 3.3 Facts to retain on interruption <a name="init-resume"></a>

Keep only necessary facts in existing handoff: the source and remaining scope of authorization, approved plan, target version, source and target, completed and remaining steps, copy basis, actual files and commits by repository, blockers, and conditions to resume. Record copying, governance alignment, repository setup, and verification separately. Keep the source by default and record its disposition separately for an explicitly required move. Read authoritative values from their INDEX, config, or rules rather than copying them here.

Resume unfinished work only. Do not rebuild repositories, redo commits, or use missing fields or old `initialized` as reasons to restart setup. If charter writing is incomplete, complete only the approved documents. If work has started, keep In development and record remaining work. After a pause or discussion, obtain explicit execution before resuming. Answers and drafts without write permission stay in chat; reuse them only if reliably recovered.

## 4. Current HANDOFF structure <a name="tpl"></a>

Keep the numbering and names below for cross-document references. Add private sections after the standard structure without changing §1, §2, or §3.1–3.6.

```text
1. Version task overview
2. Current work items
3. Handoff snapshot
   3.1 A. Current state
   3.2 B. Environment and tool pitfalls
   3.3 C. Decisions
   3.4 D. Awaiting user direction
   3.5 E. Requirements for the current version
   3.6 F. Later versions
4. Hard rules
5. Coverage and version release
6. History index
```

### 4.1 Two levels of task tables <a name="tasks"></a>

Version task overview:

| # | Version | Topic | Source | Status | Priority | Dependencies and limits |
|---|---|---|---|---|---|---|

Use the current item table when breaking down the current unit:

| # | Stable ID | Item | Status | Dependencies and limits |
|---|---|---|---|---|

Both are tables with sequential numbering from 1. The version table shows the big picture. Current items break down only the active unit at one level. Leave the table empty if no breakdown is needed; do not invent placeholder work.

Keep current dependencies and remaining items. Summarize old versions by major family with history pointers. Move completed items, their progress, and out-of-date details under #hist. A single key sentence does not justify keeping a whole section.

### 4.2 Snapshot sections <a name="snapshot"></a>

| Section | Content |
|---|---|
| A | Actual paths, version and branch, repository layout, Git capabilities, commit/release/backup state, services and ports, read-only resources, data dependencies, and recovery entries |
| B | Necessary triggers, actions, and entries. Use #pending-pit for problems, causes, fixes, retests, and evidence |
| C | User decisions, rationale, and basis. A proposal is not a decision |
| D | Still-needed user decisions or permissions, in priority order, and their impacts |
| E | One acceptable goal for the version, source, scope, locations, dependencies, limits, completion conditions, and acceptance entry |
| F | Registered future topics outside current scope, their source, dependencies, limits, and necessary pointers |

Keep only current action criteria and authorities in §4. Propose lasting responsibilities, permissions, hard rules, and methods for local governance. Use D:design-spec#scope, D:design-spec#split, and D:design-spec#use for design content, placement, single parameter authority, and distillation. Put approved design guidance in local DESIGN. Link to the governing spec or source for procedures. Give each rule one authority. Approve creation and migration of files; do not pre-create empty containers. §5 records actual commits, coverage, logs or backup, and publication policy. §6 gives actual history entries and search method.

Give detailed manual acceptance steps in the chat. Keep state, conclusions, evidence, and gaps in HANDOFF rather than duplicating long instructions.

### 4.3 Current handoff size <a name="size"></a>

When changing versions, reread the full current HANDOFF and report its actual UTF-8 bytes including metadata. Include these notices with normal drafting:

| Trigger | Notice |
|---|---|
| ≥50,000 B at a version change | Remind the user to schedule MVD measurement and cleanup |
| At 90,000 B | Warn, identify the major contributors, and suggest archiving and sensible version boundaries |
| ≥100,000 B | Warn in each draft; use actual thresholds again after reduction |

These are notice thresholds, not reasons to omit facts, requirements, limits, or acceptance or to split versions automatically. Follow #cleanup. Split only into deliveries independently acceptable in their own right. Preserve actual remaining, review, and publication states. See #hist for volumes and appendices.

## 5. Work item identity, states, and presentation <a name="items"></a>

### 5.1 Stable ID <a name="item-id"></a>

- Where no stable key exists, use `<event-type>-<serial>-<short-name>`. Choose or add short prefixes to suit the workspace's work. Record the meaning of each type used in its handoff. Examples include `ini` setup, `cre` content creation, `fea` capability, `fix` repair, `cho` governance maintenance, and `sub` subtask.
- Within a major family, assign serials consecutively from 01 across all types. Use two digits for 01–99, then 100, 101, and so on. Each issued type and serial pair identifies one work item for that major. A new major can restart at 01. Keep the IDs of work carried across versions and skip pairs still in use.
- Use a few words or a recognizable abbreviation, just enough to identify the work item. The limit is 20 characters, including internal hyphens. Rewrite an overlong short name without mechanical truncation.
- Keep identity across renames, reorder, table moves, state changes, and versions. Both names and IDs must be unique in a current list. Do not reuse an assigned identity for another item.
- Use # for this round's reading and review only. Use the ID for persistent references, with workspace for cross-workspace use and version for historical references. A table with its own stable identity such as version does not need another item ID column.
- When migrating numbering, map the old version and table location to the new ID. Preserve history as written.

### 5.2 State table <a name="status"></a>

For English handoffs governed by this revision, start each state cell with one marker and the exact label below, followed by needed detail. Interpret earlier labels under #state and preserve the recorded state and any freeze condition when mapping them. These are work item states, not the workspace states in #state. Completion, blockers, and pending review do not change lifecycle by themselves.

| Stored label | Meaning |
|---|---|
| ✅ Complete | Agreed conditions are met with verifiable evidence. Where manual acceptance is required, record Complete only after the designated reviewer confirms a pass |
| 🔄 In progress | Work is underway |
| ❌ Rejected | Failed or rejected |
| ⚠️ Blocked | Blocked by a concrete gap |
| 👀 Pending review | Work exists and awaits the user or designated reviewer. A passed self-check goes here first if manual acceptance is required |
| 💡 Pending decision | Awaiting discussion, decision, or instruction |
| ⏸️ Paused | Paused or deferred |
| ⬜ Not started | Work has not begun |
| 🧊 Frozen | Do not expand. Add `Unfreeze: <decidable condition>` in the same row |
| 🗑️ Discarded | Do not proceed. Archive with this version |

Freeze remains until the condition is met. A new version neither lifts it nor requires another question. When met, give the evidence for user confirmation and normally propose Pending decision. If obsolete, propose Discarded. Before release check all frozen conditions. If none are met, record only a count; obtain and record the user decision for met or obsolete conditions before closing.

### 5.3 Lists, reordering, and quick review <a name="review"></a>

- Use the corresponding version table, current items, or awaiting-action section when asked to list them. Show both # and stable ID for items; do not create display numbers.
- Propose migration first if IDs are missing. Reorder completed items ahead of the rest without changing relative order within each group; renumber # consecutively. With quick review, keep completed order and arrange other items by review prerequisite, dependency, and closure order; preserve order where unconstrained.
- Quick review defaults to current HANDOFF, or the draft the user specifies. Take only unfinished items in the chosen §2, including paused, frozen, and discarded work. Do not import items from F, history, or other sections. Keep their boundaries and resume conditions. Listing does not reactivate them.
- Keep # from the source current or draft table in quick review and manual review subtables; gaps are allowed. Name the source. Use “—” for an F item with no §2 number.
- Show the full proposed reordered table, then quick review in the same order. Manual review gives full object name and type, actual entry and location, action, pass conditions, untested areas and known gaps. State shared prerequisites once and describe related coverage.
- For frozen or discarded items with nothing to verify, show status only. If something remains to check, say what it is.
- State when an entry is unverified rather than asking users to guess paths, search handoff, or invent steps. Use `config.review.layout` for lists versus tables. The version, item, and reordered tables remain tables.

## 6. Version lifecycle and increment rules <a name="life"></a>

### 6.1 Minimum complete goal <a name="scope"></a>

Put one complete acceptable version goal in E. Determine the next version by actual feedback. F records later work only. Do not discuss, design, or implement it ahead of scope. The user raising a future item does not authorize it in this version.

For additional fields, capabilities, or rules outside scope, list the item, actual cost of not doing it now, and proposed disposition. The user decides current, later, or omit. Verify statements about the current situation. Do not act on hypothetical future pain.

Do not pre-build unused abstractions, runtimes, permission matrices, coordination, migration scripts, or files. Minimality does not justify removing required languages, layers, modules, or verification.

Before drafting governance, apply MVD under #rules. Use size as an observation and preserve necessary criteria, boundaries, destinations, exceptions and recovery.

### 6.2 Version objects and increments <a name="ver"></a>

Maintain the instance version, official core source, each adopted module source, and each data layer version separately. `config.fieldcase_version` and source entries in `modules` record adopted source versions. Take the actual comparison baseline from the active entry in D:upstream. Ordinary local customization preserves the recorded source.

The instance uses four parts, `0.<major>.<minor>.<patch>`. The initial 0 denotes a format not yet stabilized and does not count for classification. A trailing zero can be omitted if the version is unambiguous; prefer all four parts in records.

| Level | Criterion |
|---|---|
| patch, fourth | Repair, clarify, or correct existing behavior; add a constraint; change data or parameter values without a new usage method; or repin only |
| minor, third | Add a capability or mode the consumer can use, or remove an existing method; the consumer needs to learn a new way |
| major, second | Change partitions, path bases, metadata, version or pin mechanisms, or the increment rules themselves |

Use minor when only an item's location or name changes and an existing reference becomes invalid. Examples include moves or renames of section numbers, titles, field names, paths, commands, and checklist items. Use major when the change itself meets a structural criterion in the table. Update affected active references in both cases. Classify by behavior and structure, not line count.

A correction with evidence of the erroneous record and changes only in leading metadata may be recorded without a new product version. A real dependency update is not such a correction. Follow root rules for independent private governance maintenance, without releasing the product again for that reason. Classify changes to product text or behavior by actual effect.

### 6.3 Repositories and branches <a name="branch"></a>

Use the selection in root governance rather than selecting it again each round.

| Method | Behavior |
|---|---|
| Branch development | Establish a common starting commit in a new repository as below. Develop on `dev/<current-version>` and preview on `pre/<topic-or-version>`. Keep main at the starting point or last release while developing; advance with ff-only at release |
| Direct main | Maintain main within authorization, without a branch fast-forward. Do not claim stable formal directories plus same-repository worktree isolation |
| Custom | Establish branch names, purposes, and closure rules, then follow the approved method |

Repository creation and first commits are In development. For an approved local repository with no commits, the plan names root, author, main starting point, initial commit scope, and next branch. It can commit the approved charter and necessary files to main as a common start, then create `dev/<current-version>` before later work. Both use the same first version. The starting point is not an initialization version, completion marker, or formal release. Do not create a special completion tag by default.

Repository operations and committing require authorization, not just permission to write documents. Do not use the new-repository starting procedure for an existing HEAD, source or ancestor repository, external shared repository, or in-place upgrade. On interruption, keep actual commits and tags and complete only remaining steps. Stop the affected Git work for a decision if applicable parent rules conflict or an authorized party requests confirmation. Reuse existing authorization and do not exempt main protection.

Record versions and fixed references from their actual repository and content source. Keep external shared repositories and versions intact. T has no separate repository. For migration, copy approved business content, align governance and entries, then create the target repository locally as applicable. A prepared charter is not a completed migration and does not authorize creating an empty base repository early. Keep old history as an authorized source, separate from target version. A T worktree belongs to the original repository; without common history, do not fast-forward.

Same-version development can contain multiple commits without repeatedly incrementing, advancing main, or notifying every workspace. Keep consumed commits reachable and fixed tags unchanged. A fixed consumption baseline needs a complete, approved source and actual reference; a first commit does not create `stable_ref`. A branch name is not a substitute for a commit reference.

Use `pre/<topic-or-version>` for previews only, keeping the workspace version unchanged. Never release a version from a preview branch or merge it into `main` or a development branch. Implement approved preview work on the development branch. Retain or delete preview branches under user authorization. Maintenance of an older version, merging or rebasing, reset, and branch deletion need applicable authorization even for urgent fixes.

### 6.4 Start, commit, release, and publish <a name="release"></a>

1. Agree on target, scope, dependencies, and completion conditions in chat. Once approved, write the target `version` and E under document authorization. The first live state is Ready to start. Record the actual branch, or leave it unset before a repository exists. Document preparation in an existing repository stays in its authorized path and branch and protects main.
2. At explicit execution and the start of concrete work, enter In development with the same version. Set up the chosen working arrangement and record absence of Git honestly. Report necessary blockers and remaining work; a filled version field is not permission.
3. Implement, verify, fix, and verify again within authorization. Commit by specific paths without staging everything or committing another person's changes. Finishing a stage, going back to discussion, or waiting for review does not revert the lifecycle.
4. Submit for user acceptance. Finishing development or a stage Goal is not release. To release, obtain user acceptance and explicit release permission. An option mentioning release, or clicking such an option, does not grant release permission.
5. Close under #check. If branch mode cannot fast-forward, stop for a user decision. Do not independently make a merge commit, rebase, or reset.
6. Public publication needs separate actual authorization and a verified official entry. A local version release does not signify public distribution.

Amendment: when the user's version instruction explicitly requests an amendment, check the actual local version. Stop and ask if it differs. If the version matches and Git is enabled, use `git commit --amend` for that version and rewrite the cumulative message. Replace the same-version backup only within existing permission and check consistency. Keep consumed commits reachable and stable tag targets unchanged. If these conditions cannot all be met, ask whether to make another commit or version; do not silently rewrite fixed references. Handle multiple versions in order, implementing, accepting, committing, and backing up each. Ordinary added development commits are not this mode. Without Git, state that no commit will run.

## 7. Data dependencies and actual pins <a name="pin"></a>

Use one table, one row per layer, in the consuming HANDOFF §3.1 for pins and actual use:

| Layer | Adoption mode | Content version | Fixed source |
|---|---|---|---|
| K | Development | `<layer_version in selected INDEX>` | `<fixed development commit ID>` |

Modes can be development, formal, or candidate trial. Use actual version and fixed source for external shared layers, without inventing missing setup metadata. Where Git and reliable copies are unavailable, state local contents and guarantees. A consumer without its own Git can still use a source with a commit. Record each source's actual content version. For a joint upgrade, state the combination used.

Record the layer and stable ID scope and prior formal version and reference in the same place for a trial. Reviewing a candidate does not repin. End the trial by restoring the original dependency or approving a new stable baseline. Reuse applicable candidate verification when formalizing it, but check final differences.

Layer INDEX describes content rather than consumers. Config holds the default strategy, not a second copy of dependencies. On resume use the table to read INDEX and body from the same source; do not update silently. Report unavailable fixed sources rather than substituting current main or a search summary.

When restoring a previous workspace state subject to parent governance, take the verified `shared_layer` and `root_governance` from that version's handoff records. Consult the historical governance basis through an authorized source and check how current rules apply to the restored state. For a Git source, search its actual version record for the commit that introduced the recorded version value, for example with `git log -S`. Verify the commit against the adoption record, then use `checkout` in an authorized isolated worktree or repository copy to inspect that state. For a source without Git, consult the recorded fixed original. Report any ambiguous source or conflict in applicable rules and pause the restoration that depends on it.

## 8. Retaining and moving current content <a name="cleanup"></a>

Judge each paragraph by current and clearly established later dependencies.

| Impact if removed from current view | Action |
|---|---|
| Critical | Keep the necessary information as written if work would stop or broad history review would be required |
| Important | Shorten without losing key current details |
| Ordinary | Summarize, combine, or move to history, with pointers as needed |
| Insignificant | Archive if provenance matters; otherwise remove |
| On hold | Put details in the separate deferred record, leaving ID, state, a line, and pointer |

Keep necessary current facts, remaining work, criteria, and decisions in the handoff; move completed items, old requirements, completed procedures, and older details through #hist. Put unscheduled details in the separate deferred file with necessary pointers. Place pitfalls, design guidance, lasting rules, and procedures per #snapshot. Approve creating or moving the files, and keep necessary entries reachable.

For measurement, give five tables by impact, with location, current dependency, recommendation, bytes before and after, and destination per item. Calculate the proposed value from a complete draft. Mark proposals not yet drafted. Information recoverable through a pointer is not lost. Past importance and possible future use do not prove a current dependency.

Moving text does not change decisions, freeze, acceptance, or publication. Do not move already archived material again. Mechanical volume splitting reads headings and necessary metadata only. Move exact bytes and compare them with tools, without rereading all history through the model.

## 9. Three levels of history and appendices <a name="hist"></a>

### 9.1 L1 generation overview <a name="l1"></a>

Metadata: `doc: handoff-history`, `workspace`, `root`, `latest`, `count`, `updated`, and `current`. Use the latest formally archived version for `latest` or `null`. Count only numbered formal archives; stage entries do not increment it.

Give each generation a heading, short identification, overview of actual changes, and pointers to L2 and needed volumes. A generation is the first two version parts, such as 0.1. Do not include full completions in L1.

### 9.2 L2 version index <a name="l2"></a>

Metadata: `doc: handoff-history-index`, `workspace`, `root`, and `updated`. Append one row per version:

| # | Version | Topic | Search keywords | Release date | Backup entry | Volume |
|---|---|---|---|---|---|---|

Use one to three likely symptoms, filenames, or rule names as keywords. The real volume must contain the version section. Do not invent release dates or formal rows for unreleased versions.

### 9.3 L3 volumes <a name="l3"></a>

Metadata: `doc: handoff-history-archive`, `workspace`, `root`, `scope`, `archived`, and `frozen`. State actual range in `scope` and opening date in `archived`. An open volume has `frozen=false` and can append; sealed volumes have `true` and are read-only.

Organize volumes by the largest applicable unit, without mixing majors. Measure the complete volume in UTF-8 bytes, including metadata. Split by minor, then patch, then `part` only when the projected volume for a unit exceeds 100,000 B. An open volume with an unknown ending version omits it in its name. Keep the filename when sealing and record the actual range in `scope` so pointers remain valid.

Append stage records and formal completion entries to an open volume. Set `frozen=true` when the unit covered by that volume ends or the actual volume reaches 100,000 B. The sealed volume is read-only. Open the next volume when there is material to file.

Development stage entries show version, In development, and provenance, rather than using a Released completion statement. Formal completion adds the original requirements, release and backup, version highlights, and any existing stage pointers. Do not duplicate text already archived.

Remove state emoji when moving an item to a volume. Preserve the original short label, wording and judgment. Locate archived items by version and stable ID where known. For a state search spanning revisions, look for each exact archived label under its applicable specification. When an earlier specification is unavailable, report the recorded label as written and use the item ID or version to locate it. Keep volumes and indexes in the selected repository and necessary backups rather than ignored directories. Without Git, state the loss of repository history and still keep reachable files.

Archive earlier unnumbered work by its actual date range, read-only. Do not infer versions, mix it into version volumes, or create an L2 version row. Give it an L1 overview, keywords, and a verified backup anchor if available. State missing date evidence rather than guessing.

### 9.4 Deferred entries and pitfalls <a name="pending-pit"></a>

A deferred record uses `doc: handoff-pending` with `workspace`, `root`, and `updated`, indexed by ID without volumes. Keep only necessary pointers in F. Read targeted entries when the user names them or their dependencies apply, rather than expanding all future work.

A pitfalls appendix uses `doc: handoff-pitfalls` with `workspace`, `root`, and `updated`. Keep a trigger, action criterion, and entry in B, with evidence in the appendix. Keep incident numbers stable and never reuse them. B item `n` points to `pn`. Create an entry for an actual issue, with the finding and gap if evidence is not yet available.

Append by topic and correct by addition without erasing history. Split a single file only beyond 100,000 B. Before writing to a controlled record, remove tokens, cookies, internal network addresses, real email addresses, actual private addresses, and unnecessary sensitive material. Preserve reproducible timestamps to evaluate freshness.

### 9.5 Finding history <a name="find"></a>

Read L1 metadata and generation headings, find the L2 version row, then only its L3 section. Without an exact version, search keywords through the relevant entries. Look up deferred items and pitfalls by ID and keyword instead of reading all history. When investigating a recurring issue, search both the current HANDOFF §3.2 B and the registered D:pitfalls appendix for the same symptom, error code, or keyword. Use the incident number to find the entry.

When archiving, update current references to actual historical sections. Read historical originals with their original paths; do not rewrite them in bulk. Compare original bytes before and after moves and verify indexes and references together.

## 10. Release checks <a name="check"></a>

### 10.1 Before the release commit <a name="pre"></a>

- Current E has reachable source, scope, limits, dependencies, and acceptance evidence, with valid stage pointers.
- The actual repository root, branch, and version match the handoff. For branch development, check ancestry with `git merge-base --is-ancestor main dev/<current-version>`. Replace the placeholder with the actual target version in HANDOFF. For example, use `git merge-base --is-ancestor main dev/0.1.0.0`. Exit status 0 passes the check. Stop and obtain a decision if the branches have diverged or you cannot verify the check. Follow the approved closure rules for custom branches.
- The user accepted the work and explicitly authorized the version release. A pending candidate, initial main, fixed consumption baseline, or development commit is not completion.
- Current tables, item states, remaining and decided items, dependencies, and needed logs agree. Use the project's selected log location; do not create extra logs for this checklist.
- Check freezes under #status and relevant active contracts only if their module is installed. Follow its spec for necessary local disposition. Do not scan unrelated history.
- Active links resolve, version and state metadata agree, and evidence, distributable artifacts, and recovery backups have distinct purposes and scope.

### 10.2 Release actions and later archiving <a name="post"></a>

- Make the authorized release commit. In branch mode, fast-forward main with ff-only. Follow the chosen rules for direct main. Without Git, explicitly record that no commit or fast-forward runs.
- Save and verify the agreed version backup. Report release only once commit, main, and backup agree.
- Add the actual completion to L3 and check the sealing conditions in #l3. Append the L2 row and update the necessary L1 overview and counts. Refer to earlier stage entries rather than copying them.
- A post-release archive commit belongs to later maintenance or the opening of the next version. Do not claim archival work completed before it happens. Day-to-day placement during development is not release approval.
- At a version change, reread the entire current HANDOFF and report bytes, alerts, and reference checks under #size. If another version has not been approved, preserve the released state with the next round awaiting instruction. Record public publication and its address only on actual authorization and results.

## 11. Resuming and writing rules <a name="rules"></a>

- Follow root §1.4 for resuming and rereading. Restore fixed sources under #pin. Chat memory is not an actual input.
- Handoff must be self-contained without the original chat. Do not use “the thing from earlier” or “same as above” instead of a target, basis, or entry. Record the scope of original user permission; agent messages do not authorize work.
- While document authorization is valid, promptly record the states, site facts, decisions, blockers, and evidence pointers needed for resuming in the current HANDOFF. If compaction or a new chat is imminent and necessary material cannot be written in full, record its topic and source in §3.4 D for items awaiting authorization or §3.6 F for later work. Keep drafts in chat during ordinary discussion. Fact recording follows the existing write authorization.
- Give each fact one authoritative place and reference it elsewhere. Verify and repair contradictions within authority; do not erase differences for convenience.
- Keep current criteria and boundaries in specs. Put schedules, decision processes, and change history in handoff facts or history. Metadata, a line necessary to interpret history, and evidence timestamps may stay.
- Do not use bold as hierarchy in current handoff, L1, L2, or specs. Use approved status labels in tables. Give each numbered item its own line and do not put multiple circled numbers on one line.
- Do not include unauthorized rules in drafts, replies, or deliverables. List a new concern, its impact, and recommendation separately for decision.
- Before drafting governance, apply MVD to the criteria, boundaries, destinations, exceptions and recovery requirements. Test deletion item by item, shorten without loss, and explain retained weak clauses. Provide actual candidate bytes before and after, line changes and percentage; mark an undrafted size unavailable. Size serves the approved behavior.
- For nonconforming existing governance or history, propose migration scope first. Preserve facts and evidence of byte equivalence and migrate under authorization. With Git and commit authorization, commit history migration separately in the owning repository, restricted to the listed paths, so the move can be rolled back on its own. Do not remove needed material merely to fit a format.
- A host can use an approved pointer when it expects a different governance filename. Do not duplicate rules. Verify host capabilities and state unconfirmed gaps.

## 12. Authority and review <a name="auth"></a>

D:handoff-spec is the local handoff model. Resolve it through the root docs entry and D index, which owns the actual file and bytes. Do not add an alias table. Root rules own permissions and documentation approval; the guide gives procedures. Review triggers are in the metadata. Update actual affected templates, indexes, references, and necessary verification together.
