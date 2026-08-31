---
title: "Adapted Reconstruction Frameworks and Coherent Weighting for Circular PACT"
publications:
  - Conf_IEEE_ICEE2022_Hakakzadeh_et_al_FADAS
  - Conf_IEEE_ICBME2021_Hakakzadeh_et_al_ACF
collection: research
category: pat
date: 2022-01-01
venue: "Ring-Array / Reconstruction Research"
excerpt: "A comprehensive reconstruction and weighting framework for circular PACT, integrating Adapted Coherent Factor (ACF) with Fast Adapted Delay-and-Sum (ADAS/F-ADAS) algorithms to achieve superior resolution, contrast enhancement, and edge uniformity."
image: "images/research/pat/pat3.PNG"
image_caption: "Figure 1:  Numerical results of the reconstructed image. (a) Initial Derenzo phantom. (b, c) are reconstructed images with UBP and DAS, respectively. zoomed areas of dashed lines in (a, b, c) are shown in (d, e, f, g, h, i), respectively. (j, k, l) are reconstructed images with DAS+TGC, ADAS, and F-ADAS, respectively, and indicated dashed lines are shown in (m, n, o, p, q, r), respectively."
expanded: true
---

**Key Technical Details & Innovations:**
- **Adapted Coherent Factor (ACF):** Introduces a post-reconstruction coherent weighting strategy applied to conventional algorithms (UBP and ADAS). It leverages spatial coherence to suppress side-lobes and background noise, significantly boosting image contrast.
- **Fast Adapted Algorithms (ADAS & F-ADAS):** Develops a high-efficiency algorithmic suite consisting of "Fast Adapted Delay and Sum" (ADAS) and "Filtered Adapted Delay and Sum" (F-ADAS), designed to accommodate different hardware constraints (infinite vs. finite transducer bandwidth).
- **Edge Uniformity Index (EUI):** Proposes a novel quantitative metric to evaluate reconstruction uniformity. EUI provides a standardized way to measure the homogeneity of the reconstructed field, specifically targeting artifact-induced distortions in circular scan geometries.
- **Quantitative Performance Benchmarks:**
  - **Resolution & Contrast:** ACF implementation delivers a **$16\%–20\%$ improvement** in PSF Full-Width at Half-Maximum (FWHM) and a **$13.7–30.2\text{ dB}$ gain** in Contrast Ratio (CR).
  - **Edge Uniformity:** ADAS/F-ADAS algorithms show **$17\%–39\%$ improvement** in EUI for ideal scenarios, while achieving near-perfect uniformity ($\text{EUI} \approx 1$) in bandwidth-limited experimental conditions.
  - **Robustness:** Validated across varying SNR levels ($20\text{ dB}–80\text{ dB}$) and diverse bandwidth profiles, ensuring stability for both simulated and practical scanner configurations.
