---
type: Study Note
title: Enhancing the Explanatory Power of Usability Heuristics
description: A single-rater analysis of 249 existing usability problems synthesizes nine heuristics from 101 principles, but explanatory coverage is not evidence that the new set detects more problems.
resource: https://doi.org/10.1145/191666.191729
source: https://doi.org/10.1145/191666.191729
tags: [usability-evaluation, interaction-design, digital-interfaces, ux-metrics]
timestamp: 2026-10-11T23:50:47Z
---

# Explanatory Power of Usability Heuristics — Study Notes

**Authors**: Jakob Nielsen, Bellcore.  
**Published**: CHI '94, Boston, April 24–28, 1994, pp. 152–158.  
**Status**: Peer-reviewed conference paper; the version read is the ACM proceedings PDF. It derives a candidate set of **nine**, not the subsequently familiar ten, heuristics; help and documentation appears in an input set but not in the final candidate set.  

## What It Is

A retrospective attempt to make a compact heuristic vocabulary explain more of the usability failures already encountered in practice. Nielsen rates **101 heuristics against 249 known problems**, uses principal-components analysis to identify overlapping explanatory themes, then checks which existing principles cover the greatest number of problems. The contribution is a synthesis grounded in a problem corpus—not a comparative experiment demonstrating superior inspection performance.

## Problem and Motivation

The original heuristic set prioritized teachability and adoption of discount usability engineering. Numerous alternatives subsequently appeared, with different purposes and interface assumptions. The question is whether a small, learnable set can retain broad explanatory power without pretending to capture every kind of failure.

Nielsen explicitly declines a contest between heuristic sets. Evaluators bring prior usability knowledge into an inspection and cannot simply forget principles excluded from their assigned list. Moreover, several input sets were never intended for heuristic evaluation: the Star principles guide design, Polson and Lewis target successful guessing, and Carroll and Rosson support claims analysis. Comparing their scores as though they were interchangeable methods would misstate the study.

## Mechanism as an Idea

### The corpus and explanatory measure

The **249 problems came from 11 projects** in which Nielsen had participated: **seven heuristic evaluations and four user tests**; **four early-development and seven late-development** projects; **two character-based, six graphical, and three telephone-operated** interfaces. There is no new participant task or user outcome experiment. The analytic units are problem descriptions and heuristics, and the author is the **only explanation rater**.

For each of the **25,149 problem–heuristic pairs**, a **0–5** judgment ranges from no explanation to complete explanation. A score of **3** means a heuristic explains a major part while leaving some aspects unexplained. Two summary measures must be kept separate:

- **Mean explanation rating** for an individual heuristic is its mean across the entire corpus. For a set, the mean uses the **best-scoring heuristic for each problem**, not the mean of every member's score.
- **Explanatory coverage** is the fraction of problems with at least one member scoring **3 or more**. A second or third matching heuristic earns no additional credit; the paper leaves open whether multiple partial explanations are useful in practice.

The seven input sets are Nielsen's earlier ten heuristics; Star's design principles; Holcomb and Tharp's usability principles; Polson and Lewis's guessing principles; Carroll and Rosson's claims-analysis questions; the Macintosh Human Interface Guidelines; and SunSoft's guidelines. Most were shortened and rewritten by Nielsen, so both wording and its interpretation are part of the measurement.

### The factors and the resulting candidate set

The seven leading, subjectively named factors provide the backbone:

1. **Visibility of system status — 6.1% variance**: feedback about what is happening and whether an action has been received.
2. **Match between system and the real world — 5.9%**: familiar language, conceptual models, and conventions make system meaning intelligible.
3. **User control and freedom — 4.6%**: undo, exits, cancellation, and freedom from being trapped in a state.
4. **Consistency and standards — 4.2%**: stable meanings and behavior, including platform conventions.
5. **Error prevention — 3.7%**: avoid foreseeable mistakes rather than relying only on repair.
6. **Recognition rather than recall — 3.1%**: make available actions and alternatives salient. This differs from status visibility: it reveals what can be done next, not just what is happening now.
7. **Flexibility and efficiency of use — 2.8%**: accelerators, customization, and alternatives that bypass slower standard interaction. This differs from escape or undo: it enables productive shortcuts rather than merely avoiding entrapment.

The coverage analysis supplies two additions insufficiently represented by that backbone: **aesthetic and minimalist design**, and **helping users recognize, diagnose, and recover from errors**. The final nine are a judgment combining factors, coverage, and the author's view of important usability dimensions—not nine independently discovered latent factors.

## Results / Admissions

- **No compact statistical core**: the first two components account for about **6% each**; **25 components** explaining at least 1% each account for **62%**; **53** are needed for **90%**. The decline has no sharp elbow. Usability failures are more diverse than a tidy checklist suggests.
- **Existing-set scores**: mean best explanation / coverage are **3.72 / 82%** for the earlier Nielsen set, **2.38 / 49%** Star, **2.90 / 64%** Holcomb–Tharp, **2.31 / 47%** Polson–Lewis, **1.99 / 44%** claims analysis, **3.09 / 66%** Macintosh, and **3.31 / 73%** SunSoft. Nielsen warns against ranking these as winners: scope, modality, and corpus history differ.
- **Greedy coverage for all problems**: iteratively choosing the principle that adds the most still-unexplained problems yields **85%** coverage with ten existing heuristics. In order: consistency; user language; receipt-of-input feedback; seeing/pointing rather than remembering/typing; aesthetic integrity; shortcuts; real-world conventions; error recognition/recovery; forgiveness; salient available actions. Consistency alone covers **23%**; the first four reach **59%**, and adding aesthetics reaches **65%**.
- **Serious-problem coverage**: **82 serious problems** have high potential to delay or prevent task completion; the remaining **167** are minor. The serious-problem greedy list reaches **95%** with ten principles, compared with **85%** for all problems. Its first four—seeing/pointing, consistency, timely accurate feedback, and salient actions—cover **70%**. The prose compares this with **65%** for four heuristics covering all problems, but Table 1's all-problem list reaches only **59%** after four and 65% after five. It is unclear whether the prose evaluates a different subset or contains an off-by-one error; use the table for the displayed greedy sequences.
- **Severity does not exhaust usability**: shortcuts and aesthetic integrity are more prominent for minor failures, yet Nielsen retains them because expert efficiency and satisfaction matter even when no individual failure makes a system unusable. That rationale is an admission about the severity classification, not new evidence of sales or satisfaction effects.
- **The final nine have no measured coverage score here**: **85% and 95%** refer to greedy combinations of already-rated source heuristics. They must not be attributed directly to the rewritten final nine or interpreted as detection rates.

## Analyst Takeaways

1. **Use the set to broaden questions, not certify an interface.** The finding that many components are needed is more important than the familiar checklist: no short vocabulary guarantees complete coverage.
2. **Keep explanation, detection, and impact separate.** A principle can explain a reported failure without helping an evaluator notice it; a frequently applicable principle need not identify the highest-cost failures.
3. **Preserve the distinction between knowing the state and recognizing options.** A design can report progress clearly while keeping its next available actions opaque, or expose actions while leaving their outcomes ambiguous.
4. **Interpret consistency as one important family, not an overriding law.** Its broad corpus coverage does not establish that consistent behavior is preferable to every context-specific departure.
5. **Pair heuristic breadth with multiple perspectives.** The single-rater origin makes [the evaluator-effect review](/dossiers/evaluator-effect-usability-evaluation-methods.md) a useful methodological counterweight: an expert's explanation is not a reproducible inventory of all problems.

## Questions and Limitations

- The only rater had participated in the original projects. That supplied needed context but eliminated independent reliability assessment and created opportunities for hindsight and allegiance effects. No interrater agreement or statistical uncertainty around the coverage percentages is reported.
- Much of the corpus came from the original heuristic-evaluation work, giving the earlier Nielsen set a likely advantage. Problems missed by both initial evaluation methods are absent altogether.
- Mixing graphical, character-based, and telephone interfaces improves breadth but complicates interpretation of interface-specific input sets. The paper does not claim representativeness of contemporary products or accessibility barriers.
- Factor names are subjective abstractions; many input principles are paraphrases, not untouched source formulations. Variance in explanation ratings is not variance in actual user performance.
- The text says the seven factors each explain more than **3%**, yet lists factor seven at **2.8%**. Their displayed values sum to about **30%**, so retain the approximation but not the literal threshold claim.
- Greedy additions are marginal coverage gains, not independent importance estimates; overlapping wording changes can alter which member is selected. The study does not prove a globally optimal subset.
- The conclusion explicitly says it remains to be seen whether these heuristics help find **new** problems. This paper alone supplies no prospective replication of that central claim.

## Vault Ideas Extracted

- [Visibility of System Status](/vault/visibility-of-system-status.md) — Distinguishes information about current system activity from the salience of future options; a leading explanatory factor, not a measured treatment effect.
- [Recognition over Recall](/vault/recognition-over-recall.md) — Connects visible available actions with serious-problem coverage while separating recognition from feedback.
- [Consistency and Convention](/vault/consistency-and-convention.md) — Establishes broad explanatory coverage for stable meanings and standards within a historically bounded corpus.
- [Error Prevention and Recovery](/vault/error-prevention-and-recovery.md) — Separates preventing mistakes, escaping unwanted states, and constructively diagnosing or reversing failures.
