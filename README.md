# Repolex Knowledge Graph of samuelcolvin/array-has-slow

RDF knowledge graph data for [samuelcolvin/array-has-slow](https://github.com/samuelcolvin/array-has-slow), parsed by [repolex](https://repolex.ai).

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
rlex download samuelcolvin/array-has-slow
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── d833682ce9c148970377767e5dd7b12523aa3610
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── d833682ce9c148970377767e5dd7b12523aa3610
│           └── chunk-001.nq.gz
├── blob
│   ├── 79fc2167a05c80e3b74f57b17544b86cfb32bf17.nq.gz
│   ├── 828237cbf73d2c631c0341ce6a6b33675ef48653.nq.gz
│   ├── 91fd7655fe83e92d372cd37d4e9aebf9b432ba85.nq.gz
│   └── b84305e275d7c81dcb041d49e313dd34a1ccebcb.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── d833682ce9c148970377767e5dd7b12523aa3610.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 10 files
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

[samuelcolvin/array-has-slow](https://github.com/samuelcolvin/array-has-slow)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
