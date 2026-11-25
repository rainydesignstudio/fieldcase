---
id: agent-guide
updated: "2026-11-25"
recheck: Changes to governance adoption, setup or copy migration, shared access, questions, pacing, answer carrier, design work, resource layout, Git, modules, upgrades, or recovery
---

# Agent Guide

## 1. Where to start

From the docs entry in root INDEX, use `agent-guide` in D. Root governance defines identity, modes, and authorization. D:index-spec defines indexing and protection. D:handoff-spec defines states, work, versions, and history. D:design-spec defines design guidance and maintenance. The guide explains operations without replacing those authorities.

Confirm what the user actually opened and the fixed fieldcase resource root. Read its rules, INDEX, config, and HANDOFF. A migration source may be a non-fieldcase workspace with none of these fields. Check it separately from target adoption. Do not use an unset root to find a pack or assume the target's facts from an ancestor repository, a source marker, or an example identity.

This guide accompanies the English resource pack. Use §1.1 to distinguish review from trial. “Pack README” means the README.md in the fixed resources; it describes the materials and test scope. Before charter adoption, use the selected resource root. Afterwards, find the actual same-language original and precise version or batch through D:upstream. The instance root README is the local entry in §5.2.2. Report a missing original or cited section.

For a fresh setup, place fixed materials in the authorized target. For an existing workspace, §7.1 normally recommends copying, aligning governance, then creating Git locally in the target if chosen. Preserve the source. Choose governance direction explicitly on either route and check shared adoption under D:index-spec#paths. The target may already contain current resources and authorized copies from this task. Do not overwrite the source or infer autonomy from its old rules.

### 1.1 Distinguish the situation

Use the table to determine the task. Starting with the pack README, a target and a small goal is sufficient for first adoption. For explicit review or chat-only drafting, do the requested work. A chat-only trial may include questions and a plan. Clarify only unclear intent. Candidate files, examples, and paths do not grant authority.

When given the pack README, locate materials from its path and use their indexes. Verify the explicitly named target separately. Distinguish session working directory, material root, and workspace target. A nonexistent target is normal for first use. Report bad config, protection, or live files under root rules rather than treating them as an empty target.

| Verified situation | Responsibility and next step |
|---|---|
| Target absent, empty, or containing only candidate materials or inactive templates; no approved plan to resume | Guide first adoption with the actual clarification below. Add the small goal to the work plan |
| Approved plan with writing or setup interrupted in this task | Read plan, actual files, and handoff. Verify remaining steps and authority under §7, then resume only what remains |
| Active charter and no concrete work | Ready to start. Take current items and confirmed scope from target handoff and check execution authority |
| Concrete work for this version has started | In development. Check results and remaining work against target handoff, plan, and files. Verify authority under §7 or §8 before continuing |
| Current version actually released | Keep Released until an approved next charter takes effect and work is not started. Do not rerun first-use questions |
| Old workspace or copies already made in this authorized task | Use [11] and §7.1 to distinguish source, target, and completed steps. Do not overwrite the source or create an empty base repository first |
| Identity, root, config, source, or files do not agree | Report the gap. Do not infer completion, rebuilding, or autonomy from missing fields, old `initialized`, or an ancestor repository |

When choices are reliably confirmed, identify the case here. Verify answers and inventory against the same fixed source. Plan from the selected §2.2 profile and §4. Read and ask only unresolved applicable questions. Use §5.1, §5.2 and §5.4 for the charter, §5.3 for Git and §7.1 for migration when applicable. Consult distribution support only for selected layers and modules.

Apply root §1.3 before reading protected text. For tool checks of the inventory, byte counts, membership and fixed sources, return only the scope, results and discrepancies. Reuse complete, unchanged passages from the same source when drafting, writing or checking. If output is truncated, retrieve only the missing text from that source. Each triggered full reread follows root §1.4.

Verify the entry and target for first adoption. When required questions remain, start clarification in the first substantive reply. Before sending an unconfirmed language question [1], actually read §2.5 of AGENTS.md in the pack's own root, then follow §2.1 and §3.1. Reuse reliable answers and ask only the first unresolved required item. A process summary or task draft cannot replace the question.

After sending [1], follow pack AGENTS.md §2.5 for waiting for a real answer, retry and text fallback. Until fallback applies, text about the question only records that it is sent and awaiting an answer.

Present the plan and charter in chat under §4, with the small goal, files and pass conditions. The user must approve both and authorize execution before directory creation, copying or writing under §5.2. Document-only authority stops at Ready to start. Start the task only within existing authority. First-use guidance does not assign root maintenance.

Complete local materials support offline setup. Check actual host read and write access and chosen Git capability under root §1.5. Keep the initial preparation in chat, without adding a lifecycle state.

## 2. Clarification and quick presets

### 2.1 Shared rules

- Language is the first required clarification. The pack or system language indicates a resource or recommendation, not the user's answer.
- Reuse confirmed answers that can be recovered reliably. Do not repeat items covered by an accepted complete preset. A preselected default is not submission.
- Offer all defaults or expanding each group. State all its defaults in one sentence first. Confirm setup or migration separately from governance direction, and reuse an explicit decision. Do not answer from a preset, old customization, or retained originals. Present choices under root rules §2.5.
- For the default carrier, follow root rules §2.5 for sending, display, answer return, and text fallback. Use §2.3 for test carriers. Ask only for required module parameters described in actual module instructions.
- Do not create directories while clarifying. After the full plan is approved and execution is explicit, preserve originals, copy authorized content, and implement. Complete governance alignment before creating the target repository in migration.
- The user explicitly designates the root maintainer under root rules §1.1. Use §3.6 to verify who will take the role and propose the setup session title.

### 2.2 Three pacing options

| Method | Use |
|---|---|
| Guided groups, default | Confirm the following groups in order. Use all presented defaults or expand each group |
| Standard quick | Show and confirm the complete standard preset. Fill missing language, route, governance, name and identity, commit identity, conflicts, and permission |
| All-modules quick | Show the complete compatible preset for the same release and the actual module list. Do not omit missing material or unknown dependencies silently |

Standard preset: professional with local D and K/R/M/T. Confirm the adoption route first and use §3.2 to recommend the project area. The other local defaults are docs, knowledge, references, materials, and temp. Local Git. Confirm actual repository roots and tracking scope in the plan. Maintain D in this workspace. Branch development; standard explanations, table review, and shared development consumption. Always protect the three D core specs and directory, derive data protection from actual governance and specs, enable enforcement, and use `ask` for restoration prompts. No additional protected objects. Core and selected-layer rules only, without the three modules or project skills. Confirm language, root maintainer, actual name and paths, and any missing author identity.

Those local layer paths are defaults for an independent new instance, not answers for governance or migration. For shared parent layers, describe entry, permission, protocol, and repository differences per layer. Migration still follows copy, align, then Git at the target. Do not impose an incompatible preset.

All-modules quick adds compatible knowledge acquisition, collaboration, unattended work, and any actual supplied project wrappers. Present each actual module, dependency, and supporting change. Do not claim that missing skills or undownloaded material is present. Check compatible sources for each of the three modules separately.

Presets reduce questions only. Keep source checks, full plan, execution permission, and final verification. If the user does not adopt a preset, use guided groups. Handle a conflict such as no Git or direct main in its group rather than assembling a plan that cannot run.

In the README §1.1 minimal route, use guided groups and confirm [4] Minimal, [7] No Git and [9] Core plus selected-layer rules. Reuse explicit decisions and skip inactive layer and Git questions. Verify language, maintainer, source, target root, version, inventory and authority under §4.

### 2.3 Optional answer carriers

Carrier is where answers are entered; pacing is whether to confirm in groups or select a preset. Choose them separately. For the default carrier and text fallback, follow root rules §2.5. Ask original language [1] first and only then optionally offer a test carrier. Skipping it keeps the default. Use the same active question IDs, options, and meanings across carriers. Retain all 30 original IDs, with [7.1] reserved for earlier answer sheets. For an earlier answer sheet, check its source version or batch and user intent. Do not infer that former “minimal K + T” now removes K. Reconcile in the full plan without adding numbers or clearing choices silently.

| Carrier | Conditions and return of answers |
|---|---|
| Clarification tool or text, default | Follow root rules §2.5 for display, retry, and text fallback. Keep existing questions and presets and verify actual answers |
| Codex Visualize, test | Verify actual session capability. Have the user submit and confirm if the host requires it. Validate the complete answers once they actually arrive in this session |
| HTML in other harnesses, test | Verify it can display a page. Use an actual message bridge if supported, or let the user copy or save JSON and return it. Do not assume all hosts bridge |

Copy and saved JSON use the same answer set, IDs, and semantics. Use string keys for [3.1] and [3.2]. Return the K/R/M selections with [4] option 3. Keep separate answers for [9.1]–[9.4] under their existing IDs. When the user accepts the listed paths in [5] or the recommended path in [5.1], retain the actual project-area path with the answer. Interpret older path choices using their fixed source and the options shown at the time. Follow up only if the path cannot be recovered. Ask about required selections missing in older carriers rather than guessing. Actual submission is required even for defaults. UI presets and saved widget state are not answers. A download or success display is not evidence the agent received it.

After a message or explicitly identified result file arrives, verify question IDs, option bounds, necessary free values, and that it matches the actual submission. Combine questions for missing values, invalid JSON, unknown questions, or conflicts. Do not guess or write config. Repeated identical input does not repeat execution. If inputs differ, verify the latest explicit user submission.

Receiving answers, approving the full plan, and authorizing execution are separate. Ordinary answers do not initialize anything. Treat an actual explicitly selected [12] execution option under the original rules only after showing the complete plan and verifying the intent to authorize within that workflow. UI presets, test fixtures, or generated fields such as `authorized=true` do not replace the answer.

Selecting a test carrier does not authorize creating UI files, starting a service, or sending elsewhere. Candidate rules and a minimal test plan do not prove production readiness. Use the default if capability is unavailable. If a test is blocked, preserve the agreed candidate direction, explain the impact, and consolidate the decision on keeping or deferring it. Do not remove it independently.

## 3. Complete initialization questions

### 3.1 Language, method, and workspace

```text
[1] Which language should the workspace use from setup onward?
1. Chinese (zh-CN)
2. English (en-US)
Note: Recommend from available environment signals, but the user confirms. There is no routine language switch after setup.
```

```text
[2] How should the agent guide setup?
1. Guided groups (default): use all defaults or expand each group
2. Standard quick: confirm the full standard preset for the agent to apply
3. All-modules quick: confirm the complete same-version preset and compatible modules for the agent to apply
Note: All three are guided by the agent and executed with permission. Quick modes reduce repeated questions, not authorization or verification.
```

```text
[3] What is the workspace name?
1. Use the current directory name (suggested default)
2. Enter a name
Note: Show the detected absolute root as well. The workspace name need not match the folder name.
```

```text
[3.1] How will this workspace be established?
1. Start from scratch
2. Copy from an existing workspace
Note: Verify source and independent target first. Normally copy, align governance, then create Git in the target as applicable. Preserve the source. For an explicit required move, separately state source disposition and recovery scope.
```

```text
[3.2] Which governance direction should apply?
1. Follow fieldcase governance in full
2. Keep private adopted originals and implement local governance in part or in full
Note: Do not choose a default for the user. Reuse an explicit choice. Keeping originals does not authorize autonomy. Direction 1 retains all management requirements; direction 2 defines adoption scope, implementation, and maintainer.
```

If the selected language resource is absent, do not only change `locale`. Use question 10 to check the complete resource. Record the name and root only in HANDOFF and verify user-designated root authority separately.

### 3.2 Layers and paths

When presenting the [4] layout question for the first time or after the user returns to change their choice, follow root rules §2.5. Explain the layer names, their uses, and what each layout includes in the conversation before showing the original question and choices. Give the same explanation before offering the equivalent text menu. Keep the wording concise while giving a first-time user enough information to choose.

| Layer | What it is for |
|---|---|
| D (Docs) | Workspace documents and current specifications. Maintain it with the root, without a separate repository or layer version. |
| T (Temp) | Caches, material awaiting placement, intermediate work products, audit evidence, and backups. Follow the active T index. |
| K (Knowledge) | Build and search a reusable knowledge base. Use a local library, an existing shared library, or an approved import as needed. |
| R (References) | Reference material, snapshots, and evidence to consult when checking facts. |
| M (Materials) | Drafts, templates, and assets that you store and maintain while producing work. |

The root files, D, and T are the foundation for all three layouts. Professional adds K, R, and M. Minimal uses the foundation alone. Custom lets you decide whether to add each of K, R, and M. Include the selected layer entries in the plan and confirm their actual sources and paths later. Adopting data layers does not create new agents.

```text
[4] Which documentation and data layout?
1. Professional (default): use local D along with K, R, M, and T, with entries for all three data layers.
2. Minimal: use only the root files, D, and T, without K, R, or M for now.
3. Custom: keep D and T and select whether to adopt each of K, R, and M.
```

For [4] option 3, explain what each available layer does under root rules §2.5. If the clarification tool accepts one answer per question, use the table to ask a separate Adopt / Do not adopt question for each available layer in the same group, so the user can submit the answers together.

| Question and effect | Adopt | Do not adopt |
|---|---|---|
| [4] Adopt K, the knowledge base? This adds an entry for searchable knowledge. Set up a local library, reuse an actual shared library, or import an approved inventory. | Adopt K | Do not adopt K |
| [4] Adopt R, references and evidence? This adds an entry for references and evidence within the registered scope. | Adopt R | Do not adopt R |
| [4] Adopt M, production materials? This adds an entry for storing, maintaining, and using production materials. | Adopt M | Do not adopt M |

Before sending these single-choice questions, check that the tool request passes each row's two answers as separate options (the `options` field in Codex). Add any missing options before sending; do not ask the user to type the layer names. Follow root rules §2.5 for retries and text fallback when a question does not appear. If the user explicitly chooses a test carrier, follow §2.3.

Once all answers arrive, record them under [4] option 3 without adding question IDs. An unselected layer is left out of this adoption; existing content is kept. Record none only when the user submits Do not adopt for every offered layer. Follow up only on unanswered items.

After confirming the adoption route, establish both the projects the workspace will hold and their governance boundaries before proposing paths in [5] or a quick preset. Reuse confirmed paths and child-workspace arrangements. For migration, check actual entries and dependencies and list any path or ownership changes in the plan. Ask only when missing information affects layout or maintenance.

| Confirmed use | Suggested project area |
|---|---|
| One project maintained in this workspace | Recommend `project/` and put the work files directly in it. This workspace manages its own rules and handoff. |
| Several projects maintained together | Recommend `projects/`, with a directory for each project and shared workspace governance and handoff. |
| A project requires independent maintenance, authorization, or handoff | Set up a child workspace within the project area as needed. Confirm its maintainer, duties, and handoff scope under the applicable rules. |

Determine which parent rules apply from the actual workspace affiliation and reread the active specifications. Verify ownership of T under [5.6]. When reusing a parent's T, point the local T entry to the actual shared index and put temporary artifacts within the authorized allocation.

```text
[5] Use default directories or set them individually?
1. Use all defaults
2. Expand 5.1–5.6
Note: First show the recommended or confirmed project-area path and the actual defaults or shared entries for each selected layer. Option 1 uses the paths shown for this question. The local layer defaults are docs/, knowledge/, references/, materials/, and temp/. New local paths stay in the approved root. Reuse an existing parent share through the shared adoption rules and leave its root under its current owner.
```

```text
[5.1] Where should work projects go?
1. Use <actual recommended project-area path>
2. Enter a root-relative path
Note: Ask only when expanding the path group and the project-area path is unconfirmed. Show the actual path in option 1, for example project/.
```

```text
[5.2] Where should documentation go?
1. docs/ (default)
2. Enter a root-relative path
Note: Local specs use the spec subdirectory of D. D is not outsourced as a shared layer. The D index locates the guide, originals, history, and actual recovery snapshots; no duplicate path config.
```

```text
[5.3] Where should knowledge layer K go?
1. knowledge/ (default)
2. Enter a root-relative path
3. Reuse a parent share and verify its index, ownership, and approval scope
Note: Ask only if K is selected and paths are expanded. Do not pre-create an empty unselected layer. Import approved library files with their structure where appropriate. Retain actual entry and protocol without editing the shared source.
```

```text
[5.4] Where should reference layer R go?
1. references/ (default)
2. Enter a root-relative path
3. Reuse a parent share and verify its index, ownership, and approval scope
Note: Ask only if R is selected and paths are expanded.
```

```text
[5.5] Where should materials layer M go?
1. materials/ (default)
2. Enter a root-relative path
3. Reuse a parent share and verify its index, ownership, and approval scope
Note: Ask only if M is selected and paths are expanded.
```

```text
[5.6] Where should temporary layer T go?
1. temp/ (default)
2. Enter a root-relative path
3. Reuse a parent share and verify its index, ownership, and approval scope
Note: Temporary artifacts are not tracked in the base repository. T's overall INDEX is a governance file.
```

When there is content to organize, offer a category suggestion under D:index-spec#local. For example, images in M can go under `media/images/` and be grouped further by use as needed. Let the workspace user choose the names and depth that suit their work.

Summarize actual local and reused entries, maintainers, and applicable rules. In the root INDEX, point `projects` to the confirmed project-area path and register the approved entry for each layer. Create only under the root or a specifically authorized shared owner path. Verify actual shared objects and fixed sources under D:index-spec#paths. Providers own their indexes. Direction 1 uses local D and root governance. Record impact and conditions to resume for missing keys, permissions, or sources; handle parent-rule conflicts under root §1.6.

### 3.3 Configuration preferences and protection

```text
[6] Use all configuration defaults or adjust them individually?
1. Use all defaults
2. Expand 6.1–6.3
Note: Defaults are standard explanations, tables for manual review, enforced checks, and restore prompt ask. Always check D core and its entire specification directory. Data protection covers actual adopted governance, specs, and directories only. It may be empty with no data layers. Do not add extra objects by default.
```

```text
[6.1] Which explanation style should Help use?
1. Standard (default)
2. Plain language
Note: This changes expression only. All needed modes and permission limits still apply.
```

```text
[6.2] Which layout should manual review use?
1. Table (default)
2. List
Note: Item numbers, order, entries, actions, pass conditions, and gaps remain.
```

```text
[6.3] What else should be protected?
1. Keep the default scope without additions
2. Enter additional directories, files, or name patterns
Note: Register and resolve them through the indexes. Do not drop required objects to bypass protection.
```

Disabling enforcement and `never-ask` are root repair settings, not casual setup toggles. Record only the actual selected layers; do not mark missing R/M as enabled. Do not store another `paths` map.

### 3.4 Git, repositories, branches, and author identity

```text
[7] Enable local Git for this setup?
1. Enable local Git
2. Do not enable it now
Note: Without Git, skip Git-specific branch and author questions. There is no GitHub login requirement.
```

[7.1] is reserved for the previous repository layout question. Interpret earlier answers using their original batch. Verify actual repository roots, tracking scope, and Git actions against the approved plan.

```text
[7.2] Which branch method?
1. Branch development (default): dev for development, pre for preview, close as authorized
2. Direct main without a second branch or a fast-forward step
3. Provide branch names, purposes, and closure rules
Note: Convert custom descriptions into explicit rules. Create branches only for approved work. First setup uses the same target number as the first version, not a separate initialization version. Include Git work in the authorization.
```

```text
[7.3] What author identity should local commits use?
1. Reuse suitable detected identity
2. Choose or enter a local pseudonym and email-shaped address
3. Enter the author details
Note: Ask only when missing or when a change is needed. Change repository-level config by default. Quick modes do not invent an unapproved anonymous preset.
```

A pseudonym and email-shaped address are local commit metadata, not account authentication. The address need not receive mail. Do not infer a real identity from a name. Show any proposed values before selection or retain a free-entry field if there is no approved preset.

When checking Git, verify the actual repository root. An old or ancestor repository does not count. Choosing no Git does not install it, configure an author, or invent commits.

### 3.5 Consumption and modules

```text
[8] How should data layers consume updates by default?
1. Shared development (default): use approved committed development contents
2. Formal consumption: use a formal version by default, with development worktrees in T
Note: Check the chosen Git and branch capability. Do not claim branch isolation without it; send conflicts back to the relevant question.
```

```text
[9] Which optional module set?
1. Core plus required rules of selected layers only (standard default): add no optional modules or project skills in this adoption.
2. All compatible built-in modules at the same version: install the compatible built-in modules actually supplied in the fixed resources.
3. Expand 9.1–9.4: decide which to install, asking only applicable questions.
Note: Before the user selects all, explain each actual module, its purpose, and its limits. Handle missing materials under [10].
```

For [9] option 3, group the applicable questions from [9.1]–[9.3] and offer a choice for each under root rules §2.5. If using a multi-select control, first explain that leaving an item unchecked means Not now. After the full group is submitted, record option 2 for selected items and option 1 for displayed items left unchecked, under each original question. Leave outstanding items unconfirmed if the submission is missing or incomplete. Ask [9.4] only if a selected module has a compatible wrapper available.

```text
[9.1] Install knowledge acquisition?
1. Not now (standard preset): do not adopt the knowledge acquisition rules in this setup.
2. Install: add rules for acquisition, conversion, indexing, and optional verification. Formal knowledge output also needs an approved K target.
Note: No business library is included, and installing the module does not start acquisition.
```

```text
[9.2] Install cross-workspace collaboration?
1. Not now (standard preset): do not adopt the collaboration rules in this setup.
2. Install: add contracts, contact, and dispatch rules. Sending or dispatching still requires explicit authorization.
```

```text
[9.3] Install unattended work?
1. Not now (standard preset): do not adopt the unattended work rules in this setup.
2. Install: add rules for unattended work, continuous iteration, and pending-review closure. This does not start work or create recurring tasks. Without Git, continuous iteration that requires commits is unavailable.
```

```text
[9.4] Install project skills for the selected modules?
1. Not now (standard preset): keep the selected modules' rules without adding wrappers.
2. Install compatible wrappers supplied by this release: use them only in this instance, with the same specifications and no required global installation of external skills.
```

Without a local repository, do not claim local commits. Use a reliable commit or fixed copy at an external source if it exists; otherwise state actual guarantees. Stable formal directories and development worktrees in T require Git, common history, branch support, and authorization from the owner. The user can revise the Git or branch selection or explicitly approve a limited local approach. Do not combine incompatible choices in an executable plan.

### 3.6 Missing resources, old workspaces, and final authorization

```text
[10] A selected language or module is missing locally. May the agent obtain it online?
1. Allow retrieval of the listed compatible release materials
2. Choose an available option or a complete local pack
3. Defer setup
Note: Ask only for a real resource gap. Show source version, exact materials, and supporting requirements first. Do not silently choose the latest or drop a selection.
```

```text
[11] An old workspace or ambiguous setup was found. What should happen?
1. Confirm source and independent target and draft a copy migration
2. Preserve the state and pause for inspection
Note: Ask when the old material's purpose is unclear. If copying is confirmed, continue the approved [3.1] and §7.1 path rather than requiring a new empty directory. On interruption resume what remains. An explicitly required move needs separate verification of source disposition.
```

Confirm the root maintainer before presenting the full plan for [12], then confirm the target version. Reuse an existing explicit designation.

Explain the responsibilities before asking. The user sets goals, approves rules and results, and authorizes work. The root maintainer drafts and checks changes, then maintains the root rules and handoff when authorized.

Use the confirmed workspace name to propose a title for the setup session in the form `<workspace name> · <role>`. The setup agent chooses a role phrase that describes its actual duties, such as `demo-work · Root Maintenance` or `demo-work · Setup Guide`. Show the verified current title or a way to identify the session, together with the proposed title. If the host does not expose the title, identify the specific setup session in the message and show the proposed title. Use the same identification in the choice card and explain the duties for each option.

```text
Who will maintain the root of <workspace name>?
1. Current setup agent (<identifiable session title or reference>) (recommended) | Drafts, checks, and maintains the rules and handoff with user authorization
2. The user | Takes on ongoing governance maintenance
3. Another person or agent | The person or agent you designate takes on maintenance
```

Recommend option 1 when the current setup agent can continue as maintainer. List other known candidates by name. Ask for a name and any necessary reference only for a candidate outside that list. Use explicit names or roles in the options and record the user's actual choice. If another maintainer is designated, title the current session for its setup duties.

```text
[12] Is the complete plan accurate, and is this adoption authorized for execution?
1. Execution: Complete adoption under the stated route and inventory
2. Revise specified options
3. Do not execute now
Note: Show source, language, adoption route, governance direction, source and target, copy scope, layers, paths, configuration, modules, target version, draft charter, Git order and first commit, exceptions, and pass conditions. State whether documents alone or concrete work are authorized. Do not request complete permission already given.
```

Report resources as ready only after selecting resources actually present or obtaining what is missing. Report unverified official entries, versions, and compatibility. Do not assemble from a moving branch or edit a version field to conceal the gap.

## 4. Full plan and before implementation

The final plan includes at least:

| Item | Verifiable content |
|---|---|
| Source | The pack batch and language from the pack README, its fixed inventory, and the exact originals, versions, scope, and compatibility of the core and each selected module. Verify supporting material sources separately in the distribution index |
| Identity and root | The user-designated maintainer and a way to verify their identity, the confirmed workspace name, actual source and target roots, current session directory, and proposed session title. Use the actual target root |
| Route and governance | Setup or copy migration, governance_adoption, and full active governance. Direction 1 implements fieldcase at the target; direction 2 names the autonomous implementation and adoption record |
| Shared adoption, if selected | Real external dependencies and entries, fixed sources, maintainer, and protection. List applicable parent rules, unresolved conflicts, responsible parties, and resume conditions |
| Migration | Source inventory and fixed basis, copy batch, retained originals, path adaptations, recovery, and source preservation. Copy and align before Git at the target |
| Components | Actual layers, modules, and wrappers; unselected material remains inactive |
| Files and directories | The confirmed project-area path, actual child-workspace boundaries and who maintains each project, every actual target and moved or generated object, owning INDEX, retained original scope, and necessary tool settings |
| Instance specifications | The actual entries, directory, bytes, and complete membership of D's three core specs and selected module specs. D has no separate repository or version; data layers retain ownership |
| Configuration | locale, governance_adoption, protection, consumption, help, and review preferences; no duplicate authorities |
| Current work | Approved target version, lifecycle and tasks; values and sources for applicable parent dependencies, with unconfirmed applicability as a gap |
| Git | Enablement, actual roots, author, common starting commit scope, and same-version development branch. First creation is concrete work; do not reset existing Git. For a required fixed tag, specify the actual object and authorization |
| Exceptions and risks | Missing resources, conflicts, capability limits, decisions not yet implemented, and recovery scope |
| Completion | Write charter and support for Ready to start. Starting work enters In development, with checks and closure against the actual inventory. Stage completion, discussion, and version release are distinct |

Check JSON duplicate keys, types, adoption direction, and source display first. Verify protection using INDEX and file lists from the same source. Under D:index-spec#paths verify local and actual external dependencies separately. Required modules and supporting files must be available. Keep affected work blocked under root §1.6 while shared or parent-applicability gaps remain.

An unapproved plan stays in discussion; temporary or private directories do not bypass approval. The same explicit complete authorization can include subdirectories and files without repeated requests. Return for a decision when scope, permission, or plan changes.

## 5. First charter and setup

### 5.1 Retain adopted originals

D:upstream points to actual adopted or comparison originals, by default at `docs/upstream/fieldcase/<exact-version-or-candidate>/`. The D index records the real entry, language, and scope. Obtain the necessary files from a fixed source and preserve pack-relative structure. Do not write user customizations back to originals or copy upstream repository history for this.

Retain unmodified originals before changing working files. Save the core, selected modules, and needed INDEX or ADOPTION support for comparison. Distinguish source archives, official user packs, and unpublished candidates. Do not assemble from floating main or latest. For an unpublished candidate, explicitly approve the trial and use a fixed complete inventory and unique batch. Same-numbered content does not overwrite earlier originals or justify inventing a release tag.

Use §1 of the pack README at the same fixed resource root for the pack batch and language. Check them against any supplied fixed inventory. If you only have extracted files, record the batch using that README and the actual file inventory, and keep both with the originals. The distribution index identifies supporting material sources only. Do not infer a pack batch from them, the directory name, or a shared version number. For an older pack without a batch marker, verify a unique original fixed inventory or formal release record. If sources disagree or cannot be uniquely verified, report the gap and pause adoption or upgrades that depend on them.

Where adoption is already recorded, use the core and module source versions in config to locate actual originals through D:upstream. Confirm fixed batch, language, and scope separately. If candidates A and B both say 0.1.0.0 and the adoption entry points to A, receiving B only supplies comparison material. Switch only after adopting and verifying B under §12.2.

If an old instance has no active pointer, determine a unique original from the original adoption records and fixed inventory and include it in an approved index change. A missing original can be retrieved only from the same selected fixed version or batch. Report unavailable or ambiguous comparison sources and hold dependent changes until they are established.

Originals are comparison evidence, kept unchanged. They are not rules in force or a routine full reread target. Git state and user snapshots recover the actual instance before each change. The two uses are separate, with different cleanup authority. Do not pre-create an empty originals directory or invent an entry without a real D:upstream source.

### 5.2 Write the charter and start work

Agree on the complete plan and charter in chat, without a separate initialization-stage document. After approval, write them under document authority; the first live state is Ready to start. Create directories and place originals, governance, config, and indexes under the plan. This does not establish environment, migration, or Git completion. Retain old source rules as evidence and do not overwrite the approved target charter.

Handle the setup session title under §3.6. When authorized and supported by the host, set it during setup and verify the result. The full plan can include this authorization. If the title already matches, verify it. Report the actual title and any limitation if changing or verifying it is unavailable, and continue the remaining approved work. Apply this only to the current setup session. Record the user-designated maintainer in the existing handoff identity section, with a session reference when available.

1. Save originals under §5.1 and fill actual identity, root, target version, requirements, and needed basis. A charter alone is Ready to start; if concrete work has already begun, keep In development even when completing the documents. Do not prefill a branch or tag without a real object, or use `initialized`. When filling the charter, replace both Git and branch placeholders in root AGENTS §4.2 with the approved choices. Before repository creation record choices as planned, without claiming a branch or commit. With no Git, branching is not applicable.
2. Install the three local core specs in the dedicated D spec directory, normally docs/spec, whether K is local, external, or unused. Root docs locates D. Do not add configuration paths or a D repository or version.
3. Register the actual spec type, entry, and B for index-spec, handoff-spec, and design-spec in D. Use D references rather than root `rule-*` aliases. Same-named provider specs retain their authority and do not replace the complete local model.
4. With D and T in place, register selected K/R/M only. K may be local, shared, or imported by inventory; no unselected layer is pre-created. Establish actual protocol, owners, locale, governance, data protection, and consumption. D core is independent of data arrays. Do not copy shared roots, set up their Git, edit their indexes, or create a second T.
5. Selected module rules may be installed with authorized charter and support. Verify their clauses and specs in the same task. Retrieval, communication, and unattended work retain separate execution permissions.
6. Verify how parent rules, the three states, and first repository setup apply. Add `shared_layer` and `root_governance` when required. Do not guess missing values or rights or exempt yourself. A new layer without a reliable stable baseline uses `development` and `stable_ref=null`; maintain it from actual approval and reference.
7. Check D spec entries, actual bytes and full directory membership under root §1.3, then reread all active rules and specs under root §1.4. Use passages read in full in this reread to check clauses and prepare its record. Verify same-source fixed data separately. Once the support adopted for the core and any modules passes verification, synchronize the source versions and D:upstream entry under root §6 and read them back. Report incomplete writes with exact gaps. Status does not prove verification.
8. For document-only approval, stop at Ready to start. If the same authority includes engineering, move to In development when concrete work starts and continue. Environment, dependencies, business copying, Git setup, and commits are concrete work. For migration, copy → align governance and entries → create Git at the target if selected. Do not create an empty repository before the import. Fresh setup follows approved dependencies.

Resume only work remaining in the same valid authorization. Record actual progress in existing handoff. After a pause or return to discussion, require explicit execution to resume. Changes across files and repositories are not atomic; do not claim unfinished steps.

### 5.2.1 Unified adoption of D and shared data

Local D owns all three core specs through root docs and D INDEX. K/R/M choices affect data entries, protocols, sources and maintenance rights.

```text
Type: relationship | Local documents and data sources
root docs → D index → complete local specs
root K/R/M → actual owning index → fixed data
root T → registered temporary categories and approved ownership
Parent rules already in force retain their actual scope
```

Check the actual external index columns, including category, under D:index-spec#local and D:index-spec#paths. Use D:index-spec#targets and D:index-spec#checks for protection, with file for individual governance or design files. Explain any empty protection scope. D checks always apply.

Use D:index-spec#source to verify INDEX, members and body are from one fixed source. Otherwise record the reliable fixed subset or actual local guarantees. A copy does not make a second layer. Partial trees do not pass complete-directory checks.

Direction 1 adopts the local D model. External rules retain their authorized source and scope. Put ownership, source or applicability blockers in the plan and follow root §1.6. With no shared dependency, verify the independent D path.

For upgrades, compare old originals, local customization, and new originals. List active specs moving to D, references to update, and required directory protection. Retain old originals, history, and commits at their previous locations. Do not silently reinterpret old “minimal K + T” to remove K. Keep an existing K with knowledge, references, or independent repository history by default. Removing it requires a complete separate plan and permission. Do not delete libraries, move .git, alter tags, or automatically combine repositories. K rules and the K index become local active files only for a selected local K; external K follows its protocol.

### 5.2.2 Instance root README

Write the instance root README under the approved plan with its actual workspace name. Use “Start here” in the first view to direct readers to root INDEX, current handoff, and the Agent Guide in D. Verify the links from current indexes; a custom D still resolves through root docs.

Add a short local purpose or fact only if it helps using or resuming the workspace. Get current version, progress, and authorization from handoff; this page is navigation. Keep the pack README unchanged at D:upstream under §5.1 rather than repeating it. For an existing workspace, add approved links while retaining useful business guidance and references. Decide charter and small-task permission separately under §5.2.

```markdown
# <Actual workspace name>

## Start here

- Find files: open the [workspace index](INDEX.md).
- Continue work: read the [current handoff](HANDOFF.md).
- Find procedures: use the [docs entry](INDEX.md#docs), then open the Agent Guide in D.
```

### 5.3 Selected Git actions

Repository creation, initial commits, and version branches are concrete tasks requiring execution authority. Enter In development and use the target number agreed in the charter. In migration, finish approved copies, governance, and entry checks before creating Git at the target. Do not use source .git, parent Git, or an external shared repository as the target. Verify repository roots and author identity; stage only listed items, not unknown content.

| Scope | Initial commit boundary |
|---|---|
| Approved local repositories | Verify approved rules, handoff, overview and license, config, indexes, specs, ignores, adopted originals, and other tracked content path by path against the actual repository root. Follow the selected layers' tracking scope and keep an accessible entry for any empty selected layer |
| T | No separate repository. Exclude artifacts and track only the locally owned T index. Worktrees belong to their original repositories |
| Reused external K/R/M | Keep actual repositories and owners. Track only approved local files and reference entries in the local repository |

Ignore example for the default T path:

```gitignore
/temp/*
!/temp/INDEX.md
```

Derive ignores from the approved tracked paths, actual locations, and repository boundaries. Exclude external shared directories, other repositories, and T artifacts. Keep required governance files tracked. Check only necessary paths, including custom or nested T paths and indexes that should be tracked.

For a newly approved repository with no commits, use D:handoff-spec#branch to commit the approved charter and required files to main as the common start. The first version is normally 0.1.0.0, shared by the start and development. Create `dev/<version>` before later work in branch mode. Then main advances only at formal release. Direct main and custom branches use their approved rules. Do not recreate starting commits or move fixed tags. Stop affected Git work for unresolved parent conflicts or missing permission without requesting permission already given.

Follow actual authority for each repository. T has no separate repository and shared repositories remain with their owners. Include controlled README, license, and originals according to actual scope. Keep inactive resources in T cache. First commit does not establish acceptance, release, or formal stable consumption.

No account, remote, or network is required. If a command fails, record the repository, completed commits, and remaining steps. Do not rebuild, amend, reset, or force-push to hide history already consumed.

### 5.4 Fixed references and closure

Check the approved §4 inventory, including choices, source and language, entries, B and membership, copies and adaptations, actual repository, branch and selected commits. Record progress and gaps in the active handoff, without initialized or an initialization tag. Verify actual files; discussion or self-check does not revert In development.

A commit cannot contain its own not-yet-generated ID. If consumption needs a fixed tag or copy reference, include it in the plan. Create and check it with permission once the complete object exists. Do not record a missing or unverified reference as existing. Fixed tags stay in place.

Record actual adopted sources and resume the same fixed source. Use stable_ref=null without reliable placement; an initial commit is not a consumption baseline. Distinguish local and source Git and external guarantees under D:index-spec#source.

Report source, target, version, status, files, repositories, completed and remaining work, evidence and review entry. Close at the actual state. Follow root governance for separate release and publication permissions. Continue the same task within authority or return to discussion.

## 6. Verify initial setup and handoff

| Scenario | What to verify |
|---|---|
| Minimal layout | Root plus D and T. Create K/R/M only when selected. Check complete D core coverage. Data arrays may be empty. With Git, track only the locally owned T index within T |
| No Git | Files and entries are complete. Explicitly record no repository or commits; no invented branch or fixed tag |
| Independent minimal no-Git handoff | Use pack README §1.1 for charter and a small document task. Check instance navigation, packaged example location, D protection, absence of shared dependencies, actual work and source. Have a new session recover facts, results, and necessary basis from files and continue within authority |
| Custom paths | Local directories and approved shares match index. Guide, originals, and ignores follow actual locations |
| D resolution | With or without local or external K, use root docs, D entries, and local specs. Check all three core specs and full directory. Do not use originals or history as current rules |
| Derived directories | Real directory IDs or named file `#./`, correct boundaries, same-source membership, and B. Missing identity or files cannot pass |
| Optional knowledge base | Without K, local docs and methods still work. Formal output needs approved K, raw acquisition may use T, and installation does not create K |
| Both governance directions | Direction 1 fully aligns with fieldcase. Direction 2 records actual autonomy and retained originals; previous customizations or originals do not establish the choice |
| Copy migration | Keep the source, verify the full approved copy, align governance, then create Git at the target if selected. Source .git and ancestor Git do not count. Where layouts differ, verify classification, placement, and the affected entries, references, and tasks |
| Parent shared adoption | Verify actual shared protocol, fixed source, keys, membership, protection, and ownership. Confirm local management and applicable parent rules can both be followed. Record actual site result |
| Root maintainer and session title | Before answering, the user can identify who will assume the role and what it entails. Verify the user's designation and, when authorized and supported, the actual title. Record host limitations under §5.2 |
| Three states and document preparation | Discussion creates no state. Writing enters Ready to start, actual work enters In development. A stage does not release or revert. No `initialized` dependency |
| Target version and first commit | Set the version at charter approval, reuse it across first-version work, use common start and dev correctly, and do not add an initialization version or automatic stable tag |
| Interruption | Preserve actual results and commits, reuse reliable choices, resume remaining work only. Verify authority after pause |

After opening an empty workspace, start with one real task under §8. Add modules under §10 or upgrade and recover under §11–§12 as actual needs arise. Record the results of the steps exercised.

Do not exhaust all combinations. Run declared cases in the actual host and record them. Mark untested systems and harnesses. Distinguish static checks, actual setup, and user acceptance. Old five-state evidence does not verify the current three states.

## 7. Interruptions, failures, and moves

| Situation | Action |
|---|---|
| Discussion answers only | Reuse only reliable recovered answers. Do not treat lost answers as facts; ask about gaps if necessary |
| Some files written with valid authority | Compare each with the plan. Preserve matching results and repair within scope |
| Some repositories or commits made | Verify actual roots, branches, and commits. Continue remaining actions without recreating repositories or commits |
| A state or old flag claims completion but a file or commit is missing | Record actual remaining work and repair only as authorized. Do not claim completion or rebuild from scratch. Keep In development once work started |
| User paused, returned to discussion, or canceled | Do not resume automatically. Report actual state and wait for explicit execution |
| Target involves an old workspace | Use [11] if migration is not planned. If approved, resume §7.1 without overwriting the source |
| User explicitly requires moving the original | Verify source disposition and recovery scope, then update actual root and physical config. Do not replace default copying or redo valid documents, copies, or repositories |

Repair and reverify when possible within the original scope. Explain and clarify new scope, missing permission or evidence, or conflicts first. No-Git recovery uses actual originals, snapshots, and path inventories, not Git rollback.

### 7.1 Copy from an existing workspace

The recommended default is copy, align governance, then create the target repository locally. This applies to both governance directions. For an explicitly required move, separately specify source disposition, authorization, recovery, and verification. Do not use moving as the default or delete the source under a copy plan.

```text
Type: process | Copy migration
┌ Fix sources and copy approved content; keep the source
│ → Align governance and actual entries for the chosen direction
│ → Create and verify Git at the target if selected
└ → Continue trials and acceptance; session moves need separate authority
```

1. Verify duties, source, and independent target. Confirm route and governance, reusing explicit choices. Inventory actual source files, uncommitted and untracked changes, deletions, necessary history, and dependencies. Git HEAD is not the current business tree.
2. Show the complete copy list, batch, and target. Distinguish unchanged items from path adaptations and identify the originals, business files, and recovery inputs. Keep the source. Where layouts differ, classify by purpose, ownership, and actual dependencies. List the original and proposed locations and references to update. Keep originals and mark unclear, conflicting, or unforeseen items for a decision before processing them. Resolve unknown target contents or Git before overwriting anything.
3. After authorization, preserve fixed fieldcase originals and evidence of the source, then copy approved contents. Batch by dependencies if needed. Do not silently omit attachments, decisions, pending work, or history, and do not overwrite the target with source .git. Preserve the original repository or a read-only history copy if authorized and needed.
4. Compare unchanged copies to source evidence and record exclusions, source changes, and remaining dependencies. Keep recovery or original-structure copies read-only; run writing tools only in separately approved working copies. Do not force overwrite after source or target changes.
5. After copying, align under `governance_adoption`. Direction 1 creates live files from the approved complete fieldcase template and shared adoption rules. Prior management is migration evidence. Direction 2 implements approved local governance, adopted scope, and maintainer. Keep business rules, facts, decisions, and needed history in their new authorized locations. Do not erase them on replacing governance or substitute business rules for common governance.
6. Update current target entries, config, and HANDOFF. Verify shared layers, actual spec references, protection, and completion conditions. Do not infer completion from source root, state, repository, or `initialized`. Verify copying and adaptation separately. Do not rewrite source history in bulk.
7. After copying and alignment, create the target's own repository under §5.3 if selected. Preserve source and share repositories and keep source business version separate from target version. With no Git, record the actual capability boundary.
8. Verify resource list, lifecycle, actual Git roots and selected commits under §5.4. Record copy, alignment, Git setup, self-check, and user acceptance separately. Completing work does not revert to Ready to start. On interruption finish outstanding steps without re-creating Git or overwriting work already done.
9. Before any separate session directory change, deliver migration results and quick-review material. After agreed confirmation and explicit authority, verify affected project sessions and change only approved objects. Recheck original session, project, primary and secondary directories, actual cwd, and continuation. File migration does not establish a session move. Do not create a new session in place of moving the chosen one.

## 8. Normal takeover and a small task

1. Reread all applicable rules and specs under root governance. Verify actual workspace, version, branch, state, and original dependencies. A child uses its own handoff. Reading governance is not authorization. Use actual D entries for the approved local rules; a data pin does not replace them. Reread other applicable parent specs in full from their actual sources.
2. Resume from the active charter, items, and actual state. Interpret lifecycle and item labels under the specification adopted by the instance. Use D:handoff-spec#state and D:handoff-spec#status. Ask only about missing goal, scope, or completion conditions. A missing `initialized` or Ready to start does not require the questionnaire again.
3. Put the goal, sources, limits, necessary resources, and acceptance in current E as authorized. Draft in chat if writing is not authorized.
4. After explicit execution, do the small document task in scope, for example organize a requested note and check its links. Do not invent business tasks or content.
5. Fix K or other sources as needed and restore the same source on resume. Distinguish business facts, governance authorities, and proposals.
6. Verify actual documents, entries, and agreed outcomes. Give review paths, actions, and pass conditions. Record results, gaps, and no-commit or not-published status. Return to discussion or continue within existing authorization.

Ordinary execution starts directly. If the user requests preflight, collect necessary permissions together and use the exchange limits and closure rules in root governance. Preflight choice does not waive verification or acceptance. On version change, use D:handoff-spec#size for handoff measurements. An alert does not replace complete records or approval.

Do actual work with the target version and branch arrangement confirmed in the charter. Setup does not consume a separate initialization version. Determine new versions by real scope and approval. Follow actual repository and authorization boundaries. Without Git, a document task can still complete, with history limits stated.

### 8.1 Start or continue design work

Use D:design-spec#scope and D:design-spec#use to establish design object, scenarios, and relevant constraints. Ordinary document work with no design task proceeds without an empty DESIGN. Reading the spec is not permission to create or implement.

When brand, project, or domain design guidance exists, use its actual approved entry and retain its scope, parameter authority, and assets. If no suitable file exists and the task needs one, propose an exact path in the root, a self-contained body, scope, and registration. Create it through existing approval and execution gates. Do not add a required setup question, config switch, or optional design module.

For later design work, read the scope and applicable guidance before relevant assets or implementation. Distill from authorized current rules, verified practices, problems, and fixes. Separate facts and decisions. One success or failure is not a workspace-wide rule. Read necessary historical matches rather than all history or source.

Use D:design-spec#split for guidance, parameters, problems, and task facts. Propose amendments for new criteria, contrary evidence, limits, or changed premises. Check the original user decisions plus additions and exclusions. After approval update necessary files and active links. Distinguish documentation checks, artifact or implementation checks, and user acceptance; do not pass untested work.

Suggest reusable guidance to the user first. The user decides sharing and actual entry. Local DESIGN work does not require the cross-workspace module. Do not install it or send messages automatically to propose sharing.

## 9. Consumption, protection, and configuration issues

### 9.1 Fix data sources

Read the default in config. In one HANDOFF dependency table record actual layer, adoption mode, content version, and fixed reference. Use a concrete commit for development and a verified fixed baseline for stable use. INDEX, membership, and body come from one source for the entire task.

Switch at a new task or explicit update. Do not follow changes after another session, compaction, or interruption. Read each INDEX, its members, and content from the actual owning repository or fixed copy. Verify the version of each source. Do not switch the maintainer's worktree. Expand actual files in T only for manual review when needed.

Comparing a candidate does not change a pin. For an actual trial, record scope and prior formal dependency in the same place. Selecting K does not also change R, M, root governance, or the global formal entry or start following dev. End a trial by restoring the previous dependency or adopting an approved baseline.

Keep formal consumption stable with a same-repository T worktree for development and common history. Close root and layer work under their branch methods. Explain limits of no Git or direct main in the plan rather than inventing snapshots or isolation.

### 9.2 Protection checks and mismatch reports

Start with root startup checks. For instance specs, check the root docs entry, actual D rows, and dedicated spec directory. For data separately resolve `file`, `pattern`, and `directory` at its fixed source. `#./` only selects a named file's parent for a directory target; it is not a section or guessed path. Check full membership and per-file B without cross-source or cross-purpose deduplication, directory totals, or hashes.

Example report:

```text
Code: INDEX_BYTES_MISMATCH
Layer / ID: K:<actual-id>
Fixed source: <selected commit or verified local state>
Actual entry: <resolved from the owning index>
Registered / actual: <B> / <B>
Impact: <stopped task>
Recommendation: Have the authorized maintainer investigate content and index, repair within permission, then explicitly adopt and recheck the repair source.
```

A consumer does not change a recorded size to silence an error or use an old INDEX for a new file. Same B is not evidence of unchanged text. If an authorized content change leaves registration unchanged, do not add meaningless fields to force an index diff.

### 9.3 Configuration exceptions and repair

Use the root field and exception tables to check syntax and duplicate keys, exact sources, active locale, protection and consumption types and values, actual scope, module sources, presentation preferences, and unknown keys.

Do not guess key values. For a display preference you may explain and temporarily use `standard` or `table` for this turn. Check approved local definitions for unknown fields. Preserve and report unexplained keys without assigning meaning or writing them back.

For example, report string `false` for `enforce` as a type error and stop dependent work. Do not fix `enfoce` as if the user intended disabling protection. Changing `locale` does not translate documents or history.

Only root can remove enforced stops for existing index mismatches within explicit user-authorized repair. Keep light checking and report actual gaps. `restore_prompt=never-ask` only suppresses the restoration prompt. Do not restore automatically or repeatedly ask; act if the user explicitly asks for restoration.

## 10. Discover and adopt modules as needed

### 10.1 Check locally first, then ask about network access

For a real capability gap, check installed features and then the pack README and actual resource index. If compatible material is missing, show the official source, needed contents, and supporting requirements before asking about network access.

Get the exact fixed pack and necessary instructions. The user can adopt a compatible module, evaluate a full upgrade, or keep the current setup. A new release does not block current work or cause polling. Do not assemble from latest or floating main silently.

For local T, enter fieldcase/INDEX.md through the root T distribution entry. If reusing a parent T without that category, register the real fixed-pack entry in D and reuse retained originals where possible. Do not create a shared category or second T. Check provenance and inventory, then read `adoption`. It gives actual R/M and module targets, complete supporting changes, combinations, and checks. It is not active governance or proof of installation.

### 10.2 Integration steps

1. Verify module ID, exact version, compatible core baseline, layer and module prerequisites, supporting files and clauses, and necessary parameters from the resource index.
2. Check actual installation. Config, files, and behavior support must agree. A download or one skill is not installation.
3. Present proposed edits, directories, retained originals, configuration, index, and checks for user approval and explicit execution. Show full supporting governance text first.
4. Save selected originals and install method specs in local D/spec, with real entries and B in D and no root aliases. Acquisition methods may be installed first. Raw-only tasks can use T; formal output needs a K target first. Do not edit shared K governance or use an unauthorized shared T contract entry. Report missing dependencies instead of making a second T or overwriting the upstream index. Record inheritance separately; explicitly register adopted modes. Record the source only after support verifies.
5. Verify behavior, protection, and necessary entries. Then synchronize the actual `modules.<id>.source_version` and D:upstream entry under §12.2. Retain the core source.
6. Record actual results, gaps, adopted material, and later discovery entry in handoff. Return to discussion rather than pushing unselected modules.

Merge edits to the same file using the adoption guide and register only selected active content. Collaboration requires its dedicated contract index and exception to generic indexes. Unattended adoption adds only approved modes; it does not start a task. Keep existing questions and presets. More resources do not change user choices; no project skill wrapper is supplied in this pack.

A module can provide unattended preflight choice, thread heartbeat, continuous iteration, and separately enabled retry extension. Actual capabilities follow fixed compatible materials and definitions incorporated in root AGENTS. Installation only establishes rules. Execute only with explicit task and mode. State missing Goal, heartbeat, or communication capability and its impact rather than counting automation as passed.

A module can consist only of edits to existing files, without a new spec for form alone. Skill wraps, parameters, and directories follow compatibility and user choice, without predetermined quantities or mandatory global install.

Uninstalling also reviews actual rules, entries, dependencies, and customizations. Deleting a config row does not complete it. Installing a module alone does not change `fieldcase_version`; a core upgrade does not update every module source automatically.

## 11. Compare official updates and user customizations

Read governance direction from config first. Direction 1 keeps all applicable management requirements; direction 2 uses its approved scope and implementation. Investigate a missing direction without inferring it from older customization or switching it during an upgrade. Check D's actual active specs and entries. A provider's same-named file or new layer version does not upgrade local rules. Moving files alone does not change source version.

### 11.1 Three materials

Use §5.1 to locate exact adopted core and relevant module originals in D:upstream. Resolve current local files through current indexes and prepare new fixed originals as authorized. Verify all three independently. Report a missing old original under §5.1.

| Comparison | Shows |
|---|---|
| Old official ↔ current instance | Local customizations |
| Old official ↔ new official | Upstream additions, edits, and removals |
| Both comparisons | What to keep, adopt, combine, or defer |

Match objects by stable ID first. Retain name, root, local paths, language, repositories, and preferences under existing choices. They are not automatically governance conflicts. Preserve necessary facts, work, and history in HANDOFF.

For a three-state upgrade, use the approved current work, tasks actually started, and real release evidence. Do not derive it directly from an old label or `initialized`. Preserve previous initialization baseline, fixed tags, evidence, and history. Do not retroactively record a release, redo finished work, or reset local version. Ask the user to confirm ambiguous mappings from old uninitialized, initializing, or Ready to start. Remove old fieldcase flags only from the approved current files. Autonomous custom fields retain their own authority.

### 11.2 Decide item by item

| Case | Suggested handling |
|---|---|
| Only upstream changed | Explain impact and propose adoption, subject to applicability |
| Only local changed | Keep business and supported settings. For direction 1 explain management differences and align with fieldcase or wait for decision. In direction 2 evaluate retention under approved local rules |
| Both changed the same rule | Give location, intentions, conflict, proposed outcome, and impact for user decision |
| New dependency or required field | Include all supporting changes in the same plan without enabling an entry in isolation |
| Upstream removed something still in local use | Explain affected references and behavior, then decide retention or migration |

Do not replace user decisions with automatic scoring. For complex governance merges, advise reasoning settings under root §2.2 before starting the next round. For governance drafting advise at least `xhigh` only after verifying availability. If the user directly asks for execution, use current settings and mode. Advise changes for later stages, using actual host confirmation. Do not change models or expand scope because of a level.

## 12. Matching backups, applying changes, and targeted recovery

### 12.1 Verify recovery before changes

Follow root §6 for a prior-state recovery basis. For every path list addition, edit, removal, or move, previous presence, and recovery source. Cover affected governance, config, indexes, specs, guide, ignores, and user-added rules, plus prior source fields and current D:upstream pointers. Approve necessary business, knowledge, or history changes before including them. Keep the change list and recovery pointers in the existing plan or HANDOFF.

| Actual situation | Necessary handling |
|---|---|
| Existing Git covers all prior state | Check actual repository root, tracked paths, fixed commit, and prior contents. Keep inventory and recovery pointers. No required file snapshot or D:backups entry |
| No Git, or commit lacks needed uncommitted, untracked, or ignored material | Save matching snapshots only for affected files not covered. Combine them with sufficient Git evidence as needed. Do not copy the whole workspace |
| Only a moving branch, an ancestor repository, or unverified Git claim | Not reliable recovery. Verify actual paths, contents, and fixed source |
| Recovery source missing, inaccessible, or incomplete | Stop before changing affected files. Report the gap and continue independent authorized work |

Identify the actual repository and recovery source per path. Record the fixed commit or snapshot that covers each affected path. A commit proves its own contents only; cover actual uncommitted edits. Creating a commit, tag, stash, or other preservation step needs authorization. Do not include unrelated changes or clear and reset the worktree to manufacture coverage.

For necessary physical snapshots use the actual D:backups entry, normally `docs/backups/<date>/<upgrade-batch>/`. Put the batch INDEX outside `snapshot` with scope, source per path, additions and removals or moves, and recovery steps. Store files under their actual instance-relative paths. Do not recursively copy existing backups, adopted originals, .git, or unrelated data. Keep previous batches on same-day retries. Later Git does not authorize deleting old snapshots.

If Git already covers recovery and no physical snapshot is made, do not invent a backups entry or empty directory for a commit ID. This simplification applies only to restore coverage during resource upgrades. Regular release and backup follow D:handoff-spec and applicable parent rules.

### 12.2 Apply and record sources

After verifying originals and recovery, apply the user-approved three-way decisions. Do not overwrite adoption direction, roles, name, root, business facts, existing version, or valid customizations with new templates. Synchronize D entries and references, actual layer entries, protection, membership, B, and derived config. Keep a single writer. Move only approved current working files, not originals, old evidence, or another workspace's files.

Once current files, supporting changes, recovery, and agreed checks are complete, update actual config source versions, the root INDEX core display, and exact D:upstream originals under root §6. Reread all three and the original. Verify object, version, batch, language, and scope. Switching between same-version candidates can preserve version values but still needs the correct new pointer.

Update only the adopted core or modules in scope; preserve the rest. If application or source updates are interrupted, record completed and remaining work and original sources in existing HANDOFF or the task record. Resume or recover under §7 and §12.3. Verify commits, instance version, source adoption, acceptance, release, and public publication against their own evidence.

### 12.3 Failure and targeted recovery

| Failure point | Handling |
|---|---|
| Acquisition or comparison basis insufficient | Preserve current files and report missing originals or reliable sources; do not guess a merge |
| Recovery verification fails | Do not change affected active files. Git existing is not coverage |
| Partial application or verification failure | Repair within original authority. Otherwise use approved inventory and each path's recovery source |
| Existing upgrade commit must be withdrawn | Recover scope and make a restoration commit only if authorized. Keep consumed history, without reset or force push |
| Independent changes after upgrade | Separate scope and put conflicts to the user. Do not discard later work during recovery |

Restore modified or removed files from verified Git sources or snapshots. Remove added files only after confirming no later edit or use. Reverse moves from recorded paths and resynchronize indexes, config, and sources. Do not replace an inventory with a full repository reset or pack overwrite. Do not commit recovery without permission. Report actual remaining work.

After recovery, check actual entries, protection, B, and necessary content. For source changes check the prior config, root display, and D:upstream pointers against the inventory. Keep conclusions, evidence, and remaining authorization. Without Git there is no recovery commit. Neither Git nor snapshots promise recovery for uncovered material. Keep old originals, tags, history, and raw reports at their actual sources; structural upgrades do not rewrite evidence.

## 13. Manual review and delivery

Use Discussion: Sketch for structure, paths, or process; keep the design concise with key relationships intact. Use Discussion: Visualize for host-rendered preview and Discussion: Draft for full text and differences. None of them grants project writes or implementation; follow root rules.

At delivery, state the actual objects and status. In source-item order give entries, actions, pass conditions, gaps, and agent help needed. State shared prerequisites once, and explain coverage of reused results. Mark unverified locations.

For documents verify intended content, necessary clauses, index resolution, config, and unfilled placeholders. For setup verify actual files and selected repositories. For recovery verify the inventory and restored content. Static consistency does not establish successful operation.

Temporary execution reports changed files and absence of commits and backups. Normal release follows D:handoff-spec and public publication is separately authorized. Candidate ZIPs, drafts, or a completed setup do not trigger either.

This guide does not install background processes. State missing host capabilities, untested platforms, unconfirmed copyright, and unverified official entries. Theoretical support does not establish acceptance.

## 14. Authority and review

This guide explains procedures and its actual path is the `agent-guide` entry in the D index. Report and verify any conflict with root rules or the relevant specification rather than choosing a looser interpretation. Update affected examples, presets, and references with changes. Review triggers are in the metadata.
