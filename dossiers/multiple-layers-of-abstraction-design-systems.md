---
type: Study Note
title: Multiple Layers of Abstraction in Design Systems
description: Spotify proposes data-only defaults, replaceable sub-parts, and composition from shared pieces to balance cohesion with product variation, but its early practitioner account reports no measured adoption, accessibility, or maintenance outcomes.
resource: https://engineering.atspotify.com/2023/05/multiple-layers-of-abstraction-in-design-systems
source: https://engineering.atspotify.com/2023/05/multiple-layers-of-abstraction-in-design-systems
tags: [design-systems, digital-interfaces, case-study]
timestamp: 2026-10-13T18:45:22Z
---

# Multiple Layers of Abstraction in Design Systems — Study Notes

**Author**: Charlie Eshleman, Design Systems Engineer; Spotify.  
**Published**: **May 25, 2023**; Spotify Engineering. The saved page prints this date, and its embedded article record carries a matching creation date.  
**Status**: First-party practitioner account, not peer-reviewed research. Read the complete supplied saved HTML article and both supplied figures: the visual abstraction spectrum and its technical counterpart. The page has no canonical-link declaration; the source URL is the coordinator-verified final HTTPS URL. Its **2026** copyright footer dates the snapshot, not the article.  

## What It Is

An architectural proposal for a shared design system that must serve both ordinary interface work and specialized product needs. Rather than choosing either tightly configured components or unrestricted assembly, Spotify offers **three simultaneous levels of abstraction**: ready-made defaults driven by data, replaceable sub-parts, and custom composition from shared base pieces.

The durable idea is to make the standard case easy without making the exceptional case impossible. The article describes a production card as **“one of our first components”** exploring this pattern. It is an early implementation account and statement of intentions, not an evaluation showing that the approach improved adoption or reduced costs.

## Problem and Motivation

The opening summarizes the premise of Spotify's earlier **2021** post: **customization** offers freedom and speed, while **configuration** offers cohesion and maintainability through abstraction. This summary comes from the **2023 article itself**, not an independent reading of the earlier post. More abstraction lets the system do more with less consumer input, but also makes its behavior more opaque. Engineers may struggle against those abstractions or abandon the shared component for a local replacement. The article supplies this as a practitioner explanation, without counts of abandonment or observed task difficulty.

Under “At present,” the author describes **hundreds of designers and thousands of engineers**, serving the main consumer product, creator and advertiser products, and internal tools. These are approximate organizational scale statements, not a study sample. Some teams lack direct design support; some concentrate on interface innovation, while others primarily need to deliver data and functionality. A single customization-versus-configuration choice would impose one working style on these different needs.

The system also reportedly leaned heavily toward customization: consumers received pieces they had to assemble and maintain themselves. The author argues that withholding common, accessible behavior because someone might need a different version unnecessarily transfers work to every consuming team.

## Mechanism as an Idea

### Three levels, available together

| Level | What the shared system supplies | What the consumer controls | Intended use |
|---|---|---|---|
| **Data-only defaults** | A complete standard component, including default presentation and behavior | Content and data | Routine cases; most abstraction and least assembly |
| **Replaceable sub-parts** | The standard whole and its default constituent parts | A specific part that needs different presentation or behavior | Limited departures without replacing the whole |
| **Composition from base pieces** | A base structure and reusable individual pieces | Arrangement, additional styling, and specialized behavior | Complex cases; fewest abstractions and most local responsibility |

The visual figure holds a card's basic identity constant while moving along this spectrum. The standard card uses a rectangular image; the middle example changes that image to a circle while retaining the surrounding card; the custom example adds body content and a richer action footer. These are **illustrations of supported variation**, not tested alternatives or measured user preferences. The technical figure shows the same progression from supplying content to replacing a part to arranging the contents directly; its implementation syntax is not the model being preserved here.

At the middle level, consumers can work directly with the relevant part rather than asking the parent component to accumulate ever more special-case controls. The author argues that this makes interaction with the part more transparent and prevents complexity from collecting in the enclosing abstraction. For larger departures, composition retains shared visual pieces without requiring the product to fit the complete default component.

The levels coexist rather than replacing one another. Configuration broadens what the system can do automatically; customization remains an escape route when those defaults are inappropriate. The article acknowledges that **a single default cannot meet every customer's needs**.

### Defaults at more than one organizational level

“Enhanced reuse” proposes a second layer of standardization within a consuming project's repository. The central system handles generic interface decisions; a product team handles recurrent product-specific behavior once, such as navigation or event tracking. Feature developers can then use that local standard with data-only inputs instead of repeatedly rebuilding the specialization.

“Reduced static” argues that a broader shared baseline also makes local departures easier to inspect. Standard aspects remain supplied by the system, so a specialized promotional card can express only its distinctive presentation and tracking needs. This is a claim about the visibility of divergence, not evidence that reviewers became faster or defects declined.

## Claimed Benefits / Admissions

The “Looking forward” sections distinguish aspirations from the early production example:

- **Increased utility**: ship commonly needed behavior, including accessible focus flows and internally managed interaction state, rather than relying only on assembly examples. The author expects easier default implementation to free time for genuinely distinctive features. No accessibility audit, conformance target, participant testing, time savings, or innovation measure is reported.
- **Enhanced reuse**: establish specialized defaults once at the product-repository level. The article gives navigation and tracking as examples of repeated concerns, but reports no repository count, reduction in duplication, or maintenance comparison.
- **Reduced static**: make local differences clearer by keeping unchanged behavior in the shared baseline. This is a rationale supported by a worked example, not a measured code-review or comprehensibility result.
- **Democratized defaults**: use override analytics to learn which parts are replaced most often and with what alternatives. A variant used more often than the default could prompt collaboration with its consumers and possible adoption as a new default. The wording describes a **potential feedback mechanism**; no override frequencies, adoption statistics, instrumentation method, or completed default revision are supplied.
- **Early scope**: the example is one of the first production components exploring the pattern, and the author calls the work the beginning of a journey. Extending the pattern across platforms is an intention; the supplied implementation figure illustrates one platform rather than demonstrating cross-platform results.

The closing references offer practitioner inspiration for surfacing common tasks, offering constituent parts, and making the preferred path easiest. They are not a comparative validation of Spotify's design.

## Analyst Takeaways

1. **Standardize the ordinary path without monopolizing the exceptional path.** The proposed solution keeps stable shared defaults and deliberate escape routes in the same component model rather than forcing an organization-wide choice between rigidity and bespoke assembly.
2. **Place customization at the smallest useful boundary.** Replacing one part can preserve the rest of the baseline. The source's rationale is reduced parent complexity and more direct control, not an established optimal granularity for every component.
3. **Distinguish central defaults from product defaults.** A behavior can be common within one product without belonging in the organization-wide system. Repository-level specialization supplies an intermediate place for that agreement.
4. **Use departures as evidence to discuss, not votes that automatically determine design.** The article proposes collaboration when an alternative outgrows the default; it does not prescribe automatic promotion. Usage alone does not establish accessibility or suitability across the less-visible products.
5. **Evaluate the exchange of burdens.** This account fits [Cognitive Dimensions Tradeoffs](/vault/cognitive-dimensions-tradeoffs.md): abstraction can reduce repeated assembly while adding opacity, learning, and hidden dependencies. That connection is an analyst interpretation; the article does not measure cognitive dimensions or prove that exposing parts eliminates dependency costs.

The parallel [study of design-system practice](/dossiers/understanding-supporting-design-systems-practice.md) reports leaders balancing customizability and standardization as a main challenge, with different components needing different degrees of customizability. Spotify offers one concrete response to that reported problem, not evidence that the response is universally appropriate. Compared with [Stripe's accessible color-system account](/dossiers/designing-accessible-color-systems.md), which presents selected numerical contrast checks, this source primarily supplies architectural reasoning and an early example, not numerical evidence for its accessibility benefit.

## Questions and Limitations

- **No measured outcomes**: no recruited participants, sampling procedure, comparison condition, usability measures, accessibility results, adoption denominators, override statistics, effect sizes, or longitudinal maintenance costs are reported. The company headcounts describe context, not evidence of successful use by those populations.
- The worked card and its two figures show the model's expressiveness, not that it is easy to learn or remains coherent across components. The account gives no criteria for deciding which components deserve all three levels or how finely their replaceable parts should be divided.
- Shared accessible defaults do not establish accessible specialized compositions. The article does not describe which interaction guarantees remain intact after a part is replaced or a complex layout is assembled, or who validates the result.
- The opacity diagnosis and claims of greater transparency are plausible practitioner interpretations without observed abandonment counts or controlled comprehension tasks. Exposing parts changes where complexity lives; it does not demonstrate that total complexity disappears.
- Override analytics may reveal recurring unmet needs, but the article does not define the unit of usage, account for uneven product scale, or show how popular alternatives are judged against the needs of teams with less design support.
- This is a **2023** account, not current design-system documentation. The embedded record also carries an update timestamp of **September 30, 2024**, but the saved article supplies no revision history explaining what changed. Its cross-platform ambition and early production example should not be treated as proof of later rollout. It offers no versioning, deprecation, or compatibility policy from which to infer breaking-change cost allocation.
- **Redistribution evidence**: the saved page footer states **“© 2026 Spotify AB.”** No explicit redistribution grant appears in the supplied copy; the saved HTML and figures belong in `archive/private/`, with the canonical HTTPS URL retained as the dossier source.

## Vault Ideas Extracted

- [Standardization versus Customization in Design Systems](/vault/standardization-versus-customization.md) — Contributes the three-level model of complete defaults, replaceable sub-parts, and composition; a distinction between central and product-repository defaults; and override analytics as a proposed collaborative feedback loop. Bounds all benefits to practitioner rationale and early experience without adoption or outcome data.
- [Cognitive Dimensions Tradeoffs](/vault/cognitive-dimensions-tradeoffs.md) — Adds a practitioner example of trading repeated local assembly for the opacity of a shared abstraction, with direct access to sub-parts proposed as an escape route. The cognitive-dimensions connection is interpretive, not a measured validation of reduced burden.
