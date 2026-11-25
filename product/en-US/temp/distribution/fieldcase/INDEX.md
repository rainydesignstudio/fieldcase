# fieldcase distribution materials index

Paths are relative to this index. In a local T, enter fieldcase through T:distribution. If a shared T has no such category, use the registered D:distribution entry. Do not add a parent category.
Materials version: 0.1.0.0. The English materials derive from `fieldcase-zh-dt-04`. The English contract specification includes localized status labels. Use §1 and §5 of the README at the same fixed resource root for the pack batch and test coverage. Use the fixed inventory for exact material revisions.

The pack contains 12 core files and 10 files for K, R, M, and modules, 22 in all. D specifications live in the local `docs/spec`; K is optional for knowledge needs. A shared version number does not establish compatibility with an older K/T core or `rule-*` entries. Verify the exact source, language, and retained scope; the version number alone cannot fix the content.

## 1. Use

Read `adoption` before opening the originals selected by the user. Having the files does not mean they are adopted or running. Install only the selected working files in local D or the actual data layer under the complete approved plan. Update indexes and byte counts, supporting files, and the exact source.

K, R, and M are optional data layers and do not go in `config.modules`. The three module methods can be installed on D and T. Formal knowledge output requires an approved K destination; separately fetched raw material can go in T if authorized. No business library, external tool, or unavailable skill is bundled. Installation does not start network activity, communication, a Goal, or a heartbeat.

## 2. Fixed materials

| # | ID | Name | Type | Entry | Size | How to use it |
|---|---|---|---|---|---|---|
| 1 | <a id="adoption"></a>adoption | Layer and module adoption | Guide | [Adoption](ADOPTION.md) | 30654 B | May read in full; covers D/T core, data layers, modules, and upgrade boundaries |
| 2 | <a id="knowledge-governance"></a>knowledge-governance | K governance original | Template | [K rules](layers/knowledge/AGENTS.md) | 6273 B | Applies after local K adoption; a shared library retains its own rules |
| 3 | <a id="knowledge-index"></a>knowledge-index | K index original | Template | [K index](layers/knowledge/INDEX.md) | 2070 B | For local K only. Do not replicate local management rules into K |
| 4 | <a id="r-index"></a>r-index | R index original | Template | [R index](layers/references/INDEX.md) | 3037 B | Use after selecting R. No reference business content included |
| 5 | <a id="m-governance"></a>m-governance | M governance original | Template | [M rules](layers/materials/AGENTS.md) | 3536 B | Use after selecting M. Actual governance determines permission |
| 6 | <a id="m-index"></a>m-index | M index original | Template | [M index](layers/materials/INDEX.md) | 1923 B | After adoption or customization, check the layer's actual governance byte count |
| 7 | <a id="cache-spec"></a>cache-spec | Acquisition method original | Template | [Acquisition specification](modules/knowledge-acquisition/docs/spec/cache-spec.md) | 8071 B | With adoption §3; the working destination is local D/spec |
| 8 | <a id="contract-spec"></a>contract-spec | Contract method original | Template | [Contract specification](modules/cross-workspace/docs/spec/contract-spec.md) | 6869 B | With adoption §4; the working destination is local D/spec |
| 9 | <a id="contract-index"></a>contract-index | Empty contract index original | Template | [Contract index](modules/cross-workspace/temp/contract/INDEX.md) | 702 B | Adopt only with authority over local T. Do not overwrite a shared T. Read only the active entries by default |

This is an inventory of originals and actual bytes, not installed state. Use D references for working specifications only after actual installation and registration. Data layer IDs resolve only after their root entries are registered.

## 3. Choices and dependencies

| Choice ID | Purpose | Installation prerequisites or runtime dependencies | Supporting material |
|---|---|---|---|
| knowledge | K knowledge base | Root plus D and T; choose local, shared, or imported K | adoption §2; knowledge-governance and knowledge-index |
| references | R references and evidence | Root plus D and T; choose R | adoption §2; r-index |
| materials | M production materials | Root plus D and T; choose M | adoption §2; m-governance and m-index |
| knowledge-acquisition | Fetch, convert, index, and optional verify | D and T can host the method; choose the K target before producing formal knowledge | adoption §3; cache-spec |
| cross-workspace | Contracts, contact, and dispatch | D, T, and an authorized contract entry; verify communication capability and authorization separately | adoption §4; contract-spec and contract-index |
| unattended | Unattended work, continuous iteration, and optional retry extension | D and T; check host capability, scope, and completion conditions | adoption §5; no new permanent file |

Write the module source in `config.modules` only after completing and checking all supporting changes. An inherited mode is not a local module installation, and not installing it does not remove the parent rules already in force. Project skills are not supplied; the all-modules preset does not imply a wrapper exists.

## 4. Maintenance and cleanup

Before updating, verify the fixed identity, compatibility, dependencies, supporting files, and byte counts. Do not assemble material from moving branches. Changes to D references, optional K, and simplified recovery cannot inherit a pass from old tests. Formal distribution still requires matching verification and verified sources.

Treat non-adoption, deactivation, removal, and cleanup separately. Updating or deleting a config entry does not authorize removing old originals, unique evidence, recovery sources, or rules in force. Use D:agent-guide when resources are missing; do not invent a source.

This index owns the group's entries and compatibility information. It authorizes no installation, retrieval, sending, commit, or publication. Review it when sources, batches, paths, choices, supporting material, or compatibility change.
