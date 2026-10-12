---
type: Study Note
title: "Aesthetics and Apparent Usability: Empirically Assessing Cultural and Methodological Issues"
description: Three Israeli ATM-layout studies replicate a strong association between beauty and expected ease of use, but measure neither actual usability nor persistence after interaction.
resource: https://doi.org/10.1145/258549.258626
source: https://doi.org/10.1145/258549.258626
tags: [aesthetics, usability-evaluation, digital-interfaces, user-research]
timestamp: 2026-10-11T23:51:39Z
---

# Aesthetics and Apparent Usability — Study Notes

**Authors**: Noam Tractinsky.  
**Published**: CHI '97, March 22–27, 1997, Atlanta; pp. 115–122.  
**Status**: Peer-reviewed conference paper; read the ACM proceedings PDF. This is a replication of pre-use judgments, not a study of operating an ATM.  

## What It Is

Three studies testing whether the beauty–apparent-usability association reported by Kurosu and Kashimura in Japan survives a different population and changes in rating procedure and display medium. It does: correlations across **26 layout means** are **r=.921, .832, and .920**. The defensible finding is that attractive layouts *look easier to use*, not that beauty makes a system objectively usable.

## Problem and Motivation

HCI had prioritized functional usability while treating appearance as peripheral or potentially obstructive. The earlier Japanese study found **r=.589** between beauty and expected ease of use, larger than most associations with design features intended to improve usability. Tractinsky expected a weaker association in Israel, based on an explicitly informal cultural hypothesis. The result contradicted that expectation.

The paper distinguishes **apparent usability**, an expectation before use, from **inherent usability**, here operationalized as layout features presumed beneficial by professionals. Those features are not measured task performance. System acceptance might depend on both expectations and experience, but acceptance and long-term satisfaction are arguments motivating the study, not its outcomes.

## Mechanism as an Idea

The same components were arranged in **26 ATM layouts**, originally produced by nine GUI designers, six industrial engineers, eight engineers, and three secretaries. Participants answered two single-item **1–10** questions: how easy the interface seemed to use and how beautiful it was. Layout-average scores, rather than individual respondents' scores, were correlated.

Translation changed more than language: Hebrew words replaced single-character Japanese labels, an hourglass replaced a bowing woman, and a confirmation label replaced a yen-symbol action. Figures 1–2 show a high-rated regular keypad layout and a low-rated fragmented arrangement in both versions. These examples establish the visual nature of the manipulation, while also showing why the cross-country comparison is not a culture-only experiment.

The proposed mechanism is an appearance-based inference influencing expected usability and perhaps later attitudes. **Direction of causation, a halo mechanism, and durable influence after use are not established here.**

## Results / Admissions

- **Experiment 1**: **104 first-year engineering students** rated both attributes consecutively while each layout was projected for approximately **20 seconds**. Across 26 means, beauty and apparent usability correlated **r=.921**, versus **.589** in Japan; the difference was reported as **Z=3.09, p=.001**. Mean beauty was **5.9** versus Japan's **6.0**; apparent usability **5.4** versus **5.8**. Israeli scores had wider ranges: beauty **3.5–8.5** versus **5.2–6.8**, apparent usability **2.7–8.5** versus **4.4–6.5**.
- **Experiment 2**: **81 different first-year engineering students**, randomly assigned to question order, rated the layouts in two separately randomized rounds: all beauty judgments followed by all usability judgments, or vice versa. Projection lasted approximately **15 seconds** per layout. The association remained **r=.832**, weakening the explanation that consecutive questions alone produced it.
- **Experiment 3**: **108 third-year engineering students** viewed layouts on individual computers, with self-paced responses, separately randomized rounds, and counterbalanced question order. The association remained **r=.920**. Apparent-usability judgments took **8.68 seconds** on average versus **7.58 seconds** for beauty, **t(107)=2.49, p=.014**. This is response latency during explicit rating, not an ultra-rapid first-impression threshold.
- **Other layout variables**: seven features represented display location, keypad type, grouping, key sequence, hand dominance, confirmation location, and cancel-key location. Keypad-type contingency coefficients were **.671, .751, .760** across the Israeli studies, not Pearson correlations. Israelis favored familiar telephone keypads; Japanese ratings favored horizontal keypads. Grouping correlated negatively with apparent usability (**r=−.462, −.529, −.667**): fewer separated groups looked easier, contrary to the assumed benefit of separating unrelated controls. This does not overturn grouping guidance for actual performance.
- **Method-bias admission**: a multitrait–multimethod matrix supports convergent validity, but discriminant-validity comparisons succeed in only **5 of 12** cases, or **3 of 4** when excluding Experiment 1. The author explicitly leaves some shared-method variance unresolved.

## Later Evidence: Persistence Is Conditional

These are findings from later work, **not results of the 1997 paper**:

- [Tractinsky, Katz, and Ikar (2000), *What is beautiful is usable*](https://doi.org/10.1016/S0953-5438(00)00031-X) extended the question to use. The later [Tuch et al. review and experiment](https://doi.org/10.1016/j.chb.2012.03.024) reports that the ATM study found an aesthetics effect on post-use perceived usability; its reconstructed effect size was **partial η²=.037**. This is evidence that an effect can persist after interaction, not that it must persist.
- [Hassenzahl and Monk (2010), *The Inference of Perceived Usability From Beauty*](https://doi.org/10.1080/07370024.2010.500139) examined the literature: the [indexed abstract](https://psycnet.apa.org/record/2010-19070-002) reports **25 independent beauty–usability correlations with remarkably high variability**. The abstract-level evidence does not support a single invariant effect, and no pooled estimate is inferred here. Tuch et al.'s discussion also cites their distinction between beauty and classical aesthetics, the latter partly resembling “visual” usability.
- **A direct boundary case**: [Tuch et al. (2012), *Is beautiful really usable?*](https://doi.org/10.1016/j.chb.2012.03.024), independently varied appearance and navigation quality in an online shop with **80 participants** (42 female; mean age **25.7**). Participants evaluated a screenshot for **10 seconds**, then found and added **four specified clothing items**, with a five-minute task limit. Beauty was manipulated through decorative treatment without moving interaction elements; usability through category labels and item assignment. Aesthetics did **not** affect pre-use expected usability (**F(1,76)=.582, p=.448, partial η²=.008**) or post-use SUS (**p=.830, η²=.001**), orientation (**p=.696, η²=.002**), or pragmatic quality (**p=.643, η²=.003**). Usability strongly affected those post-use measures (**η²=.547, .483, .441**) and affected classical aesthetics (**p=.002, η²=.125**), but not the single beauty item (**p=.341**). The usability manipulation was strong and the aesthetics manipulation medium-to-large. Their proposed frustration-mediated pathway is correlational, not a separately randomized mechanism.

Together these studies support an association and some post-use effects, but reject **“beautiful always feels usable”** as an unconditional design law. Task involvement, manipulation strength, and what the questionnaire calls aesthetics matter.

## Analyst Takeaways

1. **Treat appearance as an expectation signal, not a performance certificate.** Assess beauty, anticipated usability, perceived usability after use, and task success separately.
2. **Do not apply r≈.9 to individual users.** These are correlations among aggregated layout ratings; aggregation can produce much stronger associations than individual-level data.
3. **Conventions can masquerade as inherent quality.** The keypad difference makes learned familiarity a better explanation than a universal ranking of keypad layouts.
4. **A durable rule needs its boundary cases.** Later null effects under actual use belong beside the original replication, not in a footnote to an aesthetics-first recommendation.

## Questions and Limitations

- Engineering students, one ATM layout family, and no operating task limit generalization. Age, gender, error rates, and task-completion outcomes are not reported for these experiments.
- Culture is entangled with translation, stimulus reconstruction, population, rating variability, and an earlier study run by other investigators. The author's cultural explanations are hypotheses, not identified causes.
- Single-item subjective measures and shared stimuli do not isolate appearance from visible organization or expected functionality.
- First impressions' possible effect on long-term acceptance is cited and theorized, not measured in this paper.
- **Redistribution**: the PDF's first-page notice reads: “Permission to make digital/hard copies of all or part of this material for personal or classroom use is granted without fee provided that the copies are not made or distributed for profit or commercial advantage, the copyright notice, the title of the publication and its date appear, and notice is given that copyright is by permission of the ACM, Inc. To copy otherwise, to republish, to post on servers or to redistribute to lists, requires specific permission and/or fee”. This is not permission to redistribute a public repository copy; `source` therefore uses the canonical DOI URL.

## Vault Ideas Extracted

- [Aesthetic–Usability Effect](/vault/aesthetic-usability-effect.md) — Strong pre-use layout-mean associations, methodological replication, and later post-use boundary cases distinguish perceived from actual usability.
- [Consistency and Convention](/vault/consistency-and-convention.md) — Culturally familiar keypad arrangements affected expected ease of use, cautioning against universalizing a layout preference.
