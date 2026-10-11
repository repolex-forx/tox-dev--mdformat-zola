# Repolex Knowledge Graph of tox-dev/mdformat-zola

RDF knowledge graph data for [tox-dev/mdformat-zola](https://github.com/tox-dev/mdformat-zola), parsed by [repolex](https://repolex.ai).

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
rlex download tox-dev/mdformat-zola
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── bceb47770bfe67eb16f3f997a348e70cedbbfc0e
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── bceb47770bfe67eb16f3f997a348e70cedbbfc0e
│           └── chunk-001.nq.gz
├── blob
│   ├── 0434e5cc5a4fd3da171912f9874bfeeb201d3a29.nq.gz
│   ├── 07384a67f7cbb83d41a94921e6d760006fef57b7.nq.gz
│   ├── 082b5c2f793d3634a0941d5b3c33ff6d5da14671.nq.gz
│   ├── 1bbc5a6c5814230d2f70ae6f601ab383b710cca0.nq.gz
│   ├── 1bdcc9fe4b1f86cc76d1a7bfecb6bdbeee9b0374.nq.gz
│   ├── 220f93d375a19bb70914391ab389759183167d01.nq.gz
│   ├── 22decf25feb789b33123840e6c9613122a035590.nq.gz
│   ├── 23da45eaf0a5176f2f88cf8e6c362383ee1277b4.nq.gz
│   ├── 2925dbfa73304f53ae87ff82b8d6ff1c4f201c9f.nq.gz
│   ├── 386ceeaff12f31b6a1ec447d17feb5d58451e740.nq.gz
│   ├── 3e0bbdfaf80dfff6f997ce5ae1ff3e7797d9bb15.nq.gz
│   ├── 4602404a569b9fd719995403ba105f68a535dce6.nq.gz
│   ├── 466f0212e94baec0a59bc5349fd8d4b3edeb8a52.nq.gz
│   ├── 4fd9a6e582b8ea307eadae38c0a073d25876ef11.nq.gz
│   ├── 5f89818f9e63c2f6829c7706c57f223cdb5bbd38.nq.gz
│   ├── 64946c9ba48dd134c66f0078987c7d50759775d5.nq.gz
│   ├── 69d0cfd202c019ca1d5a92d59faf9a1380c61930.nq.gz
│   ├── 7727efc2c7670b60c86b75521d712e342c3d5c4f.nq.gz
│   ├── 7c1a227a414e7da387e47187145b734874b53c1f.nq.gz
│   ├── 8e4f65fccf604c35417dc711c17c78447fae3c77.nq.gz
│   ├── a234fdfbf68e65322c90d26ba6389ee4325e2a0c.nq.gz
│   ├── a3ae5220f74924aaec2410a7fc5b4b7bed0bca8c.nq.gz
│   ├── ae419c100b25005bd082785a7709b42a9e0300ba.nq.gz
│   ├── aee08c0c2965cd5f5894eb6fe4b4c7fb6d4120f1.nq.gz
│   ├── cab4b842d61049aca993c3d9332a8b1ab7dab180.nq.gz
│   ├── de2ae2558afd4adf79fdad2efd6b9db7f72b60f4.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e937e1f4ed5cddc8243f1d774e5be8c6e0442043.nq.gz
│   ├── f6f246203f771978fdb5ade6f00ee0f2228ca2db.nq.gz
│   ├── f8c4f25d0f20ca31a31c6dfdbfcabd3fa88cead0.nq.gz
│   ├── faec868cbea20b8cfc5a0bd7fc865d60e1951e98.nq.gz
│   └── fcec87a91da27f660131ab3ea124a88a8f27936a.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── bceb47770bfe67eb16f3f997a348e70cedbbfc0e.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 39 files
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

[tox-dev/mdformat-zola](https://github.com/tox-dev/mdformat-zola)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
