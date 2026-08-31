---
title: "Phased-Array Transmit Compounding for Ring-Array RUCT Systems"
publications:
  - Conf_SPIE_MI2027_Hakakzadeh_et_al_SLCarotid
collection: research
category: sono
date: 2027-01-01
venue: "Linear-Array / Beamforming, Clutter Suppression"
excerpt: "An adaptive Data-Subset Stability (DSS) beamforming weighting framework for 64-channel carotid ultrasound, suppressing incoherent clutter and enhancing vascular lumen-wall contrast."
image: "images/research/sono/sono11.PNG"
image_caption: "Representative carotid ultrasound images obtained using (a) conventional DAS, (b) DAS-CF, (c) DMAS, (d) 
SLSC and (e) the proposed Channel-Based DSS processing with lags 1 and 2. The proposed method reduces residual 
signals within anechoic regions while improving the conspicuity of hyperechoic structures. The dynamic range is 60 dB 
across (a, b, c, e) images."
expanded: true
---


### Key Technical Details & Methodology

- **Receive-Channel RF Signal Preservation:**
  - Raw radiofrequency (RF) data is collected from a $64$-channel linear transducer array. Standard geometric focusing delays $\tau_i(\mathbf{r})$ are computed for each pixel $\mathbf{r}$, preserving the pre-summation delayed receive-channel signal matrix:
    $$\mathbf{S}(\mathbf{r}) = \left[ s_1(\mathbf{r}), s_2(\mathbf{r}), \dots, s_N(\mathbf{r}) \right]^T$$
- **Inter-Channel Correlation Stability Across Spatial Lags:**
  - Normalized inter-channel cross-correlations are evaluated across multiple spatial channel-pair subsets and lag separations:
    $$R_{i,j}(\mathbf{r}) = \frac{\sum_k s_i(t_k, \mathbf{r}) s_j(t_k, \mathbf{r})}{\sqrt{\sum_k s_i^2(t_k, \mathbf{r})} \sqrt{\sum_k s_j^2(t_k, \mathbf{r})}}$$
  - The statistical variance/stability across these data subsets distinguishes coherent specular reflections (vessel wall) from incoherent diffuse noise (lumen clutter).
- **Adaptive DSS Weighting Factor Map ($W_{\text{DSS}}$):**
  - A pixel-wise stability weighting factor $W_{\text{DSS}}(\mathbf{r}) \in [0, 1]$ is constructed to selectively suppress incoherent clutter while retaining full phase integrity for structural tissue interfaces:
    $$I_{\text{DSS}}(\mathbf{r}) = W_{\text{DSS}}(\mathbf{r}) \cdot I_{\text{DAS}}(\mathbf{r})$$
- **In Vivo Validation:**
  - Evaluated on raw in vivo human carotid artery data, comparing standard DAS, Coherence Factor (CF), and the proposed DSS framework.

---

### Key Innovations & Clinical Impact

- **Effective Lumen Clutter Evacuation:** Eliminates residual haze and speckle inside the vascular lumen, yielding a clear black blood pool.
- **Intima-Media Boundary Sharpness:** Preserves high-frequency edge gradients along the vessel wall without causing signal cancellation or dark-band artifacts common in classic adaptive beamformers.
- **Hardware-Friendly Implementation:** Operates directly on delayed channel data subsets via simple statistical metrics, making it well-suited for real-time GPU/FPGA integration on portable ultrasound scanners.
- **Modality-Agnostic Weighting:** Readily extensible to other clinical targets vulnerable to acoustic clutter, such as cardiac echocardiography and thyroid sonography.
