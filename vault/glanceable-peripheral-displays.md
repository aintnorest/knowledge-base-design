---
type: Synthesis
title: Glanceable Peripheral Displays
description: Compact, meaningful encodings can support quick interpretation once inspected, but expert-rated glanceability and peripheral event detection do not establish improved multitasking or comprehension.
tags: [attention, visual-perception, interaction-design, digital-interfaces, cognitive-load]
timestamp: 2026-10-13T00:04:31Z
---

# Glanceable Peripheral Displays

A glanceable display helps someone answer a relevant question with little
interpretation effort once they attend to it. A peripheral display supports an
ongoing activity without requiring continuous focal attention; it may still be
inspected directly. Neither term means that every change will be noticed without
looking, or that a noticed cue will communicate its meaning.

## Selection, Interpretation, and Attention Cost

Separate three requirements:

- **Event detection:** notice that something changed while occupied elsewhere.
- **Glance interpretation:** understand the relevant state when inspecting it.
- **Attention coordination:** decide whether and when to leave current work, with
  an acceptable cost to that work.

A compact display can fail any of these independently. A conspicuous arbitrary
code may be easy to find but slow to interpret; an intelligible static summary
may be missed as a change signal. Continued tracking can demand attention even
after detection; see [Motion Cues: Attention and Distraction](/vault/motion-cues-attention-and-distraction.md).

## Match Form to the Question

The exploratory glanceability report recommends meaningful mappings, abstraction
to essential information, distinct states, and consistent placement and behavior.
These are initial principles, not experimentally validated performance rules.

- Encode ordered quantities with a genuinely ordered dimension, such as position,
  size, or lightness.
- Encode a small set of unordered categories with distinguishable images, shapes,
  or colors without implying a false rank.
- Retain text for unrestricted content, or summarize it before attempting a
  compact visual code. An enormous learned codebook defeats the low-effort aim.

The email examples reveal why meaning comes first: assigning sender groups a
fixed personal–work–administrative–spam hierarchy can misrepresent current
priority. Several dots may be easy to distinguish while answering the wrong
question. A familiar picture also needs a learnable, unambiguous mapping, not
merely a recognizable silhouette.

## Evidence Strength

**Expert judgment and exploratory design:** the report created **30 email-display
versions** and interviewed **nine experienced designers**. Representative images,
colored backgrounds, and multiple dots received favorable judgments; arbitrary
bar orientations and subtle transparency differences drew criticism. Designers
wanted simpler information, distinct states, and category colors without undue
prominence. The study did **not measure glance duration, decision accuracy,
cognitive load, or primary-task performance**. Its ratings generate hypotheses,
not proof that icons beat text or compactness reduces interruptions.

**Controlled dual-task experiments:** in Moticons, **12 students** performing a
number-table editing task detected local oscillating cues nearly **100%** of the
time at near and far locations, around **1 second** after onset. Color-change
errors averaged **5.5% near versus 24% far**. Another **12-student** experiment
measured identifying the changed object separately. These results concern
notification detection and localization, not meaningful state interpretation.

A **14-student** experiment found traveling motion more subjectively distracting
than anchored motion without a clear general detection advantage. The source
recommends slow local motion as a compromise, but subjective distraction is not
a measured primary-task slowdown.

## Practical Use

- Define the question the glance must answer before choosing its visual channel;
  use [Visibility of System Status](/vault/visibility-of-system-status.md) to keep
  compact representations grounded in what the system is actually doing.
- Test each state alone as well as alongside alternatives. Subtle differences
  may be sortable on a comparison sheet yet hard to identify in isolation.
- Separate persistent state coding from attention-capture cues. Evaluate noticing,
  source identification, meaning, and disruption as different outcomes.
- Keep details available for deliberate inspection; abstraction should remove
  irrelevant detail, not consequential information.
- For software or AI-agent supervision, a small set of meaningful summary states
  with inspectable details is an **extrapolation beyond the studied email and
  abstract dual-task domains**, not a demonstrated improvement in supervision or
  uncertainty comprehension.

## Limitations

The expert report provides no rating variability or inferential tests and plots
**26 labeled bars** despite reporting **30 versions**. Its visual-channel variants
also change composed properties such as area and emphasis, so their ratings do
not isolate channel effects. No universal icon semantics, category capacity,
glance-time threshold, or accessibility benefit is established.

The motion experiments use small student samples, exclude color-blind people,
and show one cue at a time. They do not test simultaneous alarms, long-term
habituation, motion sensitivity, state comprehension, or primary-task harm.
Conflicting identification-error prose and figures and inconsistent statistical
reporting prevent a precise cue prescription. Neither source establishes an
independent replication or a general multitasking benefit.

## Sources

- [Designing Glanceable Peripheral Displays](/dossiers/designing-glanceable-peripheral-displays.md) — Proposes information-type mappings and four initial interpretation principles through literature, email-display exploration, and nine designers' judgments, without timed performance evidence.
- [Moticons: Detection, Distraction and Task](/dossiers/moticons-detection-distraction-task.md) — Supplies controlled peripheral detection/localization comparisons and trajectory-dependent subjective distraction, distinct from state comprehension and unmeasured primary-task harm.
