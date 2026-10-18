# Repolex Knowledge Graph of Qix-/better-exceptions

RDF knowledge graph data for [Qix-/better-exceptions](https://github.com/Qix-/better-exceptions), parsed by [repolex](https://repolex.ai).

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
rlex download Qix-/better-exceptions
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── b928ff9e2c933cdd3b27321c766ce68bfa60826c
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── b928ff9e2c933cdd3b27321c766ce68bfa60826c
│           └── chunk-001.nq.gz
├── blob
│   ├── 02c390de7f71f905e79c1982716a4992165a382b.nq.gz
│   ├── 0886059d10e90ce23630876018d6a16db3e11eb6.nq.gz
│   ├── 23b0120502df8ccb4d53000ea6d67d6cd4995438.nq.gz
│   ├── 3abf64628d22a88fa0f811c0a8e784d465865e75.nq.gz
│   ├── 41707b856d588bc870e01cd123b2de955c976644.nq.gz
│   ├── 44dcee2a5bcacdfaaa9435ad847c8b161a907daa.nq.gz
│   ├── 47a1f61a29bb8db9885659f2bc8950ae2a12dba2.nq.gz
│   ├── 4d193b85a894ba865f5f9db10b3aa72061930479.nq.gz
│   ├── 517ef7b463d467cb850652567cb12a860ce1567b.nq.gz
│   ├── 71e3ba8520018443018ae3429c5b9aa038ef9395.nq.gz
│   ├── 774f8529879c2fc91907f8d2404f593cf21129f5.nq.gz
│   ├── 7dc4a8c40e54a7a7753f0f9b36b85a2480e9596a.nq.gz
│   ├── 7e1ceda43f73dbec535d0bdccc7ae0c9ec417df0.nq.gz
│   ├── 8261962068d9d0aacddee08d90087d05625dd6c1.nq.gz
│   ├── 83b9f851455c0e2edd90aec3247eca76fe8c757f.nq.gz
│   ├── 880ce3ccb68956d486e68f25ec9f763434723609.nq.gz
│   ├── 8b137891791fe96927ad78e64b0aad7bded08bdc.nq.gz
│   ├── 8bf4019901b7ba55f6fff2224fc9b564ea4dd4c5.nq.gz
│   ├── 8dd092e4fdc271076319e6287f25abefa4dc47b3.nq.gz
│   ├── 8f21bbf9aece6a01e9b71f12d7556b0007e2cd3e.nq.gz
│   ├── 901f687d0b638a6bb484767b09b3d58113dd7b05.nq.gz
│   ├── 9d8c4941c49137c6642455583d14a5d7d523a86c.nq.gz
│   ├── a505388750445653d6b1c9099ba7a60de90b25c3.nq.gz
│   ├── a54ef9d66260e1603a1f360a721e61a2b52be721.nq.gz
│   ├── a757d19c4607f8866a46ea484b2e8db9f515ec38.nq.gz
│   ├── a7f7020b1d6d38c5aa0a45d9408a9e04c263722a.nq.gz
│   ├── a8175eca41726a7bb87dc8e568040e41c28db911.nq.gz
│   ├── aae2a119d82d961f76c095a7861d4a0fabaeaff9.nq.gz
│   ├── af89d9280e7351fc3922d9fbb783ac62f4d5570f.nq.gz
│   ├── b43be46d2c718417b1ea143c722fc59fed8e561d.nq.gz
│   ├── b88034e414bc7b80d686e3c94d516305348053ea.nq.gz
│   ├── c7a2c362e6e21037e4530b204a4f2043f8909cc2.nq.gz
│   ├── c7f87231e544c296a93f026024852aab18c818ce.nq.gz
│   ├── d0461a70d3c62be6642443ae3b21335e31d5c5ba.nq.gz
│   ├── d1fdb96553e5e40c906bb3742b600ac99c767048.nq.gz
│   ├── d2ee7236c863736b27d9f45cc8c0fc02dd7360ab.nq.gz
│   ├── d9e951f1c940ffa26a8961bb9a8b0880d822febd.nq.gz
│   ├── e34d3065c812f4d962ccfa5801d0ddc5fbf77db6.nq.gz
│   ├── e6881bfdb642aa74dedfb4e9201bbfc9143a40be.nq.gz
│   ├── ec20b1d500f8ed679c9abc890a45c0f9bdc72c86.nq.gz
│   └── ef6221c27cde95513a07c3daff69d8dc967379b4.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── b928ff9e2c933cdd3b27321c766ce68bfa60826c.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 49 files
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

[Qix-/better-exceptions](https://github.com/Qix-/better-exceptions)

---
*Parsed on 2026-10-18 by [repolex](https://repolex.ai)*
