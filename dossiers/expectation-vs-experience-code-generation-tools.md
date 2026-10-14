---
type: Study Note
title: "Expectation vs. Experience: Evaluating the Usability of Code Generation Tools Powered by Large Language Models"
description: A 24-person within-subjects programming study finds strong preference for generated-code assistance without significant completion-time or success gains, with comprehension and repair costs observed in short Python tasks.
resource: https://doi.org/10.1145/3491101.3519665
source: https://doi.org/10.1145/3491101.3519665
tags: [delegation, usability-evaluation, cognitive-load, trust, human-performance, digital-interfaces]
timestamp: 2026-10-14T21:30:36Z
---

# Expectation vs. Experience — Study Notes

**Authors**: Priyan Vaithilingam, Tianyi Zhang, and Elena Glassman.  
**Published**: CHI Conference on Human Factors in Computing Systems Extended Abstracts, April 29–May 5, 2022; **7 pages**.  
**Status**: Peer-reviewed CHI EA study report, not a full CHI proceedings paper. Read the complete supplied **seven-page author manuscript**, including references and the color-highlighted completion-time table. Its findings concern an early Copilot interface, not current coding assistants.

## What It Is

A within-subjects comparison of AI-generated code with conventional token completion. It separates **preference and perceived helpfulness** from **task completion and repair work**: users can value an assistant's starting point while struggling to understand and correct what it produces.

## Problem and Motivation

Model benchmarks do not establish usability in a human workflow. Almost-correct generated code creates a new task: recognizing whether it fits the requirement, then understanding enough to repair it. A long suggestion may reduce typing while increasing reading, context switching, debugging, and commitment to an unsuitable approach.

The authors investigate programming experience, error recognition, coping strategies, and obstacles to adoption. Their core design model is to support **understanding and validation**, not merely maximize code volume or one-shot task completion.

## Study Design

**24 participants** were recruited through mailing lists at two research universities: **10 undergraduates, 5 master's students, 8 PhD students, and 1 software engineer**; **4 women, 19 men, and 1 nonbinary participant**. Programming experience was **under 2 years for 1**, **2–5 years for 14**, and **over 5 years for 9**. Compensation was a **$20 gift card**.

Each person completed **two different Python tasks**, one with Copilot and one with IntelliSense in a development environment. Assignment of tasks and tools was counterbalanced through random assignment; each of the **three tasks × two conditions** had **8 sessions**, **48 sessions total**. Participants could search online and use other online resources in both conditions. The comparison is therefore generated multi-line assistance versus conventional completion plus available search, not assistance versus no tools.

The three tasks were deleting the first and last columns of a CSV (**easy**), extracting hyperlinks from a web page (**medium**), and creating a specified scatter plot with date formatting, dimensions, labels, and file output (**hard**). The nominal limit was **20 minutes**, with noncompletion counted as failure. A short tool tutorial preceded each task; audio and screens were recorded. Post-task and final surveys captured experience and preference. The first author open-coded responses, then refined themes with coauthors; no inter-rater reliability estimate is reported.

Measures were task completion time, task failure, comparative preference/helpfulness, seven-point helpfulness ratings, confidence, and qualitative accounts of comprehension, control, error handling, and adoption concerns. The paper reports t-test p-values but no confidence intervals, standardized effect sizes, or fully specified paired statistical model.

## Results / Admissions

### Preference did not establish productivity

**19/24 preferred Copilot**, **23/24 called it more helpful**, and mean helpfulness was **6.16 versus 4.45 on a seven-point scale**, a **1.71-point difference**, **t-test p < .001**. Only **10/24** reported greater confidence in its code than in conventional suggestions. Helpfulness, confidence, and preference were not identical judgments.

| Task | Completed with IntelliSense | Completed with Copilot | Reported mean time: IntelliSense / Copilot |
|---|---|---|---|
| Easy CSV editing | 8/8 | 8/8 | 7:01 / 6:11 |
| Medium hyperlink extraction | 8/8 | 6/8 | 11:44 / 11:56 |
| Hard plotting | 6/8 | 5/8 | 13:36 / 11:06 |
| Overall | 22/24 | 19/24 | 10:23 / 9:18 |

Failures were **2/24 versus 5/24**, an observed **12.5-percentage-point increase** with Copilot, reported **not statistically significant**, without a test statistic or exact p-value. Mean completion time differed by **1 minute 5 seconds** in the reported overall averages, **p = .53**. The means exclude DNF sessions and cannot by themselves summarize all sessions' effort or prove equivalent performance. The null results are absence of a detected gain, not proof of no benefit or no harm.

Reviewing recordings, the authors attributed **3 of the 5 Copilot failures** to incorrect generated code that led to protracted debugging. The remaining two reflected unfamiliarity with relevant libraries and debugging tools; the two control failures reflected plotting-library unfamiliarity. These are analyst-attributed case explanations, not randomized manipulations of code errors.

### A starting point helps, but comprehension can dominate repair

Four participants received almost the entire task solution with little or no fixing; seven explicitly said the assistant could save time. Participants valued getting beyond a blank canvas and avoiding online searches. These accounts explain preference without replacing the measured completion outcomes.

At the same time, **12/24** reported difficulty understanding and changing generated code, **5/24** perceived loss of control, and **7/24** expressed reliability concerns. The text describes eight participants limiting trust to simple tasks, though its sentence mistakenly says they trusted “participants” rather than the assistant.

**12 participants attempted repair** of erroneous suggestions; **5 of those 12** were willing only if the code was easy to read and understand. **7 participants** said they would discard and rewrite incorrect generated code without attempting repair. These are reported strategies and preferences, not mutually exclusive allocation groups or experimentally compared repair methods.

The authors observed **eight instances of overreliance**, including accepting code without understanding it and postponing validation. The count is **instances, not eight uniquely identified participants**, and no rate per suggestion or independent accuracy-based calibration measure is supplied.

### Error recognition is not sufficient recovery

In one hyperlink-extraction case, a participant accepted a regular-expression approach and remained committed to repairing it instead of considering structured HTML parsing. The participant recognized errors but underestimated repair effort and failed within the session limit. This illustrates **anchoring to an approach and costly recovery after recognition**, not merely an undetected error.

Generated blocks also forced switching between writing, reading, and debugging. The paper interprets this as cognitive overload but does not report a standardized workload measure or experimental comparison of suggestion lengths. Prompt sensitivity and ambiguity made participants' expectations harder to communicate reliably.

### Recommendations remain untested

The authors propose easier comprehension through explanations, signals of uncertainty, support for tests and corner-case checking, comparison with alternative solutions and external discussion, and task decomposition. Three successful hard-task participants decomposed the task into smaller requests; that observation does not establish a causal advantage. None of these proposed interface changes was evaluated in the study.

## Analyst Takeaways

1. **Evaluate preference and outcomes separately.** A useful starting point may produce high ratings even when completion time and success do not significantly improve.
2. **Make review and repair feasible, not merely available.** Recognizing that a suggestion is wrong is not the same as understanding why or being able to recover efficiently.
3. **Preserve alternatives and independent evidence.** A plausible generated solution can narrow the search too early; comparison may help, but this paper does not prove that showing more options improves decisions.
4. **Separate acceptance from verification.** Deferred understanding creates later work; these short-session observations do not quantify long-term security or maintenance risks.
5. **Treat decomposition as a hypothesis for design.** The successful cases motivate support for smaller inspectable units without establishing an optimal granularity.

## Questions and Limitations

- Small, largely student sample, three short Python tasks, early assistant version, and introductory exposure limit generalization to professional longitudinal work or current models. No independent replication is established in this paper.
- The within-subjects design used different tasks per participant; difficulty and familiarity matter. No per-participant paired data, confidence intervals, or standardized effect sizes are supplied. Success-only timing risks hiding the cost of noncompletion.
- **Timing inconsistency**: despite the nominal **20-minute failure rule**, Table 1 includes successful times **20:12** with Copilot and **22:42/23:13** with IntelliSense. The caption says stopping occurred after “approximately” 20 minutes, but these entries leave enforcement unclear; do not reclassify them without evidence.
- The discussion says whole-block generation improves productivity “significantly” despite nonsignificant time/success results; this is a qualitative assertion, not a supported statistical conclusion. Its characterization of internet code as generally bug-free also exceeds what was tested.
- Comprehension, workload, reliability, and overreliance themes mostly come from coding and observations rather than direct calibrated correctness measures. Counts of themes may overlap.
- **Redistribution evidence**: the PDF grants personal/classroom copying but says **“To copy otherwise, or republish, to post on servers or to redistribute to lists, requires prior specific permission and/or a fee.”** It states copyright held by owner/authors and publication rights licensed to ACM; no explicit public redistribution grant appears. Keep this manuscript private and cite its DOI.

## Vault Ideas Extracted

- [Appropriate Reliance on Automation](/vault/appropriate-reliance-on-automation.md) — Adds a programming comparison where preference and helpfulness exceed the control without detected time/success gains and where deferred validation is observed rather than scored as calibrated reliance.
- [Software Agent Oversight](/vault/software-agent-oversight.md) — Adds comprehension and repair burdens, including three error-related failures, as limits on treating acceptance or error recognition as effective supervision.
- [Error Prevention and Recovery](/vault/error-prevention-and-recovery.md) — Adds a recognized-error case where commitment to an unsuitable generated approach makes repair costly, while separating proposed recovery support from tested interventions.
