---
type: Study Note
title: Code with Me or for Me? How Increasing AI Automation Transforms Developer Workflows
description: A 20-person comparison finds more correct task completions and lower measured active effort with a coding agent than a copilot, but not clear satisfaction or understanding gains, using short tasks and unequal time definitions.
resource: https://doi.org/10.1145/3772318.3790850
source: /archive/code-with-me-or-for-me-ai-automation.pdf
tags: [delegation, human-performance, cognitive-load, usability-evaluation, interaction-design, digital-interfaces]
timestamp: 2026-10-14T21:31:31Z
---

# Code with Me or for Me? — Study Notes

**Authors**: Valerie Chen, Ameet Talwalkar, Robert Brennan, and Graham Neubig; Carnegie Mellon University and All Hands AI.  
**Published**: CHI 2026, April 13, 2026, pp. 1–19, as confirmed by ACM's Crossref deposit.  
**Status**: Controlled within-participant study published at a peer-reviewed venue; read the complete **30-page arXiv 2507.08149v2**, dated September 13, 2025, including all nine figures, three tables, task and survey appendices, and references; this is an earlier preprint, not the 19-page version of record.

## What It Is

A head-to-head comparison of assistance that largely **codes with the person** and an agent that can **act for the person**. The durable result is not that autonomy always saves elapsed time: it shifts environment setup, file handling, and debugging toward the AI, reducing measured active user effort while raising questions about understanding, controllability, and desired future use.

## Study Design

### Participants and tasks

**20 students**, recruited through university mailing lists, were selected for Python experience and regular GitHub Copilot use; none reported prior coding-agent experience. Professional programming experience was **0–2 years for 25%, 3–5 years for 60%, and 6–10 years for 15%**; **95%** rated their Python skills intermediate or advanced. Findings describe novice agent users, not experienced professional agent supervision.

The asynchronous study ran in **April–May 2025**, approximately **90 minutes** overall, with **40 minutes per condition**, randomized tool order, and **$35** compensation. Tool was within-participant; task type was randomized between participants, with the same task type in both phases. Six problems provided two variants of each type:

- Web research and data analysis, adapted from GAIA to include datasets and visualizations.
- Bug repairs in existing repositories, drawn from SWE-bench.
- Feature additions to a plotting library, created from realistic repository work.

Selected benchmark tasks had previously defeated the agent alone; this is a deliberately challenging task set, not representative sampling of all development work. Submitted code was graded for satisfying task specifications; copilot screen recordings and agent telemetry supplied trajectories, and comparative five-point ratings and open responses supplied experience evidence.

### Systems and measures

GitHub Copilot offered completions and chat with user-selected backbones, including GPT-4o, Claude Sonnet 3.7, Gemini 2.5 Pro, and o3-mini. OpenHands **0.35–0.38** used **Claude Sonnet 3.7**, with autonomous file changes, execution, browsing, and debugging. This compares bundles of interface, model, capability, and environment support—not automation level with every other factor held fixed.

Task correctness used a linear model with condition and coding problem as fixed effects; the stated model does not describe a participant random effect despite paired observations. Experience ratings used Wilcoxon signed-rank tests against the neutral midpoint, with **α = .05**. No standardized cognitive-load instrument, objective understanding test, or independent replication is reported.

**User effort is defined differently by condition**: copilot effort is start-to-end time, whereas agent effort sums intervals around user messages, intended to encompass inspection and request formulation but exclude autonomous execution. Effort comparisons include only correct solutions. Thus they neither compare identical elapsed-time measures nor estimate effort across all attempts, and they cannot isolate review time.

## Results

### Productivity and elapsed time

| Outcome | Copilot | Agent | Reported test / interpretation |
|---|---|---|---|
| Correct task completion | **25%, SE 10%** | **60%, SE 11%** | **p = .02**; a **35-percentage-point** difference, not a 35% relative increase |
| Measured effort for correct solutions | **25.1 min, SE 6.22** | **12.5 min, SE 2.8** | **p = .01**; about half the measured active effort, conditional on success |
| Agent effort plus autonomous action time | — | **27.9 min** | Comparable to copilot elapsed time, not evidence of halved end-to-end time |

Data-analysis tasks were completed correctly only in the agent condition. No significant differences by task type were reported, although bug fixing looked difficult; subgroup plots are exploratory and small. Figure 8 shows similar correctness advantages by tool order; Figure 9 shows a larger effort difference when copilot came first. The authors suggest an agent-first experience might teach a later copilot approach, but do not establish that mechanism.

### Experience is multidimensional

Table 2 reports agreement/disagreement with agent-favoring statements; the text reverses its **C1/C2 identifiers**, so the construct names are more reliable than the labels:

- **Less cognitive load**: **75% agree, 10% disagree**; text associates **p = .0006**, mean **3.95**, median **4** with this construct.
- **Ability to accomplish new tasks**: **70% agree, 5% disagree**; **p = .0013**, mean **4.25**, median **5**.
- **Faster task completion**: **50% agree, 35% disagree**, **p = .09**.
- **More in flow**: **45% agree, 30% disagree**, **p = .39**.
- **More satisfied**: **45% agree, 40% disagree**, **p = .26**.
- **Better understanding of agent than copilot output**: **25% agree, 55% disagree**, mean **2.45**, median **2**, **p = .07**; a directional concern, **not a statistically significant understanding decrement**.

Perceived competence also failed to predict intended adoption. **70%** agreed that the agent was more competent than a human programmer (**10% disagreed; p = .002**), but only **20%** intended to continue using it over copilot (**60% disagreed; p = .04**). Neither competence ratings nor preference demonstrate actual performance against a human-only baseline, which was not included.

### Workflow shift

Trajectory analysis found initial implementation largely AI-generated in **both** conditions, often from pasted task instructions in chat rather than inline completions. With copilot, users still executed commands, installed dependencies, and transferred edits; with the agent, setup and much debugging became autonomous, and people increasingly asked what changed, requested execution, and gave corrective feedback.

Users described difficulty locating or understanding changes and excessive scope, including an account of unexpected creation of **10 files with more than 1,000 lines each**. This is a participant complaint, not a measured typical output size. The study cannot precisely quantify verification effort; the authors' suggestion that agent review may exceed copilot verification burden is a hypothesis.

## Design Recommendations, Not Tested Interventions

The authors recommend **transparent actions**, **balanced proactivity**, and **effective use of human effort**. People need to understand why a change occurred, steer scope, and know when an agent should stop. Supporting parallel work during autonomous execution could exploit freed effort, but participants in this study did not multitask; the recommendation does not demonstrate safe supervision of multiple agents.

## Analyst Takeaways

1. **Separate active effort from elapsed time.** This experiment supports reduced involvement in successful attempts, not universally faster delivery or halved project duration.
2. **Measure understanding independently.** Less cognitive load and more correct output do not establish maintainability, semantic verification, or retained knowledge.
3. **Do not collapse competence, satisfaction, and adoption.** A tool may solve more tasks yet remain less desirable because of control and integration costs.
4. **Autonomy shifts the bottleneck.** Execution capability removes mechanical chores while making oversight and explanation of multi-file actions more important.
5. **Treat transparency and stopping as design hypotheses.** Interview complaints motivate these changes, but no tested remedy or optimal autonomy setting follows.

## Questions and Limitations

- Small student sample, six selected tasks, time pressure, predefined plans, and one agent/copilot comparison limit generalization to production development, low-resource languages, or prolonged maintenance.
- Model choice and system setup differ; agent onboarding was hosted, while users used their own copilot environment. Their effects cannot be separated from autonomy.
- Success-conditioned time measures compare different subsets, with only **five copilot and twelve agent successes** implied by the reported rates and N; this is not a paired time comparison over every participant.
- **Internal inconsistencies**: the text calls **25% → 60%** a “35% increase,” although that is 35 percentage points (**140% relative**); Table 2 labels cognitive load C1/new-task ability C2, whereas the results text swaps C1/C2. Appendix C reverses wording for satisfaction, understanding, and future use relative to result tables without explaining recoding.
- Recruitment says all used copilot at least weekly, yet Figures 8–9 include **“Used to use GitHub Copilot, not currently use anymore”**. The source does not reconcile eligibility with that subgroup.
- Appendix A describes a copilot agent mode despite the headline binary comparison; the study does not report exact mode usage, so these results should not be read as current products' immutable capability boundaries.
- Self-reported understanding is not code comprehension, and the nonsignificant **p = .07** is not proof of equivalence or a confirmed loss. No correction for the multiple questionnaire comparisons is described.
- **Redistribution evidence**: no explicit licence appears in the preprint text; the [arXiv v2 record](https://arxiv.org/abs/2507.08149) links **CC BY 4.0** as “Rights to this article,” permitting public archiving of this copy. ACM's landing page returned HTTP 403; [Crossref metadata](https://api.crossref.org/works/10.1145/3772318.3790850) establishes the later publication identity but does not supply a licence in the retrieved record.

## Vault Ideas Extracted

- [Software Agent Oversight](/vault/software-agent-oversight.md) — Supplies a 20-person experiment separating correct completion and reduced measured active effort from unestablished understanding gains and the emerging work of explaining and correcting agent actions.
- [Levels of Automation](/vault/levels-of-automation.md) — Shows that delegating execution and debugging can reduce human involvement without proportionally reducing elapsed time or securing satisfaction and future preference.
- [Mixed-Initiative Interaction](/vault/mixed-initiative-interaction.md) — Adds task-grounded motivation for transparent action, bounded proactivity, and timely human steering while distinguishing these design proposals from evaluated interventions.
