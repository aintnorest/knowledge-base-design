---
type: Study Note
title: How Do Users Evaluate the Credibility of Web Sites? A Study with Over 2,500 Participants
description: In a large live-site comparison study, design look appeared in 46.1% of coded credibility comments, demonstrating reported prominence rather than its causal share of trust or information accuracy.
resource: https://doi.org/10.1145/997078.997097
source: https://doi.org/10.1145/997078.997097
tags: [trust, aesthetics, user-research, digital-interfaces, visual-hierarchy]
timestamp: 2026-10-11T23:53:02Z
---

# How Users Evaluate Web Credibility — Study Notes

**Authors**: B.J. Fogg, Cathy Soohoo, David R. Danielson, Leslie Marable, Julianne Stanford, and Ellen R. Tauber.  
**Published**: ACM DUX 2003, Designing for User Experiences; 15-page proceedings paper, reporting data collected in 2002.  
**Status**: Read the ACM-format DUX paper. It analyzes comments on live-site credibility comparisons, not an experiment independently manipulating visual design.  

## What It Is

A large study of what people **say they noticed** when judging website credibility. **2684 participants** compared two live websites in one category, ranked their credibility, and supplied comments. In the analyzed comment corpus, **46.1%** mentioned **design look**, **28.5%** information design/structure, and **25.1%** information focus.

The paper's most reusable contribution is not “46% of trust comes from design.” It is the distinction between **a signal becoming noticeable** and **the interpretation attached to that signal**, together with an empirical inventory of reported cues in one evaluation setting.

## Problem and Motivation

Prior credibility research often presented participants with a specific feature—a privacy policy, banner ad, or professional-looking design—and asked how it affected credibility. That establishes interpretation *conditional on noticing*. It does not show whether anyone encounters or notices the feature on a real site.

A positive evaluation of a privacy policy is of little practical value if the policy goes unnoticed. Conversely, visual polish may repeatedly enter the assessment because it is immediately available, even when people say substantive evidence ought to matter more.

## Mechanism as an Idea

**Prominence–Interpretation theory** proposes two necessary components:

- **Prominence**: the observer notices something.
- **Interpretation**: the observer judges what that observation implies.

The paper summarizes this as **“Prominence X Interpretation = Credibility Impact”**. This is a conceptual dependency, not a fitted quantitative equation with estimated coefficients. Credibility assessment can cycle through multiple noticed and interpreted elements until the person is satisfied or constrained by time.

The paper positions its comment analysis primarily as a study of prominence, complementing earlier interpretation studies. Comments actually mix both—for example, “professional looking” names a visual cue and expresses its favorable interpretation. A comment is an imperfect trace of noticing, not a complete record of the mental process.

The proposed explanation for visual dominance draws on the **Elaboration Likelihood Model**: participants without a personal stake may rely on peripheral appearance cues rather than scrutinize content. The study did not manipulate involvement or establish that this mechanism caused the results.

## Results / Admissions

### Participants, Stimuli, and Task

Recruitment began in **May 2002**, and data were collected over **60 days**. Nonprofit groups invited supporters; each completion earned a **$5 donation** for the group. Pilot design and refinement had involved **over 200 people across six months**. The authors explicitly acknowledge that the final recruitment method was not a representative sampling scheme.

**2684 people completed the study**. Demographics were optional and supplied by **60.1%**: among those reporting, **58.1% female**, **41.9% male**, mean age **39.9**, and mean web use **19.6 hours/week**. Respondents came from **47 states plus Washington, DC**, predominantly the US, with participants from **29 other countries**. Those percentages describe the demographic subset, not necessarily all completions.

The researchers selected **100 live sites**, **ten in each of ten consumer-oriented categories**: e-commerce, entertainment, finance, health, news, nonprofit, opinion/review, sports, travel, and web search. Participants were randomly assigned a category and given two sites to review, rank, and comment on. **No fixed exposure time is reported**. Figures 1–2 show WebMD and E*Trade as examples, not the two alternatives in a controlled comparison; their visual differences are descriptive context, not experimental treatments.

### Comment Coding and Findings

The researchers removed evidence of repeated sessions and tampering with randomization. **Two independent coders** assigned categories, with a **third resolving disagreements**. A comment could receive **multiple codes**; positive and negative mentions both counted. The paper gives **2440 comments** as the denominator in its example: information bias appeared in **283**, or **11.6%**. It does not clearly reconcile that denominator with 2684 completions and two site-comment prompts per participant, so the totals should not be treated as interchangeable.

| Comment topic | Incidence |
|---|---:|
| Design look | **46.1%** |
| Information design/structure | **28.5%** |
| Information focus | **25.1%** |
| Company motive | **15.5%** |
| Usefulness of information | **14.8%** |
| Accuracy of information | **14.3%** |
| Name recognition/reputation | **14.1%** |
| Advertising | **13.8%** |
| Information bias | **11.6%** |
| Writing tone | **9.0%** |
| Site-sponsor identity | **8.8%** |
| Functionality | **8.6%** |
| Customer service | **6.4%** |
| Past experience | **4.6%** |
| Information clarity | **3.7%** |
| Performance on a self-devised test | **3.6%** |
| Readability | **3.6%** |
| Affiliations | **3.4%** |

Categories below **3%** were omitted from the paper. Because coding overlaps, the table is neither an allocation of 100% of attention nor a partition of trust's causes. No experimental effect size, correlation with rank, confidence interval, or chance-corrected coder agreement is reported for these frequencies.

“Design look” combines **layout, typography, white space, images, color schemes, and overall professional appearance**. Examples include praise for a professional-looking site and criticism of sloppy, childish, or hastily assembled graphics. Thus **46.1% is a broad-category mention rate**, not the percentage of people deceived by beauty, the share of credibility explained by aesthetics, or the effect of redesigning a particular site.

Substantive signals were also prominent. Information focus could favor either broad coverage or a targeted scope depending on the situation. Advertising was usually criticized, but restrained use was sometimes positively interpreted. Reputation and familiarity often helped, while poor past experiences could hurt. These are interpreted signals, not invariant feature rankings.

### Context Changes Which Cues Surface

The category comparisons are descriptive and not accompanied by inferential tests:

- E-commerce: reputation **25.9%** versus **14.1%** overall; customer service **16.7%** versus **6.4%**.
- News: information bias **30.2%** versus **11.6%** overall.
- Nonprofits: sponsor identity **28.9%** versus **8.8%**; information structure **18.2%** versus **28.5%**.
- Opinion/review: bias **23.8%** versus **11.6%**; accuracy **25.4%** versus **14.3%**.
- Travel: customer service **18.1%** versus **6.4%**.
- Search: information design **42.6%** versus **28.5%**, functionality **20.5%** versus **8.6%**, advertising **24.6%** versus **13.8%**, and self-devised tests **13.8%** versus **3.6%**.

The same credibility feature can therefore have different opportunities to matter across tasks and domains.

## Principles as Ideas

The source recommends investing in visual design; recognizing that content accuracy and reputation may lie outside the interface designer's control; using research to influence those stakeholders; choosing which credibility-relevant elements become prominent; asking users explicitly about credibility; and reading studies through the prominence/interpretation distinction.

The strongest rationale is **visibility of relevant evidence**, not making every assurance salient. Not everything can stand out at once, and professional styling should help people inspect accurate information and accountable authorship rather than replace them. The recommendations extend beyond what frequency coding directly proves; this study does not estimate the credibility improvement from implementing any one recommendation.

## Analyst Takeaways

1. **Comments are evidence of reported reasons, not causal weights.** The headline percentage tells us visual appearance is hard to ignore in this context, not how much credibility a polished redesign will buy.
2. **Make warranted trust assessable.** Surface authorship, evidence, relevant affiliations, or accountability where they can be noticed and understood; favorable interpretation without exposure cannot help.
3. **Evaluate perception and truth separately.** A credible-looking site can contain inaccurate information. Measure trust calibration, not merely success at increasing perceived trust.
4. **Match the cue to the domain and the user's stakes.** A searcher's functional test, a news reader's bias concern, and a nonprofit visitor's identity check should not be collapsed into a universal credibility checklist.

## Questions and Limitations

- Participants evaluated unfamiliar assigned comparisons to earn a charitable donation, not necessarily to solve a personally consequential problem. The authors themselves expect greater involvement could reduce appearance's relative prominence; that remains a proposed follow-up, not a measured moderation effect.
- Retrospective comments omit unarticulated or forgotten cues and can rationalize an existing judgment. Not mentioning a privacy policy does not prove it was never noticed or had zero influence.
- “Design look” is broader than many competing categories; the authors acknowledge its breadth inflates its comparative frequency and may conceal finer distinctions.
- The denominator, cleaned completion count, missing-comment handling, and coder reliability are insufficiently specified for reconstructing uncertainty or independently auditing rates.
- The study captures **2002 websites and users**; changes in advertising, phishing, conventions, mobile use, and contemporary authenticity cues limit use of its exact rates today.
- Statements that design has a “significant impact” should not be mistaken for a reported causal significance test in this study. This is an exploratory content analysis; its value is a model and an inventory, not experimentally demonstrated visual persuasion.
- **Redistribution**: the first-page notice reads: “Permission to make digital or hard copies of all or part of this work for personal or classroom use is granted without fee provided that copies are not made or distributed for profit or commercial advantage and that copies bear this notice and the full citation on the first page. To copy otherwise, or republish, to post on servers or to redistribute to lists, requires prior specific permission and/or a fee. Copyright 2003, ACM.” The copyright line also reads “©2003 ACM 1-58113-728-1 03/0006 5.00”. This does not grant public redistribution; `source` uses the canonical DOI URL.

## Vault Ideas Extracted

- [Visual Design and Credibility](/vault/visual-design-and-credibility.md) — Broad design-look mentions dominate a large live-site credibility comment study, with explicit limits on causal interpretation; Prominence-Interpretation theory separates noticing a credibility signal from evaluating what it implies.
