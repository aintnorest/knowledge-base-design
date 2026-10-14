---
type: Synthesis
title: Signifier Strength
description: Perceivable cues help people recognize meaningful actions and expected outcomes, but cue strength must be distinguished from real affordance, perceived affordance, and learned convention.
tags: [interaction-design, attention, cognitive-load, digital-interfaces]
timestamp: 2026-10-14T21:39:45Z
---

# Signifier Strength

A signifier is a perceivable cue communicating a possible, meaningful action.
Its strength lies in whether people recognize the action and anticipate its
consequence, not in how much decorative depth the cue has. An element can receive
attention yet be mistaken for static content—or static content mistaken for an
action.

## Affordance, Perception, and Convention

Norman's distinction separates three questions that surface styling can easily
conflate:

- **Real affordance:** what action is possible in the relation between an actor
  and the environment, whether or not the actor knows it. Physical possibility
  does not guarantee useful system response; a reachable display can be touched
  even if touch does not operate it.
- **Perceived affordance:** what the actor believes can be done. An available
  action may go unrecognized; a seemingly available action may not actually work.
- **Convention:** learned symbolic communication that helps create expectations.
  A familiar visual treatment does not create the physical ability to point or
  click; it helps communicate where that action is meaningful and what it means.

Here, *signifier* names the communicating cue, not the actual action possibility
or the user's belief. This is a synthesis vocabulary, not the organizing term of
Norman's 1999 essay. That essay itself has a terminology tension: it first calls
an advertisement of action a perceived affordance, then calls a graphical cue
neither real nor perceived affordance but symbolic communication. The distinction
between possibility, belief, and communication is more useful than pretending
those passages provide a perfectly stable definition of every screen cue.

A coherent conceptual model still matters. Stronger decoration cannot supply
missing behavior, guarantee correct interpretation, or enforce a constraint.
[Consistency and convention](/vault/consistency-and-convention.md) explain why
familiar cues work only when learned meanings and consequences remain reliable.

## Availability Is Not Goal Relevance

The [gulfs of execution and evaluation](/vault/gulfs-of-execution-and-evaluation.md)
distinguish **articulatory distance**, between form and meaning, from **semantic
distance**, between meaning and goals. A cue can clearly communicate an operation
that still expresses the user's intention poorly. Repeatedly recognizable local
actions may be a laborious substitute for one appropriate task-level operation.

A [cognitive walkthrough](/vault/cognitive-walkthrough.md) further distinguishes
having a reason to seek an effect, noticing the correct action, and associating
that action with the effect. The person may never form a system-required
prerequisite goal, or may follow a plausible competing label. Stronger visual
treatment cannot by itself repair either failure.

Recognizing an action also differs from understanding the response:
[visibility of system status](/vault/visibility-of-system-status.md) concerns
whether the resulting state makes progress interpretable in task terms.

**Availability, priority, and state must remain distinguishable.** An action
label can communicate whether proceeding also saves work or makes a consequential
commitment. Faded treatment can communicate unavailability yet conceal the
action's existence or leave its prerequisite unclear. In-field instructional
text can resemble a completed answer rather than an invitation to enter one.
Making a cue more prominent helps only if its meaning is accurate.

## Evidence

A controlled desktop eye-tracking experiment involved **71 general web users**
and **nine page pairs across six domains**. Each person saw one version of each
page, with randomized assignment and order. Participants located a specified
action, announced that they had found it, and stopped; they did not click or
complete a workflow.

Weak-signifier variants produced **22% longer average identification time** and
**25% more gaze fixations**, both **p < .05** in paired comparisons using sites as
the random factor. The manipulation bundled depth, color, underlining, contrast,
and other cue treatments, so it does not isolate shadows or establish that flat
styling causes poor usability.

One page illustrates the recognition problem: **9 of 24** weak-variant participants
stopped at a heading without looking at the intended link. A heading-to-link gaze
sequence occurred in **25 of 29 (86%)** strong-variant participants versus
**12 of 24 (50%)** weak-variant participants, **p < .005**. Attention near the right
content was not sufficient to identify its actionable role. That analysis
accounts for **53 people**, and the public report does not explain the smaller
sample.

**Three of nine pairs** had nearly identical gaze distributions. Retained color
distinction or low density, conventional placement, and separated targets
accompanied those cases. These observations show that weakened depth cues need
not remove recognition; they do not establish the independent necessity or
sufficiency of each alternative cue.

Norman's essay provides conceptual distinctions but **no new participant study**.
Practitioner guidance recommends perceivable access to necessary controls and
explicit gesture instruction; its examples provide **no controlled learning
comparison or participant counts** for those recommendations.

The direct-manipulation account supplies **conceptual theory with no participant
study** for the meaning-versus-form distinction. The walkthrough guide supplies
a theory-based analysis of exploratory learning, not a new signifier experiment;
its simplified **third version had no empirical validation** in that report.
These accounts broaden diagnosis without providing additional cue effect sizes.

A historical **25-person** permission study illustrates misleading prominence.
Explanations of familiar applications' permissions averaged **39% exact
correctness** and were overly broad **29%** of the time; researchers attributed
all but three overly broad responses to prominent category headings. Broad
summaries overpowered narrower descriptions and encouraged exaggerated authority
models. This is observed scope misinterpretation, **not a tested improvement
from redesigned wording or hierarchy**.

Button guidance **recommends** explicit outcome labels, one visually primary
action, and avoiding disabled buttons unless research demonstrates better
understanding. Its rationale is that competing prominence obscures the next
step, and low-contrast unavailable actions can be confusing. It does not establish
that every disabled design has poor contrast or that one-primary-action layouts
always improve performance.

Form guidance reports that placeholder text can look like an already-entered
default, inviting omission. A floating label preserves field identity during
entry but can retain an initially occupied appearance. Persistent identity and
recognizable invitation are therefore separate design questions. Claimed
attention and omission effects come from **unquantified usability observations**,
not an inspectable cue experiment.

Historical dark-presentation guidance **recommends** preserving depth and emphasis
through distinguishable surface lightness and sparse, contrast-tested accents
rather than literal color inversion. Relative text/icon emphasis depends on the
underlying surface, and required content must remain readable when deemphasized.
The examples illustrate a visual grammar; **no participant study** validates its
effect on recognition, depth judgment, or disabled-control discovery.

## Practical Use

- Diagnose the missing layer: unavailable action, unnoticed cue, mistaken role,
  unexpected consequence, or opaque response. Do not treat all five as styling
  problems.
- Make actions distinguishable through cues appropriate to the audience, including
  labels, familiar treatment, contrast, separation, and expected placement.
  Decorative depth is one possible channel, not a requirement.
- Test whether people identify the intended action and expect its outcome, not
  merely whether their gaze lands on it.
- Keep necessary controls visible or reachable through perceivable structures;
  teach unfamiliar gestures rather than assuming hidden operation is obvious.
- Evaluate recognition alongside [recognition over recall](/vault/recognition-over-recall.md),
  but distinguish locating a specified action from discovering an unknown one.
- Test whether the action expresses the user's actual goal, not only whether its
  label or appearance is recognizable. Remove unnecessary prerequisites rather
  than relying on stronger cues to explain them.
- Write labels that expose the action's result and persistence, not merely a
  generic invitation to proceed. Test whether prominent summaries preserve
  the narrower scope rather than encouraging overbroad interpretations.
- Treat unavailability as a state to explain, not just a faded appearance.
  Check whether people can discover the capability and understand what enables
  it; visual presence alone does not establish keyboard or screen-reader discovery.
- Distinguish empty fields, hints, actual defaults, and completed values. Test
  the initial invitation separately from label persistence after typing.
- Preserve action and state distinctions across presentation modes. Check cues
  on their actual surfaces instead of assuming a palette inversion retains them.

## Limitations

The experiment measured short desktop findability tasks, not actual clicking,
mobile interaction, long-term learning, emotional confidence, or business outcomes.
It reports no raw means, confidence intervals, or complete demographics, and no
independent replication is established in the dossier. A **22%** microtask penalty
is not a **22%** workflow penalty. Cue dimensions were bundled, and conventions
vary by community and modality. Norman's claims about screen designers' limited
control over real affordances arise from a mouse-and-keyboard context and need
reconsideration for other forms of input. Neither stronger visual cues nor
familiarity alone guarantee usable behavior or accessibility.

The permission evidence concerns historical install-time lists, a small regional
observational sample, and varying permission sets; grouping and prominence were
not independently manipulated. The newer button, form, and dark-presentation
sources add reasoned recommendations rather than causal effect estimates.
Placeholder variants differ in when instructions disappear, and dated
compatibility claims are not universal current constraints. Contrast and
hierarchical emphasis cannot substitute for accurate labels and usable behavior.

## Sources

- [Affordance, Conventions, and Design](/dossiers/affordance-conventions-and-design.md) — Separates real action possibilities, perceived possibilities, and learned symbolic communication while preserving the essay's terminology tension.
- [First Principles of Interaction Design (Revised & Expanded)](/dossiers/first-principles-of-interaction-design.md) — Recommends perceivable access and explicit gesture cues, distinguishing task simplicity from visual emptiness without controlled learning estimates.
- [Flat UI Elements Attract Less Attention and Cause Uncertainty](/dossiers/flat-ui-elements-attract-less-attention.md) — Supplies the 71-user findability experiment, heading-versus-link misrecognition, and the limits of bundled cue manipulations.
- [Direct Manipulation Interfaces](/dossiers/direct-manipulation-interfaces.md) — Distinguishes form-to-meaning correspondence from task-level fit, explaining why recognizable action cues cannot supply missing semantic operations.
- [The Cognitive Walkthrough Method: A Practitioner's Guide](/dossiers/cognitive-walkthrough-practitioners-guide.md) — Separates forming a relevant goal, noticing an action, and understanding its effect through exploratory-learning theory rather than a new cue experiment.
- [Android Permissions: User Attention, Comprehension, and Behavior](/dossiers/android-permissions-attention-comprehension.md) — Adds observed overbroad scope interpretations attributed to prominent category labels, without an experimentally tested redesign.
- [GOV.UK Button Guidance](/dossiers/govuk-button-guidance.md) — Recommends explicit persistence/consequence labels, limited primary emphasis, and evidence-led use of disabled buttons; main guidance effects are unmeasured.
- [Material 2 Dark Theme](/dossiers/material-dark-theme.md) — Supplies an unmaintained visual model for depth, relative emphasis, and contrast-tested accents across dark surfaces, not measured recognition benefits.
- [Placeholders in Form Fields Are Harmful](/dossiers/placeholders-in-form-fields.md) — Separates persistent identity from apparent-completion ambiguity through guidance and unquantified observations; floating labels address only part of the problem.
