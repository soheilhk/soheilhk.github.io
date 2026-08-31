---
title: "Physics-Based Transmit Sparsification Criterion for High-Frame-Rate Ring-Array RUCT"
publications:
  - Conf_IEEE_IUS2026_Hakakzadeh_et_al_MinTx
collection: research
category: usct
date: 2026-09-01
venue: "Ring-Array / Beamforming"
excerpt: "Deriving an analytical transmit sparsification bound for ring-array USCT based on Rayleigh scattering and transducer directivity, optimizing frame rates while avoiding off-center resolution degradation in phantom and in-vivo scans."
image: "images/research/usct/usct10.PNG"
image_caption:
expanded: true
---

**Key Technical Details & Innovations:**
- **Physics-Based Sampling Criterion:** Establishes the analytical minimum bound for transmit events ($N_{Tx}$) needed in full-view ring-array RUCT, eliminating over-sampling redundancies without compromising image quality.
- **Acoustic Interaction Modeling:** Couples Rayleigh-regime tissue scattering profiles ($\theta_s$) with element directivity angles ($\theta_D$) and the region-of-interest radius ratio ($R_{ROI}/R$) to define an effective acoustic scattering sector width ($\theta_{eff}$).
- **Ultrafast Frame-Rate (FR) Enabler:** Enables substantial transmit sparsification, significantly reducing data acquisition time and computational overhead for real-time and dynamic *in-vivo* preclinical/clinical USCT.
- **Experimental & In-Vivo Validation (512-element Ring Array, $5\text{ MHz}$, $R=4\text{ cm}$):**
  - **Phantom Study ($R_{ROI}/R = 0.5$):** Accurately predicts the lower threshold of $N_{Tx} \approx 32$ transmits required to preserve fine boundary targets without peripheral degradation.
  - **Preclinical In-Vivo Study ($R_{ROI}/R = 0.25$):** Confirms structural preservation down to only $N_{Tx} \approx 16$ transmits on *in-vivo* rat cross-sections.
  - **Spatial Degradation Profiling:** Demonstrates that sub-threshold sparsification predominantly degrades resolution in off-center regions, confirming the spatial validity of the angular coverage model.
