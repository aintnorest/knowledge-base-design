---
type: Study Note
title: "The WebAIM Million — The 2026 report on the accessibility of the top 1,000,000 home pages"
description: Automated WAVE analysis of one million popular home pages detected likely WCAG A/AA failures on 95.9% in February 2026, reversing recent prevalence improvements without establishing full conformance or the causes of technology-related differences.
resource: https://webaim.org/projects/million/
source: https://webaim.org/projects/million/
tags: [accessibility, accessibility-standards, usability-evaluation, digital-interfaces, ux-metrics, assistive-technology]
timestamp: 2026-10-12T20:28:35Z
---

# The WebAIM Million 2026 — Study Notes

**Authors**: WebAIM, Utah State University; no individual author is named in the saved report.  
**Published**: February 2026 analysis; saved report last updated March 30, 2026.  
**Status**: First-party observational web-accessibility benchmarking report, not a peer-reviewed paper. Read the complete saved 2026 HTML, every category/language/technology table, and all six report charts; year-over-year comparisons are the report's own earlier analyses.  

## What It Is

The **eighth annual** automated assessment of **1,000,000 popular home pages**, using WAVE's stand-alone API. It quantifies detectable accessibility barriers and likely **WCAG 2.2 Level A/AA** failures, not disabled participants' complete experiences or the percentage of all websites that are accessible.

Its central finding is a reversal of gradual improvement in pages with detected failures: **95.9% in 2026**, versus **94.8% in 2025**. A scan with no detected errors is not proof of accessibility or conformance. The report says the fully conforming share must be lower than the **4.1%** with no detected failures; the scan alone establishes an **upper bound**, not a measured conformance rate or a quantified size of the remaining gap.

## Problem and Motivation

Accessibility failures are common enough to require attention to recurring fundamentals rather than isolated specialist fixes. Increasing page complexity can increase the absolute number of barriers even when their density falls. The report seeks to describe prevalence, trends, and associations with site characteristics; its benchmarking should not be mistaken for a controlled explanation of what caused the trends.

## Method as an Idea

- **Sampling frame**: the Tranco ranking, combining several sources of popular sites. Sites without a home page, pages returning errors such as 404, pages with fewer than **10 HTML elements**, and pages with more than **5,000 same-domain links** used for SEO were excluded.
- **Unit and stimulus**: one rendered home page per site, with scripts and styles applied before WAVE analyzes the DOM. These are pages, not whole sites or complete transactions. There is **no human participant sample** and no assigned user task.
- **Measures**: counts of distinct detected errors, pages with at least one error, element/image/input/heading/ARIA counts, and average errors within category, TLD, declared-language, and detected-technology groups. Errors are described as notable end-user barriers with a very high likelihood of A/AA failure; additional questionable patterns are reported separately.
- **Ancillary classification**: site categories were collected with **Amazon Web Services Bedrock AI**; additional tools detected technologies. The report does not provide classification-validation accuracy, detailed crawler settings, or an adjusted model.
- **Coverage boundary**: automated tests cannot detect every conformance failure. They can identify some missing semantics or numerical contrast failures but cannot establish whether all alternatives are meaningful, interactions work for disabled people, or journeys are independently usable. [Understanding WCAG 2.2](/dossiers/understanding-wcag-2-2.md) explains why a partial test cannot certify a criterion, full page, or complete process.

The percentages in the main failure table use **home pages as denominator**; image and input percentages use their respective elements. They are not interchangeable estimates of people affected or tasks that fail.

## Results / Admissions

### Overall errors and complexity

Across the sample, **56,114,377 errors** were detected, or **56.1 per home page**, up **10.1%** from **51** in 2025. The error-count chart shows a decline from roughly 60 in 2019–2020 to roughly 50 in 2021–2023, a rise to **56.8** in 2024, a fall in 2025, and a renewed rise in 2026. Absolute counts did not improve monotonically before 2026.

Pages averaged **1,437 elements**, up **14.3%** in one year from **1,257** in 2025, with more than **1.4 billion elements** across the sample. The chart shows sustained growth since **782** in 2019. Detected error density was **3.9%**, described as about one error per **26 elements**. This is a DOM-count ratio, not an observed probability of a disabled user's encounter: many structural elements are not independent user interactions.

The report explicitly rejects error density as a sufficient accessibility metric: adding many structural elements can dilute a ratio while adding barriers. The most popular **100,000** sites averaged **1,584 elements**, versus **1,318** among the least popular 100,000, approximately **20%** more. This is an association, not a causal popularity effect.

**20.5%** of pages had five or fewer errors and **30.4%** ten or fewer. Those are still pages with possible untested barriers; a small count does not establish a usable critical task.

### Six recurring failure types

These **six categories account for 96% of detected errors**, not 96% of every possible accessibility failure. The categories have remained the same across recent annual reports.

| Failure type | Pages in 2019 | Pages in 2025 | Pages in 2026 | 2025–2026 change, percentage points |
|---|---|---|---|---|
| Low-contrast text | **85.3%** | **79.1%** | **83.9%** | **+4.8** |
| Missing image alternatives | **68.0%** | **55.5%** | **53.1%** | **−2.4** |
| Missing form-input labels | **52.8%** | **48.2%** | **51.0%** | **+2.8** |
| Empty links | **58.1%** | **45.4%** | **46.3%** | **+0.9** |
| Empty buttons | **25.0%** | **29.6%** | **30.6%** | **+1.0** |
| Missing document language | **33.1%** | **15.8%** | **13.5%** | **−2.3** |

The percentage-point column is arithmetic from the reported rates, not a source-reported significance test. Two categories improved in 2026; four worsened. The saved bar charts corroborate these values and their long-term directions.

- **Contrast**: low-contrast text was the most common failure, averaging **34 distinct instances per page**, up **15%** from 2025. Its prevalence is evidence of unmet minimum contrast, not a new experiment validating the contrast threshold or an estimate of reading impairment severity.
- **Images**: more than **66.6 million images**, **66.6 per page**, up **13.6%** in a year. **16.2%** lacked alternative text, or **10.8 per page**; empty alternatives were not counted as missing. This share fell from **18.5%** in 2025 despite the increased image count. **45%** of missing alternatives were on linked images, and **one in four linked images** lacked alternatives, also leaving their links undescribed.
- **Alternative quality**: **10.8% of images that had alternatives** had questionable or repetitive alternatives, including generic words, filenames, and duplicates of nearby content. That denominator differs from all images. Presence alone does not establish meaningful equivalence; these flags are not all individually adjudicated failures. The report summarizes missing/questionable/repetitive alternatives as affecting more than one in four images.
- **Forms**: **6.9 inputs per page**, up **36%** over three years; **33.1% of inputs** were not properly labeled through the naming mechanisms recognized by the scan. This is not the same as the **51% of pages** with at least one missing-label failure.

### Structure and interaction-related diagnostics

Nearly **30 million headings**, **29.9 per page**, were detected, up **20.4%** in a year. Pages with no headings fell from **9.8% to 7.5%**, but skipped levels rose from **39% to 41.8%** of pages, with **1,206,444 instances**, about one per **25 headings**. **94.9%** of pages with an h6 also skipped levels; h6 counts more than doubled. WebAIM interprets this as suggesting headings often do not reflect actual document structure, not as a manually verified judgment of every affected page. Multiple h1s occurred on **18.1%**, up from **16.3%**; that diagnostic should not automatically be equated with a conformance failure.

Regions/landmarks appeared on **84.3%** of pages, up from **80.5%**; a main region on **46.1%**, up from **42.6%**; search landmarks on **18.8%**, up from **16.6%**. More structure was exposed, but its mere existence does not prove meaningful organization.

Ambiguous link wording appeared on **15.2%** of pages versus **13.7%** in 2025, averaging **5.3 instances on affected pages** versus **6.8**. Skip links appeared on **17.1%** versus **15.3%**; about **one in ten** was broken through inaccessible hiding or a missing target. Of **948,225 tables** on **143,575 pages**, **181,188 (19%)** had valid data-table markup; this does not establish that the other 81% were all data tables requiring that markup.

### ARIA, technology, and other associations are not causal rankings

The sample contained **133,589,803 ARIA attributes**, over **133 per page**, up **27%** in one year and more than sixfold since 2019. ARIA excluding landmark roles occurred on **82.7% of pages**, up from **79.4%**. Those pages averaged **59.1 errors**, versus **42** without ARIA: about **17 additional detected barriers**. The report explicitly says this **does not necessarily mean ARIA introduced the errors**, because ARIA pages were also more complex. It reports no adjustment that isolates ARIA's contribution.

**5.7%** of pages had an ARIA menu; **22% of those menus** lacked necessary markup/interactions according to the report. Labels/descriptions increased **28%**, to **31.4 per page**; hidden-content attributes, button roles, and focus-management attributes also increased substantially. Neither more ARIA nor fewer attributes is, by itself, an accessibility outcome.

The remaining tables describe substantial heterogeneity:

- **Categories**: government pages (**22,345**) averaged **42.4 errors**, **24.4% below** the overall mean; shopping (**95,039**) averaged **71.0**, **26.6% above**; sports (**15,640**) **71.4**, **27.3% above**. Category samples can overlap or have different complexity; these figures do not isolate policy or industry effects.
- **TLDs**: the sample represented **1,016** TLDs. The .gov group (**1,987 pages**) averaged **18.5 errors**, and .edu (**3,174**) **23.0**, versus **56.2** for .com (**444,978**). These are domain groups, not equivalent to the government/education category groups.
- **Declared languages**: English (**521,826 pages**) averaged **46.0 errors**; Chinese (**17,909**) **136.2**; Korean (**6,628**) **94.6**. The report compares common groups with **n > 5,000** but supplies no confound adjustment or evidence that language itself causes the differences.
- **Technologies**: more than **1,200 types** were detected. Example associations include WordPress (**252,302 pages**, **52.8 errors**), Astro (**5,472**, **9.0**), React (**45,673**, **43.5**), jQuery (**560,294**, **64.9**), Bootstrap (**240,869**, **63.3**), Shopify (**42,516**, **75.1**), and Prestashop (**5,044**, **143.2**). The report explicitly warns that correspondence with a technology cannot always be attributed to it. These are overlapping observational groups, not randomized product comparisons.
- **Advertising and other features**: most listed ad networks were associated with higher error counts, though several groups were below the overall mean. ReCAPTCHA appeared on **9.6%** of pages, associated with **7.7 more errors than average**; YouTube on **6.2%**, with **9.4 more**. OneTrust pages averaged **34.6**, FingerprintJS pages **112.4**; the suggested privacy/accessibility relationship is a hypothesis, not a tested causal mechanism.

The conclusion proposes that third-party frameworks, libraries, and automated or AI-assisted coding may underlie broader changes. **AI-assisted coding was not measured as an exposure** in the described analysis; “vibe coding” is explanatory speculation, not an established cause of the 2026 increase.

## Analyst Takeaways

1. **Fix recurring fundamentals without calling that complete accessibility.** Contrast, useful alternatives, labels, named controls, and document language account for most detectable errors; manual and user-centered evaluation must address what the scan misses.
2. **Keep denominator and unit visible.** Affected pages, missing images, unlabeled inputs, and barrier counts describe different things. None directly measures the proportion of users excluded.
3. **Prefer absolute barriers and task consequences over diluted density.** More scaffolding can improve a ratio without improving any journey. Counts also need severity and task context rather than becoming a standalone score.
4. **Do not rank tools as causal accessibility treatments.** Technology choice, complexity, content type, organizational practice, and overlapping features travel together in these observational tables.
5. **Protect meaning, not mere attribute presence.** More headings, landmarks, names, or ARIA are not proof that the structure or interaction is understandable and operable.

## Questions and Limitations

- The million pages are a large popularity-based frame, not a random sample of all web pages. Exclusions, home-page-only coverage, ranking changes, and single-snapshot rendering limit generalization. The report does not establish a fixed matched panel across years.
- No disabled participants, task-success outcomes, confidence intervals, regression coefficients, exact significance tests, or causal identification are supplied. “Significantly” in prose should not be converted into a particular p-value.
- Automated absence-of-error results leave semantic quality, behavior, other states, deeper pages, and complete processes unverified. Detection trends can also depend on rendering and engine behavior; the report does not fully document year-to-year instrument invariance.
- **Internal inconsistency**: the language section says **87.3%** defined a document language and lists **127,455** with none, approximately **12.7%**. The main failure table instead reports **13.5%** missing document language. The source does not reconcile those denominators/classifications; retain both rather than choosing one silently.
- **Chart-alt mismatch**: the complexity image visibly includes a **2026** point near **1,437**, but its alternative text describes growth only through **1,257 in 2025**. The chart and body supply the 2026 value. The conclusion's broad phrase about reversing recent improvements also needs qualification: annual error counts already increased in 2024, whereas failure prevalence followed a steadier improvement before 2026.
- **Edition identity**: the saved page has no `rel="canonical"`. On October 12, 2026, the final HTTPS URL https://webaim.org/projects/million/ returned **200**, while https://webaim.org/projects/million/2026 returned **404** without redirect. The source key is therefore **`url:webaim.org/projects/million/`** under the ingestion rule, not an invented working year permalink. This reused URL cannot guarantee future access to this edition; the dossier's year, update date, and immutable private saved bundle preserve the exact source. No stable live 2026 permalink was established.
- **Redistribution evidence**: the saved footer says **“©2026 WebAIM”** and links to Copyright & Terms of Use; the supplied source contains no explicit redistribution grant. Public availability is not permission to republish the saved article or its charts. The raw bundle belongs in the private archive and this dossier uses the canonical HTTPS URL.

## Vault Ideas Extracted

- [Automated Accessibility Testing Limits](/vault/automated-accessibility-testing-limits.md) — Supplies large-scale detectable-failure prevalence while explicitly separating no detected errors from accessibility or full conformance.
- [Color Contrast Minimum](/vault/color-contrast-minimum.md) — Documents **83.9%** page prevalence and **34** low-contrast instances per page in this 2026 sample, without claiming a new threshold-validation study.
- [Text Alternatives](/vault/text-alternatives.md) — Separates missing alternatives from questionable or repetitive supplied alternatives, emphasizing that presence is not meaningful equivalence.
