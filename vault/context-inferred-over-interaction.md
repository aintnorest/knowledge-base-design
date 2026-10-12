---
type: Synthesis
title: Context Inferred over Interaction
description: Information software can reduce repeated context-setting by inferring a useful starting view from environment and history, organizing it around decision questions, and keeping correction inexpensive.
tags: [information-architecture, interaction-design, data-visualization, cognitive-load, digital-interfaces, privacy]
timestamp: 2026-10-12T00:01:45Z
---

# Context Inferred over Interaction

When a person's goal is to understand a situation, information software should
first make the relevant relationships legible. It can use available context to
present a plausible starting view instead of demanding repeated setup before
showing anything useful. Interaction then supplies missing context or corrects
wrong assumptions rather than being the default price of access.

This is a design recommendation, not a law that interaction is always bad. It
applies to learning and comparison; creating an artefact or committing a
transaction has different requirements.

## Questions Before Controls

Start with the questions a decision requires. Select and arrange information to
answer those questions, then determine which input is genuinely necessary.
Changing the visual organization can change what is readily understandable even
when the underlying data are identical.

A table can support exact arrival lookup while a time–distance graphic reveals
speed, stops, and relationships between services. Grouping options by time can
answer “what is available then?” while grouping them by venue answers a different
question. Neither arrangement is inherently correct: its usefulness depends on
the decision. Comparative richness does not mean displaying every possible datum.

[Co-visible comparison](/vault/juxtaposability-for-comparison.md) can replace
repeated navigation, extraction, and memory-dependent merging. The intended
benefit is better understanding, not fewer clicks as an isolated target.

## Infer a Starting Point, Preserve Correction

The proposed hierarchy is:

1. **Environment:** relevant time, location, current documents, or other available
   information can establish likely context.
2. **History:** previous environments and interactions can supply a starting
   point or recurring pattern, while older patterns fade as circumstances change.
3. **Interaction:** ask for what cannot be inferred and let the person correct
   the starting point. Correction can become evidence for future predictions.

The ordering is a recommendation, not a tested ranking of effectiveness. It
requires useful available context and a manageable cost of being wrong. Relative
navigation from a plausible starting point and tight feedback loops can make
correction less demanding than precise blank-state specification.

An inferred interest is not certainty about intention. The current view must
remain understandable, with alternatives discoverable and wrong assumptions
cheap to replace. Readable current behavior is also a
[system-status concern](/vault/visibility-of-system-status.md). Inferring a useful
view should support judgment, not silently make consequential commitments.

## The Evidence

The supporting design essay provides worked graphical redesigns and first-hand
experience, not recruited-participant trials. Its demonstrations expose how
representations support different questions, but supply no task-success rates,
user-time distributions, or causal comparison between inference and explicit
input.

An implemented route predictor was tested with **simulated schedules**, not
human participants. Example schedules contained **10 or 12 predictions per
week**, with visit-time noise having a **30-minute standard deviation**. The
author reports learning a regular pattern within **one week** and adapting to a
changed schedule within **a couple of weeks** under those assumptions. No
real-world prediction accuracy or confidence interval is established.

The noise example illustrates a crucial denominator problem: at roughly **two
random routes per scheduled route**, it shows about **four mispredicted scheduled
views out of ten**, while random views are described as **always mispredicted**.
That is not 60% accuracy over all consultations. Regular-case performance can
hide systematic failure on new needs.

## Practical Use

- Identify the comparisons and relationships required for the actual decision
  before selecting controls or grouping information.
- Use available, appropriate context to offer a helpful starting view; preserve
  a clear route to the missing option or a different context.
- Assess the combined burden of setup, correction, and inference failures,
  including unfamiliar situations rather than only recurring routines.
- Distinguish learning about choices from accepting one. Helpful presentation
  does not remove the need to communicate a consequential decision.
- Treat consent, purpose separation, retention, shared-device behavior, and
  security as design questions when using personal context.

## Limitations

Sparse history, changing interests, novel needs, and unavailable context weaken
prediction. Winnowing can hide an unexpected comparison. Implicit feedback is
ambiguous: looking away can indicate satisfaction, interruption, or failure.
The essay supplies no general solution to these problems and calls its predictor
ad hoc rather than a general algorithm.

Its declared scope is personal desktop software, not every social or creative
activity. Useful, enjoyable, or educational interaction can have positive value.
Graphics still impose interpretation, literacy, and visual-search demands;
nonvisual access and low-vision alternatives are not developed in the source.
Cross-source inference also raises privacy and security obligations that the
proposal acknowledges but does not resolve.

## Sources

- [Magic Ink: Information Software and the Graphical Interface](/dossiers/magic-ink-information-software.md) — Argues for question-oriented information graphics and environment/history inference; its timetable, catalog, and movie-listing redesigns, BART experience, and simulated route predictor supply rationale while exposing correction, error-denominator, and privacy limits.
