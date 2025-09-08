# PBH Merger Model: Multi-Species Interactions in Dense Clusters

This repository contains a Python-based simulation to model the dynamics of **primordial black hole (PBH) mergers** in dense astrophysical clusters, extending the formalism developed by García-Bellido et al. (2021–2022). It focuses on computing the **gravitational wave (GW) emission** from both **binary black hole (BBH) captures** and **close hyperbolic encounters (CHEs)**, including all interaction combinations between PBHs of different generations.

---

<div style="display: flex; justify-content: center; align-items: center; gap: 20px;">
  <img src="https://francia.unam.mx/wp-content/uploads/2021/10/Logo-UNAM-Azul-Landscape.png" alt="UNAM" width="225" height="125">
  <img src="https://mcdonaldinstitute.ca/wp-content/uploads/2018/05/PI-logo-2017-Black-1280x424.png.webp" alt="Perimeter" width="200" height="100">
  <img src="https://swanseauniversity.cloud.panopto.eu/Panopto/ContentCache/637582254009215017/_branding/f80a49ed-5120-415e-89fe-ab8900ad7d40/637582253354333331_largelogo.png" alt="Swansea" width="225" height="125">
</div>



## 🎯 Purpose

To evaluate the merger rates of PBHs in a dense cluster following a Plummer profile, and compute:

- The **interaction rate** for all combinations of PBH species (0G–0G, 0G–1G, 1G–1G),
- The **total power** radiated in gravitational waves,
- The **expected number of collisions** per shell,
- The evolution of **cluster energy and mass** over interaction epochs.

---

## ✅ Current Capabilities

This functional version of the code performs the following steps:

1. **Defines a Plummer density profile** for a compact PBH cluster.
2. Divides the cluster into spherical shells to evaluate local interactions.
3. Initializes two PBH species:
   - `0G`: Original (first-generation) PBHs of fixed mass $M_\mathrm{PBH}$,
   - `1G`: Merger products of 0G–0G interactions, with final masses corrected for GW energy losses.
4. Generates **all combinations with replacement** of species: (0G–0G), (0G–1G), (1G–1G).
5. For each combination:
   - Computes **number densities**, **mean-square velocities**, and **effective cross-sections**,
   - Calculates the **total GW power** radiated per shell,
   - Estimates the **number of expected events** by shell and interaction type.

6. Prints the results in tabular form:
   - Species combination name,
   - Radiated GW power,
   - Total number of collisions,
   - Characteristic interaction timescale.

---

## 📦 Dependencies

- Python 3.8+
- Required libraries:
  - `numpy`
  - `scipy`
  - `matplotlib`
  - `seaborn`
  - `astropy`
  - `itertools`

---

## 📍 Upcoming Features

- Implement cumulative power tracking to visualize the **time evolution** of $\Omega_{\mathrm{GW}}(t)$,
- Add **higher-generation species** (2G, 3G, ...) with proper mass and energy tracking,
- Calculate the **spectral energy distribution** of GW signals for both BBH and CHE scenarios,
- Animate the **hierarchical merger tree and energy output** over time.

---

# ✍️ Code Written by Tadeo D.
## Dedicated to my girlfriend and fiancée, Dra. Elizabeth América Flores Frías.

---

## 📚 References

- J. García-Bellido, S. Jaraba, S. Kuroyanagi, *The stochastic gravitational wave background from close hyperbolic encounters of primordial black holes in dense clusters*, Phys. Dark Univ. 36 (2022), [arXiv:2109.11376](https://arxiv.org/abs/2109.11376)
- E. Erfani, T. D. Gómez-Aguilar, J. C. Hidalgo, *Hierarchical Merger of Primordial Black Holes in Dwarf Galaxies*, [arXiv:2205.08906](https://arxiv.org/abs/2205.08906)
- M. Caldarola, S. Kuroyanagi, S. Nesseris, J. García-Bellido, *Effects of orbital precession on hyperbolic encounters*, [arXiv:2307.00915](https://arxiv.org/abs/2307.00915)

