---
type: Study Note
title: "Reading Between the Lines: Modeling User Behavior and Costs in AI-Assisted Programming"
description: A 21-programmer observational study finds substantial verification and prompting work hidden by code-suggestion acceptance telemetry, but lacks an unassisted baseline to establish net productivity costs.
resource: https://doi.org/10.1145/3613904.3641936
source: https://doi.org/10.1145/3613904.3641936
tags: [delegation, ux-metrics, user-research, cognitive-load, digital-interfaces, taxonomy]
timestamp: 2026-10-14T21:30:36Z
---

# Reading Between the Lines — Study Notes

**Authors**: Hussein Mozannar, Gagan Bansal, Adam Fourney, and Eric Horvitz.  
**Published**: Proceedings of the CHI Conference on Human Factors in Computing Systems, May 2024; version-of-record DOI above.  
**Status**: Peer-reviewed CHI paper; read the complete supplied **41-page arXiv:2210.14306v5 manuscript, dated April 22, 2024**, including figures, tables, references, and image-only task and survey appendices. The studied interface is **Copilot as of August 2022**, not the 2024 or current product.

## What It Is

A taxonomy and observational study of what programmers do around AI code suggestions. **CodeRec User Programming States (CUPS)** distinguishes writing, prompting, waiting, verification, editing, and deferred thought. The durable contribution is a measurement model: **acceptance is an interaction event, not proof that someone has understood or validated the code**.

## Problem and Motivation

Acceptance rate, characters saved, and time from display to acceptance omit work outside the suggestion popup. A programmer may accept code to obtain syntax highlighting or accumulate a complete implementation before reviewing it. Prompt refinement happens before display; verification and repair can happen afterward. Counting only the decision event makes these costs disappear without eliminating them.

The paper uses elapsed time as one dimension of interaction cost, explicitly not a complete measure of productivity, mental effort, code quality, or value. Time attributed to assistance is not automatically wasted time: it may replace slower unaided work.

## Study Design

### Participants and task setting

**21 developers** were recruited through developer mailing lists within the authors' large organization: software engineers, researchers, and graduate student interns. Professional programming experience was reported as **6 with under 2 years, 5 with 3–5 years, 7 with 6–10 years, and 3 with more than 11 years**. **7** used Copilot more than a few times weekly, **3** monthly or less, and **11** had never used it. **19** programmed in Python, one in C++, and one in JavaScript.

Each participant received one randomly selected task, with reassignment if unfamiliar, from eight categories: algorithm problems; data manipulation; data analysis and plotting; machine-learning training/evaluation; classes and boilerplate; tests for a black-box bracket validator; edits to a nearest-neighbor retriever; and custom regularized logistic regression. Tasks were designed for approximately **20 minutes**. Instructions were images to discourage copying the problem statement directly into a prompt. Sessions used a remote development environment and lasted approximately **60 minutes**, including labeling and a questionnaire; compensation was **$50**.

Mean coding duration was **12.23 minutes, SD 3.98**, maximum **20.80 minutes**, measured from the first task code to session end. There was **no no-Copilot control**, no randomized interface comparison, and no longitudinal deployment.

### Capturing activity rather than inferring intent from clicks

Immediately after coding, participants watched their session video and labeled intervals between suggestion display, acceptance, rejection, and browsing events. The taxonomy came from author experience and pilots with **three additional organizational participants**. Its **12 activity states** distinguish thinking/verifying; deferring thought; thinking about new code; waiting; writing new functionality; editing accepted suggestions; editing personally written code; prompt crafting; documentation writing; debugging/testing; external documentation lookup; and not thinking/away.

One label represented each telemetry interval. If typing occurred, the hierarchy favored the typing activity; otherwise participants chose the dominant activity when multiple states applied. This gives access to recalled intent, but can undercount thinking embedded inside typing intervals.

Participants supplied **3,137 CUPS labels plus 353 IDK labels = 3,490 intervals**. IDK occupied **6.5% of session time** and was excluded, often because video was unclear or intervals too short. Only three custom-state entries were needed, all mapped to existing categories. This supports coverage in these tasks, not universal completeness or inter-rater reliability.

## Results / Admissions

### The visible suggestion is only part of the work

Mean participant-normalized session shares were **22.4% thinking/verifying suggestions (SD 12.97)**, **14.05% writing new functionality (SD 8.36)**, **11.90% editing the last suggestion**, **11.56% prompt crafting**, **11.31% debugging/testing**, **10.91% thinking about new code**, **7.45% external documentation lookup**, **4.28% editing personally written code**, **4.20% waiting (SD 4.46)**, **1.39% deferred thought**, **0.53% documentation writing**, and **0.01% not thinking**. Verification was the largest state for **6/21** participants and among the top three for **14/21**.

The five assistance-specific states—verification, deferred thought, waiting, prompting, and suggestion editing—occupied **51.5% of average session time, SD 19.3**. Verification plus suggestion editing accounted for **34.3%**. These are observed allocations, **not causal productivity losses** or evidence that half the time would be saved by removing assistance.

State transitions showed recurring work cycles: prompt crafting → verification **.54**; deferring thought → verification approximately **.54**; writing new functionality → verification **.59**; prompt crafting → waiting **.25**. The main transition diagram hides self-transitions and probabilities below **.17** for readability; the appendix includes edges above **.05**. These diagrams describe the collected sequence, not experimentally established cognitive mechanisms.

### Acceptance can precede verification

There were **61 deferred-thought intervals**. Accepted suggestions were subsequently edited with probability **.53 after deferral versus .18 after prior verification** (**χ² = 29.2**, reported **p = 0**, a rounded value rather than literal zero). Suggestion length did not distinguish these groups: mean characters **75.81 versus 69.06**, **t = −.58, p = .56**; line count also did not significantly differ.

After deferral, **53.2%** of suggestions were verified immediately afterward. Counting this later verification raised mean attributed verification time **3.25 → 15.21 seconds** (SD **3.33 → 20.68**), median **1.99 → 6.48 seconds**, **paired t = −4.88, p = 1.33 × 10⁻⁵**. Even suggestions verified before acceptance had later verification **19%** of the time; attributed mean time rose **3.96 → 7.03 seconds** (SD **8.63 → 14.43**), **t = −4.17, p = 5 × 10⁻⁵**. The paper states p-values receive Benjamini–Hochberg correction at **α = .05**.

Adding explicit waiting to the broader display-to-action measure raised the average only **6.11 → 6.51 seconds**, while waiting episodes themselves added about **2.5 seconds**. A small mean latency penalty can conceal meaningful costs for particular moments.

### Prompting and subjective benefit

Of **234 suggestions shown during prompt crafting**, only **10.7%** were accepted. Yet **81.3% of 59 prompt-crafting attempts** ended with a suggestion accepted before returning to non-assistance-centered work. A low immediate acceptance rate can therefore coexist with successful iterative elicitation; it is not a standalone measure of useless assistance.

In the post-study survey, **17/21** agreed they completed the task faster and **16/21** felt more productive. **14/21** agreed assistance helped them stay in flow and spend less time searching; **6/21** expressed code-quality concerns. These are perceptions without an observed counterfactual, not measured speed improvements.

### Design proposals, not tested interventions

The authors recommend grouping successive suggestions when review is deferred, prioritizing responsiveness during actual waiting, avoiding interruptions during prompt composition, and assessing accepted code that survives later review rather than raw acceptance alone. State-aware assistance and retention-based metrics were **not validated as improving outcomes** in this study.

## Analyst Takeaways

1. **Measure the whole oversight episode.** Include preparation, acceptance, subsequent understanding, testing, and repair; shifting review after acceptance is not removing review.
2. **Do not label all rapid acceptance overreliance.** Some acceptance deliberately creates a better review surface or a complete unit; distinguish temporary incorporation from final endorsement and assess whether verification actually occurs.
3. **Keep cost attribution separate from net value.** Time spent verifying assistance can be worthwhile; a control condition and quality outcomes are needed to determine the tradeoff.
4. **Coordinate assistance with current work.** Prompt writing, coding, waiting, and reviewing have different interruption needs. This paper motivates that distinction without proving a particular adaptive design.

## Questions and Limitations

- Small organizational convenience sample, short selected tasks, predominantly Python, and substantial first-time use constrain generalization. No independent replication, security outcome, long-term maintenance measure, or causal test of the interface recommendations is established here.
- Retrospective self-labeling captures intent but is vulnerable to recall and inconsistent category interpretation. Intervals are not independent participants; suggestion-level tests do not establish population-level causal effects.
- **Internal count discrepancy**: the introduction reports **1,096 suggestions**, whereas the participant/results section reports **1,024 shown**. The manuscript does not reconcile these denominators; preserve both rather than select a hidden exclusion rule.
- **Acceptance definitions differ**: Table 3 reports **.80 ± .02** acceptance while verifying a shown suggestion and **.56 ± .04** when verification preceded display; the surrounding prose's **.70** corresponds instead to Appendix Table 4's acceptance **within the next two events**. Its approximately **.20** for thinking about new code likewise differs from Table 3's **.12/.27** and approximates Table 4's **.21**. These are different windows, not interchangeable estimates; the prose also calls the main acceptance table Table 4 although it is Table 3.
- The manuscript calls acceptance variability **11.9% standard error**, without enough explanation to reconcile it with the participant summaries. It mentions predictive models and a task breakdown in the appendix, but the supplied appendix contains neither a predictive-model evaluation nor that breakdown. Do not infer their performance.
- The task appendix includes imperfections: the graph-class instruction repeats the node-class name, and the machine-learning task asks for hyperparameter selection on the test set. The study is about interaction, not validation of these task instructions as best practice.
- **Redistribution evidence**: this arXiv v5 PDF contains **no explicit Creative Commons, public-domain, or equivalent redistribution grant**. A reported CC licence for the published ACM version does not establish permission for this supplied manuscript; archive this copy privately and cite the version-of-record DOI.

## Vault Ideas Extracted

- [Software Agent Oversight](/vault/software-agent-oversight.md) — Adds direct programming observations that acceptance can precede understanding and substantial post-acceptance verification, without establishing autonomous-agent or security outcomes.
- [Appropriate Reliance on Automation](/vault/appropriate-reliance-on-automation.md) — Distinguishes temporary acceptance, recalled verification, subsequent editing, and subjective productivity from calibrated correctness or net benefit.
- [Interruption Coordination](/vault/interruption-coordination.md) — Adds low suggestion acceptance during prompt composition and state-dependent waiting as reasons to coordinate assistance timing, while keeping adaptive designs untested.
