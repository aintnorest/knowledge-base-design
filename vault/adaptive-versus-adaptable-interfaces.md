---
type: Synthesis
title: System-Changed versus User-Changed Interfaces
description: Distinguish who changes an interface from how it changes, preserve learned locations when offering adaptive shortcuts, and weigh prediction accuracy against search, surprise, and customization costs.
tags: [interaction-design, layout, cognitive-load, human-performance, digital-interfaces]
timestamp: 2026-10-16T00:00:00Z
---

# System-Changed versus User-Changed Interfaces

Personalization is not a single interaction strategy. A **static** interface keeps
its arrangement during use. An **adaptive** interface changes under system
control. An **adaptable** interface changes under the person's control. A design
can also share control, for example by suggesting a change that the person chooses
whether to apply. Who controls change and what moves are separate decisions.

## Preserve the Learned Route

Moving commands toward likely use can save access steps while making their old
locations unreliable. Disappearance and displacement affect not only the promoted
command but neighboring commands people already know. The person may have to
search again or discover that a familiar action path has changed. This is a
spatial form of [consistency and convention](/vault/consistency-and-convention.md),
not a demand for visual uniformity.

A different strategy is to **copy likely useful actions into a separate adaptive
area while leaving the original interface unchanged**. The person can exploit a
correct suggestion or keep using the familiar route. The adaptive area still
changes and may require an extra search; stable originals do not make inaccurate
predictions free.

Do not assume that visibly changing the layout communicates what changed.
[Change detection](/vault/change-detection.md) distinguishes seeing a transition
from recognizing a completed change after looking away. The menu and toolbar
experiments below did not measure change-detection failures directly.

## Accuracy and Control Have Costs

A prediction is useful when it offers the next needed action, not simply a
frequently used one. Measure both correct promotions and what people do when a
prediction is wrong. A separate optional area limits disruption, but checking it
can still waste attention. Higher accuracy can also alter the strategy people
learn and their willingness to use future suggestions.

User control avoids unrequested rearrangement but requires discovery, setup, and
maintenance. People may not recognize the value of customization even when the
mechanism is easy. A fast personalized end state does not establish net savings
once setup and changing work patterns are included. Shared-control suggestions
are a reasonable option to test, not a demonstrated best compromise in these
sources.

## Evidence

A **27-person** split-menu experiment found an optimally preconfigured static
menu faster than an automatically moving menu: **306.51 versus 331.62 seconds**
for a repeated 200-selection block. User-controlled menus were faster than the
adaptive menus only when they were not encountered first. **22/27** participants
customized meaningfully; mean setup time across all participants was **142
seconds**, outside the reported selection time. **15/27** preferred adaptable,
but its preference advantage over adaptive was not statistically established.
Stable locations, customization uptake, and experienced control must therefore
not be collapsed into one outcome.

A later **26-person** toolbar experiment favored a separate copied-shortcut area
in ratings and rankings over a nonadaptive baseline, without establishing a timed
advantage on its realistic tasks. In a second experiment with **eight researchers**
doing repetitive selection, that copied-shortcut interface was faster than
baseline (**p = .003**), but absolute time savings were not reported. Moving
commands did not significantly outperform baseline (**p = .073**), and the two
adaptive designs did not significantly differ from one another.

In that second experiment, **70% versus 30% prediction accuracy** improved time
for both adaptive designs. When a requested command existed in both places,
people chose its adaptive copy **93.1% versus 81.0%** of the time, a
**12.1-percentage-point** difference. Those percentages are conditional shortcut
uptake, not the fraction of all requests correctly predicted. They do not define
a universal accuracy threshold.

## Practical Use

- Keep important learned locations and ordinary access routes intact when adding
  predictions. Prefer optional shortcuts over forced relocation when stability
  matters; validate the extra search area rather than assuming it is harmless.
- Evaluate correct and incorrect predictions, changed task patterns, and returns
  after attention was elsewhere. Count search, errors, and recovery as well as
  access steps.
- Measure customization uptake and setup time alongside steady-state efficiency.
  Check whether people understand the benefit, not only how to make a change.
- Separate preference, actual speed, error rate, perceived effort, and discovery.
  A popular adaptation need not be faster, and a faster one need not be preferred.
- Test the work's rhythm. Grouped shortcuts may help complex work while rapid
  repetitive selection makes looking between two locations more burdensome.

## Limitations

The direct evidence concerns **short laboratory tasks, small samples, menus and
toolbars**, with a student sample in one study and experienced users in the other.
It does not establish long-term learning, accessibility, all forms of content
adaptation, or a universal ban on automatic change. The static menu had advance
knowledge of task frequencies, while the toolbar variants differed in more than
spatial stability. Comments support a stability rationale, but its independent
causal contribution was not isolated.

The later experiments qualify rather than directly replicate the earlier one:
copying is a different intervention from moving. No independent replication of
these exact comparisons is established by the supplied sources. Reporting
ambiguities and an implementation-related highlighting slowdown further limit
precise generalization. Adaptation frequency and predictability remain partly
hypothesized mechanisms, not settled design thresholds.

## Sources

- [A Comparison of Static, Adaptive, and Adaptable Menus](/dossiers/static-adaptive-adaptable-menus.md) — Provides the 27-person split-menu comparison, order-dependent customization benefit, setup costs, and preference/performance distinction.
- [Exploring the Design Space for Adaptive Graphical User Interfaces](/dossiers/design-space-adaptive-graphical-interfaces.md) — Provides the 26- and eight-person toolbar experiments, copied-versus-moved shortcuts, accuracy effects, and conditional shortcut uptake.
