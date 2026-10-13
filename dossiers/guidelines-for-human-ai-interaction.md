---
type: Study Note
title: Guidelines for Human-AI Interaction
description: Four iterative validation phases establish the inspectability and broad relevance of 18 human-AI design guidelines, not causal improvements in user performance or a complete ethical checklist.
resource: https://doi.org/10.1145/3290605.3300233
source: https://doi.org/10.1145/3290605.3300233
tags: [delegation, usability-evaluation, interaction-design, trust, digital-interfaces]
timestamp: 2026-10-12T23:54:54Z
---

# Guidelines for Human-AI Interaction — Study Notes

**Authors**: Saleema Amershi, Dan Weld, Mihaela Vorvoreanu, Adam Fourney, Besmira Nushi, Penny Collisson, Jina Suh, Shamsi Iqbal, Paul N. Bennett, Kori Inkpen, Jaime Teevan, Ruth Kikin-Gil, and Eric Horvitz.  
**Published**: CHI 2019, May 4–9, Glasgow; ACM proceedings, nominally 13 pages.  
**Status**: Peer-reviewed research paper synthesizing and iteratively evaluating design guidance. Read the complete supplied Microsoft camera-ready PDF, **19 physical pages**, including tables, count matrices, clarity/preference figures, references, and the application/violation appendix; DOI is printed in the file.  

## What It Is

A set of **18 inspectable design guidelines** for user-facing AI, refined through four phases. Its evidence concerns whether practitioners can understand, differentiate, and find instances of the guidelines across products. It is **not a controlled comparison showing that guideline-compliant interfaces improve task accuracy, trust calibration, or safety**.

## Problem and Motivation

Probabilistic and adaptive systems complicate ordinary expectations of consistency and error prevention: apparently identical inputs may yield different results, behavior can change over time, and inferred preferences may hide information or trigger unwanted actions. Guidance existed across communities but was scattered, implicit, or too abstract to inspect. The authors deliberately sought observable interface-level recommendations rather than general aspirations such as “build trust.”

## Guidelines as Ideas

The groups describe when a guideline is likely to matter, not an exclusive chronological sequence. The names below are the final Table 1 names, without reproducing the accompanying cards.

| Group | Guideline names |
|---|---|
| Initially | **G1** Make clear what the system can do; **G2** Make clear how well the system can do what it can do |
| During interaction | **G3** Time services based on context; **G4** Show contextually relevant information; **G5** Match relevant social norms; **G6** Mitigate social biases |
| When wrong | **G7** Support efficient invocation; **G8** Support efficient dismissal; **G9** Support efficient correction; **G10** Scope services when in doubt; **G11** Make clear why the system did what it did |
| Over time | **G12** Remember recent interactions; **G13** Learn from user behavior; **G14** Update and adapt cautiously; **G15** Encourage granular feedback; **G16** Convey the consequences of user actions; **G17** Provide global controls; **G18** Notify users about changes |

The important distinctions are capability versus reliability versus retrospective explanation; current context versus learned preference; recent conversational memory versus long-term adaptation; and instance-level correction/feedback versus global controls. These distinctions were actively revised because evaluators confused them, not simply asserted to be self-evident.

## Validation Design and Results

### Phase 1: consolidation

Industry guidance, product audits/customer feedback, public articles, and academic literature supplied **168 candidate recommendations**. **Three team members** used asynchronous affinity diagramming to form **35 concepts**, then filtered these to **20 initial guidelines**. Exclusions were too vague, scenario-specific, or not AI-specific. This was a synthesis, **not an exhaustive systematic literature search**.

### Phase 2: internal modified heuristic evaluation

**11 team members** inspected **13 AI-infused products/features**, each for approximately **one hour**, seeking applications as well as violations and commenting on clarity. These differed from Phase 3 products. The set included email filtering, navigation, recommendations, photo organization, productivity assistance, social feeds, and search.

Findings prompted merging, removal, splitting, and rephrasing, producing **18 guidelines**. Human fallback and handing control back were subsumed under uncertainty scoping; privacy settings under global controls. “Explore vs. exploit in moderation” and initial conservatism were removed because evaluators could not observe them reliably at the interface level. The paper gives no aggregate Phase 2 application/violation count or controlled user-outcome measure.

### Phase 3: practitioner inspection study

**49 practitioners** evaluated **20 popular products**, two per category, across **10 categories**. The evaluated features were ecommerce recommendations (**6 participants**); navigation, music recommendations, activity tracking, autocomplete, social-feed filtering, email importance filtering, and voice reminders (**5 each**); photo album suggestions and web search (**4 each**). Products were selected for varied scenarios from US popularity rankings; only **two** were Microsoft products.

Participants were recruited through a large software company's HCI/design lists, with **11 external interns** included. They had at least **one year** of HCI/UX experience; **39** reported high/very high familiarity with discount usability methods and **10** medium/low. Roles were **19 researchers, 12 designers, 11 interns, and 7 other practitioners**; **29 women, 18 men, 2 undisclosed**. Ages were reported in bins spanning **18–54**. Each product received roughly **2–3 evaluators** familiar with it.

After examples/training, participants explored one assigned feature and submitted illustrative instances, application/violation ratings on a **five-point semantic differential**, explanations, and optionally screenshots. They separately rated each guideline's clarity on a **five-point scale**. The activity was estimated at one hour, completed independently within a week, with **$50–$70** compensation.

The authors adjusted responses through two-pass review: **55 duplicate instances removed**, **73 inappropriate “does not apply” entries removed**, **20 “does not apply” entries reclassified as violations**, **56 cross-guideline misinterpretations identified**, and **14 further instances removed** where reviewers disagreed. The adjusted inventory was **785 responses: 313 applications, 277 violations, 89 neutral, and 106 does-not-apply**. These are elicited inspection reports, not 785 observed user failures or independent product-level prevalence estimates.

Figure 1 makes the distribution concrete: **G12** had **28 applications / 13 violations**, **G1 26 / 14**, **G11 8 / 27**, **G17 13 / 29**, and **G2 16 / 23**. Explanations, global controls, and reliability expectations were frequently judged missing or inadequate. **G3, G5, and G6** had **13, 12, and 11** does-not-apply entries respectively. Pull-based features limited timing relevance; social norms and biases were sometimes invisible to an evaluator rather than demonstrably absent.

The paper interprets a **40% or greater excess of applications over violations** as widely implemented; this is a descriptive cutoff, not a statistical test. G5/G6 were least clear in Figure 2. Systematic confusion meant at least **four** instances involving another guideline or repeated similar comments; revisions addressed G1/G2/G11 (**13 confusions**), G4/G13 (**6**), G3/G4 (**4**), G12/G13 (**7**), and G15/G17 (**6**).

### Phase 4: expert review of revisions

**11 additional experts**, **6 women / 5 men**, recruited by snowball sampling from the same company, compared old and revised wording for **nine guidelines**, then judged six confusing pairs. They included **6 UX designers, 3 UX researchers, and 2 research/product planners**, with **2 to more than 20 years** of experience; estimated duration **45 minutes**, compensation **$30**.

Figure 3 shows revised/old preferences: **G1 7/4; G2 7/4; G3 9/1** (one alternative proposed); **G4 10/1; G11 7/4; G12 9/2; G13 8/3; G15 1/10; G17 8/3**. The authors retained G15 despite the strong preference for old wording because it helped distinguish granular feedback from global controls.

Table 4 reports different-in-meaning / easy / hard / neutral counts: **G1/G2 10/6/5/0; G1/G11 11/6/3/2; G3/G4 10/6/2/3; G4/G13 11/9/1/1; G12/G13 9/7/1/3; G15/G17 10/9/1/1**. Thus **five experts still found G1/G2 hard to distinguish**. These are descriptive expert judgments, not an experimentally established improvement in problem-detection accuracy.

## Analyst Takeaways

1. **Use the guidelines to generate inspection questions, not certify an AI feature.** Relevance and understandable wording are valuable but do not establish causal benefits or exhaustive coverage; compare [heuristic evaluation](/vault/heuristic-evaluation.md).
2. **Separate three kinds of transparency.** What a feature can do, how reliably it can do it, and why a particular action happened answer different user questions. [System-status visibility](/vault/visibility-of-system-status.md) alone does not supply all three.
3. **Make failure handling part of the ordinary interaction.** Invocation, dismissal, correction, and constrained action are distinct controls, complementing [error prevention and recovery](/vault/error-prevention-and-recovery.md).
4. **Inspect change over time explicitly.** One short session cannot reveal every personalization or update effect. A longitudinal evaluation is needed to test long-term behavior, not merely a settings page.
5. **Do not equate an explanation's presence with appropriate reliance.** This paper establishes that practitioners can identify explanation gaps, not that supplying explanations improves error detection.

## Questions and Limitations

- Sampling centered on one company's practitioners and popular consumer products. Cross-country participation and external interns broaden the pool but do not eliminate organizational or cultural bias.
- Product identities are obscured, reported instances involve judgment, and reviewers removed ambiguous cases. No independent validity standard, false-positive rate, inter-rater coefficient, participant task-performance effect size, or user harm reduction is reported. No independent replication is established by this source.
- **Internal inconsistency**: the relevance prose says every guideline had an application or violation in every product category, but later says **G10 had none in social networks and G14 none in activity trackers**; Figure 1 confirms those exceptions. Broad cross-category relevance should not be rewritten as universal observed coverage.
- The demographics prose says ages **18–55**, while its actual bins end at **45–54**. The citation says **13 pages**, while this supplied camera-ready file has **19 physical pages**, including the extended appendix; preserve the version distinction.
- Domain-specific guidance remains necessary for non-graphical, high-risk, and regulated systems. Interface inspectability excludes some important modeling decisions. Guideline compliance is not an ethical guarantee; diversity may reveal harms majority evaluators miss.
- **Redistribution evidence**: the printed ACM notice grants personal/classroom copying, but states **“To copy otherwise, or republish, to post on servers or to redistribute to lists, requires prior specific permission and/or a fee.”** No Creative Commons or equivalent public redistribution grant appears; the raw PDF belongs in the private archive.

## Vault Ideas Extracted

- [Heuristic Evaluation](/vault/heuristic-evaluation.md) — Adds a modified inspection method that tests guideline relevance and clarity through both applications and violations, without validating end-user outcomes.
- [Visibility of System Status](/vault/visibility-of-system-status.md) — Distinguishes capability, reliability expectations, action explanation, and notifications of changed behavior.
- [Error Prevention and Recovery](/vault/error-prevention-and-recovery.md) — Separates invocation, dismissal, correction, uncertainty scoping, and granular versus global control.
- [Mixed-Initiative Interaction](/vault/mixed-initiative-interaction.md) — Adds cross-product inspectable guidance for balancing system initiative with user invocation, dismissal, correction, and cautious adaptation.
