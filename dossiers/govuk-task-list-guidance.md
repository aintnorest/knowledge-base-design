---
type: Study Note
title: GOV.UK Task List Guidance
description: GOV.UK reports status tags mistaken for buttons and completed tasks obscuring unfinished work, motivating quieter completion cues and larger task targets, while explicitly leaving the redesigned component untested.
resource: https://design-system.service.gov.uk/components/task-list/
source: /archive/govuk-task-list-guidance.pdf
tags: [interaction-design, content-design, visual-hierarchy, usability-evaluation, design-systems, digital-interfaces]
timestamp: 2026-10-16T00:00:00Z
---

# GOV.UK Task List Guidance — Study Notes

**Authors**: GOV.UK Design System team, drawing on cross-government collaboration.  
**Published**: Living guidance captured October 16, 2026. Component introduced December 2023; latest listed change August 2024 is a rendering fix, not a dated guidance revision. The PDF and live page provide no separate guidance revision date.  
**Status**: Government design-system guidance based on earlier pattern research, not a peer-reviewed study. Read the complete eight-page PDF, including examples, research admissions, history and licence footer. The live canonical link matches the resource URL.

## What It Is

A model for helping people plan and resume long, complex services by seeing tasks and their current states. It qualifies because it gives a task-selection rationale, reports observed usability problems, and distinguishes a redesign from evidence that the redesign works.

## Principles as Ideas

### A task overview is for choice and resumption, not length alone

The source recommends this approach only when evidence shows people cannot or do not want to finish in one sitting **and** need choice over task order. Simplify the service first. A long but strictly ordered journey may instead need saved progress and resumption where the person stopped. The task overview is also not a record of the person's answers.

Short, clear names should describe recognizable user work. Difficulty naming a task may indicate an overcomplicated grouping. Optional explanations should be justified by user need; verbose names and hints burden screen-reader navigation. These are recommendations without measured reading or navigation effects.

### State and action are related but not identical

Each task has a name and state. Status conveys whether work remains and whether it can be started; choosing an available task enters that task. The source says the service can proceed beyond the task list once all tasks are completed. This is the source's service model, not a universal completion gate for every task tracker.

The redesign makes the whole task row an entry target. It also changes the status treatment so a descriptive state looks less like an independent button. Enlarging the target responds to where people already tried to act, but introduces a risk of accidental activation.

### Give unfinished work the stronger hierarchy

The source reports that once several tasks were completed, users had difficulty scanning for unfinished ones. It replaces uppercase status wording with sentence case and makes completion visually quieter than states requiring action. The claim is that reducing the visual competition from finished work will expose what remains; the page does not report a measured effect of that new hierarchy.

## Research Findings and Open Assumptions

- **Reported observation:** some people selected statuses believing them to be links or buttons. No number, proportion, participant profile, or task protocol is provided.
- **Reported observation:** accumulated completed tasks made incomplete tasks harder to spot. No scan-time, error-rate, or completion effect is supplied.
- **Readability rationale:** uppercase statuses are described as harder to read. This page supplies no controlled case comparison.
- **Explicit research gap:** the team says it **still needs user testing of the new component**, particularly whether whole-row targets' benefits outweigh accidental clicks, status contrast is sufficient, and suggested status wording makes sense.
- **Illustrations:** examples show quiet completed text beside highlighted incomplete states and a short task hint. These illustrate the proposed hierarchy, not observed performance.
- There is no sample size, quantitative effect size, comparison estimate, or independent replication in this source. The companion pattern points back to this same research and is not an independent corroborating study.

## Analyst Takeaways

1. **Test both false negatives and false positives in action recognition.** Missing a real action and trying to activate a static state are different signifier failures.
2. **Treat target expansion as a tradeoff.** Meeting a user's attempted click location can also increase unintended activation.
3. **Design for the partly completed list.** An empty or fully completed example can conceal the search problem of finding a few remaining tasks.
4. **Do not upgrade rationale into a validated redesign.** Research on a predecessor motivates a change; it does not establish the new design's safety or benefit.

## Questions and Limitations

- The source's unrestricted-order language should be read alongside its companion pattern, which permits prerequisites and unavailable tasks. Local dependencies need not imply an entirely fixed sequence; the component page does not explain that boundary itself.
- The claim that the new palette meets accessibility guidance coexists with an explicit open question about sufficient contrast. A stated design intention is not a reported user-testing result; the page names no specific WCAG success-criterion version for this claim.
- Neither the latest rendering-fix date nor the component-introduction date establishes the last substantive revision of the guidance.
- **Redistribution evidence**: the PDF footer states “All content is available under the Open Government Licence v3.0, except where otherwise stated” and identifies Crown copyright; no exception is stated for the guidance. Public archive attribution: **Contains public sector information licensed under the Open Government Licence v3.0.** No endorsement is implied.

## Vault Ideas Extracted

- [Task Lists and Status Vocabulary](/vault/task-status-vocabulary.md) — Adds the evidence-led scope for task overviews, quieter completed states, and the redesign's untested assumptions.
- [Signifier Strength](/vault/signifier-strength.md) — Adds reported status-as-button confusion and the unresolved tradeoff between whole-row entry targets and accidental activation.
