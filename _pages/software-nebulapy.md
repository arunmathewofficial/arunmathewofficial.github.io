---
layout: archive
title: "NebulaPy"
permalink: /software/nebulapy/
author_profile: true
---

{% include base_path %}

## Synthetic emission from astrophysical simulations

**NebulaPy** is a Python package for converting the physical and ionisation structure of numerical simulations into synthetic observables. It provides a bridge between computational plasma models and observations by calculating emission maps, spectral-line luminosities, and spectra.

NebulaPy uses atomic data and emissivities from **[ChiantiPy](https://github.com/chianti-atomic/ChiantiPy)**. It can work with non-equilibrium ion populations produced by NEMO, enabling consistent post-processing of radiation–MHD simulations.

## Capabilities

* Produces synthetic emission maps from simulation data.
* Calculates spectral-line luminosities and multi-wavelength spectra.
* Uses ion-by-ion plasma properties and atomic emissivity data.
* Supports non-equilibrium ionisation results from NEMO.
* Helps compare numerical models directly with astronomical observations.

## Applications

NebulaPy is designed for the analysis of stellar-wind bow shocks, circumstellar nebulae, colliding-wind systems, and other ionised astrophysical environments. Together with NEMO, it supports predictive modelling of plasma emission from radio to X-ray wavelengths.

[View NebulaPy on GitHub](https://github.com/arunmathewofficial/NebulaPy){: .btn .btn--primary}
[← Back to Software](/software/){: .btn}
