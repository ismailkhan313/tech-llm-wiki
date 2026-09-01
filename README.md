# tech-llm-wiki

A personal, LLM-maintained knowledge base on LLMs and AI more broadly —
built by ingesting papers, articles, and notes, and letting Claude Code
keep a wiki of interlinked concept pages current as sources come in.

Two ideas this repo combines:

- **The pattern**: [Karpathy's LLM wiki gist](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f)
  — raw sources in, an LLM-maintained wiki out, instead of re-deriving
  synthesis from scratch on every question.
- **The format**: [Open Knowledge Format (OKF) v0.2](https://github.com/GoogleCloudPlatform/knowledge-catalog/blob/main/okf/SPEC.md)
  — markdown files with YAML frontmatter, portable and readable without
  any tooling.

See [CLAUDE.md](CLAUDE.md) for the concrete conventions (frontmatter
fields, ingest/query/lint workflows, index and log formats).

## Structure

```
tech-llm-wiki/
├── CLAUDE.md        # schema: how the wiki is organized and maintained
├── index.md         # catalog of every concept in the wiki
├── log.md           # chronological history of what changed and when
├── references/      # raw sources, immutable
│   └── index.md
└── <concept>.md      # wiki pages, added as sources get ingested
```

Flat and unopinionated for now — subdirectories (`models/`, `papers/`,
`people/`, ...) get introduced only once there's enough content in a
category to warrant one.

## Usage

Open this repo with Claude Code (or any agent that reads `CLAUDE.md`) and:

- **Ingest** a source: drop it in `references/` and ask the agent to
  process it into the wiki.
- **Query**: just ask a question — the agent reads `index.md`, drills
  into relevant concepts, and answers with citations.
- **Lint**: periodically ask the agent to health-check the wiki for
  contradictions, stale claims, and orphan pages.

The wiki is just a git repo of markdown files — full history, diffs, and
no lock-in.
