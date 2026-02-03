---
title: Close Evaluation of Layer Potentials
permalink: /research/evaluation/
layout: layouts/page.njk
locale: en
---

Publications : [5], [7-8], [10], [15].

Funding : NSF DMS-1819052 ($200k, PI, 2018-2022) 


The close-evaluation problem in boundary integral methods refers to large errors incurred when evaluating layer potentials at points near the boundary of the domain despite being accurate elsewhere in the domain. When using a high order Nyström method to numerically evaluate a layer potential, its high order accuracy will be effective for nearly all points in the domain. However, at close-evaluation points, this quadrature rule will produce an O(1) error. The goal is to address this error using asymptotic analysis of the nearly singular behavior.

## Asymptotic Approximations Methods

##### with R. Cortez, S. Khatri, A. D. Kim, C. McCullough

We developed asymptotic approximations methods based on matched asymptotic expansions of layer potentials in 2D and 3D to control the error with respect to the distance from the boundary.

In 2D the method relies on correcting a patch using the asymptotic expansions of the solution. In 3D the approach relies on a linear mapping and rotation to locate the close evaluation point at the north pole. Results show linear convergence with respect to the boundary and can be extended to higher order. 

In the context of multiple scattering, the close evaluation problem even arises at the BIE level, where coupling effects are computed via nearly-singular behaviors. Using the previous approaches and combining spherical harmonic expansions, we provide accurate evaluation of the near-field for acoustic binding. 

<div style="display: flex; gap: var(--space-md); align-items: center; flex-wrap: wrap; justify-content: center; margin: var(--space-xl) 0;">
  <img src="/assets/img/summary-3d.png" alt="summary method" style="max-width: 300px; width: 100%; border-radius: var(--radius-md); box-shadow: var(--shadow-md);">
</div>

