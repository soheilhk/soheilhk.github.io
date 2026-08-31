---
title: "Randomized Detection Points & Artifact Score Matrix for Sparse Circular PACT"
publications:
  - Paper_Journal_J._Phys._Photonics_2025_Hakakzadeh_et_al
  - Conf_IEEE_IUS2023_Hakakzadeh_et_al_Coherent
collection: research
category: pat
date: 2024-01-01
venue: "Ring-Array / Sparse Array & Artifact Suppression"
excerpt: "A randomized detection point (DP) framework for sparse circular PACT that constructs an Artifact Score Matrix (ASM) from multiple low-resolution sub-images, achieving a 20 dB SNR gain, 25% SSIM boost, and a 50× reduction in streak artifact variance across phantom and in-vivo rat brain imaging."
image: "images/research/pat/pat5.PNG"
image_caption: "Figure 1:   (a1)–(a8) Show an example of reconstructed PACT images of triangle target obtained with 60 DPs in different positions. (b1)–(b5) are the results the triangle target with various numbers of LRIs: 0, 5, 50, 500, and 5 k, respectively. The STD values of pixels within the white boxes in (b1)–(b5) are shown as a bar chart in (b6). (c1/d1–c5/d5) show the reconstructed images of the lab-made triangle/complex leaf targets with 500 DPs obtained with different reconstruction methods. The scale bar in (c), (d) is 1 cm. (e1)–(e5) are cross-sectional reconstructed PACT images of the rat brain obtained with different reconstruction methods. The scale bar in (e) is 1 cm. (c6), (e6) are photographs of the triangle and complex leaf targets, respectively. (e6) is a 3D schematic of rat brain vasculature atlas."
expanded: true
---

**Key Technical Details & Innovations:**
- **Randomized Detection Point Sub-Sampling:** Subdivides sparse acoustic detection positions into randomized subsets to generate multiple, statistically uncorrelated low-resolution images (LRIs), breaking the spatial coherence of aliasing streaks.
- **Artifact Score Matrix (ASM):** Formulates a spatial weighting matrix derived across the randomized LRIs that explicitly identifies, scores, and cancels streak artifact locations while preserving true optical absorbers.
- **Hardware-Agnostic Acceleration:** Enables drastic reductions in required A-line density (detector/projection count), drastically lowering hardware cost and acquisition time for circular scan architectures.
- **Comprehensive Multi-Tier Validation:**
  - **Numerical:** Two complex microvascular phantoms and a high-resolution human brain model.
  - **Experimental:** Triangle wire/absorber phantom and fine-structure complex leaf phantom.
  - **In-Vivo:** Preclinical *in-vivo* rat brain imaging verifying high-fidelity vascular reconstruction.
- **Quantitative Performance Benchmarks:**
  - **SNR Gain:** **$+20\text{ dB}$ increase** in Signal-to-Noise Ratio over standard back-projection.
  - **Structural Integrity:** **$+25\%$ enhancement** in Structural Similarity Index ($\text{SSIM}$).
  - **Artifact Variance:** Delivers an **artifact standard deviation that is $50\times$ lower** ($\sim 98\%$ reduction in streak variance) compared to conventional sparse reconstruction.
