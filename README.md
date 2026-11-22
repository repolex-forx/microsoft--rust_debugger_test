# Repolex Knowledge Graph of microsoft/rust_debugger_test

RDF knowledge graph data for [microsoft/rust_debugger_test](https://github.com/microsoft/rust_debugger_test), parsed by [repolex](https://repolex.ai).

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
rlex download microsoft/rust_debugger_test
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 6b67e123861cc4a41505b4e8f7fb278e8cbc6c42
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 6b67e123861cc4a41505b4e8f7fb278e8cbc6c42.nq.gz
│   └── repolex
│       └── 6b67e123861cc4a41505b4e8f7fb278e8cbc6c42
│           └── chunk-001.nq.gz
├── blob
│   ├── 199c66f1674cf05cafbab9186c40f41bdb0c9ad4.nq.gz
│   ├── 1f12ceb80801c23e24a546b5b18ff5551b3bbac4.nq.gz
│   ├── 291d4d43733f4c15a81ff598ec1c99fd6c18f64c.nq.gz
│   ├── 30ecd0d41bb7efa30a01a1e03655e9ce865625a5.nq.gz
│   ├── 365b629dce5e8e06158444b1af4d6feae99da0e7.nq.gz
│   ├── 40290e92186726be1f51415563b935a465762da5.nq.gz
│   ├── 408e842a4ce8e6d0d413ed905795b429b78804f3.nq.gz
│   ├── 49ab9b577626062f3c7df155dcc80931979e8abc.nq.gz
│   ├── 674f01bb40a0b2453734db7e214870f7835d1482.nq.gz
│   ├── 85f1ee4b27d453f3541999f132d18c95d14968c0.nq.gz
│   ├── 869fdfe2b246991a053fab9cfec1bed3ab532ab1.nq.gz
│   ├── 88522aff74398cf423e55d7fbf01869458d7bb3f.nq.gz
│   ├── 8ad683ff9a9fd207bb2e2e3ddaf8a3a7132cdc23.nq.gz
│   ├── 9e841e7a26e4eb057b24511e7b92d42b257a80e5.nq.gz
│   ├── a12e667c90148a93e969b5f8a68f0491b052b462.nq.gz
│   └── f9ba8cf65f3e3104dd061c178066ec8247811f33.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 6b67e123861cc4a41505b4e8f7fb278e8cbc6c42.nq.gz
├── filetree
│   └── 6b67e123861cc4a41505b4e8f7fb278e8cbc6c42.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 26 files
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

[microsoft/rust_debugger_test](https://github.com/microsoft/rust_debugger_test)

---
*Parsed on 2026-11-22 by [repolex](https://repolex.ai)*
