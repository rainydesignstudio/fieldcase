# Layer and module adoption

This document contains the optional K/R/M materials, targets, supporting changes, and checks for the three modules. The root rules govern permission; use D:agent-guide for procedures. Apply the following only after the user chooses the options, approves the complete plan, and authorizes execution.

## 1. Compatibility and shared steps

- This core uses root files plus D and T, with all specs in D/spec and no root `rule-*` aliases. K, R, and M are optional and do not go into `config.modules`. Confirm the professional, custom, or minimal layout with the user. Empty arrays in the pack do not select minimal.
- Use the distribution INDEX in this directory for the version and sources of the supporting materials. Use §1 of the pack README at the same fixed resource root for the pack batch. Do not infer compatibility when layouts differ at the same version. Keep old originals, raw tests, and fixed sources at their original locations and scope. Do not claim new behavior was tested.
- The methods for `knowledge-acquisition`, `cross-workspace`, and `unattended` can be installed on D and T. Formal knowledge output separately needs an approved K target. Installation does not automatically create K, retrieve materials, communicate, start a Goal or heartbeat, or establish runtime verification.
- Before adoption, preserve originals from a fixed pack. In an existing instance compare old originals, current customization, and new originals. Check recovery coverage for this work. Reuse Git where sufficient; snapshot gaps only. Available materials do not change the adoption direction, local version, source version, or permissions.
- Install active specs only in the local dedicated D spec directory. The D index owns entry, type, and bytes. Leave unselected specs as materials, not active entries. Recalculate any example B at adoption; continue numbering and retain stable IDs.
- No external skill, tool implementation, or business knowledge base is a required dependency. Project skills are not supplied, so selecting all modules does not imply wrappers exist.

| Selection | Default active target | Supporting changes |
|---|---|---|
| K | knowledge/AGENTS.md and knowledge/INDEX.md | Root K entry, actual library protocol, protection, and chosen repository. External K retains its own entry; do not overwrite it with templates |
| R | references/INDEX.md | Root R entry, protection, repository, and reading limits |
| M | materials/AGENTS.md and materials/INDEX.md | Root M entry, maintenance rules, governance bytes, and repository |
| knowledge-acquisition | docs/spec/cache-spec.md | D entry, root method notes, T cache notes, and exact module source |
| cross-workspace | docs/spec/contract-spec.md, and contract/INDEX.md when authorized to build local T | D entry, mode registration, contract index exception, authorized T entry, and module source |
| unattended | No additional permanent file | Root §1.5, §2.1, and §2.6 additions and module source; no task is started |

## 1.1 Installing and inheriting specifications

Put method specs in the same local dedicated directory as D:index-spec. Register the actual entry, specification type, and bytes for cache-spec or contract-spec in D. Do not add root aliases, a D repository, or a D version. Example literal paths are not compulsory: resolve tool arguments through root docs and D entries.

Applicable parent modes remain in force. A same-named file in external K does not establish a locally installed module. Explain conflicts or same-name definitions and ask the authorized party to resolve them, rather than overwriting parent rules. Omitting K does not remove a parent rule already in force.

Shared K/R/M/T remains with its current maintainers. Put local procedures in local root governance. The owner still approves formal output for shared K. Reuse only authorized existing categories and ownership in shared T. Do not overwrite an upstream index with an empty one, add a shared category, or create a second T. Report missing dependencies rather than marking capabilities ready.

## 2. Optional K, R, and M

### 2.1 Place files and register root entries

Copy only selected local originals to approved targets. Locate K via knowledge-governance and knowledge-index in the distribution index; find R and M by their IDs. Before importing an existing knowledge base, check its structure, index, license, and scope. Register a real shared entry without overwriting its original governance or index.

The root table already has docs and T. Add only selected K, R, and M entries in order before T and renumber consecutively. Do not add a second D row or repository. Example additional rows for the professional layout:

```markdown
| 8 | <a id="K"></a>K | Knowledge layer | Index | [K index](knowledge/INDEX.md) | Use K:<id> under this layer's actual protocol. Specifications retain their approved scope |
| 9 | <a id="R"></a>R | Reference layer | Index | [R index](references/INDEX.md) | Use R:<id> for fixed references and evidence without editing the source snapshot |
| 10 | <a id="M"></a>M | Materials layer | Index | [M index](materials/INDEX.md) | Use M:<id> for governance and approved production material |
```

Do not add R AGENTS. K and M maintenance rules apply only on local creation or explicit adoption. Do not copy the three D core specs into K. Do not register unselected layers or create empty layers for a minimal or custom layout.

### 2.2 Protection, repositories, and the actual state

D core and its dedicated directory are always protected. Derive data-layer `layers` and `targets` from actual root entries, adopted rule files and full directories. Both may be empty without data layers or applicable targets, with the basis stated. Do not omit actual active objects. Verify identity and bytes under the local seven-column model or actual external protocol. Preserve approved custom targets and do not assume K:specs exists.

Git actions belong to authorized work in development. Use the approved repository roots and tracking inventory in the plan. D is maintained with the workspace. T has no separate repository. Preserve external repositories. Derive ignores from actual entries and tracking scope, keeping required documentation.

An existing instance does not lose its K, data, repositories, history, or version because K is now optional. Remove an old K from active use only with separate authorization, an explicit reason it is no longer needed, and a clear inventory, references, history, and recovery plan. Otherwise retain it and move only approved governance and references. Migration still copies business content and aligns governance before creating Git at the target; do not create an empty base repository early.

### 2.3 Checks

Check required D files, selected entries, actual data and protocol, full protection, governance byte counts, and permission separately. Check actual repository root and commits only when Git is selected. Label static checks as static. They do not prove an import, shared adoption, or runtime capability.

## 3. knowledge-acquisition

### 3.1 Specification and procedure

Install cache-spec.md from the fixed original in local D/spec. Continue existing D row numbering and use the actual B:

```markdown
| N | <a id="cache-spec"></a>cache-spec | Knowledge acquisition and cache specification | Specification | [Method](spec/cache-spec.md) | Actual B | Applies after module adoption; verify D protection before governance reread |
```

Reference D:cache-spec from the local root's adopted module instructions. Do not alter shared K governance or move local framework rules into K. Installing the method does not require K. Without a selected formal destination, do not create an empty layer. A raw-only task can end at its authorized T location; formal usable knowledge needs an explicit K target, content index, and approval by its owner.

### 3.2 T support and permission

Add the following only with permission to maintain local T. For shared T, keep its INDEX and use the actual cache entry and authorized owner path. Put local procedure references in root rules:

```markdown
- When using knowledge acquisition, keep approved raw material and tools under the actual owner path in T:cache. Put formal output in K after approval. D:cache-spec defines the method. Network, tool, and directory actions still need task authorization.
```

Do not add a shared T category or run fetch, convert, index, or verify on installation.

### 3.3 Checks

Check the D entry, actual B, complete directory, and references. Verify the distinction between raw material and output, first-use toolchain approval per stage, the per-job optional verify choice, and offline usability. Record installation and actual retrieval separately. A missing K target neither installs K nor produces knowledge.

## 4. cross-workspace

### 4.1 Specification, index exception, and T entry

Install contract-spec.md in local D/spec and register its ID, actual spec path, type, and bytes. Use the empty contract/INDEX.md only in an authorized local T. A shared T only uses its real compatible entry. Record an absent category or protocol as a gap; do not create a second T or overwrite the upstream index.

Append the following exception to local D:index-spec#local and recalculate the D size entry. Do not change external provider specifications:

```markdown
When cross-workspace collaboration is adopted, use the active and archived contract tables in D:contract-spec#idx rather than the generic seven columns. Mark its actual T index entry as Dynamic. Read bodies per task. This exception does not replace full D specification directory and per-file byte protection.
```

Example D row; use the actual row number and path:

```markdown
| N | <a id="contract-spec"></a>contract-spec | Cross-workspace contract specification | Specification | [Method](spec/contract-spec.md) | Actual B | Applies after adoption. Check complete D directory before governance reread |
```

Add the actual contract entry only with local T maintenance rights. For shared T, use its own registration and do not copy this row or empty template:

```markdown
| N | <a id="contract"></a>contract | Cross-workspace contracts | Index | [Contracts](contract/INDEX.md) | Dynamic | Read active entries by default; open bodies for the task. D:contract-spec governs ownership, sharing, and archiving |
```

### 4.2 Register root modes

In root §2.1 after Discussion: Reply, add:

```markdown
| Discussion: Contact | Under §2.4.1 only, send an introduction or non-execution reply to a target the user names, without writes or task dispatch |
```

In the §2.2 execution table add:

```markdown
| Execution: Dispatch | Under §2.4.2, send this self-contained task to a specified existing session; do not take over its work |
| Execution: Dispatch to a new session | Under §2.4.3, create the specified new session and deliver this task. Other creation rights are separate |
| Multi-session execution | Switch explicitly and verify actual capability under §2.4.4; dispatch within named roles and scope |
```

At the end of §2.3 Manual dispatch, add:

```markdown
Manual dispatch suspends automatic dispatch, replies across sessions, redispatch, and waiting. Explicit contact or dispatch permits only the communication in §2.4. Full multi-session coordination requires an explicit switch; one dispatch does not imply it.
```

At the end of §1.4 Taking over and rereading, add:

```markdown
- When cross-workspace collaboration is adopted, read only active contract entries by default. Open bodies selectively and leave archived entries unread by default; see D:contract-spec#idx.
```

Keep the shared limits in §2.4 and append this text before §2.5:

```markdown
#### 2.4.1 Discussion: Contact

- Once the user names an existing target, send only this introduction or non-execution reply. If a draft exists, use its scope. Otherwise introduce the bound workspace, agent identity, and purpose, and request acknowledgment and needed information.
- No execution task or file write. Use §2.4.2 and §2.4.3 for execution dispatch. Clarify an unknown target; do not scan and contact all sessions.
- Report sending and receipt separately. If the tool is unavailable, provide text to forward and record it as unsent. A received message does not authorize an automatic reply.

#### 2.4.2 Execution: Dispatch

- Once the user names the existing session and execution task, send a self-contained §2.3 task package with bound workspace, agent identity, verifiable original user authorization, scope, review gates, and required reply.
- This grants one dispatch, not multi-session coordination. The recipient checks original authorization, scope, and write gates under their own rules. Suggestions remain suggestions. Files, versions, acceptance, and publication belong to their actual owners.
- Clarify a missing target or scope. Report delivery, replies, and gaps. If capability is missing, supply a package the user can relay. Redispatch, extra sends, or periodic follow-up need corresponding authorization.

#### 2.4.3 Execution: Dispatch to a new session

- When the user explicitly specifies a new session, target workspace, and execution task, form the package under §2.4.2. Use it as the initial message. Report the actual entry or unfinished state.
- This permits only creating that session and delivering its task. Directory, repository, worktree, subagent, and external service privileges are separate. Do not substitute another execution unit for the requested new session.
- Report failure or a queued request as such. Do not claim a temporary ID is an active session, and do not create duplicates to conceal uncertainty.

#### 2.4.4 Multi-session execution

- Requires an explicit switch and real creation or dispatch capability. Name Manager, Generator, target workspaces, boundaries, and allowed execution units. Record actual sessions or agents and coordination state.
- Manager plans, assigns, reviews before committing, and handles authorized commits and backups. Generator implements only its scope, tests, fixes, and returns changes, checks, remaining work, and evidence. No role gains cross-workspace write access. Commits, backups, releases, and publication retain their gates.
- Only one session writes a workspace at a time. Transfer write ownership before takeover. Each workspace follows its own permission. Authorize new user sessions and subagents separately; neither substitutes for the other, and tool availability does not imply parallel work.
- Automatic dispatch, cross-session replies, redispatch, and necessary waits only operate within explicit coordination scope. Recipients verify original user authorization; reply requirements do not authorize sending. Other tasks, sessions, and new ongoing schedules are not automatically permitted.
- When no mechanism exists, keep the mode disabled and provide a manual task package. Do not invent dispatch or results. Switching to ordinary execution or manual dispatch stops automatic coordination. Close remaining tasks and execution units under user authorization.

Authority: this file §2.4 for permission. Review when communication or dispatch, target binding, authorization interface, or roles change. D:contract-spec governs contracts and their lifecycle; a contract does not authorize execution.
```

The §2.1 combination rules still apply. Reply plus Contact permits sending only approved non-execution content. Execution work still requires explicit dispatch. This module does not add root-only synchronization, batch governance for child workspaces, or contract overwrite exceptions.

### 4.3 Checks

Check actual adopted mode names, entries, and definitions, preserving manual dispatch and ordinary execution limits. Check actual D:contract-spec and D:index-spec entries, sizes, full spec membership, and authorized T:contract. Inherited modes keep their original definitions; they do not prove local installation. Authorize communication, new sessions, subagents, and cross-workspace writes separately. Installation is not evidence the tools ran.

Actual communication tests require a scoped authorization, target, original task, and reply boundary. Mark them untested otherwise. Do not message existing chats merely to test, and do not record relay text as delivered.

## 5. unattended

### 5.1 Two shared rules

Update the corresponding §1.5 rule and the ordinary discussion row in §2.1. Keep all other content:

```diff
-- Provide a complete draft for changes to governance files, handoff structure, specifications, and contracts. Show each HANDOFF change as a diff. Write only after the user reviews the draft and grants corresponding execution authorization. Filling fields, changing states, or recording facts under an approved charter and plan follows its explicit write permissions and still-valid authorization. Draft any new rule, requirement, scope, permission, exception, or version number. Do not ask again for explicit approvals already given.
+- Provide a complete draft for changes to governance files, handoff structure, specifications, and contracts. Show each HANDOFF change as a diff. Write only after the user reviews the draft and grants corresponding execution authorization. Filling fields, changing states, or recording facts under an approved charter and plan follows its explicit write permissions and still-valid authorization. Draft any new rule, requirement, scope, permission, exception, or version number. Do not ask again for explicit approvals already given. For approved unattended work, fact updates follow §2.6.1 and limited continuous-iteration handoff approval follows §2.6.2.
-| Ordinary discussion / Discussion: Topic | Reading, analysis, audit, and drafting in chat; no changes to files, directories, repositories, or external state |
+| Ordinary discussion / Discussion: Topic | Reading, analysis, audit, and drafting in chat; no changes to files, directories, repositories, or external state. Pause the task's heartbeat and report its result only as limited closure under §2.6.1; do not resume implementation |
```

### 5.2 Full execution section

Append after root §2.5 and before §3. Cross-workspace collaboration uses §2.4 subsections, so numbering does not conflict. Installing unattended alone does not need placeholders for cross-workspace subsections.

```markdown
### 2.6 Optional unattended execution

This section enters root rules after the compatible module is approved. Verify registration of the mode and actual module source. Installation does not start a task. Ordinary and optional modes have separate permissions. Resolve conflicting combinations and retain any no-commit or no-backup limits.

#### 2.6.1 Execution: Unattended

- Enable when the user directly invokes it and specifies version, scope, and completion conditions. If completion is unspecified, use ordinary execution without a heartbeat. Scope, rule, version, acceptance, and publication gates remain.
- For new tasks, ask once whether to use MVD preflight, recommending it. Reuse an explicit enable or skip. Do not repeat for resumes, version changes, or wakes. Stages, permission collection, one to five consolidated exchanges, and closure follow §2.2.
- On entering implementation, create or reuse one heartbeat for this thread and task, defaulting to five minutes unless the user specifies an interval. Before reuse, verify ownership and update scope, interval, and stop conditions. Do not duplicate it. Record ID, interval, and actual state in existing handoff or evidence.
- On waking, check latest user instructions and authority, continue in the existing started and dispatched state, and resume remaining writes sequentially. Do not restart or enlarge scope. Stay silent when unchanged; notify on completion, substantive failure, or a blocker requiring the user.
- At completion, cancellation, pause, return to discussion, or a blocker that prevents further work, pause this heartbeat and verify the result. Do not pause for an independent blocker while authorized work can proceed. After return to discussion only pause and reporting are allowed. Resuming needs explicit execution again.
- When the host provides Goals, keep one for this task and implement, verify, repair, and reverify. Completion requires clearing the remaining items. For unavailable or failed Goal or heartbeat creation, reuse, inspection, or pause, report state, gap, and impact and continue independent work. Do not claim start, pause, or successful automation. Do not start another thread, subagent, or external scheduler to work around it.
- For repairable blockers, use §2.6.3 only if retry extension was enabled. Otherwise record independent blockers and proceed with unaffected tasks before returning to them. For an unresolved linear blocker, preserve the state and stop that chain without waiting or polling. Record state, items, evidence, attempts, and resume conditions in handoff and report to the user. Follow actual host Goal states; never mark false completion.
- Within approved scope, update facts promptly: work state, test results and evidence, actual situation, blockers, and explicit user decisions. Draft rules, requirements, scope, permissions, exceptions, and unprovided versions before approval.
- By default, terminate or restart only this task's processes on ports listed explicitly in local rules. Do not touch outside ports or other sessions. Record actual termination or restart. Handle other port blockers as above.

#### 2.6.2 Execution: Unattended continuous iteration

- Enable when the user directly invokes the mode, names pending items, and gives the next version. Follow the user's added items, round count and contents, and interval. With a round count, stop at that scope and number; otherwise stop at the authorized list. Unless specified, completion means item self-checks, final audit, review copies, and deliverables are ready.
- Close remaining authorized current work to Pending review, then proceed with specified items at the assigned versions. Keep unaccepted versions unreleased. Do one item per round, then verify, repair, and verify again. On pass, make a path-limited development commit before the next item. Register only scope additions and handle blockers under §2.6.1.
- Under this authorization, use the existing HANDOFF structure to organize, write, and make development commits for work breakdown, pending user review, explicitly given next versions, and facts without waiting for each round's review. Draft new governance, requirements, scope, permissions, exceptions, or unspecified versions. A development commit grants no release, normal backup, or formal archive permission.
- Before changing versions keep a separate review copy under local T:audit, named <version>-<topic>/. Record fixed source, changes, and entry. Keep it independently readable and unchanged by ongoing work. If it needs to run, isolate the corresponding dependencies and build. Keep review copies and normal version backups separate.
- Current HANDOFF covers the version being worked on. Keep older details with their audit copies and list actual versions, state, and entries for user review. Do not pre-record acceptance, release, or archive. Keep one total Goal through version changes without wiping unfinished work; reuse the task heartbeat and ownership.
- When all authorized items and final audit pass, update pending reviews and handoff in a development commit, pause the heartbeat under §2.6.1, and give manual review entries, actions, pass conditions, and gaps in the user's version order.
- After the user confirms a version, clean its review-copy dependencies and build outputs. Keep source, lockfiles, findings, necessary evidence, and knowledge deliverables. Do not affect other copies.

#### 2.6.3 Execution: Retry extension (combinable)

- Enable when the user explicitly invokes this strategy with scope and completion conditions. It can combine with ordinary, unattended, or continuous execution. Without a mode use ordinary execution. It adds no scope, permission, or dispatch capability. It is unavailable until enabled.
- Count one failure for a targeted implementation or correction and matching failed recheck of a specific blocker, starting with the first. Findings, multiple errors in that round, repeated logs, and status repeats do not add attempts. Track independent problems separately. Do not reset an unresolved blocker on rename, split, new session, or different error.
- Default: three failures per blocker and two preauthorized extensions, adding three to the cumulative limit each time (3 → 6 → 9). Explicit user limits take precedence.
- At the limit preserve evidence and actual state. Spend an extension only when enough remain and there is a new correction and matching verification directed at the cause. Otherwise stop that chain and report cause, attempts, evidence, and resume conditions. Continue independent authorized work. If all remaining work depends on the blocker, preserve and report under the original mode rather than retrying mechanically. Extensions cannot clear missing rights, actual quota, or external prerequisites.
- Close that blocker's count when a matching recheck passes. Do not transfer counts. If it recurs, verify whether it is still the same unresolved blocker and retain the account if so.
- Record blocker, number of failures and extensions used, current limit, approach, and recheck result in existing handoff or evidence. Audits, periodic checks, and host blocked-state checks count separately from substantive attempts. Do not add audit rounds automatically. Existing verification and acceptance still apply.
```

### 5.3 Checks

Verify the two shared rules, three §2.6 modes, and references. Retain current core preflight interaction, reasoning recommendation timing, and ordinary execution limits. Do not replace the whole current root rules with an old file.

Installation does not create a Goal, heartbeat, continuous task, or failure account. Do not put task state in initial config. Record host capability separately from an actual test. Testing automatic start or stop requires a separate scoped task, completion conditions, and authorization. Untested capabilities are not passes.

Continuous iteration includes development commits. If combined with no Git, temporary execution, or an explicit no-commit task, explain the conflict and have the user decide a workable scope. Do not create a repository or omit commits silently. Review copies, normal backups, version release, and publication remain distinct.

## 6. Combinations, provenance, and deactivation

### 6.1 Combinations and order

Choose K, R, M, and the three modules separately. The modules have no mandatory dependencies on one another. Knowledge acquisition does not imply dispatch; unattended does not imply sending or multi-session coordination. Combined tasks include only explicit user permissions.

Verify governance direction, fixed material, and existing implementation first. Place selected originals, combine root and specification changes, and then update indexes, bytes, protection, and necessary tool config together. Order actual selected layers and modules by their dependencies without installing unselected items to complete an order.

If all three modules are selected, local D/spec contains the three core specs plus cache-spec and contract-spec, with continued numbering in the D index. K is still chosen for knowledge, not for placing specs in an external share. Combine overlapping changes once and verify core and module files, owning index sizes, complete directory membership, and active references. Retain data layers and inherited modes under their original ownership.

### 6.2 Source and completion records

After completing and verifying files and supporting changes, record actual source versions in `config.modules` and locate exact module originals in D:upstream under root §6. Keep existing adopted entries. This example shows source shape, not actual installation or formal publication:

```json
{
  "knowledge-acquisition": {"source_version": "0.1.0.0"},
  "cross-workspace": {"source_version": "0.1.0.0"},
  "unattended": {"source_version": "0.1.0.0"}
}
```

Record selected modules only. Do not substitute the core number for unknown sources. K, R, and M are not module entries. Installing a module alone does not change `fieldcase_version`. Maintain instance version, K version, consumer pin, and acceptance separately.

Initial module rules may be included in the approved charter and supporting files. Record actual adoption work, remaining work, capabilities, and evidence under current tasks and lifecycle, without an initialization completion flag. Discussion does not revert In development or start later work. Independent private governance maintenance follows existing root version and release rules.

### 6.3 Deactivate and recover

Before deactivation, check active rules, tasks, data references, and customization. Draft scope and recovery inventory; do not merely delete config. Pause unfinished unattended tasks within their original authority and verify their heartbeat. Retain unresolved contracts and unique evidence under the approved disposition rather than deleting on uninstall.

After removing specs, modes, and references from active use, apply the approved index and protection changes. Update the module entry in config and its current D:upstream pointer. Keep needed originals, migration sources, recovery sources, and history. Adoption direction follows root §1.6. Knowledge, materials, and contracts still in use must retain an entry. Obtain a decision to keep their required model or migrate them first.

For failure, follow the guide for targeted repair or recovery. Check additions, edits, removals, moves, sources, and indexes together. Do not overwrite the whole instance. Return to discussion on a scope or permission conflict and state actual facts and remaining work.

## 7. What to record

Distinguish text review, static source/membership/size/reference checks, actual installation, host capability, and user acceptance. Keep the minimum below in existing handoff or evidence rather than creating a permanent log:

| Object | Actual scope and fixed source | Checks and result | Untested or blocked | Next step or evidence |
|---|---|---|---|---|

Do not mark unperformed work as passed or invent commits, sending, replies, Goals, or heartbeats. External versions, official sources, both language packs, and public publication follow their actual completion and authorization.
