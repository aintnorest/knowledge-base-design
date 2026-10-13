---
type: Study Note
title: Positive display polarity is advantageous for both younger and older adults
description: Dark-on-light displays improve visual acuity and proofreading accuracy in younger and older adults with normal or corrected vision, but the study excludes clinically relevant eye disease and does not establish a fatigue benefit.
resource: https://doi.org/10.1080/00140139.2013.790485
source: https://doi.org/10.1080/00140139.2013.790485
tags: [visual-perception, typography, human-performance, inclusive-design, digital-interfaces]
timestamp: 2026-10-12T20:28:55Z
---

# Positive Display Polarity Across Age — Study Notes

**Authors**: Cosima Piepenbrock, Susanne Mayr, Iris Mund, and Axel Buchner.  
**Published**: Ergonomics **56(7), 2013, pp. 1116–1124**; final version received March 24, 2013.  
**Status**: Peer-reviewed experimental journal article; read the complete nine-page publisher-formatted, author-hosted HHU copy, carrying a September 16, 2013 download stamp, including all three figures.  

## What It Is

A randomized, between-subjects comparison of **positive polarity** (dark characters on a light background) and **negative polarity** (light characters on a dark background), testing whether ordinary age-related vision changes reverse the usual light-background advantage. They do not in this sample: both younger and older adults benefit in acuity and proofreading accuracy.

The title's age claim is not a claim about every visual condition. The participants had normal or corrected-to-normal vision, and clinically relevant eye disease was excluded.

## Problem and Motivation

Aging reduces retinal illumination through smaller pupils, denser lenses, and reduced transparency. A bright display could compensate. Conversely, increased intraocular scatter could make that same brightness harmful. The experiment asks which effect dominates in non-pathological aging, rather than assuming older users and users with cataracts have interchangeable needs.

Earlier polarity findings include both positive advantages and null results. The authors propose low power, CRT flicker, and effort compensation in within-subject designs as possible explanations; these are methodological interpretations, not experimentally isolated causes here. They criticize a previous age-related negative-polarity acuity advantage for ceiling effects, fixed positive-first ordering, and reused letters.

## Mechanism as an Idea

A bright background typically illuminates far more screen area than bright text. Higher overall luminance can constrict the pupil, reduce spherical aberration, and increase depth of field. Extremely small pupils introduce diffraction, so smaller is not unconditionally better. Earlier luminance-matched research cited by the authors removed the polarity advantage while retaining a brightness advantage; this study does not itself equate overall luminance or directly measure pupil size.

### Participants, tasks, and measures

The study reports **84 younger adults, ages 18–33, mean 22.63**, and **85 older adults, ages 60–85, mean 69.82**. Participants were native German speakers, passed cognitive screening, and reported normal or corrected vision. Exclusions included limiting cataract, macular degeneration, glaucoma, diabetic retinopathy, and uveitis; prior cataract surgery was allowed. Two further participants are described as excluded for disruptions.

Everyone saw only their randomly assigned polarity throughout a roughly **75-minute session**:

- **Acuity:** 30 adaptive forced-choice Landolt-C trials at **184 cm**, with eight gap orientations and an acuity ceiling of **2.0 Snellen decimals**.
- **Proofreading:** **28 German passages**, **250 words and 14 errors each**, in **10-point Helvetica**, at **50 cm**. Each passage remained visible for **50 seconds**; participants named errors and their last words read. Grammar errors required more than isolated-character scanning. Passage order was randomized, and breaks were self-paced.
- **Outcomes:** log visual acuity; detected errors adjusted for false alarms; words read; pre/post eyestrain, headache, muscle/back discomfort, and mood ratings.

White and black display elements measured **350 and 1 cd/m²**. Illumination at the eye was **16 versus 0 lux** during acuity testing and **117 versus 3 lux** during proofreading, positive versus negative respectively. Polarity therefore includes substantially different illumination, not merely swapping an otherwise equivalent color pair.

## Results / Admissions

- **Acuity:** polarity **F(1,163) = 69.31, p < .01, η² = .30**; age **F(1,163) = 42.91, p < .01, η² = .21**; interaction **F(1,163) = 19.80, p < .01, η² = .11**. The positive advantage was much larger for younger adults (**t(82) = 9.93, d = 2.17**) than older adults (**t(81) = 2.53, p = .01, d = .58**). Figure 1 shows both group means and individual acuities; it does not provide a table of exact means.
- **Proofreading:** positive polarity improved false-alarm-adjusted detection, **F(1,165) = 9.92, p < .01, η² = .06**. Younger adults performed better overall, **η² = .19**. The age-by-polarity interaction was not significant, **p = .44**. Figure 2 plots adjusted error counts per text, not an exact tabulated percentage improvement.
- **Reading rate:** neither polarity (**p = .69**), age (**p = .51**), nor their interaction (**p = .60**) was significant. The accuracy advantage therefore was not accompanied by a detected slowing of reading. Figure 3 shows similar words-read means across groups.
- **Comfort:** no significant polarity benefit for eyestrain, headache, or mood was found. Only one of **18** main-effect/interaction tests reached significance, a muscle/back-discomfort interaction (**p = .02**), which the authors regard as likely chance.
- Contrast-sensitivity testing and a final subjective questionnaire were collected but explicitly **not reported** because the authors considered them outside the research questions.

The authors recommend positive polarity independent of audience age. The supported boundary is narrower: ordinary corrected vision across these age groups, this bright LCD, these acuity and proofreading tasks, and this session duration.

## Analyst Takeaways

1. **Do not use age as a proxy for cataract or low vision.** Non-pathological older adults benefited; cloudy ocular media remain a different population for which the cited literature reports possible negative-polarity benefits.
2. **Separate accuracy from comfort.** Better error detection does not prove reduced headaches or eyestrain, and a subjective preference does not necessarily identify the better-performing polarity.
3. **Track illumination, not just contrast ratio.** [Color Contrast Minimum](/vault/color-contrast-minimum.md) concerns a necessary luminance distinction, but equal endpoint contrast does not equate total light reaching the eye.
4. **Read the batch as complementary, not contradictory.** [Dobres et al.](/dossiers/ambient-illumination-contrast-polarity-letter-size.md) find a dark-background disadvantage for briefly exposed words in near-darkness, but no significant polarity effect in daylight-like light. [Palmén et al.](/dossiers/how-bold-can-we-be-font-grade-polarity.md) find modest light-mode fluency benefits on users' own devices. [NN/g](/dossiers/dark-mode-users-issues.md) concerns preferences, expectations, and interface failures, not a replication of this experiment.

## Questions and Limitations

- No font-size manipulation was performed here. Claims that the advantage becomes stronger for small text belong to separate experiments, including the size comparison in Dobres, not this paper's age comparison.
- Acuity analyses imply **167 observations** from their degrees of freedom, whereas proofreading implies **169**. The paper explains vocabulary-test data loss (**N = 168**) but does not explicitly reconcile the acuity denominator or clarify how the two disruption exclusions relate to the stated sample counts.
- The design section describes proofreading performance as **hit rate minus false-alarm rate (Pr)**, while Figure 2 and its axis report **number of errors minus false alarms per text**. These related measures are not interchangeable denominators; the paper does not explicitly reconcile the presentation.
- Pupil contraction and the proposed explanation for the smaller older-adult acuity effect are inferred, not measured. The luminance difference supports the account but is also part of the treatment bundle.
- The study corroborates earlier positive-polarity work and extends it to older adults; it is not evidence of an independent direct replication of its exact age interaction. Generalization to sustained reading, OLED displays, pathological vision, or outdoor environments is unresolved.
- **Redistribution evidence:** the PDF states **“© 2013 Taylor & Francis.”** No explicit redistribution license appears in the supplied file. Author hosting does not provide such a grant; retain the raw copy privately and cite the DOI URL.

## Vault Ideas Extracted

- [Contrast Polarity and Legibility](/vault/contrast-polarity-and-legibility.md) — Establishes an acuity and proofreading advantage in younger and older adults without limiting eye disease, while separating performance from fatigue and polarity from total luminance.
- [Color Contrast Minimum](/vault/color-contrast-minimum.md) — Adds evidence that nominally strong endpoint contrast does not make opposite polarities equivalent in effective legibility.
