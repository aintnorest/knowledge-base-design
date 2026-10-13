---
type: Study Note
title: "The Cost of Interrupted Work: More Speed and Stress"
description: A 48-person email experiment finds interrupted primary work is completed faster with no detected error or politeness penalty but greater stress and effort, without establishing faster total workflows or equivalence between interruption contexts.
resource: https://doi.org/10.1145/1357054.1357072
source: https://doi.org/10.1145/1357054.1357072
tags: [attention, human-performance, cognitive-load, digital-interfaces, ux-metrics]
timestamp: 2026-10-12T23:51:52Z
---

# The Cost of Interrupted Work — Study Notes

**Authors**: Gloria Mark, Daniela Gudith, and Ulrich Klocke.  
**Published**: Proceedings of the SIGCHI Conference on Human Factors in Computing Systems, **CHI 2008, pp. 107–110**, April 6, 2008.  
**Status**: Peer-reviewed four-page conference short paper; read the supplied UCI author-hosted manuscript, including all three tables and references. It lacks the publisher's pagination, DOI, and copyright block. Crossref verifies the DOI by matching the authors, main title, subtitle, venue, and pages; this is not the publisher version of record.  

## What It Is

A controlled experiment asking whether an interruption on the **same topic** as ongoing work is less disruptive than one on a different topic. It also examines workload and personality differences. Its memorable result is a dissociation: participants completed the primary email work faster when interrupted, while reporting higher stress, frustration, and effort.

That result is not evidence that interruptions improve overall productivity. The time measure **subtracts time spent responding to interruptions**; it does not establish a shorter end-to-end workflow. The authors interpret faster primary work as compensation for expected lost time, not as a free performance benefit.

## Problem and Motivation

Earlier field reports suggested same-context interruptions could be beneficial, whereas experiments found interruption costs under other conditions. The paper distinguishes topical similarity from similarity of cognitive operations: an interruption about human resources can share a topic with an email without helping answer that email or using the same operations.

The study tests three possibilities: different-topic switching adds cost; similar material causes interference; or discontinuity itself matters irrespective of topic. It also asks whether time alone hides the psychological cost of coping.

## Mechanism and Study Design

**48 participants**, **15 men and 33 women**, had a mean age of **26**; **81% were German university students**. All had a German high-school qualification; all but one had used email for at least two years. Half had used instant messaging for at least one year, while **29.2% had never used it**. Participation paid **€12**.

A **3 × 2 mixed factorial design** crossed:

- **Within-person context**: baseline without interruption (**B**), same-context interruption (**S**), and different-context interruption (**D**). All six orders were counterbalanced, with random assignment to order.
- **Between-person medium**: telephone or instant messaging, randomly assigned. The paper does not explicitly report the number assigned to each medium.

Participants played a human-resource manager returning from vacation at a craft-supply company. They answered **12 emails per condition**, using a fact sheet about staffing, education, and overtime. Instructions and incentives emphasized quick, correct, polite answers. A trial email familiarized them with the equipment. Pilot studies reportedly matched block topics and difficulty, but pilot sample sizes and results are not supplied.

The experimenter acted as a supervisor, interrupting approximately **every two minutes**, with an instruction to respond immediately. S questions concerned human resources, such as current departmental staffing; D questions concerned unrelated matters, such as hot dogs needed for a company party. Pilots checked perceived context differences. The experimenter adjusted interruption duration to make conditions as comparable as possible. The session lasted about **1½ hours**; workload ratings followed each email block.

### Measures and their boundaries

- **Primary-task time**: manually recorded block duration minus interruption duration. This captures net time spent on the primary work, including any recovery overhead, but does not separately measure resumption lag or moment-to-moment working speed.
- **Quality proxies**: spelling errors, typos, and other mistakes such as misspelled names; a politeness score based on greetings, closings, and polite words. These are narrower than factual completeness, usefulness, or professional-quality judgments.
- **Email length**: average words per message, considered as a possible explanation for faster work.
- **Modified NASA-TLX**: the six facets of mental demand, physical demand, performance, temporal demand renamed time pressure, effort, and frustration, plus an added **stress** rating. Ratings use **1 low to 20 high**. Results report five facets only: mental workload, stress, frustration, time pressure, and effort; physical demand and performance results are not given.
- **Personality**: the German NEO-PI-R Openness to Actions subscale and **10 items** measuring Personal Need for Structure. These are correlational predictors, not manipulated treatments.

The proposed mechanism is **compensatory acceleration**, possibly combined with briefer responses. The authors also allow that a local recovery slowdown might be masked by faster work elsewhere in the block. Neither mechanism is directly established by block-level timing.

## Results / Admissions

### Primary work becomes faster, not demonstrably better

Table 1 reports means with standard deviations in parentheses:

| Measure | B: no interruption | S: same context | D: different context |
|---|---|---|---|
| Primary-task time, minutes | **22.77 (7.60)** | **20.31 (5.94)** | **20.60 (4.93)** |
| Reported average error count | **1.94 (.91)** | **1.93 (.88)** | **1.84 (.92)** |
| Words per email | **31.49 (8.10)** | **29.17 (7.02)** | **30.16 (7.18)** |
| Politeness score | **28.98 (5.37)** | **28.69 (5.89)** | **28.90 (6.30)** |

Context condition affected primary time, **F(2,77.98) = 3.36, p < .05**. B was slower than S, **F(1,46) = 4.22, p < .05**, and D, **F(1,46) = 4.13, p < .05**. The means imply **2.46 / 2.17 minutes less primary-work time**, approximately **10.8% / 9.5%**, calculated from Table 1 rather than reported standardized effects. **S versus D was not significant**; that is not an equivalence test establishing identical costs.

The medium main effect was not significant, printed as **F(1,92) = .20, p < .66**, and there was no significant medium–context interaction on time. This does not prove every telephone and IM interruption is equally costly.

Errors did not significantly differ, **F(2,92) = 1.70, p < .19**, nor did politeness, **F(2,92) = .10, p < .91**. No medium interactions were found for these quality proxies. Absence of a detected difference should not be described as verified equal quality.

Email length differed overall, **F(2,92) = 3.34, p < .04**. B messages were longer than S, **F(1,46) = 5.57, p < .05**, but B versus D was nonsignificant, **F(1,46) = 2.20, p < .15**. Writing less is therefore only a partial candidate explanation; the study did not isolate its contribution to speed.

Interruption durations in S and D did not significantly differ: reported difference **.62 minutes, SD 2.8**, **t(47) = 1.52, p < .14**. Nonsignificance does not establish perfectly matched duration. The paper does not give the two duration means or total elapsed-time comparison needed to claim an overall throughput gain.

### Faster work carries subjective cost

Table 3 reports means and standard deviations on the **1–20** scales:

| Facet | B | S | D | Reported context effect |
|---|---|---|---|---|
| Mental workload | **10.02 (3.90)** | **10.83 (3.96)** | **11.50 (3.55)** | **F(2,92) = 3.82, p < .03**; D > B, **p < .01**; D versus S nonsignificant, **p < .16** |
| Stress | **6.92 (3.85)** | **9.46 (3.97)** | **9.13 (4.10)** | **F(2,92) = 12.15, p < .001**; both interruption conditions > B, **p < .001** |
| Frustration | **4.73 (2.93)** | **6.63 (4.19)** | **6.48 (4.45)** | **F(2,92) = 5.21, p < .007**; both > B, **p < .01** |
| Time pressure | **11.02 (4.57)** | **12.69 (4.45)** | **12.17 (4.26)** | **F(2,92) = 4.71, p < .01**; S > B, **p < .01**; D versus B only **p < .10** |
| Effort | **9.50 (3.38)** | **11.04 (3.78)** | **11.52 (3.31)** | **F(2,79) = 8.50, p < .001**; S > B, **p < .05**; D > B, **p < .001** |

There were no reported medium interactions on these measures. Stress, frustration, and effort support costs in both interruption conditions; the paper's blanket conclusion is stronger than the individual comparisons for mental workload and D-condition time pressure. These are subjective ratings, not physiological stress measures or evidence of chronic harm.

### Personality predictions are modest and exploratory

A stepwise regression combined the interrupted conditions to predict primary-task time excluding interruption duration. It reported **R² = .14**, **F(2,47) = 3.41, p < .04**. Openness had **β = −.363, t = −2.22, p = .03**; need for personal structure had **β = −.346, t = −2.13, p = .04**. Higher scores on either predicted faster interrupted work.

The structure result runs **opposite to the introduction's expectation** that less need for structure would lower cost. The authors suggest better time management as a possible explanation, not an observed mediator. Moreover, the outcome is absolute interrupted-task time, not a baseline-subtracted interruption penalty, so it does not isolate interruption-specific coping from general task speed.

## Analyst Takeaways

1. **Do not use time alone to declare an interruption harmless.** Faster primary work can coexist with greater effort and distress; perceived efficiency and sustainable workload are different outcomes.
2. **Separate topical relevance from actual assistance.** Sharing a domain did not yield a detected advantage here, but an interruption that supplies the answer or supports the same operation is a different treatment.
3. **Keep elapsed time, active work, and recovery lag separate.** Subtracting interruption duration permits a primary-speed result; it cannot establish a net workflow benefit or absence of a local recovery cost.
4. **Treat reduced response length as a strategy change worth inspecting.** Error and politeness counts may miss lost detail or completeness. This study does not demonstrate those harms, but neither does it rule them out.
5. **Preserve people's ability to regulate secondary demands.** The authors propose tracking and controlling interruptions over longer periods and customization to tolerance. Those are implications, not tested system designs or validated personality-based policies.

For software or AI-agent supervision, the analogous risk is mistaking fast handling of status requests for low supervisory burden. That is an **extrapolation** from forced office-email interruptions, not a study of AI agents, autonomous execution, or user-controlled notification queues. The result complements [Interruption Costs](/vault/interruption-costs.md) and the [attention-aware systems experiment](/dossiers/attention-aware-systems-interruption-effects.md): different tasks and measures can reveal slowdown or compensatory speed without making the affective cost disappear.

## Questions and Limitations

- One laboratory experiment, mostly students, with an artificial supervisor and compulsory immediate responses. It does not establish long-term adaptation, fatigue accumulation, voluntary postponement, or consequences in safety-critical work. No independent replication of this exact design is established here.
- “Same context” means shared topic, not shared operation or an interruption directly facilitating the current answer. The discussion explicitly acknowledges these differences from earlier studies. Its assertion that context does not matter generalizes beyond a nonsignificant S–D contrast in this manipulation.
- No raw data, confidence intervals, standardized effects, separately measured recovery lag, or detailed quality-scoring reliability are provided. The table's error-count denominator is not specified as clearly as its words-per-email measure.
- Physical demand and self-rated performance were named as collected TLX facets but omitted from results. The conclusion that all interrupted workload dimensions rose significantly is too broad: D versus B time pressure was only **p < .10**, and the S-versus-B mental-workload contrast is not reported.
- Statistical reporting contains unexplained degrees of freedom: the between-person medium result is **F(1,92)** despite **48 participants**, effort uses **F(2,79)** without a missing-data or correction account, and the two-predictor regression reports **F(2,47)**. The fractional time denominator may reflect a correction, but no method is specified. Preserve these as printed rather than silently repairing them.
- The observed need-for-structure direction contradicts the introductory hypothesis, which the discussion acknowledges. A **14%** exploratory regression is not a validated individual scheduling rule. There is no pre-registration or multiplicity-control account for the many outcomes and contrasts.
- **Redistribution evidence**: no Creative Commons notice or explicit redistribution grant appears in the complete four-page author manuscript. Author hosting is not a redistribution license; the raw PDF belongs in the private archive and the dossier cites the verified DOI.

## Vault Ideas Extracted

- [Interruption Costs](/vault/interruption-costs.md) — Adds the distinction between faster active primary work and higher stress, frustration, and effort; bounds the finding to forced interruptions and treats context nulls as nondetection rather than equivalence.
