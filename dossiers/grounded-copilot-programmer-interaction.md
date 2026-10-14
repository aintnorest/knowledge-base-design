---
type: Study Note
title: "Grounded Copilot: How Programmers Interact with Code-Generating Models"
description: Observation of 20 programmers and five livestreams supports acceleration and exploration as distinct assistance modes with different validation needs, without causally establishing productivity or the effectiveness of proposed mode-adaptive designs.
resource: https://doi.org/10.1145/3586030
source: /archive/grounded-copilot-programmer-interaction.pdf
tags: [delegation, interaction-design, user-research, cognitive-load, trust, digital-interfaces]
timestamp: 2026-10-14T21:31:31Z
---

# Grounded Copilot — Study Notes

**Authors**: Shraddha Barke, Michael B. James, and Nadia Polikarpova; UC San Diego; first two authors contributed equally.  
**Published**: Proceedings of the ACM on Programming Languages **7, OOPSLA1, Article 78, April 2023, 27 pages**; received October 28, 2022, accepted February 25, 2023.  
**Status**: Peer-reviewed grounded-theory observational research; read the complete publication-layout PDF, including both participant/task tables, seven figures, limitations, and references; DOI and CC BY 4.0 notice are printed in the file.

## What It Is

A model of two purposes for code-generating assistance: **acceleration**, when a person knows what to do and wants help expressing it, and **exploration**, when they need help deciding what to do. These are fluid interaction modes, not fixed classes of programmer. They explain why the same suggestion can be helpful in one moment and disruptive in another.

## Problem and Motivation

Correct code-generation benchmarks do not explain how programmers formulate intent, assess suggestions, repair errors, or maintain flow. A tool that generates more code may increase the work of understanding it. The authors build an explanatory theory from observed interactions rather than conduct a tool-versus-no-tool productivity experiment.

## Research Design

**20 participants**, recruited through personal contacts, Twitter, and Reddit, included **15 from academia and five from industry**; **nine** had prior Copilot experience and **11** had not used it. Participants were not paid; people without access received technical-preview access for continued use. Target-language experience was self-rated as occasional, regular, or professional; people with no experience were screened out.

Sessions lasted roughly an hour, including training, **20–40 minutes** of core task work with think-aloud, and a semi-structured interview. Copilot use was encouraged, not required. Tasks spanned **Python, Rust, Haskell, and Java**:

- Chat server business logic and chat client networking in supplied codebases, including an intentionally unfamiliar custom cryptographic interface.
- A two-part Benford's Law task combining a familiar sequence generator with unfamiliar plotting work, allowing within-person language comparisons.
- A precise string-processing Advent of Code task with test input and separable subtasks, added to investigate validation.

The first two authors initially coded together, then one coded later recordings with discussion by both. Open, axial, and selective coding interleaved with recruitment and task changes: an emerging distinction appeared after participant eight; later tasks probed it; the authors report theoretical saturation at participant **20**. A closed codebook subsequently recoded all videos for descriptive timing analysis.

**Five external livestreams** from YouTube/Twitch, coded by one author, added qualitative corroboration across functional, competitive, and web programming. This is same-study triangulation in a different setting, not an independent preregistered replication or randomized mode comparison. No inferential tests or standardized causal effect sizes are reported.

## The Interaction Model

### Acceleration: assistance fits a known next step

When people can decompose a task into understood microtasks, suggestions act like intelligent completion. They want the next **logical unit**, whose size varies by language and goal, not necessarily a fixed line count. They often triage suggestions through expected keywords, calls, and control structures: **pattern matching** against an existing mental solution.

Long unexpected suggestions interrupt this flow. A participant rejected a **16-line** suggestion after about **four seconds**; others felt compelled to examine material they had not asked for. Three participants who had previously disabled the assistant cited distraction. These are observed episodes and self-reports, not estimates of a universally harmful snippet length.

Almost-correct output is accepted when repair is obvious; otherwise rejection is cheap and common. Assistance can also expose an unanticipated edge case. Matching expectations makes triage fast but does not establish that every accepted suggestion is semantically correct.

### Exploration: assistance helps define the next step

Unfamiliar problems, interfaces, or unexpected behavior lead people to externalize intent, request alternatives, and use generated code as a starting point. Exploration involves more explicit prompting and more substantial editing, including retaining control structure while discarding implementation details.

People examine code, execute examples, consult documentation, or rely on static analysis. More elaborate scrutiny does not ensure deep understanding: one participant distinguished being able to use an unfamiliar interface effectively from understanding it better. Another could not locate a subtle generated file-access error and tried an unrelated repair. Generated authorship can make later debugging harder.

Trust and enthusiasm encourage exploration but can also discourage independent decomposition. Participants sometimes inferred reliability from **repeated patterns across multiple suggestions** or assumed the first suggestion was ranked closest to their intent. The paper interprets these as confidence and anchoring cues, not calibrated uncertainty or experimentally established bias magnitudes.

### Alternative presentation has its own cost

Multiple options help users forage, combine fragments, and learn possible approaches, but detached presentation can make contextual relationships harder to reconstruct. Several participants wanted meaningful differences highlighted rather than many superficially similar snippets. The model is not “always show more choices”: support comparison when exploration is wanted and avoid imposing it during acceleration.

## Descriptive Results and Figures

- Total coded assistant interaction time was **248.6 minutes in exploration versus 104.7 in acceleration**, about **2.37 times** as much. This is pooled mode time, not a productivity difference or a population prevalence estimate.
- Professional language users and prior Copilot users spent more time accelerating than less-experienced groups. Figure 4's expertise categories total **22 observations** (occasional n=9, regular n=2, professional n=11), while prior-use groups total **20 people** (9/11); multi-language participants can contribute multiple language observations, so the denominators should not be conflated.
- Chat Client (**n=4**) and Benford's Law (**n=4**) favored exploration, whereas Chat Server (**n=5**) favored acceleration; Advent of Code (**n=7**) varied. One participant who solved its algorithm early spent **15.8 minutes accelerating and 3.4 exploring**. Tasks, familiarity, and participant composition were not independently randomized.
- In acceleration, code prompting comprised **71.4%** and context prompting **15.2%**; explicit comment prompting was **13.1%**, compared with **57.2% in exploration**. Figure 6 defines these as **shares of prompting time**, although surrounding prose calls them percentages of invocations; they should not be asserted as prompt-count frequencies.
- Figure 7 shows exploration devoting a larger share of validation to examination and documentation; execution takes a larger relative share in acceleration. Static-analysis time was **not quantified**, because background checking made use hard to identify. A larger relative execution share does not mean greater total scrutiny.
- Visual-output Benford's Law attracted more execution than the test-provided Advent of Code task; the authors conjecture that easy, interesting visual feedback motivated checking. This mechanism was not manipulated.
- Livestreams reproduced small logical units, unwanted long suggestions, deliberate exploration, repair, and validation. They also exposed an alternative interaction feature absent from the researchers' and participants' initial knowledge, illustrating incomplete coverage of the tool's available behaviors.

## Recommendations and Their Evidential Status

The authors propose matching suggestion scope and timing to current interaction intent; clearer control over context; legible differences between alternatives; incomplete structures that leave decisions to the person; and lower-friction continuous validation. These recommendations follow the observations but **were not implemented or experimentally tested here**. The analogy to fast/slow cognitive systems is an interpretation, not a physiological or causal measurement of dual-process cognition.

## Analyst Takeaways

1. **Infer the person's purpose, not just tool availability.** Executing a known plan and searching for a plan demand different kinds of initiative.
2. **Match assistance to a logical unit of attention.** Too much unsolicited material can turn expression into review even when generation is accurate.
3. **Separate accepting, comprehending, and verifying.** Pattern recognition, repeated alternatives, or type-check success each supplies partial evidence, not guaranteed functional correctness.
4. **Make alternatives meaningfully comparable.** The value lies in distinctions people can use, not sheer output count.
5. **Retain the source's observational scope.** “Acceleration” names a purpose and interaction pattern; this study does not measure a causal speedup over unaided programming.

## Questions and Limitations

- Small, academia-heavy convenience sample; short researcher-designed tasks and unfamiliar codebases; no longitudinal maintenance, security, or routine team-review evaluation.
- Sparse Haskell and Java observations cannot establish language-general differences; absence of noticeable Python/Rust differences is not statistical equivalence.
- Mode categories and quantitative analyses come from the same developing theory and dataset; saturation is an analytic judgment, not an independent validation criterion.
- **Internal inconsistency**: related work says only **one** participant was an undergraduate, but Table 1 lists **two (P9 and P10)**. Related work broadly says their participants did not share difficulty understanding/modifying generated code, despite explicit debugging/understanding difficulties reported in Section 4.2.6.
- Figure 6's time-based denominator conflicts with prose describing invocation frequency; preserve the plotted measure. Figure 4's language-observation counts exceed participant N and should not be reused as 22 distinct people.
- Suggestions and interface were from an early technical-preview era; the theory may travel better than individual feature complaints. No effectiveness evidence is provided for a mode-detection or adaptation intervention.
- **Redistribution evidence**: page 1 explicitly states **“This work is licensed under a Creative Commons Attribution 4.0 International License.”** Copyright remains with the owner/authors; public archival redistribution is permitted under that grant.

## Vault Ideas Extracted

- [Mixed-Initiative Interaction](/vault/mixed-initiative-interaction.md) — Adds observed acceleration/exploration modes showing when small completions preserve intent and when deliberately requested alternatives support planning, without proving a mode-adaptive intervention.
- [Appropriate Reliance on Automation](/vault/appropriate-reliance-on-automation.md) — Documents pattern-based validation, misleading repetition and ranking cues, explicit cross-checking, and generated-code debugging difficulties across 20 observed programmers.
- [Change Review Effectiveness](/vault/change-review-effectiveness.md) — Distinguishes rapid shape checking from comprehension-oriented examination and shows why unfamiliar generated authorship and detached alternatives increase review demands.
