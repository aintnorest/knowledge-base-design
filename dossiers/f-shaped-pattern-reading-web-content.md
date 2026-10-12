---
type: Study Note
title: "F-Shaped Pattern of Reading on the Web: Misunderstood, But Still Relevant (Even on Mobile)"
description: NN/g observes top-heavy and reading-start-edge-heavy scanning again on desktop and mobile, but the F-shape is conditional and the public report does not quantify its prevalence or the efficacy of proposed antidotes.
resource: https://www.nngroup.com/articles/f-shaped-pattern-reading-web-content/
source: https://www.nngroup.com/articles/f-shaped-pattern-reading-web-content/
tags: [attention, content-design, visual-hierarchy, digital-interfaces, user-research]
timestamp: 2026-10-11T23:50:37Z
---

# F-Shaped Pattern of Reading on the Web — Study Notes

**Authors**: Kara Pernice; Nielsen Norman Group (NN/g).  
**Published**: November 12, 2017; the supplied saved page additionally states “Last reviewed Aug. 19, 2026.”  
**Status**: First-party industry eye-tracking research summary and guidance, not a peer-reviewed paper. Read the supplied article, three figure images, and preview grids of its three linked gaze-replay videos; consulted the linked original 2006 research report for its sample and scope. The review date does not establish a new 2026 participant study.  

## What It Is

A clarification of an influential visual-search observation: readers sometimes concentrate attention near the top and reading-start edge of a text column, making an approximate **F**, but this is neither a universal reading law nor a layout template. The source argues that useful hierarchy and formatting can replace this low-guidance scan with more meaningful selection.

## Problem and Motivation

The original result is often interpreted as “people always read in an F, so arrange everything accordingly.” Pernice instead describes F-scanning as an economical response to insufficiently structured prose and limited commitment. The designer's opportunity is to make important information easier to select, not to exploit arbitrary line beginnings.

## Mechanism as an Idea

The approximate shape comprises an initial horizontal pass across upper content, a lower and usually shorter horizontal pass, and a vertical scan down the content's reading-start side. Some examples resemble an **E** or an inverted **L**. In left-to-right text, early words and early lines receive more attention; in right-to-left text, the pattern can mirror.

**The relevant edge is the text column's edge**, not necessarily the browser's left border or a navigation rail. The article distinguishes assessing content from inspecting navigation to choose a destination. Responsive reflow changes which words occupy privileged locations, so a spatial scan does not reliably select the same meaning across viewports.

NN/g says F-scanning emerges when three conditions coincide: **little web-oriented formatting**, a reader seeking efficiency, and insufficient interest to read every word. Its proposed mechanism is effort economization: without strong cues, people retain attention near the place they begin reading. That is an explanatory interpretation of gaze behavior, not a directly tested mediation model.

Other patterns named by the source are:

- **Layer-cake**: scan headings and subheadings while skipping much of the ordinary text; heatmaps form horizontal bands.
- **Spotted**: skip large text regions while seeking distinctive items such as links, numbers, words, addresses, or signatures.
- **Marking**: keep the eyes near one location while the page scrolls; NN/g says this happens more on mobile, without reporting a frequency comparison here.
- **Bypassing**: skip repeated opening words across successive list entries.
- **Commitment**: inspect nearly all the text when sufficiently interested or motivated.

These are alternative behaviors conditioned by goals and presentation, not fixed reader personality types.

## Results / Admissions

**Original 2006 report**: Jakob Nielsen's [April 16, 2006 article](https://www.nngroup.com/articles/f-shaped-pattern-reading-web-content-discovered/) reports **232 users looking at thousands of webpages**, with a roughly F-shaped dominant pattern across different sites and tasks. Its examples include a corporate about-us article, ecommerce product page, and search-results page. The original already admits departures: product imagery moves the lower crossbar, price and cart controls attract attention elsewhere, and a search result with a longer second headline makes the second bar longer than the first. “Dominant” is a characterization, not a published prevalence estimate.

**2017 revisit**: Pernice reports finding the pattern again on desktop and mobile and a flipped pattern in Arabic. The old Galveston heatmap aggregates **more than 45 people** learning what happened there in 1900. The newer Tigers in Crisis heatmap aggregates **47 people** looking for the number of Sumatran tigers in the wild; attention is concentrated in upper body text and toward its left edge, rather than the advertising rails. These are figure-specific samples, not the total sample of either research program.

The History.com figure is **one participant's ordered gaze plot**, showing dense early-paragraph and list fixations amid relatively unformatted prose. Unlike an aggregate heatmap, it displays temporal sequence and individual variation. Mobile replays illustrate a portrait-camera-lens information task and a Baryshnikov education task; the latter requires horizontal swiping because the text column exceeds the screen width. The Arabic desktop replay illustrates the mirrored reading direction. These examples establish that the reported behavior can occur, not its frequency in a population.

NN/g recommends prioritizing key information early, using informative front-loaded headings, emphasizing meaningful phrases, grouping related content, providing informative link labels and lists, and cutting unnecessary prose. The rationale is to substitute **semantic selection cues** for accidental line position. The article does not report a controlled comparison quantifying how much any particular antidote reduces F-scanning or improves comprehension.

## Analyst Takeaways

1. **Treat F-scanning as a diagnostic, not a design target.** Strong top/edge concentration may indicate people lack better cues. Help them identify meaningful sections rather than force the main message into an F-shaped composition.
2. **Front-load meaning, not generic introductions.** Early information and informative heading openings retain value even when only part of a line receives attention; this is a recommendation motivated by gaze findings, not a guaranteed comprehension effect.
3. **Optimize for multiple scanning strategies.** Clear hierarchy supports layer-cake scanning; distinctive labels support spotted search; high-stakes, high-interest content may elicit commitment. One geometry cannot stand in for all these tasks.
4. **Separate attention from understanding and harm.** Missing fixations on text indicates limited overt inspection, not necessarily a wrong answer, lost sale, or absence of peripheral perception. NN/g's “bad for users and businesses” claim supplies a plausible risk argument, not measured business losses.

## Questions and Limitations

- The public 2017 article does not disclose the full new-study sample, recruitment, demographics, total pages or tasks, equipment and calibration protocol, fixation thresholds, coding criteria, or pattern frequencies by device and language. Neither public article supplies inferential tests, confidence intervals, comprehension outcomes, or a controlled formatting intervention.
- The 2017 recurrence is **within NN/g's own research program**, not an independent replication. The 232-user figure belongs to the original 2006 study and must not be assigned to the mobile/Arabic revisit.
- Aggregate heatmaps can resemble a simple shape while pooling distinct individual paths. The individual gaze plot and replay examples do not establish that every reader follows the aggregate contour.
- The prose sometimes slides from conditional statements about unformatted, low-commitment reading to categorical claims that unformatted text will produce an F and that it is dominant web behavior. Those stronger formulations are not accompanied by prevalence or causal estimates. Conversely, “bad” for a single page can be efficient for users allocating effort across many sites; the article explicitly acknowledges this cost–benefit distinction.
- The saved page footer states **“Copyright © 1998–2026 Nielsen Norman Group, All Rights Reserved.”** NN/g's [copyright policy](https://www.nngroup.com/copyright-and-reprint-info/) prohibits unlicensed online reproduction, including a public digital archive; limited physical-reprint permission does not change that. The dossier uses the canonical URL.

## Vault Ideas Extracted

- [Web Content Scanning Patterns](/vault/web-content-scanning-patterns.md) — Supplies conditional F-scanning, alternative patterns, directionality and reflow limits, plus first-party recurrence evidence with explicit sample boundaries.
