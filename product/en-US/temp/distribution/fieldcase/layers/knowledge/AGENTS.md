---
id: knowledge-governance
updated: "2026-11-17"
recheck: Changes to knowledge admission, content scope, index protocol, ownership, sources, or repository layout
---

# Knowledge layer rules

## 1. Ownership and entry

- Use K only when there is a knowledge base need, through the root K entry. Create one locally, use an existing shared K, or import from an approved inventory. Do not require an empty K for the minimal workspace. Adopting K does not create an agent; the user names its maintainer.
- All local management specifications live in D, not K. The root rules govern modes and permission; D:index-spec governs indexes, sources, and protection; D:handoff-spec governs versions and consumption records. This file owns only K-specific responsibilities.
- A local K index maintains knowledge, tools, and needed local indexes. An external K retains its actual protocol, version, location, and ownership. Do not overwrite provider INDEX or AGENTS. Applicable provider rules keep their authority; residing in K does not make them reference-only.
- There is one named writer at a time. When taking over, check authorization and existing edits. Do not overwrite, stage, or commit someone else's work. Access, finding an issue, or receiving a message grants no write permission.
- Establish import source, scope, target, and permission first. Preserve the source by default. Actual copying, moving, repository actions, or reference changes must be within authorization. Reuse authorization already granted; adoption of a knowledge base does not authorize deleting the source or editing an external repository. Moving D does not clear existing business knowledge or valid references to it.

## 2. Admission and production

- Each formal knowledge item needs locally readable content, a real entry, and necessary provenance and use restrictions. Search summaries or links to retrieve content again do not substitute for the actual knowledge page. Keep usable structures and local protocols. Draft structural changes first.
- Maintain content, index, actual bytes, and active references together. IDs are stable across moves. Protected governance and spec directories require complete membership and per-file bytes; do not create an empty index for every ordinary directory.
- Matching byte counts do not prove unchanged content. Changes still require approval and source checks. Do not invent an index diff if its record did not change. Missing content or source does not pass.
- Keep reproducible raw material and tools in the T cache. Keep nonreproducible research, gap findings, and actual dependency files as knowledge after approval. A curated knowledge base does not require automated acquisition.
- When adopting knowledge acquisition, use D:cache-spec for production, the first toolchain approval, and per-job optional verify. Module rules can be installed first. Raw acquisition alone may use T if authorized. Formal output requires an approved K target. Installing a method does not start a network request, install tools, or grant shared write access.
- User and third-party material retains its own rights and licenses. The base license does not automatically apply to data. Preserve necessary licensing facts with the source; do not copy unapproved resources.

## 3. Consumption and contributions

- Use config for the default strategy. Use one data table in the consuming HANDOFF for the actual K source. Fix the source when starting work or explicitly switching it; resume from the same commit or reliable copy. Use the index, membership, and content from the same source. Do not follow a moving branch silently.
- Distinguish no local repository from no Git at the source. Use a fixed external source within its actual guarantees; state the limits when local content has no history. When a directory view is needed, use the approved T path instead of switching the maintainer's worktree or pre-creating every version.
- Record development and formal adoption separately, and distinguish comparison from actual candidate trials. A trial adds scope and the prior dependency to the same row. Stable formal directories and development in a T worktree require shared repository history, branching capability, and authorization. Do not claim these with no Git or direct main.
- Without write permission for formal K, prepare a candidate in the task's approved T location for an authorized maintainer. It is available for consumption only after review, supporting changes, indexing, and a real fixed source. Review is not admission. Layer updates do not automatically upgrade consumers. Do not update their handoff or send messages on their behalf.

## 4. Repository, versions, and repair

- Check K's tracked scope against the approved inventory and its actual owning repository. Preserve external repositories. Store `layer_version` only in this index. K does not hold D specifications. Moving D does not authorize merging, removing, or rebuilding an existing layer repository.
- D:index-spec#identity defines content identity. With no reliable fixed baseline, use `development`; explicit approval and a reliable fixed reference are required for `baseline`, and actual version release for `released`. These do not replace the three workspace lifecycle states. Keep consumed commits reachable and fixed tags unmoved.
- Commit by explicit paths. Use the root rules and D:handoff-spec for version increments, the same first-version number, main's starting point, version release, and history. A T worktree belongs to the original repository; it does not make T an independent repository.
- Report source, type, entry, membership, or byte-count mismatches under D:index-spec. Consumers do not edit counts to suppress errors. Authorized maintainers verify cause, draft, implement, and check repairs. An old index is not proof of new body text.
- Use explicit root authorization for repair exceptions. `enforce=false` does not make missing sources, files, or permissions valid. Record repairs and layer changes in existing handoff. Other workspaces own their references and pins.

Authority: K:knowledge-governance, reached through the actual K index. Review when the conditions in the metadata change. Until adopted, this file is a fixed distribution original only.
