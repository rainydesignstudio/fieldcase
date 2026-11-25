<h1 align="center">fieldcase</h1>

<p align="center"><strong>Workspace rules that agents can follow across sessions.</strong></p>

<p align="center">Open-source workspace governance. Rules, authorization, progress, and pending work live in local files.</p>

<p align="center">
  <a href="README.md">简体中文</a> ·
  <a href="#quick-start">Quick start</a> ·
  <a href="#packs">Packs</a>
</p>

<p align="center"><code>0.1.0.0</code> · <a href="LICENSE">MIT</a></p>

<picture>
  <source media="(max-width: 720px)" srcset="cover/r4/fieldcase-banner-compact.png">
  <img src="cover/r4/fieldcase-banner.png" alt="Fieldcase · 行匣. Side light falls on a silver sleeve and five frosted index plates.">
</picture>

## Quick start <a name="quick-start"></a>

1. Pick a language pack and get its ZIP and matching manifest. Compare the ZIP’s SHA-256 with the manifest, then unpack it into a separate directory.
2. Give the agent the unpacked README, the target workspace directory, and one small thing you want to do.

```text
Read this pack README. The target workspace is <target directory>. I’d like a one-page note showing people where to begin.
```

The agent checks the target and plan, then writes with your authorization. The host needs read and write access to the chosen local directories. If you choose Git, you need it installed locally.

## Packs <a name="packs"></a>

Once 0.1.0.0 is published, open it under **Releases** in the project’s GitHub repository. Get the ZIP and verification manifest for the same language, then compare the ZIP’s SHA-256 with the manifest’s `archive_sha256`. Each language pack works independently.

<details>
<summary>Check release-01 filenames</summary>

| Language | ZIP | Verification manifest |
|---|---|---|
| Simplified Chinese | `fieldcase-0.1.0.0-zh-CN-release-01.zip` | `fieldcase-0.1.0.0-zh-CN-release-01-manifest.json` |
| English | `fieldcase-0.1.0.0-en-US-release-01.zip` | `fieldcase-0.1.0.0-en-US-release-01-manifest.json` |

</details>

## When to use it

| Scenario | How to start |
|---|---|
| **🌱 Start from scratch** | Approve a charter in an empty target and begin with one small task. |
| **📦 Copy into a new workspace** | Keep the source and align directories, rules, and entry points in a separate target. |
| **🤝 Take over an existing workspace** | Give a new session the instance directory. Use the current handoff to recover rules, authorization, and remaining work. |

## Source and test coverage

The product sources are in [Chinese](product/zh-CN/) and [English](product/en-US/).

First-release trials covered starting from an empty directory, copy migration, in-place adoption, and handoff to a new session. See §5 of each pack README for the scope of those trials. The agent starts with the pack README and follows its entries to `AGENT-GUIDE.md` and the active specifications.

[MIT License](LICENSE) · Copyright 2026 Rainy
