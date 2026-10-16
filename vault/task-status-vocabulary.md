---
type: Synthesis
title: Task Lists and Status Vocabulary
description: Use the smallest meaningful set of task states, distinguish unavailable work from unfinished work, and keep completed states quieter without making status look like an independent action.
tags: [content-design, interaction-design, cognitive-load, visual-hierarchy, digital-interfaces]
timestamp: 2026-10-16T00:00:00Z
---

# Task Lists and Status Vocabulary

A task list should answer **what remains, what can begin, and what can be resumed**.
A state label is useful when it changes one of those judgments. Mirroring every
internal workflow state can create a vocabulary people must learn without helping
them decide what to do next.

## Use the Smallest Meaningful Vocabulary

Begin with a distinction such as **complete** versus **incomplete**. Split an
unfinished state only when people need the additional meaning:

- **Not started:** work has not begun, but it is available to begin.
- **In progress:** work has begun and remains unfinished; this need not mean
  someone or something is actively working on it at this moment.
- **Cannot start yet:** a prerequisite or other condition prevents entry. This is
  not interchangeable with not started and is not, by itself, an error.
- **Complete:** the task has met the relevant completion condition, not merely
  been opened or saved.

These are semantic distinctions, not a requirement to display four states in every
list. Fewer labels reduce the vocabulary to interpret and remember; that is a
reasoned guidance claim, not a measured optimum state count. Use short,
condition-describing phrases rather than commands, and keep familiar meanings
consistent unless research supports a change.

For blocked work, make the enabling condition understandable where known: another
task must finish, information must arrive, or an external event must occur. This
explanation is a synthesis inference from the distinction between availability
and progress, not a tested dependency-display design. Do not present an
unavailable task as an action that will start successfully.

## Expose Remaining Work Without Hiding Completion

As a list fills with completed tasks, strong completion decorations can compete
with the few items that still need attention. Keep completion recognizable but
visually quieter than actionable unfinished states. De-emphasis must preserve
readability; it is not permission to hide whether something is done.

Use words to carry meaning even when colour reinforces differences. Reserve error
emphasis for actual problems rather than ordinary unfinished or blocked work.
A person should not have to infer whether a state means failure, waiting, or work
still to do from colour alone.

## Separate Descriptive State from an Action Invitation

A compact, filled status label can resemble a button. Test whether people try to
activate a state and whether they understand what selecting the task will do.
Reducing button-like treatment and making an available task's entry target more
forgiving are possible responses, but a larger target can also increase accidental
activation. Neither treatment is universally validated; see
[signifier strength](/vault/signifier-strength.md).

Completion can require a person's judgment when answers are optional, need further
research, or await review by someone else. Distinguish saved work from finished
work and permit correction after a task is marked complete. Section completion,
submission, and acceptance by another party are not automatically the same state.

## Practical Use

- Simplify the work before adding a task overview. Such an overview is useful for
  planning and resumption when people need meaningful order choice, not merely
  because a process is long.
- Group related work into recognizable tasks and stages. Show the overview where
  it helps someone begin or resume rather than replacing answer review with it.
- Test partly completed lists, including a few unfinished and blocked tasks among
  many completed ones. Ask people to identify what they can do next and why.
- Test state comprehension separately from detecting the label or clicking a row.
- Keep labels grounded in the actual completion condition and known prerequisites;
  do not imply ongoing activity when the only fact known is prior work.

## Evidence and Limitations

The supporting guidance reports earlier users mistaking status tags for buttons
and having difficulty finding unfinished work after several tasks were completed.
It provides **no participant counts, task protocols, rates, or effect sizes**.
Its redesigned presentation **still needed user testing**, including wording,
contrast, and whether larger task targets' benefits outweighed accidental clicks.
The component and pattern describe one related research lineage, not independent
replications.

Minimal vocabulary, quiet completion, and flexible ordering are therefore
reasoned recommendations rather than demonstrated universal performance gains.
A strictly ordered journey may be better served by saved progress and direct
resumption. The sources concern user-completed service transactions; applying the
vocabulary to delegated or automated work requires testing who owns each task,
what “in progress” means, and what counts as completion.

## Sources

- [GOV.UK Task List Guidance](/dossiers/govuk-task-list-guidance.md) — Reports status-as-button confusion and completed-work scanning difficulties; the redesign's target size, contrast, and wording remain explicitly untested.
- [GOV.UK Complete Multiple Tasks](/dossiers/govuk-complete-multiple-tasks.md) — Recommends minimal, research-led status distinctions, explicit unavailable work, quiet completion, and user completion judgments without measured vocabulary effects.
