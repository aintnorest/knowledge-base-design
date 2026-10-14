---
type: Study Note
title: Expectations, Outcomes, and Challenges of Modern Code Review
description: Microsoft's field observations, surveys, and comment coding identify understanding as a review bottleneck and benefits beyond defects, but comment frequencies cannot measure defect-detection effectiveness.
resource: https://doi.org/10.1109/icse.2013.6606617
source: https://doi.org/10.1109/icse.2013.6606617
tags: [design-process, user-research, digital-interfaces, case-study]
timestamp: 2026-10-14T21:31:18Z
---

# Expectations, Outcomes, and Challenges of Modern Code Review — Study Notes

**Authors**: Alberto Bacchelli and Christian Bird.  
**Published**: ICSE 2013, pp. 712–721; DOI **10.1109/icse.2013.6606617**, confirmed in Crossref's record, whose registered spelling is lowercase.  
**Status**: Peer-reviewed exploratory mixed-method field study at Microsoft. Read the complete supplied 10-page manuscript, including all five figures and references; the copy lacks publication-layout copyright/DOI information and has older draft metadata, so its exact revision relative to the version of record is unconfirmed.  

## What It Is

An account of what programmers and managers expect from lightweight tool-mediated code review, what appears in review discussions, and what prevents deeper evaluation. The core model is **review as understanding**: to judge a change, reviewers need its purpose, constraints, surrounding behavior, and likely effects, not only a highlighted difference.

The evidence also separates defect finding from code improvement, alternative solutions, knowledge transfer, awareness, and shared ownership. A review can be valuable without finding a bug; conversely, approval does not demonstrate that subtle bugs were checked successfully.

## Study Design

- An earlier external-vendor study, **April–May 2012**, interviewed **23 people for 30–50 minutes** about review practices. Analysis of their expectations informed the new interview guide.
- The authors observed and interviewed **17 practitioners across 16 product teams**, drawn from **100 randomly contacted candidates** with **50–250 signed-off reviews**. Roles were five developers, four senior developers, six testers, one senior tester, and one architect. Microsoft tenure ranged from **18 months to almost ten years**, median **five years**. Meetings lasted **40–60 minutes**, combining a current assigned review with a semi-structured interview; observations became shorter after the first five or six as themes repeated.
- Open coding/card sorting covered **1,047 coherent interview units**. Separately, **200 randomly sampled discussion threads with at least two comments**, totaling **570 comments**, were classified with thread context. This excludes single-comment threads and does not sample every review outcome equivalently.
- A **six-question manager survey** reached **165 of 600 managers (28%)**; an **18-question programmer survey** reached **873 of 2,000 developers (44%)**. Active-review eligibility used **January–June 2012**; respondents had averaged at least one signed-off review per week. Manager motivations were open responses; developer motivations used a supplied list and ranked top three, so response percentages across the two are not identical measures.
- Measures are stated motivations, comment categories, reported understanding needs, and qualitative accounts of work. No manipulated review condition, seeded-error task, defect baseline, causal effect size, or measured long-term learning gain is reported.

## Results / Admissions

### Defect finding leads expectations, not discussion frequency

**383 programmers (44%)** ranked defect finding first, **204 (23%)** second, and **96 (11%)** third. **44% of managers** also gave it as their top reason. Code improvement was first for **337 programmers (39%)**, second for **208 (24%)**, and third for **135 (15%)**; **51 managers (31%)** gave it first.

Alternative solutions were ranked first/second/third by **147 / 202 / 152 programmers (17/23/17%)**, while only **four managers (2%)** mentioned the topic in open responses. This suggests a perspective difference but also a question-format difference. Knowledge transfer was first/second/third for **73 / 119 / 141 programmers**, and team awareness for **75 / 108 / 149**. Figure 3 orders motivations by a **3/2/1 weighted rank score**, not simply the number choosing each first.

Among the **570 coded comments**:

- **165 (29%)** concern code improvement: **58** better practices, **55** removing unnecessary/unused code, **52** readability.
- **78 (14%)** concern defects, the fourth-largest category after code improvement, understanding, and social communication.
- Defect subcounts are printed as **65 logical, six high-level, five security, and three exception-handling issues**, which sum to **79**, not 78.
- **12** explicitly direct someone to resources for learning. This small count is not the rate of knowledge transfer, which often leaves no explicit trace.

Most defect remarks concern local logical issues; interviews describe superficial formatting feedback sometimes substituting for deeper inspection. The authors interpret this as an expectation–outcome mismatch partly caused by understanding difficulty. However, **14% of comments is not a 14% defect-detection rate**: the study does not establish how many defects were available, missed, caught without comment, or resolved elsewhere.

### Understanding constrains the depth of review

Figure 5's four-category understanding ratings place **defect finding and alternative solutions** above the other review purposes in required understanding. No precise numerical effect or inferential test is supplied. Interviews emphasize what instigated the change and why, not merely what text differs.

**798 respondents (91%)** said unfamiliar files take longer to review. **716 (82%)** reported that familiar reviewers give different feedback, described as deeper, more conceptual, more actionable, and more likely to identify subtle defects. These are participant reports, not independently timed or scored randomized comparisons. Reviewers often need to read substantially more surrounding code than the small changed section.

Observations distinguish reviewers who begin with a description from familiar owners who go straight to known files. A useful description explains **what changed and why**; a nominal description can be misleading if the submitted change does more than it claims. Reviewers seek missing context through descriptions, execution, email, and in-person conversation. The paper reports in-person discussion “from **20% to 40% of the times**” from interviews, without a clear measured denominator; this is not a logged population frequency.

### Review supports a team, not only a patch

All but one interviewee spontaneously discussed learning. Interviewees described bidirectional education, making colleagues aware of new functionality, distributing expertise, and reducing territorial attitudes toward code. The authors explicitly acknowledge these benefits are hard to establish from recorded discussions and are supported mainly by responses rather than hard outcome evidence.

Their recommendations are to broaden shared understanding, include knowledgeable reviewers when seeking defects, supply context and direction, support richer synchronous communication when needed, and automate routine low-level checks so people can attend to deeper concerns. These are implications derived from field evidence, not tested intervention packages.

## Analyst Takeaways

1. **Design review around the understanding task.** A diff is a starting point, not the complete evidence needed to judge system consequences.
2. **Agree on the purpose before evaluating success.** Defect finding, maintainability, learning, and awareness require different measures and amounts of context.
3. **Do not infer absence of value from absence of comments.** Social and educational outcomes may leave little trace; comments also do not directly count missed defects.
4. **Preserve an independent path to context.** A change author's explanation can help but may be incomplete or misleading. Extending this to agent-authored changes is a plausible application, not a tested result here.

## Questions and Limitations

- Single-company/tool setting and active-reviewer recruitment limit generalization to newcomers, small projects, open source, and different ownership cultures. Observation can alter behavior; qualitative coding and interview interpretation remain researcher-dependent.
- Threads with at least two comments overrepresent discussion relative to silent approvals and single decisive suggestions. Off-tool conversation, knowledge gains, and review-driven author preparation are incompletely captured.
- No independent replication is established in this paper. Triangulation across methods strengthens the descriptive account but does not turn familiarity or understanding into a randomized causal effect.
- **Internal inconsistencies**: defect subcategories total **79**, versus the reported category total **78**. The discussion calls defect comments “one-eighth” of the sample, while **78/570 ≈ 13.7%** (the earlier 14% is consistent). The summary says it discussed five prominent motivations although the section contains six named motivation subsections. These do not warrant silently correcting the source.
- **Redistribution evidence**: no explicit CC, public-domain, or equivalent grant appears in this manuscript. Its availability as an author manuscript and older PDF metadata do not permit public redistribution; keep the copy private and cite the confirmed version-of-record DOI.

## Vault Ideas Extracted

- [Change Review Effectiveness](/vault/change-review-effectiveness.md) — Supplies field evidence that change rationale and prior contextual knowledge shape review depth, while distinguishing defect-oriented expectations from comment categories and broader team benefits.
