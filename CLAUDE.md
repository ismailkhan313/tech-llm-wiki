# tech-llm-wiki schema

This is a personal knowledge base about LLMs/AI, built on the pattern from
[Karpathy's LLM wiki idea](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f)
and structured as an [Open Knowledge Format (OKF) v0.2](https://github.com/GoogleCloudPlatform/knowledge-catalog/blob/main/okf/SPEC.md)
bundle. Read both if you haven't; this file just pins down the local
conventions on top of them.

## The three layers

- **Raw sources** — `references/`. Immutable. Articles, papers, transcripts,
  links dropped in as-is. You read from here, never edit it.
- **The wiki** — every other `.md` file in this repo. OKF concept documents
  you own: you create them, update them as new sources arrive, and keep
  cross-references and `index.md`/`log.md` current.
- **The schema** — this file. Update it yourself as conventions here evolve.

## Bundle root

This repo *is* the OKF bundle root. `index.md` and `log.md` at the root
are reserved (OKF §3.1) — never write a concept with either name.

## What publishes

The mirror to `ismailkhan.xyz/wiki/` carries the concept pages and `index.md`.
`references/`, this file, and `README.md` are excluded at every level —
including any per-subdirectory `references/` a future category split
creates. `log.md` is excluded from that mirror too, but republished
separately as `ismailkhan.xyz/log` (see the site's `sync-wiki.yaml`).

So a bundle-relative link to any of those resolves in this repo but 404s on
the site. When `index.md` (or any concept page) needs to point at an
excluded file, link its absolute GitHub URL under
`https://github.com/ismailkhan313/tech-llm-wiki` instead of a relative path. Links between
concept pages stay bundle-relative as described below.

## Directory structure

Flat for now. Don't pre-create category folders (`models/`, `papers/`,
`people/`, ...) — let them emerge organically as concepts accumulate, and
only split a category out once there are enough concepts in it to justify
a subdirectory with its own `index.md`. When you do split one out, update
links and the root `index.md` in the same pass.

## Concept frontmatter

Follow OKF §4-§5, using only the core fields — no Attested Computation
machinery (§10), it doesn't apply to a reading wiki:

```yaml
---
type: <Concept type>              # required
title: <Display name>
description: <One-line summary>
tags: [<tag>, ...]
sources:
  - id: <stable-key>               # used for footnote attribution
    resource: <path or URL>
    title: <label>
generated: { by: <actor>, at: <ISO 8601 datetime> }
verified: { by: <actor>, at: <ISO 8601 datetime> }   # only once actually checked
status: stable                     # draft | stable | deprecated
---
```

`type` is the only required field, but always fill in `title`,
`description`, and `generated` — they're what make `index.md` and search
useful.

**Every non-reserved `.md` file in the bundle carries this block — files under
`references/` included.** OKF §11.1 requires parseable YAML frontmatter with a
non-empty `type` on every file that isn't `index.md` or `log.md`; a source
saved with only an HTML comment header is a conformance failure. When adding a
file to `references/`, give it `type: Reference` plus:

```yaml
resource: <canonical URL the copy came from>
author: <actor, per §7>
fidelity: verbatim | transcription | excerpt
retrieved: <ISO 8601 datetime>
```

`fidelity` is load-bearing: anything but `verbatim` means the canonical
`resource` wins over the local copy, and a later reader needs to know that.

**Type values** aren't centrally registered (OKF §4.1) — pick what fits.
Common ones here: `Overview`, `Concept`, `Model`, `Technique`, `Paper`,
`Person`, `Organization`, `Benchmark`, `Comparison`, `Synthesis`.

**Actor convention** (OKF §7):
- You, confirming something yourself: `human:ismailkhan`
- This agent, writing/updating a page: `claude-code/sonnet-5` (match
  whatever model is actually doing the work)

**Provenance**: every claim traceable to a source should cite it via a
`sources[].id` and a markdown footnote (OKF §5.1). Point `sources[].resource`
at the file under `references/` (or an external URL if there's no local
copy).

**Verification**: only add a `verified` entry when you or the user has
actually checked the content against its sources — don't rubber-stamp it
on every edit. Absence of `verified` is meaningful (OKF §5.3): it means
unverified, and that's fine for most pages most of the time.

## Cross-linking

Use bundle-relative links (`/some-concept.md`), per OKF §6.1 — they
survive the concept being moved into a subdirectory later. A link just
asserts *some* relationship; say what kind of relationship it is in the
surrounding prose.

## Operations

### Ingest

1. User drops a source into `references/` (or pastes/links it — save a
   local copy into `references/` if practical).
2. Read it, discuss the key takeaways with the user.
3. Write or update the relevant concept page(s) — a single source often
   touches several: a new entity page, an update to an existing overview,
   a note where it contradicts or supersedes an earlier claim.
4. Update `index.md` (root, and any subdirectory `index.md` touched).
5. Append an entry to `log.md`.

Default to ingesting one source at a time with the user involved — check
in on emphasis and what's worth its own page — rather than silently
batch-processing many sources unsupervised, unless the user asks for that.

### Query

Read the root `index.md` first to find candidate pages, then drill in.
Synthesize an answer with citations back to concept pages (and through
them, to `references/`). If the answer is worth keeping — a comparison,
an analysis, a connection — offer to file it back into the wiki as a new
concept page rather than letting it live only in chat history.

### Lint

When asked to health-check the wiki, look for:

- Contradictions between pages.
- Claims a newer source has superseded.
- Orphan pages with no inbound links.
- Concepts mentioned repeatedly but with no page of their own.
- Missing cross-references between clearly related pages.
- Gaps worth filling with a targeted web search.

## index.md

Root and any subdirectory `index.md` is a content-oriented catalog: one
entry per concept, link + one-line description (pull the description from
the concept's frontmatter), grouped under headings. No frontmatter except
the root's optional `okf_version` key (OKF §8, §12).

## log.md

`log.md` is published to the site, so it carries frontmatter (`type: Log`,
`title`, `description`, `generated`) to render with a real title. This is
allowed: OKF §8 forbids frontmatter on `index.md` — the bundle root's optional
`okf_version` is the sole exception — but §9 sets no equivalent rule for
`log.md`.

Root and any subdirectory `log.md` is a flat, chronological,
newest-first log per OKF §9:

```markdown
# Wiki Update Log

## 2026-09-01
* **Ingest**: Added [some-source](/some-concept.md), updated [related concept](/related-concept.md).
```

A consistent leading bold word (`**Ingest**`, `**Update**`, `**Creation**`,
`**Deprecation**`) keeps it `grep`-able:
`grep "^## " log.md` for dates, `grep "^\* \*\*" log.md` for entries.
