---
type: Study Note
title: "The Evaluator Effect: A Chilling Fact about Usability Evaluation Methods"
description: Eleven studies show that evaluators using the same usability method often find substantially different problems, but agreement measures establish reliability rather than real-world validity or exhaustive coverage.
resource: https://doi.org/10.1207/S15327590IJHC1304_05
source: https://doi.org/10.1207/S15327590IJHC1304_05
tags: [usability-evaluation, ux-metrics, user-research, digital-interfaces, survey]
timestamp: 2026-10-11T23:50:47Z
---

# The Evaluator Effect — Study Notes

**Authors**: Morten Hertzum and Niels Ebbe Jacobsen.  
**Published**: International Journal of Human–Computer Interaction **13(4), 2001, pp. 421–443**; reprinted in **15(1), 2003**, under DOI 10.1207/S15327590IJHC1501_14.  
**Status**: Review of empirical usability-evaluation studies; the version read is the **17-page author preprint**, whose first line explicitly identifies the 2001 volume, issue, year, and pages. It therefore matches and is keyed to the original **10.1207/S15327590IJHC1304_05**, not treated as a separate 2003 work.  

## What It Is

A review and partial reanalysis of **11 studies**, comprising **18 experiments**, on cognitive walkthrough (CW), heuristic evaluation (HE), and thinking-aloud usability studies (TA). Its central finding is that even when evaluators use the same method on the same system, their problem lists differ substantially. Where pairwise data are available, **average any-two agreement ranges from 5% to 65%**.

This is not a claim that usability evaluation is useless. It is a challenge to the assumption that one evaluator's report—especially a user test—is an authoritative map of an interface's problems. Observer judgment remains part of the instrument even when users perform concrete tasks on video.

## Problem and Motivation

Method comparisons often treat user testing as a gold standard without asking whether another observer would extract the same problems. Inspection methods explicitly involve judgment, but walkthrough questions and observed user behavior can create a misleading impression that interpretation has been eliminated.

The paper separates **reliability**—independent evaluations yielding the same result—from **validity**—reported problems corresponding to difficulties in actual use. The evaluator effect measures the former. Disagreement alone cannot tell whether evaluators missed real problems, reported false alarms, or chose different scopes.

## Mechanism as an Idea

### Two measures with different denominators

**Detection rate** averages each evaluator's number of unique problems divided by the union found by all evaluators. Its lower bound is **1/n**, not zero: with two evaluators it cannot fall below **50%**, and with one it is automatically **100%**. Increasing the evaluator pool can lower the apparent individual rate merely by enlarging the denominator. The collective union is also not known to contain every actual problem.

**Any-two agreement** averages the intersection divided by the union for **every pair** of evaluators: the Jaccard overlap of their problem lists. It ranges from **0% to 100%** and avoids making the size of the full evaluator pool the denominator. It is the authors' preferred measure, but data are unavailable for some reviewed studies. High agreement still does not demonstrate complete coverage or validity, and the statistic is not chance-corrected agreement.

Both measures depend on adjudicating whether differently worded findings are the same problem. Broad merging increases apparent agreement and coverage; finely distinguished problem instances can lower them. This is substantive measurement work, not an innocuous cleanup operation.

### Why evaluators diverge

The authors propose three interacting sources of variability:

- **Vague goal analysis**: evaluators choose different tasks or system areas. In one two-person walkthrough study, **43%** of findings detected by one and missed by the other came from tasks only one evaluated. Identical scenarios reduce this source but do not eliminate the effect.
- **Vague procedures and anchoring**: broad heuristics inspire different inspection paths; walkthrough evaluators can substitute their own experience for an underspecified target user's capabilities. Diaries from two novice walkthrough evaluators showed that problems credited to the walkthrough had already been experienced during preparation, sometimes **15 hours earlier**. This supports a possible anchoring pathway; its extension to thinking-aloud observation is explicitly hypothetical.
- **Vague problem criteria**: the same inconvenience can fall above one observer's threshold and below another's. Greater formality may clarify thresholds but create fatigue and slips; some walkthrough evaluators skipped actions inadvertently. Agreement can also improve by excluding problem classes that matter in practice.

The mechanism is **interpretive judgment under incomplete specifications**, not simply ignorance of the method. Experience can increase findings without making different experts report identical sets.

## Results / Admissions

### The 11-study evidence base

The following records preserve the study-level denominators. **Detection / severe** refer to individual detection rates against that study's collective union; **agreement** is any-two overlap. A dash means unavailable, not zero.

| Study and method | System, evaluator sample, and collectively detected problems | Detection / severe | Agreement |
|---|---|---|---|
| Lewis et al. 1990, CW | Email; **4 evaluators**, three CW developers and one CE+ novice; **20 problems**; set tasks | **65% / —** | — |
| Dutt et al. 1994, CW | Personnel recruitment; **3 evaluators**, two CS graduate students and an HCI researcher; **32**; set tasks | **73% / —** | **65%** |
| Hertzum & Jacobsen 1999, CW | Web library; **11 CS graduate students**, first-time CW users; **33**; set tasks | **18% / 21%** | **17%** |
| Jacobsen & John 1999, CW | Multimedia authoring; **2 CS graduate students**; **46**; independently chosen tasks | **53% / —** | **6%** |
| Nielsen & Molich 1990, HE | Savings: **34 CS students, 48 problems**; Transport: **34, 34**; Teledata: **37, 52**; Mantel: **77 computer professionals, 30**; no set tasks | Savings **26% / 32%**; Transport **20% / 32%**; Teledata **51% / 49%**; Mantel **38% / 44%** | Savings **26%**; Mantel **45%**; others — |
| Nielsen 1992, HE | Banking; **16 problems**; **31 novices**, **19 usability specialists**, **14 usability-and-domain specialists**; no set tasks | Novices **22% / 29%**; specialists **41% / 46%**; double specialists **60% / 61%** | Specialists **33%**; others — |
| Nielsen 1994a, HE | Complex integrating application prototype; **11 usability specialists**; **40**; set tasks | **29% / 46%** | — |
| Connell & Hammond 1999, HE | Hypermedia browser: **8 undergraduates, 33 problems**, or **5 HCI researchers, 84**; interactive teaching: **8 psychology undergraduates, 57**; no set tasks | Browser **18% / 19%**, researchers **24% / 22%**; teaching **20% / 16%** | **9%, 5%, 8%**, respectively |
| Jacobsen et al. 1998, TA | Multimedia authoring; **4 HCI researchers** observing the same **4 users' videotaped sessions**; **93**; set tasks | **52% / 72%** | **42%** |
| Molich et al. 1998, TA | Electronic calendar; **3 commercial usability laboratories**; **141**; no common set tasks | **37% / —** | **6%** |
| Molich et al. 1999, TA | Web email; **6 usability laboratories**; **186**; no common set tasks | **22% / 43%** | **7%** |

These are heterogeneous descriptive studies, not a pooled meta-analytic estimate or randomized comparison proving that all methods are equivalent. Six directly investigated evaluator effects, two addressed them more broadly, one supplied usable published data, and two required additional data from their authors. No method consistently dominates across the reviewed settings.

### The strongest isolation of observer interpretation

Jacobsen et al.'s TA study holds users, tasks, and footage constant. The four researchers used **nine predefined problem criteria**, had unrestricted analysis time, and reported timestamped evidence. Two researchers creating the master list agreed on **86%** of problem tokens before resolving disagreements. Nevertheless, **46%** of the final problems were reported by only one evaluator and another **20%** by only two.

The two more experienced evaluators averaged **59% detection** and **40% pairwise agreement**; the less experienced pair averaged **45% detection** and **39% agreement**. Experience improved quantity more clearly than convergence. Figure 1 shows one evaluator observing all four users found about **48 problems**, whereas the four together found **93**. Adding evaluators increased findings by **42%** from one to two, **20%** from two to three, and **13%** from three to four.

The inter-laboratory studies are more confounded: different labs also varied users and procedures. In the calendar evaluation **129/141** problems were reported by only one laboratory; in web email **147/186** were. These demonstrate practical variability, not a pure observer-only treatment effect.

### Severe problems and severity judgments

Across **14 experiments** assessing severity, only **four** show appreciably better individual detection of severe problems; **ten** show largely no difference. The effect is not confined to cosmetic complaints. Severity definitions vary: expected impact, release-blocking problems, a selected top ten, predefined core problems, or the upper three values of a seven-point scale.

When rating a common problem inventory, average pairwise Spearman correlations are only **.31** for six CW evaluators (**SD .18**), **.24** for eleven HE specialists, and **.23** for four TA researchers (**SD .16**). Agreement about which problems are severe is **28% CW** and **20% TA**; it was not available for HE. No problem was unanimously rated severe in the CW and TA studies. Selecting a top ten exposes different prioritization strategies, not just different detection skills.

### Recommendations and subsequent corroboration

The authors recommend explicit goals and task coverage, at least one additional evaluator for critical evaluations, and periodic reflection on procedures and problem criteria. Independent extra observers add findings and expose disagreements. The review did **not** find studies evaluating collaborative CW teams or HE groups' final merged outputs, so the reliability of collaboration and consensus cannot be inferred from the independent-inspection results.

A proposed relationship, problems found approximately proportional to the **square root of users × evaluators**, comes from only **four users and four evaluators**. It motivates considering an additional evaluator instead of additional users, but does not justify a universal staffing ratio or extrapolation to large samples; evaluator costs are normally higher.

Later corroboration is reported in [Molich's 2018 CUE retrospective](https://doi.org/10.1145/3278154), whose [author-hosted full text](https://www.dialogdesign.dk/tekster/are_usability_evaluations_reproducible.pdf) describes CUE-9: **35 evaluators** in US and German groups independently analyzed the same **five videos** of truck-rental usability sessions and still reported different issues. This extends the fixed-footage finding beyond the four-observer example; it is not a replication of every original method or the review's exact **5–65%** range. The retrospective table combines problems and positive findings, so its **223 issues** should not be quoted as 223 independently verified usability defects.

## Analyst Takeaways

1. **Sample interpreters as well as users.** More user sessions do not remove an observer's blind spots. A second independent interpretation is especially valuable for high-consequence decisions.
2. **Do not turn the union into ground truth.** It is a discovery inventory, not an exhaustive count; agreement, coverage, and validity require distinct claims and evidence.
3. **Preserve disagreement through prioritization.** A merged problem list does not automatically create agreement about severity. Explain the user harm and prioritization basis rather than treating one rating as a release mandate.
4. **Standardize purpose before standardizing paperwork.** Shared target users, task coverage, and criteria can remove avoidable variability; excessive procedure can reduce attention without producing better judgment.
5. **Treat a low overlap as a reason to investigate, not suppress findings.** A unique finding may reflect a missed serious problem. Conversely, consensus may reflect shared blind spots rather than truth.

## Questions and Limitations

- The review supplies descriptive rates, not pooled confidence intervals, controlled causal estimates, or a reproducible systematic-search protocol. Several samples are small, novice-heavy, or unusually close to the method's creators.
- Lewis et al.'s CW developers had discussed the trends in the user evaluation beforehand; their relatively good agreement is not clean independent validation. Dutt et al.'s high overlap may coexist with missed problems or high reporting thresholds.
- Problem matching itself involves an evaluator effect: master-list construction agreement was **80%** in the library CW study and **86%** in the fixed-video TA study before consensus. Different grouping granularity can materially change the statistics.
- None of the reviewed studies separates inter-evaluator differences from the same evaluator's inconsistency on repeat evaluation. The effect should not be attributed wholly to stable personalities.
- The authors' proposed causes are explanatory hypotheses with some supporting examples, not three experimentally isolated causal effects. Anchoring in thinking-aloud analysis remains specifically conjectural.
- The original paper says validity has not been investigated to the authors' knowledge; that is a **2001 admission**, not a timeless statement that later research has provided no validity evidence.
- Tight problem criteria can improve agreement while excluding meaningful harms; reporting quotas and divergent scopes can also reduce overlap without implying incompetence. Neither zero disagreement nor maximal problem count is a sufficient evaluation objective.

## Vault Ideas Extracted

- [Evaluator Effect](/vault/evaluator-effect.md) — Defines pairwise overlap, distinguishes reliability from coverage and validity, and supports independent multiple-evaluator analysis across inspection and user-testing methods.
