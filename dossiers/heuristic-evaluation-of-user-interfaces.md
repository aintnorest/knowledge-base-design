---
type: Study Note
title: Heuristic evaluation of user interfaces
description: Four small-interface experiments show independent evaluators find complementary usability problems and simulated unions substantially improve coverage, without establishing exhaustive detection or validity in actual use.
resource: https://doi.org/10.1145/97243.97281
source: https://doi.org/10.1145/97243.97281
tags: [usability-evaluation, ux-metrics, interaction-design, digital-interfaces]
timestamp: 2026-10-12T20:35:00Z
---

# Heuristic Evaluation of User Interfaces — Study Notes

**Authors**: Jakob Nielsen and Rolf Molich.  
**Published**: CHI '90, April 1990, pp. 249–256.  
**Status**: Peer-reviewed ACM conference paper; read the eight-page proceedings PDF supplied from the cs.cmu.edu-hosted copy, including all four figures and four tables. The DOI is corroborated by publisher-registration metadata; it is not printed in this historical PDF.  

## What It Is

An empirical examination of informal usability inspection: people examine an interface and identify problems using a compact set of principles rather than a thousand-rule checklist. Its important result is not that one inspector can certify usability, but that **different inspectors notice different things**, making the union of independent reports substantially more informative than any one report.

The paper's original **nine heuristics** are simple and natural dialogue; speak the user's language; minimize memory load; consistency; feedback; clearly marked exits; shortcuts; good error messages; and error prevention. This is not the later familiar ten-heuristic formulation. [The 1994 explanatory-power paper](/dossiers/enhancing-explanatory-power-usability-heuristics.md) examines a subsequent synthesis, with a different question and evidence base.

## Problem and Motivation

Formal models and automated checks were not broadly usable in contemporary industrial development, while empirical testing was often omitted for lack of resources or tradition. The authors therefore investigate an imperfect method people already use, rather than assuming an ideal method will be adopted. Compressing guidelines makes inspection teachable, but knowing an apparently obvious rule is not the same as recognizing its violations in a concrete design.

## Mechanism as an Idea

Evaluators wrote reports identifying problems as precisely as possible. The authors matched those reports to an author-created inventory, giving credit even for incomplete descriptions. They **expanded the inventories after reading reports** because evaluators found problems the authors had missed. Detection percentages therefore use the final **known-problem inventory**, not an independently established exhaustive truth set.

### Four experiments and their denominators

| Interface | Evaluators and stimulus | Known problems | Mean individual detection |
|---|---|---|---|
| Teledata | **37 computer-science students**, taught the heuristics; ten screen dumps from Danish videotex general search and an airline subsystem, no live system | **52** | **51%** |
| Mantel | **77 contest submissions**, mostly industrial computer professionals; a one-page specification of a fictitious telephone-number lookup system, no heuristics lecture | **30** | **38%** |
| Savings | **34 computer-science students**, taught the heuristics; live touch-tone telephone account/information system | **48** | **26%** |
| Transport | **The same 34 students**; live touch-tone bus-route information system | **34** | **20%** |

There are **four experiments, 182 evaluator–interface evaluations, and 148 distinct evaluators** across the three pools, not 182 independent people. Four cross-system inconsistency problems appear in both telephone inventories. Thus the displayed **164 problem entries** are not 164 distinct, independent defects.

Aggregation uses each evaluator's independent findings to form a union. Figure 3's sorted evaluator-by-problem matrices show that even low-total evaluators sometimes detect hard problems that high-total evaluators miss. Problem sets are not perfectly nested, so the aggregate can exceed its best member rather than merely duplicate that member's expertise.

## Results / Admissions

### Exact aggregate results

Table 4 reports mean detection for **hypothetical random aggregates**, estimated by **5,000–9,000 Monte Carlo draws per size and experiment**. These are not observed collaborative teams or fresh user tests.

| Evaluators in aggregate | Teledata | Mantel | Savings | Transport |
|---|---|---|---|---|
| **1** | **51%** | **38%** | **26%** | **20%** |
| **2** | **71%** | **52%** | **41%** | **33%** |
| **3** | **81%** | **60%** | **50%** | **42%** |
| **5** | **90%** | **70%** | **63%** | **55%** |
| **10** | **97%** | **83%** | **78%** | **71%** |

The five-person improvement over one person is **39, 32, 37, and 35 percentage points**, respectively. The authors summarize five-person coverage as about two thirds, but actual values span **55–90%**. Figure 4 rises steeply through about five evaluators and flattens around ten; it does not establish a universal optimal staffing number or a fixed discovery probability.

Individual ranges are **22.6–74.5%** Teledata, **0–63.3%** Mantel, **10.4–52.1%** Savings, and **6.7–46.7%** Transport. Mantel's second-lowest result was **6.7%**. Upper-to-lower quartile ratios are **1.4, 1.6, 1.7, and 2.2**, showing substantial variation within the pools. For the same students evaluating both voice systems, performance is related at **R² = .33, p < .01**, excluding the four shared inconsistency problems. The authors call this very weak; retain the statistic rather than treating that characterization as a negligible correlation.

The matrices approximately fit a Guttman scale (**mean reproducibility .85**, range **.82–.87**), but marginal prediction already achieves **.80** (range **.79–.82**) and scalability is only **.06**. The useful conclusion is complementarity, not a clean universal ranking of inspectors or problems.

### What the study does not establish

- **No traditional user test validates the inventory.** The authors appeal to established usability knowledge and the large evaluator pool, while explicitly admitting the next person might find something new. Inspectors' complaints are not equivalent to measured user failures.
- False positives were described as few, but **no formal false-positive analysis** was performed. The suggestion that colleagues will reject a lone false alarm is experience-based, not a validated adjudication rule.
- Perfect recognition and merging of findings is an **untested assumption** of simulated aggregation. A real meeting can lose findings or fail to agree.
- Independence is recommended because joint inspection could anchor people to the same approach; **independent versus joint work was not experimentally compared**.
- Low persistence of spoken messages is offered as an explanation for poorer telephone-system detection. Modality, interface, and population differences are not isolated treatments.

The authors recommend **three to five independent evaluators**, then spending additional resources on other methods such as thinking-aloud testing. They acknowledge that inspection can identify a problem without a repair and tends not to generate design breakthroughs. The broader [evaluator-effect review](/dossiers/evaluator-effect-usability-evaluation-methods.md) subsequently corroborates disagreement across methods; it is not a replication of these exact four coverage curves.

## Analyst Takeaways

1. **Preserve independent discovery before discussion.** Complementary findings supply the value of aggregation; consensus is a later judgment, not the initial discovery instrument.
2. **Report the denominator.** A percentage of known problems is inventory coverage, not the probability of finding every real barrier or the fraction of actual users who will fail.
3. **Treat staffing guidance as bounded evidence.** Three to five is a pragmatic recommendation from small interfaces and largely nonexpert pools, not a law for complex products.
4. **Use inspection and observation for different questions.** Inspection broadens hypotheses; actual use can establish consequences, false alarms, and priorities under a specified context.
5. **Do not select solely by total findings.** Even a low-total evaluator can contribute a unique issue; inspection ability also varies by system.

## Questions and Limitations

- Small interfaces, novice-heavy student pools, self-selected contest entrants, and differing training limit generalization. Expertise benefits are conjectured, not tested here. No confidence intervals are supplied for aggregate estimates.
- Problem matching and inventory revision involve author judgment. Severity-specific coverage is not reported in this paper; later reanalyses should be labelled separately.
- The text introducing Table 3 says **“five experiments,”** although the study and table contain **four**. This is an internal count error, not evidence of an omitted experiment.
- The ACM notice states **“Permission to copy without fee all or part of this material is granted”** subject to noncommercial use, retaining notice/title/date, and acknowledging permission; it also states **“To copy otherwise, or to republish requires a fee and/or specific permission.”** This conditional copying permission does not establish permission for public repository republication. The supplied copy is treated as private, retaining the canonical DOI URL.

## Vault Ideas Extracted

- [Heuristic Evaluation](/vault/heuristic-evaluation.md) — Supplies the compact-inspection model, independent-discovery rationale, exact simulated aggregation rates, and the distinction between coverage and validation.
- [Evaluator Effect](/vault/evaluator-effect.md) — Provides four original experiments showing non-nested findings and system-dependent individual detection, with inventory and aggregation assumptions made explicit.
