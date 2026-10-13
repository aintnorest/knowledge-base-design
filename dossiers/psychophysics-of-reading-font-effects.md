---
type: Study Note
title: "Psychophysics of reading. XV: Font effects in normal and low vision"
description: A printed-chart study of 50 normally sighted and 42 low-vision readers finds Courier-Bold supports smaller readable text than Times-Roman, while maximum-speed advantages differ by vision group and cannot be attributed to monospacing alone.
resource: https://iovs.arvojournals.org/article.aspx?articleid=2161324
source: https://iovs.arvojournals.org/article.aspx?articleid=2161324
tags: [typography, low-vision, accessibility, visual-perception, human-performance]
timestamp: 2026-10-12T20:28:10Z
---

# Psychophysics of Reading: Font Effects — Study Notes

**Authors**: J. Stephen Mansfield, Gordon E. Legge, and Mark C. Bane.  
**Published**: Investigative Ophthalmology & Visual Science **37(8), July 1996, pp. 1492–1501**; accepted March 11, 1996.  
**Status**: Peer-reviewed empirical journal article. Read the supplied lab-hosted copy of the ten-page published article, including seven figures, participant table, and analysis appendix; its download footer is dated January 7, 2019. Issue and pagination agree with PubMed **8675391**.  

## What It Is

A comparison of **Times-Roman and Courier-Bold** on continuous-text MNREAD acuity charts, separating three outcomes that a generic claim of “readability” can obscure:

- **Reading acuity**: smallest print that can just be read.
- **Critical print size**: smallest print supporting the reader's maximum speed.
- **Maximum reading speed**: speed when print size is no longer the limiting factor.

The durable finding is that font choice matters differently near the visual threshold and on the reading-speed plateau. A small change in the smallest readable size can accompany a much larger speed difference when print is already below the critical size.

## Problem and Motivation

Font effects matter both for everyday reading and for clinical assessment or selection of magnification aids. Earlier findings about fixed-width versus proportional spacing disagreed; low-resolution renderings and whether tests reached below critical print size could help explain those disagreements. Readers with central field loss may also experience stronger peripheral crowding, making compressed text particularly difficult. That mechanism motivated the comparison but was not isolated by it.

## Mechanism as an Idea

**50 undergraduate psychology students** with normal or corrected-to-normal vision and **42 low-vision participants**, all native English speakers, read progressively smaller chart sentences aloud as quickly and accurately as possible. Low-vision recruitment covered two sites: **22 Minnesota** participants and **20 Texas** participants. Table 1 lists **13** with intact central vision and **29** with central field loss. The former averaged **41 ± 11.2 years**, the latter **68 ± 15.4 years**; average distance acuities were **0.87 ± 0.52** and **0.85 ± 0.35 logMAR** respectively. Diagnoses were heterogeneous in Minnesota; all Texas participants had age-related macular degeneration and central loss.

The comparison used high-contrast **black text on white paper**, **90% Michelson contrast**, printed at **3,000 dpi** and viewed under reflected luminance of at least **80 cd/m²**. Normal-vision viewing distance was **40 cm**; low-vision distance was individualized using customary correction. Each chart had **19 sentence sizes** separated by **0.1 logMAR**, ranging from **1.3 to −0.5 logMAR** at 40 cm. Size was matched by **lowercase x-height**, not point size.

The font manipulation was bundled: **Times-Roman** was proportionally spaced, while **Courier-Bold** was fixed-width, wider, and differently weighted and shaped. Figure 1 also shows different chart arrangements: Times sentences had **60 characters across three justified lines**; Courier sentences had **56 characters across four lines**. Standardized six-character words were used to calculate error-adjusted reading speed and acuity, reducing but not erasing differences in layout and sentence format.

Maximum speed was the geometric mean across an estimated plateau; critical size was the smallest size included in that plateau. Figure 2 illustrates why a fitted two-line elbow can move substantially after changing one near-threshold observation. The appendix instead selects a high-speed contiguous region separated from outside observations by a variability-dependent margin. These definitions are measurement choices, not biological discontinuities.

## Results / Admissions

| Outcome | Normal vision | Low vision |
|---|---|---|
| Reading acuity: Times requires larger print than Courier | **0.05 logMAR**, about **12%**, paired test **df = 49, p < .001** | **0.09 logMAR**, about **23%**, **df = 41, p < .001** |
| Critical print size: Times requires larger print | **0.06 logMAR**, about **15%, p < .001** | **0.06 logMAR**, about **15%, p < .002** |
| Maximum speed | Times **4.7% faster, p < .001** | Times **10% slower, p < .05** |

For low-vision readers, Courier's acuity advantage was **0.08 logMAR** with intact central vision and **0.10** with central loss, both **p < .001**. Critical-size differences were **0.04 logMAR, p = .06** for intact central vision and **0.07 logMAR, p < .01** for central loss. Both subgroups showed approximately **10% slower maximum speed with Times**.

Below critical print size, the effects were larger than the plateau-speed differences. Figure 6 normalizes size to each person's Courier critical size. At **−0.3 logMAR relative size**, normal readers' mean Times/Courier speed ratio was approximately **0.5**: Times was read half as fast. The low-vision plot also shows substantial Courier advantages below critical size, alongside wide individual variability. This is not a claim that Courier doubles reading speed at ordinary sizes.

The source stresses that suitably enlarged text yields only slight font-dependent differences. Courier also occupied approximately **40% greater mean character width** when matched for x-height. The authors therefore caution that its speed advantage can carry a substantial page-count cost.

The findings resemble earlier small-print results by Arditi and colleagues but conflict with Morris and colleagues' null result. The authors suggest Morris did not test below participants' critical print sizes. Because the fonts and methods differ, this is contextual corroboration and a proposed explanation of disagreement, not a clean replication of isolated monospacing.

## Analyst Takeaways

1. **Distinguish barely readable from efficiently readable.** Acuity alone underestimates the size needed to support maximum speed. Designing small labels around detection thresholds can sacrifice substantial performance.
2. **Do not convert Courier-Bold versus Times-Roman into “monospace is better.”** Weight, width, letterforms, serifs, line count, and spacing all differ. The experiment cannot identify which of those differences caused the advantage.
3. **Treat enlargement and font choice as interacting accommodations.** The practical importance of a font advantage depends on whether readers can reach the speed plateau through magnification or resizing.
4. **Account for spatial cost.** Wider text can help discrimination while consuming more reading area. The study measures chart reading, not the net value of fitting fewer UI labels or navigating more screens.
5. **Contrast is not a complete legibility model.** Font-dependent differences persisted in high-contrast print matched by x-height. This complements [Color Contrast Minimum](/vault/color-contrast-minimum.md), without testing or deriving a WCAG threshold.

## Questions and Limitations

- The study uses printed, high-resolution black-on-white charts, not a dark UI, rasterized micro-labels, code reading, or stylized display fonts. It contains no polarity manipulation and no basis for a dark-mode recommendation.
- Site-specific timing differs: Minnesota includes time from sentence reveal, whereas Texas begins timing at the first utterance and excludes initial localization. Site, age, diagnosis, and central-field status are partly confounded. Between-subgroup differences should not be assigned uniquely to central loss.
- The article does not report a chart-order counterbalancing procedure or font-blinded assessment. Normal-reader age details, confidence intervals, and exact t statistics are not provided.
- **Internal numerical inconsistency**: the discussion says the central-loss critical-size effect is **0.06 logMAR greater** than the intact effect, but the reported subgroup estimates are **0.07 and 0.04**, a difference of **0.03**. Figure 7 agrees with the latter pair. Also, “Times 10% slower than Courier” and the conclusion's “Courier 10% faster than Times” use different denominators; the latter is an approximate restatement, not an exact conversion.
- **Identifier evidence**: no DOI appears in the PDF or the retrieved PubMed record. Broad Crossref bibliographic lookup and a title/author query restricted to 1996 did not identify a matching DOI. The publisher URL is independently indexed under the exact title; direct reader and curl retrieval returned **403**, with curl retaining that final HTTPS URL. No publisher canonical-link element could therefore be inspected. The source key uses the normalized publisher URL, retaining its essential `articleid` query, rather than inventing a DOI or claiming definitive proof that none exists.
- **Redistribution evidence**: the first page states **“Copyright © Association for Research in Vision and Ophthalmology.”** No explicit redistribution grant appears. The lab-hosted copy belongs in `archive/private/`, not a public raw-source archive.

## Vault Ideas Extracted

- [Typeface Legibility](/vault/typeface-legibility.md) — Separates acuity, critical size, and plateau speed, with paired normal/low-vision evidence and explicit limits on attributing a two-family comparison to monospacing.
- [Color Contrast Minimum](/vault/color-contrast-minimum.md) — Demonstrates font-dependent performance at high print contrast, supporting the boundary that contrast alone does not establish efficient reading.
