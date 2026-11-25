# fieldcase · English resource pack

fieldcase is a starting point for setting up, copying into, and taking over a workspace with an agent. The root files define rules, navigation, configuration, and handoff. D holds documentation and current rules; T holds temporary artifacts. Add K, R, or M as needed. See §2 for each layer's role.

## 1. Where to start

Start with this pack README and give the agent the target workspace and one small task you want to do there. The directory you opened for this session can be the target, and the target need not exist yet. The agent checks the target separately from the pack’s location. You do not need to fill in options or write a separate onboarding prompt.

- First adoption: When you start from this README with an empty target and a small task, the agent guides first adoption unless you ask for review only or have an approved plan to resume. The same applies if the target does not exist or contains only inactive pack files or templates. The agent reads §1.1 of the guide through the entry below. If the workspace language is unconfirmed, the agent must read the text of §2.5 in the [AGENTS.md beside this README](AGENTS.md) before asking [1] in the first substantive reply. After sending it through the clarification tool, the agent waits for your actual answer. It resends the same question once only if you say it did not appear. If you still cannot see it after the retry, it offers equivalent choices in chat. With no usable clarification tool, it offers those text choices directly. If the language is confirmed, the agent asks the first unresolved required question.
- Plan and authorization: The agent puts the small task in the full plan and presents it with the charter for your review. A task draft does not replace the first question. The agent writes files or starts work only within the scope you explicitly authorize after reviewing the plan and charter.
- Takeover: With an active charter or an approved plan to resume, the agent takes over using the target’s actual files and authorization.
- Review only: If you explicitly ask only to read, check, or draft in chat, the agent gives you that result without starting the adoption questions. You can still answer the first adoption questions and review the plan before authorizing any writes.

The agent uses the [root index](INDEX.md) to find the [root rules](AGENTS.md), [handoff](HANDOFF.md), and [configuration](config.json). It follows the [docs entry](INDEX.md#docs) to the D index and finds the guide by `agent-guide`. See D:agent-guide §1.1 for starting, reviewing, and taking over. Resolve the actual directories and K/R/M/T references through their own indexes.

This fieldcase 0.1.0.0 English resource pack contains 12 core files and 10 supporting files for K, R, M, and the three optional modules. The `0.1.0.0` in the configuration and the root index identifies the resource source. Extract the pack into a separate directory and start with the instructions above. See §5 for test scope, deferred checks, and licensing.

Pack batch: `fieldcase-0.1.0.0-en-US-menu-01`; pack language: `en-US`. This batch identifies the complete resource pack. The distribution index records the sources of the supporting material for K, R, M, and the modules. If you only have the extracted files, use this pack README to verify its batch.

The agent host needs actual local read and write access. If you choose Git, it also needs local Git. Basic use does not require another project, an external skill, an MCP server, a dedicated runtime, or a GitHub login. If a capability is missing, explain the limitation and any manual alternative. State which checks were not run.

### 1.1 Minimal start

A useful first task is a brief entry note for the next person, with a check that one of its references works. For a minimal setup, you can choose the root files plus D and T, no Git, and only the core and any rules needed by the layers you select. Answer based on your needs; this example does not select an option for you.

Include the small task in the plan alongside the charter. If authorization covers only writing the charter, stop at Ready to start once it is in place. If the same authorization covers the small task, use the agreed target version and verify the result. See §1.3 to hand over to a new session.

### 1.2 From resources to an approved charter

1. Confirm the language and check the fixed resources for that language. Distinguish a built user pack from a source archive. Use an official download address only after verifying it.
2. Choose whether to start from scratch or copy from an existing workspace. Choose full fieldcase governance or partial or complete local governance with private copies of the adopted originals. Do not infer the choice from previous customizations or from the presence of originals. Retain names, business facts, and settings that can be changed as the plan permits. The usual migration sequence is copy, align governance, and then initialize Git in the target if chosen. Keep the source in place; moving it needs explicit authorization.
3. Have the agent check the source, target, identity, components, paths, configuration, and Git using the guide. Reuse reliable answers. The adopting workspace implements the chosen governance in the target and checks its actual external dependencies.
4. Review the full plan and draft charter in the chat and confirm the target version. Once document writing is authorized, preserve the adopted originals and write the charter and necessary files together. A newly active charter is Ready to start if concrete work has not begun. Preparation has no separate state or flag.
5. When environment setup, dependencies, business copying, Git setup, or the small task actually starts, use In development and keep the same target version. After an interruption, do only what remains. Finishing a stage does not return the workspace to Ready to start. Releasing a version and publishing it are separate decisions.

The template leaves `locale` and `governance_adoption` unset until the user confirms the language and governance choice. English resources and the supplied D and T files do not answer on the user's behalf. If resources for the selected language or layer are missing, use the guide to check them rather than switching the selection silently.

### 1.3 Take over an existing workspace

Give the new session the actual workspace root. The agent rereads the applicable rules and current handoff as directed by the root rules, checks the target version, state, branch, sources, existing work, and remaining items, and resumes within valid authorization. Do not redo finished work or ask again for confirmed choices. New tasks need an explicit scope and completion conditions. If there is no Git, state the actual limits on history and isolation.

## 2. Components and responsibilities

| Component | Purpose |
|---|---|
| Root files | AGENTS governs permissions, HANDOFF records the current work and lifecycle state, config records choices and core and module sources, and INDEX provides navigation |
| D | Local documentation and current rules, reached from `docs` in the root index. Rules stay in the local `spec` directory; D has no separate repository, layer version, or content pin |
| K (optional) | A working knowledge base. Create one, use a shared one, or import approved material. Core rules do not require an empty K layer |
| R and M (optional) | Reference snapshots and evidence, or production materials. Use their actual protocols and permissions |
| T | Temporary artifacts and inactive materials, filed by ownership. T has no separate repository. Do not copy a shared T or add shared categories without authorization |

D INDEX locates the three core specifications and records their types and B. Use D identifiers without root aliases. Provider and parent rules keep their actual scope.

D:upstream preserves exact adopted originals; a copy does not adopt it. See §4 and root governance for upgrade recovery, and the applicable release rules for ordinary backups.

## 3. Optional modules and discovering more capabilities

| Module | What it provides | Required support |
|---|---|---|
| Knowledge acquisition | Methods for fetching, converting, indexing, and optional verification | D methods and T cache; approved K destination for formal output. No bundled business knowledge base |
| Cross-workspace collaboration | Contracts, contact, task dispatch, and their boundaries | `contract-spec`, contract entry, and root mode rules. Installation does not authorize sending |
| Unattended work | Unattended preflight, task heartbeat, continuous iteration, and separately enabled retry extension | Root rules, handoff facts, and a T review entry. Installation does not start work. Adoption requires compatible resources and host capability |
| Project skills | Optional wrappers for actual modules | Same authority and compatibility baseline. No mandatory global install or predetermined quantity |

With local T, find the optional originals through `distribution` and the fieldcase resource index. If shared T has no such category, use the fixed pack entry registered in D instead of adding a shared category. Read that index, then the adoption guide. Available resources are not enabled resources. The pack registers only D and T by default; empty layer protection targets and `modules` do not mean the user has selected the minimal setup. Check the live root INDEX and configuration for actual adoption. Apply the user's choices, compatibility checks, and approval and execution gates. Record the exact source after adoption succeeds; do not maintain a duplicate source list here.

If work exposes a missing capability, check local capabilities and instructions first. Ask before going online for matching official materials. Install only a compatible module, assess a full upgrade, or keep the current setup as appropriate. There is no automatic upgrade or polling.

Useful discussion modes: Discussion: Sketch for a character or Markdown structure preview; Discussion: Visualize for a visual preview in the host; Discussion: Draft to review complete text and diffs. UI remains a drawing type. The root rules govern permission and capability. A preview is neither implementation nor acceptance.

## 4. Customization and updates

Root and local indexes own paths. The configuration records source versions for the core and modules. D:upstream locates the actual adopted originals, including the exact batch when version numbers are shared. HANDOFF records the local work version, lifecycle state, and actual dependencies.

Compare adopted originals, current instance and new originals under the actual governance choice. Get user approval and execution authority, then verify per-path recovery under root §6 before modifying files. Reuse covered Git state with a list and snapshot the uncovered files. Recover listed paths on failure. Update actual sources after supporting changes and checks pass.

Direction 1 uses fieldcase rules and the documented settings; replacing its entire local governance is not merely configuration. Direction 2 allows partial or complete local governance, with a clearly recorded adoption scope and owner. Updates are optional. Do not switch direction silently or promise that all customizations are compatible. For procedures, see the Agent Guide. The root rules and specifications own the models.

## 5. Test coverage and limits

The handoff and configuration files are templates. Optional materials are included. Extracting or reading the pack does not create a workspace or enable a module. Submitting ordinary answers does not replace explicit authorization to proceed.

Earlier isolated tests used separate, fixed Chinese candidates.

- First use and handoff: A user completed first use in an isolated workspace without Git and reviewed a small documentation task. A new session found the pending task from the workspace files and continued it after explicit authorization. A separate test covered read-only handoff. The original records retain deviations in rereading all applicable rules and recording pending review status. Review of the full changes before authorization was not verified.
- Git and migration: Tests covered creating a new repository, using a development branch with the same version, and a local trial release, including a main-branch fast-forward, backup, archival, and the release state. A separate migration test used an earlier answer set, copied the selected material, aligned the governance, and kept the knowledge base. The source copy was preserved, and the target used no Git.
- Source versions and recovery: Isolated examples located the exact original materials when candidates shared a version number, and verified targeted recovery using Git, necessary snapshots, or both. Earlier examples of adoption models, repository layouts, and optional materials retain their own test scope.

Field trials covered three scenarios.

- Empty workspace: The charter and entry note were written and reviewed. A new session took over from the instance files in read-only mode. A small project had a plan and follow-up tasks recorded.
- Copy migration: The source stayed in place. The separate target adopted the core governance and entry points, and a new session continued from the target files. The target had no Git repository.
- In-place adoption: An existing workspace captured its governance files and verified an isolated restore before applying the approved changes. The checks covered the actual shared source and its protections. A new session completed a scoped document task from the live workspace, and the user accepted this trial.

Earlier packs in both languages were unpacked and their entry points checked. English Minimal trials covered writing the charter and the first reread. A separate English instance also covered local Git and a one-page entry guide. These results use the status values actually written by those fixed candidates. Compatibility of the localized status labels is assessed in a focused regression for that revision.

A cross-host trial covered read-only takeover of a Chinese instance. The full Visualize or HTML questionnaire, quick-diagram interaction in the host, the broader operating system and host combinations, live module operations, and official download sources still have coverage gaps.

Check shared resources and applicable parent rules in the actual adopting workspace. Optional acquisition, workspace coordination, and unattended operation require the relevant capabilities and authorization.

See the [MIT License](LICENSE), sourced from the [Open Source Initiative](https://opensource.org/license/mit). See LICENSE for this pack's copyright year and holder. Migrated content and third-party materials retain their own license terms.
