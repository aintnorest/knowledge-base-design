---
type: Synthesis
title: Appropriate Reliance on Automation
description: Reliance should fit automation capability, action consequences, and available alternatives, because higher trust or more persuasive explanations do not necessarily improve joint decisions.
tags: [delegation, trust, decision-making, human-performance, interaction-design, digital-interfaces]
timestamp: 2026-10-14T21:39:10Z
---

# Appropriate Reliance on Automation

The objective is neither maximum delegation nor maximum skepticism. Appropriate
reliance means using automation where it helps and withholding, checking, or
correcting it where its limitations matter. **Trust is an attitude; reliance is
behavior.** Workload, self-confidence, engagement effort, time, and alternatives
can make the two diverge.

## Use, Misuse, Disuse, and Abuse

- **Use** is voluntary engagement or disengagement.
- **Misuse** is overreliance: inadequate monitoring or accepting an inappropriate
  automated decision. It includes omissions when a missing signal prevents action
  and commissions when a wrong directive is followed.
- **Disuse** is neglect or underuse of useful assistance. Configuration and
  verification costs can make nonuse rational rather than resistant.
- **Abuse** is design or management allocation that disregards the resulting
  human role, performance, and authority.

These categories describe system relationships, not a method of blaming an
operator after a bad outcome. Expertise does not guarantee immunity to misleading
cues, and automation redistributes rather than eliminates human error.

## Calibrate Trust Locally

An integrative review distinguishes **calibration** (trust matches capability),
**resolution** (trust distinguishes different capability states), and
**specificity** (trust applies to the relevant function, mode, time, and situation).
An acceptable average judgment can conceal dangerous confidence in a weak mode.

Performance, process, and purpose answer different questions: what the system
achieves, how it works, and what use its designers intended. These are bases for
assessment, not mandatory stages through which trust develops. Polished or
humanlike presentation can alter attitudes without improving actual capability.

Reliance also changes the evidence available for learning. Underuse can hide
successes; heavy delegation can hide occasional failures and weaken monitoring.
The review's closed-loop model is conceptual, not a validated prediction engine.

## Source Labels and Error Experience

Appreciation and aversion are conditional findings, not competing universal
preferences. **Before accuracy feedback**, identical numerical advice attributed
to an algorithm received more weight than advice attributed to other people:
**.45 versus .30** in a **202-person** weight-estimation experiment (**d = .42**).
In a separate choice experiment, **88%** selected the algorithm against another
participant, versus **66%** against themselves. Self-comparison weakened, rather
than reversed, algorithm preference. Forecasting professionals discounted both
advice sources more than lay participants, but this was a nonrandom sample
comparison, not proof that expertise causes appropriate skepticism.

**After observing imperfect performance**, people can reject a model that still
outperforms the human alternative. In a **361-person** forecasting experiment,
model selection was **65% without feedback**, **63% after human-only feedback**,
**26% after model-only feedback**, and **23% after both**. Subsequent model error
averaged **22.07 versus 26.61** for humans; related exposure effects appeared in
both forecasting domains and with self or another person as the alternative.
These are internally repeated findings, not evidence of universal human preference.

Relative uptake is not calibration: an algorithm label can persuade without
changing advice quality, and greater uptake than a human comparator can still
be insufficient for the advice's value. Conversely, visible errors do not
establish that rejection improves the outcome. Specify the comparator, feedback
history, and replacement's performance. Neither study validates a remedy for
software-agent reliance; hiding failures is not a justified response to disuse.

## Capability Is Not the Value of Acting

Reliability must be considered alongside the function being automated and the
consequence of being wrong; see [levels of automation](/vault/levels-of-automation.md).
An erroneous recommendation can be more damaging than erroneous status
information, while exclusive filtering can conceal the evidence needed to check
an interpretation. Mean reliability does not capture every contextual failure.

Alarm sensitivity is likewise not the chance that an alarm signals real danger.
A review's analytical example combines a **.999 hit rate**, **.0594 false-positive
rate**, and **.001 hazard base rate**, yielding only **.0168 probability of a real
hazard given an alarm**. This is a mathematical illustration, not operational
alarm data. Repeated false alarms can change future response behavior.

The mixed-initiative account recommends weighing action, inaction, and asking
against their context-dependent costs. Confidence that assistance is wanted is
not confidence that its output is right, and neither is a universal permission
to act. Its expected-utility thresholds follow assumed utilities; they were not
validated as population preferences or optimal confidence cutoffs.

## Overreliance on AI Recommendations

Explanations can persuade without helping people discriminate correct advice
from errors. Controlled studies make that distinction sharper than trust ratings:

- In a **199-person** nutrition experiment with simulated AI, cognitive forcing
  pooled requested advice, an independent first choice, and delayed advice.
  Agreement with an incorrect ingredient choice fell from **.64 to .48** compared
  with immediate explainable advice (**d = .36**). Correct ingredient identification
  rose from **.08 to .27**, but remained below **.49 without AI** on error trials.
- The complete two-choice decision had **no significant overreliance reduction**
  (**.30 versus .26**). Complete error-trial accuracy improved **.03 → .09**, but
  there was **no significant overall accuracy improvement** over immediate advice.
  No individual forcing design was a demonstrated winner.
- Three crowdworker tasks achieved human–AI accuracy above both partners alone.
  For beer sentiment, recommendation-plus-confidence reached **.89 accuracy**,
  versus **.84 AI alone** and **.82 human alone**. Adding the tested local
  explanations produced **no significant incremental accuracy gain** over that
  baseline, not proof that all explanations have zero effect.
- Explanations tended to increase wrong-advice acceptance in beer sentiment and
  logical reasoning; book sentiment did not share that error-trial penalty.
  Adaptive explanations changed agreement without significantly improving total
  accuracy. Disagreement helps only if the replacement answer is better.

The nutrition study found clearer complete-decision benefits among high
Need-for-Cognition participants, while both groups improved ingredient detection.
A significant subgroup result versus a nonsignificant one does not establish a
significant interaction. Added effort can have uneven benefits, and preference
or trust ratings cannot substitute for correctness.

## Acceptance, Understanding, and Verification

Accepting generated material can mean **temporary incorporation**, not final
endorsement. In **21 observed programming sessions**, people sometimes accepted
suggestions to obtain a better reading surface or finish a logical unit before
checking it. After deferred thought, **53.2%** of suggestions were verified
immediately afterward; including later checking raised attributed mean
verification time **3.25 → 15.21 seconds**. Subsequent editing was more frequent
after deferral than prior verification (**.53 versus .18**). These recalled
activity states measure work, not the correctness of the check. Rapid acceptance
alone cannot identify overreliance, and editing alone cannot establish validation.

Deferred checking can also leave understanding unresolved. A **24-person**
programming comparison found **19/24 preferred** generated-code assistance and
**23/24 found it more helpful**, without detected completion-time or success gains.
The authors observed **eight overreliance instances**, including accepting code
without understanding and postponing validation; these are instances, not eight
distinct participants or a calibrated error-acceptance rate. Recognizing an error
could still lead to lengthy repair of an unsuitable approach.

Across **20 observed programmers**, rapid checks matched expected calls and
control structures, while unfamiliar work prompted examination, execution, and
documentation lookup. Some users took repeated suggestions or first-option
placement as reliability cues. These cues were not validated uncertainty signals;
recognizing a familiar shape or successfully using an unfamiliar interface did
not establish semantic correctness or deeper understanding.

Interviews with **17 experienced software-agent users** extend the distinction
to review shortcuts: a good plan can substitute for checking execution, passing
tests for correctness, skimmed explanations for exhaustive inspection, and model
deference for missing expertise. **Agreement between agents** increased perceived
confidence without evidence that their errors were independent. These are
reported coping strategies under finite attention, not demonstrated error-detection
methods. A plan, test result, or rationale supplies evidence only for the narrower
claim it actually checks. See [software agent oversight](/vault/software-agent-oversight.md)
for the workflow of constraining, steering, monitoring, and reviewing work.

## Working Code Is Not Necessarily Secure Code

Code-assistant security studies supply complementary boundary conditions rather
than a single model-independent harm or safety verdict:

- A **47-person randomized study** of five short security tasks found local harms
  alongside descriptively greater perceived security with assistance. SQL
  injection appeared in **36% assisted versus 7% control** solutions; that
  category comparison had **p = .041**. However, the **adjusted aggregate
  treatment result was p = .056**, not conventionally significant, and none of
  the task treatment regressions passed its printed multiplicity threshold.
  Local mistake comparisons must not be substituted for those adjusted effects.
- A **58-student** connected C-project study over two weeks found lower mean
  participant-level weakness density with inline assistance, including **up to
  22% lower severe weaknesses per line in passing functions**. Non-inferiority
  used a chosen **10% relative margin**: severe-density results were **p = .04
  for compiling functions**, but **p = .06 for passing functions**, despite
  prose calling both significant. Favorable per-line density coexisted with
  locally worse assisted outcomes and higher pooled severe weaknesses per
  passing function (**2.24 versus 2.14**). The denominator changes the claim.

The studies differ in model, interface, language coverage, work duration, and
security measure; neither directly replicates or cancels the other. Both show
that functional success, acceptance, and later edits can leave security defects.
Ordinary tests missed authentication or access-containment requirements in the
short-task study; a basic-test-passing project function retained **three weaknesses,
two severe**. Unsafe human context could also seed later suggestions.

Security confidence therefore needs property-specific evidence, not a general
feeling that the code works. Prompt revision and substantial editing were
associated with secure outcomes in the short-task study, but were not randomized
remedies; engagement or expertise could explain those associations. These studies
do not establish the security effect of contemporary autonomous agents.

## Practical Use

- Measure behavioral use, acceptance of incorrect advice, correction quality,
  and joint outcomes alongside subjective trust. Evaluate correct- and
  incorrect-advice cases separately.
- Separate source-label persuasion and post-error disuse from capability-sensitive
  reliance. Compare observed mistakes with the actual alternative rather than
  demanding perfection or suppressing failures to preserve uptake.
- Distinguish acceptance, final retention, comprehension, checking, and repair.
  Include post-acceptance work; neither elapsed review time nor edit volume proves
  error detection, and neither is automatically wasted effort.
- Check the property at stake. Functional tests, security checks, plan adherence,
  and independent corroboration answer different questions; agreement without
  assessed error independence is not an additional correctness guarantee.
- Show relevant performance history, operating limits, and inspectable intermediate
  results; these are review recommendations, not a proven interface package.
- Preserve independent evidence and inexpensive engagement, rejection, and
  correction. Make oversight feasible rather than adding voluminous feedback.
- Compare a team with both solo partners and compare explanations with a useful
  recommendation-plus-confidence baseline. Assess error overlap, not just similar
  aggregate accuracy.
- Test whether independent initial judgment or requested advice improves the
  actual decision. Do not impose a universal waiting period from one experiment.
- **Extrapolation to software and AI-agent supervision:** assess whether reviewers
  detect actual agent mistakes and whether the workflow improves on its stronger
  baseline; fluent rationales and approval clicks are not evidence of calibration.

## Limitations

The historical automation sources are narrative reviews or conceptual models,
not pooled causal estimates. Their recommended calibration displays and authority
allocations are conditional guidance. High authority may be necessary when a
person cannot respond in time; human review is not universally the safer choice.

The recommendation experiments used short, curated crowdworker tasks, controlled
or selected errors, and particular explanation designs. They do not establish
long-term, professional, high-stakes, or coding-review effects. The explanation
paper has an unresolved logical-reasoning participant-denominator contradiction;
its total recruitment must not be presented as retained analysis size. Cognitive
mechanisms and motivation moderation remain incompletely tested. These findings
concern decision accuracy, not every possible benefit of explanations for learning,
accountability, or debugging.

The appreciation and aversion studies concern short numerical tasks, often
low-stakes and with minimally described statistical models; whole-forecaster
selection differs from reviewing individual generated changes. Source labels,
feedback exposure, and confidence do not isolate every proposed cognitive
mechanism. Their results are not an established effect size for coding agents.

The programming observations and interviews establish practices and burdens,
not their causal contribution to productivity or calibrated error rejection.
The 21-person activity study lacks an unassisted baseline; its verification
allocations are not net productivity losses. Early interfaces, small convenience
samples, recalled activity, and self-reported professional heuristics constrain
transfer. Proposed comprehension and review aids remain untested in these sources.

The security studies are small and student-heavy, with different models and
outcome definitions. The connected-project study has substantial attrition
(**58/105** submitted analyzable code), inconsistent group/function denominators,
and an unvalidated acceptable-security margin. The short-task study's repeated-
task aggregate model does not specify participant clustering and its task
categories use different security bucketing. Neither a nonsignificant harm
estimate nor a conditional non-inferiority result proves absence of risk.

## Sources

- [Humans and Automation: Use, Misuse, Disuse, Abuse](/dossiers/humans-and-automation-use-misuse-disuse-abuse.md) — Defines reliance relationships and supplies reviewed engagement-cost, monitoring, and alarm-base-rate evidence without assigning operator blame.
- [A Model for Types and Levels of Human Interaction with Automation](/dossiers/types-and-levels-of-automation.md) — Adds function-specific reliability, consequence-sensitive authority, inspectable raw data, and time-critical exceptions.
- [Trust in Automation: Designing for Appropriate Reliance](/dossiers/trust-in-automation-appropriate-reliance.md) — Distinguishes attitude from behavior, calibration/resolution/specificity, performance/process/purpose, and history-dependent learning; design implications remain tentative.
- [Principles of Mixed-Initiative User Interfaces](/dossiers/principles-of-mixed-initiative-user-interfaces.md) — Separates confidence from the context-dependent utility of acting, asking, or waiting through a normative model, not a controlled validation.
- [To Trust or to Think: Cognitive Forcing Functions Can Reduce Overreliance on AI in AI-assisted Decision-making](/dossiers/cognitive-forcing-functions-overreliance-on-ai.md) — Supplies the controlled nutrition experiment, reduced incorrect ingredient agreement, complete-decision and aggregate nulls, and unequal-benefit boundaries.
- [Does the Whole Exceed its Parts? The Effect of AI Explanations on Complementary Team Performance](/dossiers/ai-explanations-complementary-team-performance.md) — Tests complementarity against both solo partners, finds no significant explanation advantage beyond confidence, and distinguishes agreement from correctness across tasks.
- [Algorithm Appreciation: People Prefer Algorithmic to Human Judgment](/dossiers/algorithm-appreciation.md) — Supplies identical-advice label effects before feedback, self/peer comparator differences, and qualified professional-sample differences; relative uptake is not calibrated correctness.
- [Algorithm Aversion: People Erroneously Avoid Algorithms After Seeing Them Err](/dossiers/algorithm-aversion.md) — Supplies internally repeated post-performance disuse despite superior model forecasts, bounded to short tasks and without a tested remedy.
- [Expectation vs. Experience: Evaluating the Usability of Code Generation Tools Powered by Large Language Models](/dossiers/expectation-vs-experience-code-generation-tools.md) — The early Copilot comparison separates preference from nonsignificant time/success results and documents deferred checking, comprehension costs, and difficult recovery.
- [Grounded Copilot: How Programmers Interact with Code-Generating Models](/dossiers/grounded-copilot-programmer-interaction.md) — Supplies observed pattern-based checks, explicit cross-checking, repetition/ranking confidence cues, and debugging difficulties without validating their calibration.
- [Human oversight of agentic systems in practice: Examining the oversight work, challenges, and heuristics of developers using software agents](/dossiers/human-oversight-of-agentic-systems-in-practice.md) — Supplies interview-based substitutions of plans, tests, skimming, and agent agreement for direct expertise or inspection, not measured error detection.
- [Do Users Write More Insecure Code with AI Assistants?](/dossiers/insecure-code-with-ai-assistants.md) — Perry et al. supply task-specific security-confidence mismatches, functional-test blind spots, and the nonsignificant adjusted aggregate p = .056; prompting/editing associations are not proven remedies.
- [Lost at C: A User Study on the Security Implications of Large Language Model Code Assistants](/dossiers/lost-at-c-llm-code-assistant-security.md) — Sandoval et al. supply a complementary favorable-density counterweight, qualified non-inferiority, local harms, and defects surviving acceptance or modification.
- [Reading Between the Lines: Modeling User Behavior and Costs in AI-Assisted Programming](/dossiers/reading-between-the-lines-ai-assisted-programming.md) — The 2022 Copilot observations distinguish temporary acceptance, recalled later verification, and editing from correctness or net productivity benefits.
