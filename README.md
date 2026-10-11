# Design Knowledge Base

A personal knowledge system for design — UX, UI, visual design, accessibility,
and the perception and behavior research underneath them — built on the
[Open Knowledge Format (OKF)](https://raw.githubusercontent.com/GoogleCloudPlatform/knowledge-catalog/main/okf/SPEC.md).

## Philosophy

This is a **zettelkasten-style** knowledge base with two layers:

- **Dossiers** are your personal study notes — one readable summation per
  source. You read these to *understand* what a study, book, standard, or
  article actually says. They are opinionated, concise, and written for human
  consumption.
- **Vault** pages are atomic, reusable ideas extracted from across sources. You
  write these when you notice a principle, pattern, or finding that might
  appear in multiple places. A vault page grows richer every time you encounter
  the same idea in a new dossier.

### What belongs here

This knowledge base holds **principles, patterns, research findings, design
decisions, and first-hand practice** — knowledge that stays true after the
tools and trends it came from change. It is not a documentation mirror or an
inspiration gallery.

- Scope is design broadly. Most sources apply to software products, but
  research on perception, attention, color, typography, and aesthetic response
  belongs here whether or not it involves a screen.
- A source earns a place by what it teaches: a principle and the evidence for
  it, a pattern and where it breaks, a design decision and its tradeoffs, a
  study and its result, a practitioner's account of what happened when a
  design shipped.
- A source does not earn a place by describing how to operate a tool. Tool
  tutorials, plugin walkthroughs, shortcut lists, and export settings are
  invalidated by the next release; link them, never restate them.
- Design-system and product documentation is admissible only for the *model*
  it exposes: its principles, the decisions behind its components, the
  tradeoffs it admits, and version-gated guidance worth dating.
- Showcases and opinion pieces with no stated rationale, evidence, or
  first-hand experience do not qualify.
- How AI systems work belongs in the sibling
  [intelligent-systems knowledge base](https://github.com/aintnorest/knowledge-base-intelligent-systems);
  how people perceive, use, and are affected by AI features belongs here.

## Directory Layout

```text
knowledge-base-design/
├── README.md              ← this file
├── index.md               ← table of contents (dossiers + vault pages)
├── log.md                 ← authoritative source registry and append-only ingest history
├── docs/
│   ├── INGEST.md          ← agent procedure for ingesting one source
│   └── TAXONOMY.md        ← controlled tag vocabulary
├── inbox/                 ← drop zone: put PDFs/files here to ingest (contents untracked)
├── archive/               ← immutable raw material, written once, never edited
│   ├── index.md           ← archive manifest
│   └── private/           ← local-only copies that may not be redistributed (untracked)
├── dossiers/              ← one file per ingested source: your readable study note
└── vault/                 ← atomic idea pages, one per reusable concept
```

## Workflow

The complete agent procedure is in [`docs/INGEST.md`](docs/INGEST.md).

### 1. Ingest

Drop a source into `inbox/`:

```bash
cp ~/Downloads/some-paper.pdf inbox/
```

An ingest agent (or you) reads the source and creates a
`dossiers/<source>.md` file — your readable study note. Local source files move
to `archive/`; sources available only on the web may use their canonical URL
directly without an archived copy.

This repository is public. A source is committed to `archive/` only when its
license permits redistribution; otherwise the local copy goes to the untracked
`archive/private/` and the dossier cites the canonical URL. Files waiting in
`inbox/` are never committed.

### 2. Read the Dossier

Open the dossier and read through your summation of the source. This is your
literature note — opinionated, concise, and written for you to understand the
work.

### 3. Extract to Vault

As you read, notice reusable ideas and create or update `vault/` pages. Each
vault page represents **one atomic concept** that may appear across many
sources over time.

**Rule**: A vault page should be understandable without reading any dossier,
but it should link to dossiers as evidence.

Example vault page structure:

```markdown
---
type: Synthesis
title: Minimum Target Size
description: ...
tags: [motor-accessibility, accessibility, digital-interfaces, human-performance]
timestamp: 2026-10-11T15:00:00Z
---

# Minimum Target Size

Small or crowded pointer targets cause missed and accidental activations,
and the cost falls hardest on people with tremor or limited dexterity.

## How It Works
1. Give every target a minimum hit area, independent of its visible size
2. Where a target must be smaller, reserve clear spacing around it instead
3. Exempt targets whose size is set by surrounding text or is essential

## Sources
- [WCAG 2.2](/dossiers/wcag-2-2.md) — Target Size (Minimum), Level AA: 24 by 24 CSS pixels, with a spacing exception
```

### 4. Update the Root Index

Add links to new dossiers and vault pages in `index.md`.

### 5. Register the Ingest

`log.md` is the authoritative list of ingested sources and the chronological
record of changes. Check its source key before ingesting. Append one entry for
each successful source using its stable key: `doi:…`, `isbn:…`, `arxiv:…`
(without a revision suffix), `url:…` (a normalized canonical URL without the
scheme), or `sha256:…` when no stronger identifier exists.

```markdown
## 2026-10-11 (WCAG 2.2)
* **Ingest**: `url:www.w3.org/TR/WCAG22/` — `Web Content Accessibility Guidelines (WCAG) 2.2 dossier` at `/dossiers/wcag-2-2.md` — canonical: https://www.w3.org/TR/WCAG22/
* **Vault**: Created [minimum-target-size](/vault/minimum-target-size.md)
```

## Conventions

- **OKF frontmatter** on every `.md` file: `type`, `title`, `description`,
  `tags`, `timestamp`
  (<https://raw.githubusercontent.com/GoogleCloudPlatform/knowledge-catalog/main/okf/SPEC.md>)
- **Dossier `type`**: use `Study Note`
- **Vault `type`**: use `Synthesis`
- **Tags**: only from [`docs/TAXONOMY.md`](docs/TAXONOMY.md)
- **Cross-links**: use bundle-relative paths (`/dossiers/...`, `/vault/...`)
- **Archive immutability**: never edit or overwrite raw files in `archive/`;
  `archive/index.md` remains appendable
- **Inbox handling**: do not modify source contents in `inbox/`; remove a source
  only by moving it to `archive/` after a successful ingest

## Tooling

[mise](https://mise.jdx.dev) pins Node and
[markdownlint-cli2](https://github.com/DavidAnson/markdownlint-cli2); rules live
in `.markdownlint-cli2.jsonc`. Raw files in `archive/` and `inbox/` are not
linted.

```bash
mise install          # install the pinned tools
mise run lint         # check every note
mise run lint:fix     # apply automatic fixes
```

## Viewing in Obsidian

The repo can be opened as an Obsidian vault for the graph view. The hub files
(`index.md`, `archive/index.md`, `log.md`, `docs/TAXONOMY.md`) link to nearly
every note and pull the graph into star clusters around them. To hide them,
paste this into Graph view → Filters → search:

```text
-path:index.md -path:log.md -path:docs -path:README.md
```

`.obsidian/` is gitignored; vault settings stay local.
