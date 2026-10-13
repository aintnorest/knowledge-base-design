---
type: Synthesis
title: Interruption Costs
description: Interruptions can alter primary performance, affect, and the path back to sustained work, but faster active work and long observed return delays establish neither low burden nor universal causal recovery costs.
tags: [attention, cognitive-load, human-performance, interaction-design, digital-interfaces, ux-metrics]
timestamp: 2026-10-13T00:04:28Z
---

# Interruption Costs

An interruption can impose costs beyond the time spent responding to it:
primary-task loss, errors, annoyance, anxiety, and difficulty returning to
sustained work. Primary work can slow down or speed up under interruption;
neither direction alone establishes the total burden. Delivering deferrable
secondary work after meaningful completion can reduce disruption relative to
forcing a switch mid-task. A boundary belongs to the person's activity, not
merely a quiet moment or an arbitrary elapsed time.

## Timing Evidence and Its Comparisons

A single controlled experiment assigned **50 participants**, ages **18–40**, to
**25-person groups**. Both groups performed the same primary and secondary work;
one received secondary tasks approximately halfway through primary tasks, the
other after finishing them. Six primary-task categories included arithmetic,
counting, comprehension, selection, and registration. Secondary work obscured
the primary work area, and participants had to respond immediately.

The **overall between-group timing effect on primary-task time was not
significant**. The clearest slowdown evidence is instead within the mid-task
group: primary work averaged **33.60 seconds** with a reading interruption,
**32.15 seconds** with a reasoning interruption, versus **29.16 seconds** without
interruption. Category-specific penalties ranged from **3–27%**. These times
exclude secondary-work duration and do not separately measure resumption lag.

Boundary-delivered secondary work had no significant effect on primary-task
time within the control group. That is consistent with lower boundary cost,
not proof of zero cost or a significant blanket group-speed advantage.

## Errors and Affect Are Separate Outcomes

The mid-task group averaged **0.22 errors per scored primary task**, versus
**0.11** in the boundary group. However, interrupted versus uninterrupted trials
within the mid-task group did not differ significantly in errors. The group
result therefore does not mean that each interruption immediately doubles error.

Primary-relative annoyance averaged **11.40 versus 7.29** on a **1–25 scale**.
The source's claimed percentage increase conflicts with these means; numeric
rating differences are not ratio-scale quantities of emotion. Both groups'
state anxiety rose: **32.32 → 44.04** in the mid-task group versus
**32.68 → 38.96** at boundaries. The increases were **11.72 versus 6.28**, not a
doubling of final anxiety or evidence of an anxiety disorder.

Higher-demand arithmetic and counting tasks had substantial costs, but measured
difficulty did not monotonically predict slowdown: reading was second-hardest
and slowed **7%**, whereas counting slowed **27%**. Even boundary-delivered work
was more annoying after difficult tasks. Closure need not mean instantaneous
psychological recovery.

## Faster Work Can Still Be Costly

A separate **48-person controlled email experiment** found faster primary work
under compulsory interruptions: **22.77 minutes without interruption**, versus
**20.31 with same-topic** and **20.60 with different-topic** interruptions. These
times **subtract interruption duration**; they do not establish a faster total
workflow or separately measure local recovery lag.

Stress rose from **6.92** without interruption to **9.46 / 9.13** in the two
interrupted conditions on a **1–20 scale**. Frustration and effort also rose in
both. Compensatory acceleration is the authors' interpretation, not a measured
mechanism; shorter messages explain only part of the pattern. Error and
politeness differences were not significant, which is not verified equal
quality. The same-topic versus different-topic time contrast was also
nonsignificant: shared topic is not necessarily useful assistance, and the
result does not establish equivalent interruption costs.

## Forced Switching and Primary-Task Loss

In a **36-person controlled dual-task experiment**, a continuous game kept
running while secondary matching work hid it. Immediate switching saved
**23.8 jumpers per trial**, versus **30.1 with negotiated switching**, and produced
**53.5 versus 15.9 UI keying errors**. Those keying errors include redundant moves
and keys used in the wrong mode; they are distinct from wrong task answers and
were prevented from directly damaging outcomes.

Immediate delivery minimized secondary arrival-to-completion age
(**1.4 versus 15.5 seconds**) but processing after display was slower
(**1.21 versus 0.98 seconds**). Negotiation left more secondary work unfinished.
The implementation bundled timing with the ability to leave the secondary queue,
so delayed onset alone cannot explain its advantage. See
[interruption coordination](/vault/interruption-coordination.md) for the
correctness, completeness, and timeliness tradeoffs.

## Task Resumption: First Return Is Not Sustained Work

A **two-week observational workplace study** deployed logging on **27 computers**
and collected **2,267 hours** of activity; the final alert-analysis participant
count was not reported. An alert-associated diversion often expanded into
additional messages and other applications, not just the initial response.

Time from entering the alerting application to **first access to any suspended
application** averaged **9 minutes 33 seconds for email** and **8 minutes for IM**.
The **additional inferred resumption phase** averaged **15 minutes 50 seconds–
16 minutes 33 seconds for email** and **10 minutes 58 seconds–12 minutes 2 seconds
for IM**, depending on immediate/delayed response. Those within-channel response
differences were not significant.

These phases distinguish first return, navigating back through task context,
and sustained activity. The study counted **more than 15 seconds** on a suspended
application as resumption; it did not measure restored mental state. Its means
are **not pure cognitive recovery lag, causal productivity loss, or a universal
per-notification penalty**. Useful new work and intentional priority changes can
occupy the intervening time.

Suspended windows **less than 25% visible** were associated with slower return
than windows **more than 75% visible**, without a reported duration difference
or adjusted causal effect. Interviews described difficulty restoring
multi-application context and use of cursors/highlights as reminders. The source
recommends visible reminders, preserved joint context, easy return, and review
of recent actions; none of those recovery interventions was tested.

## Plausible Mechanisms, Not Measured Causes

Recovering a suspended goal and intermediate state can plausibly require effort;
anticipating another interruption may also change resource allocation. These
accounts connect to [working-memory limits](/vault/working-memory-capacity-limits.md).
The boundary experiment did **not directly measure memory allocation or
physiological workload**, and workplace window logs do not measure mental
reconstruction. Block-level email timing cannot separate a local recovery
slowdown from acceleration elsewhere. The studies therefore do not establish
one common mechanism for all observed costs.

## Practical Use

- Place deferrable secondary work at meaningful completion boundaries when urgency
  permits. The source recommends bounded waiting and shorter deferral for urgent
  or relevant work; it did not validate a scheduling algorithm.
- Distinguish secondary-work duration, primary-work overhead, waiting, first return,
  and sustained resumption from errors and affect. Neither a quick response nor
  faster active primary work proves low burden.
- Preserve the suspended goal, intermediate results, and a visible place to resume,
  including context spanning applications. Treat the field study's reminder and
  restoration proposals as candidates for evaluation, not proven remedies.
- Support return without forcing it: recovery cues can themselves interrupt more
  important current work, and an intentional diversion is not automatically harm.
- Apply the closure rationale in [response-time thresholds](/vault/response-time-thresholds.md)
  without turning it into a universal seconds-based deferral budget.
- Maintain [visibility of system status](/vault/visibility-of-system-status.md)
  while deferring optional demands; postponing secondary work is not a reason to
  conceal consequential state or withhold necessary acknowledgment.
- **Extrapolation beyond the studied domains:** in software/AI-agent supervision,
  retain suspended goals and reviewable recent actions; fast handling of status
  requests is not evidence of low supervisory burden. No cited study tested
  contemporary agents or automatic supervisory-context restoration.

## Limitations

The timing findings come from one laboratory experiment with forced, obscuring
secondary tasks, not freely managed notifications. Clear task boundaries and
little carryover limit transfer to extended activities. Frequency, urgency,
relevance, presentation, and rehearsal opportunities were not experimentally
varied. Related earlier reporting uses the same dataset, not an independent
replication.

Time-analysis degrees of freedom imply **49 users** despite **50 recruited**, with
no exclusion explanation. The source reports no confidence intervals or
standardized effects and contains annoyance arithmetic discrepancies. Its
abstract compresses within-group slowdown into an apparent direct timing-group
comparison; the nonsignificant timing main effect must remain visible. A claim
that boundary deferral required only a few seconds lacks a measured delay
distribution. Neither these data nor the inferred resource-release explanation
establish a universal optimal wait or immunity from disruption after completion.

The email experiment used mostly students and a compulsory artificial-supervisor
task. Its quality proxies omit broader completeness/usefulness, several collected
workload facets are unreported, and statistical degrees of freedom are unexplained.
The four-method experiment compares one bundled implementation per method during
a hidden nonpausable game; it does not isolate visibility's causal benefit.

The field study is observational, from one organization's desktop environment.
Window activity and **15-second** thresholds are imperfect task/attribution
proxies; analyzed participant counts, event denominators, and censoring details
are incomplete. Large variability and long tails prevent treating mean phases as
individual predictions. Visibility associations may reflect priority or display
arrangement rather than a reminder effect, and alerts cannot be credited with
causing all intervening activity.

## Sources

- [On the need for attention-aware systems: Measuring effects of interruption on task performance, error rate, and affective state](/dossiers/attention-aware-systems-interruption-effects.md) — Supplies the 50-person workload-controlled timing experiment, distinct time/error/affect comparisons, and limits of forced secondary work and inferred mechanisms.
- [The Cost of Interrupted Work: More Speed and Stress](/dossiers/cost-of-interrupted-work.md) — Adds controlled evidence of faster active primary work with greater stress, frustration, and effort, without a total-workflow benefit or context-equivalence result.
- [Comparison of Four Primary Methods for Coordinating the Interruption of People in Human–Computer Interaction](/dossiers/coordinating-interruption-four-methods.md) — Adds primary-task loss and mode-keying errors under forced switching, and distinguishes request waiting from processing time.
- [Disruption and Recovery of Computing Tasks: Field Study, Analysis, and Directions](/dossiers/disruption-recovery-computing-tasks.md) — Adds observational diversion chains, first-return versus sustained-resumption phases, and visibility/context associations; recovery interventions remain untested.
