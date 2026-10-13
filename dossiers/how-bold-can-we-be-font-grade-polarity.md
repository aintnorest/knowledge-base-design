---
type: Study Note
title: How bold can we be? The impact of adjusting font grade on readability in light and dark polarities
description: Two remote studies find faster reading in light mode and no detected paragraph-fluency effect of font grade in one tested variable typeface, while preference remains balanced and reporting inconsistencies limit precise interpretation.
resource: https://doi.org/10.1145/3544548.3581552
source: /archive/how-bold-can-we-be-font-grade-polarity.pdf
tags: [typography, visual-perception, human-performance, digital-interfaces]
timestamp: 2026-10-12T20:28:55Z
---

# Font Grade and Display Polarity — Study Notes

**Authors**: Hilary Palmén, Michael Gilbert, and David Crossland; Google.  
**Published**: Proceedings of the **2023 CHI Conference on Human Factors in Computing Systems**, April 23–28, 2023, Hamburg; **11 pages**.  
**Status**: Peer-reviewed CHI research paper; read the complete ACM-formatted PDF, including seven figures and five tables. The first page explicitly licenses the work under Creative Commons Attribution International 4.0.  

## What It Is

Two remote experiments comparing reading in light and dark modes while systematically changing **font grade**: stroke boldness without changing character advance widths or causing text reflow. The paper reports **459 analyzed participants**, comprising **126 desktop word-pair readers** and **333 Android paragraph readers**.

Light mode was faster in both settings. Grade did not produce a detected paragraph-fluency effect, nor a detected dark-mode word-pair benefit. Some heavier light-mode grades improved word-pair reading. These results do not establish that grade compensates for dark-mode halation, nor that every typeface can be made arbitrarily bolder without cost.

## Problem and Motivation

Ordinary font-weight changes can alter text width and line breaks. Grade offers a way to change apparent stroke strength without simultaneously changing layout. The authors ask whether it can preserve or improve readability across polarity, especially given popular claims that bright strokes on dark backgrounds spread optically and should be adjusted.

Figures 1 and 3 illustrate the distinction: increased weight moves text to another line, while increased grade preserves the paragraph's line structure; the same grade sequence produces visibly different strokes for the two reading formats. Figure 2 compares light/dark specimens of a different display typeface to motivate halation. It is an illustration, not an experimental halation measurement.

## Mechanism as an Idea

Grade separates stroke-strength adjustment from character width, allowing a more controlled typography comparison than comparing unrelated fonts or conventional regular/bold styles. However, it does not isolate every relevant variable: letter spacing, starting weight, text size, device rendering, luminance, and task can all change the result.

The paper proposes luminance and light spread as explanations for polarity differences. Neither pupil size nor halation was directly measured; a comparative visual-clarity question is not a selective physiological test of halation. The authors acknowledge that they have not disentangled the light-mode advantage from greater luminance.

### Study 1: self-paced word-pair reading

**184** Mechanical Turk participants were recruited and **126** retained after cleaning. About **79.2%** of retained readers were ages **25–44**; the reported age range stops at **64**. Each reader saw both polarities and five grades of **Roboto Flex**, with familiar single- and two-syllable words drawn from the Dale–Chall list. Order and words were randomized. Text was **16 px**, with a medium starting weight and fixed letter spacing; these identify the stimulus, not a general recommended setting.

Readers pressed the space bar when they had read a pair, stopping the timer, and reproduced it on a second screen. A string matching more than **40%** by a Levenshtein-based comparison counted as read. This measures self-paced reading plus the decision and keypress, not a masked minimum exposure threshold. The paper describes **56 presentations**, nominally training plus five questions per grade in both modes.

### Study 2: paragraph reading

**410** Cint US panel respondents were screened for Android-phone completion and recruited to be gender-balanced and age-representative. The analysis retained **333**, including substantial representation through ages **60–69 (19.5%)** and **70+ (4.5%)**. Exclusions were **48** survey completions below 100 seconds, **10** readers exceeding 699 words/minute on a passage, and **19** failing both comprehension questions for one passage.

Each participant read two passages of **103 and 108 words**, one in each mode, in randomized order, followed by two multiple-choice questions per passage. Paragraph typography used the same typeface at **14 px**, with lighter starting weight and different spacing than Study 1. Six grade levels were sampled; mode was repeated within readers while grade variation was between groups. Readers rated content interest/familiarity, comparative visual clarity, mode preference, usual phone mode, and their own reading speed. A four-person think-aloud pilot checked survey comprehension, not the main effect estimates.

## Results / Admissions

### Performance

- Desktop mode effect: Table 3 reports **F = 8.578, p = .004, η² = .075**, with denominator **df = 106**. At one heavier grade, reported mean word-pair time was **2.06 seconds dark versus 1.93 light**, **d = .16**; at the heaviest, **2.03 versus 1.92 seconds**. The former difference is **0.13 seconds**, not evidence of a large universal penalty.
- The overall grade effect in Table 3 is **F = 1.855, p = .117**; the mode-by-grade interaction is **F = 2.406, p = .048**. The prose reports a light-mode contrast between a thinner grade (**2.02 seconds**) and the heaviest (**1.92 seconds**), and recommends heavier grades for this particular word-pair format. It finds no dark-mode grade improvement.
- Paragraph mode effect: **F = 12.8, p < .01, η² = .038**; paired follow-up **t(332) = 3.5, p < .01** favors light mode. No significant grade effect or interaction was detected. Figure 5 plots overlapping grade trajectories with a small light-mode advantage, rather than a grade that equalizes the modes.
- A model including age reports **mode F = 10.06, p = .002, η² = .030** and **age F = 3.0, p = .007, η² = .053**. Figure 6 shows slower reading in later age groups; this does not separately establish the acuity-by-age interaction measured by Piepenbrock.
- More interesting content was read more slowly; reported familiarity did not predict fluency. Self-assessed speed was associated with performance, **F = 7.4, p < .001, η² = .083**. Slower reading is therefore not invariably worse engagement.

### Preference and clarity

Table 4 reports paragraph clarity **42% dark, 41% light, 17% neither**; reading preference **33% dark, 33% light, 34% either**. Preferences do not favor the faster group-level mode. The authors report no significant benefit from matching paragraph mode to usual phone settings (chi-square probabilities **.31 dark and .18 light**). A non-significant result does not prove familiarity has no effect.

The conclusion allows broad grade flexibility **within the tested paragraph setting and the method's detection sensitivity**. It explicitly says the result neither supports nor negates using grade to manage halation. Null effects are not equivalence tests or guarantees against small harms.

## Analyst Takeaways

1. **Use grade to separate stroke strength from reflow, not as a proven dark-mode repair.** Its conceptual value is experimental and typographic control; this paper did not find a dark-mode fluency improvement from grade.
2. **Distinguish preference, clarity, and fluency.** Balanced preference is compatible with a modest light-mode performance benefit. The aggregate percentages alone do not quantify how many individuals preferred their own slower mode.
3. **Do not conflate task variants.** [Dobres et al.](/dossiers/ambient-illumination-contrast-polarity-letter-size.md) mask single words and estimate exposure thresholds in controlled light; these remote tasks time self-paced pairs and short paragraphs. Both support a light-mode advantage in some conditions, but neither supplies a universal conversion between their timings.
4. **Keep the accessibility boundary visible.** [Piepenbrock et al.](/dossiers/positive-display-polarity-younger-older-adults.md) exclude relevant eye disease; this study reports no characterized low-vision subgroup. [NN/g](/dossiers/dark-mode-users-issues.md) recommends preserving system-level choice for differing needs. No result here justifies forcing light mode on every reader.

## Questions and Limitations

- Hardware, brightness, ambient illumination, viewing distance, and optical characteristics were uncontrolled remotely. Only one variable typeface and two task-specific typography combinations were tested, not arbitrary weight, spacing, or font designs. No independent replication of the grade null effect is established.
- **Sample inconsistency:** Study 1 says **126** analyzed, but Table 3's mode denominator **106** conventionally implies **107** complete participants. The paper does not reconcile this. The headline **459** is the two reported retained samples, not total recruited respondents.
- **Trial-count inconsistency:** the described **three training questions plus five questions × five grades × two modes** totals **53**, not the stated **56**; the paper does not explain whether training occurred separately per mode.
- **Table 3 inconsistency:** its “p-corr” values **.017 for grade** and **.022 for interaction** do not accord with the listed raw p-values **.117 and .048** and the small sphericity corrections. Do not treat those columns as a clear corrected significance result.
- **Table 4 inconsistency:** current-mode percentages **36 + 34 + 25 + 7 = 102%** despite a 100% total. Clarity is **17% neither** in the table but **18%** in discussion. Paragraph clarity and preference are described as dissociated without the corresponding person-level cross-tabulation.
- **Figure/reference inconsistency:** the word-pair result prose points to **Figure 5**, which is actually the paragraph plot; **Figure 4** is the word-pair plot. Section 4.5 describes the Faster-versus-Average post-hoc comparison as **p < .01**, while Table 5 gives **.011**.
- The methods first hypothesize lower dark-mode grade for equivalence, then hypothesize increasing dark-mode grade to improve readability by reducing halation. Those directional explanations are not reconciled, and neither is supported by the dark-mode grade results.
- The paper mentions a 95% confidence interval for the paragraph difference without giving its endpoints in that result passage. Figures supply means and standard errors but not a full numerical condition table.
- **Redistribution evidence:** first page states **“This work is licensed under a Creative Commons Attribution International 4.0 License.”** It also states **“© 2023 Copyright held by the owner/author(s).”** This is an explicit public-redistribution grant; the dossier points to the public raw archive while retaining the DOI as resource.

## Vault Ideas Extracted

- [Typeface Legibility](/vault/typeface-legibility.md) — Distinguishes grade from width-changing weight and records task-dependent stroke-strength effects, including the bounded paragraph null result.
- [Contrast Polarity and Legibility](/vault/contrast-polarity-and-legibility.md) — Adds remote desktop and Android fluency evidence and balanced preferences, without establishing luminance or halation as the isolated cause.
