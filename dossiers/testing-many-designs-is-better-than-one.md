---
type: Study Note
title: "Getting the Right Design and the Design Right: Testing Many Is Better Than One"
description: A 48-person paper-thermostat experiment finds lower ratings and less praise when designs are tested alongside alternatives, but no significant increase in substantial redesign suggestions.
resource: https://doi.org/10.1145/1124772.1124960
source: https://doi.org/10.1145/1124772.1124960
tags: [usability-evaluation, prototyping, design-process, user-research, digital-interfaces]
timestamp: 2026-10-15T04:37:29Z
---

# Testing Many Designs Is Better Than One — Study Notes

**Authors**: Maryam Tohidi, William Buxton, Ronald Baecker, and Abigail Sellen.  
**Published**: CHI 2006, Montréal, April 22–27, **pp. 1243–1252**, DOI **10.1145/1124772.1124960**.  
**Status**: Peer-reviewed randomized between-subjects usability experiment. Read the complete **10-page author copy**, including all eight figures, both tables, discussion, and references. Its publication identity matches the assigned DOI; the copy prints the ACM copyright notice and proceedings details.

## What It Is

A test of whether people give different feedback on the **same design** when it is the only option they encounter or one of three alternatives. The durable distinction is between **refining a selected design** and **learning whether that design should be selected at all**. Alternatives changed subjective evaluation, but did not reliably turn usability participants into generators of substantial redesign ideas.

## Problem and Proposed Mechanism

A lone prototype can imply commitment. Participants may avoid criticism to protect the designer, avoid seeming negative, or avoid blaming their own competence. Showing alternatives may signal openness and provide concrete comparisons. The authors propose these social and comparative mechanisms; they did not independently manipulate perceived commitment, measure fear of offending, or establish that lower ratings are objectively more accurate.

## Study Design

### Participants, prototypes, and tasks

**48 University of Toronto students or recent graduates**, **26 women and 22 men**, from varied disciplines were randomly assigned: **12** to each of three single-design conditions and **12** to the multiple-design condition. Compensation was **C$10**. An additional **12 pilot participants** helped refine the setup and instruments; they are not part of the main N.

Three low-fidelity paper prototypes represented a touch-screen **house climate-control system**, with matched intended functionality and fidelity but distinct interaction styles:

- **Circular:** dials and analog-clock representations.
- **Tabular:** familiar drop-down lists.
- **Linear:** horizontal timelines and sliders.

The figures show genuinely different representations, not colour variations. The same team designed all three; equal quality was intended, not empirically guaranteed. A second person simulated system responses while the main experimenter facilitated think-aloud use.

Each participant created weekend and vacation programs, reset date/time, and overrode the current temperature: **four tasks**. Multiple-condition participants performed the same tasks on all three designs, sequentially in counterbalanced order; after completing them they rated and discussed all three and could refer back to the prototypes. Single-condition participants were not told alternatives existed. Thus this is not simultaneous interaction with three screens, and total exposure and practice were greater in the multiple condition.

### Measures and analysis

A ten-point questionnaire covered four task-ease ratings, seven design dimensions, and overall usability. The analysis averaged the **first eleven items**, excluding the correlated overall item. Per-design single/multiple comparisons used **one-tailed Mann–Whitney U tests**.

For comments and suggestions, **24 randomly selected recordings** were analyzed: **six per condition**. An assessor extracted **337 statements**; two judges categorized positive/negative comments and superficial/substantial suggestions, with substantial suggestions separated into new versus borrowed ideas. Reliability is described as **85% agreement using Cohen's kappa, p < .001**; the wording does not clearly distinguish percentage agreement from the kappa coefficient. Two-tailed t-tests compared counts for the **same design**, not all three designs pooled against one.

## Results / Admissions

### Ratings became less favorable, not proven more accurate

| Design | Seen alone: mean (SD) | Seen among three: mean (SD) | Difference, alone minus multiple | One-tailed p |
|---|---|---|---|---|
| Circular | **9.08 (.53)** | **8.13 (1.10)** | **.95** | **.004** |
| Tabular | **8.83 (.56)** | **8.39 (.86)** | **.44** | **.064**, nonsignificant |
| Linear | **7.92 (.85)** | **6.89 (.91)** | **1.03** | **.014** |

Each cell has **N = 12**; the same multiple-condition participants supplied all three ratings. Differences are calculated from reported means on the ten-point scale. The authors interpret lower ratings as less inflated but explicitly acknowledge that the validity of positive or negative comments needs further study. Tabular familiarity is a proposed explanation for its weaker condition difference, not a randomized familiarity effect.

### Praise fell for every design; significant extra criticism was selective

Mean positive comments per participant, single → multiple for the same design, were **6.42 → 2.67 Circular (p = .045)**, **4.75 → 2.17 Tabular (p = .008)**, and **5.83 → 2.33 Linear (p = .025)**. Mean negative comments rose **1.83 → 2.50**, **1.50 → 4.08**, and **1.92 → 5.08**, respectively, but only **Linear** was significant (**p = .036**; others **.365/.182**).

The **Linear** positive/negative balance interaction was reported **p < .001**. Figures 5–7 distinguish total statements about all alternatives from statements about the target design. Comparing **70 negative comments across three designs** with **11.5 about a lone Linear design** is not a sixfold per-design effect and should not replace the matched comparisons.

Across the full sample, **3/12** multiple-condition participants explicitly rejected a prototype, versus **0/36** single-condition participants; another two multiple-condition participants volunteered a preferred design. These are descriptive observations, not an established effect on final product quality or purchasing.

### No reliable increase in substantial redesign suggestions

Total substantial suggestions per design, single → multiple, were **2.17 → 1.67 Circular (p = .623)**, **1.08 → 2.08 Tabular (p = .219)**, and **2.00 → 1.42 Linear (p = .539)**. Borrowing from alternatives occurred, but new substantial suggestions did not significantly increase. Linear superficial suggestions fell **1.75 → .33, p = .008**; other designs' superficial changes were nonsignificant.

The prediction that alternatives would generate more substantive improvement ideas was **unsupported**, not confirmed indirectly by greater criticism. This small study's nonsignificance is not proof of equivalence or that users cannot contribute to design. The authors recommend dedicated participatory-design approaches when the goal is co-creation rather than problem identification; those approaches were not compared here. End-of-session ideal-interface sketches are reserved for later research, not analyzed as evidence in this paper.

## Analyst Takeaways

1. **Use alternative concepts to test commitment, not just polish.** Comparative rejection can reveal that a direction should be abandoned rather than incrementally repaired.
2. **Treat praise as context-dependent.** Ratings from a single-prototype study are not directly interchangeable with ratings after comparative exposure.
3. **Separate problem evidence from solution proposals.** Fewer positive comments or more criticisms do not guarantee more actionable redesign suggestions.
4. **Make comparisons meaningful and neutral.** The study used functionally comparable but stylistically distinct alternatives; a token weak alternative or a visibly preferred option is not the tested intervention.

## Questions and Limitations

- One low-fidelity climate-control task with students/recent graduates and only **six analyzed recordings per condition**. No independent replication, longitudinal design outcome, higher-fidelity transfer, or professional-user validation is established by this source.
- Repeated task practice, longer exposure, comparative rating format, and the availability of alternatives change together. Counterbalanced order addresses order effects, not all exposure or social-mechanism explanations.
- Several per-design tests are reported without a stated multiplicity correction; no confidence intervals or standardized effects are supplied. The headline should preserve the nonsignificant Tabular rating difference and selective negative-comment result.
- **Reporting ambiguity:** methods call the prototypes matched in quality and make none deliberately worse; discussion calls Linear poorly designed and Tabular arguably least appropriate. These are interpretations, not independent quality benchmarks. Lower relative ratings do not establish which product should ship.
- **Internal figure error:** Figure 5's legend describes the Circular subset, but its x-axis caption says **“Tabular variation only.”** Table 2 and the figure caption identify the intended Circular comparison. Reliability's **“85%” kappa** wording is also ambiguous; do not silently convert it to a verified κ = .85.
- **Redistribution evidence**: the ACM notice permits personal/classroom copying only under its conditions and requires prior specific permission and/or a fee to republish, post on servers, or redistribute. Author availability supplies no explicit public redistribution licence; keep the intact PDF in `archive/private/`.

## Vault Ideas Extracted

- [Parallel Design Exploration](/vault/parallel-design-exploration.md) — Supplies comparative paper-prototype evidence for lower ratings and reduced praise, selective increased criticism and rejection, and no significant gain in substantial redesign suggestions.
