# Repolex Knowledge Graph of jaraco/jaraco.video

RDF knowledge graph data for [jaraco/jaraco.video](https://github.com/jaraco/jaraco.video), parsed by [repolex](https://repolex.ai).

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
rlex download jaraco/jaraco.video
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── d96997b1cb66884d83aa8a3583a07220f9f0b2f2
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── d96997b1cb66884d83aa8a3583a07220f9f0b2f2
│           └── chunk-001.nq.gz
├── blob
│   ├── 07606039e8dd43200141bc282795a4ccc572a024.nq.gz
│   ├── 10d412f406891b9683f832fcbc134c9bdf4f916e.nq.gz
│   ├── 1f2aa7533b0423a8eb943f6f4ec02498e39581a0.nq.gz
│   ├── 2209f73f964e0f240528cfe106efde08ce143e69.nq.gz
│   ├── 240329c3604d8ead4c10aa8c88352caa8e4ce7b2.nq.gz
│   ├── 2e3f4dd791a6372b427d618eb0baa8c4dc58e5f0.nq.gz
│   ├── 304196f81e11a168c9894f966e4a617ebf4ed53c.nq.gz
│   ├── 377d8ce7ccd9b1ede45f780436748f33dcdc6257.nq.gz
│   ├── 3d8bfa06089fc2793a4c5d721959409297c40d51.nq.gz
│   ├── 40fd9bc82ff748c5c7166dc13d6a945b43371b29.nq.gz
│   ├── 4495d452b3665644b387536b507dceb0ead11b62.nq.gz
│   ├── 47a78b2c54f05985dd5c6a334361c870cc61ad02.nq.gz
│   ├── 504fbfb47aa9f32aca942c267ed0013693e95c76.nq.gz
│   ├── 54cc8303b22089e12053e552d4e6cb852a865b8a.nq.gz
│   ├── 577e87a793a20e413f7321f4f17ec1eba2ea1962.nq.gz
│   ├── 5bdc232005af9be104a00437ae9bc64417a4c1cc.nq.gz
│   ├── 700235be57c1b2872455c0be5333f59cf568e252.nq.gz
│   ├── 724370638fc188317bbc7dc868f1a571995fd796.nq.gz
│   ├── 7ee279a26f5017e215e1a7a7a1cda79e78086402.nq.gz
│   ├── 818405bc31a18868b0c06755bed14e1bbf9f9387.nq.gz
│   ├── 8311ed95cbcea343322aefced6a33f38f9b1887e.nq.gz
│   ├── 913eed85606612f63bf625b866c68d84da463818.nq.gz
│   ├── 9a0f3bce1395ae3819030b822e5d9076c85068ea.nq.gz
│   ├── a8460b2b510ff44a1b2ec68157f66e65c4ad53c7.nq.gz
│   ├── afd946b11072495570179429889587f6037b86c8.nq.gz
│   ├── d869f85793899446a5e4e7cab73c63728680d1f8.nq.gz
│   ├── dea84c181bb281c400e3445324562fdb2ec6f196.nq.gz
│   ├── e05a3d4a2ab888e32952006d8cd380864368db5f.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── ef5974567c3bc39d3608366174d85ac02a91032b.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── d96997b1cb66884d83aa8a3583a07220f9f0b2f2.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 38 files
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

[jaraco/jaraco.video](https://github.com/jaraco/jaraco.video)

---
*Parsed on 2026-10-20 by [repolex](https://repolex.ai)*
