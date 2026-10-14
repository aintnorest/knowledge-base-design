---
type: Study Note
title: "The effectiveness of nudging: A meta-analysis of choice architecture interventions across behavioral domains"
description: A corrected synthesis of 447 effect sizes estimates a positive average nudge effect and larger effects for decision structure, but extreme heterogeneity and publication-bias sensitivity prevent treating that average as a dependable intervention forecast.
resource: https://doi.org/10.1073/pnas.2107346118
source: https://doi.org/10.1073/pnas.2107346118
tags: [behavior-change, decision-making, user-research, survey]
timestamp: 2026-10-14T21:31:01Z
---

# Effectiveness of Nudging Across Behavioral Domains — Study Notes

**Authors**: Stephanie Mertens, Mario Herberz, Ulf J. J. Hahnel, and Tobias Brosch.  
**Published**: PNAS **119(1), e2107346118 (2022)**; online December 30, 2021; corrected May 4, 2022, in **119(19), e2204059119**, DOI [10.1073/pnas.2204059119](https://doi.org/10.1073/pnas.2204059119).  
**Status**: Peer-reviewed meta-analysis with a substantial published data/coding correction. Read the complete supplied **33-page article and 15-page correction PMC prints**, captured October 14, 2026, including tables and figure captions; missing figure images in the prints were recovered from PMC. All substantive estimates below use the correction, not the stale article print. The linked supplementary appendix itself was not supplied or analyzed.

## What It Is

A quantitative review of interventions that change the choice environment while preserving available choices, spanning physical and hypothetical decisions rather than software alone. It distinguishes **decision information** (description and visibility), **decision structure** (defaults, effort, composition, consequences), and **decision assistance** (reminders and commitment). These are descriptive intervention categories, not proof of particular cognitive mechanisms.

The positive synthesis is counterweighted by [Maier et al.'s publication-bias reanalysis](/dossiers/no-evidence-for-nudging-publication-bias.md), which uses the corrected data and reaches a much more skeptical conclusion about the average effect. Neither paper establishes that every nudge works or that none can work.

## Evidence Base and Measures

The main search combined nudge/choice-architecture and empirical-research terms in four databases, restricted the initial search to 2008 onward, and added older studies through reviews, behavioral-unit reports, dissertations, and requests for unpublished data. It concluded in **June 2019**, yielding **9,606 unique publications**; the corrected included table nevertheless spans publication years **1982–2021**.

Eligible studies used randomized controlled designs, behavioral outcomes in real or hypothetical choices, individual-level units, and English reports. Combined techniques, significant economic incentives, and education-program combinations were excluded to isolate individual techniques. Household, classroom, and organizational units were excluded. The corrected sample contains **447 effect sizes, 212 publications, and pooled n = 2,148,439**, with study samples ranging **14–813,990**; this is an aggregated count, not a newly recruited participant cohort.

Different behavioral outcomes were converted to **Cohen's d**; positive values indicate change in the intervention's intended direction, not independently measured welfare. Three-level models represent treatment/publication dependence; cluster-robust standard errors address overlapping samples. Coding reliability on 20% of publications was **κ = .76–1, mean .87**. Moderator comparisons are across studies, not randomized head-to-head comparisons of intervention families.

## Corrected Results

### Average, variation, and publication bias

The corrected overall estimate is **d = .43, 95% CI [.38, .48], t(333) = 16.51, p < .001**. Removing influential outliers yields **d = .41 [.37, .46]**; leave-one-out estimates range **.42–.44**. This demonstrates robustness to individual observations, not robustness to systematic selective publication.

Heterogeneity remains enormous: **τ² = .16, I² = 99.52%**, with observed d spanning **−.69 to 3.08** and a **95% prediction interval [−.36, 1.22]**. Negative effects remain compatible with the synthesis. The article's approximately 15% backfire claim is a model-based inference, not a measured deployment failure rate.

Funnel asymmetry and Egger regression show an association between effect and standard error: **b = 2.10 [1.31, 2.89], t(332) = 5.22, p < .001**. In a simplified sensitivity model, **d = .40 [.36, .44], τ² = .16** falls to **.31, τ² = .18** under assumed moderate selection (**22.5% attenuation**) and **.08, τ² = .26** under assumed severe selection. These are assumption-dependent scenarios, not an empirically identified corrected truth. The authors judge severe selection only partly supported by the funnel; Maier et al. dispute that judgment.

### Intervention families and domains

| Corrected category | Effect sizes | d [95% CI] |
|---|---:|---|
| Decision information | 130 | .34 [.27, .42] |
| Decision structure | 223 | .54 [.46, .62] |
| Decision assistance | 94 | .28 [.21, .35] |

Category moderation is **F(2,330) = 12.23, p < .001**. Structure exceeds information (**b = .19 [.08, .31], p = .001**) and assistance (**b = .26 [.15, .36], p < .001**); information versus assistance is nonsignificant (**b = −.06 [−.16, .04], p = .21**). The category moderator leaves **I² = 99.33%**: a statistically detected distinction explains little of the total dispersion.

Corrected technique estimates are **translation .28 [.17,.39]**, **visibility .32 [.25,.40]**, **social reference .36 [.27,.46]**, **default .62 [.52,.73]**, **effort .48 [.26,.70]**, **composition .44 [.25,.63]**, **consequence .38 [.31,.46]**, **reminder .29 [.21,.37]**, and **commitment .23 [.08,.39]**. Defaults contribute **128 effects, n = 139,844**; the technique omnibus is **F(8,324) = 4.48, p < .001**. These primary estimates are not publication-bias adjusted.

Domain moderation is **F(5,327) = 3.64, p = .003**: **food .65 [.47,.83]**, **finance .24 [.14,.35]**, **health .34 [.25,.43]**, **environment .43 [.33,.54]**, **prosocial .41 [.27,.54]**, and **other .31 [.09,.52]**. The corrected text removes the original claim that food exceeds *every* other domain significantly. Food has only **12,077 pooled participants across 111 effects**, whereas prosocial has **1,041,501 across 58 effects**; headline participant totals do not equal uniform evidential depth.

Location (**p = .387**), adult versus child/adolescent population (**p = .587**), and experiment type (**p = .922**) are not significant moderators. More recent publication predicts smaller effects (**t(332) = −3.56, p < .001**). Absence of detected moderation is not equivalence across all countries, populations, or settings.

## What the Correction Changes

The correction removes **four observations from retracted Shu et al. (2012)**, fixes **two Rohlfs Domínguez et al. (2013) observations** and other coding errors, and fixes three moderator omnibus degrees of freedom. Its principal old → corrected changes are:

- **455 effects / 214 publications / 2,149,683 participants → 447 / 212 / 2,148,439**; abstract wording **over 450 → over 440 effects**.
- Overall **d .45 [.39,.52] → .43 [.38,.48]**; outlier-removed **.42 → .41**; leave-one-out **.43–.46 → .42–.44**; **τ² .23 → .16**, **I² 99.67% → 99.52%**, maximum d **4.69 → 3.08**, prediction interval **[−.48,1.39] → [−.36,1.22]**.
- Egger **b 2.28 → 2.10**; moderate-bias attenuation **26.79% → 22.5%** (adjusted d remains **.31**); severe-bias d **.03 → .08**.
- Information / structure / assistance **.38 / .55 / .31 → .34 / .54 / .28**; technique estimates and intervals are replaced by those above (default point estimate remains **.62**); technique minimum **.30 → .23**.
- Food **.72 → .65**, finance **.25 → .24**, prosocial **.44 → .41**, other **.29 → .31**; health and environment point estimates remain **.34 and .43**, with updated intervals. Structure-within-domain range **.33–.86 → .33–.78**.
- Category omnibus **F(3,337) 9.79 → F(2,330) 12.23**; technique **F(9,331) 4.27 → F(8,324) 4.48**; domain **F(6,334) 4.62 → F(5,327) 3.64**. Contextual statistics, table counts, pairwise contrasts, and heterogeneity decompositions also change.
- Influential outliers **three (3.08–4.69) → two (2.24–3.08)**; full-text exclusions **936 → 938**; figures 2–5, Table 2, and supplementary Tables S1–S4 are corrected. The authors say the overall pattern and conclusions remain unchanged; that is their assessment, not resolution of the publication-bias debate.

## Analyst Takeaways

1. **Use the categories to form hypotheses, not promise uplift.** Changing structure differs from clarifying information or reinforcing intentions, but cross-study rankings are not a causal recipe for a particular interface.
2. **Report an average alongside its prediction interval and bias assumptions.** A tight mean CI can coexist with broad real-world variation and systematic inflation.
3. **Do not confuse intended-direction behavior with benefit.** Preservation of nominal options does not itself establish informed consent, welfare, or distributional fairness.
4. **Separate mechanism from observation.** The proposed advantage of low processing demands and reduced dependence on values/goals is explicitly speculative, not measured mediation.
5. **Carry the counterweight forward.** The corrected .43 should never be presented without the [Maier reanalysis](/dossiers/no-evidence-for-nudging-publication-bias.md) and the unresolved dependence/bias-model tradeoff.

## Questions and Limitations

- This is synthesis, not a new replication experiment. Included randomized studies vary in tasks, outcomes, and context; primary-study-level replication histories are not enumerated.
- Search terminology and individual-only, English-only, single-technique criteria omit important evidence and deployed combinations. The June 2019 search versus 2021 publication-range discrepancy is not explained in the supplied text.
- The stale print still contains uncorrected tables and numbers despite its correction notice. The correction's abstract threshold of “440” is not the exact **447** included effects; do not treat thresholds as different samples.
- Broad invariance claims exceed nonsignificant moderator tests. Child/adolescent effects number only **27**, versus **420** adult effects.
- **Redistribution evidence**: neither supplied PMC print exposes an explicit CC/public-domain redistribution grant; “Copyright and License information” is only a collapsed heading. PMC availability is not permission. The assigned article/correction directory is kept in the private archive unchanged.

## Vault Ideas Extracted

- [Choice Architecture Effects](/vault/choice-architecture-effects.md) — Adds corrected intervention-family and default estimates together with extreme heterogeneity, a prediction interval crossing zero, and publication-bias scenarios that constrain general effectiveness claims.
