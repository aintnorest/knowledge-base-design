---
type: Study Note
title: Designing accessible color systems
description: Stripe describes aligning palette lightness across hues to make contrast predictable while retaining color identity, but its 2019 case study demonstrates selected contrast checks rather than universal accessibility or measured perceptual equality.
resource: https://stripe.com/blog/accessible-color-systems
source: https://stripe.com/blog/accessible-color-systems
tags: [color, design-systems, digital-interfaces, low-vision, accessibility, case-study]
timestamp: 2026-10-12T20:28:06Z
---

# Designing Accessible Color Systems — Study Notes

**Authors**: Daryl Koopersmith and Wilson Miner; Stripe Design.  
**Published**: **October 15, 2019**; Stripe blog.  
**Status**: First-party design-system case study, not peer-reviewed research. Read the complete supplied saved HTML article, its palette/contrast/gamut figures and embedded demonstration video; the saved page's `rel="canonical"` is **https://stripe.com/blog/accessible-color-systems**. The supplied snapshot carries a **2026** footer, not a new publication date.  

## What It Is

An account of replacing a brand-derived interface palette whose colors looked uneven and frequently failed text contrast. Its durable contribution is to organize color by **perceived lightness, hue, and chroma**, then constrain allowed foreground/background relationships so designers can reuse colors without solving contrast from scratch.

The three objectives are **predictable accessibility**, **clear, vibrant hues**, and **consistent visual weight** across hue families. They are separate objectives: a contrast pass does not establish hue discrimination or equal salience.

## Problem and Motivation

Stripe's audit found that none of its default small-text colors except black met the intended contrast threshold. The original palette figure displays **0%** of nine illustrated gray/chromatic choices passing the **4.5:1** small-text target, and **66%** passing the **3:1** icon target. Black is outside this illustrated set, so the figure and the text are compatible rather than contradictory.

Hand-picking colors and checking individual pairs was slow trial and error, made every designer responsible for the accessibility rules, and left few aesthetically acceptable combinations. Simply choosing a darker shade did not consistently repair contrast: some hues remained too light, while sufficiently dark shades became muddy and difficult to distinguish. The problem was the organization of the scales, not merely the selection of one default shade.

## Mechanism as an Idea

### Machine coordinates are not perceptual coordinates

**RGB** describes emitted red, green, and blue contributions; its values do not directly answer how to make a color perceptually lighter, more colorful, or more yellow. **HSL** exposes more intuitive dimensions, but equal mathematical lightness and saturation do not yield equal perceived lightness and colorfulness across hues. The saved comparison makes blue look dark and yellow/green light despite nominally equal settings.

Stripe used **CIELAB**, whose lightness dimension is designed to approximate human perception. Translating existing scales into a perceptual model revealed diverging lightness curves across hue families. Aligning those curves made corresponding levels approximately equal in contrast while leaving hue and chroma adjustable enough to retain brand identity. The perceptually uniform hue illustration is an explanatory comparison, not a participant experiment demonstrating perfect equality.

The core model is **shared lightness organization with hue-specific chroma and hue choices**, rather than assuming every hue can be produced with identical settings. Contrast is still a foreground/background relationship checked against WCAG's luminance-based ratios; using Lab is not itself a contrast pass.

### Contrast becomes a constrained relationship

The article uses the **WCAG 2.0** targets of **4.5:1 for small text** and **3:1 for large text**; it also uses **3:1** as an icon target. The redesign places colors on coordinated scales, verifies selected combinations, and defines sufficient separation between darker and lighter palette positions for different content roles. This turns accessibility from repeated local improvisation into a property of **approved relationships within the palette**.

The claimed guarantees have boundaries:

- New default text/icon colors pass over **white** and the **lightest tint of any hue family**, matching common interface surfaces.
- Less common foreground/background combinations can follow a prescribed separation between positions in the coordinated scales.
- The separation rule belongs to this particular tuned palette; it is **not a universal law of Lab or arbitrary color scales**.

No internal palette values or tool operations are necessary to preserve that model. The article does not publish a general derivation proving that any independently generated equal-lightness scale will satisfy the same separation rule.

### Available color constrains the design

Hue, chroma, and lightness cannot vary independently over an unrestricted rectangular range. Some combinations cannot be represented, and naively clipping them to the nearest displayable color can break the intended relationships. The shaded diagrams expose the limited feasible range for retaining vivid hues while matching lightness across families.

The authors describe “really dark yellow” and “vibrant light royal blue” as impossible. The useful bounded reading is that the **desired hue identity, vividness, and lightness cannot all be retained simultaneously** in the working color range; brown or pale blue can exist, but do not deliver the same perceptual identity and chroma. This is a gamut/appearance tradeoff, not proof that a color named dark yellow never exists.

## Results / Admissions

- After iterations and testing in real interfaces, Stripe reports that the palette met all three design goals. The article provides **no participant count, task protocol, rating distribution, error rate, or statistical test** for those interface checks.
- The new illustrated icon set shows **100%** passing the **3:1** target; the illustrated text set shows **100%** passing **4.5:1**, compared with **66%** and **0%** in the earlier figure. These are displayed contrast evaluations of selected palette colors, not an accessibility user-study success rate.
- The lightness figures show previously separated hue-family curves becoming approximately aligned. Their small remaining differences, and displayed contrast values that vary slightly across hues, support **approximate uniformity**, not exact perceptual or numerical identity.
- A badge example exposes a second problem after contrast is solved: the palest backgrounds were hard to distinguish. Making background and foreground darker together maintained text contrast while increasing background differentiation. This is first-hand design reasoning, not evidence that all color-deficient users can distinguish the revised badges.
- The authors explicitly state that WCAG contrast alone does not measure **vibrancy**. Sufficient contrast can coexist with muted hues, and vibrant hue difference can coexist with insufficient reading contrast.
- Gamut restrictions made some coordinated colors difficult to find; the palette emerged through iteration, not an automatic guarantee that perceptual color spaces produce aesthetically satisfying results.

## Analyst Takeaways

1. **Move repeated contrast work into system constraints.** Approved relationships can reduce local errors, provided their real background and role assumptions remain intact.
2. **Separate contrast, hue distinction, and salience.** A passing text ratio cannot certify status-color discrimination, and equal intended visual weight needs more evidence than matching nominal HSL values.
3. **Use perceptual models to expose the tradeoff, not to erase it.** A model can show why one hue needs different chroma to retain similar lightness; it cannot make every desired combination feasible.
4. **Validate the composed interface.** Swatches do not reproduce small marks, surrounding colors, typography, or state meaning. The reported component iteration supports contextual review but does not replace testing with disabled users.
5. **Keep the guarantee's domain explicit.** Palette substitutions, new backgrounds, altered opacity, or a different color range are outside the relationships established in this account unless separately checked.

## Questions and Limitations

- This is a **2019** implementation account, not current documentation for Stripe's palette and not a normative accessibility standard. The article names **WCAG 2.0**; its **3:1 icon** target should not be described as WCAG 2.0's later non-text-contrast success criterion. [Color Contrast Minimum](/vault/color-contrast-minimum.md) distinguishes current text and necessary-graphics obligations.
- Equal perceived lightness, equal luminance contrast, and equal attentional salience are related but not identical. The article simplifies that relationship and offers no observer study of equal visual weight, no color-deficiency subgroup analysis, and no validation across displays or viewing conditions.
- The claim that each color follows “the same curve” is an approximation: the diagrams themselves show small lightness and contrast differences. Similarly, the repeated alt text **“original-lightness-values”** labels both the old-curve illustration and the subsequent proposed-curve illustration; surrounding prose, rather than the duplicated alt label, identifies the redesigned plot.
- The phrase “imaginary colors which aren't actually reproducible or perceivable” conflates color-space coordinates, display gamut, and perceptual feasibility. The source supplies no formal gamut definition or observer experiment establishing the broadest wording. Its practical admission is that clipping can conceal unattainable intended properties.
- Full accessibility needs non-color cues, semantics, interaction access, and appropriate content as well as contrast. The opening claim of reliably legible colors does not establish those outcomes or comfortable reading for every user.
- No independent replication is reported; this is a first-party engineering/design experience supported by visual examples and computed ratios. Its additional resources explain color spaces rather than validate the shipped product through controlled research.
- **Redistribution evidence**: the saved page footer states **“© 2026 Stripe, LLC.”** No redistribution grant is present in the supplied article; the saved HTML/assets belong in the private archive. The canonical HTTPS URL remains the dossier source.

## Vault Ideas Extracted

- [Perceptually Uniform Color Scales](/vault/perceptually-uniform-color-scales.md) — Contributes aligned perceived-lightness organization, hue-specific feasible chroma, and the limits of HSL equality and gamut clipping from a real palette redesign.
- [Color Contrast Minimum](/vault/color-contrast-minimum.md) — Contributes system-level approved-pair constraints and selected before/after contrast checks while separating numerical passes from legibility, color differentiation, and complete accessibility.
- [Color Coding for Status](/vault/color-coding-for-status.md) — The badge example shows that passing text contrast can leave colored surfaces difficult to distinguish; differentiation is a separate design constraint.
