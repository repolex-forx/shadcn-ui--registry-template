# Repolex Knowledge Graph of shadcn-ui/registry-template

RDF knowledge graph data for [shadcn-ui/registry-template](https://github.com/shadcn-ui/registry-template), parsed by [repolex](https://repolex.ai).

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
rlex download shadcn-ui/registry-template
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 906f859db0125965cba71c51da1707c0a4c6d045
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 906f859db0125965cba71c51da1707c0a4c6d045
│           └── chunk-001.nq.gz
├── blob
│   ├── 004145cddf3f9db91b57b9cb596683c8eb420862.nq.gz
│   ├── 0201b961768f3a24d485cdedcd595ab208c8413f.nq.gz
│   ├── 03295ca6ac617de95b78b09e5e3a6de897a204f0.nq.gz
│   ├── 23b66ad869810a62cd2ea3ba4ba0c95c71c2085d.nq.gz
│   ├── 2eed5767e399c21e9efe614626c64f69617a70f5.nq.gz
│   ├── 326c51c231c69315c8dcfe3a0441011a94888ef3.nq.gz
│   ├── 335484f9424bf72b98e3b892275740bc8f014754.nq.gz
│   ├── 41fa2253e986d3a462178d0c15da46b8edde99a6.nq.gz
│   ├── 4308025e6e48d0a974d547c38b6d1c9782dfbb5e.nq.gz
│   ├── 5174b28c565c285e3e312ec5178be64fbeca8398.nq.gz
│   ├── 567f17b0d7c7fb662c16d4357dd74830caf2dccb.nq.gz
│   ├── 574f12ae44079f450d127dcb7e322e1920866d2e.nq.gz
│   ├── 5ef6a520780202a1d6addd833d800ccb1ecac0bb.nq.gz
│   ├── 6b431d2974f66e6c33f06f719044beec329d0f44.nq.gz
│   ├── 6b6bb9fb9b60db6b934c632a05d2f9d06a519b48.nq.gz
│   ├── 718d6fea4835ec2d246af9800eddb7ffb276240c.nq.gz
│   ├── 77053960334e2e34dc584dea8019925c3b4ccca9.nq.gz
│   ├── 7eb92d13d36a64b5070e84c5064c74d63f1e75b9.nq.gz
│   ├── 7f21b5e78a4c1c23bf41b6be206f3f81dc84fe99.nq.gz
│   ├── 96f9eaab6103797e50878a1352442e9593aad131.nq.gz
│   ├── 9aa12f959a9ac21ba1736767a6ab54f7206189c0.nq.gz
│   ├── a2df8dce675fed0712d021fa45245289ecd26c88.nq.gz
│   ├── a3d246169c023d4d950ef2f7fe2b44df9f221283.nq.gz
│   ├── a9f712d1bb7e4a1de8d811880bd46f0fa9021de8.nq.gz
│   ├── b2b2a44f6ebc70c450043c05a002e7a93ba5d651.nq.gz
│   ├── bd0c391ddd1088e9067844c48835bf4abcd61783.nq.gz
│   ├── bd202d3bd3de187ccbac8f10a0563f5ba2367b7b.nq.gz
│   ├── c5f229915cfe401b5dee1910c5fcdf2f8ab26376.nq.gz
│   ├── c7bcb4b1ee14cd5e25078c2c934529afdd2a7df9.nq.gz
│   ├── c85fb67c463f20d1ee449b0ffee725a61dfb9259.nq.gz
│   ├── d05bbc6c74cd8dbc699562cef917bb4267865aed.nq.gz
│   ├── d27102286c9bf76e80985c93123414a1ad4cc9c7.nq.gz
│   ├── d8b93235f205efbea6e8fceb1c9ddb57ddddf28d.nq.gz
│   ├── dc98be74c475620e219a99b9299c2f321231e6f1.nq.gz
│   ├── de4bbbb3fc7682f6d29e375d1431eb388603b91a.nq.gz
│   ├── e140f74590e87a75964bd7cd8e3c15711632ab7b.nq.gz
│   ├── e9ffa3083ad279ecf95fd8eae59cb253e9a539c4.nq.gz
│   ├── f7fa87eb875260ed98651bc419c8139b5119e554.nq.gz
│   └── fb5fbc3eee891a5c118bb00fd153273c16959c9e.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 906f859db0125965cba71c51da1707c0a4c6d045.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 47 files
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

[shadcn-ui/registry-template](https://github.com/shadcn-ui/registry-template)

---
*Parsed on 2026-10-10 by [repolex](https://repolex.ai)*
