---
type: Study Note
title: A Model for Types and Levels of Human Interaction with Automation
description: A qualitative framework separates four automation functions and their levels of authority, recommending choices based on human performance, reliability, and consequences rather than a universal optimum or a single autonomy score.
resource: https://doi.org/10.1109/3468.844354
source: https://doi.org/10.1109/3468.844354
tags: [delegation, decision-making, human-performance, interaction-design, digital-interfaces, taxonomy]
timestamp: 2026-10-12T23:54:32Z
---

# Types and Levels of Automation — Study Notes

**Authors**: Raja Parasuraman, Thomas B. Sheridan, and Christopher D. Wickens.  
**Published**: IEEE Transactions on Systems, Man, and Cybernetics—Part A: Systems and Humans **30(3), May 2000, pp. 286–297**; received January 26, 1999; revised February 7, 2000.  
**Status**: Peer-reviewed conceptual model and research synthesis. Read the complete **12-page publisher-layout course-hosted copy**, including Table I, Figures 1–4, references, and author biographies. Crossref confirms the DOI and matching bibliographic identity; the PDF prints publisher item identifier **S 1083-4427(00)03579-7**.  

## What It Is

A framework for asking **which functions to automate and to what extent**. It rejects both binary manual/automatic descriptions and a single overall autonomy score. A system may automate information gathering heavily while leaving interpretation, consequential decisions, or execution under different degrees of human control.

This is **a qualitative design guide**, not a validated algorithm for calculating an optimal level. Its contribution combines functional decomposition with criteria for evaluating the resulting human–machine system.

## Problem and Motivation

Technical capability and cost do not reveal whether the new division of work is usable or safe. Automation changes human activity and adds coordination demands. Optimizing individual subsystems can leave operators with an incoherent residual job and does not necessarily optimize the whole system.

Examples range from anesthesiology and financial analysis to air defense, cockpit systems, air traffic control, process plants, and telerobotics. The authors' worked application concerns future **air traffic control (ATC)**; its recommendations are illustrations, not measured outcomes of deploying the proposed system.

## Mechanism as an Idea

### Four functions, each with its own level

| Function | What is automated | Important distinction |
|---|---|---|
| **Information acquisition** | Sensing, registering, organizing, highlighting, or filtering inputs | Highlighting preserves access to unselected raw data; exclusive filtering may not. |
| **Information analysis** | Prediction, integration, inference, and context-dependent summaries | Supporting interpretation is different from choosing an action and its implicit values. |
| **Decision and action selection** | Generating, narrowing, recommending, or selecting alternatives | Recommendations and autonomous choices distribute decision authority differently. |
| **Action implementation** | Executing the selected response | Choosing an action and committing its effects can remain separately controlled. |

Figure 1 maps these to sensory processing, perception/working memory, decision making, and response selection. The authors explicitly concede this is a **gross simplification**: real processing overlaps and perception–action cycles are not a strict serial chain. Figure 2's two hypothetical profiles demonstrate that levels can differ across functions; neither profile is an empirical optimum.

### The ten-level decision/action scale

Table I adapts Sheridan's earlier scale; **higher is more computer authority, not automatically better**:

| Level | Allocation of authority |
|---|---|
| **1** | No computer assistance; the person makes all decisions and actions. |
| **2** | Computer offers a complete set of alternatives. |
| **3** | Computer narrows the alternatives to a few. |
| **4** | Computer suggests one alternative. |
| **5** | Computer executes its suggestion if the person approves. |
| **6** | Computer executes unless the person vetoes within a restricted interval. |
| **7** | Computer executes automatically and necessarily informs the person. |
| **8** | Computer informs the person only if asked. |
| **9** | Computer informs the person only if it decides to. |
| **10** | Computer decides everything and acts autonomously, ignoring the person. |

The authors **do not specify equivalent ten-level scales** for acquisition, analysis, and implementation. Those dimensions may require different numbers and definitions of levels. Applying this exact ladder mechanically to every function would contradict the stated limitation.

### Evaluate the whole allocation, including failure

Figure 3 makes selection iterative. Primary criteria are consequences for **mental workload, situation awareness, complacency, and skill degradation**. Secondary criteria include **automation reliability** and **costs of decision/action outcomes**; integration, safety–efficiency tradeoffs, operating costs, and liability also matter.

The authors describe recommended levels as **upper bounds, not required targets**. A lower bound can also arise if acceptable performance requires some automation. The paper's level **4–6** example is explicitly hypothetical, not an observed safe operating range.

Reliability includes failures of modeled assumptions in an actual situation, not just component failure frequency. A high mean reliability estimate does not describe all uncertainty or correlated system interactions. Likewise, information automation is not intrinsically harmless: an incorrect cue can divert attention from relevant uncued evidence.

## Results / Admissions

There is **no original participant sample, intervention comparison, pooled effect size, or statistical validation of the four-dimensional framework**. The evidence comes from cited laboratory, simulation, field, incident, and modeling work.

- **Workload can improve or worsen.** Cited predictor-display work found reduced pilot workload and better hazard detection; information integration can remove search and projection work. Difficult configuration and data entry can instead produce “clumsy” automation. The paper provides no study-level participant counts or quantitative workload effects for these examples.
- **Decision automation can impair situation awareness.** Cited dynamic-system studies found less awareness when another agent made changes. A telerobotic hazardous-material handling simulation found better post-malfunction performance at an intermediate decision-automation level than at higher levels. No exact level-specific means or effect statistics are reproduced.
- **Reliable automation can reduce monitoring under competing tasks.** Parasuraman and colleagues' cited work shows greater vulnerability during multitasking than when automated monitoring is the sole task. Skill decay with disuse and reduced situation awareness together create **out-of-the-loop unfamiliarity**, but they are distinct mechanisms.
- **Function matters when automation is wrong.** Crocoll and Coury's cited decision-aiding study compared status information with recommendations. Both helped equally when perfectly reliable; incorrect recommendations caused greater performance harm than incorrect status information. The authors explicitly say this is the **only direct stage comparison available to them** and call for further research. It does not validate a universal ordering of all four functions.
- **Access to raw data and feedback can support calibration.** Two cited information-automation studies found fairly rapid adjustment to occasional errors when feedback was available. This supports considering high information automation with inspectable original data and known unreliability, not guaranteeing that every summary or filter is safe.
- **Execution friction can trap errors but also introduce them.** Cited cockpit data-link studies found more decision errors caught with less automated entry than with a single accept action. Manual entry increases workload and can introduce new mistakes; the paper supplies no complete sample sizes or exact detection-rate estimates.

### What the source recommends

For its ATC illustration, Figure 4 permits high acquisition and analysis automation **if reliability is demonstrated**, high decision authority for **low-risk functions**, and lower decision authority for high-risk choices when people must remain capable of recovery. If consequential selection is highly automated, some human action at implementation can provide a final error-trapping opportunity.

This is **conditional guidance**, not a universal approval requirement. High authority may be justified when a human cannot respond in time, as with rapid reactor shutdown or ground-collision avoidance. Full automation can also be appropriate if the operator is **not expected to rescue failures**, but the footnote stresses the demanding requirement to handle known and unforeseen anomalies reliably. When human takeover is required, the burden is on designers to demonstrate that the allocation does not undermine awareness, monitoring, and skills.

Adaptive automation can change type or level with the situation, but the paper deliberately leaves its complex ancillary issues largely outside scope. It does not evaluate a dynamic allocation policy.

## Analyst Takeaways

1. **Describe an automation profile, not a single autonomy label.** Gathering evidence, interpreting it, recommending, choosing, and executing carry different responsibilities.
2. **Evaluate degraded operation, not just normal throughput.** Someone expected to rescue the system must remain able to understand and act when automation becomes unreliable.
3. **Keep source evidence distinguishable from derived conclusions.** Highlighting and exclusive filtering are not interchangeable; [status visibility](/vault/visibility-of-system-status.md) should preserve the basis for checking an aid when appropriate.
4. **Make approval meaningful rather than ceremonial.** Lower implementation automation can enable [error trapping](/vault/error-prevention-and-recovery.md), but the source's manual-entry evidence does not show that an extra confirmation always improves decisions.
5. **Treat authority as a consequence-sensitive choice.** Human review may be essential in one function and an unsafe delay in another.

Applying this decomposition to supervising AI or software agents is an **extrapolation beyond the studied systems**. It can distinguish retrieval, synthesis, recommendation, and external commitment, but the historical studies do not validate a modern AI-specific ten-level scale or prove a particular approval architecture.

## Questions and Limitations

- The model supplies no weights for balancing workload, awareness, skill, reliability, cost, or liability, and no quantitative method for selecting a level. The authors explicitly admit both gaps.
- The nondecision dimensions are not operationalized as complete ladders. Little empirical research then directly compared levels of acquisition and analysis automation; technological changes may require revised categories.
- Stages are functionally useful distinctions, not independent cognitive modules. Decision and implementation are explicitly interdependent in the high-risk error-trapping discussion.
- Evidence is narratively selected and heterogeneous; many study details and statistics are omitted. Cited findings are not new replications, and this dossier establishes no independent replication of the framework's recommendations.
- A terminology inconsistency appears in the error-trapping paragraph: reduced **“action selection”** automation describes entering data-linked flight information, operationally the paper's **action implementation** dimension. Retain the functional distinction rather than propagating that label.
- Table I's **level 7** requires automatic execution and notification, while the text describes auto-GCAS at level 7 as taking control **“if the pilot does not.”** That contingent intervention example does not cleanly map to every detail of the table; levels are illustrative, not an unambiguous certification scheme.
- **Redistribution evidence**: the first page prints **“1083-4427/00$10.00 © 2000 IEEE.”** No Creative Commons or equivalent public redistribution grant appears. Course hosting does not supply such permission; archive the raw PDF privately.

## Vault Ideas Extracted

- [Levels of Automation](/vault/levels-of-automation.md) — Supplies the four functional dimensions, ten-level decision/action ladder, iterative evaluative criteria, and upper-bound rather than target interpretation.
- [Out-of-the-Loop Supervision](/vault/out-of-the-loop-supervision.md) — Separates situation-awareness loss, monitoring deficits, and skill decay and makes takeover capability a condition of authority allocation.
- [Appropriate Reliance on Automation](/vault/appropriate-reliance-on-automation.md) — Adds function-specific reliability, action consequence, raw-data access, and time-critical exceptions to reliance decisions.
