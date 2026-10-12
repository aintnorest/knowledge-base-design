---
type: Study Note
title: Response Time in Man-Computer Conversational Transactions
description: Miller proposes task-specific latency limits based on expectation, short-term memory, and psychological closure, but explicitly presents the thresholds as calculated guesses requiring real-task validation rather than experimental findings.
resource: https://doi.org/10.1145/1476589.1476628
source: https://doi.org/10.1145/1476589.1476628
tags: [human-performance, interaction-design, cognitive-load, attention, digital-interfaces, taxonomy]
timestamp: 2026-10-11T23:54:33Z
---

# Response Time in Conversational Transactions — Study Notes

**Authors**: Robert B. Miller; International Business Machines Corporation.  
**Published**: December 9, 1968; AFIPS Fall Joint Computer Conference, part I, volume 33, pp. 267–277; DOI 10.1145/1476589.1476628.  
**Status**: Historical conference paper offering a psychological rationale and 17 response categories, not a controlled interface-latency experiment. Read the complete supplied ACM DL PDF: 11 printed article pages and a blank twelfth page. The publisher's personal/classroom-use notice does not permit public repository redistribution; the dossier therefore cites the DOI rather than a public archive copy.  

## What It Is

A foundational argument that “system response time” is underspecified until one asks **response to what?** A key's acknowledgment, a query's first useful answer, completion of a computation, and restoration after a failure are different transactions. They do not share one acceptable delay.

Miller's lasting model is **continuity of thought versus psychological closure**. Delays during an unfinished subtask impose a different cost from delays after a meaningful completion. This is more useful than memorizing one latency ceiling, and substantially richer than the later **0.1/1/10-second** mnemonic commonly associated with the paper.

“Conversational” here means interactive work with a computer terminal, not primarily natural-language chat. Its examples range from badges and keyboards to information retrieval, light-pen drawing, and engineering design.

## Problem and Motivation

A two-second response requirement was already disputed in 1968. Miller distinguishes **operating needs**—throughput, staffing, and the external process's demands—from **psychological needs**—expectancies and the continuity of goal-directed thought. This paper concentrates on the latter and intentionally does not resolve value-versus-cost tradeoffs.

Fast batch processing is not necessarily interactive thinking: replacing a two-day wait with fifteen minutes can improve operations without keeping an active train of thought intact. Conversely, a task may still be completed with long delays while promising alternatives are never explored. That lost exploration is an asserted, testable hypothesis here, not a measured experimental effect.

## Principles as Ideas

### Closure determines where a wait can be tolerated

People organize work into “clumps” ending in perceived completion. Looking up a number, dialing it, and reaching the intended person create nested closures. Interruptions before completion can disrupt the goal and the content being held in short-term memory; interruptions after completion are less damaging. Miller's broad guidance is that delays **over two seconds** should follow a perceived or deliberately structured closure.

He describes latency costs as possible **step-down discontinuities**, not a linear convenience penalty. Once attention shifts and the current thought structure is lost, a ten-second answer might be no better psychologically than a much later one for that particular task. This does **not** mean those waits have equal operational cost, or that every task has a universal discontinuity at ten seconds.

### Acknowledgment and completion are different responses

A single signal can simultaneously mean “heard,” “accepted,” “interpreted,” and “working.” If these functions are combined, Miller says the fastest component's response requirement governs the combined signal. A prompt acknowledgment is useful but does not establish that the requested work is complete. The paper explicitly allows long execution times after a command's meaning has been confirmed.

### Predictability is part of responsiveness

Miller prefers fixed, standardized delays in reflex-like identification work and no perceptible delay variation while drawing. Most category estimates lack tolerance bounds, and he acknowledges this omission. The design target is not merely a nominal average: variability, expectations, and the person's current task determine whether a delay is disruptive.

## Results / Admissions

### The 17 categories and their proposed limits

These are **Miller's proposals**, not experimentally established maxima. Several categories contain separate phases or qualified exceptions; some deliberately have no numerical bound. Times refer to the response named in the row, not necessarily complete end-to-end work.

| No. | Response category | Proposed threshold and its rationale or exception |
|---|---|---|
| 1 | Control activation | Mechanical-action feedback **≤0.1 s**; typed-character echo **0.1–0.2 s**; light-pen character-selection confirmation **≤0.2 s**. Skilled typists may need faster feedback to avoid visible hand–eye desynchronization. |
| 2 | “System, are you listening?” | Session-initialization availability signal **up to 3 s**, preferably beginning **within 1 s**. During active conversation, input must receive perceived-immediate attention; even **0.5 s** waiting to enter information is described as disruptive. |
| 3 | “System, can you do work for me?” | Acknowledge routine service requests **within 2 s**, impromptu complex ones **within 5 s**. Loading programs/data or restoring yesterday's workspace: **15 s** preferred, **up to 1 min** tolerable while the user prepares. |
| 4 | “System, do you understand me?” | For a detectable entry error, allow the thought segment to finish, then notify **after 2 s and before 4 s** following completion. The intentional pause permits closure; this is not an argument for withholding all input feedback. |
| 5 | Identification | Card-position feedback **less than 0.4–0.5 s**, sometimes unnecessary if positioning failures are rare; “I've read you” confirmation **within 2 s**, with a fixed duration. At an inquiry terminal rather than a clock-in bottleneck, acknowledgment **up to 5–7 s** may be acceptable. |
| 6 | “Here I am, what work should I do next?” | Next production assignment **10–15 s** after completing the previous one. A student continuing computer-assisted instruction should wait **less than 5 s**. |
| 7 | Simple inquiry of listed information | Direct retrieval of an existing record **within 2 s** when used frequently, e.g. more than once an hour; the answer resolves a held issue or supports repeated searching. |
| 8 | Simple inquiry of status | Normally a **2-s** limit; relax to **7–10 s** when the user understands that assembling the status requires searching/processing and is holding one relatively simple idea. |
| 9 | Complex inquiry in tabular form | A complete answer to the example inquiry **within 4 s**. Multiple product answers can arrive sequentially at **4 s per item**, allowing assimilation; **2-s** intervals are preferred and four seconds may be unnecessarily long. |
| 10 | Request for next page | At least the first several new lines **within 1 s** when continuing reading. Search/scanning requires faster response—**0.5 s** is already subjectively long. Custom-built index pages can take **2 s** if anticipated; delays over two seconds make scanning increasingly unlikely. |
| 11 | “Now run my problem” | A scientist/engineer may remain in a problem-solving frame if a computed result returns **within 15 s**; patience varies with prior effort, expected additional runs, and urgency. Longer delays can reduce experimentation. |
| 12 | Keyboard versus light-pen category entry | Illustrative expectation difference: **2 s** after light-pen selection versus **3 s** after keyboard entry; shifting attention from keyboard to display may take **1–1.5 s**. This difference disappears for page turning: **1 s maximum**, faster during search. |
| 13 | Graphic response from light pen | Slowly and deliberately drawing a line: **up to 0.1 s**, with no perceptible variability. Moving a completed symbol or constructing a display from symbols: **up to 1 s** proposed acceptable. Fast sketching is not established by the slower-drawing estimate. |
| 14 | Complex inquiry in graphic form | Begin the graphic **within 2 s** and complete it **within 10 s** to sustain thinking during search/problem solving. First response and full completion are explicitly separate. |
| 15 | Graphic manipulation of dynamic models | **No response-time estimate offered**: experience is insufficient. Miller speculates about fitting a comprehensible scenario into **50 min**, immediately notes even that could be ten times too long, and calls for developmental studies. This is not a 50-minute interface-latency allowance. |
| 16 | Graphic manipulation in structural design | Rule-violation feedback around **2 s**; waiting more than a couple of seconds during a unitary creative action is described as inhibiting. After an idea-level chunk closes, the designer may wait **1–2 min**. Relevant graphic motion might preserve coupling for **up to 10 s**; no universal fixed limit is claimed. |
| 17 | “Execute this command into the operational system” | Confirm understanding and interpretation **within 4 s**; execution and final confirmation may take **variable minutes**, including dependencies outside the automatic system, after the user's command-level activity has closed. |

The two postscripts reinforce the model rather than adding two more categories. Around **15 s and longer**, Miller recommends releasing people from physical and mental captivity so they can do other work and retrieve the result later; he says this rules out conversational interaction. For failures, preserve the last inquiry, complex-query context, or creative model so users need not reconstruct it. Restore work **within 15 s**, or failing that **within less than 5 min**, and immediately communicate the expected delay. These are again proposals.

### What evidence supports the numbers?

Miller states the epistemic status unusually plainly:

> The estimates of delay times offered in the following pages are the best calculated guesses by the author, a behavioral scientist, who has specialized in task behavior, including thinking and problem solving.

He asks readers to accept the parameters as **“indicative rather than conclusive”** and calls for extended studies in real task environments with skilled users having **many dozens of hours** of relevant practice. The paper reports **no original controlled latency experiment, participant sample, randomized conditions, or inferential effect sizes for the 17 thresholds**.

The basis is psychological argument, cited earlier work, analogies, and limited informal observation. A secondary account of temporal-interval discrimination supplies indirect laboratory evidence: for **2–4-s** click intervals, a roughly **±8%** difference permitted **75%** correct judgments; longer **6–30-s** intervals had wider equivalent tolerance ranges. Miller warns that full-attention timing tasks do not directly establish tolerances during actual work and says the latter need empirical data. He also cites conditioning and short-term-memory reasoning cautiously.

The time-clock example is an informal observation of about **3 s per employee**, including about **1 s** mechanical response. Reducing that response to **0.5 s** yields a calculated **16%** cycle-time reduction if everything else stays constant; this is arithmetic over an observation, not an intervention study. Similarly, the opening airline example explicitly says to **assume** the numbers: its 20% reservation-loss claim is not a measured result of this paper.

### How the 0.1/1/10-second shorthand emerged

[Jakob Nielsen's 1993 “Response Times: The 3 Important Limits”](https://www.nngroup.com/articles/response-times-3-important-limits/) identifies itself as an excerpt from *Usability Engineering*, chapter 5. It explicitly cites **Miller (1968)** and **Card, Robertson, and Mackinlay (1991), “The Information Visualizer: An Information Workspace.”** Nielsen presents **0.1 s** as apparently instantaneous response, **1 s** as maintaining flow of thought, and **10 s** as keeping attention on the dialogue, with feedback for longer waits.

This confirms a later synthesis and a named popularizing source, not that Miller himself formulated exactly that universal triplet or that the Card paper independently validated all three values. Miller uses 0.1 seconds for specific motor feedback, one second for page continuity, **two seconds** prominently for conversational continuity, and **15 seconds** for terminal captivity, alongside many task-specific exceptions. The familiar shorthand compresses the source; it does not reproduce its taxonomy.

### Copyright and redistribution

No copyright notice is visible in the supplied article scan. The [ACM publisher page](https://dl.acm.org/doi/10.1145/1476589.1476628), inspected in its Information & Contributors section, gives this notice verbatim:

> Copyright © 1968 ACM.
>
> Permission to make digital or hard copies of all or part of this work for personal or classroom use is granted without fee provided that copies are not made or distributed for profit or commercial advantage and that copies bear this notice and the full citation on the first page. Copyrights for components of this work owned by others than ACM must be honored. Abstracting with credit is permitted. To copy otherwise, or republish, to post on servers or to redistribute to lists, requires prior specific permission and/or a fee. Request permissions from Permissions@acm.org

The page also labels the work **Free Access**. That access label does not override the explicit server-posting and redistribution restrictions.

## Analyst Takeaways

1. **Set latency goals per cognitive transaction.** Miller recommends distinguishing kinds of response and locating closure. An analyst application is to identify acknowledgment, first meaningful result, and full completion separately rather than treating one average request duration as “responsiveness.”
2. **A wait after closure and a wait inside manipulation are different design problems.** Immediate feedback protects perceived coupling; long work should leave the user with a stable place to resume. These principles survive the paper's historical terminals and light pens.
3. **Use thresholds as hypotheses, not laws of human nature.** The exact 17 numbers are calculated guesses; Nielsen's three-number rule is useful orientation, not substitute evidence for a particular task, skill level, delay distribution, or modality.
4. **Preserve thought, not merely system availability.** Miller explicitly recommends preserving inquiry and model state after failure. A progress indication cannot compensate for losing the work that made the request meaningful.

## Questions and Limitations

- No direct replication or failed replication of this entire 17-category taxonomy is established here. Later repetition of its thresholds, including Nielsen's synthesis, is not experimental replication.
- The paper assumes strongly engaged, often skilled workers. Its expert-practice requirement limits what novice timing studies could tell about those users, but does not justify excluding novice experience from product evaluation.
- Many proposed maxima are context-dependent, and the text moves among **1-, 2-, 4-, 10-, and 15-s** boundaries. Read these as a hierarchy of response functions and closures, not a single internally consistent universal timing specification.
- The delayed error notification and tolerance for one-second symbol-following are historical judgments, not demonstrations that modern direct manipulation benefits from those delays.
- Miller distinguishes psychological effectiveness from operating efficiency but does not calculate their cost tradeoffs. Network constraints, accessibility needs, modality differences, and long-term adaptation require additional evidence.

## Vault Ideas Extracted

- [Response-Time Thresholds](/vault/response-time-thresholds.md) — Task-specific origins and uncertain empirical status of latency limits, contrasted with Nielsen's later 0.1/1/10-second synthesis; delays hurt less at meaningful subtask boundaries (psychological closure) than while users hold an unfinished goal.
- [Visibility of System Status](/vault/visibility-of-system-status.md) — Acknowledgment, acceptance, ongoing work, and completion are distinct messages with distinct response needs.
- [Error Prevention and Recovery](/vault/error-prevention-and-recovery.md) — Preserve task context and creative work after failures, and communicate recovery delay rather than forcing reconstruction.
