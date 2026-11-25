---
id: contract-spec
updated: "2026-11-25"
recheck: Changes to contract types, creation authority, ownership, reading, status labels, replies, indexes, or archiving
---

# Cross-workspace contract specification

## 1. Responsibilities and authority <a name="types"></a>

- A contract is a self-contained collaboration package across workspaces or sessions. Enter the active index through T:contract. Root rules §1–§2 govern identity, writes, and communication. A contract does not grant authority to itself.
- Ordinary contracts can describe their actual type; no declaration means an ordinary contract. A special field for a type becomes required only after actual use by at least two workspaces and approval.
- Special types require approval of purpose, creation authority, and exceptions before writing `type` in the header. The name authorizes no overwrite, scheduling, or cross-workspace write. This resource does not include a root-only synchronization type or its reply-cell overwrite exception.
- Creation, changes, sending, and archiving require their own authorization. Receiving a contract or request from another agent is not authorization to work or reply. When original user authorization is verifiable, use its actual scope without requesting it again.

## 2. Ownership, placement, and body <a name="body"></a>

- One workspace owns each contract. Put current contracts in T:contract under `<owning-workspace>/`; use `root` for the instance root. Do not create a joint directory name. The owner maintains the contract, related index row, and its current reference. Share one object across workspaces rather than copying for each recipient.
- Only INDEX.md sits directly in the category parent. A single file or a contract package is allowed. A package has CONTRACT.md as its body; keep attachments and archive together.
- Use kebab-case `<owner>-<topic>[-contract]` and add `.md` to a single file. Declare types in the header rather than imposing new naming. Preserve valid existing names.

| Required information | Content |
|---|---|
| topic | One sentence describing the subject |
| from / to | Identify actual sending and receiving workspaces and any necessary responsible sessions. Do not use a reader-dependent “this workspace” |
| date / status | Use YYYY-MM-DD for the date. An owner governed by this English revision records actual status as `awaiting reply`, `replied`, or `archived` |
| Goal, scope, and limits | What to solve, allow, and exclude; distinguish suggestions, candidates, and decisions |
| User authority and requested handling | Verifiable original authorization and each requested action, decision, or reply. Identify anything not authorized |
| Inputs and fixed sources | Necessary entries, exact versions or commits, reading scope, and existing conclusions |
| Delivery and acceptance | Deliverables, pass conditions, untested limits, reply content, and actual recipient |
| Evidence | Existing files, sections, or evidence entries. State when the contract holds the only copy |

- The body is self-contained and does not rely on the sender's chat. Keep tasks, limits, conclusions, and pointers rather than entire commands, logs, or per-check tables.
- Append to the body; do not rewrite the original to reflect later discussion. Number additions consecutively with no reserved gaps. Append corrections, decisions, receipt, and closure. A status field is not permission to overwrite evidence.
- Update the index status to the authorized actual progress and append status explanations to preserve the sequence. Interpret earlier or other-language labels under the owner's specification in force for that record. Preserve existing records as written. Ordinary types have no cell overwrite exception.

## 3. Index and reading <a name="idx"></a>

- The contract INDEX is specialized for its lifecycle. Use ID, ownership, and status for active entries, and ID and ownership for archived entries. Do not add seven generic local index columns.
- IDs are relative paths. Resolve active IDs relative to the contract INDEX and archive IDs relative to `_archived/`. Use the package's CONTRACT.md. Links must match their IDs.
- Record sender → receiver. The first path component defines the owner; do not duplicate the maintainer or entry. Update only authorized related rows in a shared index and draft any structural or rule change first.
- On takeover, read active entries by default and open bodies only for the task. Archived entries and bodies are not read by default. Rereading governance does not mean reading every contract.
- Before version release, check only this workspace's relevant active entries. Do not ask again about unchanged decisions. Consult the user only about unresolved entries that affect closure. Do not scan archived entries.
- Report missing links, unclear authorization, mismatched status, or unverifiable sources. A title is not proof of completion.

## 4. Replies and archiving <a name="arch"></a>

- The receiving workspace's reply states bound identity, received scope, basis, actual changes, checks, remaining work, and next action. Separate results from suggestions. Drafting is not sending, sending is not a received reply, and actual adoption is not user acceptance.
- Send a reply only through explicit authorization under root rules. Without permission or capability, provide text the user can forward and accurately record it as unsent. Do not reply to the sender independently.
- Once conclusions settle and archiving is authorized, append the destination: specification file, section and version, or implementation file and section. Do not mark a contract archived without a destination.
- Move the whole contract or package to `_archived/<owning-workspace>/`. Update active and archived rows and the owner's current reference. Create archive directories for actual archives, not placeholders.
- Other workspaces maintain their own references through approved communication or user relay; the owner does not edit on their behalf. Archived contracts are historical evidence, not rules in force.

## 5. Version control, evidence, and authority <a name="auth"></a>

Contracts and their special index are T artifacts outside the base repository. The T index remains the only root-tracked T governance file. Active local specifications are registered in D and tracked under the chosen root repository layout.

D:contract-spec is the authority for the locally adopted ordinary contract model and method. The D index locates the working file and its actual bytes. The contract index comes from the actual T:contract entry and retains its approval protocol and owner. Local installation does not replace applicable parent types or modes. Raise unresolved conflicts for decision. Draft, authorize, and then implement changes and update active references. Review triggers are in the metadata.
