---
title: "Adapted Reconstruction Frameworks and Coherent Weighting for Circular PACT"
publications:
  - Conf_IEEE_ICEE2022_Hakakzadeh_et_al_FADAS
  - Conf_IEEE_ICBME2021_Hakakzadeh_et_al_ACF
collection: research
category: pat
date: 2022-12-01
venue: "Ring-Array / Sparse Array & Artifact Suppression"
excerpt: "Overcoming the Nyquist-sampling bottleneck in circular PACT via a novel spatial-domain factor, combining edge-detection and statistical filtering to mitigate streak artifacts in low-cost, sparse-detector architectures."
image: "images/research/pat/pat4.PNG"
image_caption: "Figure 1:   The experimental results of the leaf phantom. (b1-b3) are the recon
structed image with the conventional back-projection method. (c1-c3) are the
reconstructed image with the proposed method. (d) and (e) are the reconstructed
image with the CTBP and interpolation method, respectively. In (b-e) NSS is
the number of spatial samples used in the experimental study"
expanded: true
---

**Key Technical Details & Innovations:**
- **Spatial-Domain Artifact Suppression:** Introduces a novel "Artifact Removal Factor"—a synergistic filter combination utilizing edge-detection operators and standard deviation analysis applied directly to back-projected signal data.
- **Sparse-Sampling Efficiency:** Successfully addresses the "Nyquist-limit" challenge in circular PACT. Demonstrates that high-fidelity reconstruction can be maintained even when reducing the transducer count to **$1/5$th** of the conventional Nyquist-required density (e.g., from 1200 down to 240 elements).
- **Clinical Translation Potential:** By enabling high-quality imaging with significantly fewer detectors, this framework lowers the hardware cost and computational barrier for clinical PACT systems without sacrificing structural visibility.
- **Quantitative Performance Benchmarks:**
  - **Structural Integrity:** Achieves **$>100\%$ improvement** in $\text{SSIM}$ (reaching values up to $0.94$).
  - **Contrast Fidelity:** Significant gains in image quality metrics, with $\text{gCNR}$ reaching $\sim 0.85$ and $\text{CNR}$ enhancements of up to **$38.6\text{ dB}$**.
  - **Spatial Resolution:** Demonstrates a **$\sim 45\%$ improvement** in tangential resolution compared to conventional sparse-sampling back-projection methods.
