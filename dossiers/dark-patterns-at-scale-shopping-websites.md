---
type: Study Note
title: "Dark Patterns at Scale: Findings from a Crawl of 11K Shopping Websites"
description: A crawl of 11,286 shopping websites documents 1,818 dark-pattern instances and a third-party supply ecosystem, but its text-centered discovery pipeline yields a lower bound rather than population prevalence or measured consumer harm.
resource: https://doi.org/10.1145/3359183
source: https://doi.org/10.1145/3359183
tags: [deceptive-patterns, decision-making, digital-interfaces, interaction-design, taxonomy]
timestamp: 2026-10-11T23:50:47Z
---

# Dark Patterns at Scale — Study Notes

**Authors**: Arunesh Mathur, Gunes Acar, Michael J. Friedman, Elena Lucherini, Jonathan Mayer, Marshini Chetty, and Arvind Narayanan.  
**Published**: November 2019; Proceedings of the ACM on Human-Computer Interaction 3, CSCW, Article 81, 32 pages; accepted August 2019.  
**Status**: Peer-reviewed CSCW work read as arXiv:1907.07032v2, posted September 20, 2019, the latest revision listed by arXiv. The PDF carries the published article's ACM reference, DOI, article numbering, and November 2019 publication footer; it is a publisher-formatted arXiv copy of the same published work, not a separate study. Key: doi:10.1145/3359183.  

## What It Is

A large-scale descriptive audit of shopping interfaces, combining automated collection with expert interpretation. The contribution is not an autonomous detector that certifies whether a design is ethical: it is a way to reduce millions of interface fragments to an inspectable corpus, then characterize how identified designs subvert decisions.

The study finds **1,818 instances**, representing **15 types in seven categories**, on **1,254 of 11,286 websites (approximately 11.1%)**. A second, mechanism-focused taxonomy describes five attributes of influence. These are distinct layers: a named pattern identifies a recurring design; an attribute explains what is wrong with its choice architecture.

## Problem and Motivation

Prior collections gave practitioners recognizable examples but little evidence of prevalence, implementation, or the infrastructure supplying them. Shopping makes possible harms concrete: unwanted purchases, undisclosed recurring fees, and unnecessary disclosure of personal information. The authors distinguish dark patterns from ordinary persuasion or impulse-buying affordances: product photographs and reasonable returns can encourage buying without fundamentally subverting the user's decision.

Their concern is benefit to the service through coercion, steering, or deception that leads to decisions a fully informed person with meaningful alternatives might not make. This is a normative counterfactual, not something directly measured for each visitor in the crawl.

## Mechanism as an Idea

### Five attributes of influence

- **Asymmetric**: explicit interface choices receive unequal weight or burden, such as a conspicuous acceptance option and a difficult rejection route. The paper deliberately limits this attribute to explicit choices, rather than every difference in process effort.
- **Covert**: the influence of the design is hidden from the person, even when the visible message itself is obvious. A decoy option can be visible while its steering role remains unrecognized.
- **Deceptive**: affirmative falsehoods, misleading statements, or omissions induce false beliefs. A countdown that expires without ending its offer is a concrete example.
- **Hides information**: necessary information is obscured or delayed, including costs disclosed only after substantial checkout effort.
- **Restrictive**: available choices are reduced, such as requiring enrollment or allowing cancellation only through customer service.

These attributes can overlap; they are not five mutually exclusive bins. **Covert influence is not identical to hidden information**, and a burdensome or coercive pattern need not contain a factual lie. The authors connect patterns to anchoring, bandwagon, default, framing, scarcity, and sunk-cost effects. Those connections are theory-grounded explanations, not measured mediators in this study.

### Seven categories and fifteen types

Counts below are **instances / websites** from Table 1; website totals overlap across types.

| Category | Types and observed counts | Decision mechanism |
|---|---|---|
| Sneaking | Sneak into Basket **7 / 7**; Hidden Costs **5 / 5**; Hidden Subscription **14 / 13** | Add an unrequested purchase, defer a cost, or conceal recurrence so the apparent transaction differs from the actual commitment. |
| Urgency | Countdown Timer **393 / 361**; Limited-time Message **88 / 84** | Accelerate choice through a threatened loss of an offer; an unspecified deadline prevents judging the actual time available. |
| Misdirection | Confirmshaming **169 / 164**; Visual Interference **25 / 24**; Trick Questions **9 / 9**; Pressured Selling **67 / 62** | Steer choices through shame, misleading hierarchy, confusing language, or expensive defaults and high-pressure upselling. |
| Social Proof | Activity Notifications **313 / 264**; Testimonials of Uncertain Origin **12 / 12** | Use apparent peer activity or endorsement to make a purchase seem desirable or normal. |
| Scarcity | Low-stock Message **632 / 581**; High-demand Message **47 / 43** | Make availability appear precarious, increasing perceived value and pressure to act. |
| Obstruction | Hard to Cancel **31 / 31** | Make leaving a recurring commitment substantially harder than entering it. |
| Forced Action | Forced Enrollment **6 / 6** | Make an unrelated disclosure, account, or marketing consent a condition of the desired task. |

The figures show why context matters. Figure 3 juxtaposes an automatically added greeting card, a last-step handling fee, and a subscription whose recurrence requires further discovery. Figure 5 shows an opt-out rendered gray despite remaining clickable: the failure is false actionability, not missing functionality. Figure 8 contrasts cancellation requirements buried in a terms PDF with the same requirement disclosed upfront; transparency changes the information-hiding attribute without removing restriction.

## Results / Admissions

### Corpus, task, and detection pipeline

There were **no recruited consumer participants**. The observational units were websites, pages, and interface segments; the task was an automated approximation of selecting a product, adding it to a cart, and proceeding to checkout without purchasing.

- The starting list contained **361,102 Alexa-ranked websites**. A shopping classifier produced **46,569** candidates, and English-language filtering left **19,455**. This list was assembled in August 2018; it is not a sample of all countries, languages, or retailers.
- Product discovery collected at most **five product pages per website**, yielding **53,180 pages from 11,286 sites**. In a separate **100-site** evaluation, discovery returned appropriate results on **86** sites. This is a crawler assessment, not dark-pattern recall.
- A checkout crawler captured page sources, screenshots after state changes, network responses, and dynamically changing text. In a **100-product-page** assessment, it reached checkout on **66**, added to cart without completing the remaining path on **14**, and encountered exceptions or failed button discovery on **20**. The approximately **90-hour** crawl therefore does not imply complete purchase-flow coverage.
- Approximately **13 million text segments** became **1.3 million** unique normalized texts. Text representations and hierarchical clustering organized them into **10,277 clusters**; clustering was expressly an aid to scanning, not latent-construct discovery or an ethical classifier.
- One researcher selected **1,768** potentially relevant clusters. Two researchers independently examined **200** of these using screenshots and live website context; agreement was **Cohen's κ = .74**. After resolving disagreements, one researcher inspected the remaining clusters, and the team grouped the findings into types and categories.

**No end-to-end recall estimate is reported.** Human agreement on selected clusters does not recover patterns lost during site classification, navigation, segmentation, text normalization, clustering, or the initial single-researcher screening. Visually constituted patterns could be found incidentally when text prompted inspection, but visual style was not part of discovery clustering.

### Prevalence and verified deception

More popular sites were more likely to contain detected patterns (**Spearman's ρ = −.62, p < .0001**, against Alexa rank). This is an observational relationship, not evidence that popularity causes manipulation.

The paper reports **234 deceptive instances across 183 websites**. Its targeted checks revisited relevant dynamic displays every **four hours for five days**, supplemented by inspection of how values were generated:

- **157 countdown-timer instances on 140 sites** reset with the offer still valid or expired without ending it.
- **29 activity-notification instances on 20 sites** used fabricated or misleading content. Server-generated notifications were excluded from this verification because their integrity could not be inspected.
- **17 low-stock instances on 17 sites** generated stock deceptively: **16** decremented on a recurring deterministic schedule and **one** generated random stock on page load. Unchanging stock was excluded from this check rather than proved truthful.

These three checks are not an exhaustive accounting of the headline 234 deceptive instances. Nor should all **1,818** identified patterns be called verified falsehoods. The study also labels pressure tactics and unclear-origin endorsements as dark patterns without demonstrating fabrication in every instance.

### Third-party supply

The authors attributed social-proof notifications through network content and manual script inspection, then searched for the responsible providers across the corpus. They identified **22 entities embedded on 1,066 shopping sites**, and on **7,769 sites** in a separate November 2018 top-million homepage crawl. Embedding is not proof that every site displayed a dark pattern during observation; homepage-only measurement also misses providers loaded only on product pages.

Beeketing appeared on **406** shopping sites, Dynamic Yield on **114**, and Yieldify on **111**. Providers often bundled social proof with urgency, scarcity, or pressured selling. **Two openly advertised fake-order capabilities**: Boost's “Fake it till you make it” page and WooCommerce Notification's claim that “the plugin will create fake orders of the selected products.” The reusable finding is a supply-chain mechanism: manipulative choice architecture can be purchased and reproduced, not merely invented independently by each retailer.

## Analyst Takeaways

1. **Use the five attributes to explain harm, not merely assign a memorable name.** Unequal burden, concealed influence, false belief, missing information, and lost alternatives identify different remedial questions. A disclosure can fix one without repairing another.
2. **Treat 11.1% as detected prevalence in this corpus, not a global rate.** The pipeline deliberately trades coverage for inspectability. Neither κ nor checkout success supplies the missing recall correction.
3. **Map taxonomies by level, not by matching labels.** In [Gray et al.](/dossiers/dark-patterns-side-of-ux-design.md), Sneaking, Obstruction, and Forced Action are direct strategic counterparts. Mathur's Misdirection broadly corresponds to Gray's Interface Interference; expensive defaults map to preselection and confirmshaming to toying with emotion. Urgency and Scarcity partly elaborate Gray's emotional/aesthetic manipulation, while Social Proof makes peer influence a separate category. Gray's Nagging has no dedicated Mathur category, although repeated pressure can overlap with it. This is an analyst crosswalk, not a validated one-to-one conversion.
4. **Trace the infrastructure as well as the screen.** Shared suppliers create repeated failure modes and potential intervention points, but supplier presence is not equivalent to a verified deceptive message.
5. **Do not turn the crawl's bias explanations into effect-size claims.** It establishes occurrence and some falsity, not purchase uplift, comprehension loss, or differential susceptibility. Later work such as [Luguri and Strahilevitz's experimental study](https://doi.org/10.1093/jla/laaa006) addresses behavioral effects with a different method; it is not a replication of this prevalence estimate.

## Questions and Limitations

- English-language, popularity-ranked shopping sites and sampled purchase paths omit home/search pages, account creation, post-purchase upsells, actual cancellation attempts, and other application domains. Geographic location and crawler failures further constrain coverage.
- Intent is often uncertain. A real shipping deadline, accurate stock disclosure, or understandable default may resemble a coded pattern without the same ethical status. The authors acknowledge disagreement about the gray area rather than measuring users' judgments of it.
- The abstract and introduction's broad language about covert, deceptive, and information-hiding patterns should not erase the difference between taxonomy-level potential and **verified** deception. The proposed warning-extension figure is a mockup, not an evaluated countermeasure.
- Section 4.1's false-positive percentages are internally inconsistent with its appendix: Table 3 shows **1/443** false positives for Alexa and **20/443** for Webshrinker, approximately **0.23% versus 4.51%**, not the text's **0.2% versus 0.4%**. The lower Webshrinker false-negative rate is supported by the table; the printed false-positive comparison is not.
- The paper's US/EU legal conclusions describe its 2019 analysis, not an adjudication of every example or current legal advice.
- Redistribution is not licensed to this repository. The PDF carries ACM's personal/classroom-use notice and states “© 2019 Copyright held by the owner/author(s). Publication rights licensed to ACM.” The [arXiv abstract page](https://arxiv.org/abs/1907.07032) links the [non-exclusive distribution license](https://arxiv.org/licenses/nonexclusive-distrib/1.0/), whose operative grant is “I grant arXiv.org a perpetual, non-exclusive license to distribute this article.” That names arXiv as licensee; it is not Creative Commons or a general public redistribution grant. The dossier therefore uses the publisher DOI as `source`.

## Vault Ideas Extracted

- [Deceptive Pattern Attributes](/vault/deceptive-pattern-attributes.md) — Five overlapping dimensions separate unequal burden, concealed influence, false belief, delayed information, and restricted alternatives; the crawl supplies concrete examples and detection limits.
