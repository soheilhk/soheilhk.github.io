---
title: "Temporal Data Subset Stability (T-DSS) for Artifact Reduction in Multi-Frame PACT"
publications:
  - Conf_SPIE_MI2027_Hakakzadeh_et_al_TDSS_PACT
collection: research
category: pat
date: 2027-01-01
venue: "Ring-Array / Sparse Array & Artifact Suppression"
excerpt: "A non-iterative Temporal Data Subset Stability (T-DSS) framework for dynamic multi-frame PACT that leverages pixel-wise temporal consistency across frame lags to eliminate sparse-sampling streak artifacts while preserving delicate microvascular structures (achieving gCNR = 0.74 vs. DARPIC = 0.45 and DAS = 0.65)."
image: "images/research/pat/pat4.PNG"
image_caption: ""
expanded: true
---


### Overview & Motivation

Photoacoustic computed tomography (PACT) combines optical contrast with acoustic spatial resolution. However, hardware restrictions and high frame-rate acquisition demands often lead to sparse detector sampling, which inevitably introduces strong streak artifacts that degrade image contrast and obscure real absorbers.

While dynamic multi-frame acquisitions provide temporal redundancy, existing state-of-the-art temporal weighting techniques (such as DARPIC) rely on aggressive nonlinear transformations and phase-aware clustering. These methods often over-penalize subtle intensity variations caused by physiological micro-motion, inadvertently suppressing or distorting weak, microvascular structures.

To overcome these limitations, we introduce **Temporal Data Subset Stability (T-DSS)**. Extending our spatial subset stability principles (RDP/DSS) strictly into the temporal axis, T-DSS evaluates pixel-wise temporal similarity across registered dynamic frames. It differentiates physically stable optical absorbers from dynamically fluctuating acoustic streak artifacts without iterative regularization or over-filtering microvessels.

---

### Key Technical Details & Formulation

- **Frame Registration & High-SNR Summed Baseline:**
  - Individual frames in a dynamic sequence of length $N$ are reconstructed via Delay-and-Sum (DAS): $F(\mathbf{r}, t)$, where $\mathbf{r}$ denotes spatial location and $t$ is the frame index.
  - Motion registration aligns consecutive frames, and the baseline composite is generated:
    $$
    p_0^{\mathrm{full}}(\mathbf{r}) = \sum_{t=1}^{N} F(\mathbf{r}, t).
    $$

- **Pixel-Wise Temporal Similarity Across Multi-Lag Subsets:**
  - Dynamic sequences are partitioned into temporal subsets separated by frame lags $\tau \in [1, 10]$ to capture artifact fluctuations induced by physiological micro-motion.
  - The normalized temporal similarity between a frame at time $t$ and delayed frame $t+\tau$ is defined as:
    $$
    S_{t, \tau}(\mathbf{r}) = \frac{F(\mathbf{r}, t) \cdot F(\mathbf{r}, t+\tau)}{\max_{\mathbf{r}} \left[ F(\mathbf{r}, t) \cdot F(\mathbf{r}, t+\tau) \right]}.
    $$

- **Coefficient of Variation (CV) Metric:**
  - For $K$ evaluated frame pairs across the temporal subsets, the mean $\mu_S(\mathbf{r})$ and standard deviation $\sigma_S(\mathbf{r})$ of similarity are computed:
    $$
    \mu_S(\mathbf{r}) = \frac{1}{K} \sum_{t, \tau} S_{t, \tau}(\mathbf{r}), \quad \sigma_S(\mathbf{r}) = \sqrt{\frac{1}{K} \sum_{t, \tau} \left[ S_{t, \tau}(\mathbf{r}) - \mu_S(\mathbf{r}) \right]^2}.
    $$
  - The stability metric is quantified using the Coefficient of Variation:
    $$
    \mathrm{CV}(\mathbf{r}) = \frac{\mu_S(\mathbf{r})}{\sigma_S(\mathbf{r})}.
    $$
  - High $\mathrm{CV}(\mathbf{r})$ signifies physically consistent absorbers; low $\mathrm{CV}(\mathbf{r})$ denotes fluctuating streak artifacts.

- **Weight Map Generation & Reconstructed Composite:**
  - A spatial median filter removes isolated noise spikes from the CV map.
  - Percentile-based segmentation generates the binary stability selector mask $\hat{S}(\mathbf{r}) \in \{0, 1\}$.
  - The final artifact-free composite is obtained via direct pixel-wise masking:
    $$
    p_0^{\mathrm{final}}(\mathbf{r}) = \hat{S}(\mathbf{r}) \cdot p_0^{\mathrm{full}}(\mathbf{r}).
    $$

---

### In Vivo Validation & Quantitative Benchmarks

The method was validated on an open-access *in vivo* dataset of an anesthetized mouse upper abdomen acquired using a 256-element full-ring transducer array at 20 Hz (600 dynamic frames).

| Method | Generalized CNR (gCNR) | Background Artifacts | Fine Microvasculature Retention |
|:---|:---:|:---:|:---:|
| **Summed DAS Baseline** | 0.65 | Severe streaks present | Preserved (buried in noise) |
| **DARPIC (State-of-the-Art)** | 0.45 | Suppressed | Over-penalized / Dimmed / Erased |
| **Proposed T-DSS** | **0.74** | **Completely Removed** | **Fully Preserved & Continuous** |

- **Contrast Enhancement:** T-DSS achieves a **gCNR of 0.74**, substantially higher than both the DAS baseline ($0.65$) and DARPIC ($0.45$).
- **Microvascular Preservation:** Unlike DARPIC, which drops contrast due to structural over-penalization, T-DSS avoids threshold degradation and maintains complete topological continuity of capillary branches.

---

### Key Innovations & Highlights

- **Temporal Stability Paradigm:** Extends subarray/inconsistency analysis into the temporal dimension, exploiting micro-motion variations to separate stationary absorbers from non-stationary acoustic streaks.
- **Non-Iterative & Direct:** Eliminates the heavy computational overhead of model-based inversion and deep learning training pipelines while outperforming nonlinear filters.
- **Preservation of Weak Absorbers:** Protects low-intensity vascular signals and subtle structural boundaries from erasure.
- **Broad Compatibility:** Directly applicable to multi-frame dynamic sequences in preclinical small-animal tomography and clinical functional PACT systems.
