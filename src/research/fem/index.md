---
title: Finite Element Method for Plasmonics
permalink: /research/fem/
layout: layouts/page.njk
locale: en
---

Publications : [1-4], [11-12].

Funding : NSF DMS-2009366 ($295k, single PI, 2020-2024) 

## Modeling Plasmonic Phenomena

Plasmonic structures are made of a positive material (dielectrics) and a negative material (metals at optical frequencies, metamaterials). Surface electromagnetic waves called surface plasmons can appear at the interface.

<div style="text-align: center; margin: var(--space-xl) 0;">
  <img src="/assets/img/plasmon.png" alt="Plasmonic structure" style="max-width: 400px; width: 100%; border-radius: var(--radius-md); box-shadow: var(--shadow-md);">
</div>

Guiding and confining such particular waves in nanophotonic devices reveal a great interest to overcome the diffraction limit, in nanophotonic sensing and related applications. 

Due to potential sign-changing coefficients, standards methods fail to capture plasmonic phenomena. We propose several technique to address this problem.

## Challenges

- Multiple scales
- Surface plasmons are very sensitive to the geometry (corners)
- Inaccurate predictions of the near-field
- Hyper-oscillating singularities, called black-hole waves, appear at the corners
- Standard FEM fail due to spurious reflections

## Novel Numerical Methods using FEM

### Mesh requirements to ensure FEM optimal convergence via the T-coercivity

##### with A.-S. Bonnet Ben Dhia, P. Ciarlet, Z. Moitier

Well-posedness of transmission problems with sign-changing coefficients has been established using the so-called T-coercivity theory. However, in practice it is not as straightforward to apply it. We designed "FEM friendly" T operators to guarantee optimal FEM convergence. Those operators are based on rotations and symmetries, they ensure same well-posedness and are easily satisfied at the discrete level by designing locally symmetric meshes. 
A package providing automatic locally T-conforming mesh is under construction. 

<div style="display: flex; gap: var(--space-md); align-items: center; flex-wrap: wrap; justify-content: center; margin: var(--space-xl) 0;">
  <img src="/assets/img/mesh0.png" alt="Standard mesh" style="max-width: 200px; width: 100%; border-radius: var(--radius-md); box-shadow: var(--shadow-md);">
  <img src="/assets/img/mesh1.png" alt="T-conforming mesh" style="max-width: 200px; width: 100%; border-radius: var(--radius-md); box-shadow: var(--shadow-md);">
</div>

### Use of Perfectly Matched Layers at the corners to capture the black-hole waves

##### with A.-S. Bonnet Ben Dhia, L. Chesnel, P. Ciarlet

The T-coercivity theory allows to establish well-posedness and FEM convergence under some conditions on the optical parameters of the scattered. In the critical regime, where the problem is ill-posed, highly oscillatory singularities (called black-hole waves) appear at the corners. We proposed to use Perfectly Matched Layers at the corners to capture them. This approach is motivated by a quasi-static approximation and a change of coordinates, allowing to interpret the singularities as propagative modes in a waveguide. 

<div style="display: flex; gap: var(--space-md); align-items: center; flex-wrap: wrap; justify-content: center; margin: var(--space-xl) 0;">
  <img src="/assets/img/summary_pmls.png" alt="summary method" style="max-width: 300px; width: 100%; border-radius: var(--radius-md); box-shadow: var(--shadow-md);">
</div>


### Asymptotic characterization of plasmonic scattering resonances and Trefftz methods 

##### with B. Latham, Z. Moitier

While the T-coercivity can guarantee well-posedness of the scattering problems in plasmonic structures, in practice FEM exhibits numerical instabilities at specific wavenumber inputs. Those values are close to so-called scattering resonances. In general, it is impossible to have the exact scattering resonances. Using the Black-Box Scattering Theory and the quais-modes analysis, we estalished their existence and provided an asymptotic characterization. 

While FEM fails to capture them due to their high amplitude signal, we investigated a Trefftz approach (called Evanescent Plane Wave Discontinuous Galerkin) to better mimic their local behavior. Well-posedness of the associated discrete problem has been established, and gets rid of the high mesh constrains imposed by T-coercivity.

<div style="display: flex; gap: var(--space-md); align-items: center; flex-wrap: wrap; justify-content: center; margin: var(--space-xl) 0;">
  <img src="/assets/img/scat_res.png" alt="summary method" style="max-width: 500px; width: 100%; border-radius: var(--radius-md); box-shadow: var(--shadow-md);">
</div>

