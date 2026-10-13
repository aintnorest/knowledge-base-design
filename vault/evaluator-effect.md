---
type: Synthesis
title: Evaluator Effect
description: Independent evaluators using the same usability method often identify different problems, so agreement, discovery coverage, and real-world validity must be assessed separately.
tags: [usability-evaluation, ux-metrics, user-research, digital-interfaces]
timestamp: 2026-10-12T20:43:27Z
---

# Evaluator Effect

The evaluator effect is variation in the problems different people report when
assessing the same interface with the same usability method. It occurs in
inspection and in interpretation of user-test observations: watching concrete
behavior does not remove the observer's judgment.

## How It Works

Evaluators can differ in task coverage, interpretation of procedures, and the
threshold for calling something a problem. Experience can increase the number
of findings without making independent experts converge on the same list.
Matching differently worded findings also requires judgment; merging broadly
can increase apparent agreement, while distinguishing instances can reduce it.

Keep three questions separate:

- **Reliability:** do independent evaluations produce similar findings?
- **Discovery coverage:** how much of the problem inventory did each evaluation
  uncover? The union of all findings is not necessarily exhaustive.
- **Validity:** do reported problems correspond to difficulties in actual use?
  Agreement alone cannot establish this.

**Any-two agreement** averages the intersection divided by the union of each
pair's problem lists: their Jaccard overlap. It ranges from 0% to 100% and is not
chance-corrected. **Individual detection rate** instead divides each evaluator's
findings by the whole group's union. Its minimum is 1/n for n evaluators, and
adding evaluators can lower the rate simply by enlarging that denominator.
Neither statistic makes the collective list ground truth.

This affects both [heuristic evaluation](/vault/heuristic-evaluation.md), where
principles guide broad inspection, and
[cognitive walkthrough](/vault/cognitive-walkthrough.md), where task-bound
learning questions still require interpretation.

## The Evidence

A review of **11 studies comprising 18 experiments** found average any-two
agreement ranging from **5% to 65%** where pairwise data were available. The
studies covered cognitive walkthrough, heuristic evaluation, and thinking-aloud
tests; they are heterogeneous descriptive evidence, not a pooled effect size.

The clearest isolation of observer interpretation involved **four researchers
analyzing the same four users' videos**, with nine predefined problem criteria.
Together they identified **93 problems**, compared with about **48** for one
observer watching all four users. **46%** of problems were reported by only one
evaluator and **20%** by only two. Pairwise agreement was **42%**. A later
fixed-footage study with **35 evaluators and five videos** also found differing
issue sets, corroborating the phenomenon rather than every original estimate.

Serious problems are not exempt: of **14 experiments** assessing severity, only
four showed appreciably better individual detection of severe problems. Severity
ratings themselves also diverged. Separate web-design guidance reports both
inspection false positives and misses, reinforcing that discovery volume is not
the same as validity; its cited case estimates are not universal error rates.

The original heuristic experiments illustrate why aggregation helps:
**148 distinct evaluators** performed **182 evaluator–interface evaluations**
across **four experiments**. Mean individual coverage of the final known-problem
inventories was **51%, 38%, 26%, and 20%**; simulated unions of **five independent
evaluators** reached **90%, 70%, 63%, and 55%**. Low-total evaluators sometimes
found problems missed by high-total evaluators, so findings were not perfectly
nested. For the same **34 students** evaluating two systems, individual
performance was related at **R² = .33, p < .01**, not a stable universal ranking.

These are the **same Nielsen–Molich studies reanalyzed by the review**, not
independent replication. Their aggregate curves simulate unions, not observed
team collaboration; inventories were expanded after reports, and neither
exhaustive coverage nor validity in actual use was established.

## Practical Use

- For consequential evaluations, obtain an additional **independent** analysis,
  not merely more user sessions interpreted by the same person.
- Agree on target users, task coverage, and problem criteria before evaluation.
  Preserve the observations and rationale behind findings during merging.
- Investigate unique findings rather than discarding them for lack of consensus.
  A unique report may be a missed serious barrier or a false alarm.
- Explain severity in terms of user consequences and prioritization criteria;
  a merged inventory does not create shared severity judgments. Keep priority
  distinct from confidence, as in
  [Importance versus Evidence Strength](/vault/importance-versus-evidence-strength.md).
- Treat both human reports and
  [automated accessibility checks](/vault/automated-accessibility-testing-limits.md)
  as partial coverage of the problem space, not interchangeable certificates.

## Limitations

Low overlap can reflect different scope or reporting granularity rather than
incompetence. High overlap can reflect shared blind spots. The reviewed studies
do not separate differences between people from the same person's inconsistency
on repeated evaluation, and several samples are small or novice-heavy.

The authors recommend multiple evaluators and clearer specifications, but their
review does not establish the reliability of collaborative teams' final outputs.
A proposed staffing relationship based on only four users and four evaluators
cannot justify a universal users-to-evaluators ratio. More formal criteria can
also increase fatigue or exclude meaningful harms: maximizing agreement is not
the purpose of evaluation.

## Sources

- [The Evaluator Effect: A Chilling Fact about Usability Evaluation Methods](/dossiers/evaluator-effect-usability-evaluation-methods.md) — Defines the agreement measures, reviews 11 studies, isolates fixed-footage observer variation, and distinguishes reliability from validity and exhaustive coverage.
- [Research-Based Web Design & Usability Guidelines](/dossiers/research-based-web-design-usability-guidelines.md) — Carries the evaluator-effect finding into evaluation guidance and reports contextual inspection false-positive, missed-problem, and severity-estimation evidence.
- [Heuristic evaluation of user interfaces](/dossiers/heuristic-evaluation-of-user-interfaces.md) — Provides the four original experiments reanalyzed in the review, showing complementary independent findings, system-dependent detection, and simulated rather than observed-team aggregation.
