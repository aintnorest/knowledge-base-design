---
type: Synthesis
title: Levels of Automation
description: Automation is a profile of function-specific authority rather than a single autonomy score, and suitable levels depend on human performance, reliability, and consequences rather than a universal optimum.
tags: [delegation, interaction-design, decision-making, human-performance, cognitive-load, digital-interfaces]
timestamp: 2026-10-14T21:39:10Z
---

# Levels of Automation

Describe which work is automated and how authority is distributed, not merely
whether a system is manual or autonomous. Gathering information, interpreting it,
selecting a response, and executing it can have different allocations within the
same system. More computer authority is not inherently better.

## Four Functional Dimensions

| Function | Automated work | Design distinction |
|---|---|---|
| **Information acquisition** | Sense, register, organize, highlight, or filter inputs | Highlighting can preserve raw evidence; exclusive filtering can remove it. |
| **Information analysis** | Integrate, predict, infer, or summarize | Supporting interpretation differs from choosing an action and its values. |
| **Decision and action selection** | Generate, narrow, recommend, or select alternatives | Advice differs from authority to choose. |
| **Action implementation** | Execute the selected response | Selection and commitment can remain separately controlled. |

This is a functional decomposition, not a claim that cognition consists of four
independent serial modules. Real perception–action cycles overlap, and selection
and implementation interact.

## Decision and Action Authority

The model adapts a **ten-level** decision/action ladder:

| Level | Allocation |
|---|---|
| **1** | Person makes all decisions and actions without computer assistance. |
| **2** | Computer offers a complete set of alternatives. |
| **3** | Computer narrows alternatives to a few. |
| **4** | Computer suggests one alternative. |
| **5** | Computer executes its suggestion after human approval. |
| **6** | Computer executes unless vetoed within a restricted interval. |
| **7** | Computer executes automatically and necessarily informs the person. |
| **8** | Computer informs the person only if asked. |
| **9** | Computer informs the person only if it decides to. |
| **10** | Computer decides and acts autonomously, ignoring the person. |

The source does **not** supply equivalent ten-level ladders for acquisition,
analysis, and implementation. Those dimensions require their own definitions;
mechanically copying this scale to every function would overstate the model.

## Choose an Allocation, Not a Target Score

The conceptual framework recommends iterative evaluation of mental workload,
situation awareness, complacency, and skill degradation, together with reliability
and the costs of decision/action outcomes. Integration, operating cost, liability,
and safety–efficiency tradeoffs also matter. Recommended levels are **upper
bounds, not required targets**; acceptable performance can also require a lower
bound of some automation.

Reliability includes failures of assumptions in a particular situation, not just
component fault frequency. Information automation can misdirect attention, so it
is not harmless by definition. A cited study found incorrect recommendations more
harmful than incorrect status information, although both helped equally when
perfectly reliable. The source identifies this as its **only direct stage
comparison**, not validation of a universal ranking of all four functions.

When people must rescue failures, authority allocation must preserve actual
monitoring, understanding, and skills; see
[out-of-the-loop supervision](/vault/out-of-the-loop-supervision.md). Some human
participation at implementation may trap decision errors, but manual entry adds
workload and can introduce errors. A confirmation step alone is not a demonstrated
safety improvement.

## Delegating Execution Changes the Residual Job

A **20-student** coding comparison found that greater execution capability took
over environment setup, file handling, command execution, and much debugging.
People increasingly asked what changed and supplied corrective feedback. Initial
implementation was largely generated in both conditions: the shift was not simply
from human-written to generated code, but toward autonomous execution and repair.

Correct completion rose **25% → 60% (p = .02)**. Measured effort among successful
attempts fell **25.1 → 12.5 minutes (p = .01)**, but effort plus autonomous action
averaged **27.9 minutes**, comparable to the less autonomous condition's elapsed
time. The conditions used different effort definitions and excluded unsuccessful
solutions. Reduced active involvement is not equivalent to reduced delivery time.

Understanding, satisfaction, and flow comparisons were nonsignificant;
understanding was self-reported, not tested. These results give direct coding
evidence that automation redistributes work, not an experimentally isolated effect
of autonomy alone: model, interface, environment, and execution support differed.
They do not validate a particular rung of the historical ladder.

## Practical Use

- Specify authority separately for evidence gathering, interpretation, selection,
  and execution, including access to unselected data and notification duties.
- Evaluate normal and failed operation at the joint human–automation level;
  subsystem speed is not sufficient evidence of a better allocation.
- Track active involvement, autonomous execution time, and end-to-end elapsed time
  separately, including unsuccessful attempts. Check the resulting understanding
  and correction work through
  [software agent oversight](/vault/software-agent-oversight.md), not only output
  completion or fewer manual actions.
- Match review and commitment requirements to consequences, available reaction
  time, and the person's ability to add useful judgment. Distinguish approval,
  time-limited veto, and after-the-fact notification.
- Treat [appropriate reliance](/vault/appropriate-reliance-on-automation.md) as a
  function- and context-specific outcome, not a single product trust score.
- **Extrapolation to software and AI agents:** map retrieval, synthesis,
  recommendation, and external commitment separately. The historical framework
  does not validate an AI-specific autonomy scale or particular approval workflow.

## Evidence and Boundaries

The historical framework is a **qualitative conceptual model and narrative
research synthesis** with no original participant experiment, pooled effect size,
statistical validation,
or numerical rule for choosing levels. Its air-traffic-control allocation is a
worked recommendation, not a deployment result. It provides neither criterion
weights nor complete operational scales for the nondecision functions.

Human approval is not universally safer: rapid reactor shutdown or collision
avoidance can require action faster than a person can respond. Full automation
can also be appropriate when no human rescue is expected, but must then reliably
handle known and unforeseen anomalies. Adaptive allocation is acknowledged, not
evaluated as a policy. Illustrative examples do not always map cleanly to every
word of the ladder; the framework is not a certification scheme.

The coding comparison adds empirical workflow evidence but involves novice agent
users, short selected challenges, bundled capability differences, and
success-conditioned timing. It neither supplies an optimal automation allocation
nor measures long-term maintenance, objective comprehension, or recovery from
consequential failures. Transparent action and stopping support are proposed
remedies, not evaluated interventions.

## Sources

- [A Model for Types and Levels of Human Interaction with Automation](/dossiers/types-and-levels-of-automation.md) — Supplies the four functions, ten-level decision/action ladder, iterative human-performance and consequence criteria, and upper-bound interpretation, with explicit gaps in validation and nondecision scales.
- [Code with Me or for Me? How Increasing AI Automation Transforms Developer Workflows](/dossiers/code-with-me-or-for-me-ai-automation.md) — Adds a 20-person Copilot/OpenHands comparison showing execution and debugging delegation, higher completion, and lower success-conditioned active effort without halved elapsed time or established understanding gains; the capability bundles differ.
