---
type: Synthesis
title: Status Announcements
description: Make dynamic status perceivable through assistive technology without moving focus, matching announcement urgency and context to the task while preserving discoverability and time to understand.
tags: [assistive-technology, accessibility, interaction-design, content-design, attention, digital-interfaces]
timestamp: 2026-10-15T04:37:24Z
---

# Status Announcements

A status change should be perceivable without requiring someone to find a new
interaction location. Announcing results, waiting, progress, or errors through
assistive technology lets people remain at their current task while learning
what changed. This complements [visibility of system status](/vault/visibility-of-system-status.md):
visible feedback alone does not guarantee that a nonvisual user encounters it.

## How It Works

### Separate Announcement from Focus Movement

**WCAG 2.2 SC 4.1.3 Status Messages (AA)** requires status messages in markup
content to be programmatically determinable so assistive technologies can present
them without receiving focus. It addresses status supplied without a change of
context; it does not require inventing a message for every content change. Search
results themselves, newly added questions, and ordinary control-state changes are
not automatically status messages under this criterion.

An informational alert preserves keyboard focus. A response-requiring dialog has
a different interaction contract: it interrupts the workflow and needs deliberate
focus management. Announcement semantics do not inherently move focus; a component
that does both is making two separate decisions. See
[interruption coordination](/vault/interruption-coordination.md).

### Match Urgency and Supply Meaningful Context

Use **polite** announcement priority for ordinary status that can wait for a pause
in current speech; reserve **assertive** priority for important, time-sensitive
information that justifies interrupting it. The criterion's commentary explicitly
identifies assertive treatment of non-important, non-time-sensitive content as a
failure. Importance does not by itself require taking over keyboard focus.

The message must carry the context visual proximity otherwise supplies. Hearing
“three” does not say whether three results, errors, or items changed. Announce the
meaningful unit, such as “Shopping cart, three items,” rather than only the changed
number. If removal of a busy indicator signifies availability, make that end state
perceivable too; silent disappearance is not equivalent feedback.

### Announce Movement While Preserving the Next Action

For a reorder or transfer, identify **the item, its old position, and its new
position**. A position may be a rank in a list or a named destination group;
the message should make the changed relationship understandable without sight.
Use **polite** priority for ordinary move completion rather than interrupting
current speech. This is confirmation of an action, not a request to navigate
to a new notice.

Keep the moved item or its action trigger active when the task is consecutive
reordering, so another move does not require finding it again. If transferring
an item removes it from the source collection, a predictable remaining source
item can instead be the useful continuation point. Announcing the result and
choosing that continuation point are separate responsibilities; see
[accessible reordering](/vault/accessible-reordering.md).

### Design Initial Discovery and Dynamic Delivery Separately

Alert-pattern guidance says most screen readers announce dynamically rendered
alerts, but warns that messages already present before page load completes may
not be announced. A prominent notice before the main heading can also be skipped
when someone navigates directly to that heading. A named, navigable notice supports
later discovery without proving that everyone encounters it.

Keep information needed for the current task in the task content, not solely in
a peripheral notice. Preserve messages long enough to locate, interpret, and revisit
them; avoid automatic disappearance and frequent alerts. Stable focus does not
eliminate auditory or cognitive interruption.

### Keep Unavailable Actions Discoverable When Needed

Communicating state also includes whether an action exists but is unavailable.
Keyboard guidance describes a **discoverability–navigation-effort tradeoff**:
removing disabled controls from the tab order saves navigation steps but can make
them harder for screen-reader users to discover. Skipping an action can be
reasonable when its existence is inferable nearby; retain discoverability within
local exploration when encountering the action is necessary to understand the
capability. Focusability must communicate unavailability, not imply executability.
This is related state-discovery guidance, not a requirement of SC 4.1.3 to announce
every disabled control or make every one a tab stop.

## Evidence and Status

The sources provide **standards rationale and informative pattern guidance**, not
participant experiments establishing announcement rates, comprehension gains, or
optimal urgency, frequency, and duration thresholds. The polite status model comes
from a sufficient technique linked by the criterion commentary; techniques are
accepted routes, not mandatory implementations. The alert pattern alone does not
compare polite and assertive priorities.

The notice guidance explicitly leaves missed-notice prevalence and dismissal
benefits unresolved. Its wording conflates alert semantics with page-load focus
movement; that conflation is not carried into this synthesis. The keyboard source
also contains unfinished guidance and supplies no measured discovery advantage or
acceptable extra-navigation budget.

Movement guidance adds an outcome–feedback–continuation model and an illustrative
example of polite completion messages. It does not establish measured announcement
rates or a universal follow-the-moved-item rule: consecutive ranking and processing
remaining source items can call for different focus destinations.

## Practical Use

- Specify the state, its task meaning, its urgency, and whether a response is
  required before choosing presentation or focus behavior.
- Preserve focus for informational updates; do not use urgency as a substitute
  for a justified response requirement.
- Include sufficient context in spoken or braille output, including completion
  when a waiting cue disappears.
- For movement, include item identity and meaningful old/new position, then
  preserve a useful next-action location rather than focusing the announcement.
- Provide a discoverable, persistent route to important notices, including those
  initially present, without relying on automatic announcement alone.
- Evaluate initial load, dynamic updates, heading navigation, disabled-action
  discovery, and repeated messages with the intended assistive technologies and
  users. Evaluate understanding as well as whether speech occurred.

## Limitations

Semantic exposure is necessary but does not guarantee compatible presentation in
every browser, screen reader, language, or user preference. No source establishes
a universal timeout, alert frequency, or optimal disabled-control policy. Extra
announcements can make an interface too chatty; extra focusable unavailable actions
can make navigation laborious. Conformance and successful announcement do not by
themselves establish an understandable or interruption-free journey.

## Sources

- [Alert Pattern](/dossiers/aria-apg-alert-pattern.md) — W3C APG guidance supplies announcement without focus movement, dynamic-versus-initial-content caveats, and frequency/disappearance cautions, without an interoperability study or measured thresholds.
- [Developing a Keyboard Interface](/dossiers/aria-apg-keyboard-interface.md) — W3C APG guidance supplies the disabled-control discovery versus navigation-effort tradeoff and separation of focus from state, without measured discovery benefits.
- [GOV.UK Notification Banner Guidance](/dossiers/govuk-notification-banner-guidance.md) — Supplies named navigable notices, heading-skipping risks, task-local placement, and an explicit announcement/focus wording limitation; missed-notice and dismissal outcomes remain unknown.
- [Understanding WCAG 2.2](/dossiers/understanding-wcag-2-2.md) — SC 4.1.3's archived commentary and its linked polite-status technique supply the scope, context-equivalence rationale, and urgency boundary; informative explanation and techniques are not empirical outcome validation.
- [Atlassian Drag and Drop Accessibility Guidelines](/dossiers/atlassian-drag-and-drop-accessibility.md) — Adds item, origin, and destination context for movement feedback and returning to the item's action trigger where possible; does not itself compare announcement priorities.
- [Example Listboxes with Rearrangeable Options](/dossiers/aria-apg-rearrangeable-listbox.md) — Adds polite completion feedback, repeated-move continuity on a ranked item, and a source-list continuation alternative after transfers; illustrative examples are not interoperability results.
