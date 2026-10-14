---
type: Synthesis
title: Change Review Effectiveness
description: Effective review reconstructs a proposed change's intent and consequences, matches scope and reviewer knowledge to the review purpose, and distinguishes approval or passing tests from demonstrated verification.
tags: [design-process, cognitive-load, delegation, usability-evaluation, digital-interfaces]
timestamp: 2026-10-14T21:39:12Z
---

# Change Review Effectiveness

Reviewing a proposed change means judging whether it serves its purpose without
unacceptable consequences. Seeing what differs is not the same as understanding
why it differs or what the difference affects. Effective review therefore needs
**intent, surrounding context, and evidence appropriate to the judgment**—not
merely an approval control or an attractive presentation.

The evidence here comes from software development. Applying the principles to
design or content changes is an **extrapolation**, not a measured cross-domain
review effect.

## Understanding Is the Core Work

A field study combining observation of **17 practitioners**, surveys of **873
programmers and 165 managers**, and discussion coding identified understanding
as a central review bottleneck. **91%** of programmer respondents said unfamiliar
files take longer to review; **82%** reported different, generally deeper feedback
from familiar reviewers. These are reports, not randomized measures of speed or
error detection. Reviewers often needed substantially more surrounding material
than the changed lines alone.

A useful account explains **what changed, why, and under which constraints**.
That account must remain checkable: a description can omit consequences or claim
a narrower change than was actually submitted. Context includes dependencies,
prior decisions, requirements, and the authority to resolve disagreement.

An observational study of comment usefulness likewise associates prior artifact
knowledge with author-valued feedback. First-time file reviewers had **32–37%**
useful-comment density, versus **65–71%** among those with prior file-review
experience. Relevant familiarity is not interchangeable with organizational
seniority or being on the same team. These are comment proportions produced by a
retrospective classifier, not rates of defects found.

## Bound Scope Without Inventing a Universal Size Limit

More changed files associated with lower useful-comment density, with substantial
fluctuation and no validated cutoff. A separate industrial account of roughly
**nine million committed changes** described a median of **24 changed lines**,
usually **one approver**, and median total review latency **under four hours**.
These describe an established workflow combining ownership, automated checks,
small changes, and review norms; they do not establish an optimum line count,
reviewer count, or causal benefit from speed.

The useful unit is a coherent, explainable change, not simply a short one. Small
configuration changes can have wide effects. Splitting a proposal helps only if
each part remains intelligible and its integration consequences can still be
judged. Recommendations to use incremental changes and add context for systemic
changes follow the field evidence but were not tested as intervention packages.

## Match Evidence to the Purpose of Review

Review serves **defect prevention, maintainability, alternatives, learning,
shared awareness, norms, and decision ownership**. These need different success
measures. In one study, **44%** of programmers ranked defect finding first, yet
only **14% of 570 coded comments** concerned defects. That is not a 14% detection
rate: the number of available or missed defects was unknown. Learning and
coordination can also occur without a recorded comment.

Author-useful feedback is narrower than independent verification. A metric based
on nearby subsequent edits or resolved discussions captures uptake, not whether
the criticism or replacement was correct; it can discount questions that matter
for learning or checking evidence. Conversely, comment volume, satisfaction, and
approval speed do not demonstrate defect detection.

A systematic review of **54 code-reading papers** reinforces this measurement
boundary: **30** included opinion tasks and **nine** used opinion alone. Liking,
confidence, reading time, and visual attention do not establish comprehension.
Tracing an example, explaining purpose, finding a flaw, and evaluating a proposed
change exercise different capabilities. The review supplies a measurement
framework, not proof that any particular presentation improves reviewing.

## Passing Tests Is Not Security Review

Tests answer the questions their cases and assertions cover. Successful ordinary
behavior can coexist with missing authentication, filesystem-containment errors,
or unsafe memory assumptions. In one audited example, a function passed basic
tests while retaining **three weaknesses, two severe**. Acceptance and subsequent
editing also sometimes retained generated defects.

The security studies do not establish a uniform assistance penalty. A
**47-person** multi-task experiment found task-specific security harms, but its
adjusted aggregate treatment had **p = .056**, not conventional significance.
A different **58-student** connected-project study found lower average
participant-level weaknesses per line with assistance while some function-level
outcomes were worse; its severe-density non-inferiority result for passing
functions had **p = .06**. Different tasks, interfaces, models, and denominators
make these complementary boundary evidence, not direct replications. Their
shared lesson for review is narrower: **functional success and security-property
verification are distinct**. Neither experiment validated a review-interface cure.

## Reviewing Generated Changes

Observation of **20 programmers** distinguished rapid matching against an
understood next step from examination and documentation when exploring an
unfamiliar solution. Familiar-looking structure, repeated alternatives, and
successful use did not guarantee semantic understanding; detached alternatives
could add contextual reconstruction work.

Interviews with **17 experienced software-agent users** similarly describe review
costs from unfamiliar authorship, output volume, and regeneration that changes
multiple areas. Participants sometimes substituted plan quality, tests, spot
checks, or deference for inspecting execution. These are reported coping
strategies, not demonstrated error-detection methods.

**Extrapolation from human review to agent-output review:** expose the actual
change alongside its intent, dependencies, and purpose-specific checks; do not
let a generated summary stand in for the artifact. Bounded delegation can make
review feasible, but the evidence does not establish an optimal task size or
show that a final human approval reliably catches agent errors. See
[Software Agent Oversight](/vault/software-agent-oversight.md) for control across
the full workflow.

## Practical Use

- State whether the review seeks correctness, safety, accessibility, clarity,
  consistency, learning, or a decision between alternatives. Evaluate that job.
- Supply rationale and surrounding context, with an independent route to inspect
  requirements and actual effects rather than relying on the author's account.
- Include relevant artifact knowledge while retaining opportunities for newcomers
  to learn; familiarity-based allocation is guidance, not a proven optimum.
- Keep changes coherent and reviewable; expose cross-part effects and distinguish
  urgent repairs from optional improvements or unresolved design questions.
- Separate automated routine checks, ordinary functional tests, and checks of
  consequential properties. For design/content review, checking comprehension
  or accessibility rather than only appearance is a cross-domain extrapolation.
- Measure missed and correctly identified problems and the quality of resulting
  changes when claiming verification gains. Keep learning, uptake, effort, and
  satisfaction as distinct outcomes.

## Limitations

Industrial review studies are observational, concentrated in mature organizations,
and often filtered to approved changes or discussion-heavy threads. They do not
supply causal size or reviewer-allocation rules. Usefulness classification has
error and a narrow author-benefit definition. The readability review excludes
high-level documentation, tools, and disability-specific presentation studies.
Generated-code observations and agent interviews do not measure review accuracy;
the security experiments are student-heavy and do not test current autonomous
systems. No cited source establishes effectiveness for general design or content
review, or a universal policy for high-consequence approval.

## Sources

- [Modern Code Review: A Case Study at Google](/dossiers/modern-code-review-case-study-google.md) — Supplies small-change workflow, review purposes, coordination breakdowns, and the distinction between perceived value and demonstrated defect detection; no optimal approver count is established.
- [Characteristics of Useful Code Reviews: An Empirical Study at Microsoft](/dossiers/characteristics-of-useful-code-reviews.md) — Associates artifact familiarity and bounded file scope with author-useful comments, bounded by retrospective uptake-based classification rather than independent correctness.
- [Expectations, Outcomes, and Challenges of Modern Code Review](/dossiers/expectations-outcomes-challenges-modern-code-review.md) — Identifies contextual understanding, rationale, familiarity, and team benefits through observations, surveys, and comment coding, not a defect-detection benchmark.
- [Evaluating Code Readability and Legibility: An Examination of Human-centric Studies](/dossiers/code-readability-legibility-human-centric-studies.md) — Supplies the 54-paper task-and-measure framework separating opinion, tracing, explanation, inspection, and contextual evaluation; no presentation winner is tested.
- [Grounded Copilot: How Programmers Interact with Code-Generating Models](/dossiers/grounded-copilot-programmer-interaction.md) — Observes pattern matching versus exploration-oriented examination, detached-alternative costs, and generated-code debugging difficulties without testing review interventions.
- [Human oversight of agentic systems in practice: Examining the oversight work, challenges, and heuristics of developers using software agents](/dossiers/human-oversight-of-agentic-systems-in-practice.md) — Supplies interview accounts of cognitive distance, regeneration costs, decomposition, and proxy-based review; effectiveness remains unmeasured.
- [Do Users Write More Insecure Code with AI Assistants?](/dossiers/insecure-code-with-ai-assistants.md) — Supplies passing-but-unsafe cases and task-specific security concerns while preserving the nonsignificant adjusted aggregate and corrected-regression boundaries.
- [Lost at C: A User Study on the Security Implications of Large Language Model Code Assistants](/dossiers/lost-at-c-llm-code-assistant-security.md) — Supplies audited passing-but-vulnerable functions, retained defects, and denominator-sensitive counterevidence to uniform assistance harm; no review-support intervention was tested.
