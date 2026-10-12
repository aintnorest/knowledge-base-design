---
type: Synthesis
title: Text Alternatives
description: Electronic text preserves the purpose and information of non-text content across sensory presentations, with the alternative shaped by function rather than appearance alone.
tags: [assistive-technology, accessibility, accessibility-standards, digital-interfaces, content-design]
timestamp: 2026-10-12T00:01:24Z
---

# Text Alternatives

A text alternative is an electronic representation of the purpose or information carried by non-text content. Text acts as a presentation-neutral intermediary: it can be rendered as speech, braille, enlarged or restyled visual text, and other forms suited to the user. The objective is equivalent access to meaning, not a verbal inventory of pixels.

## Match the Alternative to the Purpose

WCAG 2.2 **1.1.1 Non-text Content, Level A** distinguishes what the content does:

- **Controls and inputs:** express the function or purpose of the action, not merely the appearance of its symbol.
- **Informative images and complex graphics:** preserve the information. A filename, generic “image,” or a short title cannot substitute for the content of a complex diagram; fuller equivalents may be needed.
- **Decoration, visual formatting, or invisible content:** allow assistive technology to ignore it rather than introducing irrelevant narration.
- **Primarily sensory experiences:** provide descriptive identification, with further description where possible. Words need not recreate an artistic or sensory experience they cannot fully capture.

For serial presentation, meaningful relationships and reading order also matter. An alternative for an image does not by itself preserve information conveyed through the surrounding layout.

## Evidence and Qualifications

The cited source is informative accessibility commentary, not an experiment estimating an effect size for text alternatives. Its rationale is that electronic text can move information between presentation modalities, including tactile access for deaf-blind users. It provides examples and functional requirements, but no participant sample or quantified task-success gain establishing one optimal alternative format.

The sensory-experience qualification is not a general exemption for meaningful images. The raw explanation identifies works of visual art and musical performances as examples whose experience words cannot fully capture; descriptive identification still applies. Likewise, where presenting a test in text would invalidate it, the criterion calls for descriptive identification rather than an equivalent that gives away the test.

Time-based media have additional requirements. Captions include meaningful sounds and speaker identity; audio description supplies important visual action; full textual media alternatives can support deaf-blind access. A descriptive media label is not a substitute for those obligations. Text is also not automatically equivalent to sign language.

## Practical Use

- Decide whether each non-text item is functional, informative, decorative, or primarily experiential before choosing its alternative.
- Judge equivalence by the action a person can take or the information they can obtain, not whether every visual detail is described.
- Give complex information enough explanatory depth, and preserve relationships and reading sequence when presentation becomes serial.
- Avoid decorative noise that adds navigation effort without information.
- Evaluate the alternative in its actual assistive-technology and language context, not merely its presence. [Visual contrast](/vault/color-contrast-minimum.md) and text alternatives protect different access channels.

## Limitations

Some sensory experiences cannot be fully reproduced in text. Assistive-technology support also varies by environment, version, affordability, and language; exposed semantics and usable meaning can diverge. The source admits that all CAPTCHA types exclude some disabled users even when alternatives use different sensory modalities. Standards exceptions negotiate conformance boundaries rather than proving inclusion. Text alternatives must therefore be assessed alongside media requirements, semantic relationships, and complete-process usability with disabled users.

## Sources

- [Understanding WCAG 2.2](/dossiers/understanding-wcag-2-2.md) — Explains purpose-preserving text, decorative handling, media distinctions, and access across speech, braille, and visual adaptation; its underlying non-text-content explanation clarifies sensory and test qualifications.
