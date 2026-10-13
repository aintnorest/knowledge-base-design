---
type: Synthesis
title: Cognitive Dimensions Tradeoffs
description: Cognitive dimensions describe activity-dependent structural burdens in information artefacts, making redesign tradeoffs explicit rather than reducing usability to a single score.
tags: [cognitive-load, usability-evaluation, interaction-design, design-process]
timestamp: 2026-10-13T18:49:22Z
---

# Cognitive Dimensions Tradeoffs

Cognitive dimensions are a vocabulary for the cognitive consequences of an
information artefact's structure. A useful evaluation describes a **profile of
burdens for a particular activity**, then names the costs of changing that
profile. An improvement is often an exchange of burdens, not a movement toward
one universally ideal design.

The scope includes paper records, diagrams, notations, and software. Evaluate
the notation together with its editing environment and medium: the same marks
can be easy to revise when relationships are maintained automatically and costly
when every affected instance must be repaired by hand.

## Activity Determines the Tradeoff

Adding known information, transcribing content, modifying an existing structure,
and exploring an unknown solution make different demands. They describe current
activities, not permanent categories of users. A nominally sequential form may
actually be completed opportunistically from scattered information.

For example, **viscosity** is resistance to a goal-level change. Repetition
viscosity requires many actions for one conceptual change; knock-on viscosity
requires further repairs to restore consistency. This can be tolerable during
simple addition but disruptive during modification or exploration. Introducing
a reusable abstraction may reduce repetition while adding learning, scope
decisions, management work, and hidden dependencies.

Likewise, making dependencies explicit can consume space and create layout work.
Splitting a representation into smaller views can reduce local rearrangement
while worsening visibility and
[juxtaposability](/vault/juxtaposability-for-comparison.md). The remedy must be
judged against the next consequential activity, not only initial creation.

## Early Commitment and Informal Meaning

**Premature commitment** forces a decision before the necessary information is
available; **enforced lookahead** requires costly advance planning. The damage
increases when viscosity makes an early guess expensive to undo. Reducing change
cost helps repair the guess, but removing unnecessary order constraints addresses
the cause. **Provisionality** lets people represent tentative, incomplete ideas
without first settling the entire structure. **Progressive evaluation** lets
them check unfinished work along the way.

**Secondary notation** carries information outside the formal syntax:

- **Redundant recoding:** layout, grouping, or emphasis makes formal structure
  easier to interpret.
- **Escape from formalism:** rationale, uncertainty, history, or intention adds
  meaning that the formal record does not express.

These informal cues can support continued interpretation and revision, but they
can also become stale as the underlying structure changes. Removing them may
simplify maintenance while losing information people actually use.

## The Evidence

The framework's tutorial is an exposition with worked examples, not a controlled
validation study. It explicitly calls the dimensions **discussion tools** and
acknowledges little research on tradeoff relationships and difficult measurement.

An illustrative comparison had an experienced user transcribe the same
precomputed change in three programming representations. Reported editing times
were **508.3, 193.6, and 63.3 seconds**, about **8:1** between extremes. The account
attributes burden to rearrangement and rewiring and illustrates a trade between
local editing effort and co-visible structure. It supplies no participant sample
beyond that experienced-user description, repeated-trial distribution, or
inferential statistics; the authors call it a **straw-test**.

Other support includes diary analysis, observations, and toy paired examples.
These make mechanisms inspectable but do not validate a universal profile or
quantify redesign benefits. A later cautionary analysis warns that selecting only
some dimensions can miss changes in verbosity and error-proneness.

A first-party design-system account describes the same exchange in a shared
component library. More abstraction lets consumers supply less input but makes
the component's behavior harder to see and adjust, and practitioners report
consumers abandoning opaque shared components for local copies. Exposing
replaceable sub-parts and composition alongside complete defaults moves
complexity to where it can be handled rather than removing it. The account
reports no abandonment counts, comprehension tests, or maintenance outcomes,
and it does not apply the framework itself; the connection is interpretive.

## Practical Use

- Examine a realistic revision, correction, or reuse task as well as the first
  successful creation.
- For each proposed remedy, name the burden it reduces and the burdens it adds.
  Include sub-devices such as definition management, not just the main notation.
- When the end state is uncertain, inspect order constraints, reversal cost,
  tentative expression, and opportunities to check partial work together.
- Preserve useful rationale and uncertainty while deciding how their maintenance
  will remain aligned with the formal content.
- Use the profile to generate evaluation hypotheses; actual users and tasks must
  establish which tradeoffs matter and how much.

## Limitations

The dimensions are not a settled factor model or an overall usability score.
The tutorial refers to 13 dimensions but lists 14 named entries, and does not
claim completeness. Its analogy that redesign exchanges dimensions is a
reasoning aid, not an experimentally established conservation law.

There is also an unresolved inconsistency: the prose supports secondary notation
in exploration while tables label it harmful. Its interpretive benefit and
maintenance cost are defensible distinctions; a blanket prohibition on
exploratory annotation is not. Physical performance, aesthetics, emotion, and
context of use fall outside the framework, so an adequate cognitive profile does
not establish safety, accessibility, or overall experience quality.

## Sources

- [Cognitive Dimensions of Information Artefacts: a Tutorial](/dossiers/cognitive-dimensions-information-artefacts-tutorial.md) — Defines the activity-sensitive framework, viscosity, premature commitment, provisionality, and secondary notation; reports the illustrative LabView, Prograph, and Basic editing times and the framework's evidential and internal-consistency limits.
- [Multiple Layers of Abstraction in Design Systems](/dossiers/multiple-layers-of-abstraction-design-systems.md) — Spotify's 2023 first-party account supplies a practitioner example of trading repeated local assembly for the opacity of a shared abstraction, with replaceable sub-parts proposed as an escape route; no measured burden reduction.
