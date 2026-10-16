---
type: Study Note
title: GOV.UK Complete Multiple Tasks
description: GOV.UK recommends a minimal, research-led task-state vocabulary that distinguishes unfinished work from unavailable work and allows deliberate completion judgments, but reports no measured vocabulary benefit.
resource: https://design-system.service.gov.uk/patterns/complete-multiple-tasks/
source: /archive/govuk-complete-multiple-tasks.pdf
tags: [content-design, interaction-design, cognitive-load, information-architecture, digital-interfaces]
timestamp: 2026-10-16T00:00:00Z
---

# GOV.UK Complete Multiple Tasks — Study Notes

**Authors**: GOV.UK Design System team; originated with Government Digital Service and iterated through cross-government collaboration.  
**Published**: Undated living pattern guidance captured October 16, 2026; no guidance revision date is displayed in the PDF or live page. The linked origin account is dated April 4, 2017, not the revision date of this guidance. The [latest repository change to the page](https://github.com/alphagov/govuk-design-system/commit/57357510e401fc0a0b125e09ae064c8e82b70c92), October 8, 2026, replaces discussion metadata and is not a substantive guidance revision.  
**Status**: Government service-design guidance, not an empirical vocabulary experiment. Read the complete twelve-page PDF with all state and completion examples; the live page's canonical link matches the resource URL.

## What It Is

A planning and resumption model for longer transactions across multiple sessions. An overview presents related activities as named tasks, identifies their states, and groups many tasks into meaningful stages. The source recommends simplifying the transaction before adding this structure and showing the overview at the initial and returning sessions.

## Status Vocabulary as an Idea

### Start with fewer distinctions

The source recommends starting with **Completed** and **Incomplete**, adding states only when research demonstrates a useful distinction. Its rationale is that a larger vocabulary is harder to remember. States should be short, in sentence case, and describe a condition rather than sound like an action. Consistency is preferred, while evidence about a particular audience can justify different wording.

### Separate unfinished, started, and unavailable

If people need to distinguish untouched work from work they have already begun, replace the broad incomplete state with **Not yet started** and **In progress**. Neither means the task is unavailable.

Use **Cannot start yet** when a prerequisite or other condition prevents entry. The example includes a task waiting for funds to be announced, so not all blocking is another task's completion. Such a task is not an entry target. The distinction matters because otherwise the person may mistake inability to proceed for a failure to act.

The pattern encourages order choice where possible, without implying every task is immediately available. **Analyst inference:** a list can support flexible order among eligible tasks while still communicating local prerequisites. The page does not specify a dependency model or test dependency explanations.

### Let remaining work stand out

Completion is deliberately quieter than work requiring attention. Colour may distinguish states, but the text carries their meaning. The source reserves an error-associated treatment for actual errors rather than borrowing it for ordinary incomplete work. Prefer repairing errors at their origin; if an erroneous task must remain saved, use an explicit **There is a problem** state.

The colour examples demonstrate available distinctions, not an instruction to create a distinct state for every colour. The rationale remains a minimal vocabulary rather than comprehensive decoration.

### Completion is a judgment, not necessarily a filled-field count

Optional questions, long answers, information gathering, and answers awaiting another person's review can make automatic completion misleading. The source recommends sometimes letting the person decide whether the section is complete or should be resumed later. Completed tasks must remain revisitable for correction. **Analyst inference:** saved, populated, personally finished, and finally submitted are different claims and should not silently substitute for one another.

## Evidence and Limits

- The research section describes the former “Task list” pattern and points to the component's research and known gaps. It provides no new participants, task protocol, measures, effect sizes, or replication evidence.
- The companion component reports status-as-button confusion and difficulty spotting incomplete work, but explicitly says the redesigned component still needs testing, including its proposed status wording. This pattern does not validate that wording independently.
- Examples visually distinguish completed, incomplete, in-progress, not-yet-started, blocked, and error states, and illustrate a person's explicit completion judgment. They demonstrate intended meanings rather than measured comprehension.
- There is no universal optimum number of states, measured reduction in memory burden, or established task-completion advantage in this source.

## Analyst Takeaways

1. **Add a state only when it changes interpretation or the next decision.** More internal workflow distinctions do not automatically deserve more user-facing labels.
2. **Do not label blocked work as merely untouched.** Availability and progress are separate dimensions even when a compact vocabulary presents them together.
3. **Keep completion truthful and revisitable.** Entered information may still need research or review; a user-marked section is not proof of external acceptance.
4. **Evaluate mixed-state lists.** Test whether people can identify remaining work, understand why a task cannot begin, and distinguish descriptive labels from actions.

## Questions and Limitations

- The page recommends adjective-like state wording but itself includes phrases such as “Cannot start yet” and “There is a problem.” The durable distinction is **describing state rather than issuing a command**, not a rigid grammatical rule.
- The companion component's blanket free-order language is broader than this pattern's explicit prerequisite case; preserve both as a scope tension rather than assuming all dependencies are forbidden.
- The blocked-task example retains an April 1, 2022 announcement date. This is specimen content, not current eligibility information or a guidance revision date.
- **Redistribution evidence**: the PDF footer states “All content is available under the Open Government Licence v3.0, except where otherwise stated” and identifies Crown copyright; no exception is stated for this guidance. Public archive attribution: **Contains public sector information licensed under the Open Government Licence v3.0.** No endorsement is implied.

## Vault Ideas Extracted

- [Task Lists and Status Vocabulary](/vault/task-status-vocabulary.md) — Supplies minimal vocabulary, availability versus progress, explicit completion judgments, and the rationale for quiet completed states.
