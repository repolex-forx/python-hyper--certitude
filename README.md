# Repolex Knowledge Graph of python-hyper/certitude

RDF knowledge graph data for [python-hyper/certitude](https://github.com/python-hyper/certitude), parsed by [repolex](https://repolex.ai).

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
rlex download python-hyper/certitude
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 33845ae0a6b123f084f10c7dd27f11485dd73ca6
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 33845ae0a6b123f084f10c7dd27f11485dd73ca6
│           └── chunk-001.nq.gz
├── blob
│   ├── 0697bf1f935d0cf51d1ea9904201bd4242a8ced2.nq.gz
│   ├── 0779306ea4ba71a218831245c03562cae69aafda.nq.gz
│   ├── 088e997ab440331b487c0b0fb21177ab960c3f1f.nq.gz
│   ├── 0ef0323a3d65e05cff94b0a64c070f10cd12a528.nq.gz
│   ├── 12154c5ca47499d77726eb6a19d2d712723f2ee7.nq.gz
│   ├── 14107878cfaef7eb728a020afa7bc6f13ba4efca.nq.gz
│   ├── 16eb3e3a1b25b7d08bbf6176a1175eb732bfdbd5.nq.gz
│   ├── 1c3c0b481b5224d69161eb95f3073cb1eb07956b.nq.gz
│   ├── 23d6f450917a39ebf5512c3cd9896b4ba5722f39.nq.gz
│   ├── 290aa9c50bc20209d1049020835c4465f89ff098.nq.gz
│   ├── 2b4e6f20b7e9effec2d97dd34aa7e2f7a79aa2b0.nq.gz
│   ├── 30468a4ac9f3272cdd5c6b81b9ede7ed180674d5.nq.gz
│   ├── 3c9e7e89081c5e477a778ceff5b75a8f8aa90eeb.nq.gz
│   ├── 57a536bf14b9fa03c99811adaec9fb0e1a2f2743.nq.gz
│   ├── 7141783b1d40b728697b367ec00ad63af0c34ea4.nq.gz
│   ├── 811fcc4e79ec8245cf82dd5561109acb1304072b.nq.gz
│   ├── 8ce83888c7c4220a6fd664495e0cc5f14d402b2f.nq.gz
│   ├── 8e647bf4d461856a387101cb069c1581d1185b9a.nq.gz
│   ├── 8fe3daa13bc0a4835380a314b13d8a32536adfa8.nq.gz
│   ├── a72f0c6bb93faef87d256acf4cb409294d60fb6a.nq.gz
│   ├── abc2380cafaeb8ba32f81130129b8545bc4f6d3b.nq.gz
│   ├── b271da72ae5133cf8e2eb5fdcf53acea37c7eebd.nq.gz
│   ├── b53dc25fbb0ff100daca13567734d354dc7401e9.nq.gz
│   ├── b64695777a74871ca0563870a117f60097e0e272.nq.gz
│   ├── b913e395cd37f939b45be160e8d279b8f275c506.nq.gz
│   ├── b9708909b75631addad701506e6ff3cbe2424ac3.nq.gz
│   ├── c24b4c13939eefb8ab43b963c679dcfe34d2d452.nq.gz
│   ├── cc5e684bdbc4fb271cbeaa442cb0bedfdf4e5179.nq.gz
│   ├── d23faec7bf407ef7776becfea2c73eece4dbf2ce.nq.gz
│   ├── d442fe6ea9d822124c6749c825492197405f6e09.nq.gz
│   ├── db67720986351a7c7dc986c61b2524f08d9c4e44.nq.gz
│   └── e3ef11b2348b7bbe790c3c1e93f1736839326f5c.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 33845ae0a6b123f084f10c7dd27f11485dd73ca6.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 40 files
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

[python-hyper/certitude](https://github.com/python-hyper/certitude)

---
*Parsed on 2026-10-28 by [repolex](https://repolex.ai)*
