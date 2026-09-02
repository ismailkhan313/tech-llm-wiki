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

The concept pages here are mirrored, roughly every 30 minutes, to the
`/wiki/` section of [ismailkhan.xyz](https://www.ismailkhan.xyz/wiki/) — see
that repo's `.github/workflows/sync-wiki.yaml`. Edit here; the site follows.
`references/`, `CLAUDE.md`, and this file stay unpublished. `log.md` is
special-cased: it's excluded from the plain mirror but republished
separately as `/log`, retitled "Wiki Log" — see below.

## Structure

```
tech-llm-wiki/
├── CLAUDE.md        # schema: how the wiki is organized and maintained
├── index.md         # catalog of every concept in the wiki
├── log.md           # chronological history of what changed and when
├── references/      # raw sources, immutable
│   └── index.md
├── Diagrams/        # Excalidraw sources + their exported PNGs
│   └── <concept>.excalidraw, <concept>.png
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

## Publishing: from a wiki edit to the live site

Getting a change from this repo onto `ismailkhan.xyz` is a few hops, all
on GitHub — nothing here pushes to the site directly:

1. **Push here.** `git push` to `tech-llm-wiki`'s `main`. Nothing fires
   automatically from this side; this repo has no knowledge of the site.
2. **The site's sync job picks it up.** `ismailkhan.xyz`'s
   `.github/workflows/sync-wiki.yaml` runs on a 30-minute cron (or
   on-demand — see step 5). It clones this repo fresh from GitHub (never
   from anyone's local disk, so an unpushed commit is invisible to it),
   rsyncs everything except `.git`, `.gitignore`, `.claude`, `CLAUDE.md`,
   `README.md`, `references/`, and `log.md` into `content/Wiki/`, and
   separately rewrites `log.md`'s title to "Wiki Log" and writes it to
   `content/log.md`.
3. **It commits and pushes, if anything changed.** The job commits as
   `github-actions[bot]` (`Sync notes from tech-llm-wiki@<short-sha>`) to
   `ismailkhan.xyz` main and pushes. A no-op run (nothing to mirror)
   stops here — no commit, no deploy.
4. **That push triggers the site build.** `deploy.yaml` runs
   `npx quartz build` and deploys to GitHub Pages via
   `actions/deploy-pages`. The live site is now current.
5. **Anyone's local `ismailkhan.xyz` clone is still behind.** Steps 2-4
   happen entirely on GitHub; nothing pushes down to a local checkout.
   `git pull` there to catch up before trusting `localhost` or making a
   change on top of the synced content. To skip waiting on the cron,
   trigger the sync manually first:
   `gh workflow run sync-wiki.yaml -R ismailkhan313/ismailkhan.xyz`.

Net effect: edit and push here; the site catches up within ~30 minutes
on its own, or immediately with a manual `workflow_dispatch`. A local
`ismailkhan.xyz` checkout needs its own explicit `git pull` regardless —
it's never a target of anyone's push.
