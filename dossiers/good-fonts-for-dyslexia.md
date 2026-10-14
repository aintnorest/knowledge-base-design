---
type: Study Note
title: Good Fonts for Dyslexia
description: A 48-person dyslexia study finds Arial Italic slower than three upright fonts and category differences in fixation duration, but not category-level reading-time gains or a demonstrated OpenDyslexic advantage.
resource: https://doi.org/10.1145/2513383.2513447
source: https://doi.org/10.1145/2513383.2513447
tags: [typography, cognitive-accessibility, accessibility, human-performance, digital-interfaces]
timestamp: 2026-10-14T21:32:27Z
---

# Good Fonts for Dyslexia — Study Notes

**Authors**: Luz Rello and Ricardo Baeza-Yates.  
**Published**: ACM ASSETS 2013, October 21–23, Bellevue, Washington; DOI **10.1145/2513383.2513447**.  
**Status**: Peer-reviewed conference experiment. Read the complete eight-page supplied author-layout PDF, including six figures, results table, references, and first-page ACM notice.

## What It Is

A within-person comparison of twelve fonts for silent Spanish prose reading by people with diagnosed dyslexia. It distinguishes **whole-text reading time, mean fixation duration, and subjective preference**, while using a literal comprehension question to filter trials rather than estimating comprehension improvement.

The strongest speed result concerns **Arial Italic**, not a universal serif/monospace rule. The category-level results support shorter fixations for upright, sans-serif, and monospaced settings, but do **not** show statistically significant whole-text reading-time advantages for those categories.

## Problem and Mechanism

Dyslexia guidance commonly recommends particular fonts without objective font comparisons. Fonts explicitly marketed for dyslexia might differentiate letter shapes, but that rationale is not itself evidence of faster or more accurate reading. Longer fixations can indicate greater processing demands; their relation to total reading time is imperfect because fixation count and rereading also matter.

The paper proposes combining performance with preference rather than naming a winner from a raw mean ranking. Figure 6 separates an ordering by means from the much sparser ordering by statistically significant comparisons: many apparent rank differences remain unestablished.

## Study Design

**48 participants**, **22 women and 26 men**, ages **11–50**, mean **20.96, SD 9.98**, presented clinical documentation of dyslexia and had normal vision. Twenty-six attended school/high school, nineteen were studying or had completed university, and three were outside those groups. Recordings with less than **75% captured samples** were discarded, leaving **46 valid recordings**. The paper does not supply the final per-font counts after comprehension filtering.

Each participant read **twelve 60-word texts** adapted from introductory paragraphs of one Spanish book, matched for genre/style and approximate lexical properties. Mean word length ranged **4.92–5.87 letters**. Texts excluded numerical expressions, acronyms, and foreign words. Font/text combinations were counterbalanced, with **14-point, left-aligned black-on-white** text and columns no longer than 70 characters. Equal point size did not equalize x-height, width, weight, or actual line wrapping.

The twelve fonts were Arial, Arial Italic, Computer Modern Unicode (CMU), Courier, Garamond, Helvetica, Myriad, OpenDyslexic, OpenDyslexic Italic, Times, Times Italic, and Verdana. Figure 1 visibly shows bundled differences in stroke, width, shape, and slant.

Eye tracking used a **17-inch, 1024 × 768** display at about **60 cm**, individually calibrated. Sessions lasted about twenty minutes. Participants silently read, then answered one three-option literal comprehension question without looking back; incorrect trials were excluded. Five-point liking ratings followed. Reading time and fixation duration correlated **r = .67, p < .001**; liking and time correlated only **r = −.13**.

Non-normal distributions motivated Friedman repeated-measures tests for fonts, Wilcoxon post hoc comparisons with Bonferroni correction, and Wilcoxon category comparisons. The paper calls the post hoc method a **rank-sum** test, leaving unclear how participant pairing was preserved.

## Results / Admissions

### Individual fonts

Font effects were significant for reading time, **χ²(11) = 31.55, p < .001**, fixation duration, **χ²(11) = 93.63, p < .001**, and preference, **χ²(11) = 79.6119, p < .001**.

| Font | Mean reading time, seconds | Mean fixation, seconds | Mean liking, out of 5 |
|---|---|---|---|
| Arial | **28.35 ± 12.39** | **.24 ± .07** | **3.60 ± 1.13** |
| Arial Italic | **34.99 ± 16.60** | **.28 ± .08** | **2.90 ± 1.10** |
| CMU | **29.58 ± 12.05** | **.27 ± .08** | **3.31 ± .98** |
| Courier | **29.61 ± 10.87** | **.22 ± .05** | **3.14 ± 1.39** |
| Helvetica | **31.05 ± 15.04** | **.24 ± .06** | **3.62 ± 1.08** |
| Verdana | **31.16 ± 13.03** | **.23 ± .07** | **3.79 ± .98** |
| OpenDyslexic | **29.17 ± 15.79** | **.26 ± .07** | **2.57 ± 1.15** |
| OpenDyslexic Italic | **29.68 ± 14.44** | **.26 ± .07** | **2.43 ± 1.27** |

Arial Italic took longer than **Arial (p = .011), CMU (p = .011), and Helvetica (p = .034)**. Its mean was **6.64 seconds, approximately 23%, above Arial**; this is an unstandardized descriptive contrast, not a reported standardized effect or individual improvement guarantee. Only those three reading-time comparisons are identified in the results.

Courier had shorter fixations than six fonts, including Arial (**p = .046**) and CMU, Garamond, Times Italic, and Arial Italic (**p < .001**). Helvetica beat Arial Italic, CMU, and Garamond on fixation duration. Sixteen of sixty-six fixation comparisons were significant; a rank order does not imply all adjacent fonts differ.

Verdana and Helvetica received high preference ratings, including significant advantages over both OpenDyslexic variants. Arial was preferred to Arial Italic and OpenDyslexic Italic. OpenDyslexic had **no demonstrated reading advantage**; absence of superiority is not proof of identical performance for every dyslexic reader.

### Font categories: fixation benefits, reading-time nulls

| Contrast | Mean fixation duration and test | Mean reading time and test |
|---|---|---|
| Italic versus corresponding upright fonts | **.27 vs .25 s; p = .040** | **32.35 vs 29.74 s; p = .09**, nonsignificant |
| Serif versus sans-serif families | **.26 vs .24 s; p = .008** | **31.53 vs 30.80 s; p = .2021**, nonsignificant |
| Courier versus proportional upright serif families | **.22 vs .26 s; p < .001** | **29.61 vs 31.53 s; p = .159**, nonsignificant |

The monospace comparison is **one Courier design against CMU/Garamond/Times**, not all monospaced versus all proportional fonts. Category preference tests were nonsignificant. No standardized effect sizes or confidence intervals are reported for these contrasts.

The authors recommend Helvetica, Courier, Arial, Verdana, and CMU, discourage Arial Italic, and suggest use in text-heavy systems. Their claim that these settings should not harm people without dyslexia is untested: a non-dyslexic comparison is explicitly future work. The method's comprehension filter cannot demonstrate better comprehension or reduced reading errors.

## Analyst Takeaways

1. **Accessibility labels do not establish effectiveness.** OpenDyslexic's design rationale did not translate into a demonstrated advantage in this task; some conventional fonts were preferred.
2. **Choose the endpoint deliberately.** Shorter fixations can coexist with no detectable total-time difference, so “improved reading performance” needs the named measure.
3. **Do not collapse dyslexia into low vision.** [Psychophysics of Reading: Font Effects](/dossiers/psychophysics-of-reading-font-effects.md) compares acuity thresholds in print; here diagnosed dyslexia with normal vision is tested on short screen texts at one nominal size.
4. **Preserve individual choice and evaluate actual reading.** This is an analyst implication of weak liking/time association and bundled font differences, not a tested customization intervention.

## Questions and Limitations

- Short Spanish passages, a single display, one size, no non-dyslexic control, broad age range, and comprehension-based exclusions limit transfer to sustained reading, other languages, errors, or comprehension. No independent direct replication is established by this source.
- Font size was not matched by x-height; comparisons bundle letter geometry and spacing. The result cannot uniquely identify serif presence or monospacing as a cause.
- **Internal scope inconsistency:** abstract/conclusion say categories significantly improved reading performance; the detailed results and discussion explicitly limit significance to fixation duration, not reading time.
- The discussion claims Arial differed in reading time from **OpenDyslexic Italic**, but the results list only Arial Italic versus Arial/CMU/Helvetica, and Figure 6b agrees with the latter. Do not treat the additional comparison as established.
- Category preference prose incorrectly labels rating units as **seconds** and prints **33.14** on a five-point scale. Its italic mean **3.73** also conflicts with individual italic means **2.90/2.86/2.43**; the monospace/proportional mean labeling conflicts with Courier's **3.14** table value. These category-rating summaries are unreliable as printed.
- **Redistribution evidence:** the visually inspected ACM notice permits personal/classroom copies but requires permission/fee for republication, posting on servers, or redistribution. Copyright is held by the owner/authors with publication rights licensed to ACM; no public redistribution grant appears. Keep the PDF private.

## Vault Ideas Extracted

- [Typeface Legibility](/vault/typeface-legibility.md) — Adds dyslexia-specific twelve-font screen evidence distinguishing fixation duration, total reading time, preference, and nominal-size confounds without endorsing a universal font category.
- [Cognitive Accessibility User Needs](/vault/cognitive-accessibility-user-needs.md) — Adds diagnosed-dyslexia evidence against assuming a specially labeled font improves reading and separates short-task measurements from comprehension and individual accommodation needs.
