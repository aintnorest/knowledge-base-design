---
type: Study Note
title: Facets of visual aesthetics
description: VisAWI construction and validation support four related website-aesthetics facets under a general factor, while incomplete divergent validity and untested cross-cultural and test–retest stability limit universal interpretation.
resource: https://doi.org/10.1016/j.ijhcs.2010.05.006
source: https://doi.org/10.1016/j.ijhcs.2010.05.006
tags: [aesthetics, ux-metrics, user-research, digital-interfaces, color]
timestamp: 2026-10-12T20:26:53Z
---

# Facets of Visual Aesthetics — Study Notes

**Authors**: Morten Moshagen and Meinald T. Thielsch.  
**Published**: International Journal of Human-Computer Studies **68(10), 2010, pp. 689–709**.  
**Status**: Peer-reviewed journal scale-development paper; read the supplied **40-page author-hosted manuscript**, with citation cover line, end-positioned tables, and both figures rather than publisher pagination.  

## What It Is

Construction and validation of the **18-item Visual Aesthetics of Website Inventory (VisAWI)**. Seven numbered studies support **Simplicity, Diversity, Colorfulness, and Craftsmanship**, modeled as four related first-order facets under a general second-order visual-aesthetics factor. Studies 4 and 5 analyze the **same 512 people**, not independent participant samples.

The instrument assesses **positive subjective evaluations of appearance**, not the amount of a physical feature. Colorfulness here means liking the selected/composed colors, not pixel saturation; Diversity means valuing the realized variety, not requiring maximal complexity. [Table 4 of the source](https://doi.org/10.1016/j.ijhcs.2010.05.006) provides the complete item list; it is not reproduced here. Its English wording is explicitly a translation of the German originals.

## Problem and Motivation

Single beauty questions and ad-hoc questionnaires differ in wording, reliability, and domain coverage. The authors also critique classical/expressive scales for descriptive items, abstract judgments, and missing explicit color coverage. They seek an operational definition broad enough to describe appearance while avoiding direct measurement of content, trust, or usability.

Their definition is **an immediate pleasurable subjective experience directed toward an object**, arising from interaction between object and observer. They distinguish aesthetic appraisal—what a person enjoys—from normative aesthetic judgment—what a person thinks should count as important or good art. The inventory concerns appraisal.

## Principle as an Idea

Aesthetic evaluation has both **shared overall valence and distinguishable facets**:

- **Simplicity**: perceived clarity, order, unity, grouping, and balance that facilitate visual grasp.
- **Diversity**: valued variety, novelty, dynamics, and interest.
- **Colorfulness**: aesthetic response to color selection, placement, and composition.
- **Craftsmanship**: coherent, careful, skilled integration and perceived contemporary execution.

Figure 1's second-order loadings for Studies 3/4 are **.80/.83**, **.87/.79**, **.83/.79**, and **.89/.89**, respectively. Comparable loadings support a common construct, not equal causal contributions to preference. Simplicity and Diversity connect to [classical/expressive aesthetics](/vault/classical-and-expressive-aesthetics.md), but the four-facet model is not an assertion that two-factor research was wholly wrong.

## Results / Admissions

### Construction studies

| Study | Participants and stimuli | Construction result |
|---|---|---|
| 1: domain definition | **256 convenience-sample users** rated importance of 34 literature-derived aspects; **10 experts** sorted/ranked **20 sites** and were interviewed | Expanded to 42 aspects, discarded two multi-page aspects, merged the remainder into **12 domains**. **96 initial items** were reviewed by four HCI experts and three laypeople, producing **84 items**, roughly half negatively keyed. Users rated simplicity **4.72/5**, colors **4.19**, proportion **4.01**; low movement ratings may conflate importance and dislike. |
| 2: exploratory factors | **300 volunteers**, 56% male, ages **15–64**, mean **27.80 (SD 9.69)**; **seven Finnish sites**, deliberately incomprehensible to German participants, links disabled | Seven problematic items removed; maximum-likelihood EFA with oblimin on **77 items**. Parallel analysis favored five factors, but comparative interpretation favored **six**, explaining **53%**; factor correlations **.14–.46**. Item selection/revision produced **39 items**. |
| 3: refinement | **506 volunteers**, 52.6% male, ages **13–63**, mean **27.56 (SD 8.11)**; **20 different Finnish sites** | Robust CFA initially fit poorly. Novelty/variety correlated **.97**, clarity/unity **.88**, motivating mergers and a higher-order factor. Further item removal produced the **18-item, four-facet model**. |
| 4: independent confirmation | **512 volunteers**, 347 female, ages **15–82**, mean **30.50 (SD 10.61)**; **42 German sites across nine domains** | Confirmed the final model without the incomprehensible-language restriction. Each participant evaluated a randomly drawn site while simultaneously viewing questionnaire items and the site. |

Final facet lengths are **5, 5, 4, 4 items**, with seven-point agreement responses. The original six-factor/39-item CFA had **χ²(687)=2230.94, CFI=.891, RMSEA=.067, SRMR=.083**. Modified Study 3 fit was **χ²(131)=415.00, CFI=.951, RMSEA=.065, SRMR=.053**; independent Study 4 **χ²(131)=405.57, CFI=.945, RMSEA=.064, SRMR=.052**. These are acceptable rather than perfect fits; all χ² tests are **p<.01**. Study 4 item loadings range **.63–.89**. An additional Study 3 EFA reported in the footnote yielded four factors explaining **67%**, corroborating but not independently replicating the refinement.

Study 4 internal consistency: **α=.89 Simplicity, .87 Diversity, .89 Colorfulness, .85 Craftsmanship, .94 total**. Reliability here is internal consistency, not test–retest stability.

### Validity studies

**Study 5 reuses Study 4's N=512 and 42 sites.** Correlations from summed scales show:

- Convergence: total score with classical aesthetics **r=.79**, expressive **.62**, and overall appeal **.80**; Simplicity with classical **.82**, Diversity with expressive **.80**.
- Divergence was **only partial**: total with perceived usability **.64**, pragmatic quality **.65**, and content quality **.62**. Simplicity–usability was **.76**. The authors propose bundled real-site quality and visual halo as explanations; neither is isolated in this analysis.
- Concurrent criterion: total with **intention to revisit r=.51**; this is stated intention, not observed returning.
- Discrimination: across-site MANOVA **F(205,2322)=2.19, p<.01**. Least-versus-most-aesthetic site differences were **d=2.26, 2.57, 1.86, 2.14**, and **1.99 total**, respectively. These deliberately selected extremes are not typical redesign effect sizes.

**Study 6: selective color manipulation.** **78 German-panel volunteers**, 55.1% male, ages **15–77**, mean **38.82 (SD 14.05)**, randomized **39/39** to two foundation-site versions. Participants performed search tasks before rating usability and VisAWI. The colors were required to be isoluminant; Figure 2 shows identical structure and content with turquoise/green versus blue navigation and accents.

Only Colorfulness changed significantly: **4.26 (SD 1.36) → 4.96 (1.10), d=.57, F(1,76)=6.23**, marked **p<.01 one-sided** in Table 7. Simplicity **d=.08**, Diversity **−.02**, Craftsmanship **−.10**, total **.19** were nonsignificant. Post-interaction usability correlations were lower: **r=.31 total, .48 Simplicity, .41 Craftsmanship**; Diversity **.19** and Colorfulness **.04** nonsignificant. This comparison is consistent with more differentiated judgments after use, but different samples/sites prevent attributing the cross-study drop to interaction alone.

**Study 7: bundled appearance manipulation.** **375 web volunteers**, 284 female, ages **18–47**, mean **25.18 (SD 6.05)**, randomized to pleasant **n=172** or distorted **n=203** health-information sites. A designer unaware of VisAWI altered color, density, picture quality, and typography while retaining content and broad structure. All facets differed, with **d=.94 Simplicity, .49 Diversity, 1.12 Colorfulness, 1.60 Craftsmanship**, and **1.22 total**. Corresponding univariate **F(1,373)=82.48, 22.13, 114.90, 235.99, 137.05**, marked **p<.01 one-sided**. The experiment supports responsiveness to appearance change, not attribution of the effects to any single altered property.

## Analyst Takeaways

1. **Separate presence from appraisal.** More color or novelty does not automatically mean a better facet score; the inventory captures evaluated quality.
2. **Inspect facets alongside the total.** A moderate color-only effect can disappear in the overall score, as Study 6 demonstrates.
3. **Use reliability and validity claims precisely.** Strong α and independent CFA support measurement, but do not establish population invariance, temporal reliability, or causal downstream behavior.
4. **Keep usability measurement separate.** Appearance–usability correlations fell after actual tasks, reinforcing the conditional [aesthetic–usability effect](/vault/aesthetic-usability-effect.md).

## Questions and Limitations

- Convenience samples share a German cultural background; neither sites nor participants represent the web. Finnish/non-navigable development stimuli reduce content familiarity but are artificial. Independent Study 4 is a within-program replication, not a cross-cultural one.
- No test–retest reliability, nonvisual aesthetics, mobile-interface transfer, or actual revisit behavior was established. Conscious agreement ratings may not fully capture immediate aesthetic response. Some Diversity wording remains too abstract to diagnose a design change.
- **Source inconsistencies**: the stimulus-selection description says **eight descriptive criteria** but lists **seven bipolar pairs**. It also calls the earlier Lavie–Tractinsky initial pool **44 items**, whereas that source explicitly reports **41**. Study 7 prints MANOVA **F(370,3)=76.13**, an anomalous/reversed degrees-of-freedom statement given four facets and N=375; no correction is inferred. Study 6 reports **F(4,73)=2.69, p<.01** without qualifying it as one-sided; the detailed table explicitly uses one-sided univariate significance, so preserve that distinction rather than repeat an unqualified threshold.
- The abstract says “Colors”; the operational scale is called “Colorfulness.” Its evaluative meaning differs from the computed colorfulness in [Reinecke's screenshot models](/dossiers/predicting-website-aesthetics-first-impressions.md).
- **Redistribution evidence**: the cover explicitly prints **doi:10.1016/j.ijhcs.2010.05.006** and requests citation; the supplied manuscript contains **no explicit public-redistribution license or grant**. Author hosting and a citation request are not permission to redistribute; the raw PDF belongs in `archive/private/`.

## Vault Ideas Extracted

- [Classical and Expressive Aesthetics](/vault/classical-and-expressive-aesthetics.md) — Extends order/expression into a validated four-facet hierarchy and shows that evaluative color and craftsmanship carry distinguishable meaning.
- [Aesthetic–Usability Effect](/vault/aesthetic-usability-effect.md) — Provides differentiated facet correlations and a lower appearance–usability association after task interaction, without proving interaction caused the cross-study difference.
