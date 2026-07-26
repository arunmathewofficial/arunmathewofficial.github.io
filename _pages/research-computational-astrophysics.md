---
layout: archive
title: "Computational Astrophysics"
permalink: /research/computational-astrophysics/
author_profile: true
---

{% include base_path %}

<style>
  .ionisation-comparison {
    float: right;
    width: 52%;
    max-width: 560px;
    margin: 0 0 1.5rem 2rem;
  }

  .ionisation-comparison img {
    width: 100%;
    height: auto;
    border-radius: 0.35rem;
  }

  .ionisation-comparison figcaption {
    margin-top: 0.45rem;
    font-size: 0.8em;
    line-height: 1.4;
  }

  @media (max-width: 700px) {
    .ionisation-comparison {
      float: none;
      width: 100%;
      max-width: none;
      margin: 0 0 1.5rem;
    }
  }
</style>

<figure class="ionisation-comparison">
  <a href="{{ base_path }}/images/oxygen-neq-ieq-profile.png">
    <img src="{{ base_path }}/images/oxygen-neq-ieq-profile.png"
         alt="Oxygen ion distributions in a stellar-wind bow shock comparing non-equilibrium ionisation and ionisation-equilibrium states"
         loading="eager">
  </a>
  <figcaption>
    <strong>Oxygen ionisation structure of a stellar-wind bow shock.</strong> Each panel shows the spatial distribution of the labelled oxygen ion. The upper half displays the non-equilibrium ionisation (NEI) fraction, while the lower half shows the corresponding ionisation-equilibrium (IEQ) fraction. The colour bar gives the relative abundance of oxygen in each ionisation state on a linear scale from 0 to 1. The star is located at the origin; the contact discontinuity (CD) and outer bow shock are most clearly visible in the O<sup>1+</sup> panel. Select the image to view it at full resolution.
  </figcaption>
</figure>

I study the dynamics, ionisation, and radiation of astrophysical plasmas using numerical simulations. My work focuses on stellar-wind bow shocks, colliding-wind binaries, Wolf–Rayet nebulae, and other shocked or photoionised environments. A central goal is to connect plasma microphysics with observable emission across the electromagnetic spectrum, from radio wavelengths to X-rays.

My computational work includes:

* **Non-equilibrium plasma astrophysics** — multi-ion chemical kinetics and non-equilibrium ionisation in shocked and photoionised plasmas.
* **Radiation–magnetohydrodynamics** — large-scale simulations of stellar winds, shocks, and circumstellar nebulae.
* **Synthetic observations** — emission maps, line luminosities, and multi-wavelength spectra for direct comparison with observations.
* **High-performance computing** — hybrid MPI/OpenMP simulations on national and European supercomputing facilities.

I am the lead developer of **[NEMO](https://arxiv.org/abs/2409.18904)**, a multi-ion non-equilibrium ionisation solver integrated into the [PION](https://github.com/jmackey-astro/PION) radiation-MHD code. I also developed **[NebulaPy](https://github.com/arunmathewofficial/NebulaPy)**, a Python package for generating synthetic emission maps, line luminosities, and spectra using atomic data from [ChiantiPy](https://github.com/chianti-atomic/ChiantiPy).

<div style="clear: both;"></div>

[← Back to Research](/research/)
