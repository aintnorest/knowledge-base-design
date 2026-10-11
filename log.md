---
type: Log
title: Knowledge Base Source Registry and Ingest Log
description: Authoritative registry of ingested sources and chronological history of their archive, vault, and taxonomy changes.
tags: [log, source-registry, history, ingest]
timestamp: 2026-10-11T00:00:00Z
---

# Knowledge Base Source Registry and Ingest Log

Each `**Ingest**` entry registers exactly one source. Its source key is the
authoritative duplicate-detection record: `doi:…`, another stable publisher ID
such as `ssrn:…`, `isbn:…` (ISBN-13 of the edition read), `arxiv:…` (without a
revision suffix), `url:…` (normalized canonical URL without the scheme), or
`sha256:…` when no stronger identifier exists. Do not add a second ingest entry
for a registered key; append subsequent maintenance as a non-ingest event such
as `**Taxonomy**` or `**Retag**`.

## 2026-10-11 (Repository created)

* **Setup**: Created the repository structure, [ingest playbook](/docs/INGEST.md), and starting [tag taxonomy](/docs/TAXONOMY.md), adapted from the intelligent-systems knowledge base.
