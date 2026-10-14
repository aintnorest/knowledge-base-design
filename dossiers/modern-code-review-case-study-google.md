---
type: Study Note
title: "Modern Code Review: A Case Study at Google"
description: Google's interviews, survey, and nine-million-change logs describe fast small-change review serving readability and education, without establishing that its one-reviewer practice optimizes defect detection.
resource: https://doi.org/10.1145/3183519.3183525
source: https://doi.org/10.1145/3183519.3183525
tags: [design-process, user-research, digital-interfaces, case-study]
timestamp: 2026-10-14T21:31:18Z
---

# Modern Code Review at Google — Study Notes

**Authors**: Caitlin Sadowski, Emma Söderberg, Luke Church, Michal Sipko, and Alberto Bacchelli.  
**Published**: ICSE-SEIP 2018, May 27–June 3, Gothenburg; DOI 10.1145/3183519.3183525.  
**Status**: Peer-reviewed exploratory industrial case study. Read the complete supplied 10-page publication-layout PDF, including all figures, tables, and references; page 5 required visual reading because it was absent from the text extraction.  

## What It Is

A mixed-method account of a mature, mandatory, asynchronous code-review process. Its contribution is to show how review can become a lightweight **readability, education, and governance practice**, rather than a universal prescription for the optimum number of reviewers or a causal demonstration of defect prevention.

## Study Design

- **12 approximately hour-long interviews** with software and site-reliability engineers, including leads, managers, and individual contributors, selected through snowball sampling for variation across teams and roles. Tenure ranged from one month to ten years, median five years. Recent changes and think-aloud reviewing grounded discussion; multiple researchers developed and checked the coding scheme. Themes describe diversity, not population frequencies.
- Logs cover **approximately nine million committed changes**, involving over **25,000 authors/reviewers**, from **January 2014–July 2016**, and approximately **13 million comments** from **September 2014–July 2016**. The analysis excludes uncommitted changes, changes without an approver, zero-source-line deltas, and heuristically identified automation. A reviewer means an **approver**, not everyone who reads or comments.
- A questionnaire about a recently reviewed change reached **44 of 98 engineers (45%)**. It asked three rating questions, perceived effects, and open feedback, limiting recall distance but not self-selection.
- Interaction-log estimates of review time use a separate **five-week period starting October 2016**. Sessions group interactions with one uncommitted change, by a nonauthor, with gaps no longer than ten minutes; users needed data for all five weeks.
- Measures are change size, response/approval latency, approver/comment counts, session-time estimates, satisfaction, and thematic expectations/breakdowns. There is no randomized intervention, defect-detection benchmark, or causal effect size.

## Model and Mechanisms

### Review has more than one purpose

An early employee attributes the introduction of review primarily to making production code understandable to future developers and retaining knowledge across people. Interviews identify **education, maintaining norms, gatekeeping, and accident prevention**; history inspection also supports later auditing. Each of the four themes was selected by **8–11 survey respondents** for their particular change; these overlapping counts are not a ranking of universal motivations.

Figure 1 maps purpose to relationship: education and norms appear around leads and newcomers, norms around readability reviewers, gatekeeping across teams, and accident prevention among teammates. This is a qualitative relationship model, not measured causal moderation.

Google separates authorization over code areas from demonstrated familiarity with language conventions. Human approval operates alongside automated checking. The durable pattern is **explicit responsibility plus contextual competence**, not reproducing a particular permission system.

### Small units support a lightweight feedback loop

- **Over 35%** of changes modify one file; approximately **90%** modify fewer than ten.
- **Over 10%** modify one line; median size is **24 changed lines**.
- **Over 80%** involve at most one iteration of resolving comments, where an iteration is inferred from an author sending resolutions; zero iterations permits immediate submission.
- Median initial feedback is **under one hour for small changes**, approximately **five hours for very large changes**; overall median entire-review latency is **under four hours**.
- Median approver count is **one**; fewer than **25%** have more than one, and over **99%** have at most five. Approximately **30%** have more than one commenter, so approver and commenter populations differ.
- During the workweek **70%** are committed within **24 hours** of initial review dispatch. Median developer activity is approximately **three authored and four reviewed changes per week**.

These describe a jointly evolved workflow and culture. More approvers correlate with more comments, and comment count peaks around **12.5 per change at 1,250 changed lines**. Neither comment volume nor one approver establishes the number of defects caught; the authors' contrast with a prior two-reviewer recommendation does not experimentally refute or replace it.

## Results / Admissions

### Perceived value is not demonstrated bug detection

All **44** respondents agreed review was valuable overall (**14 agree, 30 strongly agree**). For the specific change, ratings from strongly disagree through strongly agree were **2 / 4 / 14 / 11 / 13**: general endorsement does not imply every review was worthwhile. **Eight** described comments as unhelpful; three elaborated that these were small configuration changes. Only **two** said comments found a bug.

Feedback quantity ratings were **2 / 2 / 34 / 5 / 0**, centered on an appropriate amount. The paper also cites **97% tool satisfaction** from internal surveys without supplying their sample or sampling detail here. Estimated reviewing time was **mean 3.2, median 2.6 hours/week**. Comparison with another study's 6.4 self-reported hours is not a controlled efficiency comparison.

### Breakdowns persist despite maturity

Interviews identify geographic/organizational distance, tone and power, disagreements over whether design belongs in code review, missing rationale or urgency, and mismatches between team policy and tool flexibility. Withholding approval can exercise social power; approval is not solely a technical evaluation event. Declaring whether review concerns an urgent repair, optional improvement, or open design question can align expectations, but no intervention test quantifies that benefit.

### Education is supported indirectly

Figure 2 shows comments on an author's changes declining with **author tenure**; newcomers within the first year typically receive more than twice as many comments per change. Figure 3 shows distinct files edited/reviewed increasing across three-month tenure buckets, with the union exceeding files edited alone. These are exposure and commenting proxies, not tests of retained knowledge or code comprehension. The proposed explanation that reviewers need fewer questions is not directly established by the author-tenure plot.

## Analyst Takeaways

1. **State the job of review.** Readability, learning, ownership, design discussion, and defect prevention require different evidence; do not assess all of them with comment count or approval speed.
2. **Make changes bounded and interpretable.** The observed workflow combines small changes, established ownership, automated checks, and quick response expectations; transplanting one-reviewer approval alone removes its context.
3. **Treat review as coordination as well as inspection.** Urgency, scope, decision authority, and interpersonal conduct shape whether discussion advances the work.
4. **Agent-change review remains an extrapolation.** These logs concern ordinary engineering review, not proof that a quick human approval reliably detects generated-code faults.

## Questions and Limitations

- One organization, mature monorepository workflow, nonrandom interview participation, and a small change-specific survey constrain transfer. Specialist security reviewers and research scientists were not interviewed.
- Committed/approved-change filtering cannot describe rejected or abandoned proposals; approvers are not all actual readers. Session boundaries approximate effort and omit some offline reasoning.
- No independent replication of the entire workflow's effectiveness is established. Comparisons with prior projects reproduce descriptive measures, not randomized reviewer-count or change-size effects.
- **Internal inconsistencies**: Table 2's feedback-quantity row totals **43**, versus **44** valid survey responses, without explanation. The abstract summarizes logs as “over two years,” whereas the method's change window is January 2014–July 2016 (approximately 2.5 years); comments use a different window. The education discussion invokes reviewer learning to interpret a plot explicitly indexed by **author** tenure.
- **Redistribution evidence**: the PDF grants personal/classroom copying subject to conditions and says **“For all other uses, contact the owner/author(s).”** Author-held copyright is not a public redistribution grant; archive privately.

## Vault Ideas Extracted

- [Change Review Effectiveness](/vault/change-review-effectiveness.md) — Adds a nine-million-change industrial description of small, fast, usually single-approver reviews and separates review purpose, perceived value, comment volume, and demonstrated error detection.
