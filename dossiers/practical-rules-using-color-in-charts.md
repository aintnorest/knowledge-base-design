---
type: Study Note
title: Practical Rules for Using Color in Charts
description: Stephen Few recommends assigning chart color to communication goals, ordered data, and selective emphasis, supported by visual demonstrations and practitioner rationale rather than controlled performance studies.
resource: https://www.perceptualedge.com/articles/visual_business_intelligence/rules_for_using_color.pdf
source: https://www.perceptualedge.com/articles/visual_business_intelligence/rules_for_using_color.pdf
tags: [color, data-visualization, visual-perception, attention, accessibility, low-vision]
timestamp: 2026-10-12T20:28:06Z
---

# Practical Rules for Using Color in Charts — Study Notes

**Authors**: Stephen Few; Perceptual Edge.  
**Published**: Visual Business Intelligence Newsletter, **February 2008**.  
**Status**: Practitioner guidance, not a peer-reviewed experiment. Read the complete **13-page supplied PDF**, including every chart, palette, and component table; the publisher's HTTPS PDF URL resolves to the same titled article.  

## What It Is

Nine rules for using color to communicate quantitative business information. Few explicitly limits his expertise to practical data-display use rather than comprehensive color theory or artistic expression. The reusable model is to assign color a job: **highlight information, group items, or encode quantitative values**, with different palettes appropriate to different jobs.

## Problem and Motivation

More and brighter color can compete with the data rather than clarify it. Arbitrary visual differences invite interpretation without supplying meaning; decorative gradients change perceived color and artificial depth adds distracting variation. A palette also needs to survive its actual mark size, background, and viewers' color perception.

## Principles and Stated Evidence

The article reports **no participant sample, timed task, error measure, effect size, or statistical comparison**. Its figures are perceptual demonstrations and design contrasts, not controlled evidence that every rule improves performance. The table preserves each recommendation and the evidence actually offered.

| Rule | Recommendation and rationale | Evidence supplied |
|---|---|---|
| **1** | Keep surrounding backgrounds consistent when equal-colored objects should look equal; avoid decorative background gradients | Identical gray squares placed across a white-to-black gradient visibly change apparent lightness. A simultaneous-contrast demonstration, without a cited study |
| **2** | Give objects sufficient contrast against their backgrounds so they remain visible | A profit/loss heatmap shows black numbers becoming hard to read in dark red/green cells, including important extremes. No contrast ratio or measured legibility threshold |
| **3** | Use color only for a communication goal; avoid decoration that competes with information | A conversation with color expert Maureen Stone about restrained conference presentations; practitioner observation, not an attention experiment |
| **4** | Map different colors to meaningful data differences rather than gratuitous distinctions; equal treatment encourages comparison | Multicolored versus single-color country-sales bars illustrate redundant category coding when axis labels already identify countries. The proposed wasted interpretation effort is not measured |
| **5** | Use restrained colors for ordinary information and brighter/darker colors for emphasis; preserve salience as a limited resource | Bar and scatterplot examples, including enlarged points, demonstrate that mark area affects visibility. Sample categorical palettes illustrate intended equal intensity; no observer ratings establish equality |
| **6** | Encode sequential quantity with one hue or closely related hues, varying perceived intensity rather than unrelated hue | Readers are invited to order unrelated hues, then ordered orange shades. Cynthia Brewer's categorical, sequential, and diverging palette framework is credited; no cited psychophysical study measures ordering accuracy or equal intervals |
| **7** | Make non-data structure only salient enough to support its role, so data dominate attention | Component tables prescribe subdued axes/borders and visible marks; rationale is visual hierarchy, not a measured fixation or performance result |
| **8** | Avoid red–green combinations for distinctions that many color-deficient viewers cannot perceive; red–blue is proposed for positive/negative heatmaps | Unsourced prevalence estimates of approximately **10% of males and 1% of females**, and a general claim about red–green difficulty. Few admits substitution does not work for everyone; no color-deficient participant test supports the word “guarantee” |
| **9** | Avoid decorative visual effects, especially light/shadow and pseudo-3D styling that add little communication value | The same employee counts appear as flat bars and shaded cylindrical forms; readers are asked which is easier to read. This is a visual comparison, not an experimentally established readability effect |

Rules 1–2 concern **context and visibility**; 3–4 concern **meaning**; 5–7 concern **ordering and attention**; 8 concerns **unequal sensory access**; 9 concerns **unnecessary encoding noise**. Color should support these goals rather than become a separate illustration layered over the numbers.

## Palette Model and Tradeoffs

### Category, magnitude, and divergence are different messages

For categories, Few recommends hues that are readily distinguishable but approximately equal in perceived intensity: difference without accidental rank. For sequential quantities, increasing intensity supplies an order that arbitrary hues do not intuitively supply. A diverging or “dual-ordered” palette combines two ordered sequences around a meaningful midpoint such as zero profit or deviation from an average. The midpoint is a semantic boundary, not merely the center of the available colors.

He credits **Cynthia Brewer and Color Brewer** as practical palette resources and mentions Stone's earlier guest article. These are expert sources, not a reference list documenting the empirical basis of the nine rules. His claim that expert palettes can remove the need for extensive usability testing is advice, not a demonstrated substitute for evaluating the actual audience and task.

### Salience depends on mark geometry and the job

A medium-intensity palette can work for bars yet become difficult to distinguish in small points or thin lines. Few proposes greater intensity **or larger/thicker marks**. This is a useful admission that palette quality is not independent of area. Pale colors can de-emphasize support structure, but the rule is “visible enough,” not “as faint as possible.”

For heatmaps, he separates **pattern scanning** from **precise-value lookup**. Removing overlaid numbers can reduce clutter and eliminate difficult text/background combinations, while a separate numeric representation retains exact values. The source recommends this division; it supplies no experiment establishing that hidden numbers universally improve scanning.

## Results / Admissions

- The strongest directly inspectable evidence is contextual appearance: equal gray squares look different across the gradient. This supports a warning about inconsistent surrounds, not a numerical estimate of resulting data-reading errors.
- Flat-versus-decorated bars, categorical-versus-single-color bars, and small-versus-enlarged points illustrate plausible mechanisms, but readers' subjective ease is not a measured performance outcome.
- The source distinguishes meaningful supporting labels and tick marks from genuinely non-data lines, borders, and fills. De-emphasis must not erase the scales required to interpret data.
- Rule 8's “guarantee” is explicitly qualified by “most” and by the admission that avoiding red–green does not solve the problem for everyone. Hue substitution alone does not supply redundant meaning or a complete accessibility guarantee.

## Analyst Takeaways

1. **Specify the message before the hue.** Category, ordered magnitude, direction about a midpoint, and selective emphasis call for different perceptual relationships.
2. **Spend salience intentionally.** Brightness or darkness is useful when it identifies something that deserves attention; making every mark prominent eliminates selective emphasis.
3. **Evaluate colors in their actual surrounds and areas.** A swatch palette is not evidence that small lines, labels, or dark heatmap cells remain distinguishable.
4. **Keep status meaning available beyond hue.** Few diagnoses red–green failure; as an analyst extension, labels, shape, position, or another redundant channel are needed when the distinction matters. The article itself does not establish that extension through testing.
5. **Separate overview and exact lookup without losing access.** Pattern displays can be uncluttered while an equivalent representation retains precise values; removing numbers is not permission to remove the information.

## Questions and Limitations

- This is **2008** guidance for business charts, not a modern WCAG conformance specification or a universal prohibition on decorative color in every communicative context. The article itself allows that advertising may have different goals.
- “Intensity” combines light–dark and pale–bright language without a formal perceptual metric. Its sample palettes are described as balanced or equally spaced, but the article gives no measurements validating those properties.
- An internal qualification deserves preservation: Rule 6 recommends darkening for **higher numerical values**, but the manufacturing example assigns the darkest palette to the **worst performance**, California, and the lightest to the best, Montana. This is ordering by evaluative concern rather than simple numerical increase; readers need the legend and the intended meaning.
- No underlying reference supports the stated **10%/1%** prevalence values, and red–green deficiency is described too categorically as inability to distinguish red and green. Record these as the author's claims, not current population estimates or a diagnostic model.
- No independent replication is applicable to the article's demonstrations as reported: there is no original participant experiment to replicate. It does not quantify how much arbitrary color, gradients, or decoration slow interpretation.
- **Redistribution evidence**: each page states **“Copyright © 2008 Stephen Few, Perceptual Edge.”** No redistribution license or public-copying grant appears in the file; the raw PDF belongs in the private archive even though the publisher makes it downloadable.

## Vault Ideas Extracted

- [Color Coding for Status](/vault/color-coding-for-status.md) — Supplies the warning that conventional red–green good/bad encoding can hide the very distinction it is intended to communicate; hue substitution is an incomplete practitioner remedy.
- [Perceptually Uniform Color Scales](/vault/perceptually-uniform-color-scales.md) — Contributes the categorical/sequential/diverging distinction and the intended roles of equal salience and perceptually ordered magnitude, without quantitative validation of its sample palettes.
- [Color Contrast Minimum](/vault/color-contrast-minimum.md) — Illustrates why dark heatmap cells can undermine overlaid text and why contrast must be assessed in context, without establishing a numerical threshold.
