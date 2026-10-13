---
type: Study Note
title: Quantifying Visual Preferences Around the World
description: A large international screenshot study finds demographic differences in preferred complexity and colorfulness, but its observational first-impression models do not establish cultural causes or universal personalized-design benefits.
resource: https://doi.org/10.1145/2556288.2557052
source: https://doi.org/10.1145/2556288.2557052
tags: [aesthetics, inclusive-design, color, digital-interfaces, ux-metrics, user-research]
timestamp: 2026-10-12T20:26:53Z
---

# Visual Preferences Around the World — Study Notes

**Authors**: Katharina Reinecke and Krzysztof Z. Gajos.  
**Published**: CHI 2014, April 26–May 1, Toronto; DOI **10.1145/2556288.2557052**.  
**Status**: Peer-reviewed conference paper; read the supplied **ACM-format author-hosted PDF from Gajos's site**, including all seven figures, not a separately licensed Harvard DASH copy. Data collected June 2012–August 2013.  

## What It Is

A large LabintheWild study of **500-millisecond website appeal judgments**, extending [Reinecke et al.'s 2013 screenshot-model study](/dossiers/predicting-website-aesthetics-first-impressions.md). Its main contribution is evidence that **demographic groups differ even in early visual preferences** and that an aggregate complexity/colorfulness optimum is not everyone's optimum.

The headline dataset is approximately **2.4 million ratings from 39,975 volunteers**; the cleaned analysis comprises **1,542,166 individual observations, or 771,083 paired ratings from 32,222 people**. These denominators are not interchangeable. The study does not test task usability, trust, purchases, or whether an automatically personalized interface improves outcomes.

## Problem and Motivation

A guideline fitted to one population can obscure subgroup preferences. Earlier work often used small, homogeneous samples, expert awards, or excluded unusual tastes. The authors aim to quantify variation instead of treating disagreement as noise. Their proposal to personalize appearance follows from descriptive differences; the paper does not evaluate that intervention.

## Principle as an Idea

The model separates **computed visual properties**, **modeled perception**, and **observer-dependent liking**. It reuses the 2013 computationally calibrated estimates of perceived complexity and colorfulness rather than directly asking this sample to rate those two attributes. The appeal model adds nonlinear terms and demographic interactions. Symmetry and balance metrics were omitted because their ordering did not match the authors' visual sanity check.

The result is an audience-conditioned preference surface, not a claim that nationality determines taste. Complexity can be too low as well as too high; visual organization and image/text balance can make sites with similar computed complexity differ substantially in appeal. Figure 1's moderate-complexity examples include both well-liked composed pages and a poorly liked page at a similar score.

## Results / Admissions

### Sample, stimuli, and measures

- **39,975 volunteers**, **54% female**, from **179 countries**, ages **12–91**, mean **32.4 (SD 12.8)**; **41%** had at least some college education. **40%** had lived abroad for at least six months and/or had parents of different nationality. No monetary payment; participants received comparisons of their visual preferences with others.
- **430 screenshots**: **350 English-language sites, 60 other-script sites, 20 Webby nominees**. They were purposively selected for genre, limited public exposure, and complexity/colorfulness range. Original **1024×768** screenshots were downsized to **600 pixels wide** on white backgrounds.
- Five common practice pages anchored ratings. Participants saw a stratified random **30-site set**—22 English, four other-script, four award pages—for **500 ms** each, rating appeal on **1–9**. The same 30 appeared again in a newly randomized order. Instructions were English. No masking is described, and remote hardware/display timing was not laboratory controlled.
- Exclusions removed abnormal/uncorrected vision, repeats, incomplete or implausible demographics, and ages outside 12–91. **47,510 pairs** differing by more than two points were removed, labeled **4.9%** of observations; retained phase-difference **SD=.7**. Consistency filtering changes the target to relatively stable reported preferences rather than all first impressions.
- Country analyses further excluded mixed-nationality/migration backgrounds and countries below **1000 paired ratings**, leaving **18,448 people, 441,478 pairs, 43 countries**. This is a rating threshold, not 1000 participants per country. The US supplied **43%**, UK **17%**, Hungary **6%**, Canada **5%**, Romania **3%** of this subset.

### Modeling and general relationships

Linear mixed-effects models included participant/site random effects, linear/quadratic complexity and colorfulness, and demographic interactions; model selection retained age, gender, country, and education. Relative to the model without demographics, the full model improved fit, **χ²(290)=7408.7, p<.0001**. Relative to the null model, **χ²(294)=7510.9, p<.0001**.

**Conditional R²=.47** includes both fixed and random effects; **marginal R²=.07** describes the fixed predictors alone. Thus **47% is not variance explained by colorfulness, complexity, and demographics alone**, nor a held-out predictive accuracy. The authors explicitly caution that this R² method is not directly comparable with the 2013 **adjusted R²=.48**. No held-out site/person performance is established in the paper.

Peak locations were estimated using website-level bootstrap resampling **1000 times**, Lowess smoothing **α=.25**, and averages/standard errors of resulting maxima. These are dataset/model-dependent perceptual scores, not transferable layout or color specifications.

- Complexity predicts appeal, **F(1)=23.96, p<.001**, with average peak **4.2/10**. The prose gives peak-versus-low **d=.6** and peak-versus-high **d=2.0**; **Figure 1 instead labels d=.4 and d=1.4**, an unreconciled discrepancy. Low/high designate the bottom/top **5%** of sites, while peak comparisons use scores within **±.5** of the peak.
- Colorfulness predicts appeal, reported **F(1)=6.18, p<.001**, with peak **6.1/9**; peak-versus-low/high differences **d=.3/.8**. Complexity is generally the stronger appeal correlate. The F report omits denominator degrees of freedom, as do other ANOVA summaries.

### Demographic differences

| Moderator | Reported effect and peak estimates | Boundary |
|---|---|---|
| Age | Colorfulness interaction **F(1)=198.3, p<.001**; ages 31–40 peak **5.6 (SE .04)**, youngest/oldest groups **6.5 (SE<.03)**. Complexity effect **F(1)=1721.1, p<.001**; ages 12–40 peaks **4.1–4.2 (SE .1)**, 41–50 **4.5 (.1)**, over 50 **4.7 (.01)**. | Older groups prefer greater complexity here, **opposite the 2013 over-45 pattern**. Greater heterogeneity/lower education is the authors' proposed explanation, not an isolated causal test. |
| Gender | Colorfulness interaction **F(1)=658.9, p<.001**; male peak **5.8 (SE .04)**, female **6.3 (.03)**. Complexity interaction **F(1)=17.8, p<.001**; peaks nearly identical, **4.2/.01** and **4.3/.01**. | The more pronounced complexity difference is tolerance for very simple pages, not a large peak shift. Gender reporting uses two categories. |
| Country | Complexity interaction **F(32)=20.50, p<.001**; Russia peak **2.5 (SE .04)** versus Serbia, Bosnia and Herzegovina, Mexico, Chile **4.6–4.8 (SE<.03)**. Colorfulness interaction **F(32)=75.89, p<.001**; Finland/Russia/France/Germany **3.6–4.4 (SE .04)**, US **6.1 (.03)**, Chile/Malaysia **6.9**, Macedonia **7.6 (SE<.04)**. | Country subgroup results exclude mixed backgrounds; proximity/shared culture explanations are observational hypotheses. Country interaction degrees of freedom are not reconciled with the stated 43-country subset. |
| Education | Colorfulness interaction **F(7)=113.04, p<.001**; pre-high-school peak **6.9 (SE .03)** versus doctorate **5.0 (.04)**. Complexity interaction **F(7)=28.80, p<.001**; corresponding peaks **4.7/.01** versus **4.0/.01**. | Less education is associated with higher preferred scores, not evidence that education causes taste or that one group appreciates “better” design. |

Figures 3–4 show concrete disagreements: text-heavy sites can appeal more to older participants, and some bright childlike sites are disliked by both genders even when women rate them relatively higher. A relative subgroup preference is not absolute approval. Figures 5–7 show different curve shapes and peak shifts; they do not imply one deterministic national aesthetic.

## Analyst Takeaways

1. **Qualify simplicity with audience and range.** High complexity is generally disfavored, but extremely sparse pages are not necessarily best. This enriches [complexity/prototypicality evidence](/vault/visual-complexity-and-prototypicality.md) without measuring prototypicality.
2. **Put the contradictory age finding beside the earlier finding.** The 2013 older-user preference should not survive as a universal age rule after this larger extension.
3. **Keep conditional and marginal fit distinct.** Site/person random variation accounts for much of the .47 conditional fit; fixed predictors explain .07 by the reported measure.
4. **Use subgroup patterns to recruit and test, not stereotype.** A fitted peak is a hypothesis about a particular population and stimulus pool, not permission to decide an individual's taste from demographics.
5. **Separate appeal from warranted trust and useful interaction.** The introduction cites those downstream relationships, but this experiment measures neither.

## Questions and Limitations

- Self-selected English-reading online participants, unbalanced countries, historical screenshots, and filtered repeatability limit population transfer. Discarding multicultural backgrounds makes the country comparison less representative of real audiences.
- Static brief exposures cannot establish longitudinal preference, responsive/mobile appeal, motion effects, task performance, or personalized-design benefits. Cultural learning, generation, exposure, and socioeconomic causes are not randomized.
- The paper does not comprehensively report interactions **among demographic variables**; its discussion says the model incorporates them, but the main model description emphasizes demographic interactions with visual factors. Do not infer unreported subgroup coefficients.
- **Internal inconsistencies**: Figure 1's **d=.4/1.4** disagrees with prose **.6/2.0**. The named **47,510 pairs at 4.9%** do not reconcile transparently with **771,083 retained pairs** or the participant-level exclusions; the paper supplies no complete sequential denominator accounting. Country interaction **df=32** is not explained against **43 countries**. The education paragraph calls complexity “less influential for appeal,” whereas general results call it more informative than colorfulness; the narrower intended comparison is not made explicit. “Older than 51,” “over 50,” and “under 20” descriptions also vary around the plotted age-bin boundaries.
- The 2014 study expands the earlier program and corroborates complexity's broad role but is not an independent replication of its perceptual calibration or the masked complexity × prototypicality experiments. The authors invite broader-language and offline-population replication.
- **Redistribution decision: private.** The PDF's first-page notice states: **“Permission to make digital or hard copies of all or part of this work for personal or classroom use is granted without fee”**, subject to its conditions, but continues **“To copy otherwise, or republish, to post on servers or to redistribute to lists, requires prior specific permission and/or a fee.”** It also states **“Copyright © 2014 ACM”** and prints the DOI. **No CC BY or equivalent grant appears in this supplied file.** A separately listed Harvard DASH license does not license these bytes; archive this copy in `archive/private/`, retaining the canonical DOI as source.

## Vault Ideas Extracted

- [Visual Complexity and Prototypicality](/vault/visual-complexity-and-prototypicality.md) — Adds large-sample audience variation, a sparse-page boundary, contrary older-user results, and conditional-versus-marginal model-fit limits; does not measure prototypicality.
