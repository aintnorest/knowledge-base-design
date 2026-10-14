---
type: Study Note
title: "Feature Congestion: A Measure of Display Clutter"
description: A color-and-contrast congestion model correlates strongly with 20 observers' clutter rankings of 25 maps, but subjective agreement does not establish task-performance improvements or generalize to text-heavy interfaces.
resource: https://doi.org/10.1145/1054972.1055078
source: https://doi.org/10.1145/1054972.1055078
tags: [visual-perception, attention, layout, color, data-visualization, digital-interfaces]
timestamp: 2026-10-14T21:31:24Z
---

# Feature Congestion and Display Clutter — Study Notes

**Authors**: Ruth Rosenholtz, Yuanzhen Li, Jonathan Mansfield, and Zhenlan Jin.  
**Published**: CHI 2005, April 2–7, Portland, Oregon; DOI 10.1145/1054972.1055078 confirmed by Crossref.  
**Status**: Peer-reviewed computational model and subjective map-ranking study. Read the complete ten-page supplied paper, all four figures, and references.

## What It Is

A proposal to measure visual clutter through **local variability in perceptually important features**, rather than simply counting visible objects. A region is feature-congested when its existing variety leaves little room to introduce a new visually salient item. The implemented model uses color and luminance contrast; orientation and motion are discussed as future extensions, not measured components.

## Problem and Motivation

Removing information can reduce search difficulty while increasing navigation and memory costs because necessary information must be fetched elsewhere. The authors define clutter broadly as excess items, representation, or organization causing performance degradation at a task. Task and expertise therefore matter: a familiar map can be easier to search than an unfamiliar one with the same marks.

The feature-congestion measure is a narrower first approximation, motivated by visual search. It is not a full account of crowding, occlusion, memory demands, semantic grouping, aesthetics, or all task performance.

## Model as an Idea

A target is salient when its features are unusual relative to the surrounding feature distribution. Difference from the local mean is evaluated relative to local variability: a color that stands out among homogeneous surroundings may become ordinary in a multicolored region. A large local distribution occupies more of the available feature space, making additional distinctive signals harder to introduce.

The model estimates local color covariance and contrast variability at several scales, then combines them into local congestion and an overall display score. Grouping similar features into separate regions can leave usable local distinctions even when total object count stays unchanged. Conversely, many unrelated colors or contrast patterns compete for attention.

This differs from simply averaging every pixel's salience. A nearly blank map has a nonsalient background but is not consequently highly cluttered; a uniform set of identical objects and a heterogeneous set can both lack a unique target while differing greatly in congestion. Feature congestion asks about the **capacity for a new distinguishing signal**, not whether each existing element is already an outlier.

## Study Design

**Twenty campus-recruited observers, ages 10–48**, ranked **25 maps** gathered from the web: **nine US maps, six Bay Area maps, three whole-San-Francisco maps, and seven maps of portions of the city**. Each was printed in full color on **8½ × 11-inch paper**, scaled to fill the page width. Observers received maps in randomized order and physically ordered them by perceived clutter.

No definition of clutter was supplied; observers used their own intuitive meaning. No geographic-knowledge assessment, task-specific target search, response-time measure, or accuracy outcome is reported. Although the model is intended for interfaces and visualizations, this validation used printed maps, not interactive software tasks.

## Results / Admissions

- **Observer agreement:** Kendall's **W = .72**, **χ²(24) = 345.3, p < .001**. Mean pairwise Spearman correlation was **.70**. Thus there was substantial consensus, not unanimity.
- **Model agreement:** Spearman correlation with **average observer rankings was .83, p < .001**. This is a rank association across 25 maps, not 83% prediction accuracy or an effect on user performance. Figure 2 separately plots **median** ranks and interquartile ranges.
- **Disagreement was informative:** some observers treated familiarity with a city's location as reducing clutter. For a text-separated map, some saw cleaner graphics while others anticipated slower reading from the separation. On a text-heavy map, people disagreed on the tradeoff between few colors and many labels.
- **Weak cases:** the model performed worst on maps **23 and 24**, with much text and little color variation. The authors suggest an explicit text feature or different weighting may be needed. It handles visual similarity and proximity, not heading semantics or meaningful text-group structure.
- **Design demonstration:** Figure 4 adds colored symbols at relatively low-congestion locations using local feature statistics. The symbols appear plausible to the authors, but no experiment measures whether these additions improve detection or comprehension.

The authors explicitly call task-performance comparisons and validation on non-map displays future work. Their claim that .83 is comparable with human agreement does not prove an upper performance ceiling: correlation with an average of observers and mean pairwise correlations are different comparisons.

## Analyst Takeaways

1. **Clutter is not an item-count synonym.** Which features vary, where they vary, and how a task uses them matter; removing information is not automatically the best intervention.
2. **Protect local signal capacity.** A new alert cannot be assumed salient because its color is distinctive in isolation; evaluate it against its actual neighborhood.
3. **Separate perceived complexity from effectiveness.** Ranking agreement supports the model as a perceptual diagnostic, not an optimal information density or verified search-performance predictor.
4. **Use grouping with a task model.** Visually homogeneous regions can reduce congestion, but useful hierarchical search also requires meaningful organization that this image-based model does not understand.

## Questions and Limitations

- One small map collection and a mixed-age campus sample; no reported independent replication, confidence interval for the model correlation, held-out validation set, or controlled manipulation of clutter.
- Printed maps omit interaction, scrolling, dynamic alerts, and motion. Text-heavy interfaces are an admitted model weakness; it should not be treated as a universal dashboard-quality score.
- The introduction's broad performance-based definition is not the measured outcome: the experiment validates subjective clutter rankings, and the design examples are illustrations rather than efficacy tests.
- **Internal notation inconsistency:** the displayed saliency equation is a squared Mahalanobis-distance form, but the explanatory prose assigns saliency **n** to an **nσ** ellipsoid, which would correspond to the unsquared distance. Do not carry that exact numerical mapping into a reusable design rule.
- **Redistribution evidence**: the first-page ACM notice permits personal/classroom copies but says other copying, republication, server posting, or redistribution requires prior permission and/or a fee. No explicit public redistribution grant appears; keep this PDF private.

## Vault Ideas Extracted

- [Visual Complexity and Prototypicality](/vault/visual-complexity-and-prototypicality.md) — Adds a .83 model–human rank correlation for map clutter while separating local feature variability from object count and subjective clutter from task effectiveness.
- [Preattentive Features](/vault/preattentive-features.md) — Explains salience relative to local feature distributions and shows why heterogeneous surroundings consume the capacity for a new attention-drawing signal.
