---
type: Synthesis
title: Color Contrast Minimum
description: Minimum luminance contrast protects access to necessary text and graphics, but a passing ratio does not establish legibility or replace non-color cues and semantics.
tags: [low-vision, accessibility, color, accessibility-standards, digital-interfaces, typography]
timestamp: 2026-10-12T00:00:55Z
---

# Color Contrast Minimum

Necessary visual information must remain distinguishable when visual acuity or contrast sensitivity is reduced. The relevant contrast is a difference in **luminance**, not a preferred hue pairing. Contrast thresholds establish a testable accessibility floor; they do not ensure that every reader can comfortably perceive the content.

## What Needs Contrast

WCAG 2.2 separates text from necessary non-text information:

- **1.4.3 Contrast (Minimum), AA:** ordinary text requires **4.5:1**; large text requires **3:1**. Large means **18 point**, or **14 point bold**. Placeholder text and text revealed during interaction remain text. Incidental or decorative text, inactive controls, and logos have exceptions; ordinary interface copy is not exempt merely because it uses corporate colors.
- **1.4.11 Non-text Contrast, AA:** visual information necessary to identify controls, states, and meaningful graphical objects requires **3:1 against adjacent colors**. This does not make every decorative line or control boundary mandatory. A text-labelled action may be recognizable without a border, while a selected-state mark still needs to be distinguishable.

For graphics, ask whether the information remains understandable if low-contrast portions are effectively invisible. A conforming alternative can carry chart information rather than requiring each graphical segment to communicate it unaided.

## Evidence and Rationale

The cited commentary is informative standards guidance, not a new experiment demonstrating optimal reading thresholds. It cites earlier standards for a **3:1** normal-vision baseline and letter-contrast/acuity research for an approximately **1.5-fold** contrast-sensitivity loss associated with **20/40** acuity: **3 × 1.5 = 4.5**. The enhanced **7:1** threshold is analogously motivated by approximately **20/80** acuity; aging-related acuity research also informs the rationale.

These are explicit derivations from cited work, not a controlled test of every modern typeface, display, or reading task. The dossier reports no participant counts or modern interface-reading effect estimates for that derivation. Thin or anti-aliased text can nominally pass while appearing faint; the guidance recommends exceeding minima or strengthening strokes.

## Practical Use

- Evaluate ordinary text, large text, necessary graphics, and states under their distinct requirements rather than applying one ratio indiscriminately.
- Identify which adjacent colors surround necessary non-text information, including changes of state.
- Preserve visible non-color cues where meaning depends on a distinction. Contrast alone does not communicate that distinction to every sighted user.
- Pair visible information with usable semantics and, where needed, [text alternatives](/vault/text-alternatives.md). Repairing visual contrast does not expose meaning to assistive technology.
- Exceed minima or strengthen text strokes when a nominal pass still produces faint reading; assess usability with the relevant disabled users.

## Limitations

Conformance thresholds are not universal legibility guarantees. Contrast, visible differentiation, and semantic access are separate obligations: a hidden accessible name cannot provide a visible non-color cue, and a visible label or shape does not automatically expose its meaning to assistive technology. Exceptions delimit the criterion rather than proving that exempt content is usable. The informative explanation must be read against the normative WCAG 2.2 criterion, and neither a partial automated check nor a passing ratio establishes accessibility of the complete experience.

## Sources

- [Understanding WCAG 2.2](/dossiers/understanding-wcag-2-2.md) — Explains text and adjacent non-text contrast thresholds, the cited acuity-based derivation, exceptions, and the distinction between nominal contrast, visible cues, semantics, and actual legibility.
