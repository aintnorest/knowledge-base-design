---
type: Study Note
title: "To Trust or to Think: Cognitive Forcing Functions Can Reduce Overreliance on AI in AI-assisted Decision-making"
description: A 199-person nutrition experiment finds cognitive forcing reduces acceptance of incorrect AI ingredient choices but not overall team accuracy, with larger benefits for high-need-for-cognition participants and subjective tradeoffs.
resource: https://doi.org/10.1145/3449287
source: https://doi.org/10.1145/3449287
tags: [delegation, decision-making, trust, cognitive-load, human-performance, digital-interfaces]
timestamp: 2026-10-12T23:54:54Z
---

# Cognitive Forcing and Overreliance on AI — Study Notes

**Authors**: Zana Buçinca, Maja Barbara Malaya, and Krzysztof Z. Gajos.  
**Published**: Proceedings of the ACM on Human-Computer Interaction **5(CSCW1), Article 188, April 2021, 21 pages**; received October 2020, revised and accepted January 2021.  
**Status**: Peer-reviewed controlled online experiment. Read the complete **21-page author-hosted publication-layout PDF**, including all tables, stimulus and correlation figures, and references; DOI is printed in the file.  

## What It Is

A test of whether changing the interaction around an explanation makes people less likely to accept **incorrect AI advice**. Three cognitive-forcing designs are compared with two immediate explainable-AI designs and a no-AI baseline. The durable finding is **better decisions on AI-error trials**, particularly identifying the ingredient to remove, not a demonstrated increase in overall human–AI accuracy.

## Problem and Motivation

An explanation can become a general competence cue rather than evidence actively scrutinized for each decision. The authors use dual-process theory to propose that people often conserve effort through heuristics; a forcing intervention may interrupt that process and prompt independent reasoning. This is a hypothesized cognitive mechanism: the experiment measures decisions and ratings, not a direct switch between cognitive systems or actual explanation-reading depth.

## Study Design

### Participants, task, and simulated assistance

**260 US adult MTurk participants** were recruited in three batches. **49** were excluded for choosing an ingredient absent from the plate on more than **55%** of questions (these participants also scored zero overall); **12** saw only exploratory conditions omitted from this paper. The retained sample was **N = 199**; **191** supplied demographics, mean age **37.09, SD 10.74**, with **125 men (65.44%)** and the remainder women. Compensation was **$2.50**, plus **$3** for the top performer in each batch; average duration was **15 minutes**.

Participants saw meal photographs and chose **which ingredient to remove** and **which substitute to add**, optimizing carbohydrate reduction while preserving flavor. Each dropdown offered roughly **10 alternatives**; each meal had one clearly highest-carbohydrate ingredient. Thus complete optimal replacement required two choices, unlike merely identifying the carbohydrate source.

The AI was **simulated, not a trained model**, with **75% accuracy** on recognizing the highest-carbohydrate ingredient. On error trials it omitted that ingredient from its recognition and recommended replacing the second-highest-carbohydrate ingredient, which was low-carb. Explanations displayed **four ranked substitutions** and feature-based estimates of carbohydrate reduction and flavor similarity. Similarity used overlap of flavor-molecule sets; the optimization used the harmonic mean of similarity and carbohydrate reduction. These operational scores are not measured taste preference or nutritional health outcomes.

### Six reported conditions

| Category | Condition | Interaction |
|---|---|---|
| Baseline | No AI | Photo and choice menus without AI advice |
| Simple explainable AI (SXAI) | Explanation | Advice, recognized ingredients, and feature explanation shown immediately |
| SXAI | Uncertainty | Same, plus an “AI is X% confident” prompt only when uncertain |
| Cognitive forcing (CFF) | On demand | Advice/explanation hidden until requested |
| CFF | Update | Make an initial unaided choice before seeing advice/explanation and revising |
| CFF | Wait | Advice/explanation delayed **30 seconds**, with an “AI is processing the image” message |

Participants completed **two blocks of 13 questions**, each under a randomly assigned different condition drawn from **nine** total designs; three exploratory designs are not reported. The first question in each block was discarded as practice, leaving **24 analyzed trials**. There were **three AI-error trials per analyzed block**, **six total**; positions of correct/incorrect trials were fixed, with question order randomized within those positions. This is an incomplete mixed within/between-person design, not everyone experiencing all six reported conditions.

### Measures and analysis

Objective measures were complete optimal replacement accuracy; correct carbohydrate-source identification; carbohydrate reduction; flavor similarity; **overreliance = agreement with an incorrect AI prediction**; and other human error on AI-error trials. Overreliance does not require demonstrating that the same person would have answered correctly unaided; comparisons with no AI use other participants on the same questions.

After each block, five-point ratings measured preference, trust, mental demand, and system complexity. A **four-item Need for Cognition (NFC)** questionnaire was administered after block one. Mixed-effects ANOVA used category/condition as a fixed effect and participant as a random effect, with Holm–Bonferroni-corrected t-test post hoc comparisons; reported means are model-adjusted marginal means. Cohen's **d** accounts for the random effect. Pearson correlations relate ratings to performance.

## Results / Admissions

### Accuracy: all trials versus AI-error trials

| Measure | All trials: no AI / SXAI / CFF | AI-error trials: no AI / SXAI / CFF | CFF–SXAI error-trial effect |
|---|---|---|---|
| Complete optimal replacement | **.17 / .35 / .33** | **.18 / .03 / .09** | **d = .37** |
| Correct carbohydrate source | **.42 / .56 / .57** | **.49 / .08 / .27** | **d = .66** |
| Carbohydrate reduction | **21.73 / 35.70 / 35.20%** | **23.58 / 2.96 / 11.37%** | **d = .53** |
| Flavor similarity | **23.57 / 35.26 / 34.63%** | **24.00 / 3.37 / 11.28%** | **d = .53** |

Both AI categories beat no AI overall, but **CFF and SXAI did not significantly differ on any overall measure**. On AI-error trials, every metric followed **SXAI < CFF < no AI**. Error-trial category effects were **F(2,261.7) = 12.59** for complete performance and **F(2,242.6) = 35.59** for source detection, both printed **p ≪ .0001**. Thus CFF mitigated advice-induced harm but did not remove it, and **H1b (overall improvement) was unsupported**. No significant differences were found among designs within either category; there is no established winner among on-demand, update, and wait.

### Overreliance depends on the decision being scored

On incorrect advice, source-detection overreliance fell from **.64 SXAI to .48 CFF**, **F(1,145.8) = 9.24, p = .003, d = .36**; correct source decisions rose from **.08 to .27**, **F(1,197.4) = 24.11, p ≪ .0001, d = .66**. Other incorrect choices were unchanged (**.27 / .26**, nonsignificant).

For the **complete two-choice decision**, overreliance was **.30 / .26**, **F(1,180.9) = 1.02, nonsignificant, d = .12**. Complete correct choices still rose **.03 → .09**, **F(1,207.6) = 8.95, p = .003, d = .37**; other errors were **.68 / .65**, nonsignificant. The distributions differed by category (**χ²(2,N = 663) = 13.30, p = .0013** complete; **44.35, p ≪ .0001** source). **663 is the pooled error-trial decision count, not participant N**.

### Subjective tradeoffs

SXAI/CFF trust means were **3.91 / 3.72**, not significantly different. Preference was **3.13 no AI / 3.78 SXAI / 3.62 CFF**; both assisted categories beat no AI, not each other. Mental demand was **3.66 / 2.86 / 2.84**, higher without AI. System complexity was **3.19 / 2.64 / 2.95**, significantly lower in SXAI than CFF or no AI (**F(2,172.2) = 6.19, p = .002**).

On error trials, trust correlated negatively with complete accuracy (**r = −.24, p = .0003**) and source detection (**r = −.29, p = .0008**); preference similarly correlated with source detection (**r = −.21, p = .0005**). Mental demand correlated weakly positively with error-trial source accuracy (**r = .13, p = .03**), while trust correlated with source overreliance (**r = .14, p = .04**). These associations support a tension, **not a randomized causal finding that disliking an interface improves decisions**.

### Need for Cognition: unequal benefits

A **median split** classified high/low NFC. High-NFC participants had greater overall complete accuracy (**.44 vs .23; F(1,172.5) = 29.13, p ≪ .0001**) and source detection (**.67 vs .44; F(1,172.2) = 32.11, p ≪ .0001**) across assisted categories.

On AI-error trials, high-NFC complete accuracy improved **.02 SXAI → .11 CFF**, **p = .002, d = .57**; low-NFC improved **.03 → .06** in Table 4, nonsignificantly (**d = .15**). Source accuracy improved in both groups: high **.08 → .29, p = .0002, d = .69**; low **.09 → .26, p = .003, d = .57**.

Source overreliance fell significantly for high NFC, **.77 → .57, p = .004, d = .50**, but not significantly for low NFC, **.50 → .37, d = .27**. Complete-decision overreliance differences were nonsignificant for both groups. High NFC also rated CFF lower in trust (**3.89 → 3.56, p = .02**) and preference (**3.75 → 3.44, p = .03**), and higher in complexity (**2.64 → 2.95, p = .01**); low-NFC rating differences were nonsignificant.

The authors interpret these patterns as cognitive-motivation moderation and possible **intervention-generated inequality**. The reported subgroup tests and effect sizes are informative, but **a significant effect in one group and nonsignificant effect in another is not itself a significant interaction**; the paper does not report a direct condition × NFC interaction test establishing that moderation.

## Analyst Takeaways

1. **Evaluate incorrect-advice cases separately.** Aggregate gains can conceal severe local harm; easier acceptance of correct advice is not calibrated rejection of wrong advice.
2. **Change the decision sequence, not just the explanation text.** Independent initial judgment, requested advice, or time for thought can reduce some error acceptance, although this study does not establish which design is best.
3. **Do not optimize trust or preference as proxies for judgment.** Higher ratings can coexist with worse error detection. Measure actual decisions as well as experience.
4. **Audit who benefits from added effort.** Low-NFC participants did improve source detection; calling them unaffected would erase that benefit. The broader complete-decision gains were clearer for high NFC.
5. **Agent supervision is an extrapolation.** Asking a developer to assess a change before revealing an agent's recommendation follows the mechanism, but nutrition choices with simulated visual errors do not validate coding-review accuracy or a universal 30-second delay.

## Questions and Limitations

- One short, low-stakes lay nutrition task; no professional/high-stakes or longitudinal replication is established. Errors were controlled recognition omissions, not arbitrary model hallucinations, biased recommendations, or generative explanations.
- The incomplete assignment and pooled category analysis constrain individual-condition claims. Three exploratory designs are omitted, and detailed per-condition participant counts are not supplied in the method.
- **Scope mismatch in summaries**: the broad claim that CFF significantly reduces overreliance applies to **carbohydrate-source detection**, not the complete two-choice agreement measure. Overall accuracy does not significantly improve despite some discussion wording implying improved team performance.
- **Internal inconsistency**: low-NFC complete correctness under CFF is **.06 in Table 4 but .07 in Table 5**, with the same test/effect size. Record the discrepancy rather than infer an unreported analysis difference.
- Figure 2 prints **“r = −16”** for one preference correlation, an impossible Pearson coefficient; the source likely omits a decimal, but that value should not be cited as a verified statistic.
- The related-work claim that cognitive forcing is more effective in medicine cites reference **55**, titled **“Ineffectiveness of cognitive forcing strategies to reduce biases in diagnostic reasoning: a controlled trial.”** That citation does not straightforwardly support the general positive claim; medical generalization remains unestablished here.
- NFC is measured, not manipulated; it is not intelligence, disability, or willingness to comply. A median split loses information and the moderation claim lacks a reported direct interaction test. No tested personalization strategy follows from the proposed adaptive interventions.
- **Redistribution evidence**: the printed ACM notice limits free copying to personal/classroom use and states **“To copy otherwise, or republish, to post on servers or to redistribute to lists, requires prior specific permission and/or a fee.”** No explicit public redistribution grant appears; keep the author-hosted PDF private.

## Vault Ideas Extracted

- [Appropriate Reliance on Automation](/vault/appropriate-reliance-on-automation.md) — Supplies controlled cognitive-forcing evidence (N=199) reducing agreement with incorrect AI ingredient choices without significant overall accuracy gains; distinguishes behavioral reliance, self-reported trust, and motivation-dependent benefits.
- [Mixed-Initiative Interaction](/vault/mixed-initiative-interaction.md) — Adds experimental tests of requested advice, independent first decisions, and delayed advice, while preserving the absence of significant individual-design differences.
