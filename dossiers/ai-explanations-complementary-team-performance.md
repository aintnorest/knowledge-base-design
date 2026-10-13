---
type: Study Note
title: Does the Whole Exceed its Parts? The Effect of AI Explanations on Complementary Team Performance
description: Three crowdworker tasks produce human–AI accuracy above either partner alone, but local explanations add no significant accuracy benefit beyond recommendations with confidence and can increase acceptance of wrong advice.
resource: https://doi.org/10.1145/3411764.3445717
source: https://doi.org/10.1145/3411764.3445717
tags: [delegation, decision-making, trust, human-performance, usability-evaluation, digital-interfaces]
timestamp: 2026-10-12T23:54:54Z
---

# AI Explanations and Complementary Team Performance — Study Notes

**Authors**: Gagan Bansal, Tongshuang Wu, Joyce Zhou, Raymond Fok, Besmira Nushi, Ece Kamar, Marco Tulio Ribeiro, and Daniel S. Weld; Bansal and Wu contributed equally.  
**Published**: CHI 2021, May 8–13, Yokohama; ACM proceedings, **16 pages**.  
**Status**: Peer-reviewed mixed-method experimental paper. Read the complete **16-page lab-hosted camera-ready/publication-layout PDF**, including all figures, tables, and references; DOI is printed on page one. The read file names the author **Joyce Zhou**, not Joyce Zhu as in some citations.  

## What It Is

A test of **complementary team performance**: can a human–AI team outperform **both** the human and the AI acting alone, and do explanations improve that result beyond showing a recommendation and confidence?

Earlier explanation studies often compared teams against weaker unaided humans, while the AI alone remained better than every team. This paper intentionally selects task samples where human and AI accuracy are comparable. It finds complementarity in all teaming conditions, **but no significant incremental accuracy benefit from the tested explanations**.

## Problem and Motivation

An explanation can make a recommendation convincing without revealing when it is wrong. If people accept correct and incorrect recommendations more often, aggregate performance may change little. A stronger test must compare with a useful non-explanation baseline and inspect the model's errors separately.

Comparable aggregate accuracy only creates an opportunity for complementarity. The **distribution and overlap of human and AI errors** determine whether one partner actually knows something the other does not. The authors argue that end-to-end decisions are a better test of this objective than asking people to simulate a model's predictions.

## Experimental Design

### Tasks, assistance, and conditions

Three tasks were chosen for crowdworkers without specialized training:

- **Beer**: classify sentiment in **50 beer reviews**.
- **Amzbook**: classify sentiment in **50 book reviews**.
- **LSAT**: answer **20 logical-reasoning multiple-choice questions**, each with **four options** and one correct answer.

Sentiment models were fine-tuned **RoBERTa** classifiers; confidence was post-hoc calibrated with isotonic regression. Task examples were selected to make AI accuracy **84%** on each sentiment dataset, with equal false-positive/negative counts. A RoBERTa reasoning model fine-tuned on ReClor achieved **65%** on selected LSAT questions, versus **67%** unaided human pilot accuracy. These are **curated study-sample accuracies**, not general deployment performance.

Each sentiment dataset had **six between-person conditions**: Human alone; Team (Conf), recommendation plus confidence; Explain-Top-1 (AI), explanation for predicted class; Explain-Top-2 (AI), explanations for both classes; Adaptive (AI); and Adaptive (Expert). LSAT had **five**: Human, Conf, and Top-1, Top-2, Adaptive with **expert explanations only**.

Sentiment explanations highlighted influential phrases inline; AI explanations used **LIME**, while one author selected short convincing spans for expert explanations. LSAT explanations were concise supporting arguments: the correct-answer account was condensed from an LSAT prep book, while alternatives were manually crafted. They are expert-authored rationales attached to model predictions, **not a faithful account of the model's hidden reasoning**.

Adaptive explained only the top prediction at high confidence and added the alternative below a threshold. Sentiment thresholds were the median confidences, **89.2% Beer / 88.9% Amzbook**, creating **25 Top-1 and 25 Top-2 examples** each. The Top-2 half contained **18 correct / 7 incorrect** AI predictions, leaving **24 correct / 1 incorrect** in Top-1. Thus low confidence helped locate most, but not all, errors. Figure 3 shows LSAT explanations in a separate pane and top-two confidence rescaled to sum to 100%.

### Pilots, participants, and procedure

The initial Beer pilot used a logistic-regression classifier and **150 workers, 50 per condition**, comparing confidence-only, Top-1, and Top-2. It suggested increased reliance without a significant overall accuracy benefit. Another **150 workers** estimated unaided accuracy across three tasks; pilots informed the final design and hypotheses, not independent replications of every finding.

The final method reports recruitment of **566 Beer + 552 Amzbook + 508 LSAT = 1,626 workers**. Workers were US-based, had **≥97% approval** and **≥1,000 approved tasks**. Sentiment screening required **four correct out of six**; about **84%** passed screening and post-filtering, yielding **93–101 analyzed participants per condition**. Post-filtering removed median response times below **two seconds** or constant labels.

LSAT screening required both of **two** questions correct; median response times below **three seconds** were removed. The printed LSAT passage says **35% of 508** passed and completed the task, yet says **100 participants per condition** across five conditions. This is an unresolved denominator contradiction; **1,626 is recruitment, not a defensible exact retained analysis N**.

Participants were randomly assigned to one condition, saw the same item order within a dataset, and received correctness feedback after each question. Incentives combined base pay, per-answer bonuses, survey payment, and additional accuracy thresholds intended to discourage blindly copying the AI. Mean task durations/pay were **13 minutes / $3.35** for sentiment and **16 minutes / $6.30** for LSAT. Mean per-item times were approximately **17 seconds** for sentiment and **one minute** for LSAT. The paper does not supply a full demographic breakdown.

### Measures

The primary outcome was **accuracy of final human decisions**. Figure 4 plots means and **95% confidence intervals**, separately overall and by whether the AI was correct. Figure 5 measures **human–AI agreement**, split at the adaptive-confidence threshold. These are not equivalent: disagreeing with the AI only improves accuracy if the human then supplies the right answer.

Post-task five-point ratings assessed usefulness of AI assistance and of explanations; these analyses were explicitly exploratory and **not tested for statistical significance**. Free-text strategies were qualitatively coded. The authors describe significance testing as Student's t-tests with Bonferroni correction, but report **z**-labelled statistics in result prose; retain that reporting ambiguity.

## Results / Admissions

### Complementarity does not establish explanation benefit

For Beer, confidence-only assistance achieved **.89 mean accuracy, SD .05**, above **.84 AI alone** and **.82 unaided human, SD .09**. Confidence-only also exceeded both partners on Amzbook and LSAT; reported relative gains over unaided people were **2.2%** and **20.1%** respectively. Figure 4 shows every teaming condition in the complementary zone.

No explanation condition significantly exceeded confidence-only:

- Beer Top-1: **.88, SD .06** versus confidence-only **.89, SD .05**, printed **z = −1.18, p = .24**. Corresponding comparisons: Amzbook **z = 1.23, p = .22**; LSAT **z = .427, p = .64**.
- Top-1 versus Top-2 was nonsignificant: Beer **z = .85, p = .40**; Amzbook **z = .81, p = .42**; LSAT **z = .42, p = .68**.
- Adaptive versus confidence-only was nonsignificant: Beer **z = −1.02, p = .31**; Amzbook **z = 1.08, p = .28**; LSAT **z = .16, p = .87**.
- Expert versus AI Adaptive explanations did not significantly change sentiment accuracy: Beer **z = 1.31, p = .19**; Amzbook **z = −.78, p = .43**.

These are **failures to detect an incremental advantage**, not formal equivalence tests proving every explanation has zero effect. Standardized effect sizes are not supplied, and exact overall numeric means for all conditions are chiefly graphical rather than tabulated.

### Incorrect recommendations reveal the cost

Figure 4B shows Top-1 explanations tending to improve accuracy when the AI was right but worsen it when wrong, especially **Beer and LSAT**. Amzbook differs: its incorrect-AI subset improved by approximately **5%** over confidence-only according to the prose. Thus the abstract's broad acceptance claim needs the dataset boundary; the wrong-advice penalty is not uniform across every task.

Adaptive explanations altered agreement in the intended direction, reducing agreement with lower-confidence recommendations and retaining greater agreement with high-confidence ones. This did **not** significantly improve total accuracy. The authors propose two reasons: confident errors still require detection, and doubting low-confidence advice is insufficient if people cannot solve the underlying task themselves. These are interpretations, not separately randomized mechanism tests.

Figure 6 exposes the error-overlap boundary: Beer and LSAT contain examples easy for humans but wrong for AI, and other examples where AI helps struggling humans. Amzbook has less useful complementarity. “Comparable accuracy” alone is therefore not a sufficient partner-selection criterion.

### Experience and qualitative strategies

Expert Adaptive assistance was more often rated useful than confidence-only: **70% vs 57% Beer**, **65% vs 49% Amzbook**, **63% vs 45% LSAT**. Expert explanations themselves received higher usefulness ratings than AI Adaptive: **53% vs 38% Beer**, **50% vs 40% Amzbook**. These descriptive preferences did not translate into a measured accuracy advantage.

Two annotators coded **409 unique responses**, after removing **11** poor-quality responses; mean **Cohen's κ = .71, SD .18**, raw agreement **93%, SD 6.5%**. The exclusive strategy codes counted **23 mostly follow AI (6%)**, **190 AI as prior guide (47%)**, **102 AI as post-check (25%)**, and **90 mostly ignore AI (22%)**. Nonexclusive codes included **138 explicit explanation use**, **17 explanation-based validation**, **90 confidence use**, **24 confidence thresholds**, **54 fallback to AI**, and **12 strategy changes**.

Only **17** explicitly described validating reasoning; this does not mean only 17 actually did so, because these are unprompted self-reports, not behavioral traces. Sentiment users more often used AI as a prior; LSAT users more often used it as a check. Interface separation, task difficulty, and expertise differ simultaneously, so their causal contributions are not isolated. Reported faster reading from highlights is qualitative, not a controlled measured speed benefit.

## Analyst Takeaways

1. **Require the right baseline.** Improving on an unaided person is different from exceeding the stronger teammate, and adding an explanation must be compared with recommendation-plus-confidence.
2. **Distinguish persuasion from discriminative information.** A plausible rationale can increase compliance without helping detect failure. Evaluate correct- and incorrect-advice subsets explicitly.
3. **Choose complementary partners, not merely similar accuracies.** Different error patterns create the opportunity for productive oversight; inspection should identify where humans add information.
4. **Do not treat doubt as a correct answer.** Lower agreement is useful only when the replacement decision is better. Adaptive alternatives need task-solving support, not just skepticism cues.
5. **For AI-agent supervision, transfer is an extrapolation.** Measure whether reviewers catch actual agent mistakes and whether the combined workflow beats its stronger baseline; this study does not validate generated code rationales or expert high-stakes oversight.

## Questions and Limitations

- Short curated crowdworker tasks, static local explanations, immediate correctness feedback, and unusually explicit accuracy incentives limit generalization. No independent replication of the complete intervention package is established here; cross-task corroboration is within the same paper.
- Similar accuracy was engineered through sample selection, not representative deployment sampling. Final unaided Beer accuracy (**82%**) also differs from its pilot (**87%**), illustrating why pilot matching does not guarantee identical realized abilities.
- No proof that explanations are useless for learning, accountability, legal justification, debugging, or other outcomes. Accuracy alone does not settle speed, workload, accountability, or user agency.
- Expert explanations were created by one author, and alternative LSAT rationales were deliberately persuasive arguments. Explanation quality/faithfulness was not fully separated from format, placement, and anchoring.
- **Internal inconsistency**: LSAT's **508 recruits / 35% retained** cannot yield **100 people in each of five conditions**. The introduction's **1,626 users** matches total recruitment, but the conclusion's “more than 1,500 participants” should not be read as an established retained sample size.
- The text references an explainer-comparison **Appendix**, but this supplied **16-page file ends with references**, not that appendix. Its claimed rationale for choosing RoBERTa/LIME is reported but the detailed comparison cannot be inspected in this version.
- Table 3's exclusive collaboration counts total **405**, not the stated **409 coded responses**; the discrepancy is not explained. The prose also calls **17%** of Beer/Amzbook users validators, while the table gives **17 people / 5%** overall; subgroup denominators differ and are not fully reconstructed.
- Figure 6's caption associates fewer easy-for-human examples with “bars towards the left,” whereas the same caption defines easy examples on the right. The plotted axis, not that phrase, supplies the orientation.
- Result prose repeatedly refers to hypotheses as **“4.1”** rather than H1–H4 and labels test statistics **z** after describing t-tests. Null results are not equivalence evidence; preserve the reporting imperfections rather than invent a precise analysis specification.
- **Redistribution evidence**: page one has the ordinary ACM personal/classroom notice, including **“To copy otherwise, or republish, to post on servers or to redistribute to lists, requires prior specific permission and/or a fee.”** It states copyright held by the owners/authors and publication rights licensed to ACM; **no printed Creative Commons or equivalent redistribution grant** appears. Lab hosting does not authorize a public archive; retain the raw PDF privately.

## Vault Ideas Extracted

- [Appropriate Reliance on Automation](/vault/appropriate-reliance-on-automation.md) — Defines complementarity against both solo partners and distinguishes agreement from correctness; explanations increased acceptance without accuracy beyond confidence alone, with task-dependent harm on wrong advice.
- [Mixed-Initiative Interaction](/vault/mixed-initiative-interaction.md) — Adds the experimentally unvalidated timing/independent-judgment design proposals motivated by upfront-answer anchoring and limited explanation gains.
