---
type: Study Note
title: Understanding and Supporting the Design Systems Practice
description: A public-issue analysis and nine leader interviews expose the tension between stable shared design knowledge and changing product needs, but do not measure maintenance effort or establish that bottom-up governance improves outcomes.
resource: https://doi.org/10.1007/s10664-022-10181-y
source: https://doi.org/10.1007/s10664-022-10181-y
tags: [design-systems, design-process, digital-interfaces]
timestamp: 2026-10-13T18:44:59Z
---

# Understanding and Supporting the Design Systems Practice — Study Notes

**Authors**: Yassine Lamine and Jinghui Cheng; Polytechnique Montréal.  
**Published**: Version of record: *Empirical Software Engineering* **27(6), article 146**, **August 6, 2022**; DOI **10.1007/s10664-022-10181-y**, publication metadata verified by the ingest coordinator through Crossref.  
**Status**: Peer-reviewed journal article; read the complete supplied **28-page arXiv preprint 2205.10713v1**, submitted **May 22, 2022**, including both figures, both tables, declarations, and references. The copy retains manuscript-template placeholders for journal name and received/accepted dates. The publisher version was not accessible to the ingest coordinator; differences between this preprint and the published article are **unverified**. Findings below refer to the preprint, not a comparison of versions.  

## What It Is

Two exploratory studies of design-system practice: a content analysis of **4,714 public GitHub issues from 41 open-source design systems**, and interviews with **nine leaders from nine companies**. The first maps what communities discuss in public trackers; the second describes what experienced decision-makers believe a design system is, why they value it, and how they manage its tensions.

The authors' “living definition” is an **all-in-one design and development environment containing UI components and guidelines, serving as a common language for unifying design** (§5). Its central tension is preserving stable shared knowledge without freezing the system against the changing needs of concrete products. A design system is therefore an evolving organizational arrangement, not merely a static component collection.

The paper offers an empirical description and design implications, **not a causal evaluation of design-system adoption, governance policies, or supporting tools**. Reported benefits are leaders' accounts; issue counts are topic frequencies, not hours of maintenance work.

## Problem and Motivation

Design systems promise consistency, reuse, maintainability, and better designer–developer collaboration. Yet the authors find little cross-organization research about their definitions, maintenance challenges, or practices that could inform supporting tools. Public communities also bring requests and concerns beyond those of the organization owning the system.

The two research questions separate these perspectives: **what issues projects deal with**, using public issue discussions as a proxy, and **how project leaders perceive and approach the practice**. Compared with general design patterns, systems include concrete support for design and implementation; compared with general front-end frameworks, they incorporate organization-specific identity and guidelines (§2.1). Neither distinction establishes that every repository calling itself a design system serves the same role.

## Study Design

### Public issue analysis: selection and coding

The researchers started with **90 projects in the curated Adele list**, which includes design systems, style guides, and pattern libraries. They selected **52** by comparing their visual design with owners' products, using incorporation of an organization's identity to distinguish design systems. They then required a public GitHub repository and excluded projects described as having **“less than 10 issues and 10 commits”**, leaving **41** (§3.1.1). The printed conjunction is not clarified into separate exclusion rules.

Data collection in **June 2019** retrieved issue titles, descriptions, comments, open/closed state, and identifying metadata. Of a reported **16,635 issues**, they randomly sampled **5,000**, then excluded **286** for insufficient or incomprehensible information, yielding **4,714** (§3.1.2). Sampling was across issues, not equal-sized samples per project; larger trackers can dominate the aggregate. Table 1 reports projects ranging from **13 to 3,698 issues** and an average **42.3 contributors**.

Two researchers independently conducted inductive coding on a random **200-issue** subset, then discussed and compared codes to establish themes for **project aspect** and **issue nature**. They used those themes to code the remaining **4,514** (§3.1.3). The paper **does not specify how many researchers coded the remainder**, whether it was single-coded, how disagreements there were resolved, or an issue-coding reliability statistic. The interview kappa must not be transferred to this analysis.

### Leader interviews: recruitment and analysis

Recorded, semi-structured remote interviews ran **August–October 2019**, lasting about **40 minutes each**. Recruitment identified highly active commit and issue-discussion contributors in the selected projects, then contacted those with public email addresses in descending contribution order. The authors stopped at **nine**, citing data saturation; the invitation count, response rate, and operational saturation criterion are not reported (§4.1).

All participants were **male**, with **2–7 years** of design-system experience. Table 2 lists **two in the UK, one in the US, one in Russia, three in Spain, and two in Canada**. Roles range from product/design leads and managers to engineering leaders and a software engineer; §6 characterizes the sample as **three designers, three developers, and three managers**. Each occupied a consequential position in a different company's system. This is a deliberately experienced leadership sample, not a representative sample of system consumers or beginners.

The interviews addressed definitions, benefits, challenges, and mitigating practices. Fully transcribed recordings underwent inductive thematic analysis within those four topics. A codebook creator identified themes; another researcher, described as a **blind coder**, applied the codebook to the transcripts. The reported **average Cohen's κ = 0.88 across codes** supports coding agreement (§4.1.3), not independent confirmation that the perceived benefits occur. Per-code kappas and quantitative outcomes are not supplied. The declarations report ethics-board approval and no competing interests.

## Results / Admissions

### What public trackers discuss

Figure 1 crosses project aspect and issue nature. Counts are reproduced as printed; percentages below are calculated against **4,714** rather than additional reported outcomes.

| Project aspect | Bugs | New-component requests | Improvement suggestions | Questions | Total | Share |
|---|---|---|---|---|---|---|
| UI-component behavior | 1,751 | 165 | 65 | 34 | **2,015** | **42.7%** |
| UI-component visual design | 396 | 52 | 19 | 13 | **480** | **10.2%** |
| Documentation | 158 | 130 | 27 | 6 | **321** | **6.8%** |
| Software development | 179 | 88 | 21 | 22 | **310** | **6.6%** |
| Community | 0 | 13 | 78 | 44 | **135** | **2.9%** |
| Other | 324 | 922 | 168 | 39 | **1,453** | **30.8%** |
| Total | **2,808** | **1,370** | **378** | **158** | **4,714** | **100%** |

By issue nature, **59.6%** are bugs/problems, **29.1%** new-component requests, **8.0%** improvement suggestions, and **3.4%** questions. Rounding produces a **100.1%** sum. Requests plus improvements total **1,748/4,714 = 37.1%**, matching §5.3. The printed **42.7% behavior** and **10.2% visual-design** figures also match their counts.

Behavior topics include state changes (**245 issues**), animation (**153**), accessibility (**124**), navigation (**101**), input verification (**112**), keyboard shortcuts (**93**), and responsiveness (**47**) (§3.2.1). Some issues mention more than one behavior aspect: these are overlapping subtopics, not a complete partition. Accessibility discussion includes screen-reader and keyboard support, but its presence does not demonstrate accessible products or successful disabled-user experiences.

The issue-nature column label remains **“requests for new components”** even for documentation and software-development rows. The paper does not fully explain that broader use of the label. Likewise, **Other accounts for 30.8%** of the sample and **922** new-component requests, but receives no separate project-aspect account. The five named aspects are not an exhaustive explanation of the corpus.

The authors interpret behavior's prominence as reflecting product-specific interaction needs, while centrally managed, brand-bound visual design may be more stable (§5.1). That is an explanation, **not a measured difference in change frequency, labor, or failure risk**. Public bugs can draw attention disproportionate to their resolution effort; private design decisions and other discussion venues are absent.

Documentation exposes a numerical inconsistency: §5.1 calls it **“about 10%”**, whereas **321/4,714 = 6.8%**. The authors suggest internal maintenance or immature communities could explain its relative scarcity, and later say leaders' centralized documentation practices partially explain it (§5.2). Neither study directly measures where all documentation discussion occurs or tests those explanations.

### How leaders define and value the system

Concept themes overlap (§4.2.1): **four** leaders describe an all-in-one design/development environment; **three** a means of crafting prototypes/products; **three** guidelines and rules; **three** a common language for unifying design. Guidelines are described as carrying practices, limitations, and organizational expectations beyond reusable artifacts. The common-language idea concerns both shared user-facing meanings and shared team understanding.

Perceived benefits (§4.2.2) are:

- **Efficiency and reduced cost — seven participants**: reusable patterns and a centralized reference reduce reinvention and speed movement from idea to product.
- **Consistency and coherence — five**: shared design and implementation align behavior and appearance across products.
- **Communication and collaboration — four**: a common vocabulary helps designers and developers refer to the same thing and helps newcomers understand local practice.

These are counts of leaders expressing themes, **not measured savings, comparative adoption rates, user-performance effects, or universal agreement**. Figure 2 connects concepts, benefits, challenges, and strategies as the authors' thematic synthesis, not a tested causal path model.

### The governance tension and recommended strategies

Three challenges recur (§4.2.3): **six** participants discuss balancing customizability with standardization; **six** keeping the system relevant as products evolve; **five** unfavorable culture or mindset. Deciding whether a requested component belongs in the shared system or should remain product-specific is itself difficult. Refusing a request can lead a team to build locally. Adoption, continued relevance, nimbleness, and preventing scope creep can be harder than initial creation.

Four strategies are recommended in §4.2.4; unlike benefits and challenges, the paper gives **no participant count for each strategy**:

1. **A dedicated team** maintains the system, supplies support, and acts as organizational ambassadors. Central responsibility does not imply relocating every product designer into that team.
2. **Bottom-up evolution** elevates components and guidelines from existing products, generalizes useful solutions, and redistributes the shared version. P1 describes a reciprocal **“push and pull”** between product innovation and central consolidation, in contrast to imposing entirely new designs from above.
3. **Proactive communication** brings consumers' feedback into the system and makes changes understood; publishing documentation alone is not treated as sufficient organizational communication.
4. **High-quality documentation** supports use, developer experience, and adoption, including in smaller organizations. The participants stress its importance without furnishing a controlled documentation-quality comparison.

The authors add that customizability should vary by component (§5.3): a **button may need less variation than a calendar**. They attribute this to participants and propose existing product variation as a signal of required flexibility. This is contextual design judgment, **not a validated complexity-to-customizability rule** or a quantified subgroup result.

Bottom-up is a **participant recommendation and author interpretation**. There is no top-down versus bottom-up outcome comparison, no before/after implementation measure, and no evidence that every local variation deserves promotion into the shared system.

## Tool Needs: Authors' Implications

The authors propose support for starting a system, discovering similar product elements for consolidation, judging appropriate customization from product variation, maintaining documentation alongside components, inviting feedback on guidelines, and synchronizing designer and developer contributions (§5.3). These follow the stable-knowledge/changing-needs tension; they are **opportunities for research**, not established requirements with measured benefits.

They mention prototypes and feedback from **six design-system experts**, reporting preliminary workflow fit and collaboration comments. No detailed recruitment, tasks, measures, numerical outcomes, or comparative evaluation accompanies that paragraph. It does not validate automated extraction, merging, documentation generation, or lower maintenance cost.

## Analyst Takeaways

1. **Treat centralization as a scope decision, not a mandate to share everything.** Recurring product needs can motivate promotion; variation that does not generalize can remain local. The interview evidence makes the dilemma visible rather than solving its decision rule.
2. **Stability and flexibility are jointly negotiated.** Stable defaults can support common meanings, while component-specific customization accommodates varied tasks. Equal customization everywhere is not the model these leaders describe.
3. **Separate maintenance visibility from maintenance burden.** Behavior dominates public issue topics here; that does not establish that behavior consumes the most labor, that visual decisions are easy, or that documentation deserves little investment.
4. **Keep product-to-system feedback open while assigning stewardship.** A dedicated team and bottom-up contribution are complementary in the accounts: one provides ownership, the other protects contact with real product needs.
5. **Do not count governance recommendations as measured improvements.** Reuse savings, collaboration gains, bottom-up superiority, and proposed tool benefits need outcome evidence beyond experienced leaders' accounts.

The common-language rationale complements [Consistency and Convention](/vault/consistency-and-convention.md), but offers no user learning/error test. The [accessible-color-system case study](/dossiers/designing-accessible-color-systems.md) illustrates a concrete constraint moved into shared defaults; this paper contributes the broader organizational tension around selecting and revising those defaults, rather than another palette evaluation.

## Questions and Limitations

- **Coverage and aggregation (§6)**: proprietary systems and discussions in forums, conferences, or internal channels are excluded. Random issue sampling favors larger projects; the authors recommend project-based analysis to address that bias. Adele selection and the identity-based inclusion judgment also bound what “design system” means in this corpus.
- **Recruitment (§6)**: GitHub is developer-oriented and can miss designers/managers, although the authors report three participants in each role category. Public-email availability and willingness to interview add selection filters. All nine participants are male; inexperienced practitioners and ordinary consumers are not represented. The authors explicitly call for their perspectives on starting and adopting systems.
- **Coding transparency**: the two-researcher inductive issue pass is explicit, but staffing and reliability for the remaining 4,514 issues are unspecified. The interview's **average κ = 0.88** applies only to its codebook/transcript analysis. Saturation is asserted without a stopping trace; theme counts should not be read as population prevalence.
- **Arithmetic and reporting**: Figure 1 is internally additive, and **42.7%, 10.2%, and 37.1%** agree with its counts. Documentation's printed **“about 10%”** does not match **6.8%**. Summing the **41 Table 1 issue totals gives 16,522**, consistent with its **403.0** mean, but §3.1.2 reports **16,635 extracted issues**, a **113-issue difference** left unexplained. Do not silently replace either source number or invent an exclusion account. The vague “about half” bugs and “about one-third” requests summarize **59.6%** and **29.1%**, respectively.
- **Residual category and interpretation**: **1,453 Other issues** receive no substantive category explanation; the public distribution cannot establish full maintenance-work coverage. More issues do not demonstrate more hours, more actual changes, or lower quality. Centrally maintained visual design and documentation are explanatory interpretations, not tests of underlying activity.
- **Outcome and version boundaries**: evidence dates to **2019**, despite the **2022** publication. There is no causal adoption study, controlled governance comparison, detailed tool evaluation, or independent replication established here. Introductory claims that systems “ensure” usability characteristics go beyond what these two studies measure. Differences from the peer-reviewed version remain unverified.
- **Breaking-change scope**: the source describes evolution, local-versus-shared responsibility, and communication of changes, but **does not study semantic versioning, deprecation windows, backward compatibility, migration costs, or end-user costs**. Any connection to those policies is a synthesis boundary, not a result of this paper.
- **Redistribution evidence**: the complete supplied preprint carries the **arXiv:2205.10713v1** date stamp but no explicit third-party redistribution grant or copyright/license block. Its [arXiv record](https://arxiv.org/abs/2205.10713v1) links the [arXiv non-exclusive distribution license](https://arxiv.org/licenses/nonexclusive-distrib/1.0/), which grants distribution to **arXiv.org**, not a general grant to third parties. This copy belongs in `archive/private/`; the dossier cites the published DOI.

## Vault Ideas Extracted

- [Standardization versus Customization in Design Systems](/vault/standardization-versus-customization.md) — Contributes **six of nine leaders** reporting the balancing challenge, a product-to-system bottom-up feedback model, dedicated stewardship, and component-dependent customization. Public behavior topics and **37.1% requests/improvements** show visible demands for change, not that all variation should be centralized or that one governance approach wins.
- [Consistency and Convention](/vault/consistency-and-convention.md) — Adds leaders' common-language rationale for coherent product meanings and cross-role communication, while distinguishing perceived organizational benefits from measured user learning or performance.
