---
type: Study Note
title: A visual model for predicting chromatic banding artifacts
description: Nine-observer VR measurements support a luminance-and-chrominance model of gradient banding, but its fitted thresholds are device-limited and are not independent validation of arbitrary image quality.
resource: https://doi.org/10.2352/ISSN.2470-1173.2019.12.HVEI-212
source: https://doi.org/10.2352/ISSN.2470-1173.2019.12.HVEI-212
tags: [color, visual-perception, human-performance, digital-interfaces]
timestamp: 2026-10-14T21:31:24Z
---

# Chromatic Banding and Visual Sensitivity — Study Notes

**Authors**: Gyorgy Denes, George Ash, Huameng Fang, and Rafał K. Mantiuk.  
**Published**: IS&T Electronic Imaging, Human Vision and Electronic Imaging, January 13, 2019; DOI confirmed by Crossref and the publisher.  
**Status**: Peer-reviewed proceedings research with psychophysical measurements and a fitted perceptual model. Read the complete seven-page supplied manuscript, all ten figures, table, and references; the publisher lists the version of record as pages 212-1–212-8.

## What It Is

A model of when quantizing a smooth color gradient produces visible false contours. Instead of assuming equal numerical errors are equally noticeable, it combines the spatial frequency of quantization error with sensitivity to luminance and two opponent-color signals. Its output is a detection probability, used to estimate the bit depth at a just-noticeable threshold.

## Problem and Motivation

Banding is especially conspicuous in low-texture regions such as sky, water, and skin. An encoding appropriate for wide-gamut or HDR imagery needs not only a wide numerical range but reasonably uniform perceptual use of its available precision. The paper argues that PSNR and SSIM do not capture the relevant perception, while the cited luminance-only visual difference models miss purely chromatic error.

## Model as an Idea

A quantized gradient differs from its smooth original by an approximately sawtooth error signal. The model considers its frequency components and weights each by the visual system's contrast sensitivity under the relevant background luminance and angular resolution. It combines detection probabilities across frequencies and, in the chromatic extension, across luminance, red–green, and yellow-green–violet channels.

This makes visibility depend on **where the color difference occurs, its spatial structure, adaptation luminance, and viewing geometry**, rather than only a color-distance scalar. The paper deliberately excludes contrast masking: its target is the worst-case smooth gradient, not a prediction that every natural textured image will exhibit equally visible error. The chromatic sensitivity function is fitted to prior measurements, with an additional cone-contrast parameter fitted to the new experiment.

## Study Design and Evidence

### Experiment 1: luminance quantization

**Nine paid observers, ages 19–45**, had normal or corrected-to-normal color vision. They used a Huawei Mate Pro 9 in a DayDream VR headset in a dark room. The calibrated display peaked at **44 cd/m²**; each gradient square subtended **20 visual degrees**, with a surrounding virtual wall matched to its mean color. Two minutes of adaptation preceded testing, and luminance conditions ran darkest to brightest.

Observers selected the one quantized gradient among **four squares**, with its location randomized. An adaptive QUEST procedure used **30 trials** to estimate each threshold; response time was unrestricted and head movement permitted. Gradients varied in contrast from zero to full contrast, across **seven chromaticities** and **three mean-luminance levels per chromaticity**, comparing PQ and sRGB transfer functions. Spatiotemporal dithering supported quantization levels beyond the native display depth.

Lower luminance required more bits. PQ showed less variation in bit-depth requirements across luminance than sRGB. Figure 6 shows fitted predictions within the reported error bars for all conditions; the prose reports PSNR-fitting errors **an order of magnitude greater** than this model, but supplies no complete numerical error table or uncertainty for that ratio. This is a comparison on the fitting dataset, not an independently held-out prediction test.

### Experiment 2: chromatic quantization

The setup and procedure were stated to be identical to Experiment 1; no separate participant count or new cohort is reported. Equiluminant gradients followed **two orthogonal chromatic directions** through the display white point in CIE L′u′v′, bounded by the display gamut, at **three fixed luminance levels**. Quantization compared **Y′CbCr and ICtCp**, labeled ITP in the figures.

The authors report that required depth changed little with luminance or chromatic direction within each encoding, while **ICtCp consistently required fewer bits than Y′CbCr**. The fitted cone-contrast parameter was approximately **two-thirds**; Figure 9 places predictions within the observed **95% confidence intervals**. The paper does not tabulate exact threshold differences or provide inferential tests for the encoding comparison, so the figure should not become a universal bit-saving guarantee.

### Color-uniformity interpretation

Figure 10 compares model-derived discrimination ellipses with CIE DeltaE 2000 and MacAdam ellipses at several luminances. Their similar shapes are suggestive, but banding detection and isolated color-patch discrimination are different tasks. MacAdam ellipses in the comparison were measured at **48 cd/m²** only; the paper's other luminance panels are model predictions, not new observer validation across that full range.

## Analyst Takeaways

1. **Perceptual uniformity is conditional.** Equal color-space steps need not produce equal gradient visibility once luminance, angular scale, and quantization interact.
2. **Smooth gradients are a stress case.** A successful textured-image metric can still miss false contours; assess the low-texture content where precision failures become visible.
3. **Keep fitting separate from validation.** Predictions inside error bars demonstrate agreement with the data used to tune parameters, not independent generalization.
4. **Do not infer chart-reading accuracy.** This study concerns visible encoding artifacts, not whether a palette preserves data ordering, semantic distinctions, or accessible status interpretation.

## Questions and Limitations

- The small sample and single low-peak-luminance VR device constrain generalization to modern HDR displays, ordinary monitors, different angular resolutions, and sustained viewing. No independent replication is established in this source.
- Darkest-to-brightest ordering is purposeful but not counterbalanced; exposure duration is self-paced. The study does not isolate order, adaptation, or eye movement effects.
- Masking is excluded, and the model is not a complete image-quality predictor. It cannot establish equal annoyance, preference, or task performance at equal detection probabilities.
- The supplied file has **seven pages**, whereas the publisher records **eight** for the version of record; preserve the manuscript identity rather than claim this is that exact published layout. No conflicting numerical result was identified in the supplied text.
- **Redistribution evidence**: no explicit redistribution grant appears in the supplied manuscript; the [publisher record](https://library.imaging.org/ei/articles/31/12/art00006) states “Copyright © Society for Imaging Science and Technology 2019.” Public availability is not a reuse licence; archive this copy privately.

## Vault Ideas Extracted

- [Perceptually Uniform Color Scales](/vault/perceptually-uniform-color-scales.md) — Adds a nine-observer gradient-banding model showing why uniformity depends on luminance, spatial structure, encoding, and device conditions rather than numerical color distance alone.
