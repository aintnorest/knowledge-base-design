---
type: Synthesis
title: Motion Sensitivity and Reduced Motion
description: Reduce unnecessary spatial motion and preserve information through controllable, non-moving alternatives, while distinguishing vestibular symptoms from distraction and avoiding unsupported claims about safe animation sizes or pulse rates.
tags: [motion, accessibility, interaction-design, accessibility-standards, digital-interfaces]
timestamp: 2026-10-16T00:00:00Z
---

# Motion Sensitivity and Reduced Motion

Interface movement can cause dizziness, nausea, headaches, or other symptoms,
not merely annoyance. For some people the effects persist after movement stops.
The design objective is to preserve information and achievable tasks without
requiring exposure to unnecessary spatial motion.

## What Can Trigger Symptoms

Practitioner accounts identify large-area movement, rapid apparent travel through
depth, parallax in which layers move at different speeds, and movement mismatched
with a person's scroll direction or speed. Unexpected motion and the absence of
an accessible way to stop it compound the barrier. Relative visual extent and
perceived distance matter; a small physical display is not itself an assurance.
These are reported risk dimensions, not experimentally validated cutoffs.

A broader research review distinguishes **vection**, the feeling of self-motion
without actual movement through space, from **visually induced motion sickness**.
Vection can occur without sickness, and their reported strengths do not reliably
rise together. Symptoms without reported vection have also been observed, though
the review questions whether some should instead be classified as oculomotor
symptoms. Absence of felt self-motion is therefore not a reason to dismiss harm.

Sensory conflict among visual, vestibular, and body signals is one prominent
explanation. Postural instability and visually elicited eye movements are other
accounts, and they may interact. The reviewed evidence does not establish a
single mechanism that predicts every individual's response to interface motion.

## Reduced Motion Means an Equivalent Presentation

Separate an animation's **informational purpose** from its **spatial path**:

- If movement is decorative, remove it rather than merely making it slower.
- If movement reveals a new state, consider an immediate state replacement or a
  non-moving change in appearance, retaining readable state and outcome cues.
- If a transition communicates a relationship, preserve that relationship with
  stable placement, labels, or another non-moving representation rather than
  silently dropping necessary information.
- Where substantial movement remains, make its nature predictable and allow
  people to prevent non-essential motion before it is encountered. Respect a
  person's reduced-motion preference across the experience, not just one screen.

These alternatives are a design synthesis, not a tested ranking of treatments.
Practitioner guidance suggests non-moving color or opacity changes as less likely
to provoke vestibular symptoms; it does not prove that every fade or color change
is safe. Repeated luminance changes introduce separate flashing concerns. The
archived standards explanation has an erratum withdrawing blur's categorical
exclusion from motion animation, so blur is not an unqualified safe substitute.

## Two Standards Boundaries, Not One Safety Guarantee

**WCAG 2.2 SC 2.3.3 Animation from Interactions (AAA)** requires that
interaction-triggered motion animation can be disabled unless essential to the
functionality or information. The commentary distinguishes ordinary controlled
scrolling from added non-essential motion such as parallax. It recommends
avoiding unnecessary movement, allowing it to be turned off, or respecting the
person's motion preference. “Essential” does not mean merely attractive or useful:
the information or function must fundamentally change without it and be
unachievable through another conforming presentation.

**SC 2.2.2 Pause, Stop, Hide (A)** addresses automatically starting movement,
blinking, or scrolling that lasts **more than five seconds** and appears alongside
other content: provide pause, stop, or hide unless the activity makes it
essential. Automatically updating information alongside other content needs
pause, stop, hide, or update-frequency control, with **no five-second exception**.
The criteria have different scopes, and an animation can implicate both.

Five seconds is an attention/distraction conformance boundary, **not a
vestibular-safe exposure duration**. A brief interaction-triggered zoom may fall
outside that timing condition while still causing symptoms. A loading-phase
exception in the commentary is conditional on no interaction being possible for
anyone and on progress feedback being needed to avoid apparent breakage; it does
not prove that every loading indicator must move or is safe.

## Practical Use and Limits

Review motion during actual navigation, scrolling, waiting, and state changes,
including automatic repetition and unexpected entry points. Preserve useful
feedback in the reduced-motion presentation; eliminating animation must not make
work appear frozen or hide completion. Seek voluntary feedback from affected
people without requiring them to endure known triggers to justify accommodation.

Keep symptom reports distinct from detection speed, irritation, and task
performance. The [attention and distraction evidence](/vault/motion-cues-attention-and-distraction.md)
does not establish vestibular safety. Two practitioner informants and a narrative
review of heterogeneous simulator/perception studies cannot estimate universal
interface risk or guarantee that a particular alternative is tolerated. Even a
static illustration suggesting movement was reported as triggering in the
practitioner article's comments.

**None of these sources tests small looping indicators or establishes safe pulse
rates.** Neither a slow pulse, small footprint, short duration, nor conformance
alone is evidence of symptom-free use. The review's conflicting correlations and
unresolved definitions further limit quantitative transfer to ordinary
interfaces. Reduced motion is a way to offer control and equivalent information,
not a clinical promise or a reason to force habituation.

## Sources

- [Designing Safer Web Animation For Motion Sensitivity](/dossiers/designing-safer-web-animation-motion-sensitivity.md) — Practitioner guidance grounded in two named first-person accounts, with risk dimensions and user-control recommendations but no controlled safety comparison.
- [Vection and visually induced motion sickness: how are they related?](/dossiers/vection-visually-induced-motion-sickness.md) — Narrative research review distinguishing self-motion perception, symptom mechanisms, inconsistent correlations, and unresolved causal necessity; not a test of interface alternatives.
- [Understanding WCAG 2.2](/dossiers/understanding-wcag-2-2.md) — Informative rationale for SC 2.3.3 (AAA) and SC 2.2.2 (A), their different scopes and essential exceptions, plus the archived animation-definition erratum; not empirical validation of safety thresholds.
