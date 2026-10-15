# Repolex Knowledge Graph of jupyterhub/tmpauthenticator

RDF knowledge graph data for [jupyterhub/tmpauthenticator](https://github.com/jupyterhub/tmpauthenticator), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [rlex](https://github.com/repolex-ai/rlex) query tool:

```bash
cargo install --git https://github.com/repolex-ai/rlex
```

Verify the install:

```bash
rlex --help
```

**rlex is designed to be used primarily by LLMs in a terminal.** Start up your favorite AI assistant and ask it to use rlex. It handles the SPARQL — you just ask questions in plain English.

To load this repo's data:

```bash
rlex download jupyterhub/tmpauthenticator
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 49cb1fb144a06e03dfab835f76e8fc5b222446b1
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 49cb1fb144a06e03dfab835f76e8fc5b222446b1
│           └── chunk-001.nq.gz
├── blob
│   ├── 0a0797613125ee4d5ca00adbf4b11815a0b9684b.nq.gz
│   ├── 0fa3c1bfb9335c617be0880dd4b86c9c6e13aba7.nq.gz
│   ├── 12cb69964652728498563e40ad54899b7f5bb0ee.nq.gz
│   ├── 1f555865ed386b171948c1d7d5599b516e82810a.nq.gz
│   ├── 246a778090c0aaa0fd1ba743f916d1de5877ace5.nq.gz
│   ├── 670699624ab0ee9c8818b2dae5c1a47277c93633.nq.gz
│   ├── 859e44d4214aac2be96e086054ff68a492ac625e.nq.gz
│   ├── 8e6c3273b9ef8a299eafe1f53ece997153e5ef23.nq.gz
│   ├── ab98d28ee2f5ddf92365c67e536715a62e48b8c2.nq.gz
│   ├── e6053d685383a51e0a408455bea2bbdee96ff586.nq.gz
│   ├── eea4b73e6824102d14f6170c3cb7ffbb9561bb34.nq.gz
│   ├── f0450bed7402942d6916ae459b77a246f873e92f.nq.gz
│   ├── f3cae140156c444142c961ea53aff87c9b844e1b.nq.gz
│   ├── f4b5bcdb85ab89726c1f6dc274504d4f7b359dea.nq.gz
│   ├── f88339c48a75da588abc35e6854151ff82f9ab56.nq.gz
│   └── fcd32a86cdc02c6b62a3a00130ed54afc06c9c3c.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 49cb1fb144a06e03dfab835f76e8fc5b222446b1.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 24 files
```

| Directory | What it contains |
|-----------|-----------------|
| `blob/` | Per-file AST graphs, content-addressed by git blob SHA. Each file in the source repo gets its own graph. |
| `aggregate/ast/` | Combined AST graph per parsed commit. Merges all blob graphs for a snapshot of the entire codebase at that point. |
| `aggregate/lsp/` | Language Server Protocol enrichment: resolved symbols, definitions, references, and type information. |
| `aggregate/dataflow/` | Interprocedural data flow edges between functions and modules. |
| `aggregate/repolex/` | Combined graph (AST + LSP + dataflow) per commit. |
| `commit/` | Git commit metadata (author, date, message, parent links). |
| `branch/` | Branch metadata. |
| `tag/` | Tag metadata. |
| `filetree/` | File tree snapshots per commit (which files existed and their blob SHAs). |
| `audit/` | Code architecture and graph audit reports per commit. |

## Source repository

[jupyterhub/tmpauthenticator](https://github.com/jupyterhub/tmpauthenticator)

---
*Parsed on 2026-10-15 by [repolex](https://repolex.ai)*
