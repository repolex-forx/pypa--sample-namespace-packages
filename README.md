# Repolex Knowledge Graph of pypa/sample-namespace-packages

RDF knowledge graph data for [pypa/sample-namespace-packages](https://github.com/pypa/sample-namespace-packages), parsed by [repolex](https://repolex.ai).

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
rlex download pypa/sample-namespace-packages
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 134414420e5f499547e8e36cb10e403a903f929b
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 134414420e5f499547e8e36cb10e403a903f929b
│           └── chunk-001.nq.gz
├── blob
│   ├── 03444e1df0185778cf840a3c583118e495d2d59b.nq.gz
│   ├── 0804c450f5f691e5f5c8829cfa1ae718e26821ca.nq.gz
│   ├── 09f5752cc981d16c983eb722f2edbce16fa6dc01.nq.gz
│   ├── 0aa810dfbf6f5ca0e2911a562cbe1436ef9fc69e.nq.gz
│   ├── 0c8034bbb5b12c8c5f8fad3aadd46d8beddc1db0.nq.gz
│   ├── 1cd580c6d991c3e30e65aebe691f947dc83c2c08.nq.gz
│   ├── 261eeb9e9f8b2b4b0d119366dda99c6fd7d35c64.nq.gz
│   ├── 27b9352a1edf4a381c0dd632227d94a111251ae4.nq.gz
│   ├── 3f97de4b54295ed04af7b89f30fd9dc2c828f83d.nq.gz
│   ├── 4ffda8ff57bb6a40acf1c73d52b5ec504faa1bc6.nq.gz
│   ├── 64aea5c0d07a54221b655a854185ed697d9c2403.nq.gz
│   ├── 69e3be50dac40cddced86e9df2f9c2df5a75f004.nq.gz
│   ├── 6ddc7e0480dbc1b83133c7cb6f6a9d80549d7de6.nq.gz
│   ├── 8021a7ab34eeec8f403c44bc3cdbe231c3e1e2f7.nq.gz
│   ├── 872122a53d4eae4feadf467ba831a7cfbe4b064a.nq.gz
│   ├── 88d3397857375d5c98d0dd0f4ff1fd7a1b73ca0c.nq.gz
│   ├── 891ded3ff37969e24212a519637fb520ee149419.nq.gz
│   ├── 8a791ed63cd49f10b1efebfc232a65ef1bea3707.nq.gz
│   ├── b2018858b57ca5b2c6da333e393f27db8c1e4b30.nq.gz
│   ├── ba466ae9c9aaae619becfd10a8da61f537b710ca.nq.gz
│   ├── bd8bb444f1277abbc5d13961c75e63f400d0d449.nq.gz
│   ├── de40ea7ca058e07a399acf61529d418c07eeee61.nq.gz
│   ├── ede6c8c9bb711dc7fb1627b8d8497ea97736c30d.nq.gz
│   └── fed528d4a7a148fd0bf0b0198a6461f8c91b87e9.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 134414420e5f499547e8e36cb10e403a903f929b.nq.gz
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

[pypa/sample-namespace-packages](https://github.com/pypa/sample-namespace-packages)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
