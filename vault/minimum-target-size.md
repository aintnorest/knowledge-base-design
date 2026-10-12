---
type: Synthesis
title: Minimum Target Size
description: Minimum active target dimensions and spacing reduce precision demands, but accessibility conformance floors do not guarantee easy or safe acquisition.
tags: [motor-accessibility, accessibility, accessibility-standards, digital-interfaces, human-performance]
timestamp: 2026-10-11T23:59:46Z
---

# Minimum Target Size

A pointer target needs enough active area, or enough isolation from competing targets, to tolerate imprecise movement. Small, crowded targets increase missed and accidental activations, especially for people with tremor, spasticity, limited dexterity, or less precise alternative pointers. Touch input adds its own precision constraints.

## Size and Spacing Are Different Protections

The relevant size is the **active target**, not the visible symbol inside it. Increasing the active area makes successful acquisition easier; reserving space around a small target reduces the chance that a miss activates something else. Isolation does not make the small target itself easy to hit.

WCAG 2.2 distinguishes two conformance thresholds:

- **2.5.8 Target Size (Minimum), AA:** at least **24 × 24 CSS pixels**, subject to spacing, equivalent-control, inline, user-agent, and essential exceptions.
- **2.5.5 Target Size (Enhanced), AAA:** at least **44 × 44 CSS pixels**, subject to equivalent-control, inline, user-agent, and essential exceptions. This criterion does **not** have the AA spacing exception.

For the AA spacing exception, a **24 CSS pixel diameter circle centered on an undersized target's bounding box** must not intersect another target or another undersized target's corresponding circle. This is not simply a fixed gap between icons: a nearby large target also matters. A circular target 24 pixels in diameter does not necessarily contain the required 24-pixel square and may need the spacing exception.

## Evidence and Rationale

[Fitts's law](/vault/fitts-law-pointing-time.md) supplies a performance model: narrower targets demand greater precision relative to travel distance. It does not establish a minimum pixel size or an accessibility threshold.

The accessibility guidance explains the benefits of size and spacing and cites thumb-target research, but does not report that study's sample, effect estimate, or a calculation proving that 24 CSS pixels is universally sufficient. The 44-pixel enhanced threshold likewise lacks a threshold-validation experiment in the cited commentary. These are standards-backed conformance boundaries, not demonstrated biological cutoffs or universal optima.

The guidance explicitly admits that very small, difficult-to-activate targets can satisfy AA when sufficiently isolated. It recommends larger targets for frequent actions, difficult reach, sequential tasks, and actions that are hard to undo.

## Practical Use

- Assess active regions and neighboring actions rather than judging visible icons alone.
- Use size to ease acquisition and spacing to protect against competing activations; do not substitute one rationale for the other.
- Give frequent, hard-to-reach, sequential, or difficult-to-reverse actions more tolerance than the minimum requires.
- Evaluate acquisition with the relevant users and input methods. A passing geometry check is not evidence of comfortable task completion.

## Limitations

Inline and essential exceptions preserve other requirements, such as readable reflow and meaningful spatial content; they do not remove the user's precision burden. Acquisition also depends on approach direction, movement distance, input method, selection behavior, and error recovery. Neither these thresholds nor the cited pointing model establishes edge or corner benefits.

## Sources

- [Understanding WCAG 2.2](/dossiers/understanding-wcag-2-2.md) — Explains AA and AAA active-target thresholds, spacing geometry, exceptions, motor-accessibility rationale, and the admission that conformance can coexist with difficult acquisition.
- [Fitts' Law as a Research and Design Tool in Human-Computer Interaction](/dossiers/fitts-law-research-design-tool-hci.md) — Models distance–precision demands and qualifies geometry and task dependence without supplying a minimum target size.
