---
type: Synthesis
title: Visibility of System Status
description: Make current activity, interpretation, and suspended work understandable, while distinguishing visible status from capability, reliability, explanation, and unproven recovery benefits.
tags: [interaction-design, content-design, cognitive-load, attention, digital-interfaces]
timestamp: 2026-10-14T21:39:12Z
---

# Visibility of System Status

People need to know what a system is doing in order to interpret its responses
and decide whether to wait, continue, or correct an assumption. Status visibility
makes the current state understandable; it is not simply the presence of a busy
indicator or the visibility of the next available action.

## How It Works

### Distinguish Response Functions and Current Modes

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

### Answer the Task Question, Not Just Signal a Change

The [gulfs of execution and evaluation](/vault/gulfs-of-execution-and-evaluation.md)
make the task-level requirement explicit: a state representation must answer
the question needed to judge the goal. Someone controlling how fast a quantity
changes needs its rate; showing only its current level leaves them to derive
the rate over time. Stronger presentation cannot supply that missing meaning.

Likewise, a [cognitive walkthrough](/vault/cognitive-walkthrough.md) asks whether
feedback lets the intended user recognize progress toward the task, not merely
whether an action produces a reaction. This differs from
[signifier strength](/vault/signifier-strength.md), which communicates a
meaningful available action before it is taken.

Event detection, source identification, and state comprehension are separate
layers. A conspicuous change can announce that something happened without
explaining what changed, what it means, or whether attention should shift.

Compact representations must retain that task meaning. An email sender category
is not automatically a priority: an administrative message can be the one a
person urgently awaits. Distinct colors or dot counts can therefore convey an
invented hierarchy clearly. [Glanceable Peripheral Displays](/vault/glanceable-peripheral-displays.md)
addresses low-effort interpretation once inspected, not merely attention capture.

### Match Message Scope and Persistence to the State

Service-notice guidance **recommends** separating service-wide information and
outcomes from a previous page from information needed for the current task. The
latter belongs in the task content; validation failures need identifiable local
messages and a recovery summary rather than a competing general notice.

Success during continuing work differs from terminal journey completion. A
temporary success notice can confirm an action while more work remains; a finished
linear journey can warrant dedicated confirmation. Retire stale success feedback
on navigation so an earlier outcome does not masquerade as current state. Express
success in words, not color alone, and identify recurring notices consistently.
These are guidance-based distinctions, not measured advantages of one container.

Status must also be encounterable beyond visual inspection. A prominent notice can
be skipped through heading navigation; [status announcements](/vault/status-announcements.md)
addresses nonvisual discovery and dynamic updates without conflating announcement
with focus movement.

### Preserve Suspended Work Without Confusing Return with Recovery

A primary task can continue changing while secondary work hides it. Returning
then requires knowing what happened during the absence, not just reopening the
display. For work spread across applications, remembering the suspended task and
restoring its context are also separate requirements. A persistent reminder may
support remembering without recovering the goal, intermediate results, or recent
actions needed to continue.

This connects visibility to [Interruption Coordination](/vault/interruption-coordination.md),
but does not establish that all work should stay fully visible or that earlier
work always deserves immediate resumption. Recovery cues can themselves disrupt
more important current work.

### Separate Status from AI Capability, Reliability, and Explanation

Human-AI guidance recommends distinguishing what the system can do, how well it
can do it, and why a particular action occurred. Current-state feedback alone
does not answer those questions. The source also recommends conveying action
consequences and notifying people about changes in behavior over time; a familiar
status indicator must not silently imply that an adaptive system still behaves
as it did previously. These are inspectable recommendations, not demonstrated
improvements in trust calibration or user performance.

## Evidence

### Heuristic Prominence and Conceptual Feedback Models

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

The direct-manipulation account's rate-versus-level example is **conceptual
theory with no participant study**. The walkthrough guide grounds meaningful
progress feedback in exploratory-learning theory, but explicitly supplies
**no empirical validation of its simplified third version**. Neither provides
a measured improvement from adding a task-level status cue.

### Detection versus Glance Interpretation

Motion-notification experiments isolate an earlier layer. In a dual-task
experiment, **12 students** detected local oscillating cues nearly **100%** of
the time at both near and far locations, around **1 second** after onset;
color-change errors averaged **5.5% near versus 24% far**. A further
**12-student** experiment separately measured identification of the changed
object. These are detection and localization results, not tests of state meaning.
In a **14-student** experiment, traveling cues drew higher subjective distraction
than anchored motion without a clear general detection advantage. Continued
attention demand and primary-task harm are not interchangeable measures.

The glanceability report explored **30 email-display versions** with **nine
experienced designers**, who criticized arbitrary category mappings, subtle
differences, and imposed sender priorities. This is **expert judgment informed
by literature and design exploration**, with no timed comprehension or
multitasking measure. It supports evaluating semantic fit, not a claim that
compact summaries necessarily improve decisions.

A **1,009-person first-click experiment** displayed fifteen app icons with exactly
one badge showing a count of one. Across all fifteen app comparisons, a badged icon
was chosen more often than the same icon when another app carried the badge:
differences calculated from rounded proportions ranged **9.1–41.5 percentage
points**, with all contrasts reported **p < .001**. These are not comparisons
against an entirely badge-free screen or independent replications.

The study measured first choice, not status comprehension, actual unread content,
urgency, task success, or improved experience. Salience and perceived urgency are
proposed explanations, not separately tested mechanisms. A cue's ability to
redirect action does not establish that its implied priority serves the person's
goal; see [choice architecture effects](/vault/choice-architecture-effects.md).

Service-notice guidance cites external banner-blindness evidence to recommend
sparse, prioritized notices, but reports **no component-specific miss rate or
controlled comprehension effect**. It explicitly leaves discovery by assistive-
technology users and the value of dismissal open to further research.

### Suspended-State Visibility: Experiment and Field Association

In a **36-person controlled dual-task experiment**, secondary matching work hid
a continuously running, nonpausable game. Negotiation saved more game characters
than immediate, mediated, or scheduled delivery, but bundled notification,
switching control, batching, and permission to leave the queue. Hidden ongoing
state is a task constraint and plausible recovery problem; **the benefit of
persistent visibility was not experimentally isolated**.

A **two-week observational workplace study** logged **27 people's** computers,
with the final alert-analysis sample unstated. Suspended windows **less than 25%
visible** took longer to return to than those **more than 75% visible** for both
email and IM diversions. No duration difference or adjusted causal effect is
reported. Interviews described cursors, highlights, and reviewing recent actions
as context aids. Visibility is associated with return, while thumbnails, context
restoration, and playback are **proposed recovery designs, not tested benefits**.
First accessing a suspended window also does not establish sustained resumption
or restored mental state.

### AI Transparency: Practitioner Inspection, Not Outcome Validation

The human-AI guidelines were refined through synthesis, internal inspection,
**49 practitioners inspecting 20 products**, and **11 additional experts**
reviewing revisions. Evaluators' confusion between capability, reliability, and
action explanation prompted wording changes. This establishes inspectability
and broad relevance of those distinctions, not causal evidence that supplying
status or explanations improves accuracy, appropriate reliance, or safety.

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
- Evaluate event detection, source localization, state interpretation, and
  goal-level progress separately. Use a salient change cue to invite inspection,
  not as a substitute for an intelligible account of the state.
- Match attention capture to the event's relevance; see
  [motion cues and distraction](/vault/motion-cues-attention-and-distraction.md).
- Keep summaries semantically faithful: distinguish category from current
  priority and avoid replacing needed state meaning with an arbitrary code.
- Place task-critical information within the task and distinguish local errors,
  wider service notices, continuing-work success, and terminal confirmation.
- Remove stale outcome notices when their context ends. Use words and consistent
  identification rather than relying on color or placement alone.
- Treat badge-driven clicks as action redirection, not proof of understood status
  or justified urgency; evaluate whether the destination advances the user's goal.
- Preserve a visible place to resume and accessible task context across
  interruptions. Treat reminders, context restoration, and recent-action review
  as design hypotheses to evaluate, not proven ways to shorten recovery.
- Inspect capability expectations, reliability expectations, action explanation,
  and changes in behavior separately from ordinary progress feedback.
- For software or AI-agent supervision, retaining ongoing state and reviewable
  suspended goals is an **extrapolation beyond the game and workplace email/IM
  studies**, not a measured supervision benefit.

## Limitations

Feedback cannot repair incorrect behavior, remove unnecessary delay, or restore
lost work by itself. The historical timing model is task- and expectation-dependent;
its exact numbers are proposals rather than validated boundaries. The heuristic
study has no independent reliability assessment or prospective detection result.
The worked visual examples do not establish universal comprehension or nonvisual
accessibility. More displayed information is therefore not automatically better
status communication: the relevant question is whether people can interpret the
state needed for their task.

The motion studies used small student samples and did not measure state
comprehension, primary-task performance loss, simultaneous alarms, long-term
habituation, or motion-sensitive users. Their identification-error prose
conflicts with a figure, and statistical degrees of freedom conflict with
reported participant counts; those inconsistencies preclude treating the exact
statistics as a precise cue prescription. Better detection does not establish
better comprehension, low distraction, or accessibility.

The glanceability evidence supplies neither behavioral comprehension thresholds
nor universally understood mappings. The coordination experiment does not
isolate visibility from its other controls. The workplace association can reflect
priority, layout, and selection; window activity is an imperfect task proxy and
cannot isolate cognitive recovery. Human-AI guideline validation concerns
practitioner judgments, not end-user outcomes or exhaustive ethical coverage.
Consequently, visible, compact, and explainable are not interchangeable claims,
and none by itself establishes effective recovery or appropriate reliance.

The badge experiment used one free choice on a static, fixed-layout screen with
one cue, no real message, and no imposed task priority. It does not establish
long-term checking, habituation, competing-badge behavior, or nonvisual access.
The service-notice guidance supplies recommendations and unresolved research
questions, not demonstrated discovery or completion benefits.

## Sources

- [Enhancing the Explanatory Power of Usability Heuristics](/dossiers/enhancing-explanatory-power-usability-heuristics.md) — Identifies status visibility as a leading explanatory factor and separates current-state feedback from available-action recognition.
- [Magic Ink: Information Software and the Graphical Interface](/dossiers/magic-ink-information-software.md) — Uses readable BART notification configuration and announcement-mode cues to demonstrate understanding current behavior before changing it.
- [Response Time in Man-Computer Conversational Transactions](/dossiers/response-time-man-computer-conversational-transactions.md) — Distinguishes acknowledgment, acceptance, interpretation, ongoing activity, and execution with task-specific, explicitly provisional timing proposals.
- [Direct Manipulation Interfaces](/dossiers/direct-manipulation-interfaces.md) — Uses the conceptual rate-versus-level example to show why visible state must answer a goal-level evaluative question, without measured participant benefit.
- [The Cognitive Walkthrough Method: A Practitioner's Guide](/dossiers/cognitive-walkthrough-practitioners-guide.md) — Distinguishes a perceptible reaction from feedback that makes task progress meaningful in exploratory learning, with an explicit third-version validation gap.
- [Moticons: Detection, Distraction and Task](/dossiers/moticons-detection-distraction-task.md) — Separates event detection and source identification from untested state comprehension, with peripheral cue comparisons and trajectory-dependent subjective distraction.
- [Designing Glanceable Peripheral Displays](/dossiers/designing-glanceable-peripheral-displays.md) — Adds expert-judgment support for compact, meaningful state representations that answer the user's question without arbitrary codes or invented priority.
- [Comparison of Four Primary Methods for Coordinating the Interruption of People in Human–Computer Interaction](/dossiers/coordinating-interruption-four-methods.md) — Exposes the recovery problem of a hidden, continuously evolving primary task in a controlled coordination experiment, without isolating persistent visibility's benefit.
- [Disruption and Recovery of Computing Tasks: Field Study, Analysis, and Directions](/dossiers/disruption-recovery-computing-tasks.md) — Associates suspended-window visibility with return and distinguishes reminders from multi-application context restoration; recovery designs remain proposals.
- [Guidelines for Human-AI Interaction](/dossiers/guidelines-for-human-ai-interaction.md) — Separates capability, reliability, action explanation, consequences, and notifications of changed behavior through practitioner inspection rather than causal outcome validation.
- [Driven by notifications – exploring the effects of badge notifications on user experience](/dossiers/badge-notifications-user-experience.md) — Supplies 1,009-person first-choice redirection by one app badge, without measuring status comprehension, real urgency, experience gains, or sustained use.
- [GOV.UK Notification Banner Guidance](/dossiers/govuk-notification-banner-guidance.md) — Supplies boundaries between wider notices, task-local information, continuing-work success, and terminal confirmation, with sparse-use rationale but unknown component-specific discovery outcomes.
