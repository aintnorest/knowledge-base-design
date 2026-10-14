---
type: Study Note
title: No evidence for nudging after adjusting for publication bias
description: Bayesian reanalysis sharply reduces the corrected nudge meta-analysis's mean effect, but its overall evidence is inconclusive or weakly positive depending on dependence handling and does not rule out effective individual interventions.
resource: https://doi.org/10.1073/pnas.2200300119
source: https://doi.org/10.1073/pnas.2200300119
tags: [behavior-change, decision-making, user-research, survey]
timestamp: 2026-10-14T21:31:01Z
---

# Nudging and Publication-Bias Adjustment — Study Notes

**Authors**: Maximilian Maier, František Bartoš, T. D. Stanley, David R. Shanks, Adam J. L. Harris, and Eric-Jan Wagenmakers.  
**Published**: PNAS **119(31), e2200300119 (2022)**; online July 19, 2022.  
**Status**: Peer-reviewed letter reporting a Bayesian reanalysis, not a new participant experiment. Read the complete **six-page PMC print**, captured October 14, 2026, including Figure 1, Table 1, footnotes, and references.

## What It Is

A methodological counterweight to [Mertens et al.'s corrected meta-analysis](/dossiers/effectiveness-of-nudging-meta-analysis.md). Its argument is that selective publication of positive studies, rather than the unadjusted positive mean, should determine how confidently nudging is described as a broadly effective behavior-change tool.

The analysis uses the **corrected Mertens dataset**, whose parent synthesis reports **447 effects from 212 publications, pooled n = 2,148,439**. It inherits that review's randomized individual-level behavioral outcomes, real/hypothetical choices, and exclusions of combined techniques, rather than recruiting a new sample. Tasks span health, food, environment, finance, prosocial, and other choices; this is not exclusively digital-interface evidence.

## Model and Evidential Tradeoff

The authors dispute the original review's description of publication bias as moderate: its corrected **Egger coefficient b = 2.10** is severe under the criterion they cite, and its own severe-selection scenario reduces d to **.08**.

**Robust Bayesian meta-analysis (RoBMA)** combines selection models of relative publication probabilities with **PET/PEESE** models relating effect sizes to standard errors. Model averaging weights models according to prediction of observed data and assesses mean effect, heterogeneity, and publication bias. This avoids choosing one adjustment model as certain; it does not remove assumptions about selection, priors, or model coverage.

Because bias-corrected three-level selection models were computationally intractable, two analyses were used:

1. Include all estimates but **ignore the three-level structure and clustering of standard errors**.
2. Retain **only the most precise estimate** from studies with multiple results.

The first risks dependence-related overstatement of information; the second discards outcomes and changes representativeness. Neither reproduces the parent analysis's full hierarchy while also adjusting selection.

## Results

### Mean effect and intervention categories

Values below are model-averaged posterior means, **95% credible intervals**, and **BF01** (evidence for absence relative to presence). BF01 near one is undecided; **3–10** is moderate evidence for absence and **>10** strong evidence. These are not frequentist confidence intervals or probabilities that a nudge works.

| Group | All estimates: d [CrI]; BF01 | Most precise: d [CrI]; BF01 |
|---|---|---|
| Combined | .04 [.00,.14]; .95 | .11 [.00,.24]; .31 |
| Information | .00 [.00,.00]; 33.84 | .00 [.00,.07]; 10.57 |
| Structure | .12 [.00,.43]; 1.12 | .23 [.00,.49]; .33 |
| Assistance | .01 [.00,.07]; 9.05 | .01 [.00,.12]; 8.00 |

The unadjusted overall comparator is **d = .43 [.38,.48], t(333) = 16.51**. After adjustment, **BF01 = .95** for all estimates is essentially no discrimination between hypotheses, **not affirmative evidence of a zero mean**. For most-precise estimates, **BF01 = .31** corresponds to **BF10 ≈ 3.23**, which the text calls weak evidence for an overall effect. The headline “no evidence” therefore compresses a more conditional result.

Information and assistance show evidence against their average effects. Structure remains undecided with all estimates and modestly favors an effect with the most-precise subset (**BF10 ≈ 3.03**). This is not a universal null for defaults or every structural intervention.

### Behavioral domains

| Domain | All estimates: d [CrI]; BF01 | Most precise: d [CrI]; BF01 |
|---|---|---|
| Health | .01 [.00,.10]; 8.98 | .02 [.00,.19]; 3.53 |
| Food | .02 [−.09,.32]; 5.16 | .27 [.00,.64]; .55 |
| Environment | .01 [−.18,.25]; 4.41 | .00 [−.44,.34]; 3.05 |
| Finance | .00 [.00,.00]; 41.23 | .00 [.00,.00]; 30.95 |
| Prosocial | .00 [.00,.05]; 11.93 | .05 [.00,.27]; 1.89 |
| Other | .08 [.00,.33]; 1.38 | .04 [−.22,.40]; 2.45 |

With most-precise estimates, health, environment, and finance favor absence; food, prosocial, and other are indecisive. The printed zero-width intervals are rounded reported outputs, not proof of mathematically exact equality.

All intervention categories and domains except finance show evidence of **heterogeneity**. The authors explicitly acknowledge that some nudges may be effective even if their mean is unsupported. Publication-bias evidence is **BFpb > 10** across subdomains, except **food BFpb = 2.49** in the most-precise analysis. A footnote reports that restricting to statistical-significance selection models confirms the results, without giving the numerical sensitivity outputs in the letter.

The table's unadjusted category estimates differ from Mertens's moderator model: **information .25**, **structure .58**, **assistance .22**. The authors explain that they fit each subfield separately to allow separate effect tests and selection processes; these are not corrected replacements for Mertens's joint-model **.34/.54/.28**.

## Analyst Takeaways

1. **Bias sensitivity belongs beside the headline effect.** A positive average robust to leave-one-out checks can still shrink under models of systematic selection.
2. **Separate no evidence from evidence of no average effect.** BF01 ≈ 1 is indecision; information and finance provide much stronger null evidence than the combined sample.
3. **Preserve the heterogeneity qualification.** An unsupported mean does not settle whether one design, population, or task benefits.
4. **Do not treat adjustment as a certainty machine.** The dependence-handling compromises are material, and the two variants give meaningfully different overall evidence.
5. **Carry both accounts.** The [corrected Mertens dossier](/dossiers/effectiveness-of-nudging-meta-analysis.md) documents positive hierarchical estimates and bias scenarios; this one explains why those results are not a secure general forecast.

## Questions and Limitations

- A reanalysis of the same evidence is not an independent behavioral replication; it tests inferential robustness. No new participant task or deployment outcome is measured.
- The brief letter does not report full priors, subgroup sample counts, or numerical outputs for its selection-only robustness check; linked code/data are not analyzed here.
- **Internal inconsistency**: the footnote says the corrected dataset is in reference **12**, but reference **11** is Mertens's corrected CSV and reference 12 is Maier's analysis/code repository. Conversely, the data-availability statement points to reference **11** for data and analysis script. The reference descriptions do not match those pointers.
- The conclusion's blanket “no evidence remains” is stronger than its own most-precise overall **BF01 .31** and acknowledged heterogeneity. Its rule-of-thumb labels also place the reciprocal Bayes factor near the moderate-evidence boundary while the prose calls it weak.
- **Redistribution evidence**: the supplied PMC print contains only a collapsed “Copyright and License information” heading and no explicit redistribution grant. Free PMC access is not a licence; retain this copy privately and cite the DOI.

## Vault Ideas Extracted

- [Choice Architecture Effects](/vault/choice-architecture-effects.md) — Supplies publication-bias-adjusted means and Bayes factors, distinguishes an inconclusive overall effect from subgroup null evidence, and preserves possible effective nudges within heterogeneous evidence.
