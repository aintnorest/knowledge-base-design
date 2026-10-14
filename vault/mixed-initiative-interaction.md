---
type: Synthesis
title: Mixed-Initiative Interaction
description: Share initiative through context-sensitive acting, asking, and waiting while preserving user control and independent judgment, without treating confidence or delayed advice as universal performance guarantees.
tags: [delegation, interaction-design, decision-making, attention, digital-interfaces]
timestamp: 2026-10-14T21:39:10Z
---

# Mixed-Initiative Interaction

Mixed initiative combines inferred assistance with direct user action. The system
can offer or begin useful work, while the person can invoke missed assistance,
dismiss unwanted help, terminate ongoing work, and correct or refine approximate
results. Sharing initiative is not simply increasing autonomy: it includes
choosing when not to intervene and when the person should judge independently
before seeing a recommendation.

## Act, Ask, or Wait

A decision-theoretic design account weighs four outcomes: wanted and unwanted
action, and wanted and unwanted inaction. Confidence that help is desired matters,
but so do the benefit of useful work, the cost of a bad guess, the cost of missing
help, and the person's current attention. Goal uncertainty is distinct from
uncertainty that the proposed result is correct.

Asking introduces another option with its own interruption cost. Under one
illustrated utility ordering, rising confidence produces **inaction → ask → act**;
other cost structures need not contain all three regions. There is no universal
confidence threshold. More intrusive unwanted action raises the case for waiting;
cheap rejection can make a tentative offer less costly.

Uncertainty should also change the *shape* of assistance. A broad, editable result
can be preferable to invented precision. Direct invocation repairs missed help;
dismissal or termination repairs unwanted help; refinement repairs an imperfect
result. Context-sensitive timing, recent-interaction memory, granular feedback,
global controls, and cautious adaptation keep these routes useful as behavior
changes over time.

## Match Initiative to the Current Purpose

Observation of **20 programmers**, with same-study corroboration from **five
external livestreams**, distinguishes two fluid purposes for assistance:

- **Acceleration:** the person understands the next step and wants help expressing
  a logical unit. Long unsolicited suggestions can turn expression into unwanted
  review; the appropriate unit is task-dependent, not a fixed line count.
- **Exploration:** the person is discovering the next step and deliberately
  requests alternatives, examines them, and repairs or combines fragments.
  Meaningful differences matter more than the number of options; detached
  alternatives can add contextual reconstruction work.

These are observed interaction patterns, not stable user types or experimentally
validated modes. Pooled exploration time was **248.6 minutes versus 104.7
accelerating**; this does not measure a causal speedup or prove that automatic
mode adaptation improves outcomes.

An autonomous-execution comparison with **20 novice agent users** further shows
why capability does not settle initiative. Correct completion increased
**25% → 60%**, yet only **20%** intended to prefer the agent over less autonomous
assistance and **60%** disagreed with that intention. Participants described
scope mismatch and difficulty locating or understanding changes. Transparent
actions, constrained proactivity, effective steering, and clear stopping
boundaries are motivated design proposals, not tested remedies. Parallel work
was proposed but was not observed in this experiment.

## Advice Before or After Independent Judgment

Immediate advice can serve as an anchor rather than material for scrutiny.
Requested advice, a required initial unaided choice, and delayed advice change
the decision sequence instead of merely adding explanation text. Their value
must be assessed on actual decisions, especially when the AI is wrong; decreased
agreement is not enough if the person's replacement answer is also incorrect.

A controlled nutrition experiment retained **199 participants** and compared
immediate explainable advice with a pooled cognitive-forcing category: on-demand
advice, initial choice followed by revision, or a **30-second** delay. On incorrect
AI ingredient advice, agreement with the wrong source choice fell from
**.64 to .48**, and correct source identification rose from **.08 to .27**.
Complete two-choice accuracy on error trials rose from **.03 to .09**, but
complete-decision overreliance did not significantly decrease. Overall accuracy
did not significantly improve over immediate advice, and no significant
differences distinguished the three forcing designs. These results support a
bounded sequencing opportunity, not a best design or optimal delay.

Experimental explanation comparisons across sentiment and logical-reasoning tasks
found human–AI teams outperforming both solo partners, but no significant added
accuracy benefit from the tested explanations beyond recommendation plus
confidence. Qualitative accounts described using advice as a prior guide or a
post-check. Task difficulty, interface placement, and expertise varied together:
this study did **not experimentally isolate advice timing or an independent-first
workflow**. Its timing proposals are motivated design recommendations, not an
additional controlled replication of cognitive forcing.

## Practical Use

- Define when a service should act, ask, or wait using the consequences of wanted,
  unwanted, and missed assistance, not confidence alone. Coordinate timing with
  [interruption coordination](/vault/interruption-coordination.md).
- Keep invocation, dismissal, termination, and result editing independently
  discoverable; do not make rejecting one suggestion disable all future help.
- Scope uncertain help to something inspectable and refinable. Distinguish a
  local correction or feedback signal from a global behavior setting, and make
  the consequences of each clear.
- Support a known next step without forcing an exploration session; make
  alternatives deliberately invocable and meaningfully comparable when the next
  step is uncertain. Treat mode-sensitive timing and scope as hypotheses to test,
  not a validated automatic adaptation rule.
- Test immediate, requested, and independent-first advice against a useful
  baseline. Measure correct- and incorrect-advice decisions separately, together
  with effort and experience; see
  [appropriate reliance on automation](/vault/appropriate-reliance-on-automation.md).
- For software-agent supervision, bounded proactivity, understandable changes,
  and stopping routes now have direct coding-study motivation; see
  [software agent oversight](/vault/software-agent-oversight.md). Their benefits
  remain untested. Independent-first review and transfer of the historical
  act/ask/wait model remain **extrapolations**, not proven coding-review designs.

## Evidence and Boundaries

The act/ask/wait model and **12 principles** are a design/theory argument
illustrated by a scheduling prototype, not a controlled usability comparison.
Its timing evidence includes a single user's plotted observations without a
reported sample count or fit uncertainty; it establishes no interruption deadline.
Probability calibration and utility elicitation were not validated.

The **18 human–AI guidelines** underwent iterative practitioner inspection and
expert wording review, including **49 practitioners across 20 products**. That
supports inspectability and broad relevance, not causal benefits from compliance,
universal applicability, or a complete safety or ethics checklist.

The cognitive-forcing experiment used short, low-stakes nutrition decisions and
simulated AI errors. Error-trial performance remained below no AI, and forcing
was rated more complex than immediate advice. Benefits differed across measured
need-for-cognition groups, but no direct interaction test established moderation;
there is no validated personalization rule. The explanation studies used curated
crowdworker tasks and contain unresolved retained-sample reporting contradictions.
Their null comparisons are not equivalence tests. None validates a universal wait
or long-term adaptation outcomes.

The programmer-mode evidence is qualitative and descriptive, from short tasks
and a convenience sample, without a mode-adaptive intervention or unaided
productivity baseline. The autonomous-execution comparison combines model,
environment, and interface differences; its students were new to agents and its
tasks were selected challenges. These coding sources motivate oversight support
but do not validate the proposed controls, safe parallel supervision, or an
optimal autonomy policy.

## Sources

- [Guidelines for Human-AI Interaction](/dossiers/guidelines-for-human-ai-interaction.md) — Adds inspectable guidance for context-sensitive initiative, invocation, dismissal, correction, scoped uncertainty, and cautious adaptation, validated through practitioner and expert judgments rather than end-user outcomes.
- [Principles of Mixed-Initiative User Interfaces](/dossiers/principles-of-mixed-initiative-user-interfaces.md) — Supplies the 12-principle account, context-dependent expected-utility choice among acting, asking, and waiting, and editable scoped assistance, illustrated rather than experimentally validated.
- [To Trust or to Think: Cognitive Forcing Functions Can Reduce Overreliance on AI in AI-assisted Decision-making](/dossiers/cognitive-forcing-functions-overreliance-on-ai.md) — Tests requested, independent-first, and delayed advice in a 199-person nutrition experiment; pooled error-trial gains do not establish overall improvement or a winning individual design.
- [Does the Whole Exceed its Parts? The Effect of AI Explanations on Complementary Team Performance](/dossiers/ai-explanations-complementary-team-performance.md) — Motivates independent-judgment and timing proposals through limited incremental explanation gains and qualitative collaboration strategies, without experimentally isolating those proposals.
- [Grounded Copilot: How Programmers Interact with Code-Generating Models](/dossiers/grounded-copilot-programmer-interaction.md) — Supplies observed acceleration/exploration purposes, unsolicited-scope costs, and comparison needs across 20 programmers and five livestreams, without testing mode adaptation.
- [Code with Me or for Me? How Increasing AI Automation Transforms Developer Workflows](/dossiers/code-with-me-or-for-me-ai-automation.md) — Supplies the 20-person Copilot/OpenHands comparison and control-related complaints that motivate transparency, bounded proactivity, and steering, not an evaluated remedy.
