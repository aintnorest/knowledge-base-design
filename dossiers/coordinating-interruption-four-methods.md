---
type: Study Note
title: Comparison of Four Primary Methods for Coordinating the Interruption of People in Human–Computer Interaction
description: A 36-person dual-task experiment favors user-negotiated interruptions overall and immediate delivery for time-critical secondary work, but compares minimal implementations around a continuous, hidden, nonpausable game.
resource: https://doi.org/10.1207/S15327051HCI1701_2
source: https://doi.org/10.1207/S15327051HCI1701_2
tags: [attention, interaction-design, human-performance, cognitive-load, digital-interfaces, taxonomy]
timestamp: 2026-10-12T23:52:39Z
---

# Four Methods for Coordinating Interruption — Study Notes

**Authors**: Daniel C. McFarlane.  
**Published**: Human–Computer Interaction **17(1), 2002, pp. 63–139**.  
**Status**: Peer-reviewed journal experiment; read the complete **77-page publisher-layout PDF** supplied from interruptions.net, including figures, questionnaires, and detailed-results appendices. The editorial record reports acceptance by Ruven Brooks and final manuscript received December 18, 2001. Crossref confirms the DOI, title, author, and pagination.  

## What It Is

An empirical comparison of **immediate, negotiated, mediated, and scheduled** interruption coordination. Coordination determines both **when secondary work arrives and who controls the switch**. The conclusion is conditional: negotiation is the best overall tested solution, **except when small differences in secondary-task timeliness are critical**, where immediate interruption is preferable.

This is not a universal ranking of every notification system. Each category has one deliberately minimal implementation, tested while a continuous primary task keeps running invisibly during secondary work. The source acknowledges that its tentative guidelines are especially relevant to that class of multitask.

## Problem and Motivation

Monitoring dynamic information, supervising autonomous services, and collaborating intermittently all create legitimate demands for attention. Eliminating those demands is not always possible; the design problem is to let people coordinate them without losing the primary task. The paper explicitly motivates intelligent-agent supervision, but **the experiment itself uses neither AI agents nor operational command-and-control work**.

Prior interruption literature supplies accounts of memory interference, recovery difficulty, anticipatory strategy changes, and individual differences. These motivate the design space; they are not separately measured causal mechanisms in this experiment. Coordination is one of eight dimensions in McFarlane's broader interruption taxonomy: source, recipient characteristics, coordination, meaning, expression, channel, changed activity, and effect.

## Mechanism and Study Design

### Four coordination methods

| Method | General principle | Tested implementation |
|---|---|---|
| Immediate | Demand attention as soon as work arrives, irrespective of current activity. | Matching work immediately replaces the game; all queued matches must be completed before returning. |
| Negotiated | Announce a request and let the person decide when or whether to address it. | Each arrival produces a **150-ms** flash of a blank matching display. The person can show/hide matching work at any time and return before clearing the queue. |
| Mediated | A broker determines when/how a request can reach the person, potentially handling it by proxy. | A workload heuristic counts visible jumpers and holds requests without notification; automatic delivery combines that count with queue length. |
| Scheduled | Restrict delivery to a prearranged time or recurring convention. | Requests accumulate silently and are delivered every **25 seconds**; the queue must then be cleared. |

The mediated rule interrupts with **0–1 jumpers**; with **2** only when the queue exceeds **2**; with **3** only when it exceeds **4**; with **4 or more** only when it exceeds **6**. Thus mediation here is not a sophisticated model of cognitive state.

### Participants, tasks, and exposure

**36 volunteers, 18 men/18 women**, ages **18–47**, median **21**, mean **24.7**, were primarily engineering students (**28**) and Navy AI-research-center employees (**6**), plus two others. Recruitment described a fun video-game-like task and offered **$20**. All passed a color-vision test; two left-handed people could use their left hand. This was self-selected, not a random population sample.

A **within-person, digram-balanced six-condition Latin square** included the four coordination methods and game-only/matching-only baselines. Every participant completed **24 trials of 4.5 minutes**: **12 practice** and **12 experimental**, two consecutive trials per condition, with at least **25 seconds** masked rest between trials. The experimental work alone comprises **432 trials / 32.4 hours**. Conditions were identified with Greek letters, and instructions declared both tasks equally important.

- **Continuous game**: move stretcher-bearers among three positions to bounce each falling character three times into safety. Each experimental trial has **59 jumpers**. A character requires its last bounce at **13.7 seconds**, then remains visible another **3.2 seconds**. Concurrent jumpers make timing difficult; individual successes/failures do not automatically affect other jumpers.
- **Intermittent matching**: choose one of two colored shapes under a changing instruction to match by color or shape, **80 matches per experimental trial**, served FIFO. Each match has a right/wrong answer; there are no interruptions of interruptions.
- **Critical constraint**: matching work completely obscures the game, which **cannot pause**. Except in negotiation, participants cannot leave before clearing queued matching work. Sound, scores, impending-event warnings, and hidden-task state feedback were deliberately omitted. One hand operates separate game/match controls, plus negotiation controls when permitted.

Event schedules are uniquely randomized for every trial under constrained interval distributions. Task similarity, interdependence, urgency, and interruption length are not factorially varied.

### Measures and analysis

Nine objective measures cover correctness, efficiency, completeness, and timeliness:

1. Jumpers saved: higher is better.
2. Game key presses per saved jumper.
3. Number of task switches, both directions.
4. Number of incorrect matches.
5. Incorrect matches as a percentage of attempted matches.
6. Matches left undone.
7. **Match age**: arrival to completion, or to trial timeout if unfinished; includes waiting.
8. **Matching speed**: display to completion; excludes waiting before display.
9. Total UI keying errors: redundant game moves, game keys in matching mode, match keys outside matching mode, illegal negotiation attempts, and unused keys. These are distinct from wrong task answers and were prevented from directly damaging task outcomes.

All but jumpers saved are treated as lower-is-better in the source. Fewer switches is not necessarily a universally desirable goal. Switches, undone work, and match age are partly imposed by the UI rather than freely controlled by users.

Pairs of experimental trials are combined, then ranked within participant. **Friedman tests with tie correction**, followed by the specified post-hoc rank comparisons, use **α = .05**. Raw chart means and ranked comparisons can order conditions differently; significance directions below follow **Figure 11 ranks**, not a visual comparison of standard-error bars. No standardized effect sizes or confidence intervals are supplied.

## Results / Admissions

### Raw means and overall differences

Figure 9 gives means per trial; baseline values are listed separately rather than pretending the baselines are dual-task conditions.

| Objective measure | Immediate | Negotiated | Mediated | Scheduled | Four-method Friedman statistic / p |
|---|---|---|---|---|---|
| Jumpers saved | **23.8** | **30.1** | **24.7** | **19.5** | **72.263 / < .0001** |
| Game keys per saved jumper | **5.67** | **4.46** | **4.85** | **5.34** | **43.000 / < .0001** |
| Task switches | **125** | **55** | **44** | **20** | **87.000 / < .0001** |
| Matches wrong | **6.35** | **4.88** | **5.10** | **4.68** | **17.599 / .0005** |
| Wrong / attempted (%) | **7.99** | **6.51** | **6.45** | **6.15** | **10.267 / .0164** |
| Matches undone | **0.58** | **5.63** | **1.31** | **3.79** | **53.034 / < .0001** |
| Match age (s) | **1.4** | **15.5** | **6.9** | **10.2** | **78.100 / < .0001** |
| Matching speed (s) | **1.21** | **0.98** | **1.07** | **1.01** | **78.733 / < .0001** |
| Total keying errors | **53.5** | **15.9** | **26.2** | **17.8** | **84.092 / < .0001** |

Negotiation increases saved jumpers by **6.3 per trial** relative to immediate delivery, but its raw mean match age is **14.1 seconds longer** and it leaves more matching work unfinished. These are descriptive contrasts, not reported standardized effects. Immediate delivery starts work promptly but **processing after display is slower**; “fast notification response” and efficient secondary work are different outcomes.

### Every objective pairwise comparison

**I = immediate; N = negotiated; M = mediated; S = scheduled.** Each cell gives the direction of mean **within-person ranks**. **An asterisk marks a significant post-hoc difference at .05**; unstarred inequalities are descriptive only, not established differences or equivalence. Higher saved-jumper ranks are better; lower ranks are better for the other rows.

| Measure | I versus N | I versus M | I versus S | N versus M | N versus S | M versus S |
|---|---|---|---|---|---|---|
| Jumpers saved | I < N* | I < M | I > S* | N > M* | N > S* | M > S* |
| Keys per saved | I > N* | I > M* | I > S | N < M | N < S* | M < S |
| Switches | I > N* | I > M* | I > S* | N > M | N > S* | M > S* |
| Matches wrong | I > N* | I > M* | I > S* | N > M | N > S | M > S |
| Wrong percentage | I > N | I > M | I > S* | N > M | N > S | M > S |
| Matches undone | I < N* | I < M | I < S* | N > M | N < S | M < S* |
| Match age | I < N* | I < M* | I < S* | N > M | N < S | M < S* |
| Matching speed | I > N* | I > M* | I > S* | N < M* | N < S | M < S |
| Keying errors | I > N* | I > M* | I > S* | N < M* | N < S | M > S* |

The rank direction of **M versus S matching speed** differs from the raw means, as does the ordering of negotiated and scheduled incomplete-work scores. This is a reported consequence of within-person ranking, not a transcription error.

### Comparisons with single-task baselines

Baseline raw means: game-only **39.8 saved**, **4.55 keys/saved**, **22.2 keying errors**; match-only **3.07 wrong**, **3.91% wrong**, **1.49 undone**, **1.6-second age**, **1.29-second matching speed**, **2.4 keying errors**. Figure 12 omnibus comparisons including baselines are all **p < .0001** for applicable measures; there is no switch baseline.

Figure 13 post-hoc results, using baseline-inclusive ranks:

- **Saved jumpers**: all four methods significantly worse than game-only.
- **Keys/saved**: immediate and scheduled significantly higher than game-only; negotiation descriptively lower but nonsignificant, mediation descriptively higher but nonsignificant.
- **Wrong matches**: immediate, negotiated, and mediated significantly higher than match-only; scheduled descriptively higher but nonsignificant.
- **Wrong percentage**: all four significantly higher than match-only.
- **Undone work**: comparisons withheld because an extra undone count may have contaminated some baseline records; experimental-condition data are reported as clean.
- **Match age**: negotiation, mediation, and scheduling significantly higher than match-only; immediate descriptively lower but nonsignificant.
- **Matching speed**: negotiation, mediation, and scheduling significantly lower than match-only; immediate descriptively lower but nonsignificant.
- **Total keying errors**: immediate significantly higher than game-only; negotiation/scheduling descriptively lower and mediation higher but nonsignificant. All four significantly higher than match-only.

### Subjective comparisons and secondary analyses

Five subjective rankings differ significantly: preference **Fr = 13.594, p = .0035**; perceived game errors **10.063, .0180**; feeling interrupted **12.851, .0050**; predictability **36.943, < .0001**; game complexity at interruption onset **15.533, .0014**. Ease, perceived matching errors, stress, distraction, and complexity on return are reported nonsignificant.

The complete significant post-hoc set is: **N preferred over I and S**; **N perceived as causing fewer game errors than I**; **N less interruptive than I and S**; **N and S each more predictable than I and M**; **N perceived as starting interruptions at lower game complexity than I and S**. Every other pair for these five rankings is nonsignificant. The nonsignificant raw rank tendencies are N > M > S > I for preference; I > S > M > N for perceived game errors; S > I > M > N for interruption; S > N > I > M for predictability; and S > I > M > N for onset complexity (higher means more of the named attribute).

**17/35 valid first choices** favored negotiation, **6 immediate, 7 mediated, 5 scheduled**; one person gave no valid preference ranking. Preference is not unanimous. Relative preference correlated with saved-jumper ranks (**Kendall τ = .237**), keys/saved (**−.178**), matching speed (**−.162**), and keying errors (**−.139**), each significant at .05. These are modest associations, not proof that letting everyone choose causes optimal performance. Single-value judgments and self-rated skills mostly did not correlate with objective performance; the source's broad rejection of self-report is stronger than this study warrants.

Trial two has slightly faster matching (**Wilcoxon = −3.095, p = .0020**) and more keying errors (**−3.266, .0011**); other trial effects and all treatment-sequence tests are nonsignificant. Order-group effects occur for saved jumpers (**Kruskal–Wallis = 15.552, p = .0082**) and switches (**13.780, .0171**). Groups starting with game-only or negotiation performed better overall; primacy/strategy formation is the proposed explanation, not a directly measured cause.

There were **9,942 UI keying errors**, about **23 per experimental trial**: **72.85%** redundant moves and **22.70%** game keys during matching. Their four-method omnibus tests are **Fr = 76.711 / 97.475, both p < .0001**. Redundant-move pairwise directions/significance match total keying errors in the table above. For game keys during matching: **I > N*, I > M*, I > S*, N < M*, N < S*, M > S** (last nonsignificant). Against baselines, redundant moves are significantly **higher I, lower N, lower S** than game-only, with M descriptively higher but nonsignificant; game keys during matching are significantly higher than match-only for I/M/S but not N. The game-only/match-only omnibus tests for these two outcomes are **83.271 / 133.530, both p < .0001**.

### The guideline tables: recommendations, not universal optima

Figure 16's tentative best/worst recommendations are reproduced below. Slashes designate methods the author groups together because a difference was not established; **nonsignificance does not demonstrate equal effectiveness**.

| Design goal | Source's best | Source's worst |
|---|---|---|
| Continuous-task accuracy | Negotiated | Scheduled |
| Continuous-task efficiency | Negotiated / mediated | Immediate / scheduled |
| Fewest task switches | Scheduled | Immediate |
| Intermittent-task accuracy | Not immediate | Immediate |
| Intermittent-task completeness | Immediate / mediated | Scheduled / negotiated |
| Intermittent-task promptness | Immediate | Scheduled / negotiated |
| Intermittent-task efficiency | Negotiated / scheduled | Immediate |
| Keying accuracy | Negotiated / scheduled | Immediate |
| User preference | Negotiated / mediated | Immediate / scheduled |
| Perceived own continuous-task accuracy | **Not immediate** | **Not negotiated** |
| Perceived least interruption | Negotiated / mediated | Immediate / scheduled |
| Perceived greatest predictability | Scheduled / negotiated | Immediate / mediated |
| Perceived continuous-task complexity when interrupted | Negotiated / mediated | Immediate / scheduled |

The perceived-accuracy row is printed in this unusual form; it should not erase the clearer result that negotiation yielded fewer perceived game errors than immediate delivery.

Figure 17 gives **correlational**, user-relative recommendations: preferred methods associate with better continuous-task effectiveness/efficiency, intermittent processing efficiency, and keying accuracy; perceived ease with intermittent accuracy; greater interruption with worse continuous effectiveness/efficiency, intermittent efficiency, and keying accuracy; greater distraction with worse continuous effectiveness and intermittent accuracy/efficiency. Predictability associates with faster processing and fewer keying errors **but poorer completeness/timeliness**. Convenient low-demand onset associates with better continuous effectiveness/efficiency and faster intermittent processing. These are not tested personalization algorithms.

## Analyst Takeaways

1. **Negotiate deferrable attention, not merely notification styling.** The successful condition lets users interleave work and return before emptying the secondary queue. Its advantage cannot be attributed to delayed onset alone.
2. **Separate deadline compliance from handling speed.** Immediate delivery minimizes arrival-to-completion age but does not minimize display-to-completion time, errors, or primary-task loss.
3. **Treat mediation as a model that can be wrong.** The tested mediator's “low workload” can result from jumpers already being lost while hidden; it then interrupts again, creating a feedback loop. Current visible workload is not necessarily current task demand.
4. **Do not confuse fewer switches with better work.** Scheduling minimizes switches yet saves the fewest jumpers. Optimize the actual consequence of each task, not a convenient activity metric.
5. **For agent supervision, expose negotiable requests without forcibly hiding ongoing state.** This is an extrapolation from the abstract game to software/AI-agent supervision, consistent with the source's motivation, not a measured AI result. Hybrid mediated defaults with user override were suggested by three participants but not tested.

The timing distinction complements [interruption costs](/vault/interruption-costs.md) and the [attention-aware experiment](/dossiers/attention-aware-systems-interruption-effects.md), but negotiation here offers substantially more control than that study's forced modal tasks. Notification detection, covered by [motion cues](/vault/motion-cues-attention-and-distraction.md), does not by itself establish successful coordination or recovery.

## Questions and Limitations

- One implementation per method bundles onset, notification, batching, switching control, and ability to leave a queue. The experiment cannot isolate which ingredient caused negotiation's advantage or establish that all mediators perform worse.
- The continuous, hidden, nonpausable game with independent subtasks differs from document work, dependent workflows, and safety-critical operational tasks. Priorities and memory demands were not varied; low-frequency interruption environments require further study.
- Order effects remain despite an hour of practice. The author judges them nonconfounding from graphs, but switch differences occur specifically in negotiation; the broader “no effect of repeated measures” summary needs this qualification.
- **Internal inconsistencies**: the mediation prose says the queue does not exceed six, while its explicit rule interrupts only when it is **more than six** at highest workload. Figure B–12 prints stress **Fr = 9.9771, p = .8563**, an incompatible pair for the stated four-condition Friedman reference distribution; retain its reported nonsignificance without treating the statistic as resolved. Figure 16's perceived-accuracy wording is ambiguous/reversed relative to its natural best/worst labels. Section B3's discussion refers to distraction (26) where its stated interruption associations belong to interruption (25). The paper also references nonexistent Section 6.6 and Figure 33A, apparently stale cross-references.
- Most subjective–objective associations are small and drawn from **90 comparisons**; self-report correlations involve **945** and **567** pairs. The dossier does not treat isolated associations as robust universal predictions. Nonparametric testing alone does not remove all dependence or sampling assumptions, despite the paper's broad methodological assurances.
- The article revises/extends the author's **1998 dissertation and INTERACT 1999 paper**, rather than establishing independent replication of them. No independent replication of this exact four-way experiment is documented here.
- **Redistribution evidence**: no explicit Creative Commons or equivalent public-redistribution grant appears in the supplied PDF. Its publisher layout and third-party hosting are not permission. Keep the raw copy in the private archive and cite the DOI.

## Vault Ideas Extracted

- [Interruption Coordination](/vault/interruption-coordination.md) — Proposes a new synthesis separating immediate, negotiated, mediated, and scheduled attention control, with the full correctness/completeness/timeliness tradeoff and limited four-way evidence.
- [Interruption Costs](/vault/interruption-costs.md) — Adds primary-task loss and mode-keying errors under forced switching, and distinguishes request waiting from processing time.
- [Visibility of System Status](/vault/visibility-of-system-status.md) — Adds the hidden, continuously evolving primary task as a recovery problem; the benefit of persistent visibility itself was not experimentally isolated.
