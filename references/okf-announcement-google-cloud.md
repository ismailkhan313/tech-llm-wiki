---
type: Reference
title: "Introducing the Open Knowledge Format"
description: Google Cloud's announcement of OKF, describing v0.1 of the format and its reference implementations.
tags: [source, okf, standards, google-cloud]
resource: https://cloud.google.com/blog/products/data-analytics/how-the-open-knowledge-format-can-improve-data-sharing
author: team:google-cloud
fidelity: transcription
retrieved: 2026-09-01T19:01:57Z
generated: { by: claude-code/opus-5, at: 2026-09-01T19:01:57Z }
status: stable
---

<!--
NOT VERBATIM. Agent transcription of the rendered page: section structure and
code blocks preserved, prose condensed in places. The canonical URL in
`resource` is authoritative for exact wording and quotation.
Authors: Sam McVeety (Tech Lead, Data Analytics); Amir Hormati (Tech Lead,
BigQuery, Engineering, Data Cloud). Published 2026-06-12.
-->

# Introducing the Open Knowledge Format

Published 2026-06-12 by Sam McVeety and Amir Hormati.

## Overview

Google Cloud introduced the Open Knowledge Format (OKF), an open specification
that formalizes the LLM-wiki pattern into a portable, interoperable format.
OKF v0.1 represents knowledge as a directory of markdown files with YAML
frontmatter — a vendor-neutral, agent- and human-friendly standard for the
metadata, context, and curated knowledge modern AI systems need.

## Key characteristics

- **Just markdown** — readable in any editor, renderable on GitHub, indexable
  by any search tool.
- **Just files** — shippable as a tarball, hostable in any git repo, mountable
  on any filesystem.
- **Just YAML frontmatter** — structured fields (type, title, description,
  resource, tags, timestamp) that are queryable.

## The problem OKF solves

In most organizations, internal knowledge used by foundation models is
fragmented across metadata catalogs with proprietary APIs, wikis and shared
drives, code comments and docstrings, and senior engineers' heads. This
fragmentation forces every AI agent builder to solve the context-assembly
problem from scratch, and knowledge stays locked behind whichever system
created it.

## Structure

An OKF bundle is a directory of markdown files representing "concepts"
(tables, datasets, metrics, playbooks, runbooks, APIs). Each concept is one
file.

```
sales/
├── index.md
├── datasets/
│   ├── index.md
│   └── orders_db.md
├── tables/
│   ├── index.md
│   ├── orders.md
│   └── customers.md
└── metrics/
    ├── index.md
    └── weekly_active_users.md
```

Example document with YAML frontmatter:

```yaml
---
type: BigQuery Table
title: Orders
description: One row per completed customer order.
resource: https://console.cloud.google.com/bigquery?p=acme&d=sales&t=orders
tags: [sales, revenue]
timestamp: 2026-05-28T14:30:00Z
---
# Schema
| Column | Type | Description |
|--------|------|-------------|
| `order_id` | STRING | Globally unique order identifier. |
| `customer_id` | STRING | FK to [customers](/tables/customers.md). |

# Joins
Joined with [customers](/tables/customers.md) on `customer_id`.
```

## Three design principles

1. **Minimally opinionated** — only a `type` field is required; producers
   determine their own content models.
2. **Producer/consumer independence** — separates knowledge writing from
   consumption; the format is the contract.
3. **Format, not platform** — vendor-neutral, no proprietary accounts or SDKs
   required.

## Reference implementations

Google shipped an enrichment agent that walks BigQuery datasets and generates
OKF concept documents with citations and schemas; a static HTML visualizer
that turns OKF bundles into interactive graph views; and three sample bundles
(GA4 e-commerce, Stack Overflow, Bitcoin datasets).

## Resources and next steps

- GitHub: https://github.com/GoogleCloudPlatform/knowledge-catalog/tree/main/okf
- Google Cloud's Knowledge Catalog was updated to ingest OKF and serve it to
  agents.
- The post encourages the community to read the spec, write producers and
  consumers, try the reference implementations, and contribute issues and PRs.

The post emphasizes that OKF is designed to evolve as an open standard, with
the format itself as the primary contribution rather than proprietary tooling.
