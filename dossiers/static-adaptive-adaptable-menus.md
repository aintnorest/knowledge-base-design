---
type: Study Note
title: A Comparison of Static, Adaptive, and Adaptable Menus
description: A 27-person menu-selection experiment finds an optimally arranged static split menu faster than an automatically changing one, while user customization helps when taken up and is preferred by a majority, without proving universal superiority of static layouts.
resource: https://doi.org/10.1145/985692.985704
source: https://doi.org/10.1145/985692.985704
tags: [interaction-design, human-performance, layout, cognitive-load, usability-evaluation, digital-interfaces]
timestamp: 2026-10-16T00:00:00Z
---

# A Comparison of Static, Adaptive, and Adaptable Menus — Study Notes

**Authors**: Leah Findlater and Joanna McGrenere.  
**Published**: CHI 2004, April 24–29, Vienna.  
**Status**: Peer-reviewed conference experiment; complete eight-page supplied paper read, including figures and tables. Spaced-letter extraction was checked against page images for the numerical results.

## What It Is

A controlled comparison of three **split menus**, separating who controls change from whether personalization is useful:

- **Static**: locations remain unchanged during use; the top partition is prepopulated with the four most frequently requested items in the experimental sequence.
- **Adaptive**: the system changes the partition using frequency and recency of selection.
- **Adaptable**: the person chooses which items occupy the top partition and their order.

The comparison is not between an arbitrary static menu and every possible adaptive design. The static condition has advance knowledge of task frequencies; the adaptive condition moves items rather than retaining duplicate commands in their original locations.

## Problem and Mechanism

A shorter route to frequently needed commands can reduce pointing and search. But moving commands also changes where people expect to find them. Personalization therefore trades access savings against repeated search, predictability, and the cost of customization.

The adaptable condition supplies explicit control, but that control is useful only if people recognize its value and use it. The authors propose demonstrating useful customization and possibly combining suggestions with user control. These are recommendations motivated by the findings, not separately tested interventions.

## Study Design

**Participants**: **27 undergraduates**, ages **18–39**, **21 women and six men**; ten self-described novice computer users, 16 intermediate, one expert. Participants were paid and offered a speed bonus. Eight pilot participants are mentioned separately.

**Task**: select prompted items in three menus modeled on File, Format, and Insert. The sequences derive from **20 weeks of one administrative assistant's usage**, with **788 selections** in these menus. Familiar command labels were replaced with cities, drinks, occupations, and other semantic sets to reduce prior-software knowledge. This is an abstract selection task, not document production.

**Design**: within-person menu comparison, crossed with three structurally equivalent labeling schemes; Latin squares counterbalanced condition and scheme orders. Each condition had **two identical 200-selection blocks**. Block 1 was familiarization; Block 2 supplied the performance analysis. Customization was available only between blocks, with extra time permitted. The adaptable menu started without promoted items, while the static and adaptive conditions started with the task's optimal four-item top partition.

**Measures**: total Block 2 selection time, errors, customization behavior and duration, and ranked overall preference, efficiency, errors, frustration, and initial ease. An incorrect selection had to be corrected, so error costs were also reflected in time. Customization time was recorded separately, not included in Block 2 selection time.

## Results

### Time and customization

Table 2 reports the following **seconds per 200-selection block**, not seconds per selection:

| Menu | Block 1, all 27 | Block 2, all 27 | Block 2, 22 who customized |
|---|---:|---:|---:|
| Static | 327.23 | 306.51 | 301.76 |
| Adaptable | 410.71 | 318.80 | 300.72 |
| Adaptive | 354.22 | 331.62 | 326.86 |

- Menu type affected time: **F(1.44,34.64) = 12.54, p < .001, partial η² = .343**. Menu and presentation order interacted: **F(2.89,34.64) = 6.14, p = .002, partial η² = .338**, using Greenhouse–Geisser correction.
- **Static was faster than adaptive in every order**: differences **20.787, 29.478, and 25.048 seconds**, Bonferroni-adjusted **p = .002, < .001, < .001**, with pairwise partial η² **.681, .719, .810**. The overall means differ by **25.11 seconds**, calculated as **7.6% less time relative to adaptive**.
- **Adaptable was faster than adaptive only when not encountered first**: differences **26.871 and 28.854 seconds**, **p = .041 and .026**, partial η² **.556 and .500**. In these orders it did not significantly differ from static. When adaptable came first, it was **42.327 seconds slower than static**, **p = .001**, partial η² **.672**, and did not significantly differ from adaptive.
- **22/27** customized in a task-relevant way; three did not customize and two appeared not to understand the process. **Four of these five** encountered adaptable first. Mean customization time across all 27 was **142 seconds**. The 22-person subgroup's similar static/adaptable means are descriptive and selected by behavior, not an equivalence test or a randomized customization effect.

### Errors and preference

Mean Block 2 error counts were **6.8 static, 6.6 adaptable, and 6.9 adaptive**. An order-by-menu interaction was reported, **F(4,48) = 2.94, p = .030**, but no Bonferroni-adjusted pairwise error contrast was significant.

**15/27** preferred adaptable, **8/27** adaptive, and **4/27** static; the three-way first-choice distribution differed from equal frequencies, **χ² = 6.89, p = .032**. The planned adaptable–static preference contrast was significant (**p = .012**); **adaptable–adaptive was not**. The majority count alone does not establish a statistically supported preference over both alternatives.

Adaptable was ranked most efficient by **16**, initially easiest by **17/26**, and most frustrating by only **1/26**. Adaptive was most frustrating for **15/26**. Six participants explicitly criticized adaptive inconsistency. Other participants liked its help before learning the menu. Perceived efficiency and measured time did not fully agree.

## Analyst Takeaways

1. **Protect learned locations, not simply a static aesthetic.** This adaptive movement strategy lost to an optimally configured stable menu; it does not establish that optional duplicate shortcuts are harmful.
2. **Treat customization uptake and setup cost as part of the design.** A fast customized state is not free, and easy manipulation did not ensure everyone understood why to customize.
3. **Separate preference, selection time, and errors.** A majority preferred a condition that did not beat static on measured speed; no reliable pairwise error advantage appeared.
4. **Do not turn a nonsignificant difference into equivalence.** The source's “not slower” language is stronger than its null contrasts establish.

## Questions and Limitations

- A short laboratory session, homogeneous undergraduate sample, one person's command distribution, and repeated sequences limit generalization to changing work, expert habits, unfamiliar commands, and long-term personalization. Accessibility is proposed as future work, not tested.
- The optimal static starting state and initially empty adaptable partition are deliberate but asymmetric. Fine control of order was also available only in adaptable. Block 2 omits setup time; it does not establish a net time saving over a whole work period.
- Spatial predictability is a plausible explanation supported by comments, not an isolated causal variable. Exposure to another split-menu example before customization is confounded with presentation order; “guide by example” was not independently randomized.
- **Source reporting issues**: the methods say four top items “always” appear in all conditions, but later specify the adaptable partition starts empty and can contain fewer than four. Table 2 labels its mixed 27/22-person summary “N=27”; subgroup headings clarify the denominator. Preference contrast notation prints **χ²(2,27) = 6.37, p = .012**, although that p-value corresponds to a one-degree-of-freedom contrast, not two. Missing questionnaire data are disclosed: two for perceived errors, one each for frustration and initial ease. These are retained rather than silently normalized.
- No confidence intervals are given. Independent replication of this exact experiment is not established by the supplied paper. The later [adaptive-interface design-space study](/dossiers/design-space-adaptive-graphical-interfaces.md) tests different toolbar designs and qualifies a blanket anti-adaptation conclusion; it is not a direct replication.
- **Redistribution evidence**: the first-page ACM 2004 notice permits personal/classroom copying but requires specific permission and/or a fee for republication, server posting, or redistribution. No public-repository redistribution grant is supplied; retain the raw PDF privately.

## Vault Ideas Extracted

- [System-Changed versus User-Changed Interfaces](/vault/adaptive-versus-adaptable-interfaces.md) — Defines control of change and supplies conditional speed, uptake, setup-cost, and preference evidence.
- [Consistency and Convention](/vault/consistency-and-convention.md) — Adds direct stable-location evidence while limiting it to the tested moving split menus and task-optimal static comparison.
