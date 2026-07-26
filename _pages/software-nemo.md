---
layout: archive
title: "NEMO"
permalink: /software/nemo/
author_profile: true
---

{% include base_path %}

## Multi-ion non-equilibrium ionisation

**NEMO** is a multi-ion non-equilibrium ionisation solver for ionised astrophysical plasmas with arbitrary elemental abundances. It is designed to follow time-dependent ionisation and recombination in environments where the plasma state cannot be described accurately by an instantaneous ionisation-equilibrium approximation.

NEMO is integrated into the **[PION](https://github.com/jmackey-astro/PION)** radiation–magnetohydrodynamics code, allowing ion populations to evolve self-consistently with the gas dynamics and radiation field.

## Capabilities

* Evolves multiple ionisation states for multiple chemical elements.
* Supports arbitrary elemental abundances.
* Models non-equilibrium ionisation in shocked and photoionised plasmas.
* Couples ionisation kinetics to radiation–MHD simulations.
* Provides physically consistent ion populations for synthetic emission calculations.

## Applications

NEMO is used to investigate stellar-wind bow shocks, circumstellar nebulae, colliding winds, and other dynamic plasma environments. By resolving departures from ionisation equilibrium, it improves predictions of the spatial and spectral signatures observed from radio to X-ray wavelengths.

## Publication

Mathew, A., Mackey, J., Celeste, M., Haworth, T. J., & Mellema, G. (2025), “A multi-ion non-equilibrium solver for ionised astrophysical plasmas with arbitrary elemental abundances,” *Astronomy & Astrophysics*, **695**, A73.

[Read the paper](https://doi.org/10.1051/0004-6361/202452373){: .btn .btn--primary}
[← Back to Software](/software/){: .btn}
