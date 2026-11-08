# Repolex Knowledge Graph of deepset-ai/dap-github-agent-template

RDF knowledge graph data for [deepset-ai/dap-github-agent-template](https://github.com/deepset-ai/dap-github-agent-template), parsed by [repolex](https://repolex.ai).

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
rlex download deepset-ai/dap-github-agent-template
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 0ee0930a41cd3234a8664c3757f70bfa694297f3
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 0ee0930a41cd3234a8664c3757f70bfa694297f3
│           └── chunk-001.nq.gz
├── blob
│   ├── 002f0bae8b54e70fb93810814d69b9e6be47af6f.nq.gz
│   ├── 03bc6a41d066d041aa39e8857a20754212053291.nq.gz
│   ├── 044f7b157e6d11285af8845df05d4694fa576fb8.nq.gz
│   ├── 0c03128cdb509de03bb02d3bcea2857c58470e67.nq.gz
│   ├── 138b28bc26869c1c594a899ff274368b3a06e49a.nq.gz
│   ├── 1e5eca1d8e5bb8f169391a8b129bad57e58246c6.nq.gz
│   ├── 2aeedfc9a3b0dc8ae31ea8b86b2a755c64310dea.nq.gz
│   ├── 3080be3520fba2784c789dd09a8c5723bb1c9e9f.nq.gz
│   ├── 3c7ec073c20140e24746127c0d9dcd9a1801eeec.nq.gz
│   ├── 516bebcc543083adb851e46d6f9c342a9ce133f0.nq.gz
│   ├── 56005faceaa1b6cef28f1a35de31a398db34837c.nq.gz
│   ├── 5841758dc50ee3fdd51083f2bd090f1a1a185ae4.nq.gz
│   ├── 59beef1bb5c0c82f58a781ad111863ead50303d4.nq.gz
│   ├── 62d2dca615068d0915dfbade5e81f4d671254b29.nq.gz
│   ├── 6ce4081fcfa9f724ac98f7ecf927f006a5524fa2.nq.gz
│   ├── 736670089226689a62e9849ee7eb465ea3c0ea8e.nq.gz
│   ├── 81b29553b96a75dd322acba5cb52d32217755d38.nq.gz
│   ├── 84332a9ab4b56234a1c17e8872e17a977a7f9c3d.nq.gz
│   ├── 8f8e0fd9f27b4376cb1dda9f0f69458f8685623e.nq.gz
│   ├── 9b6f7e0ddbd0bc7b755dcb570a568e3d7c6426a4.nq.gz
│   ├── a4af032be323991c33edec8cbfc18005dd3239f1.nq.gz
│   ├── b7e96724b389853a4705dc0e88a1b7454937bec7.nq.gz
│   ├── c33f2a39bd11a2d059a7a4a508e24c9fcd1dc043.nq.gz
│   ├── c38cfbabd861f2ae1a6b5b43c7902d7e3ecfec34.nq.gz
│   ├── ccfb17a4883ef59233be9c2561f9781499c054d1.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ea003cae4ece5a400a22fa81c799e6d7f4aaec2e.nq.gz
│   ├── f23879c76b3661be7e32da38b4db96d25463a2e0.nq.gz
│   ├── f3e2d96581de9b4f053be69727e04dceb358ac0a.nq.gz
│   ├── f4010d88c5fb735ee2c36f6964e851a1cf5366f5.nq.gz
│   ├── f445de6e61fadd8a60f93af49e09a9b83e4d53b7.nq.gz
│   └── fd0d0f86db0dd300afc2721da6b19c1e1d4bb983.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 0ee0930a41cd3234a8664c3757f70bfa694297f3.nq.gz
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

[deepset-ai/dap-github-agent-template](https://github.com/deepset-ai/dap-github-agent-template)

---
*Parsed on 2026-11-08 by [repolex](https://repolex.ai)*
