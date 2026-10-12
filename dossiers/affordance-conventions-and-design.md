---
type: Study Note
title: Affordance, Conventions, and Design
description: Norman separates possible action from perceived action and learned screen conventions, but offers conceptual clarification rather than an empirical test of their usability effects.
resource: https://doi.org/10.1145/301153.301168
source: https://doi.org/10.1145/301153.301168
tags: [interaction-design, digital-interfaces, design-process]
timestamp: 2026-10-11T23:50:37Z
---

# Affordance, Conventions, and Design — Study Notes

**Authors**: Donald A. Norman.  
**Published**: May–June 1999; ACM interactions 6(3), pp. 38–42.  
**Status**: Published conceptual essay; the supplied PDF is the magazine article, not a later revision of The Design of Everyday Things. It presents no new participant study.  

## What It Is

A correction to the design community's use of *affordance* as a synonym for a visible invitation to click. Norman accepts responsibility: his earlier book usually meant **perceived affordance**, although it used the unqualified term. The practical distinction is between what an actor can do, what the actor believes can be done, and the conventions through which a display communicates meaningful action.

## Problem and Motivation

Designers debating whether an icon “affords clicking” were substituting terminology and opinion for evidence about users. A mouse already lets a person point and click throughout the screen; drawing a new icon does not create that physical possibility. What matters for screen design is whether users recognize clicking a particular object as useful and anticipate its outcome.

Norman places **a coherent, perceivable conceptual model** above affordance as the central design problem. Constraints and conventions make that model intelligible; they are not lesser substitutes to be ignored while polishing surface clues.

## Principles as Ideas

- **Real affordance is relational possibility.** In Gibson's formulation, actionable relations between actor and world exist whether visible, known, or desirable. A reachable non-touch-sensitive display still affords touching, even though touching does not operate the computer. Possibility and useful system response are different questions.
- **Perceived affordance concerns believed possibility.** In physical products, real and perceived affordances can differ. On conventional screens, much of the physical action repertoire is supplied by hardware; designers mainly influence what users think is meaningful. Feedback, actual possibility, and perceived possibility can be manipulated independently.
- **Physical constraints prevent action.** A cursor cannot leave its permitted screen area; restricting it to meaningful locations or disabling a mouse button changes what can be done. A graphic that merely suggests “do not click” does not provide this kind of constraint.
- **Logical constraints support inference.** If a task requires five locations but only four are visible, an intelligible model can imply that another lies off-screen. Making task structure visible helps users deduce the next action and know when they are finished.
- **Cultural constraints are learned conventions.** A scrollbar's position and operation, or an arrow becoming a hand, communicate through shared learning rather than intrinsic physical necessity. Logical and cultural constraints can be ignored; physical ones cannot. Conventions develop within a community and change slowly, so novelty carries a relearning cost.

The distinction is causal, not just lexical: changing a target's appearance, changing its response, and preventing an action solve different problems. The article does not use the later term *signifier* as its organizing vocabulary; applying that term to visible cues is a synthesis rather than a quotation of Norman's 1999 model.

## Results / Admissions

There are **no experimental sample sizes, task-performance measures, or effect sizes**. Examples and Norman's account of his earlier writing support a conceptual argument, not a measured superiority ranking among constraints or cues.

He recommends observing real people doing real activities in their normal environments to establish whether conventions are shared. He cites Nielsen's claim that **three to five people** often provide enough practical data, but does not test evaluator coverage or establish that number as a universal sample-size rule here. His preference for concrete physical controls over abstract commands is explicitly a personal position, not a result.

The article contains a terminological tension: p. 40 first describes displays advertising affordances as “perceived affordances,” then says a graphical depiction suggesting action is **neither real nor perceived affordance**, but symbolic communication. Read this as an unresolved boundary between the user's perceived possibility and the visual convention producing it, not as a perfectly stable definition of every screen cue.

## Analyst Takeaways

1. **Diagnose the missing layer before changing the interface.** An available action can be unrecognized; an obvious action can be unavailable; a response can be opaque. Better decoration cannot repair an absent or incoherent behavior model.
2. **Do not mistake familiarity for physical inevitability.** Screen conventions work because people have learned them. Preserve useful shared expectations unless the benefit of change justifies relearning, and establish that familiarity with users rather than designer consensus.
3. **Communicate meaningful consequences, not mere clickability.** The useful question is whether the user anticipates an action and outcome, not whether the object resembles a button in isolation.
4. **Treat constraints as different strengths of guidance.** Prevention, inference, and convention should not be presented as interchangeable safeguards. A cultural prohibition is not an enforced boundary.

## Questions and Limitations

- The examples describe late-1990s mouse-and-keyboard screens. The conceptual distinction transfers, but claims about designers' limited control over real affordances need reconsideration for touch, tangible interfaces, and other input modalities.
- There is no comparative evidence establishing which cue or convention works for a given audience. The essay itself insists observation is necessary.
- Calling conventions both “arbitrary” and “not arbitrary” is clarified by context: they are not physically necessary, but their development and cognitive fit are not random. The essay's strongest contribution is this distinction, not a blanket prohibition on innovation.
- The PDF states **“COPYRIGHT © 1999 DONALD A. NORMAN. ALL RIGHTS RESERVED.”** No redistribution grant appears; the dossier therefore links to the publisher DOI rather than a public archive copy.

## Vault Ideas Extracted

- [Signifier Strength](/vault/signifier-strength.md) — Separates actual action possibilities, perceived possibilities, and learned visual communication, including the essay's terminology tension.
- [Consistency and Convention](/vault/consistency-and-convention.md) — Explains why shared conventions constrain behavior and why their usefulness must be established with users.
- [Error Prevention and Recovery](/vault/error-prevention-and-recovery.md) — Distinguishes enforced physical prevention from weaker logical and cultural guidance.
