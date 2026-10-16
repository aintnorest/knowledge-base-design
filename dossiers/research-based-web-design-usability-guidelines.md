---
type: Study Note
title: Research-Based Web Design & Usability Guidelines
description: A 2006 synthesis separates the judged importance of 209 web-design guidelines from their research support, but its evidence ratings are contextual expert assessments and many desktop-era prescriptions have aged.
resource: https://www.govinfo.gov/content/pkg/GOVPUB-HE-PURL-LPS73842/pdf/GOVPUB-HE-PURL-LPS73842.pdf
source: https://www.govinfo.gov/content/pkg/GOVPUB-HE-PURL-LPS73842/pdf/GOVPUB-HE-PURL-LPS73842.pdf
tags: [usability-evaluation, design-process, information-architecture, interaction-design, content-design, digital-interfaces]
timestamp: 2026-10-11T23:51:57Z
---

# Research-Based Web Design & Usability Guidelines — Study Notes

**Authors**: U.S. Department of Health and Human Services (HHS), in partnership with the U.S. General Services Administration (GSA); contributions from web designers, usability practitioners, and researchers; forewords by Michael O. Leavitt and Ben Shneiderman.  
**Published**: 2006 revised edition, U.S. Government Printing Office; **209 guidelines**, 18 chapters, xxii preliminary pages and 267 numbered pages; the supplied PDF has 292 pages. The [GovInfo catalog](https://www.govinfo.gov/app/details/GOVPUB-HE-PURL-LPS73842) identifies the publication year as 2006.  
**Status**: Complete official-government edition read, including appendices, bibliography, and indexes; representative rating panels and comparison figures inspected. The official-edition notice, unnumbered PDF page 2, prints only **ISBN-10 0-16-076270-7**; source key **isbn:9780160762703** is its deterministic ISBN-13 conversion, not a printed ISBN-13. This is a historical guidance synthesis, not a modern accessibility standard or an experiment validating all 209 recommendations. The local PDF is approximately **165 MB**, so the source link remains the canonical GovInfo PDF even though the coordinator retains the raw file privately.  

## What It Is

An unusually explicit answer to two different questions: **“How important do professionals judge this issue?”** and **“What kind of evidence supports the recommendation?”** Every guideline receives separate five-level ratings, a short recommendation, explanatory comments, references, and usually a visual example. The result is a map of priorities and uncertainty, not 209 equally proven laws.

The book is particularly concerned with **information-oriented websites**, including public health and government information. Its general applicability statement is English-language sites for adults **18–75**, with warnings that low-literacy audiences and specialized contexts may require different decisions (p. xix). The chapter organization was elicited from designers rather than derived from a cognitive theory. Screenshots illustrate the intended distinction; they are not themselves empirical results.

## Problem and Motivation

Unreferenced guidelines turn one expert's preferences into apparent standards, conceal contradictory results, and fail to distinguish important problems from well-studied ones. HHS wanted designers to make decisions with traceable support and researchers to see where important questions lacked research (pp. xv–xvi). The introduction specifically criticizes guideline collections that fail to disclose whether advice reflects consensus or a **single, unreplicated study**.

Shneiderman's foreword adds an essential boundary: guidelines are **not rigid standards, contractual guarantees, or a comprehensive predictive theory**. They need education, review, a rapid exemption route for justified departures, and continual enhancement. His example of misusing Miller's memory estimate to limit visible links is particularly valuable: a page that can be inspected is not equivalent to a list that must be held in memory (pp. iii–v).

## Principles as Ideas

### Production and review model

The project began in **March 2000**. Its staged process matters because the ratings assess an already selected collection, not all possible design questions (pp. xx–xxii):

1. **Collect widely**: existing guidelines and style guides, published research, research summaries, public usability reports, and in-house test lessons yielded **more than 500** candidate guidelines.
2. **Reconcile internally**: combine duplicates, resolve conflicts, and clarify language; reviewers with design, usability, technical communication, programming, and HCI experience reduced the set to **398**.
3. **Screen by perceived importance**: **16 external reviewers**, half web designers and half usability specialists, judged each guideline's importance to website success. Eliminating low-importance items left **287**.
4. **Construct an evidence scale**: **eight doctoral researchers/practitioners/authors**, all published researchers and experienced peer reviewers, established criteria for evidence strength. This is evidence appraisal by a panel, not a pooled effect-size calculation.
5. **Find examples and organize**: selecting clear graphic examples reduced the set further. **20 web designers** independently grouped and named guidelines through card sorting; analysis informed the chapters. Draft print layouts were usability tested for findability, comprehension, and preference. The methodology dates the first published **187-guideline** set to **2004**.
6. **Revise the edition**: continuing literature searches supported substantial revision of **21 existing guidelines** and addition of **22**. Three independent groups of computer professionals edited the new/revised guidance. **36 web professionals** rated all **209** guidelines in an online importance survey; **13 usability professionals**, familiar with research and with experience conducting studies, rated the new/revised research support. The book reports **Cronbach's alpha = .92** for those evidence ratings, calling it high agreement.

The alpha is a reported reliability statistic, **not proof that recommendations cause better outcomes**, nor a substitute for a reported inter-rater agreement analysis. Evidence ratings for unchanged guidelines were not necessarily freshly reassessed in the revision.

### Two scales, not one quality score

**Relative Importance (I)** is professional judgment about contribution to website success. The revised survey's anchors ran from **“Important” to “Very Important.”** The displayed ratings **1–5** rank the retained recommendations from relatively lower to higher importance; even **1** is still important enough to survive selection. The book does **not** publish distinct verbal meanings or score-to-category conversion thresholds for each of these five displayed levels. Do not invent them, read 1 as “unimportant,” or interpret I=5 as a measured effect size. Guidelines are ordered by importance within chapters, with whole-book rankings in pp. 205–209.

**Strength of Evidence (E)** has explicit level meanings (p. xxii):

| E | Meaning | Evidence criterion |
|---|---|---|
| **5** | Strong research support | Cumulative, compelling research; at least one formal, rigorous study with contextual validity; no known conflicting research findings; expert opinion agrees. |
| **4** | Moderate research support | Cumulative research; conflicting findings may or may not exist; expert opinion tends to agree and consensus appears to be building. |
| **3** | Weak research support | Limited research, possibly conflicting findings, and/or mixed expert agreement. |
| **2** | Strong expert-opinion support | No research-based evidence under the scale; multiple supporting opinions in textbooks/style guides; tends toward professional agreement or accepted practice. |
| **1** | Weak expert-opinion support | No research-based evidence; limited or conflicting expert opinion. |

The small rating panels use **filled red circles containing consecutive numerals**, with empty circles for unused positions. Five filled positions means 5; four filled and one empty means 4. This visual shorthand represents ordinal categories, not uncertainty intervals. The scale's useful distinction is between **research support (3–5)** and **expert opinion without research support (1–2)**, while recognizing that E=3 can be quite inconclusive.

The intended decision model is: use importance to prioritize work, evidence to calibrate confidence, and **high importance with low evidence to prioritize local testing** (p. xviii). A third axis overrides both: **legal obligation**. Accessibility panels explicitly say federal sites must follow Section 508 regardless of the reviewers' importance ratings. Weak experimental support for a requirement is not permission to exclude disabled users.

## Results / Admissions

### Highest importance: the complete I=5 group

The table joins the independent appendix rankings, pp. 205–214. **Only 1:1, Provide Useful Content, is simultaneously I=5 and E=5.** Eleven other highest-importance guidelines have moderate support (E=4); **13 of the 25** have weak research or expert-opinion support (E≤3). These are the book's ratings, not present-day re-ratings.

| Guideline | I | E |
|---|---|---|
| **1:1 Provide Useful Content** | **5** | **5** |
| 1:2 Establish User Requirements | 5 | 4 |
| 1:3 Understand and Meet User's Expectations | 5 | **3** |
| 1:4 Involve Users in Establishing User Requirements | 5 | **3** |
| 2:1 Do Not Display Unsolicited Windows or Graphics | 5 | **3** |
| 3:1 Comply with Section 508 | 5 | **2** |
| 3:2 Design Forms for Users Using Assistive Technologies | 5 | **2** |
| 3:3 Do Not Use Color Alone to Convey Information | 5 | 4 |
| 5:1 Enable Access to the Homepage | 5 | **3** |
| 5:2 Show All Major Options on the Homepage | 5 | **2** |
| 5:3 Create a Positive First Impression of Your Site | 5 | 4 |
| 6:1 Avoid Cluttered Displays | 5 | **3** |
| 6:2 Place Important Items Consistently | 5 | 4 |
| 6:3 Place Important Items at Top Center | 5 | 4 |
| 8:1 Eliminate Horizontal Scrolling | 5 | 4 |
| 9:1 Use Clear Category Labels | 5 | 4 |
| 10:1 Use Meaningful Link Labels | 5 | 4 |
| 13:1 Distinguish Required and Optional Data Entry Fields | 5 | **3** |
| 13:2 Label Pushbuttons Clearly | 5 | **2** |
| 15:1 Make Action Sequences Clear | 5 | 4 |
| 16:1 Organize Information Clearly | 5 | 4 |
| 16:2 Facilitate Scanning | 5 | 4 |
| 16:3 Ensure that Necessary Information Is Displayed | 5 | **2** |
| 17:1 Ensure Usable Search Results | 5 | **3** |
| 17:2 Design Search Engines to Search the Entire Site | 5 | **3** |

For a broader **high-importance** set, the following are all the **I=4/E=5** guidelines: **2:3 Standardize Task Sequences; 2:5 Design for Working Memory Limitations; 6:7 Align Items on a Page; 9:3 Use Descriptive Headings Liberally; 11:1 Use Black Text on Plain, High-Contrast Backgrounds; 12:1 Order Elements to Maximize User Performance; 14:1 Use Simple Background Images; 14:4 Use Video, Animation, and Audio Meaningfully; 15:6 Use Mixed Case with Prose; 16:4 Group Related Elements; 18:1 Use an Iterative Design Approach.** Together with 1:1, these form the strongest-research/high-importance intersection. Strong support still attaches to the stated context, not every possible implementation of the heading.

### Chapter-level decision map

The chapters run from design process through experience, accessibility, technical environment, homepage, layout, navigation, scrolling, labeling, links, typography, lists, controls, media, writing, content organization, search, and testing. The following groups preserve that structure without turning the book into a checklist. Where I=4 recommendations also have weak support, they are identified explicitly; **E=2 means expert-opinion support, E=3 means weak research support**.

#### 1. Design Process and Evaluation — pp. 1–8

Useful content outranks cosmetic polish. Requirements evidence mixes project studies, information exchange, use-case comparisons, and reviews of user involvement. Crucially, **1:4** says user involvement is useful for discovering what a system should do, but evidence is unclear for acceptance and little or absent for increased efficiency/effectiveness; users are not thereby established as good interface designers. Parallel design **(I=2/E=4)** is supported more strongly than personas **(1/2)**. The latter explicitly admits no research clearly showing improved website success despite observational reports.

Additional I=4 weak-support advice: **1:5 Set and State Goals (E=2); 1:6 Focus on Performance Before Preference (3); 1:7 Consider Many User Interface Issues (3)**. Treat the performance-before-aesthetics claim as a priority recommendation, not a finding that aesthetics never influences trust, acceptance, or behavior.

#### 2. Optimizing the User Experience — pp. 9–21

The durable model is allocation of effort: computers do computation and retention; users should receive directly usable information, repeatable task sequences, and feedback during waits. Working-memory guidance **(4/5)** recommends co-visible comparisons and avoiding cross-page retention, citing cognitive research, age comparisons, and number-entry studies rather than imposing a menu-item limit. Credibility advice draws on **two large surveys**, not proof that professional appearance makes information true. Reading-versus-printing guidance rests on a survey; waiting advice combines response-time research and older interface guidance.

I=4/E=3: **2:2 Increase Web Site Credibility; 2:4 Reduce the User's Workload; 2:7 Warn of Time Outs; 2:8 Display Information in a Directly Usable Format; 2:9 Format Information for Reading and Printing; 2:11 Inform Users of Long Download Times**. **2:12 Develop Pages that Will Print Properly is 4/2**. These rationales are often sound, but not equivalent to a quantified causal effect for a current service.

#### 3. Accessibility — pp. 22–28

The chapter chiefly translates the **then-current Section 508 requirements** and **WCAG 1.0 (1999)**, rather than presenting disability-inclusive trials. Its model is equivalent access: usable forms, non-color cues, text alternatives, navigation bypass, perceivable script changes, synchronized media alternatives, and accommodation of assistive technology. **3:4 Skip Repetitive Navigation Links; 3:5 Text Equivalents; 3:6 Accessible Plug-Ins/Applets are all 4/2**. These low evidence labels reflect the book's scale, not diminished obligation or usefulness.

The book's claim that roughly **8%** of users have a disability is drawn from an old web-user survey and is not a defensible present-day population estimate. Its frames, applets, stylesheet independence, separate text-only fallback, and flicker formulations identify an old compliance environment. Use current standards for conformance decisions; retain the principle of equivalent perceivable and operable access.

#### 4. Hardware and Software — pp. 29–33

The reusable idea is to understand the actual access environment instead of designing only for the team's equipment. The evidence is predominantly **market-share/connection statistics plus professional guidance**, not comparative outcome trials. All the I=4 items here are **E=2**: **4:1 Common Browsers; 4:2 Browser Differences; 4:3 Popular Operating Systems; 4:4 Typical Connection Speed**. The named dominant systems and monitor distributions are expressly time-bound.

#### 5. The Homepage — pp. 34–43

The homepage functions as an orientation and recovery point: communicate purpose, reveal the breadth of the site, and make important paths recognizable. Evidence mixes homepage audits, usability observations, and quality-selection studies; the first-impression rationale reports that participants inspected only the homepage about **half the time** when seeking high-quality sites. This measures a selection behavior, not objective site quality. Additional weak-support I=4 advice is **5:4 Communicate Value and Purpose (E=3); 5:5 Limit Homepage Prose (3)**. Homepage primacy is a model for these information sites, not a guarantee that today's visitors arrive there first.

#### 6. Page Layout — pp. 44–57

Layout governs search, comparison, and learned location. Support includes visual-search experiments, eye tracking, location learning, and reading studies. **6:4 Easy Comparison (4/4)** connects layout to memory offloading; **6:7 Alignment (4/5)** and stable placement are more reusable than top-center coordinates. Additional weak I=4 prescriptions are **6:5 Establish Level of Importance (E=3); 6:6 Optimize Display Density (3)**.

The comments do not support “more whitespace is always better”: sparse local groups can make targets easier to find, while other studies associate higher overall density with faster scanning, or find preference changes without performance changes. Fluid-layout guidance **(3/3)** admits **no performance degradation with non-fluid layouts**, despite preferring fluid layouts. Line-length guidance **(2/4)** separates speed from preference and acknowledges different paper findings. These are task/measure tradeoffs, not one universal ideal layout.

#### 7. Navigation — pp. 58–70

Preserve escape routes, distinguish navigation groups, and reveal location. Support ranges from usability reports/style guides to controlled menu comparisons and hypertext-navigation research. Every I=4 guideline in this chapter has weak support: **7:1 Provide Navigational Options (E=2); 7:2 Differentiate and Group Navigation Elements (3); 7:3 Clickable List of Contents on Long Pages (3); 7:4 Location Feedback (2); 7:5 Primary Menus in the Left Panel (3)**.

The left-menu comments themselves report near-equivalent right-menu performance. Breadcrumb guidance **(1/3)** reports usage on only **6%** of occasions versus **32%** potential opportunities, with no task-time/page-count benefit in one study, but faster tasks after instruction in another. That is an adoption-and-learning limitation, not evidence that hierarchical context is useless. Site-map comments likewise admit that maps need not improve mental representations and lose utility when their structure disagrees with users' concepts.

#### 8. Scrolling and Paging — pp. 71–75

Distinguish **reading for comprehension** from **finding a target**, and navigation cost from latency. Evidence includes older paging/scrolling experiments, web-use observations, and age-related performance studies. The book recommends scrolling for uninterrupted reading **(8:3, 2/4)**, yet admits no reliable comprehension difference when pages load quickly and cites benefits for paging's mental representation and later retrieval. Its adjacent fast-response paging recommendation **(8:4, 2/4)** cannot be combined into “never scroll.” Horizontal scrolling **(5/4)** is a separate burden, not evidence against vertical reading flow.

#### 9. Headings, Titles, and Labels — pp. 76–84

Language and visual hierarchy let people infer contents before committing to a path. Evidence includes comprehension/recall/search experiments, technical-communication research, and usability observations; descriptive headings **(4/5)** have stronger support than many individual labeling conventions. Weak-support I=4 items: **9:2 Descriptive Page Titles (E=2); 9:4 Unique and Descriptive Headings (3); 9:5 Highlight Critical Data (3); 9:6 Descriptive Row/Column Headings (3)**. Headers also convey table context to assistive technology, a rationale distinct from whether every stylistic prescription has trial evidence.

#### 10. Links — pp. 85–99

Links require both **destination meaning** and **visible actionability**. Support combines information-scent/protocol analysis, navigation models, web usability tests, and style guidance. Avoid making people sweep a pointer around to discover actions; matching destination headings provides confirmation after selection. Weak I=4 items are **10:2 Related Content Links; 10:4 Avoid Misleading Click Cues; 10:7 Designate Used Links**, each **E=2**. Their comments can cite observations or secondary reports despite this expert-opinion classification—references alone do not mean the panel judged the underlying evidence sufficient.

#### 11. Text Appearance — pp. 100–110

Separate legibility, salience, and preference. The chapter combines print/CRT reading research with screen-font comparisons and search/eye-movement studies. High-contrast plain backgrounds **(4/5)** have strong support in the scale, but the reported **up to 32%** faster reading for black-on-white than light-on-dark is not a universal dark-mode effect size. Familiar-font comments report **no reliable reading-speed/preference difference** among the specified familiar fonts; they do not establish a mandatory serif or sans-serif winner.

Weak I=4 items: **11:2 Format Common Items Consistently (E=2); 11:3 Mixed-Case Prose (3)**. In the bolding comparison **(11:5, 3/3)**, users spent roughly **four times** as long looking at bold field labels as at plain values; bolding the values changed gaze allocation but plain values had better search accuracy. The figure helps explain why emphasis should follow the task, not why all bold text is harmful.

#### 12. Lists — pp. 111–119

Ordering and grouping reduce scanning work. Evidence includes menu/visual-search research, document-comprehension studies, and interface guidance. **12:1 Order Elements to Maximize User Performance (4/5)** is task-relative; alphabetical order is a fallback, not a universal ranking principle. A cited comparison reports horizontal-list scanning takes **20% longer** than vertical scanning, without enough protocol detail here for a general population estimate. Static menus **(3/3)** outperform automatically reordering menus in the cited comparisons; user-controlled adaptation is distinguished from system-controlled movement. Stable locations support learning, but this does not establish that all personalization is harmful.

#### 13. Screen-Based Controls — pp. 120–141

Controls should expose what action will occur, which input is needed, what is optional, and how errors can be detected. Evidence combines older data-entry/widget experiments, usability reports, and design handbooks. Weak I=4 guidance: **13:3 Consistent Field Labels (E=3); 13:4 Case-Insensitive Entered Codes (2, with security exceptions); 13:5 Clear Field Labels (3); 13:6 Minimize Data Entry (3)**.

A key admission is the **speed–accuracy tradeoff**: text entry for dates/reservations **(13:22, 2/5)** was faster and preferred in at least two studies, but produced more errors. Thus strong evidence does not imply that the fastest control is always the correct choice. Automatic focus warns of screen-reader harm; auto-tabbing is explicitly for skilled frequent users. Neither belongs in an indiscriminate form rule.

#### 14. Graphics, Images, and Multimedia — pp. 142–157

Use media to communicate, not merely attract attention. Evidence includes perceptual readability studies, multimedia-learning research, latency experiments, banner-blindness observations, and picture-memory experiments. Weak I=4 items: **14:7 Limit Large Images Above the Fold (E=3); 14:8 Ensure Images Convey Intended Messages (3)**. The reported **75% versus 17%** information-finding success on content/link-rich versus graphic-intensive sites compares whole designs; it does not isolate an image's causal effect.

Picture superiority **(14:15, 1/5)** is strongest for recognition/recall of common objects, with stated exceptions for conceptually similar stimuli and brief presentations. It is not a license to replace informative text with unexplained icons. Photographs-as-trust-builders **(1/2)** explicitly juxtaposes a positive e-commerce result with another study finding no trust/preference effect. Latency comments likewise report one study finding no relationship between slow downloads and abandonment. The source admits conflicting findings more often than its imperative headings suggest.

#### 15. Writing Web Content — pp. 158–168

Make sequences, vocabulary, and sentence structure intelligible to the intended audience. Support combines psycholinguistics, technical-instruction research, readability studies, and web usability reports. Weak I=4 advice: **15:3 Familiar Words (E=3); 15:4 Define Acronyms/Abbreviations (2); 15:5 Use Abbreviations Sparingly (2)**. “Cancer screening” becoming “testing for cancer” illustrates a comprehension mismatch, not a generic ban on domain terminology. Affirmative instructions admit exceptions when preventing a dangerous wrong step is the central need. Scannability and concision are information-access strategies, not grounds for deleting necessary qualifications.

#### 16. Content Organization — pp. 169–178

Organize around user tasks and preserve the information needed at the point of use. Support includes document-design studies, grouping/visual-search research, web observations, and information-display comparisons. **16:4 Group Related Elements (4/5)** connects spatial proximity/common background to conceptual grouping. Additional weak I=4 guidance is **16:5 Minimize Clicks/Pages (E=3)**: it advises common information within two or three clicks, then acknowledges that users were **no more likely to quit after three clicks than after twelve**. This directly rejects a fixed three-click abandonment threshold. Optimize meaningful progress, not an arbitrary click count.

Audience-specific versions can help without forcing people to declare an identity before seeing content. Tables versus graphs depends on whether the task needs exact lookup or rapid pattern recognition; the source's qualified comments are better than treating either format as inherently superior.

#### 17. Search — pp. 179–187

Search should match users' vocabulary, expected scope, and next task. Evidence combines search-interface studies, search logs/surveys, technical reports, and professional guidance. Weak I=4 items: **17:3 Equivalent Upper/Lowercase Terms (E=2); 17:4 Search on Each Page (2); 17:5 Search Around Users' Terms (3)**. Simple search is recommended because advanced syntax is rarely used, not because every specialized collection needs the same search model. Search hints can improve the corresponding semantic or syntactic outcome, while piling multiple hint types together can reduce performance. Search is explicitly **not a substitute for good organization**.

#### 18. Usability Testing — pp. 188–197

Iterate against task success, time, and satisfaction benchmarks; distinguish inspection predictions from observed barriers. The evidence includes before/after redesigns, evaluation-method comparisons, problem-discovery models, and comparative multi-team evaluations. One iterative redesign reports **30% more task completions, 25% less completion time, and 67% greater satisfaction**; another purchasing example rises **22%→88%** success. These are source-reported case outcomes, not the average causal return from iteration.

Inspection caution **(2/4)** reports approximately **1.3 false positives and 0.5 misses per hit**; another study needed **16 evaluators** to uncover **75%** of potential issues and described a problem-detection rate as **“p=.09”**. In that passage, p is described as detection probability, not presented as a significance-test p-value. Evaluator-effect evidence **(2/4)** shows substantially different problem sets even among experienced evaluators; one person is unlikely to find the majority of collectively detected severe problems. Severity judgments also disagree: a cited exercise used **17 teams**, and another comparison reports **22% overestimation / 78% underestimation** relative to test results.

The sampling model distinguishes small early formative sessions (approximately six per markedly different user group) from quantitative comparisons requiring larger samples for stated confidence. It does not promise that five or six people certify usability. Remote/lab and paper/computer comparisons often report no reliable difference, which is narrower than proof of universal equivalence.

## Clearly Dated Guidance

- **Desktop market baseline (4:1–4:5, pp. 29–33)**: Windows XP dominates, Windows 2000/98 remain material, dial-up is a home-access concern, and **56%** of monitors reportedly use **1024×768 in June 2006**. The advice to design for that resolution cannot serve as a present-day viewport model. Devices, browser windows, zoom, touch, and reflow differ from monitor-resolution counts.
- **Frames and applets (3:6, 3:12, 6:13, 7:9)**: persistent access to controls is a durable objective; recommending browser frames as the vehicle is historical. The book itself notes printing/search confusion and difficulty with multiple frames. Its plug-in/applet assumptions and parallel text-only fallback do not describe the modern web's normal interaction architecture.
- **Single-screen home/navigation pages (5:7, 7:8, 8:4–8:5)**: the rationale emphasizes missed below-fold links and slow scrollbar use, especially among novices/older users. Do not generalize it to “users do not scroll,” particularly for touch interfaces. In [Fessenden's 2018 scrolling study](https://www.nngroup.com/articles/scrolling-and-attention/), **120 participants** contributed over **130,000 eye fixations** on **1920×1080** screens across varied website tasks: **57%** of viewing time was above the fold versus **80%** in the earlier 2010 study, and **74%** fell within the first two screenfuls. This later observational comparison supports top-heavy attention while undermining the old fixed one-screen prescription; changed screens and sites prevent a direct controlled replication or a mobile claim.
- **Top-center/left-panel and hover-based models (6:3, 7:5, 7:11, 10:10)**: these findings concern particular desktop layouts, pointer actions, and conventions. Preserve visible hierarchy and discoverability; do not transfer exact coordinates or pointer-hover assumptions to every device, language, or task.
- **Historical latency and printing assumptions (2:9–2:12, 14:3)**: hourglass-based waits, connection-specific download estimates, and print-centric document preferences reflect their environment. Retain feedback and intentional output formats, not period-specific delivery mechanics.
- **Search visibility (1:8)**: being in the external search engine's **“top 30”**, keyword-metatag examples, and registration advice are a period-specific discovery prescription. The durable issue is findability, not that result cutoff or those ranking mechanisms.
- **Typography and accessibility formulations (11:8, 3:13)**: fixed point-size comparisons include Windows/Mac rendering differences, and flicker advice reflects the historical Section 508 formulation. They are not current measurable accessibility conformance rules. Retain readable, adaptable text and seizure-risk avoidance; cite contemporary standards separately.

## Analyst Takeaways

1. **Importance and confidence must remain separate.** The only 5/5 item is useful content. Many apparently obvious high-priority recommendations are opinion-supported or weakly researched; treating the whole collection as “scientifically proven” destroys its main contribution.
2. **A requirement can be justified without a causal usability trial.** Accessibility obligations and equivalent access are not optional because their research score is low. The rating model measures one kind of support, not moral or legal priority.
3. **Extract mechanisms, not coordinates.** Memory offloading, predictable task sequences, clear destination language, meaningful grouping, and iterative task measurement outlive screen resolutions, operating-system shares, and frames.
4. **Read comments against headings.** The scrolling, three-click, fluid-layout, graph/table, photograph/trust, and text-entry examples repeatedly qualify an imperative. Those qualifications contain the actual decision model.
5. **Do not confuse outcome types.** Preference is not speed; speed is not accuracy; visual credibility is not truth; a predicted inspection problem is not an observed user failure. The book's better passages keep these separate.
6. **Use the bibliography as an evidence trail, not an effect-size database.** The book commonly omits original sample sizes, detailed tasks, confidence intervals, and statistical tests. Its percentages describe cited cases with incomplete denominators; none should become a performance guarantee without reading the original study and checking the modern context.

## Questions and Limitations

- This is a broad narrative synthesis and panel appraisal, not a reproducible systematic review. Search strategies, exclusion criteria for studies, study-level risk-of-bias assessments, and the transformation of importance means into five categories are not fully reported. No pooled treatment effect is established.
- E=5 means no conflicting findings **known to this review at the time**, not absence of future counterevidence. Agreement among raters does not resolve publication bias, weak source studies, or transfer from print/CRT and desktop tasks to current interfaces.
- Bibliographic entries include empirical articles, research summaries, books, industry reports, internal technical reports, surveys, standards, and style guides. These support different inferences; a long source list is not a count of independent replications. Original participants/tasks/statistics are often unavailable in the book and are not fabricated here.
- There are real editorial inconsistencies. The introduction/Leavitt foreword places introduction of the original set in **2003**, while the methodology names the first published edition **2004**. The **Strength of Evidence** appendix repeatedly labels its numeric column **“Relative Importance”** even though its ordering and values match evidence ratings; the 1:1/1:2 panels make the intended distinction visible. Mixed-case prose appears twice, **11:3 (4/3)** and **15:6 (4/5)**, with materially different ratings and source lists. Treat these as inconsistencies, not independent confirmation.
- Page 104's figure caption says its plain-text example “proves” easier reading, although the discussion concerns a specific form-field search comparison. Screenshots elsewhere likewise make confident claims without carrying experimental controls. Use figures to interpret the recommendation, not to upgrade its evidence.
- The source does not establish that persona use improves success, that breadcrumbs never help, that all images damage findability, or that modern users should be prevented from scrolling. Its admitted nulls and contextual exceptions are important safeguards against those readings.

### Rights and archival boundary

No explicit **public-domain declaration, copyright license, or blanket redistribution grant** was found in the complete book. Government authorship is not substituted for such a statement. The unnumbered **“U.S. Government Official Edition Notice,” PDF p. 2**, does explicitly restrict seals/logos. The relevant text is reproduced verbatim, joining line-wrapped words:

> The seal and logo of the U.S. Department of Health and Human Services (HHS) and the U.S. General Services Administration (GSA) authenticates the Research-Based Web Design & Usability Guidelines as the official codification of Federal regulations established under the Federal Register Act. The HHS seal and logo displayed in this book are protected under the provisions of 42 U.S.C. 1320b-10. The GSA seal and logo displayed in this book are protected under the provisions of 18 U.S.C 506. The unauthorized use of these seals and logos in a publication is prohibited and subject to a civil penalty of up to $5,000 for each unauthorized copy of it that is reprinted or distributed.
>
> It is prohibited to use the HHS or GSA seal or logo displayed in this book without the express, written permission.

The same notice says:

> The Superintendent of Documents of the U.S. Government Printing Office requests that any reprinted edition clearly be labeled as a copy of the authentic work with a new ISBN.

That reprint-label request is not an explicit unrestricted license. The notice's “codification of Federal regulations” language also sits awkwardly beside the foreword's warning that guidelines are not rigid standards; do not treat the entire book as binding regulation. Independently of rights interpretation, the supplied file exceeds GitHub's **100 MB** per-file limit and is assigned to private archival storage; its dossier therefore links the public GovInfo original.

## Vault Ideas Extracted

- [Working Memory Capacity Limits](/vault/working-memory-capacity-limits.md) — Co-visible comparisons and point-of-use context reduce cross-page retention; the guideline does not justify a fixed limit on visible options.
- [Consistency and Convention](/vault/consistency-and-convention.md) — Repeatable task sequences and learned locations reduce effort, while preference, speed, and error outcomes still need separate assessment.
- [Evaluator Effect](/vault/evaluator-effect.md) — Multiple evaluators find different problem sets; aggregate coverage and inspection false positives limit reliance on a single expert review.
- [Importance Versus Evidence Strength](/vault/importance-versus-evidence-strength.md) — Separate implementation priority, confidence in supporting research, and overriding obligations; high-priority low-evidence questions are candidates for contextual evaluation.
- [System-Changed versus User-Changed Interfaces](/vault/adaptive-versus-adaptable-interfaces.md) — Relates the panel-rated static-menu guideline to control of change and distinguishes disruptive movement from optional adaptive copies; the newer experiments qualify a blanket anti-personalization reading.
