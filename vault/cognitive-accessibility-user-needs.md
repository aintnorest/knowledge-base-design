---
type: Synthesis
title: Cognitive Accessibility User Needs
description: Cognitive accessibility supports independent task completion by reducing avoidable comprehension, memory, attention, and recovery demands, but consensus patterns do not establish universal usability or measured treatment effects.
tags: [cognitive-accessibility, accessibility, digital-interfaces, cognitive-load, content-design, user-research]
timestamp: 2026-10-14T21:39:12Z
---

# Cognitive Accessibility User Needs

Cognitive accessibility concerns whether people with cognitive and learning
disabilities can understand and complete a task without avoidable dependence on
someone else's help. A technically available action is insufficient if finding,
interpreting, remembering, or recovering it creates an insurmountable barrier.
Needs vary within and across diagnoses; competence in one domain does not imply
ease with every interface demand.

## A Functional Needs Model

The guidance organizes needs into **eight objectives**:

- Understand what things are and how they work.
- Find what is needed.
- Understand the content.
- Avoid mistakes and correct them.
- Maintain focus.
- Complete processes without memory barriers.
- Obtain help.
- Adapt the interface to personal needs.

These objectives connect a user need to a proposed pattern, an illustrative
scenario, and questions about actual task completion. Familiar cues, literal
language, persistent instructions, visible task position, forgiving input,
retained work, controllable distraction, and accessible help address different
barriers. Simplification should remove unnecessary demands without hiding needed
actions, meaning, or a route back to fuller functionality.

[Working-memory capacity limits](/vault/working-memory-capacity-limits.md) explain
why retention demands need attention, but do not supply a universal visible-choice
limit. [Recognition over recall](/vault/recognition-over-recall.md) externalizes
needed context, while [error prevention and recovery](/vault/error-prevention-and-recovery.md)
asks whether the correction journey itself remains achievable.

## Evidence and Status

The model rests on **task-force consensus and cited research**, supporting issue
papers and syntheses, public feedback, and reasoned functional explanations. It
reports **no original participant experiment or replication test** of the model,
and does not establish measured treatment effects for individual patterns.

The **ten personas are fictional**, not research participants or a prevalence
sample. They illustrate heterogeneous memory, language, attention, numerical,
and executive-function barriers. Scenario-to-pattern mappings make the rationale
traceable; they do not confirm causality or coverage of every user.

This is informative **2021 supplemental guidance beyond WCAG**, not a set of
additional conformance requirements. It cites a **2020 WCAG 2.2 Working Draft**,
not the later final Recommendation. The distinction does not make a barrier
unimportant to the person it excludes.

### Reading Accommodations Need Outcome Evidence

A within-person experiment recruited **48 people with clinically documented
dyslexia**, with **46 valid eye-tracking recordings**, to read twelve counterbalanced
**60-word Spanish passages** in different fonts. A font specially designed and
labeled for dyslexia showed **no demonstrated reading advantage**. Absence of
superiority in this task does not prove identical performance for every reader.

Some upright, sans-serif, and monospaced settings produced shorter fixations, but
the category comparisons did **not** establish significant whole-text reading-time
gains. One italic design was significantly slower than three upright alternatives.
Liking and reading time were only weakly associated (**r = −.13**), so preference,
processing measures, and reading speed answer different accommodation questions;
see [typeface legibility](/vault/typeface-legibility.md).

Comprehension questions filtered out incorrect trials rather than demonstrating
improved comprehension. The experiment provides task-specific participant evidence
alongside the broader consensus needs model, not validation of that whole model or
of a universal dyslexia font.

## Practical Use

- Identify what the complete task demands of understanding, retention, attention,
  timing, and recovery, especially in consequential services.
- Keep instructions, earlier choices, current position, and consequences
  inspectable where they are needed; avoid unaided memory or puzzle-solving as
  prerequisites for authentication and help.
- Preserve valid work and user-selected support. Keep defaults accessible rather
  than requiring customization before the person can begin.
- Evaluate with diverse disabled participants and accessible, ongoing voluntary
  consent, breaks, and preferred environments. Distinguish assistance from
  independent completion.
- Observe task success, errors, completion time, and satisfaction rather than
  accepting verbal assurance or automated checks as proof of understanding.
- Evaluate reading accommodations through relevant comprehension, errors, speed,
  and user preference rather than trusting a disability-specific label or shorter
  fixations alone. Preserve individual choice as an **analyst implication**, not a
  customization intervention proven by the font experiment.

## Limitations

Numerical pattern suggestions are not validated universal thresholds. The
source's illustrative impaired-memory ranges vary between **1–3**, **1–4**, and
**1–2 items**, alongside an unqualified average of **seven**; their measurement
conditions are absent. Do not turn them into menu-size rules or replace the
conditional chunk account of working memory.

Familiarity is individual and cultural; a symbol that helps one person can
confuse another. Security and privacy can limit retention, and simplification
can remove useful information. A successful test supports only the participants,
tasks, conditions, and version examined, not usability for everyone. Situational
stress or unfamiliar-language testing cannot substitute for participation by
people with cognitive and learning disabilities.

The font study used short Spanish texts, one display, one nominal size, and no
non-dyslexic comparison. Equal point size did not match x-height, width, spacing,
or wrapping; category differences cannot isolate a single typographic cause.
Its abstract's broad performance claims exceed the detailed reading-time results,
and some preference summaries conflict internally. It supplies neither sustained-
reading evidence nor a measured individual-customization benefit.

## Sources

- [Making Content Usable for People with Cognitive and Learning Disabilities](/dossiers/making-content-usable-cognitive-learning-disabilities.md) — Supplies the eight-objective needs model, fictional personas, independent-completion testing guidance, and research-informed task-force rationale, bounded as the informative 2021 Note rather than measured treatment effects or WCAG requirements.
- [Good Fonts for Dyslexia](/dossiers/good-fonts-for-dyslexia.md) — Supplies diagnosed-dyslexia screen-reading evidence separating fixation duration, reading time, and preference, with no demonstrated OpenDyslexic advantage or comprehension improvement; short texts and unmatched glyph dimensions constrain generalization.
