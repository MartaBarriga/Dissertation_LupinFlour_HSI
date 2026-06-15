# Dissertation_LupinFlour_HSI
Python Script 
# Dissertation_LupinFlour_HSI

Code for an MSc dissertation on the non-destructive prediction of moisture and
protein content in commercial white lupin (*Lupinus albus*) flour using
near-infrared hyperspectral imaging (NIR-HSI, 900-1700 nm) combined with
chemometric modelling.

## Overview

Thirty-seven flour samples from eleven commercial brands were imaged and
partitioned at the brand level, with entire brands withheld from calibration to
provide a realistic estimate of performance on unseen products. Three regression
models (PLSR, PCR, and SVMR) were optimised across 21 spectral preprocessing
strategies, using both the full spectral range and reduced wavelength subsets
selected by Competitive Adaptive Reweighted Sampling (CARS). The best models were
applied per pixel to generate spatial distribution maps of both constituents.

## Contents

The analysis is contained in a single Jupyter notebook
(`lupinflour_hyperspectral_final.ipynb`), organised as follows:

- reflectance calibration, region-of-interest segmentation, and edge-band trimming
- spectral preprocessing (SNV, MSC, Savitzky-Golay first and second derivatives,
  and combinations)
- preprocessing and hyperparameter optimisation under brand-level
  leave-one-out cross-validation
- CARS wavelength selection
- external prediction on the held-out brands, for both the full spectral range
  and the CARS-selected subsets
- pixel-level distribution maps for moisture and protein
