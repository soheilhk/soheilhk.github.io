---
title: "Detector-Subset Stability-Guided Artifact Suppression in Circular PACT"
publications:
  - Paper_Journal_2027_Hakakzadeh_et_al_DSS_PACT
  - Conf_IEEE_IUS2024_Hakakzadeh_et_al_CVPACT
collection: research
category: pat
date: 2026-11-01
venue: "Ring-Array / Sparse Array & Artifact Suppression"
excerpt: "A non-iterative Detector-Subset Stability (DSS) framework for suppressing sparse-sampling streak artifacts in circular PACT while preserving absorber morphology and intensity. Pixel-wise stability maps generated from multiple detector-subset images identify artifact-prone regions and guide correction of the full-detector image. Validation on simulated and experimental phantoms and in vivo rat-brain data achieved 96–98% Precision and F1 scores, gCNR values of 0.67–0.73, and SNR gains of up to 57 dB."
image: "images/research/pat/pat3_DSS.PNG"
image_caption: "In-Vivo Brain Imaging Results. (a) Anatomical 3D schematic of rat brain vasculature
atlas. (b-c1) DAS reconstruction with 512 and 256 DPs, respectively. (c2–c3) Randomized and
RISP methods reduce artifacts but attenuate vascular signals. (c4) Final DSS reconstruction
showing clear artifact suppression with preserved major and fine cerebral vessels. The scale
bar is 1 cm."
expanded: true
---

### Overview & Motivation

Sparse detector sampling is widely used in circular photoacoustic computed tomography (PACT) to reduce hardware complexity, acquisition time, and computational cost. However, undersampling produces strong streak artifacts that can obscure true absorbers, reduce image contrast, and cause substantial errors in absorber intensity.

Many existing artifact-reduction methods suppress streaks by applying aggressive filtering, nonlinear weighting, iterative optimization, or learned priors. Although these methods can improve visual appearance, they may also atten priors. Although these methods can improve visual appearance, they may also atten amplitudes.

This project introduces a **Detector-Subset Stability (DSS)-guided artifact suppression framework**. The method exploits a key distinction between true absorbers and sparse-sampling artifacts: genuine absorbers remain spatially stable when different subsets of detector elements are used for reconstruction, whereas streak artifacts vary substantially across detector subsets.

---

### Key Technical Details & Methodology

- **Full-Detector Reconstruction:**
  - A full-detector image (FDI) is first reconstructed from all available detector channels:
    $$
    I_{\mathrm{FDI}}(\mathbf{r}) =
    \mathcal{R}\left\{D_{\mathrm{full}}\right\},
    $$
    where $\mathcal{R}\{\cdot\}$ denotes the reconstruction operator and $\mathbf{r}$ is the image position.

- **Detector-Subset Image Generation:**
  - The detector array is divided into multiple subsets:
    $$
    D_1, D_2, \ldots, D_M.
    $$
  - Each subset is independently reconstructed to generate detector-subset images (DSIs):
    $$
    I_m(\mathbf{r}) =
    \mathcal{R}\left\{D_m\right\},
    \qquad m=1,\ldots,M.
    $$

- **Pixel-Wise Detector-Subset Stability:**
  - The intensity consistency of each pixel across DSIs is analyzed to distinguish stable absorber responses from unstable streak artifacts.
  - A detector-subset stability ratio is calculated from the variation of corresponding pixel intensities:
    $$
    \mathrm{DSS}(\mathbf{r}) =
    g\left(
    I_1(\mathbf{r}), I_2(\mathbf{r}), \ldots, I_M(\mathbf{r})
    \right),
    $$
    where high stability indicates a reliable absorber and low stability indicates an artifact-prone region.

- **Stability Map Generation:**
  - The DSS map is processed to reduce isolated outliers and identify pixels with sufficient detector-subset consistency.
  - A binary or continuous stability map is generated:
    $$
    W_{\mathrm{DSS}}(\mathbf{r}) \in [0,1].
    $$

- **Artifact Suppression in the Full-Detector Image:**
  - The stability map is applied directly to the FDI:
    $$
    I_{\mathrm{DSS}}(\mathbf{r}) =
    W_{\mathrm{DSS}}(\mathbf{r})
    I_{\mathrm{FDI}}(\mathbf{r}).
    $$
  - Stable absorber regions are retained, while regions dominated by fluctuating streak artifacts are suppressed.

- **Non-Iterative Processing:**
  - The method does not require iterative model-based optimization, neural-network training, or a manually designed anatomical prior.
  - It operates directly on multiple reconstructions generated from detector subsets.

---

### Validation Studies

The framework was evaluated using multiple complementary datasets:

- **Simulated breast phantom**
  - Used to assess structural fidelity and absorber-intensity preservation under controlled sparse-sampling conditions.

- **Experimental leaf phantom**
  - Used to evaluate the suppression of streak artifacts around extended absorber structures.

- **Experimental triangle phantom**
  - Used to assess preservation of geometric morphology and boundary continuity.

- **In vivo rat-brain data**
  - Used to demonstrate performance in biologically realistic imaging conditions with complex absorber distributions.

The evaluation included comparisons with conventional and artifact-suppression reconstructions under severe detector undersampling.

---

### Quantitative Performance

| Metric | DSS-Guided Framework |
|:---|:---:|
| Precision | **96–98%** |
| F1 score | **96–98%** |
| gCNR | **0.67–0.73** |
| Maximum SNR gain | **Up to 57 dB** |

The DSS-guided method consistently achieved high structural-detection accuracy while improving image contrast and suppressing sparse-sampling artifacts.

---

### Key Innovations & Impact

- **Detector-Subset Stability Analysis:**  
  Uses reconstruction consistency across detector subsets to identify reliable absorbers without requiring a ground-truth image.

- **Morphology Preservation:**  
  Suppresses streak artifacts while maintaining absorber shape, continuity, and spatial structure.

- **Intensity Fidelity:**  
  Preserves absorber intensity closer to the ground truth than methods that rely on aggressive attenuation or nonlinear artifact suppression.

- **Non-Iterative and Interpretable:**  
  Provides a direct stability-guided correction mechanism with transparent physical interpretation.

- **Robustness Under Severe Undersampling:**  
  Achieves SNR improvements of up to 57 dB even when the detector array is substantially undersampled.

- **Broad Validation:**  
  Demonstrated using simulated, experimental, and in vivo datasets, including breast, leaf, triangle, and rat-brain phantoms.

- **Potential for Efficient PACT:**  
  The framework may enable lower-channel-count and reduced-acquisition PACT systems while preserving image quality and structural reliability.
