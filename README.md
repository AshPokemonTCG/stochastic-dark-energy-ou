# stochastic-dark-energy-ou

Independent analysis of stochastic fluctuations in dark energy using public DESI DR2 BAO data, including tests for tachyonic quantum fluid instabilities and the gauge structure of spacetime.

## Overview

This repository contains research on whether the late-time dark energy sector contains any detectable stochastic component. The analysis uses public DESI DR2 Baryon Acoustic Oscillation data to test both stationary (Ornstein–Uhlenbeck) and non-stationary models, as well as the implications of volume-preserving diffeomorphisms (SDiff) for the protection of the cosmological vacuum.

## Main Findings

- No significant evidence is found for stationary stochastic fluctuations when the cosmological background is allowed to vary.
- A globally coherent tachyonic quantum fluid model with negative effective mass is strongly disfavored.
- The observed smoothness of the vacuum (\(\sigma_X < 1.5 \times 10^{-4}\)) is naturally explained by the reduction of the spacetime gauge group to volume-preserving diffeomorphisms (\(\mathrm{SDiff}(M)\)).
- Future observations with Euclid DR1 can help distinguish whether \(\mathrm{SDiff}(M)\) is a fundamental symmetry or an emergent feature.

## Repository Structure

### Scientific Documents (.md)

| File | Description |
|------|-------------|
| `stochastic-dark-energy-desi-dr2.md` | Main analysis paper on Ornstein–Uhlenbeck and QNM models fitted to DESI DR2 data. |
| `quantum-fluid-instabilities-desi-dr2.md` | Paper testing tachyonic quantum fluid instabilities using rank-1 growing covariance. |
| `principle-of-vacuum-smoothness.md` | Short note presenting the **Principle of Late-Time Vacuum Homogeneity**. |
| `smoothness-of-the-vacuum-unimodular.md` | Theoretical discussion on unimodular gravity and vacuum smoothness. |
| `unimodular-gravity-vacuum-smoothness.md` | More developed theoretical synthesis on unimodular gravity and the geometric origin of vacuum smoothness. |
| `sdiff-fundamental-vs-emergent.md` | **New** — Analysis of whether volume-preserving diffeomorphisms (SDiff) are fundamental or emergent, with observational implications for Euclid DR1. |
| `sensitivity_kernel_table.md` | Supplementary table with BAO sensitivity kernel values. |
| `README.md` | This file. |

### Python Scripts (.py)

| File | Description |
|------|-------------|
| `ou_bao_stochastic_test.py` | Main likelihood pipeline with OU and QNM kernels, MLE fitting, and sensitivity kernel computation. |
| `ou_bao_likelihood.py` | Core BAO likelihood functions. |
| `cross_correlation_DESI.py` | Cross-correlation analysis between DESI galaxies and Pantheon+ supernovae. |
| `test_desi_dr2_correlations.py` | Additional correlation tests on DESI DR2 data. |

### Figures (.png)

| File | Description |
|------|-------------|
| `Figure_1.png` | Main results figure (exclusion limits or model comparison). |
| `Figure_2.png` | Secondary results figure. |
| `exclusion_plot.png` | Plot showing exclusion limits on stochastic amplitude. |
| `falsos_positivos_detectores.png` | Figure related to false-positive analysis. |
| `gpe_negative_mass_evolution.png` | Evolution of a negative-mass Gross–Pitaevskii condensate. |
| `gpe_negative_mass_instability.png` | Instability growth in the tachyonic quantum fluid model. |
| `test_desi_QNM.png` | Diagnostic plot for quasi-normal mode behavior with DESI data. |

### Other Files

| File | Description |
|------|-------------|
| `requirements.txt` | Python package dependencies. |
| `resume.txt` | Internal notes and summary of results. |

## Data Sources

- DESI DR2 BAO: https://data.desi.lbl.gov/public/
- Pantheon+ Type Ia Supernovae (used for cross-checks)

## Status

This is independent research (July 2026). The results are not yet peer-reviewed. The project is being extended for future datasets such as Euclid DR1, with particular focus on testing the fundamental vs emergent nature of volume-preserving diffeomorphisms.

## Author

Jesús Morales Souhail  
ORCID: [0009-0000-7637-1818](https://orcid.org/0009-0000-7637-1818)
