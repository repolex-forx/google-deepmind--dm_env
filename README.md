# Repolex Knowledge Graph of google-deepmind/dm_env

RDF knowledge graph data for [google-deepmind/dm_env](https://github.com/google-deepmind/dm_env), parsed by [repolex](https://repolex.ai).

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
rlex download google-deepmind/dm_env
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 91b46797fea731f80eab8cd2c8352a0674141d89
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 91b46797fea731f80eab8cd2c8352a0674141d89
│           └── chunk-001.nq.gz
├── blob
│   ├── 09749542e90fe8cc92a2b79d1ff64d074c778f15.nq.gz
│   ├── 0dc989a407be89b857baabfa80a512509290bc40.nq.gz
│   ├── 123f7890144038deb428dc39f0e3c18c4607007a.nq.gz
│   ├── 1785412bb7716e357cbfb21909bb82e2de3a73c8.nq.gz
│   ├── 1aba38f67a2211cf5b09466d7b411206cb7223bf.nq.gz
│   ├── 30452b0f4d6e48a784cb0b2b911307a89cd08d59.nq.gz
│   ├── 363a4e2e9f1468b2bbbb082f11d6b717f5a4f3eb.nq.gz
│   ├── 37ed80ad11e501b791193193b7cd22a546b70e7e.nq.gz
│   ├── 3a12abc8bf91ab212730949edab9581acb08c369.nq.gz
│   ├── 5c8ec9c760ac41cb1eba50eae81c8ac6c5eae922.nq.gz
│   ├── 5ce49418f08d700ceac2c1ab690f9c59034051b5.nq.gz
│   ├── 628c73c662237e484a28b8d8cdfcf5840507440e.nq.gz
│   ├── 63a243e91c3d11e60f65c0f3bf6f8ea58298d1e5.nq.gz
│   ├── 6b3ef5c52a68b64335a9f1e60b652b22eb276294.nq.gz
│   ├── 763ed8f08a154a74967d73497358b34e4a42f875.nq.gz
│   ├── 7a4a3ea2424c09fbe48d455aed1eaa94d9124835.nq.gz
│   ├── 7e701dc51ebb2a65f27030f7fe69fceae3c78965.nq.gz
│   ├── 807c1e4b99029513df2ecd11abf595271d5c223e.nq.gz
│   ├── 8d9ce9599ca4b508aefc983cfe87fd69990dc665.nq.gz
│   ├── b05528ca10f2f427624840e9fe73633556e95acb.nq.gz
│   ├── c0467d3ebc62e933565d3436eea384d1f9ea4c3b.nq.gz
│   ├── c5a47246d9954aad8fa325738b09d3a131c3c7d1.nq.gz
│   ├── c5a660b03d697d9fcb1c0aa63b886a5c1edd4832.nq.gz
│   └── e81473136970ff925c99a58a9ed0854b1d672c07.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 91b46797fea731f80eab8cd2c8352a0674141d89.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 32 files
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

[google-deepmind/dm_env](https://github.com/google-deepmind/dm_env)

---
*Parsed on 2026-11-06 by [repolex](https://repolex.ai)*
