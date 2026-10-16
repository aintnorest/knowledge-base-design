---
type: Study Note
title: "Establishing tradeoffs that leverage attention for utility: empirically evaluating information display in notification systems"
description: Two undergraduate dual-task experiments separate primary-task interruption, notification reaction, and later comprehension, finding faster reaction to in-place text than tickers but implementation- and recall-dependent comprehension advantages.
resource: https://doi.org/10.1016/s1071-5819(03)00022-3
source: https://doi.org/10.1016/s1071-5819(03)00022-3
tags: [attention, motion, human-performance, ux-metrics, digital-interfaces]
timestamp: 2026-10-16T00:00:00Z
---

# Notification Display Attention–Utility Tradeoffs — Study Notes

**Authors**: D. Scott McCrickard, Richard Catrambone, C. M. Chewar, and John T. Stasko.  
**Published**: International Journal of Human-Computer Studies **58(5), May 2003, pp. 547–582**.  
**Status**: Peer-reviewed journal article; read the supplied **32-page author manuscript**, including all 12 figures, both recommendation tables, and references. [Crossref's record](https://api.crossref.org/works/10.1016/s1071-5819(03)00022-3) confirms publication metadata and returns the DOI with lowercase **s**; the source key follows that case. Manuscript pagination is not the journal's pagination.

## What It Is

An evaluation framework plus two experiments on cycling textual secondary displays during a primary browsing task. The durable contribution is **three separately measured objectives**:

- **Interruption:** primary-task performance cost when attention is reallocated.
- **Reaction:** timely acknowledgment of a specified secondary-information state.
- **Comprehension:** later recognition of categories, details, and temporal patterns in the secondary information.

These objectives can conflict. A conspicuous or fast-to-read notification is not automatically memorable or harmless. The authors recommend choosing a balance appropriate to the task, not maximizing one generic “notification effectiveness” score.

## Tasks and Measures

Participants navigated condensed text-only hypertext pages to find numerical answers. Incorrect answers required continued work. A separate display cycled fictional but realistic news, stocks, weather, and sports information; participants acknowledged two specified conditions per round and later answered multiple-answer, four-choice awareness questions. Figure 1 shows the browser, separate cycling display, and response area.

Primary measures were **time to correct answer, incorrect attempts, and back-button selections** as a proxy for bad links, plus retrospective perceived intrusiveness. Secondary measures were **monitoring latency from information availability to button acknowledgment**, basic category hit/false-alarm rates, and detailed-awareness correct-choice and false-alarm rates. “Detailed awareness hit rate” includes recognizing correct **and incorrect** choices; it is not a pure count of facts freely recalled. Acknowledgment latency includes monitoring and reading opportunities in a cyclic display, not only perceptual detection or motor reaction time.

Both tasks required visual attention and moderate processing; the investigators specified **no task priority or urgency**. Each round reportedly contained four browsing tasks. Browsing observations exceeding five minutes or five attempts were screened out, so the reported primary-task results exclude some of the worst outcomes.

## Experiment 1: Fade, Ticker, Abrupt Replacement, and No Display

**Participants and design:** **70 undergraduates**, participating for class credit. A **15-person no-display control** performed only browsing; **55** experienced all three secondary-display styles over six rounds, with counterbalanced starting order (groups **17, 17, 21**). Each style occurred in two rounds. Of **1,680** possible browsing observations, **1,629** passed screening. The manuscript calls abrupt replacement “blast”; its order list inconsistently prints “browse” where this condition is expected.

**Stimuli:** a smooth horizontally moving ticker, an in-place fade between items, or abrupt in-place replacement. Rates were based on previously selected preferences and **not matched across styles**, so animation form and information timing are not isolated.

### Results

- **Primary completion time:** no detected overall difference, **F(3,1625) = 1.93, p = .12**; mean differences were about **four seconds around a one-minute task**. This is not an equivalence result or proof of no interference.
- **Incorrect answers:** an overall difference, **F(3,1625) = 5.58, p < .01**, with fewer attempts in the no-display control than abrupt replacement (**p = .03**). Control contrasts with fade (**p = .06**) and ticker (**p = .16**) were not significant. Figure 3 places averages around **0.24–0.33 incorrect attempts**; these are approximate graph readings.
- **Back-button selections:** no overall difference, **F(3,1625) = 0.28, p = .84**, approximately **1.5–2** per task.
- **Monitoring latency:** ticker **54.3 s**, fade **35.5 s**, replacement **33.6 s**, overall **F(2,618) = 9.53, p < .01**. Ticker was slower than both other styles: **18.8 s** slower than fade and **20.7 s** slower than replacement, calculated from reported means. The manuscript's “additional 65 percent” cost relative to replacement is approximate; those means imply about **62%**.
- **Basic awareness:** reported **95% confidence intervals** were **88–91% ticker**, **79–83% replacement**, and **74–78% fade**. Ticker also produced more category false alarms than either in-place style; remembering more categories was not uniformly more accurate recognition.
- **Detailed awareness:** ticker outperformed the in-place styles statistically, but the source describes the maximum improvement as **four percentage points**. Figure 6 puts the means at approximately **.67 ticker versus .65 fade/replacement**, not a large comprehension gain. These questions were administered **only after a correct basic-category report**.
- **Opinions:** ticker was preferred for low intrusiveness, ease of awareness, and expected use; replacement was least favored. Preference and measured browsing slowdown were not interchangeable outcomes.

An exploratory “optimal browsing” filter retained **102/1,680 task observations**, produced by **41/70 participants**. Some awareness/false-alarm orderings changed. The authors explicitly reject causal prediction from this selected subset; it does not demonstrate that expert users benefit more.

## Experiment 2: Size and Speed Change the Tradeoff

**Participants and design:** **91 undergraduates**, class credit, eight rounds, within-person fade/ticker comparison and between-person **normal, slow, or small** implementation. Six groups combined implementation with starting style; five had **15 participants**, one **16**. This was **not a full size-by-speed factorial**: smaller-and-slower was not tested. No no-display control was included.

Recall administration changed: **all five awareness questions were asked**, regardless of whether the participant recognized the category. Question and answer wording could therefore cue retrieval. Normal settings also differed from Experiment 1. Cross-experiment comprehension changes cannot cleanly be assigned to animation style or speed alone.

### Results

- **Browsing:** the results section reports **F(5,2906) = 2.21, p = .05**, slower completion with small displays and faster completion with slow rates (**p = .03**); the small-versus-slow ticker contrast was **p = .04**. The prose describes differences of up to **20 seconds within roughly two minutes**. Figure 7 places condition means roughly **103–115 s**; these are approximate readings rather than a precise pairwise effect. Back-button selections and perceived intrusiveness did not distinguish styles; incorrect-answer differences were only marginal.
- **Reaction:** all fade variants yielded shorter latency than all ticker variants, **F(5,1289) = 79.82, p < .01** overall. Normal fade latency was about **one-third** normal ticker latency. Figure 10 shows approximate means **36–46 s for fades**, **94–100 s for normal/slow ticker**, and **67 s for small ticker**. Smaller tickers improved reaction relative to the other tickers, but smaller displays also worsened primary browsing in the reported analysis.
- **Basic awareness:** rates clustered just below **.90**, within roughly **eight percentage points** overall; small tickers exceeded slow tickers. The authors judge many statistically significant awareness and false-alarm differences practically slight.
- **Detailed awareness:** slow fade produced about **.86**, versus about **.68–.71** for the other conditions in Figure 12. The source describes an improvement of about **20 percentage points**, with pairwise comparisons **p < .01**. These are cued multiple-choice results, not uncued long-term memory.
- **Opinions:** unlike Experiment 1, no clear preference differences emerged. Removing replacement changed the comparison frame; this is a proposed explanation, not a measured mechanism.

The authors recommend **slow fade as the best all-around tested option for this browsing task**, not a universally best notification. In-place text supported reaction consistently; the ticker's Experiment 1 comprehension advantage did **not** survive the changed slow-fade and question conditions. This is within-program convergence for reaction, not an independent replication or clean comprehension replication.

## Source Inconsistencies and Analytical Limits

- **Experiment 2 counts and denominators:** eight rounds × four browsing tasks × 91 participants imply **2,912 observations**, but screening says **24 tasks/person**, **2,184 possible**, and **116 excluded**, implying **2,068 retained**. Meanwhile **F(5,2906)** corresponds to 2,912 observations in a conventional six-group analysis, not the stated screened total. The platform section also says “24 or 36” observations although its round description implies **24 or 32**. The manuscript does not reconcile these counts; do not silently select one denominator.
- **Width claim:** the text calls a reduction from **1,180 to 840 px** “more than halved.” Those values imply a reduction of approximately **29%**, not more than 50%; the accompanying **160 to 70 characters** estimate does not reconcile it. These are source discrepancies, not design-size recommendations.
- **Discussion versus results:** Experiment 2's discussion says no browsing-time differences were found, although its results section, Figure 7, and Table 2 report differences between implementations. The abstract/general discussion's “not interruptive” framing also overlooks Experiment 1's incorrect-answer effect and the absence of a no-display control in Experiment 2.
- **Unit of analysis:** analyses use hundreds or thousands of task/choice observations despite participants contributing repeatedly. A participant-level repeated-measures or hierarchical error model is not clearly reported; statistical precision may therefore be overstated. Numerous pairwise comparisons, outcome screening, and exploratory optimal-trial selection further limit inference. Confidence intervals are plotted, but standardized effect sizes and participant-level uncertainty are not supplied.
- **Statistical wording:** nonoverlapping confidence intervals are used to identify differences, while overlapping intervals do not generally establish absence of a significant difference. The reported **z = 3.04, p = .03** pair is also inconsistent with an ordinary two-sided normal z test. Preserve these as reported rather than repairing the analysis.
- **Generalizability:** sessions lasted less than an hour, samples were homogeneous undergraduates, and the task was text browsing. No long-term habituation, demanding safety-critical task, accessibility or motion-sensitivity evaluation, or independent replication of these exact comparisons is established. Related prior work found more disruption with different movement and tasks; smoothness is a proposed explanation, not experimentally isolated here.
- **Redistribution evidence:** this author manuscript supplies no explicit permission to redistribute. Crossref's separate **text/data-mining** licence is not permission to republish this PDF. Retain the raw file privately.

## Analyst Takeaways

1. **Measure interruption, reaction, and comprehension separately.** Good monitoring latency cannot stand in for understood information or acceptable primary-task cost.
2. **Distinguish event signaling from reading moving content.** Motion can attract attention while horizontal text travel slows extraction of a sought fact.
3. **Do not assume smaller is less disruptive.** Less area improved monitoring in some conditions but also increased reported browsing cost.
4. **Treat recall prompts as part of the intervention.** Cued recognition and uncued awareness are not interchangeable evidence.
5. **Keep the recommendation conditional.** Slow in-place replacement with a fade worked well in this particular task; the study does not establish a universal animation prescription or accessibility benefit.

## Vault Ideas Extracted

- [Motion Cues: Attention and Distraction](/vault/motion-cues-attention-and-distraction.md) — Adds measured browsing cost, reaction latency, and comprehension as separate outcomes, with in-place fade/replacement versus moving text.
- [Glanceable Peripheral Displays](/vault/glanceable-peripheral-displays.md) — Adds behavioral evidence that quick extraction, later awareness, and primary-task preservation can trade off with text motion, size, speed, and recall conditions.
