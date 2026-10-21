# Repolex Knowledge Graph of piccolo-orm/piccolo_videos

RDF knowledge graph data for [piccolo-orm/piccolo_videos](https://github.com/piccolo-orm/piccolo_videos), parsed by [repolex](https://repolex.ai).

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
rlex download piccolo-orm/piccolo_videos
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 1c96be8e65949bfab90bc0d68a9138946298d436
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 1c96be8e65949bfab90bc0d68a9138946298d436
│           └── chunk-001.nq.gz
├── blob
│   ├── 09e37fe9c7a70cede3d5b42793385a10482ee720.nq.gz
│   ├── 0c1157327c1e07a75763a56d301b94ffaf448cec.nq.gz
│   ├── 0c78208ca03af27526a06eae268764f4f6606f86.nq.gz
│   ├── 0d45d3a357e7dcecfbb9f3019448976b1edd7ef2.nq.gz
│   ├── 1b7340b80bf93851197567074298350540581f73.nq.gz
│   ├── 1bc8644a89d24fc83e35aa546c86f6c1f6c2e3f4.nq.gz
│   ├── 35881fcb02dc226d60a4848c5d454a67d2697d38.nq.gz
│   ├── 3a611e23d8c7ddc8134edb9fbceeb08f0a1ec0f5.nq.gz
│   ├── 3bd36586a72873722aab79e07bbc89fca3bf81b0.nq.gz
│   ├── 48356460fd1300fff1711b29b67e7166501d06a3.nq.gz
│   ├── 5bd4c683a3dc1180d237526ed53a932fcafa339d.nq.gz
│   ├── 60e9f8a5fe9ea45e2a5600d1684aa9bf89354c87.nq.gz
│   ├── 62b113e948dea452f9d802fbd44d4a6a609c5d6e.nq.gz
│   ├── 81a06f63bb4c7bd17101ba6c8fd57d14a9da9cd7.nq.gz
│   ├── 85e3978f4e9c520d1d5183a9077bc5e3e2dd56e9.nq.gz
│   ├── 98f2d57b00eeb5c4cc1541ab7bbe994c1fa34967.nq.gz
│   ├── add00c5a9c633eccf0ec918bd6529fb9a9b2ad34.nq.gz
│   ├── b846e13274c05245f64c5587cc817788c39f1d6f.nq.gz
│   ├── ba77a2781e8ff686b47f15855450520d807a0999.nq.gz
│   ├── bc481e9f098c5a2157c157e99bacb4231816ec4f.nq.gz
│   ├── c7dbb5b8a177af426e0ce2c6fcab9ac3b9815a9a.nq.gz
│   ├── ca185c349b1bae4bc7acfd791ef1ea7e602a8537.nq.gz
│   ├── dd48d1a2630d00ab43e316eda16a219599e36816.nq.gz
│   ├── dd640d030a727ee827d3e2f0a68e59b50fe63a8e.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f2fbb37e586fd40902e081cf27490efe027f31c5.nq.gz
│   ├── f3efe5b2e45a0089dc036ba3b42c972347459806.nq.gz
│   ├── f4036230da4c6e0755a3453b8592cc6f86fc40da.nq.gz
│   └── fffbb4a7d7b706063c91fab0f97d1e11b98bfdbc.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 1c96be8e65949bfab90bc0d68a9138946298d436.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 35 files
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

[piccolo-orm/piccolo_videos](https://github.com/piccolo-orm/piccolo_videos)

---
*Parsed on 2026-10-21 by [repolex](https://repolex.ai)*
