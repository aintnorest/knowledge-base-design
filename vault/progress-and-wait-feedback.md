---
type: Synthesis
title: Progress and Wait Feedback
description: Meaningful progress can improve wait preference and visual motion can shorten judged duration, but truthful state, uncertainty, and user control matter more than making unfinished work merely appear fast.
tags: [interaction-design, visual-perception, motion, trust, digital-interfaces]
timestamp: 2026-10-16T00:00:00Z
---

# Progress and Wait Feedback

Wait feedback has two different jobs: **explain what is happening** and **make an unavoidable wait more tolerable**. A person can prefer an informative wait without judging it shorter; a wait can appear shorter without conveying more useful information or finishing sooner. Neither outcome proves better task performance.

## Communicate What Is Known

- **Acknowledgment** means the request was received, not that it succeeded.
- **Determinate progress** relates completed work to a meaningful whole. It supports estimating what remains only insofar as the denominator and work-rate assumptions are credible.
- **Indeterminate activity** says work continues when its remaining extent cannot be estimated. Repeating motion is not a percentage, an estimated finish time, or proof that useful work has advanced.
- **Completion** means the requested outcome has actually been reached, not simply that an animation finished.

A fraction of records processed can misrepresent remaining time when later stages are more costly or more work is discovered. Separate stage progress from total progress where that distinction matters; communicate uncertainty rather than inventing precision. These are practical inferences from the estimation problem, not measured benefits of a particular display.

This is a specific application of [visibility of system status](/vault/visibility-of-system-status.md), not a replacement for clear task-level meaning.

## Preference and Perceived Duration: Different Evidence

A **48-person** query experiment compared progress feedback with no progress under constant **10-second** and variable **1–17-second** delays. Progress improved subjective semantic-differential ratings (**p = .0006**); the paper reports **86.1%** liked it, but leaves that percentage's denominator unexplained. There was **no significant preference for constant response time** and **no significant variability-by-progress interaction**. Proposed anxiety and multitasking benefits were not separately demonstrated. This is not a determinate-versus-indeterminate comparison.

A separate series tested sequential, fully watched bars. In a **16-person** duration-matching study, plain bars lasting **5 and 15 seconds** felt equal to backward-decelerating textured bars lasting **5.61 and 16.75 seconds**, respectively (**SE 0.14 / 0.45 seconds; p < .001** as reported). The augmented bars could therefore last **12.2% / 11.7% longer** while feeling equal; the authors summarize the perceptual benefit as about **11%**. This is not an 11% reduction in computation time.

The supporting comparisons were not uniformly positive: a separate **10-person** study found both pulsating and textured bars judged faster than plain at **15 seconds**, but no contrast reached **p < .05 at 5 seconds**. Its measure called “preference” meant judged faster, not liking or comfort. Relative-motion and rhythmic-timing explanations are plausible mechanisms, not separately established causes.

These studies complement [response-time thresholds](/vault/response-time-thresholds.md): they study feedback during selected waits, not the second at which a feedback treatment becomes necessary.

## Practical Use and the Ethics Boundary

1. **Reduce avoidable delay first.** Perceptual styling does not repay lost time or repair blocked work.
2. **Choose determinate feedback only when the represented whole is meaningful.** Use honest activity feedback when completion extent is unknown; do not let looping decoration imply measured advance.
3. **Keep operational meaning independent of decorative motion.** A slower-moving texture or more pleasing rhythm must not hide a stall, failure, changed estimate, or actual completion.
4. **Preserve decisions about the wait.** People should retain accurate information needed to continue, leave, or cancel. Making a wait appear almost finished to discourage cancellation crosses from comfort into misleading choice architecture.
5. **Judge the user's outcome, not only perceived speed.** Evaluate comprehension, actual delay, satisfaction, and ability to act separately; include motion comfort and nonvisual access rather than assuming visual preference establishes accessibility.

The ethical line is not that every perceptual improvement is deception. It is whether the presentation induces false beliefs or conceals information needed for informed action. The [deceptive-pattern attributes](/vault/deceptive-pattern-attributes.md) distinguish covert influence, misleading claims, hidden information, and restricted alternatives. That vocabulary supports review; neither the duration studies nor the taxonomy empirically validates a universal ethical cutoff for progress animation.

## Limitations

The visual-duration evidence concerns **attended, short, completing bars**, principally **5–15 seconds**, not long-running background work, indefinite spinners, failing operations, multiple tasks, or occasional glances. Longer pilots lost attention, and the longer duration-matching condition had not clearly stabilized. Extending the effect linearly to long waits is speculation.

The earlier query study also did not test multitasking: background-work planning was a proposed benefit. Small samples, repeated judgments, unexplained percentage denominators, selected winning treatments, and no established independent replication restrict precision. None of these studies establishes motion safety, disability-specific benefit, sustained trust, or a reason to keep people watching instead of letting them do other useful work.

## Sources

- [The Importance of Percent-Done Progress Indicators for Computer-Human Interfaces](/dossiers/percent-done-progress-indicators.md) — Supplies progress-versus-no-progress preference evidence, estimation problems, and a failed constant-latency preference replication; background-work benefits remain proposed.
- [Faster Progress Bars: Manipulating Perceived Duration with Visual Augmentations](/dossiers/faster-progress-bars-perceived-duration.md) — Supplies short attended-bar comparisons and duration matching, with mixed five-second results and no actual speed or ethical-outcome benefit established.
