# Repolex Knowledge Graph of asimov-platform/asimov-chrome-extesion

RDF knowledge graph data for [asimov-platform/asimov-chrome-extesion](https://github.com/asimov-platform/asimov-chrome-extesion), parsed by [repolex](https://repolex.ai).

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
rlex download asimov-platform/asimov-chrome-extesion
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 6542efc7261aaba3b784406e8ad26213d7a28d93
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 6542efc7261aaba3b784406e8ad26213d7a28d93.nq.gz
│   └── repolex
│       └── 6542efc7261aaba3b784406e8ad26213d7a28d93
│           └── chunk-001.nq.gz
├── blob
│   ├── 0cfff0277ef33706d951fa72d94583d1b64af94c.nq.gz
│   ├── 26ce133f051b10193a82cbbe27366020b629d4c5.nq.gz
│   ├── 294b389980549b9c318ebf798f08adbf81272f28.nq.gz
│   ├── 2a2265490960ebfd0e4c230ce93e79f0e76f3ef1.nq.gz
│   ├── 5220a81938d2f9a64d6e9c6295678fd979c8e76c.nq.gz
│   ├── 66f6288eb7705860a70850de30afcdd3761bd715.nq.gz
│   ├── 6ac0b10083df1c56629129b9786feffd4a1bd45b.nq.gz
│   ├── 8e32ae6d023e0f00a4903759481573afcf46a8ed.nq.gz
│   ├── e52dee7f5ec0f339f1436d52c7120e03876de744.nq.gz
│   └── ed90fe722819f1c9004ef641d30a18fd4e057c89.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 6542efc7261aaba3b784406e8ad26213d7a28d93.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 17 files
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

[asimov-platform/asimov-chrome-extesion](https://github.com/asimov-platform/asimov-chrome-extesion)

---
*Parsed on 2026-09-27 by [repolex](https://repolex.ai)*
