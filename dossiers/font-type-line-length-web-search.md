---
type: Study Note
title: The influence of font type and line length on visual search and information retrieval in web pages
description: Two web-task experiments find longer lines speed target-present search and shorter lines are preferred, but neither font nor line length measurably improves navigational information retrieval in the tested small-screen layouts.
resource: https://doi.org/10.1016/j.ijhcs.2005.08.015
source: https://doi.org/10.1016/j.ijhcs.2005.08.015
tags: [typography, layout, human-performance, usability-evaluation, digital-interfaces]
timestamp: 2026-10-14T21:32:27Z
---

# Font Type and Line Length in Web Search — Study Notes

**Authors**: Jonathan Ling and Paul van Schaik.  
**Published**: International Journal of Human-Computer Studies **64 (2006), 395–404**; available online October 11, 2005.  
**Status**: Peer-reviewed experimental journal article; supplied ten-page publication-layout PDF retains an “ARTICLE IN PRESS” running header. Read the complete text, four figures, two tables, and references.

## What It Is

Two experiments separating **finding a visually marked target**, **navigating to an answer**, and **liking a layout**. Their central contribution is a task boundary: a line-length advantage in isolated visual search does not automatically become a benefit in a complete information-retrieval task.

## Problem and Mechanism

Web typography guidance often imported print conventions or plausible but untested claims. Longer lines put the same content into fewer lines, potentially reducing the number of separate scan paths. Shorter lines can feel easier or more familiar without improving measured performance. These are interpretations; eye movements, familiarity, fatigue, and adoption were not directly measured.

The comparison used **Arial at 10 point versus Times New Roman at 12 point**, chosen to approximate physical size and preserve the amount of text, rather than equal nominal size. It does not isolate serif presence or match every glyph dimension. Figures 1 and 3 show wider, shallower content blocks as line length increases and a persistent left navigation area; typography changes spatial layout as well as individual letters.

## Study Design

### Experiment 1: target-present versus target-absent search

**72 participants**, **57 women**, were an opportunity sample tested in laboratory classes: **39 Arial, 33 Times**; **61% aged 25 or younger**, the remainder 26–50. All had normal/corrected vision, and 76% used the web at least daily. Font was between participants; **55, 70, 85, and 100 characters per line (cpl)** were within participants.

Participants completed eight practice and **72 randomized experimental trials**, seeing a target word and then a bitmap of a mock web page. They pressed a key for presence/absence within **five seconds**. Links were visually distinguished by color, boldness, and underlining, with target locations counterbalanced. Displays were **14-inch, 800 × 600**; viewing distance was unrestricted. Outcomes distinguished hit accuracy/time from correct-rejection accuracy/time, followed by paired preferences and seven-point aesthetic judgments.

### Experiment 2: finding and entering an answer

A separate **99-person** sample included **82 women, 17 men**, mean age **24, SD 7.1**; **52 Arial, 47 Times**, and 77% daily web users. Participants navigated five three-level sites with **30 pages each**, answering **40 questions** whose answers were one or two links from the home page. The four line lengths each appeared ten times; pages contained the same amount of text and **did not scroll**. One practice site and five practice questions preceded the task.

Correct-answer time and number of pages visited operationalized speed and navigation efficiency; accuracy was **96–98%** across conditions. Aesthetic ratings and paired preferences were collected afterward. Analyses used mixed ANOVAs and Bonferroni-adjusted pairwise comparisons.

## Results / Admissions

| Outcome | Evidence |
|---|---|
| Target-present speed | Line-length effect **F(3,210) = 13.10, η² = .038, p < .001**; 85/100 cpl faster than 55/70 |
| Target-present mean times, Arial | **1786 / 1805 / 1639 / 1699 ms** at 55/70/85/100 cpl |
| Target-present mean times, Times | **1752 / 1718 / 1511 / 1609 ms** at the same lengths |
| Target-absent accuracy | **F(3,210) = 2.77, η² = .004, p < .05**; 70 more accurate than 85 cpl |
| Target-absent accuracy means | Arial **86.04 / 88.89 / 84.05 / 85.75%**; Times **81.14 / 83.84 / 80.81 / 79.80%** |
| Other Experiment 1 performance | No significant font effects, interactions, hit-accuracy or rejection-speed effects |
| Experiment 2 performance | No significant font, length, or interaction effects on correct-answer time or pages visited |

The objective line-length effects were small. At 85 versus 55 cpl, target-present mean time fell **147 ms with Arial** and **241 ms with Times**, but that does not describe absent-target verification or navigation.

Shorter lines were preferred in both experiments. Experiment 1's line-length preference effect was **F(3,210) = 3.95, η² = .044, p < .05**, with 70 preferred over 100 cpl. Experiment 2's effect was larger: **F(3,291) = 29.00, η² = .224, p < .001**. Its 55/70/85/100 preference shares were **30.45/30.77/22.12/16.67%** after Arial and **40.07/29.08/20.21/10.64%** after Times. The reported interaction was **F(3,291) = 3.60, η² = .028**, with a questionable printed p value noted below.

Arial was preferred by about **72–74%** after Experiment 1, **χ²(1) = 14.63, w = .45, p < .001**. After Experiment 2, **58–60%** preferred Arial, but the comparison was nonsignificant, **χ²(1) = 2.92, w = .17, .05 < p < .10**. Experiment 1's four-item aesthetic scale was reliable in only half the combinations, so analysis used the overall-impression item: Arial rated higher, **F(1,67) = 5.63, η² = .007, p < .05**. Experiment 2's reliable scale found no effects.

The authors recommend **55–70 cpl for thorough reading**, longer lines for quick scanning, and Arial based on preference. Thorough prose comprehension was not directly compared here; the recommendation combines preference with an interpretation of task demands. Claims about increased site acceptance and future sans-serif familiarity are predictions, not outcomes.

## Analyst Takeaways

1. **Do not use search speed as a substitute for reading comprehension.** A visible-link detection result is narrower than processing prose or successfully navigating a site.
2. **Preference is an outcome, not proof of efficiency.** Short-line preference persisted when navigation measures did not change.
3. **Preserve positive and negative decisions separately.** Fast hits can coexist with poorer rejection accuracy; a layout optimized for discovering present information need not support determining absence.
4. **Relate typography to task and size.** [Typeface Legibility](/vault/typeface-legibility.md) distinguishes acuity and speed plateaus; this paper instead studies navigation and search, without establishing a general serif disadvantage.

## Questions and Limitations

- Small, non-scrolling desktop layouts, opportunity samples, predominantly young women, two bundled font settings, and dated rendering technology limit generalization to long articles, mobile screens, older readers, or disabled users. No direct independent replication of these full experiments is established here.
- Null tests are not equivalence tests; no confidence intervals or prespecified equivalence margins establish that all fonts or lengths perform identically.
- **Internal reporting inconsistencies:** four line lengths have six unique pairs, not the method's **“15 possible paired combinations.”** Experiment 1 preference percentages sum to **82.90% Arial and 95.96% Times**, despite the footnote saying they add close to 100 because of missing data; missingness is not quantified.
- Table 2 unexpectedly includes **Trebuchet** and labels the preceding task “visual search,” although Experiment 2 describes a two-font information-retrieval comparison. Its percentages do not directly support the binary preference percentages in the prose. Keep these streams separate.
- The interaction **F(3,291) = 3.60** is printed **p < .005**, which is inconsistent with the usual F-distribution tail for those degrees of freedom (approximately .014); do not reproduce the stronger threshold as settled evidence.
- **Redistribution evidence:** the first page prints **“© 2005 Elsevier Ltd. All rights reserved.”** No explicit redistribution grant appears. Archive the supplied PDF privately and cite the DOI URL.

## Vault Ideas Extracted

- [Line Length and Reading](/vault/line-length-and-reading.md) — Adds task-specific 55–100-cpl evidence separating faster target-present scanning, target-absent accuracy, navigation nulls, and strong short-line preference.
- [Typeface Legibility](/vault/typeface-legibility.md) — Adds a bounded Arial/Times performance null in web search and retrieval while distinguishing preference, approximate physical-size matching, and serif-category overgeneralization.
