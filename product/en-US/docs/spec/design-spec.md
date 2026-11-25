---
id: design-spec
updated: "2026-11-19"
recheck: Changes to design scope, distillation and use, placement or parameter authority, verification, or ownership
---

# DESIGN document maintenance specification

From the root docs entry, locate `design-spec` in the D index. D:index-spec defines index formats, D:handoff-spec defines handoff, and the root rules govern authorization. A file with the same name in K does not automatically govern the instance. Parent specifications that already apply retain their actual scope.

This specification governs distilling, organizing, using, and maintaining a workspace's DESIGN. “Workspace” means the consuming workspace identified by the user. Reading this specification gives no root or other workspace authority. Local governance controls authorization and implementation. Use the user's actual registered design sources; no K:design, frontend stack, reference project, design pack, or external skill is required. Complete governance rereading still applies. Reading only the relevant design sections does not waive it.

## 1. Content and scope <a name="scope"></a>

- Start the workspace DESIGN with the design object, type, usage scenarios, and scope. Include only approved design decisions and guidance. Preserve the prerequisites, relationships, methods, behavior, limits, exceptions, and acceptance criteria needed for later design decisions.
- Distinguish design types by object and use rather than tooling or format. One workspace can have several. Visual assets center on presentation; interfaces can also require interaction, components, compatibility, responsiveness, motion, and a technology stack. Choose what applies; do not require a uniform checklist. Specific design rules belong in the workspace DESIGN. This specification does not standardize styles, components, or stacks.
- Technical or medium constraints that affect whether a design works may be prerequisites, relationships, or agreements. Use #split for installation, build, debugging, and delivery. Design guidance retains necessary technical grounds.
- DESIGN may include specific rules with explicit scope. They need not apply to all work. Separate general principles, relationships that apply to a scenario, and concrete parameters as needed. Do not assume every workspace has a design pack, tokens, or the same tools.
- Design acceptance criteria state what a design should satisfy, not the result of a particular acceptance check. Do not record events, causal investigation, execution history, test results, acceptance results, incident IDs, or evidence chains in DESIGN. References to active specifications and assets only help locate what to apply. Preserve prerequisites and reasoning criteria when moving content.

## 2. Placement and a single authority <a name="split"></a>

Use the workspace's approved files and entries. Approve any new location or move under local governance.

| Location | Responsibility |
|---|---|
| Workspace rules, such as AGENTS.md | Long-term duties, permissions, hard rules, and when to read or maintain DESIGN |
| Workspace handoff, such as HANDOFF.md | Current authorization, tasks, state, and decisions; B has triggers and problem entries, C has user decisions |
| Workspace DESIGN | Approved design guidance, applicability, limits, exceptions, and design acceptance criteria |
| Parameter, asset, and implementation entries | Actual formulas, values, examples, resources, components, and capabilities. Organize them locally; do not copy the entire set into DESIGN |
| Problem record, per D:handoff-spec#pending-pit | Issues, events, verified causes, fixes, retests, evidence, and complete incident IDs |
| Original task record | Successful procedures, raw inputs, implementation, and verification for that task. Record decisions in handoff as prescribed |

- Give each rule one authority and reference it where needed. Specific guidance can be distilled. Do not maintain independent copies of rules or values. Test assertions and historical snapshots are not another specification.
- Move problem details according to D:handoff-spec#pending-pit. Keep original IDs and necessary history references. Do not invent a separate incident numbering scheme. If a problem record does not exist, propose its exact path and content before creating it. Successful work and its evidence stay in the task record without inventing an issue.
- Handoff, problem, and task records may point to current DESIGN rules. DESIGN does not link back into incident chains. Artifact versions, delivery, receiving responsibilities, asset lifecycle, and other non-design governance stay with their existing authorities.

## 3. Distillation, use, and revision <a name="use"></a>

- Without applicable design work, do not create an empty DESIGN or block ordinary document work. When a design task first arises, identify the object, scenario, existing sources, and necessary constraints. If a new file is needed, propose its exact path within the root and its self-contained body. Create and register it through existing approval and execution gates. Do not add a mandatory initialization question or a design flag.
- Where brand, project, or domain design rules already exist, adopt those first with their scope and parameter authority intact. Do not copy an entire source or override user customizations with a new DESIGN.
- Before design work, locate DESIGN through approved local governance or its owning index. Read its scope and applicable rules, then the relevant assets or implementation entries. Confirm locked choices under local governance.
- Distill existing guidance from authorized current rules, design assets, instances, and task records. Look for reusable principles, scenario relationships, and gaps beyond known issues or examples. Read only necessary matches in history through D:handoff-spec. Earlier placement does not invalidate a rule. Do not read all history or source. Read enough to support conclusions, and state evidence gaps.
- Distinguish explicit user decisions, rules in force, verified problems and fixes, tested success, and implementation capabilities. A failure does not establish a general rule, and one successful case does not become a workspace-wide default. Distill reusable relationships, methods, and prerequisites, with their scenario differences. Do not generalize a one-off constant.
- When implementation, repair, acceptance, or handoff cleanup produces a new criterion, a correction, a boundary, or an exception, propose it in an existing approved record or reply. Do not wait for release or invent entries when there is no finding. Update DESIGN and current references after user approval. Business verification does not approve documentation.
- Use and verify approved guidance in later work. Propose changes when counterevidence, recurrence, or altered premises warrant them. Keep current rules even if not recently used. Retire superseded or invalid content under local cleanup rules. For handoff use D:handoff-spec#cleanup and #rules; keep active references reachable.

## 4. Review, verification, and shared use <a name="review"></a>

- Group review material by design issue. State source location, proposed guidance, scope, and maintenance location in language the user can judge. For a pending decision, state what is unresolved, alternatives, and impact. References support verification but do not replace decision text. Ask according to local governance and the user's current request.
- When consolidating decisions, check each final user response. Preserve accepted statements, later additions, and exclusions. A summary or placement table does not replace the decision.
- Governance changes need a complete draft or diff and MVD measurement under D:handoff-spec#rules. Keep provenance in the review or an existing record. Do not add it to DESIGN or create a fixed ledger. Check the content boundary, usability of approved guidance, stated gaps, layering, single authority, and whether entries, reading, and later refinement can continue.
- Choose checks for the task stage, design object, and target scenario. Observe real visual output. For interfaces, inspect the applicable states, operations, and responsive relationships. Code, algorithms, and measurements support judgment but cannot replace observations. Separate documentation checks, implementation or artifact checks, and user acceptance. State missing conditions and untested cases.
- Suggest promoting reusable DESIGN guidance when it helps another workspace. The instance user decides whether to make it shared, who reviews it, and its entry. K:design is not required. If cross-workspace collaboration has been adopted and sending is authorized, use the root rules. Otherwise give the user text to forward. Local approval is not shared approval.
- The owning workspace maintains DESIGN under user authorization. Revise this specification through root documentation approval and adoption boundaries. Cross-workspace feedback can address distillation, organization, applicability, or verification. A specific local design rule does not automatically enter this specification. Adopt actual versions explicitly; new shared drafts do not silently change local rules or pins.

Authority: D:design-spec. The D index records the file and actual bytes. Review triggers are in the metadata.
