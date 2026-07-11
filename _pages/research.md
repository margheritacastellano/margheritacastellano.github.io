---
layout: page
title: Research
permalink: /research/
description: PhD research, and research projects beyond my PhD.
nav: false
---

## PhD {#phd}

My PhD, at CMAP, École Polytechnique, focuses on finite-volume numerical methods for **Cahn-Hilliard-Navier-Stokes systems with surfactants** — a multiphysics model describing two immiscible fluids (such as water and air) whose interface is modified by surfactant molecules, the same molecules that let soap bubbles form and stay stable. The coupled system is stiff and does not satisfy a maximum principle, so standard schemes struggle to preserve its physical structure (positivity, energy dissipation) on general meshes.

I study and compare two finite-volume discretizations — a **two-point flux approximation (TPFA)** scheme and a **Discrete Duality Finite Volume (DDFV)** scheme — proving existence of discrete solutions and analyzing their convergence. My main result is the convergence analysis of the DDFV scheme, built on a discrete energy estimate that mirrors the continuous system's energy dissipation on general mesh geometries. A second main result is coupling the phase-field model with the Navier-Stokes equations in the DDFV framework, to capture the joint evolution of the interface and the surrounding flow — see my [numerical simulations](/numerical-simulations/) of the resulting two-phase flows.

## Beyond my PhD {#beyond-my-phd}

<div class="row row-cols-1 mt-3">
  <div class="col mb-4">
    <div class="card h-100">
      <div class="card-body">
        <h5 class="card-title">SEMES — Clima-Tek</h5>
        <h6 class="card-subtitle mb-2 text-muted">Semaine d'étude maths, entreprises et société</h6>
        <p class="card-text">
          A simplified 2D+1D ocean transport model for marine carbon dioxide removal via Ocean Alkalinity Enhancement (OAE), developed with <strong>Clima-Tek</strong> together with A. Pinet, A. Mohamed Houmed, and I. Oubarka. The model couples an implicit finite-volume scheme for 1D vertical advection-diffusion with a 2D Lagrangian transport of alkalinity particles (ECCO-Darwin/LLC270 currents, via OceanParcels), validated in the Antarctic Circumpolar Current with exact mass conservation.
        </p>
      </div>
    </div>
  </div>
  <div class="col mb-4">
    <div class="card h-100">
      <div class="card-body">
        <h5 class="card-title">Electrostatic modeling of microelectrode arrays</h5>
        <h6 class="card-subtitle mb-2 text-muted">Internship, Inria Paris</h6>
        <p class="card-text">
          During a two-month internship at Inria Paris, supervised by Damiano Lombardi and Muriel Boulakia, I built 2D PDE models (monodomain equations) describing the propagation of electric potential in cardiomyocyte tissue on a microelectrode array (MEA) device, incorporating a thin adhesion (fibronectin) layer between the cells and the electrodes. I compared models with and without this layer under several boundary conditions and ionic models (a linear ionic term, then the Mitchell-Schaeffer model), discretizing in time by operator splitting (implicit Euler, then BDF2) and in space by P1 finite elements, solved with FreeFem++. The adhesion layer's conductivity turned out to have a strong effect on the potential measured at the electrodes, especially when the device's ground is positioned between them.
        </p>
      </div>
    </div>
  </div>
  <div class="col mb-4">
    <div class="card h-100">
      <div class="card-body">
        <h5 class="card-title">Brain transcriptomics &amp; epigenetics in Autism Spectrum Disorder</h5>
        <h6 class="card-subtitle mb-2 text-muted">Master's project, University of Trento — poster, SIBBM 2021</h6>
        <p class="card-text">
          With Mario Lauria (Dept. of Mathematics, University of Trento / Microsoft Research–University of Trento COSBI Centre), I investigated whether brain transcriptional and epigenetic signals are associated with Autism Spectrum Disorder, using a public RNA expression dataset (GEO GSE38609, 36 samples from the Cerebellum and Occipital regions). I combined unsupervised methods (PCA, the rank-based SCUDO method) with supervised ones (Random Forest, LASSO) to characterize gene-expression differences between ASD and control groups. The two brain regions proved too different to classify jointly, so I focused on the Cerebellum, where LASSO and SCUDO agreed on a common gene and a Random Forest selection of 40 significant genes reached 83.3% accuracy. Presented as a poster at SIBBM, Frontiers in Molecular Biology (2021).
        </p>
      </div>
    </div>
  </div>
</div>
