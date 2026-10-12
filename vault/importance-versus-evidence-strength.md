---
type: Synthesis
title: Importance versus Evidence Strength
description: A design recommendation's implementation priority and the strength of its supporting evidence are separate judgments, with obligations supplying an independent constraint.
tags: [design-process, usability-evaluation, decision-making, digital-interfaces]
timestamp: 2026-10-11T23:59:36Z
---

# Importance versus Evidence Strength

An important design question is not necessarily well researched, and a
well-supported finding is not necessarily the highest implementation priority.
Keep **importance**, **confidence in evidence**, and **overriding obligations**
separate instead of collapsing them into one quality score.

## The Decision Model

Importance asks how much an issue matters to the intended outcome. Evidence
strength asks what justifies the recommendation: cumulative research, a limited
or conflicting study base, or professional opinion. A rating of either kind is
not a measured effect size.

The useful combinations inform different decisions:

- **High importance, strong evidence:** prioritize application while checking
  whether the studied users, task, and outcome match the current context.
- **High importance, weak evidence:** prioritize contextual evaluation rather
  than presenting the recommendation as proven or dismissing the issue.
- **Lower importance, strong evidence:** retain confidence in the finding without
  assuming it outranks more consequential work.
- **Binding obligation:** meet the requirement independently of its experimental
  evidence rating. A lack of causal usability trials does not nullify a legal
  duty or the rationale for equivalent access.

## The Evidence

A **2006 collection of 209 web-design guidelines** explicitly assigned separate
five-level importance and evidence ratings. In the revision, **36 web
professionals** rated importance and **13 usability professionals** rated research
support for new or revised guidance. These are panel judgments about selected
recommendations, not trials validating all 209 designs.

Its evidence scale distinguished:

- **5:** cumulative, compelling research, at least one rigorous contextually
  valid study, no known conflicting findings, and agreeing expert opinion.
- **4:** cumulative research with building professional consensus, potentially
  including conflicting findings.
- **3:** limited or conflicting research and/or mixed expert agreement.
- **2:** strong expert-opinion support without research-based evidence under
  the scale.
- **1:** limited or conflicting expert opinion without research-based evidence.

The importance categories are relative rankings among recommendations that
survived selection. A displayed **1** does not mean unimportant, and the source
does not publish a distinct verbal definition or conversion threshold for every
importance level.

The separation has a concrete consequence: among **25 highest-importance
recommendations**, only **one** also received the strongest evidence rating;
**13 of 25** had weak research or expert-opinion support. Accessibility
requirements could have high importance and expert-opinion evidence ratings
while remaining obligatory. The source recommends local testing for important,
poorly supported questions; it does not experimentally demonstrate the benefit
of this prioritization model.

## Practical Use

- Record the user outcome, priority rationale, supporting evidence, and relevant
  obligations separately when choosing design work.
- Treat research gaps on consequential issues as candidates for evaluation.
  Specify whether the outcome is comprehension, completion, speed, accuracy,
  preference, or trust; these are not interchangeable.
- Read a recommendation's qualifications and context, not just its imperative
  heading. Strong evidence for a speed benefit does not resolve an accuracy
  tradeoff.
- Preserve disagreement in expert assessments rather than upgrading consensus
  into causal proof; the
  [Evaluator Effect](/vault/evaluator-effect.md) explains why evaluator judgment
  remains part of the measurement process.

## Limitations

The example scale is a historical narrative synthesis, not a reproducible
systematic review or a universal evidence-grading standard. Its original scope
was largely English-language information sites for adults **18–75**. Unchanged
guidelines were not necessarily reappraised in the revision, and strong support
meant no conflicting findings known to the reviewers at that time.

A reported **Cronbach's alpha of .92** for evidence ratings is a reliability
statistic, not proof of inter-rater agreement or improved user outcomes. Study
quality, publication bias, transfer to new contexts, and editorial inconsistencies
remain possible. Expert-opinion support is not proof of ineffectiveness, while a
long bibliography is not a count of independent replications. Guidelines also
remain distinct from current standards and legal requirements.

## Sources

- [Research-Based Web Design & Usability Guidelines](/dossiers/research-based-web-design-usability-guidelines.md) — Supplies the two rating scales, review-panel sizes, 209-guideline evidence map, recommendation to test high-importance low-evidence issues, and independent boundary of accessibility obligations.
