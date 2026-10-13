---
type: Study Note
title: Effects of ambient illumination, contrast polarity, and letter size on text legibility under glance-like reading
description: Brief word-recognition thresholds worsen for white-on-black text in near-darkness, especially at the smaller tested size, while daylight-like illumination removes the statistically significant polarity difference in a selected working-adult sample.
resource: https://doi.org/10.1016/j.apergo.2016.11.001
source: https://doi.org/10.1016/j.apergo.2016.11.001
tags: [visual-perception, typography, human-performance, digital-interfaces]
timestamp: 2026-10-12T20:28:55Z
---

# Ambient Illumination and Glance Legibility — Study Notes

**Authors**: Jonathan Dobres, Nadine Chahine, and Bryan Reimer.  
**Published**: Applied Ergonomics **60, 2017, pp. 68–73**; accepted November 4, 2016; copyright 2016.  
**Status**: Peer-reviewed experimental journal article; read the complete six-page publisher-formatted author-hosted copy, including the task diagram, threshold plot, and both results tables. DOI verified from the first-page imprint.  

## What It Is

A within-subject psychophysical experiment crossing **ambient illumination, display polarity, and letter size**. Legibility means the minimum stimulus-display duration needed to decide whether a briefly presented string is a real word at approximately **80% accuracy**, not reading speed for continuous prose or completion time in a real car.

Its important qualification to the positive-polarity literature is a boundary: in near-darkness, white-on-black text requires longer exposure; under **4750 lux**, the polarity difference is not statistically significant.

## Problem and Motivation

Automotive and mobile interfaces are often read in short glances under changing light. Dark backgrounds can reduce emitted light and blend with hardware, but reducing glare or creating a preferred aesthetic need not optimize recognition. Most earlier studies measured longer-form reading in comparatively dim indoor light, leaving uncertainty about daylight and glance-like reading.

## Mechanism as an Idea

The proposed mechanism is illumination-dependent pupil size. A bright background or bright surroundings can constrict the pupil and reduce optical aberrations. When both surroundings and background are dark, the pupil may dilate and degrade the image. This predicts a **negative-polarity disadvantage under low illumination**, rather than a benefit of positive polarity under every environment. Pupil size was not measured in this experiment.

### Sample and comparison

**50** Italian-speaking FCA headquarters employees were recruited; **34** remained, **13 women and 21 men**, mean ages **36.2 and 39.0** respectively. Eligibility required normal or corrected vision, self-reported good health, ages **20–65**, and driving at least weekly; actual participants were as old as **59**. Exclusions were **one** discomfort withdrawal, **five** thresholds exceeding 300 ms, **six** mean responses exceeding 1000 ms, **three** unstable staircases, and **one** incomplete attendance. Thus **32%** of recruits were absent from the final sample, including people who performed poorly on the task.

Participants judged Italian words and matched pseudowords in **Neue Helvetica 55 Roman** on a desktop LCD at approximately **0.7 m**, without a head restraint. The eight conditions crossed:

- Positive versus negative polarity.
- **3 versus 4 mm capital-letter height**, approximately **14.7 versus 19.6 arcmin**; the actual stimuli were lowercase.
- Near **0 lux** versus **4750 lux**, representing near-dark and slightly overcast daylight-like conditions.

Words lacked diacritics and were frequency-matched. **410 words and 410 pseudowords** were sampled, with no repeated stimulus for a participant. Forward and backward masks curtailed visual persistence. An adaptive staircase changed exposure duration to target **79.4% accuracy**; thresholds were median durations across each block's last **20 trials**. Figure 1 makes clear that response time and exposure duration are different: the word disappears before the lexical judgment.

Each participant completed **400 trials per session**, **100 per polarity/size condition**. Within-session block order was randomized, but **bright always preceded dark on separate days**. Monitor white-screen brightness also changed, approximately **300 cd/m²** in bright ambient light versus **225 cd/m²** in darkness. The ambient comparison therefore is not isolated from day/order and display brightness.

## Results / Admissions

Mean exposure thresholds in **milliseconds**, with reported standard deviations in parentheses:

| Ambient light | Polarity | 3 mm | 4 mm |
|---|---|---|---|
| Daylight-like | Negative | **88.7 (50.0)** | **92.2 (61.7)** |
| Daylight-like | Positive | **86.0 (34.7)** | **77.5 (41.9)** |
| Near-dark | Negative | **122.3 (56.8)** | **106.9 (50.9)** |
| Near-dark | Positive | **84.1 (43.7)** | **83.3 (53.5)** |

- Overall effects: illumination **F(1,33) = 7.61, p = .009**; polarity **F(1,33) = 24.40, p < .001**; size **F(1,33) = 4.21, p = .048**; illumination-by-polarity **F(1,33) = 14.18, p < .001**.
- In daylight-like light, polarity was not significant (**p = .665**), nor was polarity-by-size (**p = .236**). Smaller text required **87.4 versus 84.8 ms**, a reported **3.0%** increase, **p = .025**, averaged across polarities.
- In darkness, polarity was strong (**F(1,33) = 49.60, p < .001**). Size mattered within negative polarity (**t(33) = 2.31, p = .027**) but not positive polarity (**p = .898**). From the tabulated means, negative polarity required **38.2 ms more at 3 mm** and **23.6 ms more at 4 mm** than positive polarity; these are arithmetic differences, not separately reported effect sizes.
- Accuracy averaged **79.1%**, and none of the eight conditions differed significantly from the **79.4%** target (**all p > .27**). Table 1 shows condition accuracy means **77.6–80.1%**. Similar accuracy is expected because exposure duration adapts; it does not show equivalent legibility.
- Figure 2 presents the marked dark/negative separation with **within-subject standard errors**, not the between-person standard deviations shown in Table 2.

The authors recommend larger text where possible, particularly on negative-polarity displays, and balancing readability with nighttime brightness/distraction constraints. Actual driving, adaptation back to the road, glare, and accident risk were not measured.

## Analyst Takeaways

1. **Do not equate a comfortable dark surface with fast recognition.** Near-darkness is precisely where this sample needed longer exposure to dark-mode text.
2. **Use context-specific evidence.** [Piepenbrock et al.](/dossiers/positive-display-polarity-younger-older-adults.md) establish an age-bounded positive advantage in acuity and proofreading; this experiment adds ambient light and size, not pathological low vision.
3. **Keep threshold and workflow metrics distinct.** [Palmén et al.](/dossiers/how-bold-can-we-be-font-grade-polarity.md) time self-paced word-pair and paragraph reading. Their same-direction light-mode advantage corroborates a broad pattern, but its seconds-based timings are not comparable to these masked exposure thresholds.
4. **Treat user preference as a separate outcome.** [NN/g's dark-mode report](/dossiers/dark-mode-users-issues.md) describes comfort beliefs and system-level expectations; those observations do not refute the near-dark legibility penalty.

## Questions and Limitations

- Bright-first ordering permits practice or session effects; the authors suggest practice could partly explain the null size difference for positive polarity on day two. Different monitor brightness further limits a pure ambient-light interpretation.
- Removing slow and unstable performers restricts generalization to people who may most need accessible typography. This is not a study of disabled people or frail older adults.
- The experiment tests one typeface, two relatively close sizes, one language without accents, and a stationary desktop task. It does not establish a universal minimum font size, a WCAG contrast threshold, or an optimal nighttime vehicle interface.
- The discussion acknowledges daylight polarity differences were **non-significant**, although some preceding prose says positive polarity retains an advantage “regardless” of lighting. Interpret the bright result as nominal direction, not demonstrated superiority or statistical equivalence.
- The analysis description labels the factors **“lighting × typeface × polarity”** although only one typeface was tested; the actual manipulated factor is **size**. This is an internal labeling error, not a hidden typeface comparison.
- The findings converge with previous polarity studies and extend them to wide ambient variation; no independent direct replication of this eight-condition experiment is established here.
- **Redistribution evidence:** the PDF states **“© 2016 Elsevier Ltd. All rights reserved.”** No explicit redistribution grant is present. The author-hosted copy belongs in the private archive; use the DOI as source.

## Vault Ideas Extracted

- [Contrast Polarity and Legibility](/vault/contrast-polarity-and-legibility.md) — Supplies a strong illumination boundary: near-dark negative-polarity exposure thresholds rise, especially for smaller text, while the daylight polarity comparison is non-significant.
- [Typeface Legibility](/vault/typeface-legibility.md) — Shows that measured legibility depends on type size and viewing context even with typeface held constant; masked word recognition is not continuous-reading fluency.
