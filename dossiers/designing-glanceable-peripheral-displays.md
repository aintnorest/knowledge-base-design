---
type: Study Note
title: Designing Glanceable Peripheral Displays
description: A literature-informed exploration of 30 email-display designs and interviews with nine designers proposes meaningful, abstract, distinct, consistent encodings for quick interpretation, but does not measure glance time or multitasking performance.
resource: https://www2.eecs.berkeley.edu/Pubs/TechRpts/2006/EECS-2006-113.html
source: https://www2.eecs.berkeley.edu/Pubs/TechRpts/2006/EECS-2006-113.html
tags: [attention, visual-perception, interaction-design, digital-interfaces, user-research, taxonomy]
timestamp: 2026-10-12T23:51:52Z
---

# Designing Glanceable Peripheral Displays — Study Notes

**Authors**: Tara Lynn Matthews, Jodi Forlizzi, and Stacie Rohrbach; the paper byline shortens the first name to Tara Matthews.  
**Published**: University of California, Berkeley, EECS Technical Report **UCB/EECS-2006-113**, September 7, 2006.  
**Status**: Institutional technical report, not identified as a peer-reviewed conference or journal publication. Read the complete supplied **11-page PDF**: cover and copyright pages plus nine numbered paper pages, including Table 1 and Figures 1–6. The EECS landing page confirms the title, authors, report number, date, and linked PDF; no DOI is supplied.  

## What It Is

An exploratory account of **glanceability**: how quickly and easily someone can understand displayed information with low cognitive effort **once attending to it**. It offers a taxonomy of visual variables and four initial design principles, derived jointly from literature, the authors' design experience, an email-display case study, and designer interviews.

The source distinguishes **peripheral display use** from **notification**. In its Activity Theory framing, a peripheral display supports an ongoing activity at the low-cost operation level; a notification demands focal attention at the action level. A display can sit at the edge of a workspace yet be inspected with foveal vision. Glanceability therefore is not a synonym for detecting an event without looking at it.

## Problem and Motivation

Ambient displays often communicate attractive abstractions without evidence that people can understand them rapidly or that the information is desirable. Adding a visual feature does not establish that its mapping is learnable, that its states are distinguishable, or that it supports the user's immediate question.

The authors focus on **interpretation after attention has shifted**, leaving notification timing and attention capture largely outside the project. They want meaningful information to require less departure from primary work. Claims about saving human or financial resources motivate the work; no economic or workflow savings are measured.

## Mechanism as an Idea

### Match the encoding to the information structure

The authors distinguish three information types, inspired by Wurman's *Information Anxiety 2*, developed through the email exploration, and reinforced by interviewees:

| Information type | Proposed visual treatment | Boundary supplied by the case study |
|---|---|---|
| **Ordered**: a continuum such as amount or priority | Vary size, position, lightness, number, or another genuinely ordered dimension. | Do not manufacture priority merely because a visual variable has an order. |
| **Unordered, finite groups**: a small set of categories | Use recognizable images, icons, shapes, or distinct category colors without an unintended ranking. | A limited arbitrary mapping may be learnable; the report does not test how many categories or how much training is acceptable. |
| **Unordered, effectively infinite groups**: arbitrary message contents or very large sets of names | Retain text, or summarize/categorize the information before attempting a compact representation. | An enormous visual codebook would itself demand learning and recall; the claim that text is most effective is an argument, not a measured text-versus-icon comparison here. |

The email designs exposed a semantic failure: assigning personal > work > administrative > spam a fixed hierarchy can conflict with what matters now. An administrative message may be the one a person urgently awaits. **Perceptual discriminability and correct meaning are separate requirements**: four dots can be easy to distinguish while conveying an unjustified priority.

### A taxonomy is an exploration aid, not a validated ranking

The literature-informed taxonomy separates **four categories**: static variables affecting the whole display, static variables affecting its parts, temporal variables, and other modalities. Examples include hue, intensity, value, transparency, blur/clarity, resolution, location, amount, proximity, hierarchy, size, shape, orientation, duration, motion, sound, and touch. The paper's own empirical exploration is visual; listing modalities does not mean they were tested.

Table 1 illustrates **six examples**, including a gear shift, two periodic-table displays, InfoCanvas, a poetic garden, and IC2Hear. They are a **portion** of the collected displays, not a reported complete sample. Figure 1 shows how existing forms communicate: InfoCanvas maps quantities into familiar pictorial objects; IC2Hear represents sounds visually; gear position supplies state while numbers provide redundant information. These are illustrative analyses of existing designs, not new participant evaluations by this report.

The literature review cites **29 references**, spanning visual search, graphic design, human factors, ambient displays, and email workflow. Bertin, Dondis, Kosslyn, and Tufte inform the visual-variable vocabulary. Cited visual-search research supplies a rationale for distinctiveness and interaction between top-down goals and bottom-up salience; proximity compatibility and ecological display theory motivate information organization. The authors suggest applying these accounts to glanceability, not that those studies experimentally validate this report's email designs. No systematic search, screening counts, pooled effect, or complete display-corpus size is given.

## Case Study and Interview Evidence

The authors created **30 versions** of an email peripheral display. Each illustrated **four messages** from spam, administrative, work, and personal senders, with sender and subject text. A visual variable represented the sender group; some variables had multiple implementations, such as coloring text versus its background. The goal was to help decide whether to read or ignore a message, but participants did not perform a timed read/ignore task.

A cited email-workflow survey supplies a content rationale: **five of its ten most important email-priority factors** concern senders. That is prior research, not the present sample, and sender group is not the same as each person's current message priority. The authors acknowledge that selecting other information could change the display's usefulness.

**Nine experienced designers** evaluated the variations in interviews: **three professional designers, two design professors, and four graduate students with prior design experience**. Reported expertise overlaps: **five interaction, four graphic, two information, one typographic, one branding, and one print design**. These are not separate participant groups.

Interviewees first discussed existing displays, then sketched a glanceable email display, inspected the authors' variants, rated each on **1 very poor to 7 very good glanceability**, explained their ratings, and offered general principles. This is expert elicitation and design critique, not an experiment with representative email users under divided attention. No primary-task performance, response accuracy, gaze duration, learning curve, delayed recall, or physiological cognitive-load measure was collected in the reported evaluation.

## Results / Admissions

### What the designers preferred

- **Representative images were highest-rated**, followed by **colored message backgrounds** and **multiple dots**. Figure 6's approximate plotted values are **5.6, 4.8, and 4.4**, respectively; these are graph readings, not tabulated exact means or statistically established advantages. The chart reports no uncertainty intervals or significance tests.
- Figure 2 maps sender categories to a spam can, calculator, briefcase, and lock. Interviewees valued a picture's compact conceptual meaning but still asked for stronger visual differences and sometimes more abstraction. A familiar-looking image is not automatically a uniquely interpretable category code.
- Figure 3's colored backgrounds were judged easier to recognize than smaller colored elements. Interviewees attributed this to a larger area and visible distinction, while warning that the depicted green and blue were too similar. Another wanted comparable saturation so no unordered sender category acquired undue prominence. This is designer reasoning about composed designs, not an isolated causal effect of mark area or saturation.
- Multiple dots were considered easy to distinguish even if only one message appeared, yet interviewees objected to their artificial prioritization. A favorable perceptual rating did not validate the information model.
- **Bar orientation was least popular**, approximately **1.5** in Figure 6. Designers cited a weak semantic connection to sender category and difficult discrimination. Small transparency differences also received criticism: comparing subtly faded dots was difficult, particularly in isolation, and could fail to reduce the need to read the message.
- The authors argue that unrestricted content should stay out of a peripheral display unless categorized or summarized. Interviewees requested simple, clear, low-detail information. This is a content-selection recommendation, not proof that no detailed peripheral display can work.

### Provenance of the four principles

The authors explicitly synthesize all inputs; the report does **not** assign one isolated experiment to each principle. The most direct support is:

| Principle the source recommends | Direct case-study / interview basis | Literature or conceptual contribution | What remains untested here |
|---|---|---|---|
| **Match user expectations** | Designers preferred semantically meaningful images and objected to arbitrary bar orientations and an imposed sender hierarchy. | Graphic-design accounts of relating form to content, plus the information-type grouping inspired by Wurman. | Lower learning effort, universally shared mappings, and task-appropriate comprehension. |
| **Use abstract representations** | Interviewees requested minimal detail; all regarded the representative-image design as effective/glanceable, with suggestions to exaggerate recognizable features. | Authors' prior display-design experience and graphic-design rationale for selecting essential information. | Whether abstraction preserves enough information, outperforms text, or improves multitasking. |
| **Make visuals distinct** | All interviewees emphasized differences from other elements and backgrounds; critiques addressed orientation, transparency, size, blur, and other subtle variations. | Cited visual-search and pop-out research supplies a conditional perceptual rationale; the taxonomy catalogs available channels. | Detection and interpretation thresholds, reliable category capacity, accessibility, and actual attention cost. |
| **Maintain consistency** | Designers supplied examples of ambiguous magnifying-glass meanings and stable icon families with one meaningful variation. | The authors generalize from interviews and experience; no principle-specific causal study or dedicated literature citation is attached to this final rule. | Measured reduction of disorientation or processing time from stable placement, behavior, or color. |

The conclusion calls these **initial principles**. A lab study of email-design effects on user performance in multitasking is described as **currently underway**, with results intended to refine the principles. That planned study is not evidence reported in this technical report and is not an independent replication established here.

## Analyst Takeaways

1. **Design for the glance's question before selecting its visual channel.** “Which category is this?” and “Which message deserves attention now?” are not interchangeable. A fast answer to the wrong question is not glanceability in service of the task.
2. **Do not confuse noticing with understanding.** [Preattentive Features](/vault/preattentive-features.md) and [Motion Cues: Attention and Distraction](/vault/motion-cues-attention-and-distraction.md) concern conditional search or event detection; this report adds the need for low-effort interpretation once the display is inspected.
3. **Evaluate a state alone as well as beside alternatives.** A barely different shade or orientation may be sortable in a comparison sheet yet hard to identify in a single live message. The interview critiques support this concern, not a tested universal discrimination threshold.
4. **Keep unordered categories distinguishable without falsely ranking them.** [Color Coding for Status](/vault/color-coding-for-status.md) must preserve meaningful distinction and avoid accidental emphasis, not simply maximize brightness everywhere.
5. **Treat expert ratings as hypotheses for behavioral evaluation.** These critiques identify plausible semantic and perceptual failures. They do not establish faster decisions, less interruption, or better sustained work.

A glanceable summary of software automation or AI-agent status could expose a small number of meaningful states while leaving details available for deliberate inspection. This is an **extrapolation** from email displays and design interviews, not evidence that a compact agent dashboard improves supervision or appropriately communicates uncertainty. [Visibility of System Status](/vault/visibility-of-system-status.md) still requires an intelligible account of what the system is doing; compactness must not replace correctness.

## Questions and Limitations

- The evaluation is **nine designers' judgments of 30 author-created variants**, not measured performance by end users. The report provides no recruitment detail, interview duration, coding/reliability procedure, rating-order counterbalancing, raw ratings, exact tabulated means, variability, or inferential statistics.
- The paper says variants produced “significantly different results,” but reports no statistical test. Treat that wording as qualitative variation, not demonstrated statistical significance. Figure 6 presents **26 labeled bars** despite the stated **30 versions**; no aggregation, omission, or exclusion explanation is given.
- Although each version is described as focusing on one variable, changing a text color into a colored background also changes area and emphasis. The design critique cannot cleanly isolate a visual-channel effect from its specific implementation.
- The statement that finite categories can use “colors of similar hue” sits awkwardly beside interviewees' request for “distinctly different colors” and their complaint that green and blue are too similar. The defensible principle is distinct categories without an implied ranking, not a prescription that hues should be similar.
- The definition excludes attention capture, yet the discussion and final distinctness principle invoke standing out and drawing the eye to important/new information. This is a boundary tension: salience can aid selection during a glance while also capturing attention outside it. The report does not measure or separate those effects.
- General claims about reduced learning effort, improved identification, and consistency reducing processing time are recommendations and inferred mechanisms. No glance-duration threshold, cognitive-effort estimate, primary-task disruption effect, or long-term learning result validates them here.
- The illustrated IC2Hear application concerns deaf users, but this report recruits no disabled-user subgroup and tests no color-vision, low-vision, or nonvisual-access needs. Calling the proposed principles “accessible” in the introduction is an aspiration, not demonstrated accessibility.
- The four sender categories and chosen metaphors are context-specific. The source does not establish universal semantics for colors or icons, a safe number of categories, or a general priority model. No independent replication or results of the then-planned lab study are established from this version.
- **Identifier evidence**: the PDF supplies a report number and institutional URL, not a DOI. The HTTPS EECS landing page returned **HTTP 200** without redirection, identifies this exact report, and has no report-specific `rel="canonical"` element in its HTML head. It is therefore the canonical URL used for the source key, rather than a checksum or the linked PDF's location.
- **Redistribution evidence**: the copyright page states **“Copyright © 2006, by the author(s). All rights reserved.”** It permits personal/classroom copies under conditions, but explicitly says **“To copy otherwise, to republish, to post on servers or to redistribute to lists, requires prior specific permission.”** That is not permission to put the raw report in a public repository; use the private archive and retain the canonical URL.

## Vault Ideas Extracted

- [Glanceable Peripheral Displays](/vault/glanceable-peripheral-displays.md) — Proposes separating attention capture from rapid interpretation and matching a compact encoding to information structure; evidence is a literature-informed case study and nine designers' judgments, not a timed multitasking benefit.
- [Preattentive Features](/vault/preattentive-features.md) — Adds the boundary that distinctive visual selection is not sufficient for meaningful, learned interpretation after a glance.
- [Color Coding for Status](/vault/color-coding-for-status.md) — Adds qualitative evidence for distinct, non-ranked category colors, mark-area effects in composed examples, and problems identifying subtle differences in isolation.
- [Visibility of System Status](/vault/visibility-of-system-status.md) — Adds the need to answer the user's state question with compact, meaningful representations rather than arbitrary codes or an invented priority hierarchy.
