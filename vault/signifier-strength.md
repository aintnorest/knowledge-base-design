---
type: Synthesis
title: Signifier Strength
description: Perceivable cues help people recognize meaningful actions and expected outcomes, but cue strength must be distinguished from real affordance, perceived affordance, and learned convention.
tags: [interaction-design, attention, cognitive-load, digital-interfaces]
timestamp: 2026-10-12T00:02:01Z
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

## Sources

- [Affordance, Conventions, and Design](/dossiers/affordance-conventions-and-design.md) — Separates real action possibilities, perceived possibilities, and learned symbolic communication while preserving the essay's terminology tension.
- [First Principles of Interaction Design (Revised & Expanded)](/dossiers/first-principles-of-interaction-design.md) — Recommends perceivable access and explicit gesture cues, distinguishing task simplicity from visual emptiness without controlled learning estimates.
- [Flat UI Elements Attract Less Attention and Cause Uncertainty](/dossiers/flat-ui-elements-attract-less-attention.md) — Supplies the 71-user findability experiment, heading-versus-link misrecognition, and the limits of bundled cue manipulations.
