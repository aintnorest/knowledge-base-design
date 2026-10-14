---
type: Study Note
title: "Human oversight of agentic systems in practice: Examining the oversight work, challenges, and heuristics of developers using software agents"
description: Interviews with 17 experienced software-agent users identify preventative control, co-planning, monitoring, and post hoc review, but document oversight heuristics rather than establish their error-detection effectiveness.
resource: https://doi.org/10.1145/3805689.3812402
source: /archive/human-oversight-of-agentic-systems-in-practice.pdf
tags: [delegation, user-research, trust, cognitive-load, interaction-design, digital-interfaces]
timestamp: 2026-10-14T21:31:31Z
---

# Human Oversight of Agentic Systems in Practice — Study Notes

**Authors**: Shipi Dhanorkar, Samir Passi, and Mihaela Vorvoreanu; Microsoft; the first two contributed equally.  
**Published**: FAccT 2026, June 25, 2026, pp. 6438–6465; version-of-record DOI confirmed by ACM's Crossref deposit.  
**Status**: Peer-reviewed qualitative research; read the complete 28-page arXiv **2606.05391v1**, dated June 3, 2026, including participant table, usage-scenario figure, interview guide, oversight table, and references; not the publisher's version of record.

## What It Is

An exploratory account of the work experienced developers do to keep autonomous software agents aligned with their goals. Oversight is not a single approval at the end: it includes **preventing, steering, monitoring, and evaluating**. The paper also describes practical shortcuts people use when exhaustive review is infeasible. It does not show those shortcuts catch errors reliably.

## Problem and Motivation

Normative demands for meaningful human control often assume someone can continuously understand and correct an agent. Coding agents instead act across files and tools, produce more material than a person can comfortably inspect, and can diverge from their own explanations. This study asks what oversight actually looks like in situated professional work rather than measuring performance on an artificial verification task.

## Research Design and Evidence

- **17 professional users**, recruited through contacts and snowball sampling; one additional person was excluded by a secondary conceptual/usage screener. Eligibility required at least weekly professional agent use and some experience; **16 used agents several times weekly, 12 daily**.
- **13 had at least seven years of programming experience**, two had four to six years, and two one to three years. Agent expertise was self-rated: nine experienced, four somewhat experienced, four very experienced. Appendix A lists **15 men and two women**, with 15 US participants, one in India, and one in Brazil.
- **12 worked at the authors' large technology company**, on distinct teams without shared projects; five worked elsewhere. NDA and competitive concerns constrained cross-company recruitment. The authors intentionally sampled heavy users in well-resourced organizations, not a representative developer population.
- One-to-one, video-recorded semi-structured interviews averaged **60 minutes**, conducted **July–August 2025**, with **US $40** compensation. Participants described their own agent tasks and practices; no standardized coding task, planted errors, or behavioral observation of their actual reviews was administered.
- Inductive analysis used open coding by the first author, **13 axial codes**, and selective coding by the first and second authors, with discussion to resolve disagreements. The before/during/after interview lens helped shape the four-form organization; the authors explicitly call it an organizing device, not an exact or exhaustive taxonomy.
- Findings are interview accounts and interpretive themes, not error rates, causal effect sizes, or tests of oversight effectiveness. No independent replication is established.

## Four Forms of Oversight

| Form | Purpose | Reported work and boundary |
|---|---|---|
| A priori control | Prevent predictable failure before delegation | Establish boundaries, autonomy limits, project context, and constraints; some users invest heavily, others leave defaults unchanged, and black-box deployments limit perceived control |
| Co-planning | Align goals before execution | Negotiate plans, decompose work into independently testable chunks, and supply partial solutions; unclear specificity and implicit requirements make articulation difficult |
| Real-time monitoring | Detect and redirect divergence during execution | Glance at actions or explanations, pause or stop work; participants report little vigilant monitoring and often infer trouble from long runtimes or excessive turns |
| Post hoc review | Check output and how it was achieved | Inspect changes, test functionality, revise or re-prompt; code volume, unfamiliar authorship, and broad regeneration make review costly |

**Preventative control is different from co-planning**: the former configures standing boundaries, while the latter actively develops common ground for a task. Treating both as a permission setting loses the negotiation work.

Production tasks were usually deliberately small and bounded, often described as taking **a few dozen seconds to a minute**. Longer examples involved prototypes (**20–25 minutes**, P10) or a power user's extended work (**15–20 minutes**, P16). The Appendix B figure places agent use across requirements, architecture, implementation/debugging, testing, deployment, and maintenance; these are illustrative accounts, not quantified usage prevalence.

Monitoring was rarely intensive. The authors hypothesize that small tasks made brief glances and final review sufficient for participants' workflows; they did not experimentally establish this explanation. Agent reasoning may misrepresent actual behavior, and attempted redirection sometimes led users to stop and restart rather than recover in place.

## Review Challenges and Heuristics

### Cognitive distance and repeated review

Developers described understanding generated code only superficially because they had not authored it. Even a small later modification could demand considerable reconstruction. In established systems, interdependencies motivated more stringent review than in disposable prototypes. When a repair regenerated multiple areas, participants felt obliged to review everything again. The finding concerns **loss of understanding and increased perceived review cost**, not a measured cognitive-load or bug-detection effect.

### Four practical substitutions

1. **Plan quality substitutes for inspecting actual execution.** Participants treat a carefully negotiated plan as a faithful account of what was done; this assumes plan adherence rather than verifies it.
2. **Passing tests substitute for code correctness.** Test results are easier to inspect than all generated code. Participants acknowledge that this works only insofar as the tests and specification capture the real requirements; a participant's hypothetical perfect test suite is not evidence that such completeness is achievable.
3. **Eyeballing substitutes for exhaustive information processing.** People spot-check signatures, outputs, summaries, rationales, or diagrams to keep review manageable. Self-generated explanations remain possible sources of mistaken reassurance.
4. **Deference substitutes for expertise in unfamiliar domains.** Users sometimes trust a model because they cannot independently judge its library or language choices. Agreement between agents increases perceived confidence, but the study does not establish independent errors or reliable corroboration.

The authors frame these as **imperfect coping mechanisms under bounded rationality**, not simply laziness and not recommended guarantees. Their design proposals—clearer constraints, planning support, contextual monitoring signals, and review aids linking intent to changes—are motivated by interviews and remain untested interventions.

## Analyst Takeaways

1. **Count oversight work before execution.** Configuring boundaries and negotiating scope can serve oversight intentions, even when they resemble ordinary engineering practice.
2. **Make the unit of delegation reviewable.** Participants use decomposition to reduce integration ambiguity and downstream review burden; the study does not identify an optimal task size.
3. **Distinguish reassuring artifacts from independent evidence.** A good plan, fluent rationale, passing tests, or agreement between agents each answers a narrower question than complete correctness.
4. **Preserve understanding, not only approval.** A human remaining responsible does not imply they retain enough context to diagnose or maintain what an agent produced.
5. **Design for finite attention without blessing shortcuts.** Efficient review needs meaningful evidence and intervention routes, not an expectation that people read every trace continuously.

## Questions and Limitations

- Self-reported practices were not observed or tested for actual error detection; interview descriptions of reviewing “every line” do not establish semantic verification.
- Experienced, predominantly male users in well-resourced firms—especially one organization—limit transfer to novices, constrained settings, and other professions.
- Short bounded production tasks limit what rare monitoring means for long-running, parallel, or high-consequence agent work.
- The four forms are analytically influenced by temporal interview prompts; no mutually exclusive or exhaustive classification is claimed.
- No numerical inconsistency was found in the participant counts: Appendix A reconciles the reported programming experience and usage totals. Quoted probabilities and runtimes are participant estimates, not study measurements.
- **Redistribution evidence**: no licence notice is printed in the supplied preprint. The [arXiv record](https://arxiv.org/abs/2606.05391) explicitly links **CC BY 4.0** as “Rights to this article”; ACM's [Crossref metadata](https://api.crossref.org/works/10.1145/3805689.3812402) also deposits CC BY 4.0 for the version of record. The arXiv grant supports public archiving of this copy; the ACM landing page itself returned HTTP 403.

## Vault Ideas Extracted

- [Software Agent Oversight](/vault/software-agent-oversight.md) — Adds a 17-user interview account of preventative control, co-planning, sparse monitoring, and heuristic-driven final review without mistaking reported practice for proven effectiveness.
- [Change Review Effectiveness](/vault/change-review-effectiveness.md) — Shows how task decomposition, unfamiliar authorship, large change volume, and regeneration shape perceived review effort and the temptation to substitute plans or tests for inspection.
- [Appropriate Reliance on Automation](/vault/appropriate-reliance-on-automation.md) — Documents epistemic deference and proxy-based confidence in plans, tests, skimmed explanations, and agreement between agents, without measuring calibrated error rejection.
