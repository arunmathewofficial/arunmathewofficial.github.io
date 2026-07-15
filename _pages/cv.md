---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

{% comment %}
  Renders only once files/cv.pdf exists, so no broken link ships before then.
  Drop the PDF at files/cv.pdf and the button appears by itself.
{% endcomment %}
{% assign cv_pdf = site.static_files | where: "path", "/files/cv.pdf" | first %}
{% if cv_pdf %}
<p><a href="{{ base_path }}/files/cv.pdf" class="btn btn--primary">Download CV as PDF</a></p>
{% endif %}

Professional summary
======
Theoretical and computational astrophysicist with over ten years of research experience across non-equilibrium plasma astrophysics, radiation–magnetohydrodynamics (MHD), general relativity, cosmology, and higher-order gravity. My work spans the modelling of ionised plasmas in stellar and high-energy astrophysical environments, with a focus on connecting fundamental microphysics to observable phenomena, as well as studies of extended gravity in compact objects and early-Universe physics, including inflation and reheating.

Developer of the multi-ion non-equilibrium plasma solver NEMO and the non-equilibrium spectral synthesis package NebulaPy, based on ChiantiPy and NebPy, enabling self-consistent simulations and predictive modelling of multi-wavelength emission from radio to X-rays. Author of more than 13 refereed publications, eight as first author, with an h-index of 5.

Over four years of teaching and mentoring experience across senior secondary, undergraduate, and postgraduate levels, with demonstrated capability in delivering lectures, tutorials, and laboratory sessions in physics and computational methods. Supervised and supported research projects at undergraduate, master's, and PhD levels.

Education
======
* **Ph.D., Astrophysics and Cosmology** — August 2021
  * [Indian Institute of Technology Guwahati](https://www.iitg.ac.in/), Guwahati, India
  * Thesis: *Generalized uncertainty scenario of quantum gravity in white dwarfs and extended gravity scenarios in quark stars and inflationary cosmology*
  * Supervisor: [Dr. Malay Kumar Nandy](https://iitg.irins.org/profile/4443)
* **M.S. in Applied Physics** — 2013
  * Mar Thoma College, Mahatma Gandhi University, Tiruvalla, India
* **M.S. in Physics (Astrophysics)** — 2010
  * Indian Institute of Technology Guwahati, Guwahati, India
* **B.S. in Physics (Major), Mathematics, and Statistics** — 2010
  * CMS College, Mahatma Gandhi University, Kottayam, India

Postdoctoral research
======
**Computational and High Energy Astrophysics** — 2022–2024
  * Dublin Institute for Advanced Studies, Dublin, Ireland
  * Project: *Synthetic observations and computational modelling of Wolf–Rayet nebulae, investigating their ionisation structure and emission properties using MHD simulations*
  * Mentor: [Dr. Jonathan Mackey](https://homepages.dias.ie/jmackey/)
  * Supported under the Royal Society Enhanced Research Expenses Grant (RF\ERE\210382)

Non-academic experience
======
**Production Operator** — March 2025–present
  * Syntro Health, Melbourne, Australia
  * cGMP-compliant manufacturing of clinical trial pharmaceuticals, involving precision processes and rigorous quality and regulatory compliance.

Competitive fellowships and academic achievements
======
* Senior Research Fellowship, MHRD, Government of India — 2017–2019
* Junior Research Fellowship, MHRD, Government of India — 2013–2016
* [Graduate Aptitude Test in Engineering](https://gate2024.iisc.ac.in/) (All India Rank: 185) — 2013
* Graduate Aptitude Test in Engineering (All India Rank: 827) — 2012
* [Joint Admission Test for M.Sc.](https://gateoffice.iitkgp.ac.in/jam/) (All India Rank: 189) — 2008

Code design and development
======
* [**NEMO**](https://arxiv.org/abs/2409.18904) — Lead developer of a multi-ion, non-equilibrium ionisation solver integrated into [PION](https://github.com/jmackey-astro/PION).
* [**NebulaPy**](https://github.com/arunmathewofficial/NebulaPy) — Designed and developed a Python pre/post-processing tool generating synthetic emission maps and line luminosities using the [Chianti](https://github.com/chianti-atomic/ChiantiPy) database.
* [**Gravity-Matter GR Code**](https://github.com/arunmathewofficial/QuarkStar-fRT-Gravity) — An iterative solver for quark star structure in a perturbative f(R,T) gravity-matter model.
* [**Dynamical Instability Code**](https://zenodo.org/records/4625488) — Stellar structure and dynamical instability analysis of white dwarfs with a generalized uncertainty principle equation of state.

High-performance computing experience
======
* [**Kay**](https://www.ichec.ie/about/infrastructure/kay) at [ICHEC](https://www.ichec.ie/) — cluster of 336 nodes, 2×20 cores each. Allocation: 1,000,000 CPU core-hours over one year. Application: investigation of X-ray emission from interstellar bow shocks. Hybrid MPI/OpenMP parallelisation, with SLURM job scheduling for efficient resource allocation.
* [**Meluxina**](https://www.luxprovide.lu/meluxina/) at [LuxProvide Data Center](https://www.luxprovide.lu/) — 2 sockets per node, 64 cores per socket, 2 CPUs per core. Allocation: 500,000 CPU core-hours over one year. Application: investigation of wind-blown bow shocks with NEMO.

Skills and tools
======
* **Programming**: C++, C#, Python, git
* **CFD developer**: NEMO for PION
* **Python package developer**: NebulaPy
* **Multiprocessing**: implemented multiprocessing in NebulaPy
* **High-performance computing**: Kay (ICHEC), Meluxina (LuxProvide Data Center)
* **Spectral synthesis codes**: Cloudy, ChiantiPy, PyNeb
* **Documentation generators**: Sphinx, Doxygen
* **Utility packages**: Mathematica, Xmgrace, VisIt
* **Operating systems**: Linux/Unix, macOS

Publications
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>

Talks
======
  <ul>{% for post in site.talks reversed %}
    {% include archive-single-talk-cv.html  %}
  {% endfor %}</ul>

Teaching
======
  <ul>{% for post in site.teaching reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>

Research mentoring
======
* **PhD projects**, Indian Institute of Technology Guwahati (2020)
  * *Maximal mass of the neutron star with deconfined quark-gluon plasma core*
  * *Reheating in scalar-tensor model with non-minimal coupling to curvature and non-minimal kinetic coupling of the scalar field to the Einstein tensor*
  * *Neutron star in f(R,T) gravity with gravity-matter coupling*
* **Master's projects**, Indian Institute of Technology Guwahati
  * *Analysis of narrow and broad resonance regimes in the primordial reheating phase of the Universe* — April 2021
  * *Scalar-tensor gravity and white dwarfs in the Jordan frame* — April 2019
  * *Stability of compact stars with the Harrison-Wheeler equation of state in general relativistic and Newtonian gravity* — April 2018
  * *Stability of white dwarfs in general relativity and Newtonian gravity* — April 2018
* **B.Tech. projects**, Indian Institute of Technology Guwahati (May 2020)
  * *Analysis of the rotation curve of the ESO138-G014 galaxy in the framework of modified Newtonian dynamics*
  * *Magnetic field of neutron stars*

Conferences
======
* [Advances in Cool Evolved Stars](https://sites.google.com/monash.edu/aces/home?authuser=0) — Monash University, Melbourne, Australia — 8–12 July 2024
* [Stellar Feedback in the ISM, IAU](https://chu2023.astrosen.unam.mx/) — Instituto de Astronomía, UNAM, Mexico — 11–14 December 2023 (conference summary: [arXiv](https://arxiv.org/abs/2409.12838))
* Irish National Astronomy Meeting 2023 — [School of Physics, University College Cork](https://www.ucc.ie/en/physics/), Ireland — 24–25 September 2023
* Irish National Astronomy Meeting 2022 — [DIAS, Dunsink Observatory](https://www.dunsink.dias.ie/), Ireland — 1–2 September 2022
* Irish National Astronomy Meeting 2021 — virtual — 1–3 September 2021
* Testing General Relativity using Gravitational Waves — virtual workshop, [IACS](https://www.iacs.res.in/) and [IITGN](https://iitgn.ac.in/) — 13–14 August 2020

Selected outreach
======
* Hamilton Walk — 16 October 2024
* Festival of History, DIAS Dunsink Observatory — 10 October 2024
* Visitor Night, DIAS Dunsink Observatory — 25 January 2024
* Visitor Night, DIAS Dunsink Observatory — 2 November 2023
* Public Visitor Night, DIAS Dunsink Observatory — 19 October 2023
* Open House Dublin, DIAS Dunsink Observatory — 14 October 2023
* Culture Night, Dunsink Observatory — 22 September 2023

Other previous projects
======
* Expertise in f(R, φ) gravity.
* Surveyed dark matter evidence at various scales.
* Explored scalar field dark matter in scalar-tensor gravity.
* Verified cold boson dark matter halo formation.
* Investigated spin waves in magnetic lattices.
