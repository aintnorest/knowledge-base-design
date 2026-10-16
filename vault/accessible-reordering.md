---
type: Synthesis
title: Accessible Reordering
description: Preserve reordering outcomes through single-pointer non-drag controls and keyboard access, contextual feedback, and a useful continuation point rather than requiring people to reproduce a dragging gesture.
tags: [motor-accessibility, assistive-technology, accessibility, interaction-design, accessibility-standards, digital-interfaces]
timestamp: 2026-10-15T04:37:24Z
---

# Accessible Reordering

Reordering is an outcome, not a gesture. A person should be able to choose an
item and its destination without holding a pointer down while moving it. An
accessible alternative also makes the result understandable and leaves the
person ready for the next move.

## How It Works

### Separate Outcome Access from Dragging

**WCAG 2.2 SC 2.5.7 Dragging Movements (AA)** requires functionality that uses
dragging to be achievable through a **single pointer without dragging**, unless
dragging is essential or the unmodified user agent determines the functionality.
Keyboard equivalence alone is insufficient: someone using touch, eye gaze, or a
speech-controlled pointer may not have access to keyboard-specific commands.
Keyboard access and single-pointer access must be evaluated independently.

Offer buttons, menus, or destination choices that can be activated by clicks or
taps and operated with the keyboard. Controls can be revealed when the person
selects an item, provided selection itself requires no drag and the action route
is discoverable. Selection-revealed adjacent movement buttons and menus for
moving between groups are examples in the criterion commentary, not mandatory
layouts. A separate equivalent control on the same page can also provide access.

### Express the Destination in the Task's Terms

For a short, ordered list, moving one place at a time can be meaningful. For a
large collection or a transfer between groups, choosing the destination directly
can avoid repeated commands and ambiguous spatial language. Name the affected
item and intended outcome so the action remains understandable without visual
proximity. Do not require people to infer where an unlabeled direction will lead.

Keyboard accelerators may support repeated moves, but ordinary navigation must
also expose the actions. Keep shortcuts contextual and distinguish navigating
among items, selecting items, and committing a move. When a selected set persists
while focus moves, make selection and the next-action target distinguishable.

### Confirm the Move and Preserve Continuity

Communicate **which item moved, where it was, and where it is now**. Position can
mean an ordinal rank or a named group; use enough context to disambiguate it.
Ordinary completion feedback should be **polite**, allowing current speech to
finish rather than treating every move as urgent. Announcement does not require
moving focus to the message; see [status announcements](/vault/status-announcements.md).

For consecutive reordering, keep the moved item or its action trigger active and
visible at its new position. This preserves the next operation on the same
object, not necessarily the same visual coordinate. If the operation removes the
item from the current collection, select a predictable continuation point: a
source-list successor can be more useful than following the transferred item
when the task is processing several source items. Do not leave focus nowhere.

### Allow Abandoning an Uncommitted Move

If reordering introduces a destination-choice or movement mode, provide a clear
way to cancel before commitment, leave the order unchanged, and return to the
initiating item or control. This is an **analyst design implication** of separating
selection from action and preserving focus, not a cancellation behavior tested or
fully specified by the sources. Canceling an uncommitted choice and undoing an
already completed move are different interaction contracts; do not label one as
the other.

## Evidence and Status

The evidence combines WCAG 2.2's requirement and informative rationale with
reasoned design-system guidance and illustrative accessibility examples. It
supports a model of equivalent outcomes, explicit controls, contextual feedback,
and continuity; it does **not** supply participant comparisons, effect sizes,
replication, or a universally fastest reorder interaction.

The sources differ on directional controls. One recommends avoiding reliance on
directional commands for most experiences because of nonvisual ambiguity, input
mode conflicts, and repeated effort. Another uses context-bound directional
accelerators for a specific ordered list alongside explicit action buttons.
Neither establishes that all arrows are harmful or that keyboard shortcuts alone
make dragging accessible.

## Practical Use

- Check that every destination reachable by dragging also has an equivalent
  non-drag route; test single-pointer activation separately from keyboard use.
- Make item actions discoverable on selection or through a persistent action
  route. Do not hide the only alternative behind dragging or hover alone.
- Choose relative movement or direct destination choice from the task and number
  of possible moves, not from the pointer interaction's appearance.
- Announce the item and meaningful old/new position without commandeering focus.
  Retain the moved item's continuation point for consecutive ranking.
- Define boundary, empty-list, transfer, and disappearing-control continuation
  behavior. Keep the active item visible and distinguish focus from selection.
- Where movement is staged, expose cancellation before commitment and preserve
  the original order on cancellation. Assess completed-move recovery separately.
- Evaluate discoverability, repeated moves, cancellation, and understood outcomes
  with disabled users and intended assistive technologies, not just whether a
  command can technically execute.

## Limitations

The illustrative examples are explicitly not production-ready and warn about
browser and assistive-technology gaps, particularly mobile/touch. Semantic
exposure and polite feedback do not guarantee successful delivery or comprehension.
No source establishes a maximum list size, optimal command count, universal focus
fallback, or complete cancellation/undo policy. A selection model suitable for a
simple list may not fit nested collections or multi-object transfers. Conformance
to one criterion does not establish accessibility of the complete workflow.

## Sources

- [Atlassian Drag and Drop Accessibility Guidelines](/dossiers/atlassian-drag-and-drop-accessibility.md) — Supplies the outcome–feedback–continuation model, named controls, item/origin/destination messages, and qualified concerns about directional-command dependence.
- [Example Listboxes with Rearrangeable Options](/dossiers/aria-apg-rearrangeable-listbox.md) — Supplies explicit movement actions with optional accelerators, polite completion confirmation, repeated-ranking continuity, and source-list continuation after transfer; illustrative rather than tested production guidance.
- [Understanding WCAG 2.2](/dossiers/understanding-wcag-2-2.md) — The archived SC 2.5.7 Dragging Movements commentary supplies single-pointer non-drag access, its independence from keyboard access, exceptions, and selection-revealed button/menu examples.
- [Developing a Keyboard Interface](/dossiers/aria-apg-keyboard-interface.md) — Supplies discoverable actions beyond remembered shortcuts, persistent logical focus, and the distinction between selection and the current interaction target; no measured efficiency benefit is established.
