---
type: Study Note
title: "Designing Empty States in Complex Applications: 3 Guidelines"
description: NN/g recommends truthful status, contextual learning cues, and direct task entry in empty containers, illustrated by enterprise applications but without measured comprehension, confidence, or learnability effects.
resource: https://www.nngroup.com/articles/empty-state-interface-design/
source: https://www.nngroup.com/articles/empty-state-interface-design/
tags: [interaction-design, content-design, cognitive-load, digital-interfaces]
timestamp: 2026-10-16T00:00:00Z
---

# Designing Empty States in Complex Applications — Study Notes

**Author**: Kate Kaplan.  
**Published**: Nielsen Norman Group, September 19, 2021.  
**Status**: Practitioner guidance, not an empirical study. Read the complete eleven-page supplied PDF, including its illustrated comparisons. The live page's canonical link confirms the resource URL.

## What It Is

Three uses for a content-less container: communicate system status, explain how content reaches the area, and provide a route into the relevant task. The article concerns empty panels, workspaces, favorites, recent items, alerts, and query results in complex applications. It is eligible for its explicit usability rationale, not as a collection of screenshots.

## Principles as Ideas

### Empty is a conclusion, not a loading placeholder

A blank result leaves several explanations open: work is continuing, processing failed, filters exclude everything, or nothing exists. The source recommends a brief no-results message **after processing completes**, and progress feedback while processing continues.

Its employee-management example initially says “No records” and later displays records. This is not merely missing feedback: it makes a false claim about the outcome. The source argues that people may leave before seeing the data or lose confidence in the system. These consequences are reasoned warnings, not measured rates.

### Explain how the area becomes useful

Contextual help can connect a feature to a task the person is already trying to perform. A favorites list explains that starring an item puts it there; a recent-items area explains that opening content creates its history. The source calls such in-context cues “pull revelations,” contrasting them with forced initial tutorials that must be remembered until relevant.

The alerts comparison shows why populated designs alone are insufficient: controls that make sense beside existing alerts teach little when the panel is blank. The article recommends explaining the function and how to begin, but does not distinguish every configured-but-quiet alert state from an unconfigured one; that distinction requires additional guidance.

### A next-step description is not a route into the task

An instruction to send a request does not help someone locate the request function. The source prefers a direct pathway where appropriate, with concise instructions or optional further explanation. Illustrated alternatives include creating an alert and either connecting real log sources or exploring demo data. These are examples of task entry, not evidence that every empty area needs multiple actions.

## Evidence / Admissions

- **Illustrated contrasts:** an empty log query versus an explicit completed no-results message; a premature no-records message versus its later populated state; populated versus blank alerts; favorites and recent-items learning cues; an instruction without a route versus direct entry and documentation; real-data versus demo-data entry.
- **No reported experiment:** no recruited participants, task protocol, sample size, measures, effect sizes, confidence intervals, or replication results are supplied. Screenshots show the proposed design differences, not their effects on users.
- **Claims versus evidence:** the article says in-context cues are generally more successful than forced tutorials and predicts greater confidence, learnability, and feature discovery. It supplies rationale but no comparative results establishing those claims in this article.

## Analyst Takeaways

1. Treat loading and a completed empty result as different system claims; an empty-looking container does not establish either one.
2. Explain the actual source of future content rather than merely restating that none is present.
3. Provide an intelligible route when a useful action exists; naming a task without locating it can leave the person stuck.
4. Inspect unconfigured and no-results states as deliberately as populated ones. Do not turn every absence into an error or a compulsory onboarding opportunity.

## Questions and Limitations

- This is guidance grounded in examples, not a controlled demonstration of reduced retries, increased trust, better memory, or task completion. Independent replication is not reported and is not applicable to these recommendations as though they were experimental findings.
- The broad advice against totally blank states does not establish how much explanation a small or repeated area needs, whether an optional section should be removed, or how nonvisual users encounter the message.
- No quantitative inconsistency is present because no quantitative study results are supplied. The unconfigured-versus-quiet alerts ambiguity should not be silently resolved by assuming all empty alert panels require setup.
- **Redistribution evidence:** the supplied footer states “Copyright © 1998–2026 Nielsen Norman Group, All Rights Reserved.” No explicit redistribution grant appears; the unchanged PDF is archived privately.

## Vault Ideas Extracted

- [Empty States](/vault/empty-states.md) — Supplies truthful no-results feedback, contextual explanations of how content arrives, and routes into related tasks, with guidance-only evidence.
- [Visibility of System Status](/vault/visibility-of-system-status.md) — Adds the distinction between work still loading and a completed request with no matching content.
