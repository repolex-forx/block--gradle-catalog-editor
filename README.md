# Repolex Knowledge Graph of block/gradle-catalog-editor

RDF knowledge graph data for [block/gradle-catalog-editor](https://github.com/block/gradle-catalog-editor), parsed by [repolex](https://repolex.ai).

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
rlex download block/gradle-catalog-editor
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 10fc19b8c35805961ce1d22fa795167a693b65c7
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 10fc19b8c35805961ce1d22fa795167a693b65c7.nq.gz
│   └── repolex
│       └── 10fc19b8c35805961ce1d22fa795167a693b65c7
│           └── chunk-001.nq.gz
├── blob
│   ├── 0367d2331a2cbfb3dadb43da08affe106a235c28.nq.gz
│   ├── 081cbe83449cf8e625a3e2e79b6b35415c4e1503.nq.gz
│   ├── 0ba9db25329d0b336e39ca8cde8470c5b7bc45eb.nq.gz
│   ├── 25f0bc5ed80683a81f46e6bfd1cf8ea0b56c6807.nq.gz
│   ├── 28f51764668db9d20405696882f899ee8d5adb87.nq.gz
│   ├── 2f5c619a87e72fe8f2cec1901d029940e98ee4f2.nq.gz
│   ├── 31559b7d115e3c105b328cce9b9dcd9774025061.nq.gz
│   ├── 383f4511d444516caed0fd113ee8a2b640cd2290.nq.gz
│   ├── 3cc70d3849f5fb3fee2f01e66659c996ebb5abd4.nq.gz
│   ├── 4180f0cfde134913324d0a50ead7c9b2ed26fcb6.nq.gz
│   ├── 656ab745123b7399ac02ea5554891ce4e5ce04cf.nq.gz
│   ├── 67bcc2f72725f6057a8ff744444db07d234fb991.nq.gz
│   ├── 6bccf43368fd7c96d9c659562a5142b8b8cb98a1.nq.gz
│   ├── 862ee3c28647e7a58801a75236855c269c1448ae.nq.gz
│   ├── 9582fc588754f78d9875691a3bd5e674295436b3.nq.gz
│   ├── 9decb08fc1981b54975b576dc05b60b5195906b4.nq.gz
│   ├── 9f827930779f45d3a659076804fb85c390e49c37.nq.gz
│   ├── a2cde42065383d471c6881fe007e3883744a67e9.nq.gz
│   ├── a4ecfbe7eeca8c4f58825d1dac272f9900f3a6c4.nq.gz
│   ├── a62762dbf0548f0c84a1c2963f335cd9c7f1bec6.nq.gz
│   ├── b2f8bcc531be497e7a14dd93259208de6a547507.nq.gz
│   ├── b78ae3114fcb3932e61a09f5ee56e78aeaa6ab5f.nq.gz
│   ├── c709a34155ebc467236f8b1cce29ffcbbd0fa0e4.nq.gz
│   ├── cd0a80988307477eda75700f6a5943cf7394f1d4.nq.gz
│   ├── e0c4ae255fcf8866ec8e31fb2e4be777d8892969.nq.gz
│   ├── e889550ba4cbc92a720527042e5f6e7a303bfcbc.nq.gz
│   ├── fd495da0fc1a2967da2db2caf4e0dfc09ba48a60.nq.gz
│   └── fe28214d3352b0ed40820a4999317694c8b1ef57.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 10fc19b8c35805961ce1d22fa795167a693b65c7.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

14 directories, 37 files
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

[block/gradle-catalog-editor](https://github.com/block/gradle-catalog-editor)

---
*Parsed on 2026-10-02 by [repolex](https://repolex.ai)*
