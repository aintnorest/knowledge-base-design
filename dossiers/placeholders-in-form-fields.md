---
type: Study Note
title: Placeholders in Form Fields Are Harmful
description: NN/g argues that disappearing labels and hints obstruct recall, checking, and error repair and that floating labels only partially mitigate these problems, but reports no study samples or effect estimates for its usability and accessibility claims.
resource: https://www.nngroup.com/articles/form-design-placeholders/
source: https://www.nngroup.com/articles/form-design-placeholders/
tags: [forms, cognitive-load, cognitive-accessibility, accessibility, content-design, digital-interfaces]
timestamp: 2026-10-14T21:32:03Z
---

# Placeholders in Form Fields — Study Notes

**Authors**: Katie Sherwin; Nielsen Norman Group (NN/g).  
**Published**: May 11, 2014; last reviewed September 10, 2018; supplied page print captured October 14, 2026.  
**Status**: Research-informed practitioner guidance, not a peer-reviewed study report. Read the complete eight-page print and substantive form illustrations, and opened the live article to recover material obscured by the print's repeated privacy overlay. Its canonical link matches the resource URL.

## What It Is

A critique of using in-field text as the only label or as the only location for essential entry instructions. It distinguishes **field identity**, **supplementary examples**, and **persistent requirements**, rather than treating all text inside a control as the same design choice. The source is eligible because it supplies cognitive, perceptual, and accessibility rationales and refers to first-party usability observations.

## Principles as Ideas

### Persistent identity supports entry, checking, and repair

A disappearing label makes the person remember what the field asks for after typing begins. Interruption, switching tabs, fetching documents, and mobile distraction increase the importance of resuming with visible context. Recovering the instruction may require deleting entered text and sometimes leaving the field, which discards work merely to recover information.

The same disappearance makes review harder: a filled or autofilled form no longer visibly identifies what each answer belongs to. After validation fails, a person may need to reconstruct those instructions to understand and correct the error. These are distinct stages of the form journey, not just an initial-entry inconvenience.

The article gives an important boundary: a familiar one- or two-field form imposes less memory demand than a complex or rarely used form. Even login can remain ambiguous if the disappeared label distinguished username-only from username-or-email entry.

### Occupied appearance can hide an invitation to act

The source says eyetracking shows empty fields attract attention and that people can mistake placeholder content for an already-entered default, skipping the control. It separately criticizes implementations in which the hint is editable content that must be removed, or dimmed content whose behavior is unfamiliar. A real default, a temporary visual hint, and an editable instruction are not interchangeable interaction states.

Keyboard traversal creates another problem when in-field information disappears on focus: the person may move into the field before studying its hint. This concerns focus-triggered implementations, not every modern placeholder's behavior.

### Essential hints should survive entry

An external label is an improvement over placeholder-only identity, but it does not rescue an essential instruction that still disappears. The article recommends persistent external hints as well as persistent labels. Its diagrams compare placeholder-as-label, external-label-plus-placeholder, floating labels, and external-label-plus-external-hint; these illustrate different persistence models rather than measured ranking effects.

### Floating labels address memory, not every affordance problem

A floating label moves out of the input area but remains visible during entry. NN/g credits it with mobile space savings and addressing the first four listed pitfalls: memory, checking, repair, and focus-triggered disappearance. The initially occupied-looking field can still be less noticeable or appear already completed, and accessible identification may still fail depending on implementation.

The article's preference for external labels and hints when space permits is a reasoned recommendation, not a controlled comparison of all floating-label variants.

## Evidence / Admissions

- **Usability observations:** NN/g says testing continually finds placeholders harmful, that users sometimes skip apparent defaults, and that unfamiliar dimming can produce failed deletion attempts. It gives no participant count, demographics, recruitment, field tasks, test dates, observed frequencies, or quantitative error/completion outcomes.
- **Attention claim:** eyetracking is cited at the topic level rather than with an inspectable experiment, sample, fixation measures, or effect estimate. The article does not establish a numerical detection penalty for in-field text.
- **Accessibility rationale:** low-contrast hints, extra recall and deletion demands, and inconsistent screen-reader exposure can disproportionately burden people with visual, cognitive, or motor impairments. No disabled-user sample, assistive-technology/browser matrix, or measured group difference is supplied.
- **Illustrations:** password-field diagrams and a shipping-form floating-label example show the stated mechanisms, not causal outcomes. No randomized comparison, confidence interval, conversion uplift, or independent replication is reported; repeated testing is asserted without auditable study details.

## Analyst Takeaways

1. **Assess the filled state, not only the empty form.** Entry requirements still matter while checking autofill, returning after interruption, and correcting errors.
2. **Preserve the information needed to interpret work.** A persistent label is insufficient if the decisive format or eligibility instruction disappears.
3. **Separate label persistence from apparent completion.** Floating labels can preserve context while retaining a control-discovery problem.
4. **Treat compatibility claims as dated.** The durable model is reliable accessible identity and instruction access, not a permanent claim about what all current browsers or screen readers support.

## Questions and Limitations

- Strong language such as “impossible” to check work and “business-killing disaster” is not backed by quantified outcomes here; the source itself acknowledges familiar short forms are less demanding.
- The initial definition says hints typically disappear when typing; later keyboard guidance addresses disappearance on focus, and editable/dimmed variants behave differently again. These are heterogeneous implementations, not one uniform treatment; do not assign every failure to every placeholder.
- Browser styling and screen-reader claims were last reviewed in 2018 and need current compatibility evidence before being treated as present-day universal constraints.
- The PDF's privacy overlay repeatedly obscures text and parts of the first and final diagrams. The live article resolves the text and image descriptions; the archived print is retained unchanged. No numerical inconsistency was found.
- **Redistribution evidence:** the saved footer states “Copyright © 1998–2026 Nielsen Norman Group, All Rights Reserved” and links its Copyright & Reprint Policy. No open digital-redistribution grant appears; keep the intact PDF privately and cite the canonical URL.

## Vault Ideas Extracted

- [Recognition over Recall](/vault/recognition-over-recall.md) — Adds persistent field identity and essential hints as memory support across entry, interruption, autofill review, and repair.
- [Error Prevention and Recovery](/vault/error-prevention-and-recovery.md) — Adds the loss of correction context when filled fields hide their requirements, without a quantified recovery effect.
- [Signifier Strength](/vault/signifier-strength.md) — Adds the apparent-completion ambiguity of in-field text and explains why floating-label persistence does not fully restore an invitation to enter data.
