---
type: Study Note
title: "When and Why Defaults Influence Decisions: A Meta-analysis of Default Effects"
description: A synthesis of 58 datasets finds substantial average opt-out effects but extreme heterogeneity, with endorsement and status-quo interpretations offering tentative rather than causal explanations.
resource: https://doi.org/10.1017/bpp.2018.43
source: /archive/default-effects-meta-analysis.pdf
tags: [decision-making, behavior-change, trust, survey]
timestamp: 2026-10-14T21:31:53Z
---

# Default Effects and Their Variability — Study Notes

**Authors**: Jon M. Jachimowicz, Shannon Duncan, Elke U. Weber, and Eric J. Johnson.  
**Published**: Behavioural Public Policy **3(2), 159–186 (2019)**; accepted December 10, 2018.  
**Status**: Peer-reviewed meta-analysis. Read the complete 28-page publisher PDF, including forest and funnel plots, both regression tables, references, coding instructions, and the appendix channel-correlation plot.

## What It Is

A quantitative synthesis of whether people choose an option more often when it is preselected and must be rejected than when it requires affirmative selection. The strongest finding is **an average opt-out effect with very large variation**, not a reliable forecast for a particular default or proof that default uptake improves welfare.

The scope spans consumer, environmental, health, financial, and other decisions rather than a specific interface. Software applications are possible, but the synthesis is not screen-specific.

## Problem and Motivation

Defaults are attractive because preselection can be simple to implement, yet policy makers must decide between defaults, active choice, smaller choice sets, deadlines, or different information presentations. The paper argues that spectacular examples such as organ donation should not stand in for a distribution of likely effects. It recommends rigorous local testing rather than assuming that any default will work.

## Evidence and Method

Searches of five databases, four conference-abstract sources, and academic mailing lists ended in **May 2017**. Inclusion required an explicit **opt-in versus opt-out** comparison and enough information to calculate an effect size. Active-choice-only comparisons were excluded. The final collection was **58 datasets from 55 studies in 35 articles, pooled N = 73,675**, with dataset sample sizes **51–41,952**; the largest was a German household energy trial. The abstract loosely calls these “58 default studies”; the method distinguishes datasets from studies.

Outcomes included binary uptake and continuous quantities such as donations or investment. A positive effect means greater selection/quantity under opt-out. Continuous differences were standardized by pooled SD; binary effects used an arcsine transformation expressed on the paper's d scale. The base random-effects model used inverse-variance weights and restricted maximum likelihood; a three-level model accommodated observations within studies within articles. Data and code are linked at <https://osf.io/tcbh7>.

Two external trained coders inferred likely psychological-channel activation from study designs, rather than observing participants' actual mediators. Endorsement and ease were rated **0–2 in half-steps**, endowment **0–1**; agreement was **κ = .59, .58, .80**, respectively. Domain coding by the first two authors had **κ = .94**; ten studies belonged to more than one domain.

## Results / Admissions

### Average influence is not uniform influence

- Base estimate: **d = .68, 95% CI [.53, .83], p < .001**.
- Three-level estimate: **d = .63, 95% CI [.47, .80], p < .001**.
- For **38 binary datasets**, **Cramér's V = .29, 95% CI [.21, .37]**, with the paper reporting an **absolute average uptake difference of 27.24%**. This is not a 27.24% relative lift or a universal expected conversion increase.
- **46 observations** were significantly positive, **10** nonsignificant, and **2** significantly negative.
- Heterogeneity was **I² = 98.21%** in the base model and **98.01%** in the three-level model. Even excluding datasets above 1,000 observations left base-model **I² = 92.85%**.

The forest plot makes both reversals and wide intervals visible. The synthesis aggregates repeated evidence across settings, but does not establish successful replication of every implementation or a new preregistered replication program.

### Three possible channels

1. **Endorsement**: preselection communicates what a trusted choice architect thinks one should do.
2. **Ease**: staying with the default requires less effort than changing it.
3. **Endowment**: the default becomes a reference point or perceived status quo, making departure feel like a loss.

In the model including study characteristics and channels, endorsement predicted larger effects (**b = .32, SE .15, p = .038**), as did endowment (**b = .31, SE .15, p = .044**); ease did not (**b = −.05, SE .15, p = .75**). With robust variance estimation, endorsement remained significant (**p ≈ .02**), but endowment weakened to **p = .081**. These are meta-regression associations based on inferred channels, not randomized causal mediation.

The authors explicitly warn that ease was noisily measured and lacked the substantial opt-out-effort variation seen in actual policy changes. **No detected ease moderator does not mean friction is irrelevant.** The appendix correlations are small (ease–endorsement **−.204**, ease–endowment **−.0551**, endorsement–endowment **−.13**).

### Context explains only part of the dispersion

With study characteristics alone, consumer decisions had larger effects (**b = .73, p = .003**; robust **p = .03**), while environmental decisions were weaker but not conventionally significant (**b = −.47, p = .08**). Adding channels gave consumer **b = .89, p = .0003** and environmental **b = −.60, p = .028**; the robust environmental test weakened to **p = .056**. Residual **I² remained 92.32%**. Online/offline presentation, field/lab setting, location, decade, financial consequences, and other coded attributes did not supply a stable explanation.

### Publication-bias diagnostics

Trim-and-fill imputed **eight missing larger effects**, increasing the estimate to **d = .80, 95% CI [.65, .96]**. Egger's asymmetry test was nonsignificant (**t(56) = −.39, p = .69**). The authors interpret this as no evidence that missing small effects inflate the mean, but caution that high heterogeneity complicates diagnostics. Imputed studies are not discovered replications, and a nonsignificant test cannot certify an unbiased literature.

## Analyst Takeaways

1. **Treat default selection as an intervention, not a neutral starting state.** It can communicate endorsement and define the comparison reference as well as reduce effort.
2. **Use the pooled effect to establish plausibility, not to forecast a launch.** Reversals and residual heterogeneity demand testing the actual decision and population.
3. **Separate uptake from informed preference and benefit.** This paper measures choices, not understanding, consent quality, or welfare.
4. **Measure the proposed mechanism directly.** Trust in the architect, perceived switching effort, and status-quo interpretation are better evidence than assuming preselection invokes all three.

## Questions and Limitations

- The search ends in 2017. This is a historical synthesis, not a current assessment of all default studies or later publication-bias debates.
- Channel ratings are subjective proxies with moderate agreement for endorsement and ease; moderator relationships can reflect confounding among study designs. Most heterogeneity remains unexplained.
- Preference strength, importance, and population preference distributions are proposed future moderators, not measured explanations. Personalized defaults and comparisons with other interventions remain research proposals.
- **Reporting distinctions**: the abstract's 58 “studies” are 58 datasets/55 studies; environmental and endowment claims become marginal under robust variance estimation. The paper's phrase that characteristics “reduce heterogeneity by 4.67%” describes the change from **98.21 to 93.54 percentage points**, not a 4.67% relative reduction.
- Cross-domain comparisons with other nudges in the discussion are not randomized head-to-head evidence that defaults are superior.
- **Redistribution evidence**: page 159 explicitly grants **Creative Commons Attribution 4.0**, permitting unrestricted reuse, distribution, and reproduction with attribution. The immutable publisher PDF belongs in the public archive.

## Vault Ideas Extracted

- [Choice Architecture Effects](/vault/choice-architecture-effects.md) — Adds the average opt-out effect, extreme heterogeneity and reversals, and the distinction between inferred endorsement/status-quo mechanisms and demonstrated causal mediation.
