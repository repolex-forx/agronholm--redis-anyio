# Repolex Knowledge Graph of agronholm/redis-anyio

RDF knowledge graph data for [agronholm/redis-anyio](https://github.com/agronholm/redis-anyio), parsed by [repolex](https://repolex.ai).

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
rlex download agronholm/redis-anyio
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── cf2c8f2cc8b6f5005a170ad002b75e05dc4939d6
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── cf2c8f2cc8b6f5005a170ad002b75e05dc4939d6
│           └── chunk-001.nq.gz
├── blob
│   ├── 07106f0a7cba3ef5531fb89d1c7b72a05a47d6ac.nq.gz
│   ├── 07806f8af9dd3253ebdb5710b67e73124aea4941.nq.gz
│   ├── 1ad405597debfe7858b4df6bbc9f948f6b61c5f9.nq.gz
│   ├── 2b5f229a16977b152cebc6863b4f56979f1c62a6.nq.gz
│   ├── 34211a684365dc1d6fbd8149abca29cb1693a77c.nq.gz
│   ├── 3ba13e0cec6cbbfd462e9ebf529dd2093148cd69.nq.gz
│   ├── 45a2f73673edab66a13ab5de206142341e996f10.nq.gz
│   ├── 48ac4e1dc57fc0d2d6718a8fab56c98bfdff35d3.nq.gz
│   ├── 4b4eff4fee12aa254c44d81fe1b3122bd73aa99d.nq.gz
│   ├── 6ff0537c4ac0c426651c7c9ff5dc6fcaf8dc748c.nq.gz
│   ├── 71060d8645872d4e1ce8ace4955d432747b246cd.nq.gz
│   ├── 715f13ef3342510d284027480f182c41645c6ff0.nq.gz
│   ├── 7ecad6768ac2ecf460e390b60014fb91ae356b1e.nq.gz
│   ├── 8a7c9c37dd8dd075d553aa6cb92bde4118d86630.nq.gz
│   ├── 8c150d493c6ec03bcab126f0005e56229becc513.nq.gz
│   ├── 8dd0eb2c9d87ded99ec02a09ac8ee8ca06c586d2.nq.gz
│   ├── 8dfdc2f4750c08b86b6c2a9cc90a53bad83c3030.nq.gz
│   ├── 8f62801e69b148cedf2c0f78c8ebbefaa67ef2c9.nq.gz
│   ├── 94b4dafe1e17f9f53a07dd41688449110a3767a5.nq.gz
│   ├── ac291b5ca4162fba7ea0a2b2bdec1e2c90724f81.nq.gz
│   ├── b619a688cc8b51c18adb1f85adf376c82f0d5434.nq.gz
│   ├── b6f99099dcbd0917095414e3557ebd8f2c31f943.nq.gz
│   ├── bfe4a2302c4d2d5a5ccf72162f13e5e822e8c77d.nq.gz
│   ├── c5bcbecb80693ef6df5ca5671ae50fdf05b7fa3f.nq.gz
│   ├── d1fa36e951afface52530299130e2cd58bf682c7.nq.gz
│   ├── d66eb5ae85b8fb6d0b7bdc8f3a820e64c1405070.nq.gz
│   ├── d950f4c6b2a55520d4e136bfe41a8e236a46b890.nq.gz
│   ├── e36aa219942066a05227bc2e0627ff33ae3cbee6.nq.gz
│   ├── e4605d9c4f66614a69a638ddd928aad6bb1dc26b.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── eabbc2260f9b90e094da97ce7e199f5b8670f7ec.nq.gz
│   ├── ee540659cd437b6baf69c4d09ad03514ce3c7dab.nq.gz
│   ├── f0584f188d8d0e5bf5e834347cc27d1c2fee3de3.nq.gz
│   ├── f36acc37227dec0698017588af06a19f9c782956.nq.gz
│   ├── f3c9774adf2d710e8e9f234f80cef6ca88bcec85.nq.gz
│   ├── f7df8ddfafaa6ee5a31bebf5c88dca8b45fb90e6.nq.gz
│   └── f8fe245cad1957923f090dfe31fa3235093fac0e.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── cf2c8f2cc8b6f5005a170ad002b75e05dc4939d6.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 45 files
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

[agronholm/redis-anyio](https://github.com/agronholm/redis-anyio)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
