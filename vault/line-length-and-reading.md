---
type: Synthesis
title: Line Length and Reading
description: Characters per line, physical width, and viewing angle describe different constraints; search speed, comprehension, and preferred measure can diverge, so screen reading has no established universal line-length optimum.
tags: [typography, layout, human-performance, digital-interfaces]
timestamp: 2026-10-14T21:39:20Z
---

# Line Length and Reading

Line length changes both the path through text and the shape of the text block.
Longer lines can reduce line changes and scrolling, yet a layout that speeds
scanning need not improve comprehension or feel easiest to read. Choose measure
for the task and reader rather than treating one character count as a universal
optimum.

## What Is Being Measured

- **Characters per line (cpl):** how much text fits before wrapping; proportional
  lettering and word lengths make this an approximate description of a passage.
- **Physical width:** the space occupied on the display, not the amount of text.
- **Visual angle:** the width as seen from the reader's viewing distance.

Increasing type size within fixed margins reduces cpl; holding cpl constant
instead expands physical width. Changing a typeface can also change wrapping.
Record these separately, alongside spacing, margins, viewport height, and text
movement. [Typeface Legibility](/vault/typeface-legibility.md) explains why equal
point sizes do not equalize visible letter dimensions.

More characters can require more fixations per line but fewer overall lines and
return sweeps. Reduced scrolling can contribute to speed differences; locating
the next line can become harder at long measures. A critical review treats cpl
as a useful explanatory variable, but neither the upper useful limit nor the
relative contributions of return sweeps and scrolling are settled. Scrolling as
a cue to line location and familiarity as a source of preference are proposed
mechanisms, not isolated findings.

## Evidence Depends on the Reading Task

A **72-person** visual-search experiment compared **55, 70, 85, and 100 cpl**.
Targets were visually distinguished links, not passages to understand. Present
targets were found faster at **85/100 than 55/70 cpl**, with a small line-length
effect (**η²=.038**). Absent-target judgments were more accurate at **70 than
85 cpl**, with a still smaller effect (**η²=.004**). Faster discovery therefore
did not imply better verification of absence.

A separate **99-person** navigation experiment found no significant line-length
effect on correct-answer time or pages visited. Shorter lines nevertheless had a
strong preference advantage (**η²=.224**). Both experiments used small desktop
layouts without scrolling; neither tests sustained prose comprehension. Their
recommendation of **55–70 cpl** for thorough reading combines preference and
interpretation rather than a direct comprehension comparison.

The critical review preserves conflicting sustained-reading results:

- A **48-person** experiment with approximately 800-word passages found
  **100 cpl faster than 25**, but no other significant length comparisons.
- A **20-person** substituted-word detection study found no time or accuracy
  differences across **45/76/132 cpl**. It did not reproduce the long-line speed
  advantage, although task and layout differences prevent a clean replication
  comparison.
- A richer comprehension test favored **55 over 100 cpl**, without a reading-speed
  difference. The review supplies no sample size or numerical effect estimate
  for this comparison; it is secondary evidence, not a pooled result.

Moderate lines were often judged easiest even when longer lines were faster.

## Practical Use

- Decide whether the task is finding a marked item, checking absence, navigating,
  proofreading, or learning from sustained prose before optimizing line length.
- Measure comprehension, errors, time, and preference separately; a fast scan or
  favorable comfort rating cannot stand in for understanding.
- Treat moderate measures as starting hypotheses, not mandatory limits. Compare
  realistic alternatives using representative content, readers, and devices.
- Keep type size usable while adjusting measure. Do not fit more characters by
  shrinking or squeezing letters without evaluating the identification cost.
- Assess wrapping, spacing, margins, columns, and scrolling together in use, but
  distinguish a successful layout package from an isolated causal font effect.

## Limitations

The evidence is largely small-sample, desktop-era research with dated rendering,
limited measures, and heterogeneous reading tasks. The critical review is not a
systematic review or meta-analysis; its numerical examples are secondary reports
and do not supply a contemporary mobile or disability-specific prescription.

Search-study nulls are not equivalence tests. Its preference and interaction
reporting contains inconsistencies documented in the dossier; the disputed
interaction p value is not used here. The studies do not establish long-term
fatigue, a safe maximum width, or an optimal cpl range for every language,
viewport, magnification setting, and reader.

## Sources

- [The influence of font type and line length on visual search and information retrieval in web pages](/dossiers/font-type-line-length-web-search.md) — Separates present-target speed, absent-target accuracy, navigation nulls, and short-line preference across 55–100 cpl; does not test sustained comprehension.
- [How physical text layout affects reading from screen](/dossiers/physical-text-layout-reading-from-screen.md) — Distinguishes cpl, width, and visual angle and reviews conflicting speed, comprehension, preference, and scrolling evidence without a universal optimum.
