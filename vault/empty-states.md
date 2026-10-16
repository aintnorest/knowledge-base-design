---
type: Synthesis
title: Empty States
description: An empty area should explain the actual system state, how relevant content arrives, and any useful route forward, with explanation proportionate to importance and without empty nonvisual structure.
tags: [interaction-design, content-design, cognitive-load, assistive-technology, accessibility, digital-interfaces]
timestamp: 2026-10-16T00:00:00Z
---

# Empty States

An empty container is not self-explanatory. It can mean that work is still loading,
a completed request found nothing, setup has not happened, content is unavailable,
or nothing currently needs attention. These states imply different decisions:
wait, change the request, configure something, recover access, or simply move on.

## Communicate the Reason Before Offering an Action

Make the state truthful and specific enough for the current task:

- **Loading:** the outcome is not known yet. Do not briefly claim that no content
  exists while retrieval continues.
- **Completed with nothing:** the request has finished without relevant results.
  Where useful, explain the request's scope or a way to adjust it.
- **Not populated or configured:** explain what belongs here and how content
  arrives, whether through deliberate setup, selecting items elsewhere, or use
  over time.
- **Configured and quiet:** nothing currently requires attention. A brief statement
  may be sufficient; do not suggest that successful setup needs repeating.
- **Unavailable:** distinguish an access or system barrier from a genuine absence
  of data, and explain an available remedy or enabling condition where known.

This is [visibility of system status](/vault/visibility-of-system-status.md), not
just a choice of placeholder. A no-results message makes an outcome claim that a
loading indicator does not.

When a useful next step exists, provide an intelligible route into it rather than
naming a task whose entry point the person must hunt for. When none is needed,
do not manufacture an action to fill the space. A short explanation of how content
arrives can teach the feature at the moment it becomes relevant without forcing
a tutorial.

## Scale the Explanation to the Context

Prefer brief text for small, secondary, familiar, or repeated areas. Explanation,
illustration, and competing action invitations all consume attention; a dashboard
with several empty areas should not become a wall of onboarding messages.

More substantial education can be appropriate for an important, complex feature
that people do not understand. That is a conditional choice, not a reward for
having more space. Keep it tied to the current feature and account for maintenance,
translation, optional participation, and what remains after starter content is
removed.

## Showing Empty Is Different from Removing the Section

A visible empty state says **this capability or category exists, but currently has
nothing to show for this reason**. Removing the section removes that cue as well.
A person may instead infer that the capability is unavailable or look elsewhere
for it. This is a synthesis inference related to
[information scent](/vault/information-scent.md), not a measured effect of hiding
empty sections in the supporting guidance.

Retaining every unused section is not therefore mandatory: removal may reduce
irrelevant clutter. Consider whether people need to discover the feature,
understand an outcome, or maintain a stable place to check. If a section disappears
between visits, do not assume its deletion was noticed or understood;
[change detection](/vault/change-detection.md) distinguishes noticing a transition
from recognizing a completed change. These sources do not validate a universal
show-versus-hide policy.

## Avoid Empty Nonvisual Structure

Do not make screen-reader users traverse a content-less table or other redundant
structure before discovering that there is nothing in it. Preserve the contextual
state explanation without exposing a shell that suggests useful content is there.
Replacing empty structure with an explanation is different from removing all
trace of the section.

Decorative imagery should not add nonvisual noise, and essential state or action
information must remain available in text rather than only in the illustration.
The supporting guidance gives accessibility rationale, not measured assistive-
technology outcomes or a complete dynamic-announcement policy.

## Practical Use and Limits

- Review first-use, loading, completed no-results, configured quiet, unavailable,
  and populated states rather than designing only the populated view.
- Ask whether someone can explain why the area is empty, how content will arrive,
  and what, if anything, they should do next.
- Test small and repeated contexts as well as the main first-use screen, including
  nonvisual navigation and transitions between states.
- Evaluate false conclusions of absence and unnecessary retries separately from
  message discovery or action clicks.

The direct sources are **practitioner and design-system guidance, not studies**.
They report no participant comparisons, effect sizes, optimum message length,
measured learning gain, or proof that retaining an empty section outperforms
removing it. Their rationales support design questions and hypotheses, not
universal performance guarantees.

## Sources

- [Designing Empty States in Complex Applications: 3 Guidelines](/dossiers/nngroup-empty-states-complex-applications.md) — Recommends truthful loading-versus-empty feedback, contextual learning cues, and direct task entry through illustrated examples, without measured effects.
- [Carbon Empty States](/dossiers/carbon-empty-states.md) — Adds proportionality, configured-but-quiet states, optional next steps, maintenance costs, and avoiding empty screen-reader structure; living guidance last updated August 11, 2026.
