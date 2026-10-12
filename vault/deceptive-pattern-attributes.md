---
type: Synthesis
title: Deceptive Pattern Attributes
description: Five overlapping attributes distinguish unequal choice burden, concealed influence, false beliefs, hidden information, and restricted alternatives without treating every persuasive design as deception.
tags: [deceptive-patterns, decision-making, interaction-design, digital-interfaces]
timestamp: 2026-10-12T00:00:39Z
---

# Deceptive Pattern Attributes

Deceptive-pattern attributes describe **how an interface subverts informed
choice**, rather than merely naming a familiar trick. Unequal burden, concealed
influence, false beliefs, delayed information, and restricted alternatives are
different problems. A design can carry several at once; repairing one does not
necessarily repair the others.

## Five Attributes

| Attribute | What changes | Review question |
|---|---|---|
| **Asymmetric** | Explicit choices receive unequal weight or effort. | Is acceptance prominent while refusal is obscure or burdensome? |
| **Covert** | The influence itself is concealed, even if its message is visible. | Can the person recognize how the presentation is steering the decision? |
| **Deceptive** | Falsehoods, misleading statements, or omissions induce false beliefs. | Does the apparent offer or consequence match what actually happens? |
| **Hides information** | Necessary information is obscured or delayed. | Can the person know the relevant cost or commitment before investing effort? |
| **Restrictive** | Meaningful alternatives are reduced. | Can the person decline, leave, or complete the intended task without an unrelated condition? |

Covert influence is not synonymous with hidden information: a visible decoy can
conceal its steering role. Restriction or pressure need not contain a factual
lie. Asymmetry here concerns **explicit choices**, not every difference in effort
between arbitrary activities.

These attributes complement a strategy vocabulary: **nagging** repeatedly
redirects activity; **obstruction** makes an action unnecessarily difficult;
**sneaking** hides or delays decision-relevant information; **interface
interference** manipulates presentation or interpretation; **forced action**
requires an additional action to obtain the desired functionality. Strategies
describe what happens to the interaction, while attributes explain its influence.
There is no validated one-to-one mapping between the two vocabularies.

## The Evidence

A descriptive shopping-site crawl identified **1,818 pattern instances on 1,254
of 11,286 websites**, approximately **11.1%** of the observed corpus. It supplied
the five-attribute model and concrete examples. There were **no recruited
consumers** and no measured purchase, comprehension, or harm effects.

Targeted follow-up reported **234 deceptive instances across 183 sites**,
including checks showing apparent deadlines that did not end offers and
fabricated activity or stock signals. This does not mean all 1,818 detected
patterns were verified falsehoods. Two researchers agreed at **Cohen's κ = .74**
on **200 selected candidate clusters**; that measures coding agreement at one
stage, not the detection pipeline's recall or the taxonomy's behavioral validity.

A separate qualitative analysis of **118 practitioner-circulated artifacts**
derived the five strategies. Its materials included commentary and resources,
not necessarily 118 unique interface instances. It recruited neither users nor
designers and supplied no inter-rater reliability statistic. Its contribution is
an ethical vocabulary supported by exemplars, not a prevalence estimate or proof
of malicious intent.

## Practical Use

- Review refusal, cancellation, comparison, and information-seeking paths, not
  just the organization's desired conversion. Smooth task completion can still
  serve an outcome contrary to the person's goals.
- Name the affected attribute when proposing a remedy. Upfront disclosure can
  remove information hiding while leaving a restrictive condition intact.
- Inspect what the interface communicates, not only what is technically possible.
  A working alternative that appears unavailable can mislead through weak
  [signifiers](/vault/signifier-strength.md).
- Separate observed mechanisms from inferred motivations and measured outcomes.
  Record which consequence is hidden, which alternative is burdened, and whose
  goal benefits before making claims about intention or harm.

## Limitations

Neither ordinary persuasion nor every default, reminder, prerequisite, or real
stock warning is necessarily deceptive. Accurate information, proportionality,
user goals, and context can change the ethical interpretation. The taxonomies do
not supply a validated threshold for borderline cases or a mechanical verdict
about legality.

The crawl was English-language, popularity-ranked, text-centered, and limited to
sampled shopping paths; no end-to-end recall estimate corrects its missed flows
or visual patterns. The artifact study intentionally sampled publicly discussed
failures. Neither supports global prevalence or causal consumer-effect claims.
Connections to scarcity, framing, defaults, and other biases are explanatory
accounts, not measured mediators in these studies.

## Sources

- [Dark Patterns at Scale: Findings from a Crawl of 11K Shopping Websites](/dossiers/dark-patterns-at-scale-shopping-websites.md) — Defines the five overlapping attributes, documents shopping-site occurrence and targeted verification of falsehoods, and states the crawl's coverage and effect-measurement limits.
- [The Dark (Patterns) Side of UX Design](/dossiers/dark-patterns-side-of-ux-design.md) — Supplies the complementary five-strategy vocabulary and ethical account of user versus organizational goals, while distinguishing artifact interpretation from evidence of intent or behavioral effects.
