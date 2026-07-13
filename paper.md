# Constraints on Stochastic Dark Energy from Quantum Fluid Instabilities and DESI DR2 Baryon Acoustic Oscillations

**Author:** Jesús Morales Souhail  
**Date:** July 2026  
**ORCID:** [0009-0000-7637-1818](https://orcid.org/0009-0000-7637-1818)  
**Repository:** https://github.com/AshPokemonTCG/Bogoliubov_DESI_extension  
**Status:** Preprint – not peer reviewed

---

## Abstract

Recent DESI DR2 BAO data show no evidence for a stochastic component on top of a smooth dynamical dark energy evolution. In this work, we test whether a dark-energy fluid with negative effective mass (\(m^* < 0\)) and quartic self-interaction can generate such fluctuations through a Bogoliubov instability. We derive the correct dispersion relation for a tachyonic condensate and construct the physically consistent rank-1 covariance induced by the coherent growing mode. Maximum Likelihood Estimation directly on the DESI DR2 BAO data excludes any finite collapse time \(t_c\); the data strongly prefer the limit \(t_c \to \infty\) (no growth). A globally coherent tachyonic quantum fluid is incompatible with current observations.

---

## 1. Introduction

Baryon Acoustic Oscillation measurements from DESI DR2 have provided precise constraints on the late-time expansion history. Previous analyses using a stationary Ornstein–Uhlenbeck model drive any additional stochastic amplitude to zero. This null result motivates testing alternative mechanisms that could generate density fluctuations in the dark-energy sector.

One such mechanism is a quantum condensate with negative effective mass, analogous to instabilities observed in engineered Bose–Einstein condensates. If the dark-energy fluid possessed similar properties, it could produce exponentially growing fluctuations detectable in BAO data. In this work we derive the instability growth rate from first principles, construct the correct covariance matrix implied by the model, and confront it directly with DESI DR2 observations.

---

## 2. Theoretical Framework

We consider a complex scalar field \(\psi\) whose condensed state mimics dark energy. The dynamics are governed by a modified Gross–Pitaevskii equation with negative effective mass \(m^* = -M\) (\(M > 0\)) and repulsive quartic interaction \(g > 0\):

$$
i\hbar \frac{\partial\psi}{\partial t} = \left[ -\frac{\hbar^2}{2M a^2(t)}\nabla^2 + g|\psi|^2 \right]\psi.
$$

The background condensate density is identified with the dark-energy density \(\rho_\Lambda \simeq |\psi_0|^2\).

---

## 3. Bogoliubov Excitations and the Instability Growth Rate (Corrected)

Linearising around the homogeneous background and inserting the negative mass \(m^* = -M\) into the Bogoliubov–de Gennes framework yields the dispersion relation:

$$
\omega_q^2 = \varepsilon_q(\varepsilon_q + 2g|\psi_0|^2),
\qquad
\varepsilon_q = -\frac{\hbar^2 q^2}{2 M a^2(t)}.
$$

For small \(q\), \(\omega_q^2 < 0\), indicating dynamical instability. The growth rate is

$$
\Gamma_q = \frac{1}{\hbar}\sqrt{-\omega_q^2} = \frac{\hbar q}{M a^2}\sqrt{2Mg|\psi_0|^2 - \hbar^2 q^2}.
$$

The fastest-growing mode occurs at

$$
q_{\rm max} = \sqrt{2}\,a\,\frac{\sqrt{Mg|\psi_0|^2}}{\hbar},
$$

and the maximum growth rate is

$$
\Gamma_{\rm max} = \frac{g|\psi_0|^2}{\hbar} \equiv \frac{1}{t_c}.
$$

Thus the characteristic collapse time is \(t_c = \hbar / (g|\psi_0|^2)\).

---

## 4. Covariance Induced by the Growing Mode

The model predicts that a single frozen primordial random realisation is amplified coherently. In the saddle-point limit this produces a **rank-1** covariance across redshift bins:

$$
C_{ij} = \delta_{ij}\sigma_i^2 + \sigma_0^2\, S(z_i)S(z_j)\,
\exp\left(\frac{t(z_i) + t(z_j)}{t_c}\right),
$$

where \(t(z)\) is cosmic lookback time and \(S(z)\) is the BAO sensitivity kernel. This structure is fundamentally different from the stationary Ornstein–Uhlenbeck covariance used in previous work. Therefore the numerical limit \(\sigma_X < 1.5\times10^{-4}\) cannot be imported directly.

---

## 5. Maximum Likelihood Estimation on DESI DR2 Data

We perform a direct MLE on the public DESI DR2 BAO measurements (7 bins) using the physically correct rank-1 covariance above. The log-likelihood is maximised in the limit \(t_c \to \infty\) (no growth). Any finite \(t_c\) yields a significantly worse fit than pure \(\Lambda\)CDM. The data therefore exclude a globally coherent, exponentially growing tachyonic condensate at high significance.

---

## 6. Discussion and Conclusion

We have examined a dark-energy model based on a tachyonic quantum fluid with quartic self-interaction. While the mechanism is mathematically interesting and \(\Gamma_{\rm max}\) is robust, the observational analysis shows that a globally coherent growing mode is incompatible with DESI DR2 BAO data.

**Important methodological note:** The upper limit \(\sigma_X < 1.5\times10^{-4}\) obtained in the companion stationary Ornstein–Uhlenbeck analysis cannot be applied directly to this model, because the two frameworks predict qualitatively different covariance structures. The constraint derived here uses the covariance that the growing-mode model actually produces and is therefore the appropriate observational bound.

Future surveys with larger numbers of redshift bins will further tighten limits on any residual stochastic component, but this particular class of globally coherent tachyonic quantum-fluid models is already disfavoured by current data.

---

## References

[1] DESI Collaboration, arXiv:2503.14738 (2025).  
[2] Morales Souhail, J., arXiv:xxxx.xxxxx (2026) [companion OU paper].  
[3] Khamehchi et al., Phys. Rev. Lett. 118, 155301 (2017).  
[4] Sorkin, R. D., arXiv:gr-qc/0503057 (2005).  
[5] Bekenstein, J. D., Phys. Rev. D 7, 2333 (1973).
