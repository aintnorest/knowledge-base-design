---
type: Study Note
title: Carbon Empty States
description: Carbon distinguishes absent data, action outcomes, and unavailable data, recommending proportionate contextual guidance and avoiding empty screen-reader structure without reporting pattern-specific user studies.
resource: https://www.carbondesignsystem.com/building-blocks/core/patterns/empty-states
source: https://www.carbondesignsystem.com/building-blocks/core/patterns/empty-states
tags: [content-design, interaction-design, design-systems, assistive-technology, accessibility, digital-interfaces]
timestamp: 2026-10-16T00:00:00Z
---

# Carbon Empty States — Study Notes

**Author**: IBM Carbon Design System.  
**Published**: Living pattern guidance; printed last update August 11, 2026.  
**Status**: Design-system guidance, not a user study. Read the complete twenty-page supplied PDF, including diagrams and examples. The live response has no canonical link; the final HTTPS URL after redirects is the resource URL above.

## What It Is

A model for explaining missing content in context, with enough information to support the next useful decision. It distinguishes first-use absence, outcomes of user actions, and data that exists but cannot be displayed. It also considers when a primary feature warrants deeper education rather than a basic empty-state message. These rationales make the source eligible; its layout and component specifications are not the knowledge being ingested.

## Principles as Ideas

### Diagnose the reason for absence

- **No data yet:** explain what belongs in the space and how it can arrive.
- **An action's outcome:** explain an empty search result or confirm completion, and give relevant follow-up when useful.
- **Data unavailable:** explain access, system, or configuration barriers with enough specificity to identify an available remedy or the circumstances under which data will appear.

The source explicitly separates **alerts not configured** from **configured alerts with nothing triggered**. The latter may need only a short no-alerts statement: no further task is required. Absence is not intrinsically a problem, and a call to action is optional rather than obligatory.

### Match explanation to importance, complexity, and repetition

Carbon argues that more content has a cognitive cost. Basic, brief messages suit simpler situations and secondary features. More substantial explanation is reserved for important or complex first-use situations, especially when evaluation indicates that people do not understand the feature.

Small areas may warrant text alone. Repeating illustrations across several empty dashboard areas can dilute their impact; repeated strong action emphasis also competes for attention. The durable principle is proportionality, not a particular visual recipe or component choice.

For actionable situations, prioritize a relevant next step. A direct route reduces the gap between explanation and action; pointing to an existing action elsewhere can instead teach where the recurring task lives. Do not fill the message with unrelated features or unfamiliar product vocabulary.

### Replace empty structure, not its explanation

The guidance recommends replacing an empty table, including redundant headers and footer, with its contextual message rather than making a screen-reader user traverse the empty table before learning that it contains nothing. This is a nonvisual navigation rationale, not a recommendation to erase all indication that the feature exists.

Decorative illustration should not add nonvisual noise or carry information omitted from the text. The source cites Web Content Accessibility Guidelines with a 2018 reference, but names no success criterion or conformance level. Its dated preference between image-hiding techniques is not a universal compatibility finding and is not reproduced here as implementation instruction.

### Education has maintenance and fallback costs

For primary features, richer contextual explanation, optional onboarding, or safe starter content may help people begin. The source notes that images and localized content need maintenance, optional tours do not replace a usable baseline, and deletable starter content requires a fallback empty state. The rationale is learning through contextual explanation or low-consequence exploration, not compulsory education for every absent item.

## Evidence / Admissions

- The diagrams illustrate small and large contexts, direct task entry versus pointing to an existing action, no-result recovery, configured-but-quiet alerts, a system failure, extended explanation, optional onboarding, and starter content. They demonstrate the proposed model, not measured benefits.
- External references include Nielsen's error-recovery heuristic and error-message guidance, application-design and no-results guidance, Tidwell's rationale for safe exploration, and WCAG. Their empirical methods and effects are not reproduced in this pattern.
- **No original evaluation:** no participants, task protocol, sample size, comprehension or completion measures, effect sizes, or independent replication results are reported. The page suggests using testing and metrics to decide whether extra explanation is needed; it does not report such a test itself.

## Analyst Takeaways

1. Decide what the absence means before deciding how much copy or illustration to add.
2. Keep a quiet, successfully configured state distinct from missing setup and failure; do not invent corrective work.
3. Count explanation and repetition as attention costs. More help is not automatically more useful help.
4. Communicate the empty outcome without forcing nonvisual users through structure that has no content.
5. Treat richer education as a conditional response to complexity or observed misunderstanding, with an ongoing maintenance obligation.

## Questions and Limitations

- No measured optimum length, illustration effect, screen-reader navigation savings, engagement increase, or learning advantage is established. Applicability to a particular audience remains to be evaluated.
- The page's broad aim to provide a solution path is qualified by its explicit allowance for states with no useful next step. Preserve that exception rather than attaching an action to every message.
- The anatomy illustration numbers five items, while the accompanying enumerated text restarts numbering for its last two items. This editorial inconsistency does not change the model. There are no quantitative study results to reconcile.
- The accessibility passage makes a comparative support claim about image-hiding techniques without browser, assistive-technology, version, or test evidence. Its WCAG reference is dated 2018 but does not identify a criterion; do not treat it as a current conformance audit.
- **Redistribution evidence:** the supplied footer states “Copyright © 2026 IBM” and links Terms of use. The linked [IBM terms](https://www.ibm.com/legal/terms), dated November 20, 2020, grant limited access/display and prohibit mirroring content in another website or medium absent a separate licence. No separate redistribution grant appears in the supplied pattern; the unchanged PDF is archived privately, irrespective of software licensing elsewhere in the design system.

## Vault Ideas Extracted

- [Empty States](/vault/empty-states.md) — Adds reason-sensitive, proportionate messages, a no-action-needed exception, and the nonvisual cost of empty structure.
- [Visibility of System Status](/vault/visibility-of-system-status.md) — Distinguishes no data yet, action outcomes, configured quiet states, and data unavailable for a known reason.
