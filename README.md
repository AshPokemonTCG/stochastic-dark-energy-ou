# Stochastic Dark Energy: Constraints from DESI DR2

**Author:** Jesús Morales Souhail  
**Contact:** jmskjym@gmail.com  
**ORCID:** 0009-0000-7637-1818
**Repository:** https://github.com/AshPokemonTCG/stochastic-dark-energy-ou

This repository contains the numerical tools, statistical analysis scripts, and
technical documentation to test the **Stochastic Dark Energy (SDE)** hypothesis
against public DESI DR2 BAO data. The SDE framework postulates that the
cosmological constant is not strictly static, but experiences small stochastic
fluctuations motivated by the finite information content of the observable
universe (Bekenstein–Hawking bound) and the ~1/√N fluctuation scaling suggested
by unimodular gravity and causal-set arguments.

Fluctuations in Ω_Λ are modeled as an **Ornstein–Uhlenbeck (OU) process**
in x = ln a, with mean-reversion rate θ and diffusion amplitude σ. A
**quasi-normal mode (QNM) extension** with an oscillatory kernel is also
tested.

---

## Key Results (DESI DR2, July 2026)

### Test 1 — BAO Likelihood with OU Covariance

Using DESI DR2 BAO data (7 bins, arXiv:2503.14738), the maximum likelihood
estimation (MLE) forces the stochastic amplitude to zero:

| Model | θ | σ_X | ω_R | ΔlogL vs ΛCDM | AIC | BIC |
|---|---|---|---|---|---|---|
| **ΛCDM** | — | — | — | 0.00 (ref) | ref | ref |
| **H0: OU free MLE** | 0.001 | 5 × 10⁻⁵ | 0 (fixed) | 0.00 | -50.03 | -50.14 |
| **H1: QNM free MLE** | 0.001 | 5 × 10⁻⁵ | 0.00 | 0.00 | -48.03 | -48.19 |

**Conclusion:** There is **no evidence** for stochastic fluctuations in the
DESI DR2 BAO data. The data are fully consistent with smooth CPL evolution
(\(w_0 \approx -0.87, w_a \approx -0.41\)) plus instrumental noise.

**Strict upper limit (95% CL):** \(\sigma_X < 1.5 \times 10^{-4}\).

### Test 2 — Angular Cross-Correlation (δ_g × δΩ_Λ)

DESI DR1 LRG (1,476,135 + 662,000 objects) × Pantheon+ residuals (1,701 SNe):
r_cross = 0.1673 ± 0.0613 (Z ≈ 2.73σ, 67 overlapping pixels)
OU prediction: r_pred ~ 0.023

text

**Preliminary.** Imaging systematics not yet controlled. DESI DR2
with WEIGHT_SYS column required for systematic-controlled reanalysis.

### Test 3 — Lag Correlations in BAO Residuals

| Lag | DR2 (7 bins) | OU Prediction | 95% CI | Significant? |
|---|---|---|---|---|
| 1 | +0.37 | +0.83 | ±1.0 | No |
| 2 | −0.32 | +0.85 | ±1.0 | No |
| 3 | −0.81 | +0.85 | ±1.0 | No |

None individually significant at 7 bins. Decisive test: >20 bins (Euclid DR1,
H2 2026).

---

## Requirements and Installation

Python 3.8+

```bash
pip install -r requirements.txt
requirements.txt:

text
numpy>=1.24
scipy>=1.10
astropy>=5.3
healpy>=1.16
matplotlib>=3.7
6. Uhlenbeck & Ornstein, Phys. Rev. 36, 823 (1930)
