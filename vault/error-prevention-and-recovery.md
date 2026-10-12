---
type: Synthesis
title: Error Prevention and Recovery
description: Prevent foreseeable mistakes and make unavoidable failures identifiable, correctable, and recoverable without discarding the user's work or task context.
tags: [interaction-design, forms, accessibility, cognitive-accessibility, digital-interfaces]
timestamp: 2026-10-12T00:00:49Z
---

# Error Prevention and Recovery

A forgiving interface does not require perfect users. It reduces foreseeable
mistakes before commitment, explains failures when they occur, and preserves a
route back to useful work. Prevention and recovery are complementary: avoiding a
mistake, escaping an unwanted state, correcting an entry, and reversing a completed
action solve different problems.

## How It Works

1. **Clarify the action before it happens.** Communicate expected input and
   consequences. Supply enough instruction to prevent misunderstanding without
   burying the task in unnecessary explanation.
2. **Match the safeguard to the consequence.** Enforced constraints change what
   can actually be done; logical guidance and learned conventions only help
   someone infer what to do. A visual warning is not physical prevention.
3. **Identify and explain the failure.** Make the affected item and problem
   identifiable, and offer a known, actionable correction rather than merely
   announcing that something went wrong.
4. **Permit correction or reversal.** Provide an understandable exit, cancellation,
   undo, or review route where appropriate. Make the scope of reversal predictable.
5. **Preserve accumulated effort.** Keep valid entries, later work, and task
   context through errors and interruptions. If recovery takes time, communicate
   the delay instead of requiring the person to reconstruct the task.

These costs are not distributed equally. Memory difficulties, reading and
processing demands, repeated motor effort, and assistive-technology operation can
make error detection and recovery especially burdensome for disabled people.

## Evidence and Requirements

A retrospective heuristic analysis rated **101 principles against 249 known
problems from 11 projects**, with **one explanation rater**. Error prevention
explained **3.7%** of variance in the rating matrix; user control and freedom,
including undo and escape, explained **4.6%**. Error recognition, diagnosis, and
recovery were added to the candidate set through coverage analysis rather than
as a leading factor. This supports separating the failure families, not a
quantified treatment benefit or detection guarantee.

WCAG 2.2's informative explanations connect that separation to accessibility:

- **3.3.1, Level A:** automatically detected input errors and affected items must
  be identified in text; a silent return or silent correction is insufficient.
- **3.3.3, Level AA:** provide known correction suggestions unless doing so would
  jeopardize security or purpose.
- **3.3.4, Level AA:** specified legal, financial, user-data, and test submissions
  need reversibility, checking with correction, or review/confirmation.
  **3.3.6, Level AAA** extends safeguards to all information submissions.
- **2.2.5, Level AAA:** preserve work across re-authentication. Timeout provisions
  also address warning and retained data rather than treating speed as a neutral
  prerequisite.

These are explanations of consensus requirements, not a participant experiment
establishing an optimal error rate or recovery time. The normative requirements
reside in WCAG itself, not its informative commentary.

Practitioner guidance argues that safe exploration and preserved work support
fluency. Its cited hazardous-interface and reversible-commitment studies provide
no inspectable samples, protocols, or effect sizes. A historical response-time
model likewise recommends preserving inquiries and creative models after failure
and immediately communicating expected recovery delay, but reports **no original
controlled experiment**. Neither source establishes a universal numerical payoff
for undo or retained state.

## Practical Use

- Review both the chance of a mistake and the burden of recovering from it,
  including journeys using assistive technology or slower input.
- Use review, correction, or reversibility for consequential commitments; do not
  interpret error prevention as a requirement to confirm every ordinary action.
- Keep correct information when one entry fails, and avoid making recovery from
  an earlier step destroy later work.
- State what failed and what can be done next without automatically blaming the
  user for a possible system failure.
- Pair preserved context with truthful
  [system-status feedback](/vault/visibility-of-system-status.md). A progress
  indication does not compensate for lost work.

## Limitations

Not every action is reversible, and security or the transaction's purpose can
limit correction guidance. A convention is weaker than an enforced constraint,
while excessive instructions or confirmations can impose their own burden.
Accessibility conformance does not establish usability for every disabled person;
complete-process evaluation remains necessary. The heuristic evidence explains
already-known problems, and the practitioner and historical arguments do not
supply controlled effect estimates. Recovery speed and safeguards therefore need
judgment about the actual task and consequences, not universal cutoffs.

## Sources

- [Affordance, Conventions, and Design](/dossiers/affordance-conventions-and-design.md) — Distinguishes enforced physical prevention from ignorable logical and cultural guidance.
- [Enhancing the Explanatory Power of Usability Heuristics](/dossiers/enhancing-explanatory-power-usability-heuristics.md) — Separates prevention, escape/control, and constructive error diagnosis and recovery within a known-problem corpus.
- [First Principles of Interaction Design (Revised & Expanded)](/dossiers/first-principles-of-interaction-design.md) — Argues for reversibility, intelligible error messages, and preserving accumulated work, while exposing the limits of uncited supporting studies.
- [Response Time in Man-Computer Conversational Transactions](/dossiers/response-time-man-computer-conversational-transactions.md) — Recommends retaining inquiry and creative context after failures and communicating recovery delay as task-specific guidance.
- [Understanding WCAG 2.2](/dossiers/understanding-wcag-2-2.md) — Explains identification, correction, consequential-submission safeguards, and work preservation in terms of unequal accessibility costs.
