---
title: "Minimum Transmit Sampling for Resolution Preservation in Ultrasound Tomography"
collection: publications
category: conferences
permalink: /publication/Conf_IEEE_IUS2026_Hakakzadeh_et_al_SGPWCEcho
authors: "S Hakakzadeh, VA. Nili, SM Mostafavi, Z. Kavehvash, M Mehrmohammadi"
excerpt: "A Stability-Guided Pixel-Wise Correlation (SG-PWC) beamformer that analyzes the consistency of short-lag inter-channel correlations to suppress cardiac clutter while preserving speckle texture, achieving gCNR = 1.00 and CNR = 4.2 in in-vivo echocardiography."
date: 2026-9-15
venue: '2026 IEEE International Ultrasonics Symposium (IUS)'
paperurl: 'files/publications/Conf_IEEE_IUS2026_Hakakzadeh_et_al_SGPWCEcho.pdf'
publisherurl:
citation: 
---
Background, Motivation, and Objective  
Ultrasound cardiac imaging is frequently degraded by acoustic clutter and incoherent echoes that 
obscure anatomical structures and reduce diagnostic visibility. Conventional delay‑and‑sum (DAS) 
beamforming preserves speckle texture but is highly susceptible to clutter. Nonlinear and 
coherence‑based approaches such as delay‑multiply‑and‑sum (DMAS) and short‑lag spatial coherence 
(SLSC) can improve cavity contrast but often introduce speckle distortion or excessive smoothing that 
reduces structural detail. To address these limitations, we propose Stability‑Guided Pixel‑Wise 
Correlation beamforming (SCB), an approach that enhances coherent tissue responses by evaluating 
the stability of spatial correlations across receive channels. 
Statement of Contribution/Methods  
For each image pixel, normalized cross‑correlations between delayed channel signals are computed 
over multiple short spatial lags. Instead of relying only on the correlation magnitude, the proposed 
method analyzes the dispersion of lag‑wise correlations around their mean value. A stability‑guided 
weighting factor is then derived by penalizing large deviations of individual lag correlations from the 
mean correlation. Echoes exhibiting consistent correlation across lags produce a strong stability factor, 
while unstable or incoherent signals associated with clutter and reverberation are suppressed. This 
stability factor is applied pixel‑wise to the beamformed signal, reinforcing reliable coherent echoes 
while attenuating unstable contributions.  
Results/Discussion  
The method was evaluated on in‑vivo cardiac ultrasound data and compared with DAS, DMAS, and 
SLSC beamformers in parasternal short‑axis (PSAX) and parasternal long‑axis (PLAX) views. 
Qualitative results show substantially cleaner ventricular cavities, sharper myocardial borders, and 
improved delineation of cardiac structures while preserving natural speckle texture. Quantitative 
analysis demonstrates that SG‑PWC achieves the highest contrast performance with a gCNR of 1.00 
and a CNR of 4.2, outperforming SLSC (gCNR 0.99, CNR 3.2) and both DAS and DMAS (gCNR 0.96, 
CNR 2.5). These results indicate that incorporating correlation stability provides robust clutter 
suppression while maintaining structural fidelity in cardiac ultrasound imaging. 
