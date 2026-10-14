---
type: Synthesis
title: Interruption Coordination
description: Coordinate secondary demands through immediate, negotiated, mediated, or scheduled delivery according to urgency and attention, without treating one tested implementation or task boundary as a universal optimum.
tags: [attention, interaction-design, decision-making, human-performance, digital-interfaces]
timestamp: 2026-10-14T21:39:12Z
---

# Interruption Coordination

Interruption coordination determines **who controls the switch and when secondary
work is addressed**, not simply how a notification looks. Legitimate demands
cannot always be eliminated, but their delivery can respect ongoing work while
still meeting consequential deadlines. Coordination trades primary-task
protection against secondary-task correctness, completeness, and timeliness;
[interruption costs](/vault/interruption-costs.md) are broader than response speed.

## Four Ways to Coordinate

- **Immediate:** demand attention as soon as work arrives, regardless of current
  activity. This favors prompt handling when even small delays matter.
- **Negotiated:** announce a request and let the person decide when or whether to
  address it. Meaningful control can include leaving secondary work unfinished
  and returning to the primary task, not merely postponing the initial switch.
- **Mediated:** a broker decides when or how a request reaches the person,
  potentially handling it by proxy. Its estimate of demand can be wrong.
- **Scheduled:** deliver at a prearranged time or recurring convention. Batching
  can reduce switches without improving the consequences of either task.

These are coordination policies, not four mutually exclusive visual styles.
The tested mediator used a simple workload heuristic; the scheduled condition
used a fixed interval. Neither stands for every attention-sensitive system.

## What the Controlled Evidence Shows

McFarlane's **36-person within-person experiment** compared one minimal
implementation of each method during a continuous game and intermittent matching
work. Matching completely hid the game, which could not pause. Negotiation alone
allowed users to leave matching before clearing its queue.

Negotiation saved **30.1 jumpers per trial**, versus **23.8 immediate**, **24.7
mediated**, and **19.5 scheduled**; its primary-task advantage over each method
was significant. Yet mean arrival-to-completion age was **15.5 seconds negotiated
versus 1.4 seconds immediate**, and negotiation left more matching work unfinished
than immediate delivery. Processing once displayed was faster with negotiation:
**0.98 versus 1.21 seconds**. Thus waiting for a request and handling it efficiently
are separate outcomes. All four methods saved significantly fewer jumpers than
the single-task baseline.

The source concludes that **negotiation is the best overall tested solution,
except where small differences in secondary-task timeliness are critical**;
there, it favors immediate delivery. That is a conditional recommendation from
the tested tradeoffs, not a universal notification ranking.

A separate **50-person controlled experiment** compared forced secondary work
mid-task with delivery after meaningful task completion. Mid-task delivery
produced higher group-level errors, annoyance, and anxiety; interrupted trials
within that group took longer than uninterrupted trials. The **overall
between-group primary-time effect was not significant**. This supports using
meaningful task boundaries for deferrable work, not claiming zero boundary cost
or a guaranteed speed advantage. A boundary belongs to the person's activity,
not an arbitrary quiet moment.

## Attention-Sensitive Act, Ask, or Wait

Horvitz's mixed-initiative account **recommends**, rather than experimentally
proves, weighing the value of desired assistance against unwanted intervention,
missed assistance, uncertainty about goals, and current attention. Asking has
its own interruption cost. The illustrated expected-utility model can yield
wait, ask, then act as confidence rises, but different costs can change that
ordering or remove an option; there is no universal confidence threshold.

Its timing illustration is one user's fitted observation, with no reported
sample count or uncertainty interval. It does not establish an optimal delay.
See [mixed-initiative interaction](/vault/mixed-initiative-interaction.md) for
sharing control after assistance has begun.

## Match Delivery to Response Need and Current Activity

Platform alert guidance **recommends** reserving modal interruption for essential
information with useful immediate actions. Discoverable in-context status can
communicate a connection problem without forcing a decision, and startup notices
need not block entry to the task. This is an actionable-criticality rationale,
not experimental evidence that every informational alert should disappear.

Accessibility pattern guidance distinguishes **preserving focus from preserving
attention**. An informational alert can leave the next keyboard action unchanged
while still disrupting speech or concentration. Frequent alerts can inhibit use
for people with visual and cognitive disabilities, and automatically disappearing
messages can impose time pressure. The guidance supplies no safe frequency or
duration threshold; see [status announcements](/vault/status-announcements.md).

A **21-developer observational programming study** further distinguishes prompt
composition, waiting, writing, and verification. Only **10.7% of 234 suggestions**
shown during prompt composition were accepted, yet **81.3% of 59 complete prompting
attempts** ended with acceptance. Low immediate acceptance therefore does not prove
that assistance was useless. Explicit waiting occupied **4.2% of average session
time**; adding it to display-to-action measurement raised the mean only
**6.11 to 6.51 seconds**, while waiting episodes added about **2.5 seconds**.
Aggregate latency can conceal moments when responsiveness matters more.

The authors propose avoiding interruption during prompt composition, grouping
suggestions when review is deferred, and prioritizing responsiveness during actual
waiting. These are **untested state-sensitive delivery proposals**, not demonstrated
benefits of an adaptive scheduler.

## Practical Use

- Prefer negotiable requests when secondary work can wait; retain a direct route
  to urgent work and a way to return before emptying a secondary queue.
- Use task completion as a candidate delivery point, with bounded waiting and
  shorter deferral for urgent or relevant information. The timing source
  recommends these policies but did not validate a scheduling algorithm.
- **Interpretation:** a non-blocking notification, such as a toast, can implement
  negotiated coordination if it announces work while leaving timing to the
  person. A toast's appearance alone does not establish negotiation or low cost;
  McFarlane tested a brief flash and explicit show/hide controls, not toasts.
- Evaluate primary-task outcomes, secondary correctness/completeness, arrival-to-
  completion delay, and processing time separately. Fewer switches is not success.
- Separate an immediate response requirement from a need for awareness. Keep
  non-actionable information discoverable in context rather than automatically
  blocking task entry.
- Evaluate the entire announcement stream and time available to understand it,
  not just whether each message preserves focus.
- Distinguish composition, waiting, and review when evaluating assistance timing;
  retain later acceptance and review in the measurement window.
- **Extrapolation beyond the studied tasks:** for software/AI-agent supervision,
  expose pending requests without forcibly hiding ongoing state, and weigh
  act/ask/wait against attention and consequences. These studies do not establish
  performance gains for contemporary agents.

## Limitations

The four-way experiment bundles onset, notification, batching, and switching
control; it cannot isolate the cause of negotiation's advantage. The game is
hidden, continuous, and nonpausable, unlike many document workflows. Mediated
workload estimates can even reflect prior task loss rather than genuine spare
capacity. Preference was not unanimous, and untested hybrid policies are not
validated improvements.

The boundary study used compulsory modal tasks with clear completions, not
freely managed notifications. It did not vary urgency or validate automatic
boundary detection. The mixed-initiative model is a design/theory account with
no controlled usability comparison and unvalidated utility elicitation and goal
probabilities. These sources establish neither a universal wait budget nor a
safety-critical interruption policy.

The alert sources provide reasoned recommendations without controlled outcome
comparisons. The programming study used short tasks, a small organizational sample,
retrospective activity labels, and no unassisted baseline or interface intervention.
It establishes neither a productivity loss from suggestions during composition nor
a benefit from suppression. Its timing proposals do not validate automated state
detection or delivery policies for autonomous-agent supervision.

## Sources

- [Comparison of Four Primary Methods for Coordinating the Interruption of People in Human–Computer Interaction](/dossiers/coordinating-interruption-four-methods.md) — Supplies the four coordination methods, controlled primary/secondary tradeoffs, and conditional preference for negotiation except when timeliness is critical.
- [Principles of Mixed-Initiative User Interfaces](/dossiers/principles-of-mixed-initiative-user-interfaces.md) — Supplies an attention-sensitive expected-utility rationale for acting, asking, or waiting; the prototype and single-user timing illustration do not validate optimal delivery.
- [On the need for attention-aware systems: Measuring effects of interruption on task performance, error rate, and affective state](/dossiers/attention-aware-systems-interruption-effects.md) — Supplies controlled task-boundary timing evidence, bounded to forced modal secondary work and distinct time, error, and affect comparisons.
- [Apple Human Interface Guidelines — Alerts](/dossiers/apple-hig-alerts.md) — Supplies actionable-criticality and startup-context reasons to prefer discoverable in-context information over modal interruption, as unquantified platform recommendations.
- [Alert Pattern](/dossiers/aria-apg-alert-pattern.md) — Supplies focus-preserving announcement with frequency and disappearance cautions for visual and cognitive access, without safe-frequency or duration estimates.
- [Reading Between the Lines: Modeling User Behavior and Costs in AI-Assisted Programming](/dossiers/reading-between-the-lines-ai-assisted-programming.md) — Supplies prompt-composition acceptance and state-dependent waiting observations from 21 developers using August 2022 Copilot; state-aware delivery remains an untested proposal.
