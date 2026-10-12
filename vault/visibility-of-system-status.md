---
type: Synthesis
title: Visibility of System Status
description: Communicate what the system is doing and how it interpreted an action, distinguishing acknowledgment, acceptance, ongoing work, and completion from the options available next.
tags: [interaction-design, content-design, cognitive-load, digital-interfaces]
timestamp: 2026-10-12T00:01:27Z
---

# Visibility of System Status

People need to know what a system is doing in order to interpret its responses
and decide whether to wait, continue, or correct an assumption. Status visibility
makes the current state understandable; it is not simply the presence of a busy
indicator or the visibility of the next available action.

## How It Works

An action can produce several different messages:

- **Acknowledgment:** the input was received.
- **Acceptance and interpretation:** the request was understood in a particular
  way and accepted for work.
- **Ongoing activity:** the work is still proceeding, with a meaningful account
  of the wait where possible.
- **Completion:** the requested outcome has actually been reached.

These messages need not arrive together. Prompt acknowledgment does not establish
completion, and an activity indication does not establish that the request was
interpreted correctly. Combining signals must not obscure which claim is being
made.

Status also includes persistent configuration and modes, not only transitions.
Expressing current behavior in readable terms lets someone understand the state
before trying to change it. When context is inferred, that distinction helps keep
correction grounded in what the system currently assumes; see
[context inferred over interaction](/vault/context-inferred-over-interaction.md).

Knowing what is happening now differs from knowing what can be done next. The
latter is [recognition over recall](/vault/recognition-over-recall.md): a design can
expose its actions while leaving results opaque, or report progress while hiding
the next useful action.

## Evidence

In a retrospective analysis of **101 heuristics against 249 known usability
problems from 11 projects**, visibility of system status was the leading named
factor, explaining **6.1% of variance in explanation ratings**. The study used
**one rater**, not a new user-performance experiment. Receipt-of-input feedback
was also selected early in a greedy explanatory-coverage analysis. These findings
establish prominence within that corpus, not a causal improvement of 6.1% or a
prospective problem-detection rate.

A historical response-time paper distinguishes acknowledgment, acceptance,
interpretation, and work in progress from final execution. It explicitly permits
long execution after meaning has been confirmed. Its **17 response categories**
provide task-specific timing proposals, but **no original controlled latency
experiment or participant sample** validates those thresholds. The durable
contribution is separating response functions, not assigning every status
message one universal deadline.

An information-software essay demonstrates readable current configuration and
explicit mode cues in worked designs. Its rationale is inspectable, but it
reports **no recruited participant comparison, task-success estimate, or effect
size** for those status cues. First-hand reception and unrelated prediction
simulations do not establish their causal benefit.

## Practical Use

- Specify what each message claims: received, understood, working, or finished.
  Do not make a completion claim when only acknowledgment is known.
- Expose the current configuration or mode before asking someone to adjust it.
- Make feedback timely for its response function rather than judging only total
  execution time; use [response-time thresholds](/vault/response-time-thresholds.md)
  as contextual guidance rather than universal laws.
- Evaluate state comprehension and next-action recognition separately. A visible
  set of controls does not prove that users understand the system's activity.
- During a failure, communicate the recovery state while retaining the task
  context; [error prevention and recovery](/vault/error-prevention-and-recovery.md)
  addresses the work that feedback alone cannot preserve.

## Limitations

Feedback cannot repair incorrect behavior, remove unnecessary delay, or restore
lost work by itself. The historical timing model is task- and expectation-dependent;
its exact numbers are proposals rather than validated boundaries. The heuristic
study has no independent reliability assessment or prospective detection result.
The worked visual examples do not establish universal comprehension or nonvisual
accessibility. More displayed information is therefore not automatically better
status communication: the relevant question is whether people can interpret the
state needed for their task.

## Sources

- [Enhancing the Explanatory Power of Usability Heuristics](/dossiers/enhancing-explanatory-power-usability-heuristics.md) — Identifies status visibility as a leading explanatory factor and separates current-state feedback from available-action recognition.
- [Magic Ink: Information Software and the Graphical Interface](/dossiers/magic-ink-information-software.md) — Uses readable BART notification configuration and announcement-mode cues to demonstrate understanding current behavior before changing it.
- [Response Time in Man-Computer Conversational Transactions](/dossiers/response-time-man-computer-conversational-transactions.md) — Distinguishes acknowledgment, acceptance, interpretation, ongoing activity, and execution with task-specific, explicitly provisional timing proposals.
