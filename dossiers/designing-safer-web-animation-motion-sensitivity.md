---
type: Study Note
title: Designing Safer Web Animation For Motion Sensitivity
description: Val Head's practitioner guidance and two first-person accounts identify large, unexpected spatial motion as an accessibility barrier and recommend purposeful motion and user control, without validating safe sizes, speeds, or alternatives.
resource: https://alistapart.com/article/designing-safer-web-animation-for-motion-sensitivity/
source: https://alistapart.com/article/designing-safer-web-animation-for-motion-sensitivity/
tags: [motion, accessibility, interaction-design, digital-interfaces]
timestamp: 2026-10-16T00:00:00Z
---

# Designing Safer Web Animation For Motion Sensitivity — Study Notes

**Author**: Val Head.  
**Published**: A List Apart, September 8, 2015. The live page records an April 30, 2020 modification date, not a new study date.  
**Status**: Practitioner article informed by conversations with two named people who experience symptoms, not a controlled experiment. Read the complete 15-page PDF print, including comments and illustrations; the live page's canonical link confirms the resource URL. The print preserves video-player placeholders rather than the motion of the embedded demonstrations.

## What It Is

An account of how interface animation can prevent people from using content through dizziness, nausea, headaches, or symptoms that persist after the animation ends. Its eligible contribution is first-person experience and a reasoned accessibility model: motion has different consequences depending on its spatial scale, direction, apparent travel, predictability, and controllability. This is more than an aesthetic objection to animation.

## Principles as Ideas

### Spatial motion is not one uniform exposure

Head identifies three risk dimensions: **movement relative to available screen space**, **direction and speed mismatched with the person's action**, and **perceived distance traveled in virtual space**. A full-screen wipe, exaggerated parallax, unexpected horizontal travel during vertical scrolling, or a rapid apparent journey through depth can be problematic even if the underlying content is useful.

The source predicts that a small rotating button is less likely to cause trouble than a screen-wide transition, and that non-moving opacity, color, and blur changes are unlikely to be problematic. These are guidance judgments, **not measured safety guarantees**. They do not establish safe dimensions, trajectories, contrast changes, or pulse rates.

### Preserve purpose while allowing a less moving presentation

Head recommends giving each animation a design purpose, explaining substantial motion before someone encounters it, and offering a way to reduce or turn off motion across the experience. Predictability and control matter because merely reading an ordinary article should not unexpectedly expose someone to substantial movement.

The article argues that animation can externalize a path between states, support spatial understanding, and reduce the need to mentally reconstruct changes. It links outside research on learning, decision-making, and change blindness, but supplies no participant counts or effect estimates from those papers. Those claimed benefits do not establish that every transition is needed, or that its benefits outweigh symptoms for affected users.

## Experiences / Admissions

- **Informants**: Greg Tarnoff, an accessibility and UX consultant who experiences vertigo and migraines, and Craig Grannell, a writer/editor who experiences dizziness. These are two named conversational accounts; no recruitment procedure, structured interview protocol, or clinical diagnosis verification is reported.
- **Encountered content**: Tarnoff identifies large moving areas and different foreground/background speeds as troublesome. Grannell describes a carousel's return to the first image, parallax-like product content, and an unexpected horizontal shift during downward scrolling. Lack of pause/stop control makes the carousel unavoidable.
- **Variation**: other examples were only mildly annoying or caused little trouble beyond an opening animation. Head says neither informant wanted every interface animation eliminated. This supports individual variation, not a prevalence estimate or universal tolerance hierarchy.
- **Measures and effects**: qualitative reports of symptoms and annoyance; no standardized severity scale, exposure duration, task-completion measure, effect size, controlled alternative comparison, or replication is supplied.
- **An important counterexample in the comments**: Tarnoff says the article's own static header illustration, with doubled outlines suggesting intermediate movement, triggers him; illustrator Sue Lockwood also reports difficulty looking at it for long. The image visibly depicts successive running/falling poses. This qualifies any simple assumption that removing literal animation necessarily removes every trigger.
- **Illustrated proposal**: the browser notification mockup asks whether to reduce animation. It is a proposed form of user control, not an evaluated intervention. The browser-level discussion reflects 2015 capabilities and aspirations.

## Analyst Takeaways

1. **Separate physical symptoms from annoyance and distraction.** Finding motion irritating is not the same outcome as becoming unable to use the interface.
2. **Review apparent travel, not just object size.** Depth effects and movement inconsistent with a scroll action can imply a large journey without a large moving object.
3. **Preserve information when reducing movement.** A non-moving change or immediate state replacement may retain meaning without replaying the spatial path; this is a design inference from the guidance, not a tested treatment effect.
4. **Make control available before an avoidable exposure.** An explanation or switch that can be reached only after the triggering transition is a weak accommodation.

## Questions and Limitations

- Two accounts cannot estimate how often symptoms occur, which diagnoses predict them, or which motion every person will tolerate. The cited approximately eight million adults with balance problems and 2.4 million with dizziness are background figures, not measured prevalence of web-animation sensitivity or additive counts established by this article.
- There is no experiment on small looping activity indicators, no safe pulse rate, and no comparison of reduced-motion treatments. First-person reports of a triggering static illustration limit blanket claims about non-moving presentation.
- The article mentions epilepsy and migraine sensitivity but does not establish seizure-safe flashing thresholds. Its tentative reassurance about blur must not override later standards commentary: the archived WCAG 2.2 animation definition includes an erratum withdrawing blur's categorical exclusion.
- No numeric results contradict one another; the important tension is between broad reassurance about some presentations and the variability reported in the comments. Historical examples are not claims about those products today.
- **Redistribution evidence**: the PDF footer states “Copyright © 1998–2026 A List Apart & Our Authors.” No explicit redistribution grant is present; the unchanged print is kept in the private archive, while this dossier cites the canonical HTTPS page.

## Vault Ideas Extracted

- [Motion Sensitivity and Reduced Motion](/vault/motion-sensitivity-and-reduced-motion.md) — Supplies practitioner risk dimensions, first-person variation, and the case for purposeful, predictable, controllable alternatives without claiming validated safety thresholds.
