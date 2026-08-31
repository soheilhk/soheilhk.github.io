---
title: "Minimum Transmit Sampling for Resolution Preservation in Ultrasound Tomography"
collection: publications
category: conferences
permalink: /publication/Conf_IEEE_IUS2026_Hakakzadeh_et_al_MinTx
authors: "S Hakakzadeh, M Mehrmohammadi"
excerpt: "Deriving an analytical transmit sparsification bound for ring-array USCT based on Rayleigh scattering and transducer directivity, optimizing frame rates while avoiding off-center resolution degradation in phantom and in-vivo scans."
date: 2026-9-15
venue: '2026 IEEE International Ultrasonics Symposium (IUS)'
paperurl: 'files/publications/Conf_IEEE_IUS2026_Hakakzadeh_et_al_MinTx.pdf'
publisherurl:
citation: 
---
Background, Motivation, and Objective  
Reflection ultrasound computed tomography (RUCT) enables high‑resolution full‑view imaging for 
breast and small‑animal imaging. RUCT typically uses many transmit events to provide sufficient 
angular diversity for reconstruction. However, dense transmit sampling limits the achievable frame rate 
(FR), which is critical for ultrafast imaging. Moreover, the minimum transmit sampling required to 
preserve spatial resolution is not well established, and more transmissions than required may be used. 
The objective of this work is to determine the minimum number of transmit events required to avoid 
resolution degradation within a region of interest (ROI), enabling transmit sparsification and higher 
FR USCT imaging. 
Statement of Contribution/Methods 
We derive a physics‑based criterion to estimate the minimum transmit events required to preserve 
resolution in ring‑array USCT. A circular array surrounds a ROI with radius 𝑅𝑅𝑂𝐼. Due to the combined 
effects of Rayleigh‑regime scattering (Fig. B) and transducer directivity (𝜃𝐷), the detectable scattered 
field from a given transmit element is confined to a limited angular sector characterized by an effective 
scattering width 𝜃𝑒𝑓𝑓 (Fig. A), defined as the minimum between the FWHM of the scattering angular 
response 𝜃𝑠 and the transducer directivity 𝜃𝐷. The effective angular coverage per transmit is further 
limited by the angular span of the ROI. The effective angular step and resulting minimum number of 
required transmit events are illustrated in Fig. A,B (red equation). 
Results/Discussion 
Two datasets were evaluated using a 512‑element ring array (R=4 cm, f=5 MHz) with 256 receivers per 
transmit. For the hexKey phantom with RROI /R=0.5 (Fig. C1–C3), the model predicts NTx ≈ 32 which 
preserves the structures indicated by arrows. Reducing NTx leads to resolution loss, particularly away 
from the center. For the in‑vivo rat with RROI/R=0.25 (Fig. D1–D3), the predicted requirement decreases 
to NTx ≈ 16. Reconstructions confirm that features degrade as NTx decreases and as structures lie farther 
from the center. The agreement between the predicted transmit requirements and the observed 
resolution degradation across both datasets supports the validity of the proposed physics‑based 
criterion for determining the minimum transmit sampling needed to preserve spatial resolution in 
sparse‑TX RUCT.  
