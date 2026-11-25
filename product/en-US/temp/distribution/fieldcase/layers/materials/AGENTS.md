---
id: materials-governance
updated: "2026-11-17"
recheck: Changes to ownership, production scope, admission, source licensing, or repository layout
---

# Materials layer rules

## 1. Ownership and permissions

- Enter from M in the root INDEX. Root rules §1–§2 govern work modes and execution authorization. Use the user-designated maintainer or the root maintainer when no other is named. Enabling M does not create an agent.
- This layer's INDEX is the single entry for production materials. D:index-spec owns indexing, fixed sources, and reading; D:handoff-spec owns versions and consumption records.
- There is one named writer at a time. Before production, define the object, writable scope, purpose, source, and delivery criteria. Check existing edits on takeover. Do not overwrite, stage, or commit another party's work.
- Consumers read approved materials only. Referencing, downloading, generating, or receiving a suggestion is not formal admission or write authorization. Keep candidate content in the task's approved T location. After approval, the authorized maintainer brings it into M.

## 2. Production and admission

- M holds brand, content, design, and other actual production materials. Put unfinished assets, intermediate artifacts, and discardable conversions in the right T category; put reference snapshots in R. A filename extension does not determine ownership.
- Before adding or replacing material, explain provenance, purpose, use conditions, actual gaps, and affected references. User and third-party content retains its own rights. Network retrieval, generation services, and external sending need corresponding authorization.
- For governance, specifications, and index structure, submit a complete draft or diff and MVD measurement first. Implement file bodies under the actual approved plan. Editing material does not change root rules, business requirements, or other workspaces.
- Formal material is usable locally and has a reachable entry. Keep required provenance and restrictions in the existing index or material entry, without pre-creating a dedicated record. An empty layer does not need fabricated brands, content, or sample projects.
- Check files, their index, actual byte counts, and active references together. Keep a stable ID when moving the same object. Delete, migrate, or clean up only within explicit scope. Preserve the identity of an old final version.

## 3. Repository, handoff, and maintenance

- With local Git enabled, track M governance and its overall index in the owning workspace repository. Leave material content outside by default and maintain it under the relevant task authorization. Tracking material content requires an approved path inventory. Use the actual repository and approved version and branch rules. Keep `layer_version` only in the layer INDEX.
- Commit by exact paths and verify ownership first. State the real limits without Git. Keep fixed references and consumed commits reachable. An amendment or cleanup cannot invalidate consumption records.
- Keep task facts, remaining work, and evidence in the responsible session's existing HANDOFF. Do not create a separate M handoff or edit consumer records. Layer updates do not switch users to a new source automatically.

## 4. Authority and review

M:materials-governance is the authority for this layer's distinct production, admission, and maintenance rules. M INDEX owns the actual entry. Changes require corresponding approval and execution authorization. Review triggers are in the metadata.
