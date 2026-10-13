---
type: Study Note
title: Assessing dimensions of perceived visual aesthetics of web sites
description: Four scale-development studies distinguish orderly classical aesthetics from creative expressive aesthetics, with stronger perceived-usability correlations for classical qualities but no causal preference or performance test.
resource: https://doi.org/10.1016/j.ijhcs.2003.09.002
source: https://doi.org/10.1016/j.ijhcs.2003.09.002
tags: [aesthetics, ux-metrics, user-research, digital-interfaces, usability-evaluation]
timestamp: 2026-10-12T20:26:53Z
---

# Perceived Visual Aesthetics of Web Sites — Study Notes

**Authors**: Talia Lavie and Noam Tractinsky.  
**Published**: International Journal of Human-Computer Studies **60, 2004, pp. 269–298**; accepted September 17, 2003.  
**Status**: Peer-reviewed journal scale-development research; read the supplied Wayback snapshot of the author-hosted publisher-layout PDF, marked **“ARTICLE IN PRESS”** throughout and carrying a 2003 copyright notice despite the 2004 bibliographic year.  

## What It Is

Four studies developing a **two-dimensional measure of perceived website aesthetics**, not a prescription to maximize symmetry or special effects. **Classical aesthetics** captures pleasing clarity, cleanliness, and order. **Expressive aesthetics** captures perceived creativity, originality, sophistication, and fascination. The final instrument contains **five items per dimension**; item wording and coefficients are available in [the source's Table 2 and Appendix B](https://doi.org/10.1016/j.ijhcs.2003.09.002).

## Problem and Motivation

A single beauty question can hide different kinds of visual appreciation. It also makes the [beauty–usability relationship](/vault/aesthetic-usability-effect.md) seem paradoxical when a person is partly rating visible clarity as both aesthetics and usability. The authors seek a dependable measurement model before studying aesthetic causes or consequences.

The historical discussion contrasts order/proportion with expression/novelty and adopts an exploratory, subjective approach to whole websites. Those traditions help interpret the factors; the labels do not prove that users think in art-historical categories.

## Principle as an Idea

**Order and expression are related dimensions, not opposing ends of one slider.** A design can be appreciated for both. A clear, controlled composition can have aesthetic value independent of ornamental novelty; a creative composition can be appreciated without being regarded as easy to navigate. Correlations with usability depend on which facet is measured.

The study treats these as latent perceptions rather than counts of visual elements. It does not establish how much clarity or novelty maximizes preference, and the authors explicitly distinguish scale development from investigating website preferences.

## Results / Admissions

### Construction and replication within the study program

| Study | Participants and stimuli/task | Measurement and result |
|---|---|---|
| 1 | **125 engineering students**, 36 female/89 male, mean age **25**; randomly assigned to Time magazine or Universal Usability in a supervised lab | Literature plus **11 experts** generated **41 adjectives**. Seven-point agreement ratings and participant feedback reduced/revised the pool. Eight eigenvalues exceeded one, but scree, parallel analysis, and interpretation favored **two factors**; the eight-factor extraction explained **61.5%**. |
| 2 | **212 engineering students**, 92 female/120 male, mean **24.8**; Gap **107**, Macy's **105**; simulated purchase of two items | **35 aesthetics items**, seven-point responses. Maximum-likelihood EFA with oblimin rotation, separately by site and pooled, repeatedly supported **two factors**. Low/cross-loading and negatively phrased items were dropped. |
| 3 | **145 engineering/business students**, 61 female/84 male, mean **24.3**; browsing HaShulchan, an Israeli food/wine site | **25 aesthetics**, seven usability, six playfulness, five pleasure, five service-quality items. Aesthetic two-factor solution explained **55.7%**, factor correlation **.55**. Six-factor analysis explained **62%**, but cross-loadings and awkward playfulness wording required refinement. |
| 4 | **384 ordinary web volunteers**, 173 female/211 male, ages **17–67**, mean **27**; recruited on five Israeli forums and evaluated the recruiting site | Sample split into **192 initial-validation and 192 holdout participants**. CFA in model-generation mode refined the instrument on the first half; the frozen model was tested on the second. Playfulness was omitted. |

Study 4's unrefined aesthetics model fit poorly: **χ²(229)=894.822, RMSEA=.123, CFI=.781**. Item reduction and a correlated residual for semantically similar clean/clear judgments produced the ten-item two-factor model: initial **χ²(33)=49.28, p=.034, RMSEA=.051, CFI=.983, SRMR=.036**; holdout **χ²(33)=50.22, p=.028, RMSEA=.052, CFI=.982, SRMR=.050**. A single-factor alternative fit poorly: **χ²(34)=191.508, RMSEA=.156, CFI=.836**.

In the combined model, **clear design** was allowed to indicate both classical aesthetics and usability. The complete five-factor model had initial **RMSEA=.062, CFI=.957**, and holdout **RMSEA=.058, CFI=.962**. This is evidence of separable but overlapping perceptions, not complete measurement independence.

### Reliability and relationships

- Classical-aesthetics **Cronbach α=.85/.86** and expressive **α=.87/.86**, initial/holdout respectively. High internal consistency does not establish stability over time.
- The aesthetics-only CFA reports latent-factor correlation approximately **.61**. Table 3's scale intercorrelations are **.69/.63**; these should not be silently treated as the same statistic.
- Classical aesthetics correlated with perceived usability **r=.68/.78**, versus expressive aesthetics **r=.46/.40**. All Table 3 correlations are **p<.01**. This strengthens the visible-clarity account of part of the aesthetic–usability association without demonstrating a causal pathway.
- Pleasure correlated **.68/.61** with classical and **.59/.54** with expressive aesthetics. Service quality correlated **.60/.61** and **.42/.37**, respectively—higher than expected, with common-method bias explicitly admitted as an alternative.
- Age and gender correlations with either aesthetics scale were nonsignificant at **.05** in both halves. These nulls are not evidence of demographic universality; [larger later first-impression research](/dossiers/predicting-website-aesthetics-first-impressions.md) uses different measures and samples.

## Analyst Takeaways

1. **Ask what “aesthetic” means in a result.** A usability association involving clarity-heavy classical aesthetics is not equivalent to one involving beauty or creative novelty.
2. **Do not collapse order and expression into a mandatory tradeoff.** They correlate positively but retain different relationships to other evaluations.
3. **Separate model validation from causal design evidence.** Good factor fit and α support measurement; they do not show that adding effects improves appeal, performance, or trust.
4. **Retain the holdout boundary.** Cross-validation strengthens the modified model, but both halves come from the same recruiting ecosystem rather than an independent cultural replication.

## Questions and Limitations

- Familiarity can contaminate visual appraisal, particularly because Study 4 participants evaluated sites on which they already encountered recruitment. English/Hebrew stimuli diversify language, not the cultural background of participants.
- Item selection, residual correlation, and the retained clear-design cross-loading are consequential researcher decisions. The authors do not claim that classical/expressive is the only possible taxonomy; later VisAWI work expands the domain.
- No task-time effect, causal halo, durable preference, or actual revisit behavior is established. Test–retest stability and transfer beyond websites remained open.
- The exact source title includes **“Assessing dimensions of”**; the shorter inbox/task label is not the publication title. Study 1 names Time magazine while printing **times.com**, a source URL-label mismatch. The narrative says service-quality correlations are lower than the aesthetics factors' relationships with every other construct; in the holdout table, classical service quality **r=.61** instead equals classical pleasure **r=.61**, so that wording is not strictly true in every cell.
- **Redistribution evidence**: first page states **“© 2003 Elsevier Ltd. All rights reserved.”** and explicitly prints **doi:10.1016/j.ijhcs.2003.09.002**. No public redistribution grant appears; archive privately and use the canonical DOI as source.

## Vault Ideas Extracted

- [Classical and Expressive Aesthetics](/vault/classical-and-expressive-aesthetics.md) — Supplies the two-factor distinction, held-out CFA, reliability, and its clear boundary from causal preference claims.
- [Aesthetic–Usability Effect](/vault/aesthetic-usability-effect.md) — Shows that classical clarity-heavy aesthetics has stronger perceived-usability relationships than expressive aesthetics and admits measurement overlap.
