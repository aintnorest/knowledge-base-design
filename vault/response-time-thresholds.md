---
type: Synthesis
title: Response-Time Thresholds
description: Acceptable delay depends on the response function and the user's unfinished task, while familiar numerical thresholds are guidance rather than universal experimentally established limits.
tags: [human-performance, interaction-design, cognitive-load, attention, digital-interfaces]
timestamp: 2026-10-12T00:00:32Z
---

# Response-Time Thresholds

A response-time threshold is meaningful only after specifying **response to what**: acknowledgment of input, confirmation of understanding, the first useful result, and full completion are different events. Their timing requirements need not be the same.

## Continuity and Psychological Closure

An unfinished subtask requires people to keep a goal and relevant content active. A delay within that activity can interrupt the train of thought. A delay after a meaningful completion—a **psychological closure**—is less disruptive in Miller's model because the person has reached a stable boundary rather than being suspended mid-thought.

Miller proposed placing delays **over two seconds** after perceived or deliberately structured closure. This is a psychological rationale and design proposal, not a measured universal boundary. A brief acknowledgment does not itself prove that the user's subtask has closed: the person may still be awaiting information needed to continue.

Responsiveness therefore includes predictability and the location of a wait, not just average duration. Once attention shifts and task context is lost, additional delay may have a different psychological cost, even though its operational cost continues to grow.

## Numerical Guidance and Its Evidence

Three often-repeated levels come from a later synthesis:

| Approximate delay | Proposed experiential meaning |
|---|---|
| **0.1 second** | Response appears instantaneous. |
| **1 second** | Flow of thought is maintained. |
| **10 seconds** | Attention remains on the dialogue; longer waits need feedback. |

These are useful orientation, not a faithful reproduction of Miller's **17 task-specific categories** or proof of universal limits. His proposals include **0.1-second** mechanical feedback, **1-second** continuity when requesting the next page, prominent **2-second** conversational targets, and release from mental and physical captivity around **15 seconds and longer**. Other task boundaries permit different waits after closure.

Miller explicitly calls his estimates calculated guesses, “indicative rather than conclusive.” The paper reports **no original controlled latency experiment, participant sample, randomized conditions, or inferential effect sizes** establishing those thresholds. Later repetition is not experimental replication.

Practitioner guidance separately prescribes escalating wait feedback: a busy indication at **0.5–2 seconds**, a possible duration beyond **2 seconds**, animated progress beyond **5 seconds**, continued information and occupation beyond **10 seconds**, and strong completion cues beyond **15 seconds**. Its prose recommends acknowledging input within **50 milliseconds**. These exact boundaries also lack a supporting latency experiment in the source.

## Practical Use

- Define timing goals separately for acknowledgment, first useful information, and completion.
- Locate unfinished subtasks and meaningful boundaries before deciding where a wait can occur.
- For longer work, preserve a stable place to resume and allow other useful activity rather than keeping the person captive.
- Communicate actual receipt, ongoing work, and completion through [visibility of system status](/vault/visibility-of-system-status.md); do not imply completion merely because an acknowledgment appeared.
- Preserve task context through failures, connecting responsiveness with [error prevention and recovery](/vault/error-prevention-and-recovery.md).
- Treat numerical targets as task-specific hypotheses. Better feedback and faster execution are complementary; feedback does not remove unnecessary delay.

## Limitations

Expectations, skill, modality, variability, urgency, and the task's external operating requirements affect acceptable delay. A nominal average cannot describe all of those conditions. The historical account emphasizes strongly engaged, often skilled workers and does not resolve accessibility needs or adaptation to other contexts.

Neither the closure model nor the threshold collections establish a universal step change in performance at a particular second. No direct replication verdict for the entire 17-category taxonomy is established in the dossier, and the later three-number shorthand does not validate it retrospectively.

## Sources

- [Response Time in Man-Computer Conversational Transactions](/dossiers/response-time-man-computer-conversational-transactions.md) — Miller's closure-based rationale, task-specific calculated guesses, and the distinction from Nielsen's later 0.1/1/10-second synthesis.
- [First Principles of Interaction Design (Revised & Expanded)](/dossiers/first-principles-of-interaction-design.md) — Practitioner-prescribed escalating wait feedback, prompt acknowledgment, honest progress, and reduction of blocked time, without experiments validating the exact cutoffs.
