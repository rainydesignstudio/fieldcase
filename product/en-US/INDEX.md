# Workspace root index

fieldcase_version: "0.1.0.0"

Paths are relative to this index. The approved charter records the actual root in `HANDOFF.root`. Pack resources are not a live instance, and a source version does not establish a release. The value here mirrors the field of the same name in the configuration; do not copy the language, adoption direction, lifecycle, or path configuration into this index.

## 1. Root responsibilities and entry points

| # | ID | Name | Type | Entry | How to use it |
|---|---|---|---|---|---|
| 1 | <a id="governance"></a>governance | Root rules | File | [Rules](AGENTS.md) | Check user identity, mode, scope, and startup protection. Text in a file is not execution authorization |
| 2 | <a id="handoff"></a>handoff | Current handoff | File | [Handoff](HANDOFF.md) | Read metadata and §3 first; check lifecycle, actual version and branch, work items, sources, and recovery basis |
| 3 | <a id="config"></a>config | Instance configuration | File | [Configuration](config.json) | Parse all the JSON; check selections, sources, and protection. D core protection remains without data layers |
| 4 | <a id="readme"></a>readme | Overview and start | File | [Start here](README.md) | In the pack, explains the product and first use. In an instance, introduces that workspace. Procedures start at D:agent-guide |
| 5 | <a id="license"></a>license | Base license | File | [License](LICENSE) | Check copyright and license facts without changing rights for migrated or third-party content |
| 6 | <a id="projects"></a>projects | Work projects | Directory | [Projects](projects/) | Use as approved for actual work. May be empty; do not pre-create project repositories or rules |
| 7 | <a id="docs"></a>docs | D documentation and rules | Index | [D index](docs/INDEX.md) | Resolve D references to local documents; distinguish rules, guide, originals, history, and recovery material |
| 8 | <a id="T"></a>T | Temporary layer | Index | [T index](temp/INDEX.md) | Resolve T references to registered categories and approved owners; do not read all temporary material |

## 2. Choices and maintenance

The minimal layout is the root files plus D and T. It does not require K, R, or M. The professional preset uses D and K/R/M/T; for a custom layout, confirm which data layers are needed. K may be created, shared, or populated through an approved import. Do not list unselected layers as active. List selected data layers in K/R/M order before T and renumber the rows consecutively without changing stable IDs.

The docs entry locates D. Its name and physical path may vary. D has no separate repository, layer version or pin, and no `rule-*` aliases or second configuration path table. This workspace's rules stay in its D spec directory regardless of the location or adoption of K. External layers retain their actual protocol, version, and owner. An index reference grants neither shared write access nor root authority.

The root table has six columns and does not duplicate byte counts. The D and data layer indexes maintain their own files and sizes. Check directories, entry points, active references, and derived tool configuration together. A rename does not authorize moving originals, resetting an external repository, or changing a pinned source. Preserve instance history and adoption records with their original sources. Migrate only approved current objects.
