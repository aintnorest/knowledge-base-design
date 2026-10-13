---
type: Study Note
title: Making Content Usable for People with Cognitive and Learning Disabilities
description: W3C's supplemental guidance treats independent task completion as a cognitive-accessibility goal through familiar interfaces, clear content, recoverable errors, and reduced memory demands, without making these patterns WCAG conformance requirements or uniformly validated treatments.
resource: https://www.w3.org/TR/coga-usable/
source: /archive/making-content-usable-cognitive-learning-disabilities/w3c-making-content-usable-coga.html
tags: [cognitive-accessibility, accessibility, digital-interfaces, cognitive-load, content-design, user-research]
timestamp: 2026-10-12T20:28:35Z
---

# Making Content Usable — Study Notes

**Authors**: W3C Cognitive and Learning Disabilities Accessibility Task Force (Coga TF), of the Accessible Platform Architectures and Accessibility Guidelines Working Groups; editors Lisa Seeman-Horwitz, Rachael Bradley Montgomery, Steve Lee, and Ruoxi Ran.  
**Published**: April 29, 2021; dated version https://www.w3.org/TR/2021/NOTE-coga-usable-20210429/.  
**Status**: W3C Working Group Note, informative supplemental guidance rather than a Recommendation or peer-reviewed empirical paper. Read the supplied complete single-page HTML, including user stories, all design patterns, testing guidance, ten fictional personas, glossary, mapping/policy appendices, references, and three illustrations. The saved publication calls itself work in progress and says publication does not imply W3C Membership endorsement.  

## What It Is

A model of cognitive accessibility organized around **eight objectives**: understand things and their operation; find what is needed; understand content; avoid and correct mistakes; maintain focus; complete processes without memory barriers; obtain help; and adapt the interface. User stories articulate the need, patterns suggest responses, fictional scenarios explain possible failures, and testing questions ask whether people can actually complete the task.

The document explicitly provides **guidance beyond WCAG**: following it is not required for WCAG conformance. That does not make its needs optional for the affected person. Its working definition is consequential: if disability prevents someone using the content without help, the content is not accessible to that person. Compare [Understanding WCAG 2.2](/dossiers/understanding-wcag-2-2.md), whose testable thresholds similarly do not guarantee usability for every disabled user. The Note cites the **August 2020 WCAG 2.2 Working Draft**, not the later final Recommendation.

## Problem and Motivation

Interfaces often assume the ability to learn new symbols, infer categories, decode indirect language, retain codes across screens, switch attention, and recover from repeated errors. Cognitive and learning disabilities may affect only some of these functions while leaving other intellectual and professional capabilities intact. Diagnosis is often absent, disabilities are frequently invisible, and terminology varies across cultures.

For someone with persistent memory, language, attention, numerical, or executive-function difficulties, an inconvenience for another user can prevent independent use. The document gives particular priority to health, safety, critical services, autonomy, caregiving, social participation, and work. Situational stress and unfamiliar language can produce related difficulties, but are not substitutes for testing with disabled people.

## Principles as Ideas

### Make purpose, action, and context inspectable

Familiar controls and stable placement let prior learning remain useful. Clear page purposes, persistent labels, discriminable actions, and explicit control-to-content relationships reduce the need to infer how an unfamiliar system works. Breadcrumbs and step indicators expose completed work, current position, pending steps, and important choices so a person can resume after distraction.

Findability includes comprehensible categories, visible disclosure cues, search that tolerates spelling difficulties, and prominence for users' critical tasks rather than the organization's promotions. Media should have meaningful navigable segments so losing attention does not require starting over. Availability alone is insufficient: a control may be visible yet not recognized as actionable.

### Reduce interpretation and retention demands without erasing meaning

The Note recommends common words, literal language, simple sentence structure, short topical chunks, explicit instructions, useful summaries, and adequate separation of regions. Necessary linguistic marks, understandable dates and number formats, and distinguishable foreground content support both direct reading and text-to-speech. Numerical concepts may need qualitative alternatives; other people find numbers easier than prose, so the recommendation is to **offer appropriate alternatives**, not replace all numbers with words.

Symbols can support people with language impairments, but must be familiar, associated with the content, and culturally meaningful. More icons are not automatically better: clutter can defeat the intended support. A personalized symbol vocabulary may work where a designer's supposedly universal icon does not.

### Prevent cascading failure and make recovery achievable

The recommended form model minimizes entry, accepts equivalent formats, offers valid choices, and corrects only reliably interpretable mistakes. Instructions precede the problem; feedback explains whether an action happened. Review and cancellation protect consequential commitments, and going back should preserve valid work and the original task position.

**Theoretical reversibility is not enough** if the correction journey is itself too complex. Re-entry can create a fatigue–error–re-entry cycle. Timeouts can interrupt slow reading, information lookup, or a necessary break; a last-minute extension warning may be unreadable before expiry. The Note therefore prefers avoiding unnecessary time limits and preserving safe work, while admitting security/privacy can limit retention.

### Protect attention and remove cognitive prerequisites

Short critical paths separate optional offers from required steps. Preparation information tells people what resources and effort a process requires before they begin. Unwanted motion, pop-ups, notifications, and automatic rerouting can destroy context; reminders should be chosen and controlled by the user rather than filling a calendar uninvited.

Authentication and help should not demand unaided memorization, transcription, calculation, puzzle solving, fast responses, or complex voice-menu navigation. The Note argues that inaccessible security can lead to insecure workarounds, including asking temporary caregivers to handle credentials. Security and accessibility are joint goals, not permission to weaken protection indiscriminately.

### Preserve user-selected support and test actual use

Simplification and personalization let people retain familiar symbols, presentation, and task structure. They must preserve meaning, wanted content, and working critical paths, with an understandable route back to fuller functionality. Compatibility with assistive tools matters because disabling a user's support can recreate the original barrier. Defaults still need to be readable; customization is not an excuse for an inaccessible starting point.

Section 5 recommends diverse disabled participants and peer researchers, understandable and ongoing voluntary consent, breaks and preferred environments, and safeguards against distress. Guardian consent does not replace the participant's consent. A support person's assistance should be distinguished from independent task completion. Measures include **task success, errors, completion time, and satisfaction/mood**; the questions ask for demonstrated understanding and action, not merely verbal assurances. Automated accessibility checks cannot establish these cognitive outcomes.

## Results / Admissions

### Evidence is a rationale network, not a treatment experiment

The declared foundation is [Cognitive Accessibility User Research](https://www.w3.org/TR/coga-user-research/), [Cognitive Accessibility Issue Papers](https://w3c.github.io/coga/issue-papers/), and [Cognitive Accessibility Gap Analysis and Roadmap](https://www.w3.org/TR/coga-gap-analysis/). These are linked supporting syntheses, not empirical datasets reproduced in the Note. Standards references ground compatibility, presentation, authentication, and telecommunications guidance. The change log records task-force mapping, public feedback, other working groups' review, internationalization, and plain-language revision.

Most individual patterns support recommendations through **reasoned functional explanations and illustrative scenarios**, not an identified controlled study with participants, stimuli, statistics, or a measured benefit. For example, stable labels reduce what must be remembered; retained entries prevent repeated work; accessible help avoids repeating the barrier that caused the need for help. This is consensus guidance with research-informed background, not evidence that every proposed pattern independently improves task success by a known amount.

Some passages explicitly invoke research without providing enough identification to evaluate it here:

- The whitespace pattern says spacing has been shown to ease reading and understanding, but supplies no local study sample or effect estimate.
- The implied-content pattern describes autistic people watching actors' mouths and missing facially conveyed sarcasm in a movie, without identifying a study or reporting participant counts or statistics.
- The interruptions pattern refers to research connecting interruptions/social media with depression and focusing difficulties, without a local citation or causal estimate.
- The business appendix attributes wealth/disposable-income claims to Georgia State University's Center for Mature Consumer Studies and reports seniors completing **55.3%** of attempted online tasks. It sends readers to developer resources for sources but gives no study year, sample, tasks, uncertainty, or protocol. The **$7.1 trillion** market claim is likewise not a measured result of this Note.

Do not promote these statements into individually verified empirical effects. The Note reports **no original participant experiment and no replication test** of its eight-objective model.

### Personas explain heterogeneous barriers

The **ten personas are explicitly fictional**, not ten research participants or a prevalence sample:

| Persona | Barrier illustrated and useful support |
|---|---|
| Alison, mild cognitive impairment | Changed interfaces and repeated errors undermine confidence; familiar cues, spelling/reading support, retained work, and accessible feedback help. |
| Amy, autistic computer scientist | Illogical navigation, unexpected sounds/movement, and metaphors interfere with use despite strong programming skills; literal explanations and predictable control help. |
| George, Down syndrome | Dense text and unfamiliar symbols restrict independent communication; known symbols, clear short instructions, larger targets, and undo help without requiring childish presentation. |
| Gopal, dementia | New vocabulary, disappearing instructions, and lost task context block everyday actions; familiar language, persistent cues, and direct human help matter. |
| Jonathan, dyscalculia | Quantities, relative prices, dates, and graphs can remain confusing despite competence elsewhere; meaningful non-numerical representations and summaries help. |
| Kwame, traumatic brain injury | Ambiguity, disorientation, complex search results, and unexpected route changes impose overload; clear structure, forgiving input, and predictable routes help. |
| Maria, memory loss | Hidden controls and earlier-step information become unavailable; point-of-use context and consistent recovery help. |
| Sam, hemiplegia and aphasia | Disappearing labels, dense text, ambiguous controls, and timeout/re-entry cycles reduce independence; persistent instructions, clearer language, spacing, and reading support help. |
| Tal, dyslexia and impaired coordination | Transposed credentials, image-only documents, lost entries, buried announcements, and mistaken taps compound; accessible text, saved state, prominence, and undo help. |
| Yuki, AD(H)D | Motion, unnecessary information, and opaque multi-step work disrupt focus; controllable distraction, saved stages, summaries, and navigable media segments help. |

Appendix A maps these scenarios to user stories and patterns. The mapping supplies traceability of the rationale, not causal confirmation or population coverage.

### Figures communicate principles and expose a caption mismatch

The first grouping illustration shows **24 circles in three rows**, separated into **15 and 9** by two blue bordered regions. Its alternative text describes the count but says the blue backgrounds make the groups apparent; the visible division relies importantly on the boundary/gap because both regions use the same blue. The second illustration groups four circles into two blue/white pairs: a boundary distinguishes the sets even though the adjacent white circles might otherwise group together. These are demonstrations, not experiments.

The **five-face mood selector** offers a low-language satisfaction measure. The surrounding guidance explicitly admits that faces may themselves be hard to interpret and suggests simple textual alternatives. No psychometric validity or equivalence across these response formats is established.

## Analyst Takeaways

1. **Treat independent completion as the outcome.** A conforming fragment or technically available undo is not enough if the person cannot traverse the whole task and correction path.
2. **Externalize needed context at its point of use.** Labels, prior selections, current step, consequences, and completion feedback reduce concurrent memory demands rather than requiring the person to become better at remembering.
3. **Familiarity is individual and cultural.** Stable meanings support reuse; personalized alternatives can preserve that benefit when a single common convention does not.
4. **Reduce unnecessary work, not necessary explanation.** Simplification that hides the needed action, removes meaning, or makes help hard to find can be as exclusionary as a dense screen.
5. **Bring disabled people into the evidence loop.** Failed feedback and inaccessible support can make the people most excluded disappear from the product's data. Diverse participation and observable tasks expose what automated checks miss.

## Questions and Limitations

- Numerical recommendations are **guidance, not validated universal limits**: media segments of **six minutes or less**, roughly **1,500 common words/phrases**, breaking English paragraphs above **50 words**, and **five or fewer main choices** are not accompanied by threshold-validation experiments. The simplification pattern separately describes **3–6 functions**, showing that these are contextual suggestions rather than one consistent maximum.
- Memory descriptions are internally variable: Section 2.2 says impaired working memory may hold **1–3 items**, Section 4.7 says **1–4**, and the voice-menu discussion says **1–2**, alongside an unqualified average of **seven**. They are illustrative and lack measurement conditions. Do not replace the conditional chunk account in [Working-Memory Capacity Limits](/vault/working-memory-capacity-limits.md) with a universal menu-size rule.
- Claimed links between inaccessible authentication/voice menus and reduced life expectancy are explicitly possibilities, not demonstrated causal results. Fictional emergencies and purchase failures convey stakes but do not establish incidence.
- Section 5's declaration that an objective can be considered completed after successful tests must be bounded by the participants, tasks, conditions, and versions tested. A diverse but finite sample cannot establish usability for everyone.
- The document's proposed personalization technologies are version-dependent and sometimes explicitly immature. Its durable claim concerns compatible, controllable assistance, not the continuing availability of a particular syntax or platform behavior.
- The saved page identifies the exact **2021 Note** and has `rel="canonical"` pointing to the latest-version URL. Those identify different things; the immutable saved source and dated-version link preserve what was read.
- **Redistribution evidence**: the publication says “W3C liability, trademark and permissive document license rules apply”; its license link names the **2015 software-and-document license**. The supplied **2023 Software and Document license** states: “Permission to copy, modify, and distribute this work, with or without modification, for any purpose and without fee or royalty is hereby granted”. It requires the full notice, pre-existing intellectual-property notices, and notices of modifications on distributed copies; its change note says the 2023 revision updates copyright-holder identification. The source bundle can be publicly archived with its notices and supplied license intact. The acknowledgments separately identify the MOOCAP persona contribution as **CC-BY-4.0**; that line is not a blanket license for unrelated material.

## Vault Ideas Extracted

- [Cognitive Accessibility User Needs](/vault/cognitive-accessibility-user-needs.md) — Supplies eight functional objectives and a needs-to-pattern-to-scenario model, bounded as supplemental consensus guidance rather than a universal test battery.
- [Recognition over Recall](/vault/recognition-over-recall.md) — Extends externalized context to persistent labels, prior-step information, orientation after distraction, and cognitive-accessible authentication without claiming a quantified treatment effect.
- [Error Prevention and Recovery](/vault/error-prevention-and-recovery.md) — Explains why nominal reversibility, last-minute timeout warnings, and repeated entry may still prevent independent recovery.
- [Consistency and Convention](/vault/consistency-and-convention.md) — Connects stable learned meanings and familiar layouts to cognitive access, while qualifying familiarity through culture, individual symbol vocabularies, and personalization.
