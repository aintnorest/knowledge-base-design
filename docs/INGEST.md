# Source Ingest Playbook

Use this playbook to ingest exactly one eligible source from `inbox/` into the
knowledge base.

## Repository Model

- `inbox/` is the transient drop zone for source files. Its contents are
  tracked by Git until ingest moves them out.
- `archive/` stores immutable raw source files when a local copy is available
  and its license permits redistribution.
- `archive/private/` stores immutable raw source files that may not be
  redistributed. It is not tracked by Git; this repository is public.
- `dossiers/` contains one human-readable study note per source.
- `vault/` contains atomic synthesis notes supported by one or more dossiers.
- `index.md` is the root table of contents.
- `log.md` is the authoritative source registry and append-only ingest history.
- `archive/index.md` is the archive manifest.
- `docs/TAXONOMY.md` is the controlled tag vocabulary.

Read `README.md`, `docs/TAXONOMY.md`, representative dossiers, and
representative vault pages before making changes. Follow their established
style where it does not conflict with this playbook.

## Tagging

All `tags:` frontmatter must use the controlled vocabulary in
`docs/TAXONOMY.md`: 3–6 tags per page, most central first;
`digital-interfaces` on every page whose subject is a software or screen-based
product; `accessibility` on every page whose central question involves disabled
people; at most one genre tag. Do not invent tags during ingest — if nothing
fits, use the nearest broader tag and flag the gap in the final report as a
candidate addition to `docs/TAXONOMY.md`.

## Candidate Reconciliation

Inspect source files in `inbox/`. Ignore `README.md`, hidden files, temporary
files, and other administrative files.

Identify each source and derive exactly one source key using the strongest
available evidence, in this order:

1. `doi:<identifier>` for a DOI or another stable publisher identifier such as
   `ssrn:<abstract-id>`
2. `isbn:<isbn-13>` for a book, using the ISBN-13 of the edition read without
   hyphens; a different edition is a different source
3. `arxiv:<base-id>` for an arXiv source, treating revisions of the same base
   ID as the same source unless the task explicitly requests a revision update
4. `url:<normalized-canonical-url-without-scheme>` for a web source, including
   standards and guidelines published as web pages. Derive the canonical URL
   from the page's `rel="canonical"` value when available, otherwise use the
   final HTTPS URL after redirects. Remove fragments and tracking parameters;
   normalize the host to lowercase and use one trailing-slash convention.
5. `sha256:<checksum>` for a local source with no stronger identifier

Search `log.md` for the exact source key before writing anything. The log is
the authoritative record: a matching key makes the candidate ineligible.

For an incoming source whose key cannot be established, use normalized title
and authors, then exact checksum, to establish the key. Filenames are
supporting evidence only. Dossier frontmatter, `archive/index.md`, and archive
metadata may corroborate an apparent historical inconsistency, but do not
supersede `log.md` as the eligibility record.

Do not re-ingest a source because another part of its earlier ingest is missing
or inconsistent. Report that inconsistency without repairing it unless the task
explicitly asks for repository repair.

If no eligible source exists, make no changes and report that result.

A source is also ineligible when its substance is operational instruction —
tool tutorials, plugin walkthroughs, shortcut references, export or handoff
settings, troubleshooting — with no stated principle, rationale, measured
result, or first-hand experience. Report it as "not eligible: operational
content" and leave it in `inbox/`.

A source is likewise ineligible when it is a showcase, inspiration collection,
or opinion piece that gives no rationale, evidence, or first-hand experience
for its claims. Report it as "not eligible: unsupported opinion" and leave it
in `inbox/`.

If several sources are eligible, select the one with the highest expected
long-term knowledge value. Consider strength of evidence, completeness,
relevance to existing topics, and potential for reusable synthesis. State the
selection rationale in the final report.

## Ingest Procedure

1. Read or extract the complete selected source before writing notes,
   including its figures: design sources often make their argument visually.
   For a PDF, use an available local extractor or install a lightweight
   library such as `pypdf` if necessary. For a saved web page, extract the
   article text with any HTML parser installed for the task. Do not add
   extraction tools as repository dependencies.
2. Choose a descriptive lowercase kebab-case slug. Never overwrite an existing
   archive, dossier, or vault file.
3. Decide where the raw source lives:
   - A local file whose license explicitly permits redistribution (Creative
     Commons, public domain, or an equivalent grant) moves to
     `archive/<slug>.<ext>` without modifying its bytes.
   - Any other local file — a book, a paywalled paper, a saved article, or
     anything whose license is unclear — moves to
     `archive/private/<slug>.<ext>` without modifying its bytes.
   - A source available only on the web retains its canonical URL; do not
     create a placeholder archive file.
4. Create `dossiers/<slug>.md` with OKF frontmatter containing:
   - `type: Study Note`
   - `title`
   - `description`
   - `resource` when known
   - `source: /archive/<filename>` for a source archived in `archive/`, or the
     canonical `https://` URL for a private or web-only source
   - `tags`
   - an ISO-8601 UTC `timestamp`
5. Write an evidence-grounded dossier matching the existing style. Adapt the
   headings to the source, but normally cover: what it is; the problem or
   motivation; the principle, pattern, or mechanism *as an idea* (how it works
   and why, not how to build it in a tool); important results, admissions, or
   experiences; analyst takeaways; questions or limitations; and Vault Ideas
   Extracted.

   Record the evidence behind each claim. For an empirical study, record the
   participants, stimuli or task, measures, and effect sizes, and note whether
   the effect has replicated or failed to replicate when known. For guidance,
   standards, and pattern sources, record the rationale the source gives and
   what evidence, if any, backs it. Keep "the source recommends" distinct from
   "the source shows."

   Record the model, not the manual. Do not reproduce tool steps, component
   APIs, design-token values, or troubleshooting lists; link the canonical page
   instead. Product-specific names may appear only where they identify a
   design decision or a limitation (for example, "the system's default button
   meets contrast on light surfaces only"). Note the version or date when
   guidance is likely to change, and the success-criterion version for
   accessibility standards.
6. Create or update zero to four genuinely reusable vault notes. Prefer
   updating an existing matching concept over creating a near-duplicate. Each
   vault note must be understandable independently and contain:
   - OKF frontmatter with `type: Synthesis`, `title`, `description`, `tags`, and
     an ISO-8601 UTC `timestamp`
   - a concise explanation
   - practical use and limitations where applicable
   - a Sources section linking to the new dossier
   - product-independent wording: name the principle, the evidence behind it,
     and the conditions where it stops holding; never a tool's feature, a
     component library's API, or a vendor setting in the body. Product
     specifics belong in the Sources bullet as evidence.
   - the note must remain correct if every product cited in Sources changed
     its implementation tomorrow.
7. Add the dossier and any newly created vault pages to `index.md`. Do not add
   a link already present.
8. Append a dated ingest entry to `log.md`. Do not rewrite prior entries. Its
   required form is:

   ```markdown
   * **Ingest**: `<source-key>` — `<title> dossier` at `/dossiers/<slug>.md` — canonical: <canonical-url-or-archive-path>
   ```

   The source key must be unique in the log. Keep related archive and vault
   changes in the same dated section.
9. For a locally archived source, public or private, append it to
   `archive/index.md`; list a private file as `private/<filename>`. Do not add
   a web-only source to the archive manifest. Raw archived sources are
   immutable; the manifest remains appendable.
10. Preserve unrelated content and pre-existing inconsistencies.

Use bundle-relative Markdown links such as `/dossiers/example.md` and
`/vault/example.md`.

## Verification

Before finishing, verify that:

- a successfully handled local source no longer exists in `inbox/`
- a locally archived file exists in `archive/` or `archive/private/` and
  retained the source checksum
- no file without an explicit redistribution grant was placed in `archive/`
  outside `private/`
- a dossier `source:` under `/archive/` points to an existing file, or a
  private or web-only `source:` is a canonical `https://` URL
- every Markdown link added or changed by the ingest resolves to an existing
  file
- all new Markdown files contain the required frontmatter
- the source key appears exactly once in `log.md` and its canonical reference
  matches the selected source
- no duplicate index or manifest entry was introduced
- the diff contains only files required for the ingest
- the dossier and any vault notes contain no tool steps, component APIs,
  token values, or troubleshooting content copied from the source
- `mise run lint` passes

Report the selected source, why it was eligible, where its raw file was
archived and why, files created or updated, pre-existing inconsistencies left
untouched, and whether every verification check passed.
