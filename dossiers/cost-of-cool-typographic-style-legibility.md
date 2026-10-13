---
type: Study Note
title: "The Cost of Cool: Typographic Style Legibility in Reading at a Glance"
description: A 31-person masked lexical-decision experiment finds lowercase and condensed Frutiger require longer exposure than uppercase and regular-width text, with case penalties amplified at smaller sizes, not a demonstrated cost of aesthetic appeal or real-world multitasking.
resource: https://doi.org/10.1177/1541931213601698
source: https://doi.org/10.1177/1541931213601698
tags: [typography, human-performance, visual-perception, digital-interfaces]
timestamp: 2026-10-12T20:28:10Z
---

# The Cost of Cool — Study Notes

**Authors**: Ben D. Sawyer, Jonathan Dobres, Nadine Chahine, and Bryan Reimer.  
**Published**: Proceedings of the Human Factors and Ergonomics Society 2017 Annual Meeting, pp. **833–837**; DOI printed on the first page.  
**Status**: Empirical conference proceedings paper; the supplied author-hosted copy reproduces the published five-page proceedings layout. The PDF does not describe its review procedure; do not equate proceedings publication with a full journal review. Read all pages, references, and three figures.  

## What It Is

A within-participant experiment on the **exposure duration needed for approximately 80% accurate word-versus-pseudoword judgments**, crossing letter height, width, and case. It investigates typography for glanceable electronic displays, not whether attractive typography is intrinsically unusable.

## Problem and Motivation

In an operational interface, reading competes with attention to the surrounding task. A seemingly cosmetic change can extend the time needed to encode text. The authors argue that typography should be evaluated through human performance rather than appearance alone, especially where milliseconds away from an operational environment might matter. The present experiment isolates reading; it does not measure that surrounding-task risk.

## Mechanism as an Idea

**31 native-English-speaking Boston-area participants**, **14 men and 17 women**, aged **31–72**, had Snellen acuity of at least **20/40** and passed self-reported health screening. Mean ages were **55.7 years** for men and **54.8** for women. Participants used optical correction as desired.

All stimuli used the **Frutiger family** in **eight conditions: 3 or 4 mm × condensed or regular width × upper- or lowercase**. They appeared on a high-resolution **2560 × 1440, 60 Hz** display in dim room illumination at approximately **70 cm**, without head restraint. Figure 1 illustrates the manipulations; it is not a comparison between decorative display families.

Participants classified strings as words or pronounceable pseudowords. The stimulus appeared between **200 ms masks**, after a **1,000 ms fixation cue**, and was followed by a response window of up to **5 seconds**. Each condition had **100 consecutive trials**; block order was randomized within participants. A one-up/three-down adaptive staircase targeted approximately **80% accuracy**, bounded by **16.7–1,000 ms**. Each participant's threshold was the median duration of the **final 20 trials**, not motor response time or total task completion time.

Larger glyphs and less compression may make useful letter features easier to discriminate. Case and nominal size are not independent in their visual consequences: the authors observe that prominent lowercase Frutiger elements are approximately **three-quarters** the size of their uppercase counterparts. Uppercase at a smaller nominal size can therefore approach the actual visual size of larger lowercase text. Crowding and letter-confusion explanations are plausible accounts, not independently manipulated mechanisms here.

## Results / Admissions

- **Lowercase required 26% more exposure time** than uppercase on average: case main effect **F(1,30) = 95.24, p < .01**.
- **Condensed text required 11.2% more exposure time** than regular width: width main effect **F(1,30) = 6.77, p = .01**.
- **4 mm text had lower thresholds than 3 mm text**: size main effect **F(1,30) = 35.85, p < .01**. The paper does not give a corresponding aggregate percentage penalty for the smaller size.
- Case interacted with size: **F(1,30) = 6.79, p = .01**. The uppercase advantage was larger at **3 mm**. Figure 3 shows the largest thresholds for small condensed lowercase text and within-subject standard-error bars; numerical cell means are not tabulated.
- **No other interaction was significant**, including the hypothesized increase in the condensed-width penalty at smaller sizes. The abstract's statement that lowercase and condensed text reduce performance “especially” when smaller should not be read as statistically established size moderation for both factors.
- The order test was nonsignificant: **Friedman χ² = 9.25, p = .24**. This is compatible with no detected order effect, not proof that randomization eliminated every learning effect.
- Regular-width lowercase conditions were compared with an earlier study by the same research group: **3 mm, t(57) = 1.23, p = .22; 4 mm, t(56) = .91, p = .37**. This provides cross-sample consistency for two conditions, not a formal equivalence test or independent replication of the complete factorial result.

The authors point to **3 mm uppercase** and **4 mm lowercase** having similar observed thresholds, while explicitly declining to claim absolute equivalence. Proposed high-legibility modes for operational contexts and restrictions on customization are recommendations, not interventions evaluated in the experiment.

## Analyst Takeaways

1. **Measure the cost relevant to the task.** Exposure thresholds for masked lexical decisions capture glance encoding, not paragraph readability, label search, aesthetic preference, or driving safety.
2. **Do not treat case as a size-free choice.** An uppercase advantage at a fixed nominal setting can partly purchase larger visible letters; compare actual glyph dimensions before attributing it to word shape or familiarity.
3. **Evaluate typography at its smallest intended use.** The size-by-case result shows that a change tolerable at a larger size can have a greater encoding cost when reduced.
4. **Avoid turning “cool” into a causal variable.** The paper manipulated height, width, and case, not beauty or brand expression. It does not condemn all stylized fonts or establish a general monospace advantage.

## Questions and Limitations

- A single type family, native-English sample, constrained health criteria, and single-task laboratory protocol limit generalization. No actual vehicle operation, secondary task, prolonged reading, or disability-specific condition was tested. The prediction that multitasking would amplify penalties remains untested here.
- No contrast-polarity comparison is reported; the schematic is not evidence for a dark-interface effect. Display luminance and stimulus contrast are not quantified in the methods. Findings cannot specify how much stronger or weaker these penalties become in dark UIs.
- Exact cell means, confidence intervals, and standardized effect sizes are not supplied. Percent-correct is held approximately constant by the staircase and not analyzed as a separate outcome.
- The paper says it offers **four hypotheses** but enumerates **five (a–e)**; its discussion then calls the replicated size result the first hypothesis although size was initially **(c)**. The substantive results are clearer than those labels.
- Monotype Imaging partly funded the work and supplied staff time and typographic expertise; Chahine was affiliated with Monotype.
- **Redistribution evidence**: the PDF states **“Copyright 2017 by Human Factors and Ergonomics Society.”** No explicit redistribution grant appears in the supplied copy. Author hosting does not supply permission for a public repository archive; retain the raw file in `archive/private/`.

## Vault Ideas Extracted

- [Typeface Legibility](/vault/typeface-legibility.md) — Supplies exposure-threshold evidence for size, compression, and case in one family, including size-by-case interaction and the distinction between nominal size and visible glyph size.
