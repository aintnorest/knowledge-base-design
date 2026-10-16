---
type: Study Note
title: Accordion Pattern (Sections With Show/Hide Functionality)
description: W3C APG describes expandable sections as a way to reduce scrolling while preserving discoverable headings and intelligible disclosure state, but supplies no measured evidence that hiding content improves discovery or comprehension.
resource: https://www.w3.org/WAI/ARIA/apg/patterns/accordion/
source: /archive/aria-apg-accordion-pattern/source.pdf
tags: [interaction-design, information-architecture, assistive-technology, accessibility, digital-interfaces]
timestamp: 2026-10-16T00:00:00Z
---

# Accordion Pattern — Study Notes

**Authors**: W3C WAI-ARIA Authoring Practices Task Force.  
**Published**: Undated living APG guidance, captured October 16, 2026. Neither the supplied PDF nor the canonical page displays a guidance revision date; the footer's 2026 copyright is not a revision date.  
**Status**: Informative accessibility pattern guidance, not a normative accessibility standard or a user experiment. Read the complete four-page PDF and its illustration; the live page declares the canonical URL above.

## What It Is

A model for organizing several sections behind a vertically stacked set of interactive headings. A heading identifies the content and provides a way to reveal it; the associated panel contains the section. The source explicitly gives **reducing scrolling** as the rationale. This organizational model and its accessibility tradeoffs make the source eligible beyond its implementation instructions.

## Principles as Ideas

### Preserve an inspectable representation of hidden content

A collapsed section still needs a visible representation: a title, snippet, or thumbnail tells people what they can reveal. The source allows snippets and adjacent section actions to remain visible. Hidden detail and persistent orientation are therefore separate design choices, not an all-or-nothing demand to conceal a section.

### Disclosure policy changes the reading task

The source permits multiple sections to be open, only one open, or one required to remain open. In a single-open arrangement, opening one section can close another. **Analyst inference:** this reduces simultaneous content but can make cross-section comparison require repeated switching and memory. The source describes these policies without testing or ranking them.

### Navigable structure must survive compression

Headings remain meaningful in the page's information architecture, and disclosure state must be understandable to assistive-technology users. Opening content must not remove its interactive contents from ordinary keyboard navigation. The source also warns against proliferating navigable regions: extra structural destinations can become noise rather than orientation. Its approximate panel-count example is not a validated maximum number of sections.

The small example illustration represents a form divided into three expandable sections. It demonstrates grouping, not a measured improvement in form completion or a prescription that forms should be collapsed.

## Evidence / Admissions

- The page supplies no participants, research task, discovery rate, completion time, comprehension measure, effect size, or independent replication.
- The claimed benefit is less scrolling, not evidence that hidden information is encountered or understood more often.
- It provides no comparison between always-visible content, single-open sections, and multiple-open sections, and no rule for deciding which content is safe to hide.
- The live page includes a schematic accordion image that is absent from the saved PDF's main explanation; the PDF retains the small expandable-form example illustration. Neither illustration supplies outcome evidence.

## Analyst Takeaways

1. **Distinguish shorter pages from easier discovery.** A compact heading list can reduce scrolling while adding a decision to expose every hidden section.
2. **Leave enough context visible to choose meaningfully.** A title or short preview should identify the section without requiring prior knowledge of its contents.
3. **Choose disclosure policy for the task.** Simultaneous reading and comparison may justify several open sections rather than forced switching.
4. **Keep essential decision context perceivable.** The existing evidence on requested explanations belongs to a different task, but cautions against treating technically available content as necessarily encountered.

## Questions and Limitations

- No quantitative benefit, current assistive-technology compatibility result, or WCAG conformance claim follows from this pattern alone. The source is guidance rather than a success criterion; no success-criterion version is being asserted.
- No internal numerical or substantive contradiction was identified. The absent revision date limits version-specific interpretation.
- **Redistribution evidence**: the PDF footer states copyright © 2026 World Wide Web Consortium and that liability, trademark, and permissive-license rules apply, linking the W3C Software and Document License. The supplied 2023 licence explicitly permits copying and distribution, conditional on preserving its notice and existing terms. The PDF is archived unchanged with the full [2023 licence notice](/archive/aria-apg-accordion-pattern/W3C-SOFTWARE-AND-DOCUMENT-LICENSE-2023.html) alongside it. No endorsement is implied.

## Vault Ideas Extracted

- [Recognition over Recall](/vault/recognition-over-recall.md) — Adds the scrolling-versus-disclosure tradeoff, persistent section representations, and the untested comparison cost of single-open policies; no separate collapsible-sections note is needed.
