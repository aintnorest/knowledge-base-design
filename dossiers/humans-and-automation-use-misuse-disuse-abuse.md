---
type: Study Note
title: "Humans and Automation: Use, Misuse, Disuse, Abuse"
description: A review distinguishes automation use, overreliance, underuse, and design or management abuse, showing that reliability, workload, feedback, and alarm base rates interact rather than making human supervision uniformly effective.
resource: https://doi.org/10.1518/001872097778543886
source: https://doi.org/10.1518/001872097778543886
tags: [delegation, trust, human-performance, decision-making, digital-interfaces, survey]
timestamp: 2026-10-12T23:54:32Z
---

# Humans and Automation — Study Notes

**Authors**: Raja Parasuraman and Victor Riley.  
**Published**: Human Factors **39(2), June 1997, pp. 230–253**; received June 17, 1996; accepted November 11, 1996.  
**Status**: Peer-reviewed theoretical, empirical, and analytical review. Read the complete **24-page image-only ProQuest scan**, with every page OCRed and all three figures inspected visually. DOI verified against Crossref's matching title, authors, volume, and pagination.  

## What It Is

A framework for analyzing four different relationships with automation, not a new participant experiment:

- **Use**: voluntarily engaging or disengaging automation.
- **Misuse**: overreliance, including inadequate monitoring and inappropriate acceptance of automated decisions.
- **Disuse**: neglect or underutilization, including ignoring or disabling useful alarms.
- **Abuse**: designers or managers applying automation without adequate regard for the resulting human role, performance, and authority.

The labels are explicitly **not intended to assign blame**. Designers, managers, regulators, and operators are all human participants in the system. Automating an operation changes work and redistributes error; it does not remove human fallibility.

## Problem and Motivation

Technological feasibility and subsystem economics often determine what is automated, leaving people an accidental collection of supervisory tasks. The authors ask whether the resulting human–machine system performs well, especially when normal operation gives way to unexpected conditions.

Aviation, manufacturing, medicine, transportation, and process control supply examples. The review deliberately focuses on **individual task performance**, not a full theory of teams, organizations, employment, or sociopolitical effects. Accident narratives reveal plausible failure pathways but are multicausal and cannot, by themselves, prove that a particular operator used automation too much or too little.

## Mechanism as an Idea

### Use depends on competing costs and beliefs

Reliance reflects trust, confidence in manual ability, perceived risk, fatigue, task complexity, learned automation states, and the overhead of configuring or evaluating an aid. Figure 1 distinguishes **experimentally supported solid arrows** from **hypothesized or system-dependent dashed relationships**; the diagram is not an estimated universal causal model.

High workload does not necessarily produce more automation use. Engaging an aid can require immediate work precisely when spare capacity is unavailable. Predictable future work may justify that investment; rapidly changing conditions may not. Kirlik's cited dual-task flight study and Markov analysis show that an apparently helpful aid can rationally go unused when engagement costs and secondary-task delay are included.

Trust is important, but subjective attitude is not actual reliance. General automation questionnaires did not consistently predict multitask usage. Trust may also compete with overconfident judgments of one's own performance.

### Misuse includes decisions and monitoring

**Omission errors** arise when people do not notice or act because an aid fails to signal a problem. **Commission errors** arise when they follow an inappropriate automated directive. Cited cockpit simulations found automated cues could replace information seeking, including inspection of contradictory evidence; professional expertise did not guarantee immunity.

Monitoring suffers when reliable automation competes with manual tasks for attention. Looking near an automated display is not equivalent to allocating attention to it. Integrating relevant variables into an emergent normal-state pattern can reduce detection demands, whereas central placement or visual superimposition alone did not remove the cited monitoring deficit.

High autonomy can reduce manual practice and state understanding. Lower confidence then encourages still more reliance: a proposed reinforcing loop, not a quantified inevitable trajectory.

### Disuse depends on predictive value, not just sensitivity

An alarm's hit rate, its false-positive rate among safe states, and the probability that an emitted alarm indicates real danger are different quantities. With rare hazards, a sensitive detector can still produce mostly false alarms. Repeated unnecessary responses can undermine trust and future use; their downstream behavioral costs belong in the design tradeoff.

The source also distinguishes nuisance alarms from useful early indications that a collision is possible. It recommends considering graded likelihood alarms rather than making every warning a definitive assertion of danger. That recommendation is not a universal experimentally established alarm policy.

### Abuse changes the entire supervisory role

Automation can substitute a designer's assumptions for an operator's judgment, or enforce management's operating policy. A protection may prevent one foreseeable human mistake while blocking recovery when its sensing assumptions fail. Defining operator duties and authority deliberately is therefore different from leaving a person to oversee whatever could not be automated.

## Results / Admissions

The paper synthesizes the following evidence; it does **not** recruit a new sample or supply a pooled effect estimate. Most cited studies' sample sizes, uncertainty intervals, and inferential statistics are not reported here.

| Evidence cited in the review | Tasks and measures | Reported result and boundary |
|---|---|---|
| Riley 1994a/1996, students and pilots | Manual step tracking plus automatable character classification; automation engagement | Tracking difficulty did not predict use in either group; students used automation **less than about 50%** of the time. The authors admit the workload manipulation may have been weak and tasks artificial. |
| Riley 1994b, students versus pilots | Dual-task performance with failed automation; disengagement and performance | Almost all students disengaged failed automation, but **almost half the pilots did not**. No sample denominator or effect statistic is supplied; a nonaviation task limits domain interpretation. |
| Mosier et al. 1994, ASRS incident reports | Reports where overreliance was suspected; probable monitoring failures | **77%** involved a probable monitoring failure. This is conditional on a selected incident category, not 77% of all aviation accidents or a causal risk estimate. |
| Parasuraman et al. 1993/1994 | Tracking and fuel management plus engine-status monitoring; detection of malfunctions missed by automation | Manual engine monitoring detected **more than 70%**; automated monitoring under constant reliability declined markedly. Monitoring alone yielded **over 95%** detection. Figure 2 shows variable-reliability detection roughly **60–90%**, versus roughly **20–40%** under constant reliability across nine **10-minute blocks**; these are visual ranges, not exact digitized means. |
| Molloy and Parasuraman 1994; Molloy et al. 1995, pilots and nonpilots | Baseline circular gauges versus integrated deviation-bar engine display; automation-failure detection, with manual performance initially equated | Baseline detected **about one-third** of failures; the integrated display detected **twice as many**. No complete group sizes, confidence intervals, or exact test statistics are supplied. |
| Parasuraman et al. 1996 and related pilot study | Multitask flight simulation; temporary return of engine monitoring to manual control | After **40 minutes** automated, **10 minutes** manual improved subsequent failure detection. Experienced-pilot corroboration is cited; no quantitative improvement estimate is given. |
| Getty et al. 1995 | Visual warning during tracking; response latency | Responses grew slower as warning predictive value declined from **.75 to .25**. The review does not provide response-time means or participant counts. |

The monitoring findings were extended to **experienced pilots** and a simulation with **a single automation failure**, not only novice participants or frequent faults. These are cited corroborations of the mechanism under changed conditions, not independent replication of this entire review or all its proposals.

The Bayesian alarm example, reproduced in Figure 3, fixes sensitivity at **d′ = 4.7**, hit rate **.999**, false-positive rate **.0594**, and hazard base rate **.001**. The reported posterior probability of a real hazard given an alarm is **.0168**, approximately **one true hazard in 59 alarms**. This is an analytical illustration from a cited paper, not an observed operational alarm dataset. It explains why high detection sensitivity alone cannot establish usable warning reliability.

The authors recommend low engagement/disengagement overhead, operator education, salient and informative feedback, active involvement, and consideration of both alarm thresholds and hazard base rates. They also admit exhaustive feedback can create an **information explosion** and that adaptive allocation can reproduce conventional automation problems if technology, rather than the human role, drives it.

## Analyst Takeaways

1. **Evaluate reliance as behavior, not approval.** Positive attitudes, expertise, and high workload do not reliably imply appropriate use.
2. **Design the residual job.** A person responsible for catching failures needs attention capacity, state understanding, practical authority, and a viable intervention path—not merely a nominal override.
3. **Separate attention capture from comprehension.** [System-status visibility](/vault/visibility-of-system-status.md) must both invite inspection and supply the information needed to act. Display proximity alone is insufficient.
4. **Include future distrust in alarm costs.** A false alarm can affect the response to later real alarms; sensitivity and per-event inconvenience are incomplete metrics.
5. **Do not interpret underuse automatically as irrational resistance.** Configuration and verification costs can exceed an aid's benefit.

For supervising software automation or AI agents, these are **extrapolations** from aviation, process-control, and artificial-task evidence: expose consequential state and independent evidence, preserve correction authority, and assess whether concurrent work leaves realistic capacity for review. The paper does not test generative AI, code agents, or a specific modern approval workflow.

## Questions and Limitations

- This is a narrative synthesis, not a systematic review with reproducible searches, inclusion rules, or meta-analysis. Many cited results lack participant counts, protocols sufficient for reconstruction, exact statistics, or uncertainty estimates.
- Accident examples are multicausal; the authors themselves warn against declaring operator reliance clearly wrong simply because an accident followed.
- Workload–use evidence is explicitly mixed. Continued reliance after failures also conflicts across cited studies; reliability, visibility, engagement cost, complexity, and task strategy are suggested explanations, not isolated causes.
- The human-centered recommendation of full operator authority is a design position, not an experimentally demonstrated rule for every time-critical or fully automated system.
- The printed discussion says high-autonomy systems can act “only with initiating input” yet subsequently describes functions that cannot be overridden. Initiation, authority, and autonomy should be separated rather than treating that phrase as a precise operational scale.
- The source cites **Tversky and Kahneman (1984)** for the familiar *Science* **185, 1124–1131** heuristics article; those volume/pages correspond to **1974**, an internal bibliographic year inconsistency, not evidence of a distinct 1984 experiment.
- **Redistribution evidence**: the first page states **“© 1997, Human Factors and Ergonomics Society. All rights reserved.”** The scan footer states **“Reproduced with permission of the copyright owner. Further reproduction prohibited without permission.”** That is a restriction, not a transferable redistribution grant. Archive the raw scan privately.

## Vault Ideas Extracted

- [Appropriate Reliance on Automation](/vault/appropriate-reliance-on-automation.md) — Distinguishes use, misuse, disuse, and abuse and supplies attention, engagement-cost, and alarm-base-rate evidence for context-sensitive reliance; feedback must be salient and actionable rather than voluminous.
- [Out-of-the-Loop Supervision](/vault/out-of-the-loop-supervision.md) — Supplies multitask monitoring deficits, pilot and single-failure corroboration, and bounded evidence for integrated displays and temporary manual involvement.
