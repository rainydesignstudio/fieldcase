---
id: cache-spec
updated: "2026-11-17"
recheck: Changes to retrieval or conversion tools, source structure, content indexes, cache ownership, or production approvals
---

# Knowledge acquisition and cache specification

This specification covers fetching, conversion, indexing, registration, and consumption of external material. It does not define the business content. Locate the method at D:cache-spec, use the root rules for permission and D:index-spec for sources and protection. Approve the actual destination through its K entry and owning governance. Do not assume all shared K uses the same governance ID.

Install module rules without creating K if appropriate. A task that only fetches raw material may use T by authorization. For formal knowledge output, identify an approved K target and register under its real protocol. Without a target, do not claim a complete knowledge base or create an empty layer to install the method.

## 1. Raw material and usable output <a name="split"></a>

- Put raw material and tools under `knowledge/<category>/<library>/<batch>/` in T:cache. Resolve the actual path through the T index. Create only the approved paths and do not track these in the base repository.
- Put output in the approved K library. Use the chosen repository if Git is enabled. Without Git, output still needs to work locally, with the lack of history and fixed snapshots stated.
- Decide ownership by whether the tool plus the indexed source URL or fixed commit can recreate it. Cache rebuildable raw material whose necessary sources stay available. If recreation depends on something outside the instance's control, retain the consumed files as output. Admit nonreproducible research or gap findings as output.
- Leave disposable fixtures, sample pages, source assets, and build products with the raw material. Retain official comparison originals, recovery snapshots, and unique evidence under their own rules, rather than as cache.
- For a Git source, its `.git` may stay with the authorized raw copy for targeted queries and consistency checks. It is a source snapshot, not initialization of a separate base repository for T.
- Do not bulk-restructure curated libraries or assume an SDK, site, or stack toolchain. Propose a suitable plan for unusual sources.

## 2. Output and paths <a name="files"></a>

- Group libraries by technology, platform, or source as appropriate. Use recognizable kebab-case names. The K index owns actual entries; do not infer them by path depth or extension.
- Use one Markdown file for each documentation page, next to the corresponding `index-partNN.json` file. Do not create a second directory for content or duplicate it to satisfy multiple entries.
- In a snapshot library, keep the actual documentation or code needed, unchanged, located by the local index. Links back to the cache or web are not a substitute.
- Keep a README, manifest, GAPS file, or verification report only when an existing entry cannot hold necessary information. They are not a required file set.
- Keep provenance, fixed versions or commits, scope, license facts, and necessary external links in the content index or existing library entry. Do not duplicate that metadata in every Markdown file.

## 3. Content index <a name="idx"></a>

- Use `index-partNN.json` files split for actual size and access. An index locates local content and records provenance and links. Do not transform body text while indexing.
- Each item has at least `title`, `markdown_path`, and `source_url`. Keep links removed from text in `external_links`. Resolve `markdown_path` relative to the index; it must point to actual local content. Snapshot items may use it for unmodified files.
- Add fixed commits, reading limits, and other fields only for actual navigation needs. Describe library search, shard scope, and restrictions in the K index's reading instructions.
- Indexed material must be readable locally. Missing body text is a gap. A summary, web link, or refetch instructions do not complete a knowledge page.

## 4. Production and tool approval <a name="tools"></a>

- Produce as needed. Name one producer per library at a time; consumers read only. Determine source, scope, destination, tools, and network actions first, and get task authorization.
- For first adoption, confirm the fetch, convert, and index toolchain with the user at each stage. Show tools, parameters, output, observations or samples, and known gaps before choosing the next stage. Running a sample also requires execution authorization.
- With the same approved tools and strategy, the selected steps may run within one execution authorization. Changes to tools, source structure, conversion, or indexing strategy require identifying affected stages and reconfirming those, not all unrelated checks.
- Fetch obtains needed originals and records provenance and missing items. Convert turns documents into Markdown and keeps code unchanged, based on actual content. Do not assume site member lists or discussion areas. Index uses local content without converting or copying it again.
- Verify is optional. Each time the user requests retrieval, ask before work whether to verify this time. Obtain an answer; do not reuse a previous choice. Run only the selected verification and scope.
- Skipping optional verify does not lower the #accept usability standard or establish that verification ran. Record the choice, stage approval basis, and gaps in existing handoff or the library entry rather than making a permanent record file.
- Keep tools with the raw material and register their entries. A single tool may cover multiple stages. Pass the resolved target explicitly; defaults are not authorities. Report missing tools or network permissions before proceeding; do not install external skills, services, or runtimes automatically.

## 5. Content and acceptance <a name="accept"></a>

- Use Markdown headings, lists, tables, and code blocks for documentation. Remove page styling and rendered HTML. Put code examples in code blocks.
- Keep document text free of external links and remote dependencies. Change internal links to local relative paths and anchors. Retain text for other links and put URLs in the index. Include necessary images or attachments locally if they can be lawfully obtained. Deleting links alone does not complete them.
- Preserve code files unchanged, including links that are part of the source. Do not apply document conversion rules to code. State required dependencies and what did not run.
- Basic acceptance requires locally usable, self-contained content that works offline. Check selected body text, paths, references, and provenance. Treat required material not obtained or not usable locally as a gap. An index alone is not completion.
- Retain existing rights and licenses for migrated and third-party material. Obtain only the approved scope. The base MIT terms do not replace source requirements.

## 6. Registration, failures, and maintenance <a name="prod"></a>

- Handle new libraries, moved entries, files, and protection changes together under D:index-spec and K admission. Provide a fixed consumption source only after actual content and registration are complete.
- On failed retrieval or incomplete content, use existing handoff or the library entry to record missing items, impact, attempts, and conditions to resume. Do not substitute search summaries or label unfinished output as consumable.
- Use existing libraries as registered. Bulk rename, migration, cleanup, or rebuilding needs explicit task authorization. Rebuilding the raw cache is not permission to overwrite formal output.

## 7. Authority and review <a name="auth"></a>

D:cache-spec is the local authority for knowledge acquisition. Install the working file in D/spec, with actual path and bytes in the D index. The root rules govern authorization and the owning data layer maintainer admits output. Installing locally does not take over a parent K. Draft and obtain execution authorization before changing this specification. Review triggers are in the metadata.
