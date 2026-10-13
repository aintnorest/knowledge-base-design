---
type: Study Note
title: "Disruption and Recovery of Computing Tasks: Field Study, Analysis, and Directions"
description: Two weeks of workplace logging associate communication-alert diversions with roughly 8–10 minutes away and a further 11–17-minute resumption phase, but window-based observational proxies cannot isolate cognitive recovery or prove alerts caused the whole delay.
resource: https://doi.org/10.1145/1240624.1240730
source: https://doi.org/10.1145/1240624.1240730
tags: [attention, cognitive-load, interaction-design, human-performance, digital-interfaces, user-research]
timestamp: 2026-10-12T23:52:39Z
---

# Disruption and Recovery of Computing Tasks — Study Notes

**Authors**: Shamsi T. Iqbal and Eric Horvitz.  
**Published**: Proceedings of CHI 2007, **pp. 677–686**, conference April 28–May 3, 2007, San Jose, California.  
**Status**: Peer-reviewed conference field-study paper. Read the complete **10-page Microsoft-hosted PDF**, including lifecycle diagram, tables, cumulative-probability figures, and references. Crossref confirms DOI, authors, venue, and pagination; its abbreviated title omits the subtitle printed in this version.  

## What It Is

A naturalistic study of **task suspension, chains of diversion, and eventual resumption** around email and instant-messaging alerts. Its important contribution is distinguishing returning to a window from returning to sustained work: efficient application switching does not guarantee efficient task recovery.

The study shows associations in ordinary workplace behavior, not a randomized cost of receiving versus suppressing alerts. Its proposed reminder, context-preservation, and playback designs are **research directions**, not interventions evaluated by this study.

## Problem and Motivation

A communication alert can initiate more than one response. People may check additional messages, visit other applications, or start other work before returning. A task can involve several windows, so remembering one application is not the same as reconstructing the original activity's context.

The authors ask whether people stabilize work before leaving, switch more rapidly during diversion/recovery, focus on communication during diversions, return faster when suspended windows remain visible, struggle to resume, and recover differently according to prior task focus. Cognitive-resource reallocation and memory reconstruction are explanatory accounts from prior work; **the logger does not directly measure memory or mental workload**.

## Mechanism and Study Design

### People and logging

The DART background logger was deployed on **27 people's primary computers at Microsoft over two weeks**. Roles included program manager, administrator, researcher, and developer; primary work included programming, document editing, presentations, and managing external communications. The authors sought varied work roles, not a representative random sample. They excluded from alert analysis people without alerts enabled, but **do not report the final included participant count or demographic distribution**. Availability/interest determined the **14 face-to-face follow-up interviews**.

The dataset contains **2,267 hours across 974 sessions**, defined by login/logout or unlock/lock. Mean session length is reported as **2 h 17 m, SD 410.37 minutes**. Logging captured application/window access, dimensions and position, visibility, opening/closing, mouse/keyboard activity, and selected content events: periods/carriage returns, saving, cutting, and pasting. Window titles were truncated and only selected keyboard events collected for privacy. Users knew monitoring was occurring but not its interruption/recovery purpose.

Alerts came from **Outlook**, **Windows Messenger**, **MSN Messenger**, and **Office Communicator**. IM logging **did not distinguish conversation pings from sign-in/presence alerts**. That matters: conversational response obligations cannot explain every logged IM event.

### Operational definitions: the phases are proxies

Figure 1 depicts a primary task distributed across applications, an alert, response preparation, diversion into peripheral work, and a return across the suspended application group.

- **Pre-interruption baseline**: the **five minutes before an alert**, not a matched no-alert experimental condition.
- **Preparation**: alert arrival to switching into its notifying application. A switch within **15 seconds** is classified as immediate and likely alert-driven; later switches are called delayed/self-initiated. This is a causal-attribution heuristic, not proof of the user's motive.
- **Diversion**: response to the notifying application and visits to peripheral applications before accessing any suspended application. First return is a proxy for intent to resume, **not completed task recovery**.
- **Resumption**: a period inferred from minimizing/closing peripheral windows and beginning to revisit suspended work, until renewed activity. **More than 15 seconds on a suspended application** counts as resumption, including possible reading without input. The authors acknowledge that the phase's onset is difficult to identify.

Focus is approximated by window-switch rates and prior dwell duration. Paragraph completion uses carriage-return-like events, not semantic understanding of a completed thought. Consequently, “resumption phase” includes navigating among task windows and other activity; it is not an isolated laboratory resumption lag or a direct measure of restored mental state.

## Results / Admissions

### Alert frequency and initial response

Hourly means were **4.28 email alerts (SD 5.56)** and **3.21 IM alerts (SD 4.31)**; the paper reports an overall **3.74/hour (SD 4.94)**. That overall number is not the sum of channel rates and should not be quoted as each person's total combined alert burden. Job roles did not significantly affect alert counts.

Across all responses, mean delays were **4 m 59 s** to Outlook (**SD 8 m 43 s**), **7 m 54 s** to MSN Messenger (**SD 16 m 50 s**), **7 m 13 s** to Communicator (**SD 13 m 49 s**), and **34 s** to Windows Messenger (**SD 1 m 5 s**). The source reports no significant differences by alert type or job role despite the disparate means.

| Channel | Immediate response (< 15 s) | Delayed response | Suspended task windows |
|---|---|---|---|
| Email | **40.8%, 2,344/5,747**; mean **2 s**, SD **3.77 s** in the detailed subsection | **59.2%**; mean **7 m 32 s**, SD **11 m** | Approximately **3**, SD **1.92** immediate / **2.1** delayed |
| IM, including presence alerts | **71.01%, 3,186/4,487**; mean **1.72 s**, SD **1.1 s** | **28.99%, 1,301/4,487**; mean **8 m 48 s** | Approximately **3**, SD **2.3** |

The initial heuristic discussion gives immediate Outlook mean **2.35 s, SD 1.39 s**, rather than the detailed **2 s, SD 3.77 s**. It also says email responders tabbed through **7.5 applications** on average (**SD 2.88, printed with a seconds unit**) while saying no other application was interacted with; traversing without dwelling may explain the latter distinction, but its meaning is underspecified. No intermediate application was accessed for immediate IM responses.

### Diversion is separate from resumption

Time from switching to the alerting application until **first access to any suspended application** averaged **9 m 33 s for email (SD 13 m 15 s)** and **8 m for IM (SD 11 m 32 s)**. The source says these durations are similar across immediate/delayed response patterns but does not provide a full subgroup table.

The **additional resumption-phase durations**, not total alert-to-recovery times, were:

| Channel and response | Mean resumption phase | SD |
|---|---|---|
| Email, immediate | **16 m 33 s** | **27 m 20 s** |
| Email, delayed | **15 m 50 s** | **25 m 5 s** |
| IM, immediate | **10 m 58 s** | **14 m 16 s** |
| IM, delayed | **12 m 2 s** | **14 m 58 s** |

Immediate versus delayed differences within each channel were **not significant**. Do not turn these means into “every notification costs 25 minutes,” a measured period of pure mental reconstruction, or a causal productivity-loss estimate. Some peripheral work may be useful, and the phases have heuristic boundaries.

### Preparation and task focus

Paragraph completions increased from **0.78/min (SD .49)** at baseline to **10.9/min (SD 5.2)** before immediate IM responses, **12.8/min (SD 13.75)** before immediate email responses, and **1.17/min (SD .49)** before delayed email responses; all reported comparisons are **p < .038**. The interpretation is that people may finish conceptual/motor subtasks before switching. Very short preparation denominators also produce high per-minute rates; these are not several minutes of sustained accelerated writing.

Pasting before delayed email responses increased **.37 → .69/min** (**SD .12 / .62**) only **marginally, p < .067**. Externalizing a clipboard goal is plausible because it otherwise lacks a visible reminder, but the study does not establish a significant conventional-.05 effect or directly observe that intention. Saving did **not** significantly increase; interviewees described habitual periodic saving.

Table 1 records switches per minute (**mean, SD**):

| Phase | Email | IM |
|---|---|---|
| Baseline | **.84 (.60)** | **.84 (.60)** |
| Immediate preparation | **0** | **0** |
| Delayed preparation | **.69 (.62)** | **.49 (.45)** |
| Immediate diversion | **1.33 (1.95)** | **1.42 (2.36)** |
| Delayed diversion | **1.24 (2.01)** | **1.36 (2.33)** |
| Immediate resumption | **2.34 (2.71)** | **2.56 (2.82)** |
| Delayed resumption | **2.42 (3.26)** | **2.05 (2.14)** |

Diversion exceeds baseline (**t(18) = 6.787, p < .001**); resumption exceeds baseline (**p < .0001**) and diversion (**p < .0004**). Greater switching supports the hypothesized browsing/search pattern, not a direct measurement of poor concentration. Job-role influence during email preparation was only marginal (**F(2,15) = 3.442, p < .059**); researchers versus developers **p < .06**. Other role effects were absent.

### Communication expands during diversion

Communication-application traversal rose from **.475/min (SD .21)** to **.77/min (SD 1.56)**, **t(19) = 4.283, p < .001**. Mean dwell per visit rose **33 s (SD 7.5) → 66 s (SD 165.9)**, **t(10) = 3.674, p < .002**. Rapid switching and longer individual communication visits can coexist.

| Outlook action / minute | Baseline mean (SD) | Diversion mean (SD) | p |
|---|---|---|---|
| Open mail | **.53 (.50)** | **3.66 (6.70)** | **.001** |
| Write mail | **.44 (.31)** | **3.15 (5.71)** | **.002** |
| Send mail | **.35 (.27)** | **1.69 (2.89)** | **.008** |

Web-mail visits also increased **.41 → 1.76/min** (**SD .27 / 1.91**), **t(7) = 3.357, p < .012**. An alert-associated break can become an opportunity to handle other communications, not merely the triggering message.

### What is associated with slow return?

- **Occlusion**: suspended windows **<25% visible** took longer to return to than those **>75% visible** for email (**t(20) = 3.131, p < .005**) and IM (**t(23) = 2.503, p < .02**). No duration difference, confidence interval, or adjusted causal effect is reported. Visible windows may remind users, but task priority, display arrangement, and selection could also explain the association.
- **Brief prior focus**: Figure 3 shows windows worked on for **5–30 minutes** before suspension usually resumed within **5–15 minutes into resumption**; those with **<5 minutes** prior engagement had approximately **10% probability of not resuming within two hours**. No formal significance test is reported for these curves. The 15–30-minute group reaches its plateau sooner than the 5–15-minute group.
- **Long-tail delays**: among windows active during the **15 seconds before suspension**, approximately **27% of alerts** were associated with those windows not being resumed for **more than two hours into resumption**. This selected active-window analysis is not interchangeable with the mean phase durations above.
- **Response/channel pattern**: Figure 2 shows delayed email responses with the lowest probability of resuming the selected recently active windows within two hours, immediate IM highest, delayed IM next, and immediate email next. Descriptively, delayed email is near **40%** at two hours versus roughly **75% immediate email**, **83% delayed IM**, and **97% immediate IM**. These are approximate chart readings, not independently tabulated estimates or significant pairwise effects.
- **Deadline/importance and display focus**: interviewees reported that important tasks/deadlines prompted earlier return, and windows on an unattended secondary display were weaker reminders. These are reported experiences; the study does not isolate their effects experimentally or fit a validated prediction model.

Interviewees often intended to return quickly but stayed away longer than expected. Some described social pressure to answer IM; others treated work email as more urgent than social IM. All reported habitual self-interruption to check Outlook independently of alerts. They left cursors/highlights as context cues, sometimes used undo sequences to recall earlier actions, and reported difficulty restoring multi-application context. These explanations enrich, but do not causally validate, the logs.

## Design Directions: What the Source Recommends

Four proposals follow from the associations and interviews:

1. **Make occluded suspended work visible enough to remember.** Suggested approaches include reminder icons and progressively revealing hidden windows according to time since access and task importance. No particular cue design was tested.
2. **Preserve task context on suspension, not just document bytes.** A task may require a document, spreadsheet, and analysis application together. Saving/restoring their joint state is proposed to reduce reconstruction effort; the field study did not evaluate automatic context capture.
3. **Provide easy access to the suspended context.** Thumbnails of suspended states could make return easier. This is a design example, not a measured thumbnail benefit.
4. **Provide a review of recent actions and context.** Playback is motivated by users employing undo to remember previous steps. It is not evidence that literal replay or additional undo operations are safe or effective.

The authors explicitly warn that reminder/recovery cues can themselves interrupt **more important current work**. Appropriate timing, display technique, and task-priority handling remain unresolved design problems. Recovery support should not mandate returning to whichever activity happened to be earlier.

## Analyst Takeaways

1. **Measure return and recovery separately.** First opening a suspended window, finding the right context, and sustained work are different events. A fast application switch does not show successful cognitive recovery.
2. **Design for the diversion chain, not only the first message.** A short initial response can initiate additional communication and peripheral work; message dismissal time alone understates the observed lifecycle.
3. **Preserve a task's cross-application context and visible place to resume.** The logs support a visibility association; interviews support the importance of multi-window context. Exact reminder and restoration designs still need causal evaluation.
4. **Do not equate every delay with harm.** Deliberately doing important new work may be appropriate. Recovery cues should preserve agency and priority rather than maximize mechanical return rate.
5. **For software/AI-agent supervision, retain suspended goals and reviewable recent actions.** This is an extrapolation beyond the studied email/IM workplace setting, not an AI performance finding. A resumable supervisory context is more defensible than repeatedly forcing the person back into earlier work.

This adds a naturalistic recovery lifecycle to [interruption costs](/vault/interruption-costs.md) and the controlled [attention-aware timing study](/dossiers/attention-aware-systems-interruption-effects.md). It also distinguishes persistent reminders from the initial attention capture in [motion cues](/vault/motion-cues-attention-and-distraction.md): a cue can be noticed without ensuring a timely return.

## Questions and Limitations

- Observational associations cannot establish that alerts caused the entire diversion/resumption duration or that increasing visibility will shorten it. The **15-second** attribution and resumption thresholds are heuristics; delayed responses may still be alert-influenced and immediate switches may be coincidental.
- Window/application activity is an imperfect task model. A person can read without input, use one application for several tasks, or switch applications within the same task. The exact algorithm for identifying full resumption of a multi-window task is not sufficiently specified to reconstruct a cognitive-recovery endpoint.
- The analyzed participant count after alert-disabled exclusions is unstated; degrees of freedom vary substantially across tests. No event-level exclusion/censoring account, confidence intervals, standardized effects, or multiple-comparison correction is provided. Very large SDs and two-hour tails make means poor universal expectations.
- **Internal inconsistencies**: the two immediate-email delay summaries differ (**2.35 s / SD 1.39** versus **2 s / SD 3.77**). The supplied totals **2,267 hours / 974 sessions** imply about **2 h 20 m**, not precisely the printed **2 h 17 m**; the paper does not explain whether summaries use different subsets. Its overall **3.74 alerts/hour** is between the channel means, not their combined sum, with the aggregation denominator unclear. The application-count SD is printed in seconds. The “less focused” interpretation sits alongside significantly longer communication dwell times and should not be read as less engagement on every individual application.
- The lessons section says immediate responders seldom stabilize work and describes saving as part of delayed preparation, whereas the quantitative section finds **strongly increased immediate paragraph-completion rates** and **no significant saving increase**. Retain the measured results rather than treating the narrative summary as an established immediate-versus-delayed contrast.
- Figure 2's delayed-email two-hour resumption probability is much lower than the roughly 16-minute mean phase duration. These involve different reported windows/phase summaries, but the paper does not give enough denominator and censoring detail to reconcile them completely. Do not combine the distributions and means into one synthetic recovery statistic.
- The supplied paper's reference to Bailey/Konstan prints **pp. 709–732**, whereas the existing [dossier](/dossiers/attention-aware-systems-interruption-effects.md) records **685–708** for the title it cites. This bibliography discrepancy is not evidence of a separate replication.
- One organization's 2007 desktop communication environment and self-selected interview subset limit transfer to mobile work, modern collaboration suites, disability-related needs, or other occupations. Phone and face-to-face interruptions were not logged. No independent replication of this exact field analysis is established here.
- **Redistribution evidence**: the first page grants copies for **“personal or classroom use”**, but says **“to republish, to post on servers or to redistribute to lists, requires prior specific permission and/or a fee.”** It also states **“Copyright 2007 ACM.”** This is not permission for a public repository archive; retain the raw PDF privately and cite the DOI.

## Vault Ideas Extracted

- [Interruption Costs](/vault/interruption-costs.md) — Adds two-week workplace evidence that communication-alert responses can expand into lengthy diversion chains, and separates first return from sustained resumption, with observational visibility/prior-focus associations; elapsed time is not causal cognitive overhead.
- [Visibility of System Status](/vault/visibility-of-system-status.md) — Adds the distinction between remembering suspended work and restoring its multi-application context; visible-window associations motivate, but do not validate, recovery cues.
