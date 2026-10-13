---
type: Study Note
title: What is beautiful is usable
description: A 124-person ATM-simulation experiment finds appearance predicts post-use perceived usability despite deliberately slower interaction, but not better task performance or inevitable persistence across systems.
resource: https://doi.org/10.1016/S0953-5438(00)00031-X
source: https://doi.org/10.1016/S0953-5438(00)00031-X
tags: [aesthetics, usability-evaluation, digital-interfaces, ux-metrics, user-research]
timestamp: 2026-10-12T20:26:53Z
---

# What Is Beautiful Is Usable — Study Notes

**Authors**: N. Tractinsky, A.S. Katz, and D. Ikar.  
**Published**: Interacting with Computers **13(2), 2000, pp. 127–145**; accepted March 24, 2000.  
**Status**: Peer-reviewed journal experiment; read the publisher-layout author-hosted PDF preserved in the supplied **2011 Wayback Machine snapshot**, including all tables, three result figures, and both stimulus appendices.  

## What It Is

An interaction-based extension of [Tractinsky's 1997 apparent-usability studies](/dossiers/aesthetics-and-apparent-usability.md). Participants first rated ATM layouts, then operated a simulator whose appearance and interaction difficulties were varied separately. Beauty and perceived usability remained associated after use, while the usability treatment changed completion time without significantly changing subjective evaluations.

This **is the later ATM interaction study** summarized in the existing [aesthetic–usability synthesis](/vault/aesthetic-usability-effect.md). It supplies the missing participant denominator, but its primary statistics do **not** reproduce the later review's **partial η²=.037** using the conventional conversion from F and degrees of freedom.

## Problem and Motivation

Pre-use beauty–ease correlations cannot establish that first impressions survive actual difficulty. The study asks whether use dissolves the association and whether appearance colors every judgment indiscriminately. Perceived amount of information serves as a comparison attribute; satisfaction is added after use.

## Mechanism as an Idea

### Design, participants, and task

**132 third-year industrial-engineering students** participated for class credit; mean age **25**, approximately **67% male**. Eight were excluded because their highest and lowest beauty ratings differed by **three points or less**, leaving **124 analyzed participants**.

The actual design is **3 aesthetics levels × 2 usability levels**, between groups, despite the methods' opening description as “2 × 2.” Nine layouts were selected from the earlier 26-layout family, with identical objects arranged differently. Participants rated each layout separately for aesthetics, ease of use, and information amount on **1–10 single-item scales**: **27 layout–attribute combinations in randomized order**. Assigned high-, medium-, or low-aesthetics conditions used a layout matching that participant's own ratings. The paper explicitly reports random allocation to usability within aesthetics conditions after practice; it does not comparably specify random allocation to aesthetics.

Six analyzed cells, ordered high/low usability, were **21/20** at high aesthetics, **20/19** at medium aesthetics, and **23/21** at low aesthetics. Four practice task types preceded **11 fixed-order experimental tasks**: three balance inquiries, four withdrawals, two combined inquiries/withdrawals, and two deposits. A shared four-digit code operated the simulation; no physical cash changed hands. Appendices show a regular telephone-style keypad and a horizontally dispersed alternative, with Hebrew messages and separate task/rating areas. The appearance manipulation therefore concerns spatial organization, not purely decorative polish.

Low usability added approximately **nine seconds of delay per task**, buttons that failed on their first press, and removal of a shortcut in one task. Participants were urged to finish quickly. Completion time and errors were recorded. Afterwards, participants again rated aesthetics, usability, and information amount, plus satisfaction, using single-item subjective measures.

### Proposed explanation

Stereotyping, an initial-appearance halo, and appearance-induced positive affect are **alternative proposed mechanisms**, not measured mediators. The evidence concerns judgments following a short interaction, not emotional processing or long-term acceptance.

## Results / Admissions

- **Manipulations**: pre-use beauty means were **8.26, 4.97, 2.07**, **F(2,121)=338.58, p<.001**; all pairwise Scheffé contrasts were significant at .001. High-usability tasks averaged **23.5 seconds**, versus **37.5 seconds** under low usability, **F(1,118)=414.05, p<.001**. Nine of the 14 additional seconds were programmed delays. Appearance had no time effect, **F(2,118)=.01, p=.987**, or time interaction, **F(2,118)=.96, p=.387**. Mean session errors were **1.26**, with no significant main or interaction effects reported.
- **Individual-level correlations, N=124**: beauty–usability was **r=.66 before** and **r=.71 after** use; post-use satisfaction correlated **r=.87** with usability and **r=.71** with aesthetics. Table 2 marks these **p<.01**. Pre-to-post stability was **r=.62** for aesthetics, **.48** for usability, and **.63** for information amount. Unlike the 1997 layout-mean correlations, these do not use 26 aggregated stimulus means.
- **Adjusted post-use judgments**: the MANCOVA used pre-use apparent usability as covariate and post-use usability, aesthetics, satisfaction, and information amount as outcomes. Roy–Bargmann stepdown analysis entered usability first. **Table 3** gives appearance → perceived usability **F(2,117)=4.75, p<.01**, and appearance → aesthetics **univariate F(2,117)=9.73, p<.001; stepdown F(2,116)=4.49, p<.01**. Satisfaction was significant univariately, **F(2,117)=4.88, p<.01**, but not after preceding outcomes, **F(2,115)=.06**.
- **Effect-size reconciliation**: the conventional reconstruction for the primary adjusted usability effect is **partial η²=(2×4.75)/(2×4.75+117)=.0751**. The paper itself reports no η². The previously recorded **.037** is a later secondary reconstruction, not this paper's reported effect size; neither Table 3 nor its reversed prose establishes it as the correct primary partial η².
- The interaction-difficulty factor had no significant adjusted subjective effects: perceived usability **F(1,117)=1.38**, aesthetics **1.17**, satisfaction **2.92**, information amount **.04**. Appearance × usability was also nonsignificant; perceived usability **F(2,117)=.66**. Nonsignificance does not establish that usability is irrelevant.
- Adjusted usability contrasts favored high over low aesthetics, **t=3.06, p<.01**, and high over medium, **t=2.20, p=.03**. Figure 1 shows lower post-use ratings at lower aesthetics, with near-overlap of usability treatments under high aesthetics; that visual pattern does not override the null interaction test.
- Change-score analyses tell a different story from post-use levels. Aesthetics changed by aesthetics condition, **F(2,118)=36.04, p<.001**; medium/low groups improved. Usability change had only **F(2,118)=2.63, p=.07**. Figure 2's high-aesthetics/high-usability bar falls, while its high-aesthetics/low-usability bar rises, qualifying the prose's blanket description of a high-aesthetics decrease. Extreme-score-based layout selection also makes regression toward the mean a plausible alternative to the proposed mere-exposure/adaptation explanation.

## Analyst Takeaways

1. **Keep performance and evaluation separate.** Appearance influenced perceived ease, not measured speed or errors here; the title must not become “beauty makes systems objectively usable.”
2. **Use the primary table for corrections.** Record **132 recruited, 124 analyzed**, the **3 × 2** design, and **F(2,117)=4.75** rather than carrying forward an unexplained secondary η².
3. **Persistence is conditional evidence.** The later 80-person online-shop null case documented in the [1997 dossier](/dossiers/aesthetics-and-apparent-usability.md) limits generalization; it does not negate this experiment's result.
4. **Aesthetic organization overlaps visible usability cues.** Personalized layouts vary grouping and keypad arrangement, so this is not a clean test of ornamental attractiveness alone.

## Questions and Limitations

- The methods incorrectly call the design **2 × 2** before specifying three aesthetics levels. The paragraph interpreting Table 3 **swaps the outcome labels** attached to **4.75 (2,117)** and **4.49 (2,116)**; the table and stated stepdown order identify usability first. Preserve these inconsistencies rather than silently quoting the reversed prose.
- Single items, engineering students, exclusions ensuring appearance contrast, short simulator use, fixed task order, and personalized stimulus selection restrict transfer. Actual-usability difficulties emphasize latency and unreliable activation rather than navigation or task comprehension. Covariate adjustment does not isolate a psychological mediation mechanism.
- No long-term acceptance or positive-affect performance benefit was measured. The paper speculates about both. Independent replication is not established here; later research contains a directly manipulated post-use boundary case.
- **Redistribution evidence**: the first page states **“© 2000 Elsevier Science B.V. All rights reserved.”** It prints **PII: S0953-5438(00)00031-X**, confirming the publisher identifier underlying the DOI key. No public redistribution grant appears; the raw copy belongs in `archive/private/` and the source remains the DOI URL.

## Vault Ideas Extracted

- [Aesthetic–Usability Effect](/vault/aesthetic-usability-effect.md) — Adds the exact short-interaction design and participant denominator, distinguishes subjective persistence from performance, and corrects the unexplained secondary effect-size reconstruction against Table 3.
