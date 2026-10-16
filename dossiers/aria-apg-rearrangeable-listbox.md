---
type: Study Note
title: Example Listboxes with Rearrangeable Options
description: W3C's illustrative listboxes combine explicit move actions, optional keyboard accelerators, polite completion feedback, and intentional focus continuity, while warning that examples are not production-ready or proof of assistive-technology support.
resource: https://www.w3.org/WAI/ARIA/apg/patterns/listbox/examples/listbox-rearrangeable/
source: /archive/aria-apg-rearrangeable-listbox/source.pdf
tags: [motor-accessibility, assistive-technology, accessibility, interaction-design, accessibility-standards, digital-interfaces]
timestamp: 2026-10-15T04:37:24Z
---

# Example Listboxes with Rearrangeable Options — Study Notes

**Authors**: W3C Web Accessibility Initiative (WAI), ARIA Authoring Practices Guide (APG).  
**Published**: Living example page, **last updated August 12, 2025**; supplied PDF captured **October 14, 2026**, with a 2026 copyright footer.  
**Status**: Informative pattern example, not a normative WCAG requirement or empirical study. Read the complete **14-page PDF**, including both illustrated listboxes, keyboard and state tables, included example markup, and footer; the live page confirms the canonical URL. Its expanded support notice warns about browser/assistive-technology gaps, especially mobile/touch, and requires evaluation before production use.

## What It Is

Two examples of **selecting objects and explicitly applying movement actions**, rather than requiring a drag. A single-select example ranks features important when choosing a home and transfers them between important and unimportant lists. A multi-select example transfers transport upgrades between available and chosen lists. Only the first demonstrates ranking within a list; the second demonstrates moving a selected set between collections.

The durable contribution is the relationship among action availability, selection, focus, confirmation, and the person's next operation. The command inventory and implementation syntax are not the knowledge being extracted.

## Principles as Ideas

### Selection chooses the objects; an action chooses the outcome

Visible action buttons expose reordering and transfers without requiring gesture precision. Keyboard shortcuts accelerate those same actions only in the relevant context; they are not the sole route to the outcome. Grouping related actions reduces repeated navigation through a collection of controls while preserving local access.

The two selection models differ deliberately. The single-select list couples navigation and selection. The multi-select list lets a person move the current interaction point without discarding the selected set and visually distinguishes focus from selection. The source notes that this model differs from native multi-select behavior; it is an intentional interaction choice, not evidence that all selection widgets behave alike.

### Place focus for the next meaningful operation

When a ranking shortcut moves an item, the active item remains the same, allowing consecutive moves and making its new position available to a screen reader. Maintaining identity matters more than retaining the same screen coordinate.

Transferring an item between lists has a different continuation goal: the example leaves interaction in the source list, on the first subsequent remaining option if the previously active one is gone. Moving focus to the transferred object is therefore not a universal rule. Choose continuity according to whether the likely next task is moving that object again or processing another source item.

The source distinguishes the visually and semantically active option from the container that holds browser focus. Its design requirement is agreement among the active item, visible focus, scrolling, and assistive-technology representation; no implementation algorithm is reproduced here.

### Confirm completion without commandeering navigation

Live feedback confirms completed actions. Both included examples specify **polite** announcement priority: ordinary movement confirmation need not interrupt ongoing speech. This complements focus continuity rather than replacing it. A person needs both to know what happened and to retain a useful location for the next action.

### Keep the current interaction point perceivable

When the active item changes in a scrollable list, bring it into view. Focus and selection must be distinguishable where they represent independent states. The figures illustrate paired lists, explicit action controls, and unavailable movement actions before selection; they do not measure discoverability or demonstrate dynamic operation in the print.

## Evidence / Admissions

- **Evidence type:** illustrative APG examples and accessibility rationale, with no participants, study task, measured task times, error rates, announcement rates, effect sizes, or replication.
- **Demonstrated scenarios:** one-item ranking and transfer, plus multi-item transfer. These are example tasks, not participant-study conditions.
- **Stated benefit:** retaining the active ranked option supports consecutive moves and hearing its new position. The page explains the mechanism but does not quantify the gain or establish success across assistive technologies.
- **Explicit warning:** the example is not intended for production environments. The live notice identifies possible support gaps and the need for assistive-technology testing; its support-measurement project is not a reported result for this captured source.

## Analyst Takeaways

1. **Make movement a discoverable action before adding accelerators.** Keyboard commands can complement buttons without making remembered commands the entry price for reordering.
2. **Preserve object identity for consecutive ranking.** A moved item should remain the next-action target when another move of that item is the ongoing task.
3. **Do not confuse focus continuity with always following the object.** Batch processing can justify retaining context in the source list after transfer.
4. **Expose the new state without moving to a notice.** Polite confirmation and an intentional continuation point solve different parts of the interaction.
5. **Keep spatial shortcuts contextual.** The [Atlassian guidance](/dossiers/atlassian-drag-and-drop-accessibility.md) discourages directional-command dependence for most experiences; this example uses accelerators within a specific ordered-list model, alongside explicit buttons. Neither source establishes a universally better model.

## Questions and Limitations

- The source does not establish production readiness, a complete conformance assessment, or cross-browser/assistive-technology success. A static print cannot verify the working example's announcement and focus behavior.
- It does not specify a cancellation or undo model for already committed moves. Cancellation before committing a destination is an analyst design implication, not a demonstrated behavior of these examples.
- **Internal inconsistency:** the accessibility-features prose says the first example groups **four** action buttons in a toolbar, but its included markup and figure show **three** grouped actions on the important-list side, with the fourth transfer action separate beside the other list. Preserve the grouping rationale without repeating the inaccurate count as an implemented fact.
- **Shortcut mismatch:** prose groups “Important” with actions using a removal command, while the included markup gives it an addition command. This does not alter the reusable model; it limits reliance on the page as a command reference.
- **Redistribution evidence:** the PDF footer states **Copyright © 2026 World Wide Web Consortium** and applies W3C liability, trademark, and **permissive license** rules unless otherwise noted. The linked [W3C Software and Document License, 2023 version](https://www.w3.org/copyright/software-license-2023/) explicitly permits copying and distribution subject to preserving notices and including the full licence notice. Following the existing APG alert archive, the unchanged PDF is publicly archived as `source.pdf` with `W3C-SOFTWARE-AND-DOCUMENT-LICENSE-2023.html` alongside.

## Vault Ideas Extracted

- [Accessible Reordering](/vault/accessible-reordering.md) — Adds explicit move actions, optional context-bound accelerators, distinct focus and selection, repeated-move continuity, and a different source-list continuation model for transfers.
- [Status Announcements](/vault/status-announcements.md) — Adds polite completion confirmation and the distinction between announcing a move and retaining the active item or a logical source-list successor.
