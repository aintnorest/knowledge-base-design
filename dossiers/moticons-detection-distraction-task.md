---
type: Study Note
title: "Moticons: Detection, Distraction and Task"
description: Small dual-task experiments find oscillating icons easier to detect than color or shape changes, especially far from the task, but traveling motion draws more subjective distraction and primary-task harm was not measured.
resource: https://doi.org/10.1016/S1071-5819(03)00021-1
source: https://doi.org/10.1016/S1071-5819(03)00021-1
tags: [motion, attention, visual-perception, human-performance, digital-interfaces]
timestamp: 2026-10-12T20:26:48Z
---

# Moticons — Study Notes

**Authors**: Lyn Bartram, Colin Ware, and Tom Calvert.  
**Published**: International Journal of Human-Computer Studies **58(5), May 2003, pp. 515–545**.  
**Status**: Peer-reviewed journal article; read the supplied **28-page author manuscript**, not the journal-layout version. The file prints neither DOI nor publication details; [Crossref's DOI record](https://api.crossref.org/works/10.1016/S1071-5819(03)00021-1) verifies authors, venue, issue, and pages, although its title field is truncated to “Moticons:”. The full title above follows the manuscript.  

## What It Is

Three studies of simple moving icons as notification signals during a concurrent primary task. Experiments **1A/1B** compare motion with color and shape change; Experiment **2** adds identifying which icon changed in a heterogeneous display; Experiment **3** compares detection and subjective distraction/irritation across different tasks and motion trajectories.

The durable distinction is between **noticing an event, locating its source, and being distracted after noticing it**. Good detection is not proof of low interference, comprehension of the event's meaning, or successful primary-task performance.

## Problem and Motivation

Static changes can be poor notifications when the user is looking elsewhere, especially when color and shape already encode other data. The source seeks signals that preserve those existing encodings while communicating that something happened. Its rationale is that peripheral motion sensitivity falls off less than fine shape or color discrimination.

The authors use Woods' criteria for attention-management tools: information should be accessible without abandoning current work, convey enough partial meaning to inform an attention shift, and be mentally economical. Whether motion meets these criteria is an empirical question, not something established by calling it preattentive.

## Mechanism as an Idea

A local oscillation adds a change channel without replacing the icon's static color or shape. An **anchored** motion remains near the icon's origin; a **traveling** motion crosses a much larger area and may demand continued tracking. Detection and tracking can therefore impose different attention costs even when both signals are easy to notice.

Only one cue occurred at a time. The studies do not establish that dozens of simultaneously moving icons retain this advantage. Nor does a motion-detection result determine whether the user understands the state it represents; that is a separate question from [visibility of system status](/vault/visibility-of-system-status.md).

## Results / Admissions

### Experiments 1A and 1B: detection versus color and shape

**Participants**: the same **12 paid SFU Computing Science/Psychology students**, **6 women and 6 men**, completed both parts in counterbalanced order; none were color-blind and five wore glasses.

**Task and conditions**: edit a scrollable number table, replacing every 0 with 1, while monitoring **15 icons** on a **116 × 87 cm**, **800 × 600** projected screen from **95 cm** away. The primary task was left or right, counterbalanced by block. Near targets were approximately **7–20°** from its center; far targets **40–52°**. Middle-distance icons were never targets. Cues began **5–20 seconds** into the trial, lasted **5 seconds**, and an undetected trial timed out at **30 seconds**. Participants pressed a key on detection.

Each part used four cue types crossed with near/far location, plus no-change conditions (**20%** of trials), **80 trials per person**, with randomized order and prior training. Motion was vertical sinusoidal oscillation at approximately **3 Hz**, either one icon-height or half an icon-height; this also changes velocity, so amplitude is not isolated from speed. In 1A, differently shaped black icons changed to red or green. In 1B, differently colored circles changed to X or flag shapes. Measures were **detection error and response time**, not primary-task completion.

- **1A**: motion detection was nearly **100%** at both eccentricities, with times around **1 second**. Color error averaged **5.5% near versus 24% far**, with detection times **2.3 versus 4.6 seconds**. Reported error effects: cue **F(4,48) = 14.098, p < .0001**; location **F(1,12) = 14.846, p < .0002**; interaction **F(4,48) = 7.304, p < .0001**. Time effects: cue **F(4,48) = 40.278, p < .0001**; location **F(1,12) = 7.135, p < .01**; interaction **F(4,48) = 2.695, p < .05**. Motion amplitude had no reported effect.
- **1B**: shape detection became less accurate and slower in the far field; shape times averaged approximately **2.0 versus 4.4 seconds**, while high-amplitude motion stayed around **1 second**. Error effects: cue **F(4,48) = 13.19, p < .0001**; location **F(1,12) = 15.92, p < .0001**; interaction **F(4,48) = 7.37, p < .0001**. Time effects: cue **F(4,48) = 19.55, p < .0001**; location **F(1,12) = 31.33, p < .0001**; interaction **F(4,48) = 4.66, p < .05**. Low-amplitude motion slowed from **0.92 to 1.78 seconds** far from the task, unlike 1A. The authors explicitly call this discrepancy puzzling and propose speed/distance thresholds rather than a demonstrated cause.

The conclusion rounds color failures to **6%/25%** and motion failures to **under 2%**. The precise earlier **5.5%/24%** figures should not be silently replaced by those rounded summaries.

### Experiment 2: detecting and identifying the changed object

**Participants**: **12 paid SFU students** in Computing Science, Psychology, or Kinesiology; none color-blind, four wearing glasses. Whether they overlapped with Experiment 1 is not stated.

**Task and conditions**: same editing task, display, and eccentricities, but icons now varied in both shape and color. Six signals were a green color change, an X shape change, smooth/jumpy linear motion, and smooth/jumpy enlargement-and-shrinkage (“zoom”). Jumpy variants returned abruptly to the original position/size. No-change trials accounted for **25%**; there were **80 trials per person**, with training and randomized conditions. Following detection or timeout, users pointed to the changed icon or reported no change; identification was not time-limited. Measures were detection and identification **errors and times**. Timing analyses included incorrect as well as correct responses.

- Motion detection was more accurate than static change in both fields: **F(6,72) = 72.76, p < .0001**. Location affected error **F(1,12) = 22.67, p < .0001**, with cue–location interaction **F(7,84) = 12.84, p < .0001**. Figure 8 places static errors roughly at **35% color/20% shape near**, and **55% color/65% shape far**, while motion errors are much smaller. These are approximate graph readings, not tabulated estimates.
- Detection time differed by cue, **F(5,60) = 29.52, p < .0001**, with no overall location effect but an interaction **F(5,60) = 4.28, p < .001**. Motion was faster than both static cues near and faster than color far; high far-field shape failure prevents interpreting its surviving detection times as good overall performance. Smooth versus jumpy motion did not significantly differ.
- Identification accuracy differed by cue, **F(5,60) = 8.85, p < .0001**, with no location effect or interaction. **Figure 10 contradicts the text's identification percentages**: its color-error bars are about **20% near/15% far**, not “almost 50%” and “over 60%.” The X bars are about **6%/5%**, and motion bars approximately **0–7%**. These chart values are approximate; the manuscript does not resolve the discrepancy or fully explain the denominator after failed detections.
- Identification times were all approximately **1.5 seconds**, with no significant effects. Motion improved source identification accuracy in the reported analysis, **not identification speed**.

### Experiment 3: motion type, task, distraction, and irritation

**Participants**: **14 paid SFU students**, equal women/men, from Psychology, Engineering, Computer Science, and Kinesiology; none color-blind.

**Task and conditions**: a central task on a **21-inch monitor**, framed by **32 fixed-position icons**, with randomized icon shapes/colors. Tasks were studying unfamiliar online text, user-paced FreeCell, and continuously paced Tetris. Four cue types—linear local motion, zoom, blink, and screen-crossing travel—each had nominal slow/fast frequencies around **1/2 Hz**. Each participant performed **12 blocks**: four for each task, eight cues per block (**96 cue trials**). Task order was counterbalanced, cue order/location randomized and balanced. Cues lasted **10 seconds** and continued after detection.

After each block, shorter replays elicited four separate **5-point ratings**: current distraction, hypothetical persistent distraction, irritation, and hypothetical persistent irritation. Distraction meant continued awareness/attention demand after detection. These are retrospective ratings, not measured declines in primary-task performance, and persistent exposure was hypothetical.

- Detection was most accurate and fastest during text; game conditions were harder, and FreeCell produced the slowest times despite the prediction that Tetris would be most demanding. Reported error effects were cue **F(7,84) = 3.84, p < .001** and task **F(2,24) = 4.75, p < .0001**; the statistical reporting problems below limit confidence in these exact labels.
- Slow blinking was generally least detectable. Even its worst case was **89% detected within 10 seconds**, with mean time **under 3 seconds**. Linear/travel cues were efficiently detected, but traveling did not clearly outperform anchored motion. Faster motion did not generally improve detection aside from the slow-blink disadvantage. Figure 14's pairwise matrix shows task-specific differences, not a universal ordering of all eight cues.
- The four subjective scales differed little, so the paper reports only distraction in detail; longer hypothetical persistence increased ratings somewhat but **not significantly**. Reported rating effects: task **F(2,24) = 14.62**, motion type **F(7,84) = 86.89**, and frequency **F(1,12) = 40.18**, all **p < .0001** as printed.
- Traveling motion was rated most distracting, zoom next, with slow blink and slow linear among the least. Figure 15 approximately spans **1–1.4 blink**, **1.3–1.8 linear**, **1.9–2.3 zoom**, and **2.7–3.1 travel**; Figure 17's Tukey matrix supports traveling's high cost across tasks. These are approximate graph readings. The authors recommend slow local linear motion as a compromise between reliable detection and low subjective distraction.

## Analyst Takeaways

1. **Separate persistent state coding from event signaling.** Color/shape may encode what an object is while motion announces a change; the experiment does not show motion conveys every state meaning better.
2. **Evaluate cues where users are looking away.** Central inspection can conceal notification failures that become apparent with peripheral placement and an occupied primary task.
3. **Prefer bounded local change over unnecessary travel when attention capture is needed.** Large trajectories add subjective cost without a demonstrated general detection advantage.
4. **Measure detection and primary-task harm independently.** Failure to notice a signal and disruption from attending to it are different outcomes; this paper measured the former and subjective ratings, not actual task slowdown.
5. **Do not assume more speed means better notification.** Type, context, existing task motion, and individual engagement all mattered; slow local motion was often sufficient.

## Questions and Limitations

- Samples are small, student-based, and explicitly exclude color-blind participants. There is no disability-specific or motion-sensitivity evaluation, no simultaneous-alarm test, no long-term habituation test, and no established independent replication of these exact experiments in the supplied source. Experiments 1 and 2 corroborate detection direction within the same research program, not independent replication.
- No confidence intervals or standardized effect sizes are supplied. Degrees of freedom repeatedly conflict with reported sample sizes: **12 participants** coexist with denominators **12/48/60/72/84** suggestive of different analysis counts, while Experiment 3 reports **14** but often uses the earlier denominators. No exclusion explanation is given. Several F/p pairs also appear incompatible with conventional F distributions, e.g. **F(2,24) = 4.75, p < .0001**. Statistics above are quotations, not independently corrected estimates.
- The manuscript says “five hypotheses” then lists six; calls its seven listed initial colors “6”; prints screen resolution as approximately **145 mm/pixel**, inconsistent with **116 cm/800 pixels ≈ 1.45 mm/pixel**; and retains broken figure numbers/references such as “0-1” and “5-11.” Experiment 2's factor-count wording is ambiguous, although its 25% no-change description implies two no-change levels within eight cue levels.
- The identification-error prose disagrees with Figure 10. Figure 16 also depicts its labeled **slow** ratings above **fast** across tasks, whereas Figure 15 and the discussion associate fast cues with greater distraction. The frequency description “30 frames/sec” slow versus “15 frames/sec” fast is ambiguous alongside nominal 1/2 Hz. Preserve the qualitative trajectory result rather than treating frequency values as a precise recipe.
- The text claims evenly distributing cues removes task-timing effects, but no timing-effect manipulation establishes that. Speculation about tracking, perceptual onset, or engagement is not a direct measurement of those mechanisms.
- **Redistribution evidence**: no copyright notice, permissive license, or explicit redistribution grant was found in the manuscript. Crossref's separate text/data-mining license metadata is not a grant to republish this supplied file. Keep the raw author manuscript private.

## Vault Ideas Extracted

- [Motion Cues: Attention and Distraction](/vault/motion-cues-attention-and-distraction.md) — Supplies peripheral detection advantages, trajectory-dependent distraction, and the boundary between subjective demand and unmeasured task harm.
- [Color Coding for Status](/vault/color-coding-for-status.md) — Shows color-change notifications degrading with eccentricity and heterogeneous background coding; does not test conventional color meanings or state comprehension.
- [Visibility of System Status](/vault/visibility-of-system-status.md) — Separates detecting a state-change signal from identifying its source and understanding the state it represents.
- [Glanceable Peripheral Displays](/vault/glanceable-peripheral-displays.md) — Supplies controlled dual-task evidence that peripheral notification detection depends on the cue type and distance from the task, while subjective distraction rises with traveling motion.
