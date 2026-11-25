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

# Current handoff

> This is a pack template for user approval and completion. Empty identity, root, and version fields do not denote an active workspace. The status shows Ready to start, the initial state of an approved charter. Discussion and drafting stay in chat; template wording does not start work.
> Confirm the target version when approving the charter. The first version is normally 0.1.0.0 and is separate from the official core source in config. The actual setup uses that same target version without a separate initialization version.

## 1. Version task overview

| # | Version | Topic | Source | Status | Priority | Dependencies and limits |
|---|---|---|---|---|---|---|
| 1 | Pending; suggested first version 0.1.0.0 | Set up the workspace and required capabilities | Root rules and D:agent-guide | 💡 Pending decision | P1 | Confirm the adoption route, governance, source and target, components, target version, and charter in chat. Authorized charter writing establishes Ready to start. Beginning authorized concrete work changes it to In development. Acceptance and version release are separate |

## 2. Current work items

`ini` denotes an initial setup item. Keep its identity across handoffs; it does not denote a lifecycle stage. Record answers, charter writing, concrete work, and acceptance separately. Break down the current work as planned without inventing every work item in advance.

| # | Stable ID | Item | Status | Dependencies and limits |
|---|---|---|---|---|
| 1 | ini-01-setup | Plan and set up the first version | 💡 Pending decision | This is an unapproved template. Confirm charter, document, and work scope first. No directory creation, file writes, repository creation, or commit without authorization. Record preparation, progress, and blockers against the actual work |

## 3. Handoff snapshot

### 3.1 A. Current state

- Workspace name, actual root, and root maintainer are pending user confirmation. Do not infer authority from the pack name, path, or session directory.
- Charter and work: This is only a pack template. No user-approved target or valid authority for work is recorded. The charter first enters Ready to start; actual work enters In development. Record Released only after meeting the version release conditions. There is no `initialized` field. The source state does not establish results in the target.
- Documents and data: Root plus D and T is the minimum. Missing K/R/M entries in the pack do not mean the user selected it. D holds the local rules; create, import, or share data layers as needed. Establish entries and ownership after the plan is approved.
- Git and branches: Not selected or established. A Git repository found in an ancestor is not this instance's repository. Do not record any branch or tag as existing before verifying Git here.
- Use configuration for core and adopted module versions. After enabling resources, locate their exact originals from the actual adoption entry in D:upstream. Locate inactive resources and compatibility information through the actual distribution cache.
- K/R/M dependencies are not selected. When adopted, use one row for each layer and record the fixed source. D has no layer version or content pin; read the rules approved for the instance. Record the recovery plan against current work. Locate real file snapshots through D:backups. Distinguish a workspace with no repository from a source with no Git.
- Services, ports, backup, history, and public entries: Nothing is confirmed for this instance. Do not mark an unstarted or unverified object as usable.

| Layer | Adoption mode | Content version | Fixed source |
|---|---|---|---|

For a candidate trial, add the applicable layer or stable IDs and the preceding formal dependency here. Do not prefill an example commit or invent a release tag in the pack template.

### 3.2 B. Environment and tool pitfalls

There are no pitfalls observed in this instance yet. After observing a reproducible issue, record the condition for action here under D:handoff-spec and index necessary evidence at its actual location. Do not create an empty appendix.

### 3.3 C. Decisions

There are no decisions from this instance's user. Use the actual answers and final approved plan for language, adoption route, governance, root authority, layers, paths, Git, branch, consumption, and modules. Defaults and preselected options have not been submitted.

### 3.4 D. Awaiting user direction

| Order | Confirmation or authorization needed | Purpose |
|---|---|---|
| 1 | Confirm language, adoption route, governance, identity, and components using the guide | Complete the plan and reuse confirmed choices. Do not infer autonomy from old rules or preserved originals |
| 2 | Address missing resources, configuration, capabilities, old directories, or other actual gaps | No guesses about sources, automatic switches, or silent removal of choices |
| 3 | Approve the charter and plan and define what may be written | Check the target version, lifecycle, supporting files, and parent dependencies. Writing the charter establishes Ready to start; it does not authorize Git or environment setup |
| 4 | Authorize the concrete work and its scope | Environment, dependencies, copying, governance checks, and selected Git work start In development. Continue on explicit authorization already covering the same scope. Do not start other work or publication |

### 3.5 E. Requirements for the current version

Goal: Build a workspace that future sessions can continue from its files, within the user's approved goal. Write the charter and necessary files under document authorization for Ready to start. When setup or copying actually starts, enter In development. Migration follows copy, governance alignment, then local repository creation at the target. If the user chooses no Git, retain that boundary. Finishing a stage does not release the version or revert to Ready to start.

Currently limited to identifying, reading, and discussing. There is no approved complete plan or execution instruction yet. When obtained, record its source, scope, and remaining work here. Do not rely on “approved” alone.

| Scope | Completion conditions |
|---|---|
| Identity and language | Verify source, target, name, and maintainer. Confirm and fix `locale` through the first language question |
| Governance adoption | Record `governance_adoption`. Direction 1 fully applies fieldcase. Direction 2 preserves private originals and adoption records and applies the approved local governance |
| Copy migration | Preserve the source, keep a complete inventory, and verify unchanged copies and adaptations separately. After alignment, initialize Git locally in the target if chosen; the source's Git and an ancestor repository do not count. Moving the source requires an explicit user request |
| Files and entries | Root plus D and T and the selected data layers are present for the approved scope. Protect the three D core specs and the full spec directory. K is optional for knowledge purposes. Check shared protocols, ownership, real links, complete membership, and bytes separately |
| Configuration and sources | Full JSON, correct types and values, matching core source and root display. After adoption, D:upstream locates the exact originals for core and adopted modules. Record verified `shared_layer` and `root_governance` if applicable parent rules require them |
| Git, if enabled | Treat this as concrete work in In development. At this workspace's new repository, use the approved common starting commit and same-version development branch under D:handoff-spec#branch. For migration, copy and align before creating the approved target repository. Keep shared repositories intact |
| No Git | Verify actual files and results against the current inventory; record no repository or commits and limits on historical recovery. No Git is not a failure or a capability the workspace can claim |
| Resume | Keep work that matches the approved plan. Do only what remains, obtain valid authority after a pause, and do not recreate repositories or commits |
| Close | Record completed work and gaps from actual files, selected commits, and the acceptance list. Once concrete work starts, it remains In development even in discussion. Record Released only after meeting the actual acceptance and version release conditions |

Record progress, remaining work, and blockers when implementing. Do not duplicate existing authoritative values. The charter being in place, concrete work completing, user acceptance, version release, and public publication are distinct facts. No single status or marker replaces proof.

### 3.6 F. Later versions

No business version is approved. Set scope and authorization separately when the user raises further migration, development, or upgrades outside first adoption. Describing a capability does not start it.

## 4. Hard rules

Use the root rules for identity, authorization, work modes, and configuration permissions; D:index-spec for indexing and protection; and D:handoff-spec for lifecycle, items, versions, size notices, and where to record information. Keep only the criteria and references needed for current action here. Avoid a second set of rules. For history see D:handoff-spec#hist, for deferred entries and pitfalls see D:handoff-spec#pending-pit, and for design guidance and its maintenance see D:design-spec. Establish files as authorized.

## 5. Coverage and version release

There are no verified commits, released versions, backups, or publications for this instance. The charter's target version, first common starting commit, and development commits are not version releases. User acceptance, version release, and public publication are separate. Report only verified actions.

## 6. History index

There is no history yet and `history` stays null. Create the needed overview, index, and volume when archiving an actual stage or recording an actual version completion under D:handoff-spec. Register the reachable entry in the D index. Do not create empty history, deferred work, or pitfalls files.
