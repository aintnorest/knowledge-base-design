---
type: Study Note
title: "On the need for attention-aware systems: Measuring effects of interruption on task performance, error rate, and affective state"
description: A 50-person experiment finds mid-task interruptions increase within-person completion time and between-group errors, annoyance, and anxiety relative to task-boundary delivery, but it tests forced modal tasks rather than freely managed notifications.
resource: https://doi.org/10.1016/j.chb.2005.12.009
source: https://doi.org/10.1016/j.chb.2005.12.009
tags: [attention, cognitive-load, human-performance, interaction-design, digital-interfaces, ux-metrics]
timestamp: 2026-10-12T20:26:48Z
---

# Attention-Aware Systems and Interruption Effects — Study Notes

**Authors**: Brian P. Bailey and Joseph A. Konstan.  
**Published**: Computers in Human Behavior **22(4), 2006, pp. 685–708**; available online February 7, 2006.  
**Status**: Peer-reviewed controlled experiment. Read the complete **24-page publisher-layout PDF** supplied from the third-party literature site interruptions.net, including figures and references; DOI is printed on the first page. The paper expands results from the same experiment partly reported by Bailey, Konstan, and Carlis in 2001, not a new replication of that earlier report.  

## What It Is

An experiment isolating **when** secondary work is presented: halfway through a primary task versus just after that task finishes. Both groups perform the same amount of primary and peripheral work. This separates interruption timing from the common confound of giving the interrupted group additional work.

The main claim is not that secondary information should never appear. It is that delivery at a meaningful boundary can reduce disruption without removing the secondary task. The evidence distinguishes immediate primary-task slowdown from broader error and affective differences; the abstract compresses these distinct comparisons too aggressively.

## Problem and Motivation

Notifications, messages, and system-initiated interactions impose costs beyond their own duration. People may need to recover the suspended goal and intermediate state, and may allocate resources in anticipation of another interruption. Measuring only elapsed time misses errors and affective consequences.

Following Miyata and Norman, the authors hypothesize that task completion releases mental resources before the next task acquires them. A task boundary should therefore be a less disruptive point for secondary work. This is a theoretical explanation: the experiment tests timing effects but **does not directly measure working-memory allocation or physiological workload**.

## Mechanism and Study Design

**50 participants**, **20 women**, ages **18–40**, with at least **one year** of computer experience, included students and working professionals. Random assignment, constrained by gender balance, produced **25 per group**: each **15 men/10 women**. Primary-task category and peripheral-task category were within-person factors; timing was between-person: a **6 × 3 × 2 mixed design**.

Each person completed **18 primary tasks** (three in each category) and **12 peripheral tasks** (six reading, six reasoning). Within each primary category, one trial had a reading peripheral task, another a reasoning task, and one none. Task-category, task-instance, and peripheral-task orders were randomized, with practice and opportunities to rest between categories.

| Primary category | Stimulus and response |
|---|---|
| Addition | Mentally sum four four-digit numbers and enter the total. |
| Counting | Count a target word in a **40-word, 10 × 4** table. |
| Reading comprehension | Read **7–10 sentences** and answer three questions. |
| Image comprehension | Inspect an eight-team tournament bracket and answer five questions. |
| Selection | Select matching target words in a **40-word, 10 × 4** checkbox table. |
| Registration | Answer eight form-style questions using text fields and selections. |

Primary tasks were piloted with **five users** to target approximately **30 seconds**, although actual categories differed. Peripheral tasks, piloted with five users to target approximately **20 seconds**, involved reading a **3–5-sentence** news item and selecting a title, or reasoning about a stock scenario and choosing a trading action. Figures 1 and 2 show these concrete stimuli rather than full realistic applications.

The experimental group received secondary tasks about halfway through the primary task; the control group received them after selecting the primary task's “finished” link and before the next primary task. Secondary tasks appeared in **modal windows covering the primary work area**. Participants were instructed to attend immediately and perform all tasks quickly while maintaining accuracy. They could not choose to ignore, postpone, or batch the interruption.

### Measures

- **Time on primary task (TOT)** excludes the time doing peripheral work. It captures primary-work overhead, not total elapsed workflow time or a separately measured resumption lag.
- **Time on peripheral task (TOP)** measures secondary-work duration.
- **Errors** were scored from screen recordings against correct answers; registration and peripheral tasks were excluded because the authors classified them as lacking objectively right/wrong answers.
- **Difficulty** used rankings from **1 easiest to 6 hardest**, permitting ties.
- **Annoyance** used a continuous **1–25** scale, with category labels positioned after all computer tasks. Ratings assessed receiving peripheral tasks relative to each primary category and performing each peripheral category.
- **State anxiety** used the **20-question STAI Y-1**, range **20–80**, immediately before and after the session. It cannot locate anxiety changes at individual interruptions. Sessions lasted approximately **60 minutes**.

## Results / Admissions

### Primary-task completion: the comparison matters

The **between-group timing main effect on primary time was not significant**, **F(1,47) = 0.16, p < .69** as printed. Peripheral task interacted with timing, **F(2,94) = 4.79, p < .01**. The clearest time evidence is therefore the **within-person interrupted versus noninterrupted comparison inside the experimental group**, not a significant blanket group-speed difference.

Within that group, peripheral category affected primary time, **F(2,46) = 15.69, p < .001**: reading interruptions yielded **33.60 seconds**, reasoning **32.15 seconds**, versus **29.16 seconds** without interruption (**p < .001 / p < .002**). The two interruption categories did not significantly differ.

| Category | Interrupted / noninterrupted primary time | Reported slowdown and significance |
|---|---|---|
| Addition | **39.06 / 31.51 s** | **24%, p < .001** |
| Counting | **19.31 / 15.25 s** | **27%, p < .001** |
| Reading | **49.32 / 45.94 s** | **7%, p < .04** |
| Image comprehension | **38.28 / 34.71 s** | **10%, p < .05** |
| Selection | **18.88 / 16.21 s** | **16%, p < .03** |
| Registration | **32.39 / 31.34 s** | **3%, p < .001** |

In the control group, peripheral task had no significant effect on primary time, **F(2,48) = 2.37, p < .10**, with no interaction. This is consistent with lower boundary-delivery cost, not proof that the true cost is exactly zero.

The source says slowdown tends to rise with task difficulty, but the measured difficulty order was addition, reading, counting, image, selection, registration: reading was second-hardest yet slowed only **7%**, while counting slowed **27%**. Difficulty is not a monotonic predictor of the relative penalty.

### Peripheral work

Reading peripheral tasks took **25.96 seconds** on average versus **17.10 seconds** for reasoning, **F(1,47) = 98.01, p < .001**. Timing was only **marginal**, **F(1,47) = 3.05, p < .087**. Experimental-group secondary tasks were about **15% faster**: reading **23.87 versus 27.97 seconds**, reasoning **15.50 versus 18.64 seconds**, with **p < .10 / p < .08**. Faster return motivated by interruption is an interpretation, not a separately measured motivation effect. These results do not establish a significant secondary-task advantage at conventional .05.

### Errors: group-level rather than immediate-trial cost

The experimental group averaged **0.22 errors per scored primary task** versus **0.11** in the control group, approximately two versus one error per ten tasks: timing **F(1,48) = 67.30, p < .001**. Task category also mattered, **F(4,192) = 4.35, p < .002**.

However, neither the overall peripheral-task factor nor its within-experimental-group analysis significantly affected errors (**F(2,96) = 0.95, p < .39**; **F(2,48) = 0.18, p < .83**). Thus the study does **not** show that each interrupted trial immediately doubles error. Anticipatory resource allocation or residual interference are plausible accounts of the group difference; the design does not isolate them from each other.

### Annoyance and anxiety

Timing increased primary-relative annoyance, **F(1,48) = 9.18, p < .01**: **11.40 experimental versus 7.29 control**. The authors describe this as “about 64%”; the reported means actually imply approximately **56%**, an unresolved arithmetic inconsistency.

Category-specific annoyance increased **68% addition**, **31% reading**, **106% counting**, **41% image**, **50% selection**, and **40% registration**. Reading and registration comparisons were only marginal (**p < .055 / p < .065**), while addition/counting were **p < .001**, image **p < .038**, and selection **p < .03**. A timing–category interaction, **F(5,240) = 5.18, p < .001**, reflects larger addition/counting changes. These percentages summarize numeric ratings on an anchored subjective scale, not ratio-scale quantities of emotion.

Peripheral-task annoyance also differed, **F(1,48) = 13.10, p < .001**: **12.85 versus 7.57**. The paper calls this “about 60%,” whereas those means imply approximately **70%**. Reading was more annoying than reasoning. Even boundary-delivered work was more annoying following difficult primary tasks, suggesting completion is not necessarily instantaneous psychological recovery.

Both groups' anxiety rose. The session–timing interaction was **F(1,48) = 3.90, p < .05**: experimental STAI increased **32.32 → 44.04**, a change of **11.72**, while control increased **32.68 → 38.96**, a change of **6.28** (**p < .028** for the comparison reported). This is about **1.87 times the increase**, not twice the final anxiety level or a diagnosis of an anxiety disorder.

## Analyst Takeaways

1. **Place deferrable secondary work at meaningful completion boundaries.** Timing matters even when total assigned work is unchanged; “more work” is not the sole explanation.
2. **Preserve the distinction between overhead and interruption duration.** The **3–27%** figures exclude secondary-work time and are within-group trial penalties, not a universal workflow slowdown or significant overall between-group time effect.
3. **Measure emotional cost as well as speed.** Faster secondary responses can coexist with worse annoyance and anxiety; a quick dismissal is not proof of a good notification.
4. **Account for anticipatory and residual costs.** Group-wide errors may change even on individual trials without an interruption. The exact mechanism remains unresolved.
5. **Balance deferral with urgency and relevance.** The source recommends bounded waiting and shorter deferral for urgent/relevant information, particularly in non-safety-critical work; those scheduling policies are design implications, not experimentally validated algorithms.

The closure rationale complements [response-time thresholds](/vault/response-time-thresholds.md), while adding empirical timing evidence rather than a new universal seconds-based rule. [Working-memory limits](/vault/working-memory-capacity-limits.md) make context recovery a plausible design concern, but memory capacity was not directly measured here.

## Questions and Limitations

- Forced modal secondary tasks with immediate-response instructions are not equivalent to unobtrusive cues or user-controlled notifications. These results cannot establish the cost of every banner, sound, or message that can be postponed.
- The primary tasks have clear boundaries and little carryover. Boundaries embedded in extended activities may not provide the same release; fine-grained subtask boundaries and automatic boundary detection remain proposals.
- Frequency, complexity, relevance, urgency, rehearsal opportunity, and presentation style were not experimentally varied. Neither attention latency nor resumption lag was directly measured, and no physiological workload measure validates the proposed resource-release mechanism.
- Completion-time analyses use degrees of freedom implying **49 users**, while the study recruited **50** and other analyses use all 50; no missing-data/exclusion explanation is supplied. No confidence intervals or standardized effects are reported.
- The abstract's **3–27%** summary implies a direct boundary-versus-mid-task time comparison, whereas the detailed significant percentages compare interrupted and uninterrupted trials within the experimental group. The lack of a timing main effect must remain visible.
- In addition to the annoyance arithmetic discrepancies, the text twice says interruption causes a “decrease in completion time” where its tables/graphs and surrounding argument show an increase in time, meaning decreased performance. Its statement that boundary deferral was “no more than a few seconds” is not supported by a delay distribution and sits uneasily beside halfway interruptions in tasks lasting roughly **15–49 seconds**. Do not turn that claim into a measured universal deferral budget.
- The addition-task description specifies four four-digit numbers, but Figure 1a shows decimal monetary amounts (for example **79.32** and **24.96**). The figure's concrete arithmetic stimulus is not the integer-like example implied by the method prose; retain this ambiguity when describing the task's cognitive demands.
- Some p-values and t-test descriptions are unusually reported, including **F(1,48) = 104.04, p < .01** and small t statistics paired with one-sided-looking p thresholds despite the general Bonferroni statement. Preserve printed values without implying a fully reconstructable analysis.
- Related studies corroborate interruption costs under other tasks; the 2001 report is the **same dataset**, not independent replication. No independent replication of this exact workload-controlled experiment is established here.
- **Redistribution evidence**: the PDF states **“© 2005 Elsevier Ltd. All rights reserved.”** on the first page. No explicit redistribution grant appears. Hosting on interruptions.net does not authorize a public archive; keep the raw publisher PDF private.

## Vault Ideas Extracted

- [Interruption Costs](/vault/interruption-costs.md) — Supplies workload-controlled timing evidence for primary-work overhead, group-level errors, annoyance, and anxiety, bounded to forced modal tasks.
- [Response-Time Thresholds](/vault/response-time-thresholds.md) — Adds empirical support for locating deferrable work after closure, without establishing a universal optimal delay or proving instantaneous recovery.
- [Working-Memory Capacity Limits](/vault/working-memory-capacity-limits.md) — Connects interruptions with suspended-goal recovery and possible anticipatory resource allocation while clearly marking these mechanisms as inferred.
- [Interruption Coordination](/vault/interruption-coordination.md) — Supplies controlled evidence for scheduling deferrable interruptions at task boundaries rather than mid-task, bounded to forced modal interruptions.
