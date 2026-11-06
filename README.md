# Repolex Knowledge Graph of ansible-community/antsibull-docs-loader

RDF knowledge graph data for [ansible-community/antsibull-docs-loader](https://github.com/ansible-community/antsibull-docs-loader), parsed by [repolex](https://repolex.ai).

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
rlex download ansible-community/antsibull-docs-loader
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── f6f58f89cb22a293b69c905d44f963bbba20a558
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── f6f58f89cb22a293b69c905d44f963bbba20a558
│           └── chunk-001.nq.gz
├── blob
│   ├── 025f9be18baaf8ffe58777d98d87787f313efbfd.nq.gz
│   ├── 0b2a0dee3944e99157b674f26e618bacf9a36c1c.nq.gz
│   ├── 0f5584739274f7d01d4afdbdc86c2b04c2155865.nq.gz
│   ├── 11f72e9fdc5429da687696227aa471a25de4491e.nq.gz
│   ├── 1a04d58405be1473e4378b50b09e889ec8baf3af.nq.gz
│   ├── 23898dc4da45e6b1f1d99d9e11caa01f20d1ba0c.nq.gz
│   ├── 29588eb30c4d53b1c108aaa4e44682a70b4b5978.nq.gz
│   ├── 335aa76a663da0f13cddab3ab759545172d5ef10.nq.gz
│   ├── 5b88fbeb398ce2bb787c69c3ac4bbcbaf1919c62.nq.gz
│   ├── 5ee7812edbb236187b2434d8d01342f71c10b922.nq.gz
│   ├── 6228b395aac801a04376a4e5e2fab1c75210d9dd.nq.gz
│   ├── 8b90c04c4867e9b6dcdf6296e0860de9fc0946a3.nq.gz
│   ├── 91c1918e7f727f022e2b0b095832b7483a0e2068.nq.gz
│   ├── 9b54d4bb3db3c412b0249ece8cc8c341dc2b84bb.nq.gz
│   ├── a44a6754b442e746654a6172a922517e4232bde3.nq.gz
│   ├── a9d8dd99ce76d5e1b148603d0c0d30f00d32f740.nq.gz
│   ├── ab115f1754b89cdb3606e40de409fabc37fb174d.nq.gz
│   ├── b4aaeb15545e86fac367127a5e66146dfa8077f9.nq.gz
│   ├── b5f56f101ec4fc56852f0b4cc3120371b85c3bcc.nq.gz
│   ├── c6b8d51fe3980c1c4bd2f9645b6c3d75952fec10.nq.gz
│   ├── c6ecdfd6ddaacf56bf6ac88b409bf5c5ec755da5.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ea5b60640b01f74e295037aa8a6b7d4ea278a739.nq.gz
│   ├── f079ad06624a975d6cabb72feeef8466b2ebcb87.nq.gz
│   ├── f288702d2fa16d3cdf0035b15a9fcbc552cd88e7.nq.gz
│   ├── f39beccebb9d899756154e9968d844ebe786a0ae.nq.gz
│   ├── f57975c8b9557a5f83f34ce040088e91d4b79873.nq.gz
│   ├── f71b322d2aabd560774185ebb7c3fec99c47ef3e.nq.gz
│   └── fe6449a5addb50bc83b72e9689f7aab91a6774f2.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── f6f58f89cb22a293b69c905d44f963bbba20a558.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 36 files
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

[ansible-community/antsibull-docs-loader](https://github.com/ansible-community/antsibull-docs-loader)

---
*Parsed on 2026-11-06 by [repolex](https://repolex.ai)*
