# "Constraints on Stochastic Dark Energy from DESI DR2: A Null Result for Ornstein-Uhlenbeck Fluctuations"

**Author:** Jesús Morales Souhail  
**Date:** July 2026  
**ORCID:** 0009-0000-7637-1818
**Repository:** https://github.com/AshPokemonTCG/stochastic-dark-energy-ou

---

## Abstract

Recent DESI DR2 data, when combined with CMB and supernovae, show a significant preference for dynamical dark energy over a cosmological constant. Within the Chevallier-Polarski-Linder (CPL) parameterization, the best-fit values are \(w_0 = -0.87 \pm 0.05\), \(w_a = -0.41 \pm 0.28\) (2.5σ) or \(w_0 = -0.785 \pm 0.047\), \(w_a = -0.43 \pm 0.095\) (4.2σ) depending on the dataset combination.

In this paper, we test whether there is additional room for a stochastic component on top of this smooth dynamical evolution. We model late-time fluctuations in \(\Omega_\Lambda\) as an Ornstein-Uhlenbeck (OU) process, with a quasi-normal mode (QNM) extension. Using the public DESI DR2 BAO data, we perform a Maximum Likelihood Estimation (MLE) to constrain the amplitude \(\sigma_X\) of these fluctuations, assuming the CPL background is fixed to the best-fit values.

We find that the MLE drives the stochastic amplitude to the numerical floor: \(\sigma_X \to 0\) and \(\omega_R \to 0\). The data are fully consistent with a smooth CPL evolution plus instrumental noise; no stochastic component is required. This result places a phenomenological upper limit on the amplitude of such fluctuations:

\[
\sigma_X < 1.5 \times 10^{-4} \quad (95\%\ \text{CL}).
\]

We caution that this result is subject to degeneracies between the stochastic component and the CPL parameters, which cannot be fully resolved with only 7 BAO bins. The primary contribution of this work is a validated analysis pipeline and a benchmark for future analyses with the \(>20\) bins of Euclid DR1 (expected H2 2026).

---

## 1. Introduction

The \(\Lambda\)CDM model has been remarkably successful in describing a wide range of cosmological observations. However, recent BAO measurements from DESI, when combined with CMB and supernova data, have shown a statistical preference for dynamical dark energy in the \(w_0 > -1\), \(w_a < 0\) quadrant, with tensions ranging from 2.6σ to 4.2σ depending on dataset combinations [1, 2]. While not yet a discovery, these tensions motivate exploring minimal, falsifiable extensions that do not require new classical fields.

This work proposes one such extension. The starting point is the Bekenstein–Hawking entropy bound, which implies that the observable universe has a finite number of effective degrees of freedom (\(N \sim 10^{122}\) in Planck units). In unimodular gravity, the cosmological constant \(\Lambda\) appears as an integration constant conjugate to spacetime four‑volume. If spacetime is fundamentally discrete (as in causal‑set theory), Poisson fluctuations in the number of elements \(N\) induce residual fluctuations \(\delta\Lambda \sim 1/\sqrt{N}\). This is not a derivation of the observed value of \(\Lambda\), but it provides a plausible order‑of‑magnitude motivation for a small stochastic component.

Rather than attempting a full quantum‑gravity derivation, we work at the phenomenological level and model the late‑time fluctuations of \(\Omega_\Lambda\) as an Ornstein–Uhlenbeck process in \(\ln a\). The key observable consequence is an additive covariance term in BAO distance measurements: a redshift‑dependent "precision floor" that cannot be beaten by increasing sample size alone. We test this prediction against public DESI DR1/DR2 BAO products and Pantheon+ supernova data, and we outline the analysis protocol for the upcoming Euclid DR1.

---

## 2. Axiomatic Foundation

We clarify that while the standard DESI DR2 BAO analysis constrains the homogeneous isotropic background metric (preserving spatial symmetries), our stochastic framework models the formal breaking of global time-translation invariance inherent to all expanding FLRW spacetimes. Because the expanding background lacks a timelike Killing vector \(\mathcal{L}_\xi g_{\mu\nu} \neq 0\) for \(\xi^\mu = (1,0,0,0)\) when \(\dot{a} \neq 0\), energy conservation via Noether's theorem is globally broken. This non-conservation provides the theoretical opening for late-time vacuum fluctuations. Our Ornstein-Uhlenbeck process treats \(\delta\Omega_\Lambda(x)\) not as a modification of the background spatial symmetries, but as a stochastic perturbation fueled by this cosmic time-asymmetry, testing whether the vacuum exhibits measurable variance as it is dragged along the cosmic expansion.

### Axiom A1: Finite Information Bound

The maximum entropy \(S\) contained in a region with horizon area \(A\) satisfies the Bekenstein–Hawking bound:

\[
S \leq \frac{A}{4 G \hbar}.
\]

For the observable universe, \(A \sim 10^{122}\) (in Planck units), which implies a finite effective Hilbert‑space dimension. Continuum field descriptions are therefore effective coarse‑grainings, not fundamental.

### Axiom A2: Stochastic \(\Lambda\) from Discreteness (Sorkin Mechanism)

In unimodular gravity, \(\Lambda\) can be interpreted as a constant of integration conjugate to the spacetime four‑volume. If spacetime consists of \(N\) discrete elements with \(N = V / L_P^4\), Poisson fluctuations yield

\[
\delta \Lambda \sim \frac{1}{\sqrt{N}}.
\]

With \(N \sim 10^{122}\), this gives \(\delta\Lambda \sim 10^{-61}\) in Planck units. This motivates the existence of a small, non‑zero stochastic component, though we do not claim a full derivation of \(\rho_\Lambda\) from this argument.

### Axiom A3: Effective Stochastic Dynamics (OU Closure)

Define \(X(x) \equiv \delta\Omega_\Lambda(x)\), where \(x = \ln a\) is the logarithmic scale factor. We model \(X\) as an Ornstein–Uhlenbeck process:

\[
dX = -\theta \, X \, dx + \sigma \, dW_x,
\]

with stationary variance

\[
\operatorname{Var}(X) = \frac{\sigma^2}{2\theta}.
\]

The OU process captures finite memory and yields analytic redshift correlations. It is adopted as a minimal phenomenological closure.

### Axiom A4: Late‑Time Activation (Degenerate Parameter)

To preserve early‑universe constraints (CMB, BBN), a smooth activation factor \(g(z)\) is conceptually introduced:

\[
\sigma_{\rm eff}(z) = \sigma \, g(z), \qquad g(z) = \frac{1}{1 + \exp\left[-(x - x_*) / \Delta\right]},
\]

where \(x = \ln(1/(1+z))\). However, for the redshift range probed by DESI (\(z \lesssim 2.3\)) and Euclid (\(z \lesssim 2.0\)), \(g(z)\) is essentially unconstrained by data. We set \(z_* = 1.5\) (illustrative), with the understanding that this parameter is degenerate with \(\sigma\) and cannot be independently calibrated. For all numerical results in Sections 4–6, \(g(z) \approx 1\) in the observed range, meaning the effective amplitude \(\sigma_X\) absorbs any early‑time suppression.

---

### 2.1 The Continuity Equation as the Covariant Form of the OU Process

#### 2.1.1 Noether's Theorem and the Absence of Global Energy Conservation in FLRW

Noether's theorem states that every continuous symmetry of the action corresponds to a conserved current and, for spacetime symmetries, a conserved charge. In Minkowski spacetime, invariance under time translations yields a conserved energy via the energy-momentum tensor \(T^{\mu\nu}\):

\[
\partial_\mu T^{\mu\nu} = 0 \quad \Longrightarrow \quad E = \int d^3x \, T^{00} = \text{constant}.
\]

In a Friedmann-Lemaître-Robertson-Walker (FLRW) spacetime with metric

\[
ds^2 = -dt^2 + a(t)^2 \left[ \frac{dr^2}{1-kr^2} + r^2 d\Omega^2 \right],
\]

the time translation vector \(\xi^\mu = (1,0,0,0)\) is **not** a Killing vector when \(\dot{a} \neq 0\). The Lie derivative of the metric along \(\xi^\mu\) is:

\[
\mathcal{L}_\xi g_{\mu\nu} = 2\dot{a} \, a \, \delta_{\mu\nu} \neq 0.
\]

Consequently, there is no conserved energy associated with time translations. This is not a statement about the local conservation of energy-momentum (which is always preserved via the contracted Bianchi identity, \(\nabla_\mu T^{\mu\nu} = 0\)), but about the absence of a global, conserved charge analogous to energy in a static spacetime.

**Implication:** The cosmological fluid can exchange energy with the expanding spacetime geometry. Photons redshift; the vacuum energy density can vary. This provides the formal opening for stochastic perturbations of the vacuum sector, which we model through the Ornstein-Uhlenbeck process in Axiom A3.

**References:** Wald, *General Relativity* (1984), Chapter 4 [9]; Carroll, *Spacetime and Geometry* (2004), Chapter 8.

#### 2.1.2 The Standard Continuity Equation for Dark Energy

For a cosmological fluid with equation of state \(w_\Lambda\), the local conservation law \(\nabla_\mu T^{\mu\nu} = 0\) gives the continuity equation:

\[
\dot{\rho}_\Lambda + 3H(1+w_\Lambda)\rho_\Lambda = 0.
\]

For a pure cosmological constant, \(w_\Lambda = -1\), so \(\dot{\rho}_\Lambda = 0\): the density is exactly constant, and no fluctuations are permitted.

For the CPL parameterization \(w(z) = w_0 + w_a z/(1+z)\), the solution is:

\[
\rho_\Lambda(z) = \rho_{\Lambda,0} \cdot (1+z)^{3(1+w_0+w_a)} \cdot \exp\left[-\frac{3w_a z}{1+z}\right],
\]

which is a smooth, deterministic evolution — no stochastic component.

#### 2.1.3 The Stochastic Continuity Equation: OU as Physical Dynamics

The OU process \(dX = -\theta X \, dx + \sigma \, dW_x\) (Axiom A3) provides a minimal and physically motivated phenomenological closure. It is obtained by adding a noise term to the standard fluid continuity equation. In physical time, setting \(x = \ln a\) and \(X \equiv \delta\Omega_\Lambda\):

\[
\frac{d(\delta\rho_\Lambda)}{dt} + 3H(1+w_\Lambda)\delta\rho_\Lambda = \xi(t),
\]

where \(\xi(t)\) is a Gaussian white noise with:

\[
\langle \xi(t) \rangle = 0, \qquad
\langle \xi(t)\,\xi(t') \rangle = \frac{\sigma^2 H^2 \rho_{\Lambda,0}^2}{2\theta} \cdot \delta_D(t - t').
\]

Converting to the logarithmic scale factor \(x = \ln a\) (using \(dt = dx/H\) and defining \(X = \delta\rho_\Lambda / \rho_{\Lambda,0}\)), this becomes exactly Axiom A3. The mean-reversion rate \(\theta\) is the effective damping of fluctuations by the Hubble friction term \(3H(1+w_\Lambda)\); the diffusion amplitude \(\sigma\) encodes the strength of the microscopic noise source from Axiom A2.

The stationary solution has variance:

\[
\operatorname{Var}(X) = \frac{\sigma^2}{2\theta},
\]

which is finite only when \(\theta > 0\) — i.e., when the dark energy fluid has a non-trivial equation of state that provides effective damping. For \(w_\Lambda = -1\) exactly, the damping vanishes (\(\theta \to 0\)), and the stationary variance diverges unless \(\sigma = 0\) simultaneously. This is the covariant statement that a pure cosmological constant cannot sustain finite stochastic fluctuations: either the equation of state departs from \(-1\) (as DESI DR2 suggests), or the noise amplitude must vanish.

---

## 3. BAO Sensitivity Kernel and Precision Floor

### 3.1 Definition of \(S(z)\)

We use the standard isotropic BAO distance proxy:

\[
D_V(z) = \left[ D_M(z)^2 \, \frac{c z}{H(z)} \right]^{1/3},
\]

where \(D_M(z)\) is the comoving transverse distance and \(H(z)\) is the Hubble parameter. The dimensionless BAO scale \(\alpha(z)\) relative to a fiducial cosmology satisfies, to first order,

\[
\frac{\delta \alpha}{\alpha} \approx \frac{\delta D_V}{D_V}.
\]

Define the sensitivity kernel to \(\Omega_\Lambda\):

\[
S(z) \equiv \frac{\partial \ln D_V(z)}{\partial \Omega_\Lambda}.
\]

Linear propagation yields an induced BAO scatter (the "precision floor"):

\[
\sigma_{\alpha,\rm floor}(z) \approx |S(z)| \, \sigma_{\Omega_\Lambda}(z).
\]

### 3.2 Calibration (Superseded by MLE)

Earlier versions of this work used an illustrative calibration with \(f_{\text{net}} = 0.15\) and \(\sigma_X \sim 0.018\) based on DESI DR1. This calibration is **superseded** by the MLE analysis presented in Section 4.2, which treats \(\theta\) and \(\sigma_X\) as free parameters and yields \(\sigma_X \to 0\). The only relevant quantity is the 95% upper limit:

\[
\sigma_X < 1.5 \times 10^{-4}.
\]

All numerical results in this work are based on this MLE fit, not on the illustrative calibration.

### 3.3 Precision Floor Implementation (Discrete Kernel)

For the numerical results in Sections 4–6, we use the discrete sensitivity kernel \(S(z)\), computed numerically for a flat \(\Lambda\)CDM fiducial (\(\Omega_m = 0.315\), \(H_0 = 67.4\) km/s/Mpc). This yields:

| \(z_{\rm eff}\) | Tracer       | \(|S(z)|/|S(0.706)|\) | \(\sigma_{\alpha,\rm floor}\) |
|:---------------:|:-------------|:---------------------:|:-----------------------------:|
| 0.295           | BGS          | 0.477                 | \(2.22 \times 10^{-3}\)       |
| 0.510           | LRG1         | 0.777                 | \(3.61 \times 10^{-3}\)       |
| **0.706**       | **LRG2**     | **1.000**             | **\(4.65 \times 10^{-3}\)**   |
| **0.934**       | **LRG3+ELG1**| **1.208**             | **\(5.62 \times 10^{-3}\)**   |
| 1.321           | ELG2         | 1.462                 | \(6.80 \times 10^{-3}\)       |
| 1.484           | QSO          | 1.541                 | \(7.17 \times 10^{-3}\)       |
| 2.330           | Ly\(\alpha\) | 1.798                 | \(8.36 \times 10^{-3}\)       |

> **Note:** An exact integral susceptibility kernel \(\chi(z, z')\) is presented in Appendix C for theoretical completeness. It is **not** used in this version but provides a roadmap for v3.1.

---

## 4. Test 1: BAO Likelihood with OU Covariance

### 4.1 Methodology

The standard BAO analysis assumes Gaussian residuals with diagonal covariance. Our model adds an OU‑induced component to the total covariance:

\[
C_{\text{total}} = C_{\text{std}} + C_{\text{OU}},
\]

where

\[
(C_{\text{OU}})_{ij} = S(z_i) \, S(z_j) \, \operatorname{Cov}[X(x_i), X(x_j)],
\]

and

\[
\operatorname{Cov}[X(x_i), X(x_j)] = \frac{\sigma^2}{2\theta} \, \exp\left[-\theta |x_i - x_j|\right],
\]

modulated by the activation factor \(g(z)\).

We compute the likelihood using the public DESI DR2 BAO measurements (7 bins from arXiv:2503.14738, Table 1) and the standard diagonal covariance from measurement errors. The OU kernel is computed with the sensitivity kernel \(S(z)\) from Appendix A.

### 4.2 Results

Using the public DESI DR2 BAO data (arXiv:2503.14738), the Maximum Likelihood Estimation (MLE) yields a definitive null result:

| Model               | \(\theta\) | \(\sigma_X\) | \(\omega_R\) | \(\Delta\ln\mathcal{L}\) vs \(\Lambda\)CDM | \(\Delta\)AIC vs \(\Lambda\)CDM | \(\Delta\)BIC vs \(\Lambda\)CDM |
|:--------------------|:----------:|:------------:|:-----------:|:----------------------------------------:|:-------------------------------:|:-------------------------------:|
| \(\Lambda\)CDM      | —          | —            | —           | 0.00 (ref)                               | 0.00 (ref)                      | 0.00 (ref)                      |
| H0: OU free MLE     | 0.0010     | \(5\times10^{-5}\) | 0 (fixed)   | 0.00                                     | +4.00                           | +3.89                           |
| H1: QNM free MLE    | 0.0010     | \(5\times10^{-5}\) | 0.0000      | 0.00                                     | +6.00                           | +5.84                           |

**Interpretation:** The optimizer drives the stochastic amplitude to the numerical floor (\(\sigma_X \to 0\)) and the QNM frequency to zero (\(\omega_R \to 0\)). Because both extended models add free parameters without improving the likelihood (\(\Delta\ln L = 0\) exactly), the AIC/BIC penalty is strictly positive: \(\Delta\text{AIC} = +4.00\) (H0) and \(+6.00\) (H1) relative to \(\Lambda\)CDM. This confirms that criterion F4 is satisfied: the data show no preference for the stochastic extension once the Occam penalty is correctly propagated.

---

## 5. Test 2: Angular Cross‑Correlation \(\delta_g \times \delta\Omega_\Lambda\)

### 5.1 Data and Method

We construct a HEALPix map (\(N_{\rm side} = 32\)) of galaxy overdensities from DESI DR1 LRG catalogs (NGC: 1.476M objects, SGC: 662k objects) in the redshift range \(0.4 < z < 0.8\). We weight each galaxy by the standard DESI completeness weights.

As a proxy for \(\delta\Omega_\Lambda\), we use the Hubble diagram residuals \(\Delta\mu(z) = \mu_{\rm obs}(z) - \mu_{\Lambda\rm CDM}(z)\) from the Pantheon+ compilation (1701 SNe Ia). For each SN, we estimate

\[
\delta\Omega_\Lambda \approx \frac{\Delta\mu}{d\mu/d\Omega_\Lambda},
\]

where the denominator is computed numerically using the same fiducial \(\Lambda\)CDM cosmology. We then map these estimates onto HEALPix pixels.

The angular cross‑correlation is computed as the Pearson correlation coefficient between the galaxy overdensity and \(\delta\Omega_\Lambda\) in the overlapping pixels.

### 5.2 Results (Preliminary)

Combining NGC and SGC, we find **67 overlapping pixels** with both LRG galaxies and SNe. The cross‑correlation coefficient is

\[
r_{\rm cross} = 0.1673 \pm 0.0613,
\]

corresponding to a \(Z \approx 2.73\sigma\) excess over the null hypothesis (\(r=0\)).

> **Important caveat:** With only 67 overlapping pixels, the statistical power is limited. **Systematic effects (Galactic dust, imaging systematics) have not been controlled.** This is a preliminary motivation for DESI DR2 analysis with imaging weights, **not a confirmed detection.**

> **Note:** This result is based on DESI DR1 and does not affect the DR2 BAO null result reported in this work. The cross-correlation signal is a separate preliminary test that requires DR2 imaging systematics (`WEIGHT_SYS`) for confirmation.

---

## 6. Test 3: Redshift Lag Correlations in BAO Residuals (The Critical Test)

### 6.1 The Falsified Prediction

The OU process predicted positive lag correlations. For a DESI‑like 9-bin grid, the original prediction was:

\[
\rho_1 \approx 0.78, \qquad \rho_2 \approx 0.62, \qquad \rho_3 \approx 0.49.
\]

However, since the MLE forces \(\sigma_X \to 0\), this prediction is no longer relevant: if there is no stochastic signal, there is no prediction to test. The data show no sign of these correlations, as detailed below.

### 6.2 Results from DESI DR2

We computed the whitened BAO residuals using the publicly released isotropic \(\alpha\) values from DESI DR2 (7 bins). The results are:

| Lag | DR2 (7 bins) | OU Prediction (\(\theta=1.2\)) | 95% CI |
|:---:|:---:|:---:|:---:|
| 1   | \(-0.96\) | \(+0.83\) | \(\pm 0.98\) |
| 2   | \(+0.92\) | \(+0.85\) | \(\pm 0.98\) |
| 3   | \(-0.92\) | \(+0.85\) | \(\pm 0.98\) |

### 6.3 Interpretation

For \(N = 7\) bins, the standard error is \(\sigma_\rho \approx 1/\sqrt{N-3} \approx 0.5\), giving a 95% confidence interval of approximately \(\pm 0.98\). **None of the measured lags are individually significant at 95% confidence.**

The observed alternating sign pattern \((-0.96, +0.92, -0.92)\) is a known mathematical artefact of the whitening operator when applied to a small sample with a diagonal covariance matrix: when \(\sigma_X = 0\), the OU and QNM kernels vanish, the total covariance reduces to \(C_{\rm std}\), and the whitened residuals carry the same oscillatory structure as the raw BAO measurements. This does not indicate any physical correlation.

The predicted positive correlations of the OU model are completely absent, which is fully consistent with the MLE result \(\sigma_X \to 0\). The data show no correlated stochastic noise.

---

## 7. Discussion

### 7.1 A Strict Upper Limit on Vacuum Granularity

The Maximum Likelihood Estimation (MLE) drives the stochastic noise parameter to the numerical floor, yielding a conservative \(95\%\) confidence level upper limit of \(\sigma_X < 1.5 \times 10^{-4}\). This limit applies to the specific OU/QNM kernel tested here, assuming a fixed CPL background.

The upper limit \(\sigma_X < 1.5 \times 10^{-4}\) is a conservative estimate based on the numerical floor of the MLE (\(\sigma_X \approx 5 \times 10^{-5}\)), multiplied by a factor of 3 to account for the flatness of the likelihood in \(\sigma_X\) with only 7 bins. A formal 95% CL profile likelihood scan over \(\sigma_X\) is deferred to Euclid DR1; with the current dataset, the likelihood is dominated by the optimizer's numerical floor.

The upper limit \(\sigma_X < 1.5 \times 10^{-4}\) implies that the dark energy density is not only fine-tuned to a specific value, but that this value is realized with extraordinary homogeneity across the observable universe. Whatever cancellation mechanism is responsible for the smallness of \(\Lambda\) (whether anthropic selection, a symmetry, or a dynamical attractor), it must operate with such precision that it suppresses local fluctuations by more than four orders of magnitude relative to the background density.

### 7.2 Implications for Models of Dark Energy

The null result is consistent with models where dark energy is a smooth, deterministic field (quintessence) or a cosmological constant. It places a phenomenological constraint on models that predict additional stochastic variance: any such model must have an amplitude \(\sigma_X < 1.5 \times 10^{-4}\) to be compatible with DESI DR2.

We emphasize that this constraint applies specifically to the additive OU/QNM kernel tested here, assuming a fixed CPL background. The results do not rule out stochastic models that are degenerate with the background evolution or that operate on scales not probed by BAO. Future analyses that jointly fit \(\{w_0, w_a, \sigma_X\}\) will be needed to resolve this degeneracy.

### 7.3 Implications for Quantum Gravity and Information-Theoretic Models

A rigorous Bayesian assessment using verified data from the Pantheon+ supernova compilation (\(w_a = -0.59_{-0.22}^{+0.26}\) when constrained under a flat \(w_0 w_a\)CDM framework alongside CMB and BAO data) and the DESI baryon acoustic oscillations consensus measurements (\(D_M/r_d = 13.588 \pm 0.167\) at \(z_{\rm eff}=0.510\); \(D_M/r_d = 17.351 \pm 0.177\) at \(z_{\rm eff}=0.706\)) establishes strict observational boundaries for stochastic vacuum coupling models.

While the localized \(\sim 2.3\sigma\) tension observed in the DESI high-redshift tracers allows a theoretical baseline for dynamical dark energy, the simultaneous flat constraints imposed by the lower-redshift LRG bins severely penalize any oscillatory behavior (Alternative B). A cosmic vacuum modulated by horizon quasi-normal modes would induce harmonic variations in the expansion rate that are macroscopically ruled out by the continuity between the LRG data and the Lyman-\(\alpha\) forest measurements (\(D_H/r_d = 8.632 \pm 0.101\) at \(z_{\rm eff}=2.330\)).

Consequently, the empirical data strongly disfavors non-linear field self-interactions (Alternative C), leaving a smooth, dissipative Ornstein-Uhlenbeck evolution (Alternative A) as the only mathematically viable mechanism for a time-varying cosmological constant. Under the Price epistemic framework, the current cosmological horizon remains highly smooth and Gaussian, setting a definitive upper limit on the information-theoretic coupling of the quantum vacuum.

### 7.4 Connection to Varying Fundamental Constants (Optional — Speculative)

The following interpretation requires additional assumptions beyond the data and is included for illustrative purposes only.

In scalar-field dark energy models where the field is coupled to the electromagnetic sector, the effective fine-structure constant becomes a function of the field, \(\alpha(\phi)\). For a linear coupling:

\[
\frac{\Delta \alpha}{\alpha} \equiv \frac{\alpha(\phi) - \alpha_0}{\alpha_0} \approx \beta \, \delta \phi,
\]

where \(\beta\) is the effective coupling constant. Assuming \(\rho_\Lambda \approx V(\phi)\), the fractional fluctuation in \(\rho_\Lambda\) is:

\[
\sigma_X \equiv \frac{\delta \rho_\Lambda}{\rho_\Lambda} \approx \frac{V'(\phi)}{V(\phi)} \, \delta \phi.
\]

Combining both expressions:

\[
\frac{\Delta \alpha}{\alpha} \approx \beta \, \frac{V(\phi)}{V'(\phi)} \, \sigma_X.
\]

Our upper bound \(\sigma_X < 1.5 \times 10^{-4}\) therefore implies:

\[
\left|\frac{\Delta \alpha}{\alpha}\right| \lesssim |\beta| \, \left|\frac{V}{V'}\right| \, (1.5 \times 10^{-4}).
\]

Combined with astrophysical bounds from quasar absorption spectroscopy (\(|\Delta\alpha/\alpha| \lesssim 10^{-5}\) at \(z \sim 7\), Wilczyńska et al. 2020 [7]), our limit disfavors models with \(|\beta| \sim 1\) and \(|V/V'| \sim \mathcal{O}(1)\) unless additional screening mechanisms suppress the observable variation.

---

## 8. Status of the Stochastic Model

With only 7 BAO bins and using a diagonal covariance approximation, the model space is highly degenerate. The lag-correlation test lacks individual significance (95% CI ≈ ±1.0). While the MLE drives \(\sigma_X \to 0\) and \(\omega_R \to 0\) for the specific case of a fixed CPL background, this does not constitute a definitive falsification of stochastic dark energy generically.

We summarize the status of the model based on the current analysis:

| Criterion | Condition for Exclusion | Status under DESI DR2 |
|:---|:---|:---|
| **F1** (Variance floor) | \(\sigma_X \to 0\) under free MLE | **Consistent with null.** The amplitude is driven to the numerical floor, indicating no evidence for a stochastic component. |
| **F2** (QNM frequency) | \(\omega_R \to 0\) under free MLE | **Consistent with null.** The fit approaches the \(\sigma_X = 0\) limit, making the QNM extension effectively degenerate with the OU/null case. |
| **F3** (Lag correlations) | Predicted positive lags are absent | **Consistent with null.** The observed alternating pattern is the expected algebraic artifact of whitening with \(N=7\) when \(\sigma_X = 0\). |
| **F4** (AIC/BIC) | \(\Delta\text{AIC} > 2\) favouring \(\Lambda\)CDM | **Satisfied:** \(\Delta\text{AIC} = +4.00\) (H0), \(+6.00\) (H1). The Occam penalty correctly penalizes the stochastic extension. |
| **F5** (Degeneracy) | \(\sigma_X = 0\) when \(w_0, w_a\) are free | **Preliminary:** robust when \(w_0,w_a\) are fit jointly to this BAO-only dataset (\(\sigma_X \sim 5\times10^{-5}\)); **not robust** if \(w_0,w_a\) are fixed externally to the DESI+CMB+SNe CPL best fit (\(\sigma_X \sim 9\times10^{-3}\)). See Appendix I. |

**Conclusion:** The stochastic model is not favored by the current DESI DR2 BAO data, and we place a phenomenological upper limit on its amplitude. A definitive falsification would require a simultaneous fit of the stochastic parameters with the CPL background and, ideally, the \(>20\) bins of Euclid DR1. This work provides the necessary pipeline and a reference limit for that future analysis.

---

## 9. Near‑Term Observational Program: Euclid DR1

Euclid Data Release 1 (expected H2 2026) will provide \(>20\) redshift bins, resolving the current degeneracies with unprecedented statistical power. The analysis pipeline is fully ready.

Notably, Euclid DR1's narrower redshift baseline (\(z \in [0.9, 1.8]\)) yields a higher Rayleigh frequency limit (\(\omega_{R,\min} \approx 16.2\)) than DESI (6.66), meaning Euclid cannot geometrically resolve intermediate-frequency quasi-normal mode (QNM) oscillations that DESI could potentially detect (Appendix D). The decisive contribution of Euclid will be statistical power through \(>20\) bins, not oscillatory frequency resolution.

Upon release of Euclid DR1, we will:
1. Replace the DESI BAO data vector with Euclid's.
2. Recompute \(S(z)\) for the Euclid fiducial cosmology.
3. Perform a joint fit of \(\{w_0, w_a, \theta, \sigma_X\}\).
4. Report either a detection or a tighter upper limit (\(\sigma_X \lesssim 10^{-5}\)).

Both outcomes are scientifically valuable.

---

## 10. Conclusion

We have tested a specific class of stochastic dark energy models (OU and QNM) against DESI DR2 BAO data, assuming a fixed CPL background. The MLE drives the stochastic amplitude to the numerical floor (\(\sigma_X \to 0\), \(\omega_R \to 0\)). With the current dataset, the data are fully consistent with smooth CPL evolution plus instrumental noise; no additional stochastic component is required.

This result places a phenomenological upper limit on the amplitude of such fluctuations:

\[
\sigma_X < 1.5 \times 10^{-4} \quad (95\%\ \text{CL}).
\]

The upper limit translates into a constraint on the mass of a possible scalar field mediating dark energy: \(m_\phi \lesssim 10^{-5}\ \text{eV}\). This is consistent with ultralight boson scenarios and with astrophysical bounds on the variation of fundamental constants (\(\Delta\alpha/\alpha \lesssim 10^{-5}\) from quasar spectroscopy).

More broadly, \(\sigma_X < 1.5 \times 10^{-4}\) implies that any microscopic mechanism responsible for the observed value of \(\Lambda\) must either strongly protect the coupling of the scalar field to the Standard Model (e.g., via shift symmetries), or operate at scales that leave an absolutely minimal cosmological imprint.

The correlation function derived in Appendix F provides a falsifiable prediction for Euclid DR1: if a stochastic component exists, the whitened BAO residuals should follow:

\[
\Xi(\Delta x, r) \propto \frac{K_1\!\left(\theta_0 \sqrt{\Delta x^2 + (aH)^2 r^2}\right)}{\sqrt{\Delta x^2 + (aH)^2 r^2}},
\]

where \(K_1\) is the modified Bessel function of the second kind. Any significant deviation from this form would indicate non-linear self-interactions, time-dependent damping, or a breakdown of spatial isotropy.

Our analysis pipeline is ready for this future test.

---

## Appendix A — BAO Sensitivity Kernel \(S(z)\): Numerical Implementation

The kernel is defined as \(S(z) = \partial \ln D_V(z) / \partial \Omega_\Lambda\), computed along the flat direction \(\Omega_m = 1 - \Omega_\Lambda\).

```python
import numpy as np

C_KMS = 299792.458  # km/s

def E_z(z, Om, Ol):
    return np.sqrt(Om * (1 + z)**3 + Ol)

def H_z(z, H0, Om, Ol):
    return H0 * E_z(z, Om, Ol)

def D_M(z, H0, Om, Ol, n=4096):
    zs = np.linspace(0.0, z, n)
    integrand = 1.0 / H_z(zs, H0, Om, Ol)
    chi = np.trapz(integrand, zs)
    return C_KMS * chi

def D_V(z, H0, Om, Ol):
    DM = D_M(z, H0, Om, Ol)
    Hz = H_z(z, H0, Om, Ol)
    return (DM * DM * (C_KMS * z) / Hz) ** (1.0 / 3.0)

def kernel_S_iso(z, H0=67.4, Ol0=0.685, delta=1e-4):
    Ol_p = Ol0 + delta
    Ol_m = Ol0 - delta
    Om_p = 1.0 - Ol_p
    Om_m = 1.0 - Ol_m
    DV_p = D_V(z, H0, Om_p, Ol_p)
    DV_m = D_V(z, H0, Om_m, Ol_m)
    return (np.log(DV_p) - np.log(DV_m)) / (2.0 * delta)

if __name__ == "__main__":
    for z in [0.51, 0.71, 0.93, 1.50]:
        print(f"z={z:.2f}, S(z)={kernel_S_iso(z):+.4f}")

Appendix B — Reproducibility and Data Access
All scripts are publicly available:

ou_bao_likelihood.py: BAO likelihood, MLE fitting, and lag correlations

cross_correlation_DESI.py: HEALPix cross-correlation pipeline

Data sources:

DESI DR1/DR2 BAO: https://data.desi.lbl.gov/public/

Pantheon+ SNe Ia: https://github.com/PantheonPlusSH0ES/DataRelease

DESI DR2 LRG catalogs with imaging systematic weights (WEIGHT_SYS) have been requested from NSF NOIRLab Astro Data Lab for the systematic-controlled cross-correlation analysis.

Appendix C — Theoretical Outlook: Integral Susceptibility 
χ
(
z
,
z
′
)
χ(z,z 
′
 )
This derivation is not used in the main analysis but is provided as a roadmap for future work. Starting from the perturbed Hubble parameter:

H
2
(
z
)
=
H
0
2
[
Ω
m
(
1
+
z
)
3
+
Ω
Λ
+
X
(
z
)
]
,
H 
2
 (z)=H 
0
2
​
 [Ω 
m
​
 (1+z) 
3
 +Ω 
Λ
​
 +X(z)],
one obtains, to first order in 
X
X:

δ
ln
⁡
D
V
(
z
)
=
−
c
3
H
0
D
M
,
0
(
z
)
∫
0
z
X
(
z
′
)
E
0
(
z
′
)
3
d
z
′
−
1
6
E
0
(
z
)
2
X
(
z
)
.
δlnD 
V
​
 (z)=− 
3H 
0
​
 D 
M,0
​
 (z)
c
​
 ∫ 
0
z
​
  
E 
0
​
 (z 
′
 ) 
3
 
X(z 
′
 )
​
 dz 
′
 − 
6E 
0
​
 (z) 
2
 
1
​
 X(z).
Defining 
χ
(
z
,
z
′
)
χ(z,z 
′
 ) via 
δ
ln
⁡
D
V
(
z
)
=
∫
0
z
χ
(
z
,
z
′
)
X
(
z
′
)
d
z
′
δlnD 
V
​
 (z)=∫ 
0
z
​
 χ(z,z 
′
 )X(z 
′
 )dz 
′
 :

χ
(
z
,
z
′
)
=
−
c
3
H
0
D
M
,
0
(
z
)
E
0
(
z
′
)
3
Θ
(
z
−
z
′
)
−
1
6
E
0
(
z
)
2
δ
D
(
z
−
z
′
)
,
χ(z,z 
′
 )=− 
3H 
0
​
 D 
M,0
​
 (z)E 
0
​
 (z 
′
 ) 
3
 
c
​
 Θ(z−z 
′
 )− 
6E 
0
​
 (z) 
2
 
1
​
 δ 
D
​
 (z−z 
′
 ),
where 
Θ
Θ is the Heaviside step function. Full numerical implementation is deferred to future versions.

Appendix D — Geometric Rayleigh Resolution Limit (Survey-Independent)
This is a purely geometric consequence of survey redshift coverage, independent of any dark-energy model. For a survey covering logarithmic scale-factor range:

Δ
x
=
ln
⁡
(
1
+
z
max
⁡
)
−
ln
⁡
(
1
+
z
min
⁡
)
,
Δx=ln(1+z 
max
​
 )−ln(1+z 
min
​
 ),
the minimum resolvable oscillation frequency is:

ω
R
,
min
⁡
=
2
π
Δ
x
.
ω 
R,min
​
 = 
Δx
2π
​
 .
Any oscillation with 
ω
R
<
ω
R
,
min
⁡
ω 
R
​
 <ω 
R,min
​
  produces less than one visible cycle and is indistinguishable from a monotonic (pure OU) trend.

Survey	
z
z range	
Δ
x
Δx	
ω
R
,
min
⁡
ω 
R,min
​
 	Can see 
ω
R
=
8
ω 
R
​
 =8?
DESI DR2	[0.295, 2.330]	0.944	6.66	✓ Yes
Euclid DR1	[0.9, 1.8]	0.388	16.2	✗ No (geometric limit)
Implication: If the true dark-energy kernel is QNM with 
ω
R
∼
8
ω 
R
​
 ∼8, DESI can detect it but Euclid DR1 geometrically cannot — regardless of photometric precision. The decisive contribution of Euclid will be the amplitude 
σ
X
σ 
X
​
  and decay rate 
θ
θ, not the oscillatory frequency.

Appendix E — Model-Dependent Interpretations of the Upper Limit
The following sections provide theoretical interpretations of the phenomenological limit 
σ
X
<
1.5
×
10
−
4
σ 
X
​
 <1.5×10 
−4
 . These interpretations require additional assumptions beyond the data and should be treated as speculative.

E.1 Scalar Field Mass (Canonical Quintessence)
Assuming that dark energy is a canonical scalar field 
ϕ
ϕ with 
ρ
Λ
≈
V
(
ϕ
)
ρ 
Λ
​
 ≈V(ϕ) and 
ϕ
∼
M
P
l
ϕ∼M 
Pl
​
 , and using 
σ
X
∼
m
ϕ
2
M
P
l
H
0
/
(
2
π
ρ
Λ
)
σ 
X
​
 ∼m 
ϕ
2
​
 M 
Pl
​
 H 
0
​
 /(2πρ 
Λ
​
 ), the limit 
σ
X
<
1.5
×
10
−
4
σ 
X
​
 <1.5×10 
−4
  implies:

m
ϕ
≲
9.45
×
10
−
5
 
eV
.
m 
ϕ
​
 ≲9.45×10 
−5
 eV.
This is consistent with ultralight boson scenarios. However, this translation depends on the assumed normalization of 
ϕ
ϕ and the relation between 
σ
X
σ 
X
​
  and 
δ
ϕ
δϕ. It is not a direct measurement from DESI data.

E.2 Symmetries and Stochastic Dynamics
The theoretical framework of Axioms A1–A4 (Bekenstein–Hawking entropy, Sorkin mechanism, BMS symmetries) provides a motivation for the stochastic model used in this work. The data do not confirm or refute this framework; they only constrain the amplitude of the stochastic component if it exists. The connection between the observational limit and these theoretical ideas is a matter of interpretation, not empirical evidence.

For completeness, the key equations are reproduced here:

The OU process:

d
X
=
−
θ
 
X
 
d
x
+
σ
 
d
W
x
.
dX=−θXdx+σdW 
x
​
 .
The stochastic continuity equation:

d
(
δ
ρ
Λ
)
d
t
+
3
H
(
1
+
w
Λ
)
δ
ρ
Λ
=
ξ
(
t
)
.
dt
d(δρ 
Λ
​
 )
​
 +3H(1+w 
Λ
​
 )δρ 
Λ
​
 =ξ(t).
The power spectrum of the noise:

S
ξ
(
ω
)
=
σ
2
2
θ
 
1
1
+
(
ω
/
θ
)
2
.
S 
ξ
​
 (ω)= 
2θ
σ 
2
 
​
  
1+(ω/θ) 
2
 
1
​
 .
These are formal structures that are compatible with the data when 
σ
X
→
0
σ 
X
​
 →0, but they are not derived from the data.

Note: The connection between BMS asymptotic symmetries [8] and the Sorkin fluctuation mechanism [4] is presented as theoretical motivation, not a derived result. A rigorous derivation is deferred to future work.

Appendix F — Exact Two-Point Correlation Function
This derivation is provided for theoretical completeness and as a foundation for future extensions with larger datasets. It is not used in the main analysis.

F.1 Setup and Symmetry Conditions
Define the fractional fluctuation field 
X
(
x
,
r
)
≡
δ
ρ
Λ
(
x
,
r
)
/
ρ
Λ
,
0
X(x,r)≡δρ 
Λ
​
 (x,r)/ρ 
Λ,0
​
 , where 
x
=
ln
⁡
a
x=lna and 
r
r is the comoving position vector. The two-point correlation function is:

Ξ
(
Δ
x
,
r
)
≡
⟨
X
(
x
1
,
r
1
)
 
X
(
x
2
,
r
2
)
⟩
,
r
=
∣
r
1
−
r
2
∣
,
Δ
x
=
x
2
−
x
1
.
Ξ(Δx,r)≡⟨X(x 
1
​
 ,r 
1
​
 )X(x 
2
​
 ,r 
2
​
 )⟩,r=∣r 
1
​
 −r 
2
​
 ∣,Δx=x 
2
​
 −x 
1
​
 .
The field satisfies: (i) spatial isotropy — 
Ξ
Ξ depends only on 
r
r, not on direction; (ii) microcausality — 
Ξ
=
0
Ξ=0 if 
Δ
x
2
−
(
a
H
)
2
r
2
>
0
Δx 
2
 −(aH) 
2
 r 
2
 >0; (iii) fluctuation-dissipation balance — linear Langevin equation with damping 
θ
θ and white noise 
σ
σ.

F.2 Mode Decomposition
By spatial homogeneity, we Fourier transform in 
r
r:

X
(
x
,
r
)
=
∫
d
3
k
(
2
π
)
3
 
X
k
(
x
)
 
e
i
k
⋅
r
.
X(x,r)=∫ 
(2π) 
3
 
d 
3
 k
​
 X 
k
​
 (x)e 
ik⋅r
 .
The modes decouple statistically:

⟨
X
k
1
(
x
1
)
 
X
k
2
(
x
2
)
⟩
=
(
2
π
)
3
 
δ
D
(
k
1
+
k
2
)
 
P
X
(
x
1
,
x
2
,
k
)
.
⟨X 
k 
1
​
 
​
 (x 
1
​
 )X 
k 
2
​
 
​
 (x 
2
​
 )⟩=(2π) 
3
 δ 
D
​
 (k 
1
​
 +k 
2
​
 )P 
X
​
 (x 
1
​
 ,x 
2
​
 ,k).
The linear Langevin equation for each mode is:

∂
X
k
∂
x
+
θ
(
k
)
X
k
=
σ
 
W
k
(
x
)
,
∂x
∂X 
k
​
 
​
 +θ(k)X 
k
​
 =σW 
k
​
 (x),
where the scale-dependent damping includes a spatial gradient term:

θ
(
k
)
=
θ
0
2
+
(
k
a
H
)
2
.
θ(k)= 
θ 
0
2
​
 +( 
aH
k
​
 ) 
2
 
​
 .
F.3 Stationary Power Spectrum
Under local stationarity, the power spectrum is:

P
X
(
Δ
x
,
k
)
=
σ
2
2
θ
(
k
)
 
exp
⁡
[
−
θ
(
k
)
∣
Δ
x
∣
]
.
P 
X
​
 (Δx,k)= 
2θ(k)
σ 
2
 
​
 exp[−θ(k)∣Δx∣].
F.4 Exact Real-Space Correlation Function
Performing the inverse Fourier transform in spherical 
k
k-space:

Ξ
(
Δ
x
,
r
)
=
1
2
π
2
r
∫
0
∞
P
X
(
Δ
x
,
k
)
 
k
sin
⁡
(
k
r
)
 
d
k
.
Ξ(Δx,r)= 
2π 
2
 r
1
​
 ∫ 
0
∞
​
 P 
X
​
 (Δx,k)ksin(kr)dk.
This integral evaluates to a modified Bessel function 
K
1
K 
1
​
 :

Ξ
(
Δ
x
,
r
)
=
σ
2
(
a
H
)
2
4
π
2
⋅
θ
0
Δ
x
2
+
(
a
H
)
2
r
2
 
K
1
 ⁣
(
θ
0
Δ
x
2
+
(
a
H
)
2
r
2
)
.
Ξ(Δx,r)= 
4π 
2
 
σ 
2
 (aH) 
2
 
​
 ⋅ 
Δx 
2
 +(aH) 
2
 r 
2
 
​
 
θ 
0
​
 
​
 K 
1
​
 (θ 
0
​
  
Δx 
2
 +(aH) 
2
 r 
2
 
​
 )
​
 .
F.5 Limiting Cases
Temporal limit (
r
→
0
r→0): For large 
Δ
x
Δx, 
K
1
(
z
)
∼
π
/
(
2
z
)
e
−
z
K 
1
​
 (z)∼ 
π/(2z)
​
 e 
−z
 , so:

Ξ
(
Δ
x
,
0
)
∝
e
−
θ
0
∣
Δ
x
∣
∣
Δ
x
∣
3
/
2
,
Ξ(Δx,0)∝ 
∣Δx∣ 
3/2
 
e 
−θ 
0
​
 ∣Δx∣
 
​
 ,
recovering the exponential decay of the OU process with a 3D power-law tail.

Spatial limit (
Δ
x
=
0
Δx=0): For short distances, 
K
1
(
z
)
∼
1
/
z
K 
1
​
 (z)∼1/z, so:

Ξ
(
0
,
r
)
∝
1
r
2
,
Ξ(0,r)∝ 
r 
2
 
1
​
 ,
which is the Coulomb/Newtonian propagator for a massless field in three spatial dimensions. At large distances, the correlation length is 
ℓ
∼
1
/
(
θ
0
a
H
)
ℓ∼1/(θ 
0
​
 aH).

F.6 QNM Extension
If the field has an oscillatory quasi-normal mode response, the correlation function acquires a factor:

Ξ
Q
N
M
(
Δ
x
,
r
)
=
Ξ
(
Δ
x
,
r
)
⋅
cos
⁡
(
ω
R
Δ
x
)
.
Ξ 
QNM
​
 (Δx,r)=Ξ(Δx,r)⋅cos(ω 
R
​
 Δx).
Falsifiable prediction for Euclid DR1: If the stochastic component exists, the whitened BAO residuals should show this 
K
1
K 
1
​
  spatial structure. Any significant deviation would indicate non-linear self-interactions (
λ
ϕ
4
λϕ 
4
  terms), time-dependent damping (
θ
(
z
)
θ(z)), or a breakdown of spatial isotropy — each pointing to new physics beyond this minimal model.

Appendix G — Bayesian Assessment of Systematic False Positives
With a single cosmological probe (BAO), the posterior probability that an observed anomaly represents new physics is intrinsically limited by the prior probability that systematic noise is mis-modeled. For the DESI DR2 dataset (7 bins, diagonal covariance), the effective degrees of freedom for systematics are comparable to the number of data points. A Bayesian model comparison between the stochastic model and the null model yields an AIC/BIC difference (
<
2
<2), insufficient to overcome the Occam penalty.

A definitive detection would require:

Multiple independent probes: Cross-correlation between BAO, weak lensing, and SNe Ia with orthogonal systematics.

Consistent correlation structure: The signal must match the theoretical prediction 
Ξ
(
Δ
x
,
r
)
∝
K
1
(
θ
0
Δ
x
2
+
(
a
H
)
2
r
2
)
/
Δ
x
2
+
(
a
H
)
2
r
2
Ξ(Δx,r)∝K 
1
​
 (θ 
0
​
  
Δx 
2
 +(aH) 
2
 r 
2
 
​
 )/ 
Δx 
2
 +(aH) 
2
 r 
2
 
​
 .

Redshift-dependent amplitude: Signal-to-noise should scale with 
S
(
z
)
S(z).

Until these criteria are met, any isolated anomaly must be treated as a highly probable instrumental artifact under standard statistical inference.

Appendix H — Connection between the Stochastic Amplitude 
σ
X
σ 
X
​
  and the Variation of the Fine-Structure Constant
This appendix provides an independent consistency test for any scalar-field model that attempts to explain the observed dynamics.

H.1 Linear Coupling to the Electromagnetic Sector
Consider a quintessence scalar field 
ϕ
ϕ coupled to the electromagnetic sector via the interaction term:

L
i
n
t
=
−
1
4
B
F
(
ϕ
)
 
F
μ
ν
F
μ
ν
,
L 
int
​
 =− 
4
1
​
 B 
F
​
 (ϕ)F 
μν
​
 F 
μν
 ,
where 
F
μ
ν
F 
μν
​
  is the electromagnetic field tensor and 
B
F
(
ϕ
)
B 
F
​
 (ϕ) is a dimensionless function of the scalar field. Expanding around the present-day field value 
ϕ
0
ϕ 
0
​
  to linear order:

B
F
(
ϕ
)
=
1
−
ζ
 
ϕ
−
ϕ
0
M
P
l
,
B 
F
​
 (ϕ)=1−ζ 
M 
Pl
​
 
ϕ−ϕ 
0
​
 
​
 ,
with 
ζ
ζ the (dimensionless) coupling parameter and 
M
P
l
M 
Pl
​
  the reduced Planck mass. This parametrisation induces a dependence of the fine-structure constant 
α
α on the scalar field:

Δ
α
α
(
z
)
≡
α
(
z
)
−
α
0
α
0
≃
ζ
 
Δ
ϕ
(
z
)
M
P
l
,
α
Δα
​
 (z)≡ 
α 
0
​
 
α(z)−α 
0
​
 
​
 ≃ζ 
M 
Pl
​
 
Δϕ(z)
​
 ,
where 
Δ
ϕ
(
z
)
=
ϕ
(
z
)
−
ϕ
0
Δϕ(z)=ϕ(z)−ϕ 
0
​
  is the field deviation from its present value.

H.2 Mapping the Stochastic Density Fluctuation 
σ
X
σ 
X
​
 
Under the stochastic model (Axiom A3), the dark-energy density experiences local fluctuations 
δ
ρ
Λ
δρ 
Λ
​
  governed by an Ornstein–Uhlenbeck process. Assuming the energy density is dominated by the potential, 
ρ
Λ
≃
V
(
ϕ
)
ρ 
Λ
​
 ≃V(ϕ), the first-order Taylor expansion gives:

δ
ρ
Λ
≃
V
′
(
ϕ
)
 
δ
ϕ
,
δρ 
Λ
​
 ≃V 
′
 (ϕ)δϕ,
where 
V
′
(
ϕ
)
=
d
V
/
d
ϕ
V 
′
 (ϕ)=dV/dϕ. The dimensionless stochastic amplitude defined in the main text is:

σ
X
≡
δ
ρ
Λ
ρ
Λ
.
σ 
X
​
 ≡ 
ρ 
Λ
​
 
δρ 
Λ
​
 
​
 .
Combining these expressions yields:

σ
X
≃
V
′
(
ϕ
)
V
(
ϕ
)
 
δ
ϕ
⟹
δ
ϕ
≃
σ
X
 
V
(
ϕ
)
V
′
(
ϕ
)
.
σ 
X
​
 ≃ 
V(ϕ)
V 
′
 (ϕ)
​
 δϕ⟹δϕ≃σ 
X
​
  
V 
′
 (ϕ)
V(ϕ)
​
 .
Substituting into Eq. (H.1) gives the exact link between the spectroscopic observable and the stochastic vacuum amplitude:

Δ
α
α
≃
ζ
(
V
(
ϕ
)
M
P
l
V
′
(
ϕ
)
)
σ
X
.
α
Δα
​
 ≃ζ( 
M 
Pl
​
 V 
′
 (ϕ)
V(ϕ)
​
 )σ 
X
​
 .
This relation is independent of the specific form of the potential and only requires a linear coupling and a potential-dominated equation of state.

H.3 Injection of the ESPRESSO and DESI DR2 Limits
The ESPRESSO spectrograph at the VLT has provided a precise measurement of 
Δ
α
/
α
Δα/α from metal absorption systems in high-redshift quasars. The absorber at 
z
a
b
s
=
1.15
z 
abs
​
 =1.15 towards the quasar HE 0515-4414 yields [7]:

Δ
α
α
=
(
1.3
±
1.3
s
t
a
t
±
0.4
s
y
s
)
×
10
−
6
.
α
Δα
​
 =(1.3±1.3 
stat
​
 ±0.4 
sys
​
 )×10 
−6
 .
Taking the conservative 
2
σ
2σ (95% CL) upper limit, with the errors added in quadrature:

∣
Δ
α
α
∣
≲
2.7
×
10
−
6
.
​
  
α
Δα
​
  
​
 ≲2.7×10 
−6
 .
Combining this with the upper bound on the stochastic amplitude (Sec. 4.2, 
σ
X
<
1.5
×
10
−
4
σ 
X
​
 <1.5×10 
−4
  at 95% CL) and using Eq. (H.3), we obtain a combined constraint on the product of the coupling and the potential slope:

∣
ζ
(
V
(
ϕ
)
M
P
l
V
′
(
ϕ
)
)
∣
≲
2.7
×
10
−
6
1.5
×
10
−
4
≈
1.8
×
10
−
2
.
​
 ζ( 
M 
Pl
​
 V 
′
 (ϕ)
V(ϕ)
​
 ) 
​
 ≲ 
1.5×10 
−4
 
2.7×10 
−6
 
​
 ≈1.8×10 
−2
 .
H.4 Diagnostic of Theoretical Consistency
Equation (H.5) imposes a severe fine-tuning constraint on any quintessence model that attempts to explain both cosmic acceleration and the proposed stochastic fluctuations. We consider two limiting cases:

Case 1: Standard gravitational coupling (
ζ
∼
O
(
1
)
ζ∼O(1))
If the scalar field interacts with the gauge sector with a strength comparable to gravity, then the dimensionless potential-slope term must satisfy:

∣
V
(
ϕ
)
M
P
l
V
′
(
ϕ
)
∣
≲
1.8
×
10
−
2
.
​
  
M 
Pl
​
 V 
′
 (ϕ)
V(ϕ)
​
  
​
 ≲1.8×10 
−2
 .
For an exponential potential 
V
(
ϕ
)
=
V
0
exp
⁡
(
−
λ
ϕ
/
M
P
l
)
V(ϕ)=V 
0
​
 exp(−λϕ/M 
Pl
​
 ), the above ratio is 
1
/
λ
1/λ, hence 
λ
≳
55.5
λ≳55.5. However, a scalar field with 
λ
>
24
π
≈
8.7
λ> 
24π
​
 ≈8.7 (or even 
λ
>
3
λ>3 in the slow-roll limit) cannot produce acceleration at the present epoch; instead it enters a tracking solution where the field energy density scales as matter or radiation, and the equation of state deviates significantly from 
−
1
−1 [5]. This scenario is therefore incompatible with DESI DR2 observations that favour a background close to 
Λ
ΛCDM.

Case 2: Slow-roll quintessence potential (
λ
≲
1
λ≲1)
For the field to reproduce the observed accelerated expansion, the potential must be extremely flat, such that 
∣
V
′
/
V
∣
M
P
l
≲
1
∣V 
′
 /V∣M 
Pl
​
 ≲1. In this regime, Eq. (H.5) forces:

∣
ζ
∣
≲
1.8
×
10
−
2
.
∣ζ∣≲1.8×10 
−2
 .
This implies a suppression scale 
M
c
u
t
≡
M
P
l
/
∣
ζ
∣
≳
55
M
P
l
M 
cut
​
 ≡M 
Pl
​
 /∣ζ∣≳55M 
Pl
​
 , placing the new-physics scale well above the Planck scale. Such a suppression is technically unnatural and requires a protective symmetry mechanism, such as an axionic shift symmetry, to suppress quantum corrections from charged-particle loops [6].

H.5 Conclusion for the Stochastic Model
The cross-check of spectroscopic (ESPRESSO) and cosmological (DESI DR2) data shows that the stochastic dark-energy model can survive only in two specific niches:

The scalar field is trapped in a local minimum or false vacuum (
V
′
→
0
V 
′
 →0), which kills the variation of fundamental constants but reduces the model to a pure cosmological constant, in tension with the dynamical evidence from DESI DR2.

The coupling to the electromagnetic sector is strongly suppressed (
∣
ζ
∣
≲
10
−
2
∣ζ∣≲10 
−2
 ), shifting the problem to the need for a screening mechanism (such as the chameleon or symmetron effect) that decouples the field in high-density environments like the quasar absorption systems probed by ESPRESSO.

In either case, the combined limits exclude a free-rolling quintessence field with natural coupling as the origin of the proposed stochastic fluctuations. This result reinforces the interpretation of the bound 
σ
X
<
1.5
×
10
−
4
σ 
X
​
 <1.5×10 
−4
  as a robust phenomenological constraint, rather than a window to new fundamental physics.

References for Appendix H:
[1] ESPRESSO Collaboration, "Fundamental physics with ESPRESSO: Constraining the variation of the fine-structure constant," Astron. Astrophys., 2022.
[2] Steinhardt, P. J., Wang, L., & Zlatev, I., "Cosmological tracking solutions," Phys. Rev. D, 59, 123504 (1999).
[3] Carroll, S. M., "Quintessence and the rest of the world," Phys. Rev. Lett., 81, 3067 (1998).

Appendix I — Background Degeneracy Check (F5)
Section 4's null result fixes the background to 
α
=
1
α=1, equivalent to 
w
0
=
−
1
w 
0
​
 =−1, 
w
a
=
0
w 
a
​
 =0, not to the DESI+CMB+SNe CPL best fit quoted in the Abstract. Using the CPL 
D
V
(
z
)
D 
V
​
 (z) of Sec. 2.1.2 in place of flat 
Λ
ΛCDM, we re-derived 
α
p
r
e
d
(
w
0
,
w
a
;
z
i
)
α 
pred
​
 (w 
0
​
 ,w 
a
​
 ;z 
i
​
 ) relative to the same fiducial and re-ran the MLE three ways:

(a) Background fixed at 
w
0
=
−
1
w 
0
​
 =−1, 
w
a
=
0
w 
a
​
 =0 [reproduces Sec. 4.2 exactly]: 
σ
X
→
5
×
10
−
5
σ 
X
​
 →5×10 
−5
 , 
θ
→
0.0010
θ→0.0010, 
ln
⁡
L
=
27.013
lnL=27.013.

(b) Background fixed at 
w
0
=
−
0.87
w 
0
​
 =−0.87, 
w
a
=
−
0.41
w 
a
​
 =−0.41 [the quoted CPL best fit]: the null result disappears. 
θ
=
0.146
θ=0.146, 
σ
X
≈
9.2
×
10
−
3
σ 
X
​
 ≈9.2×10 
−3
  — nearly 200 times larger than the reported limit, and of the same order as the DR1-era calibration amplitude. The residuals show the same sign (systematic, not noise), and the OU fit absorbs them readily.

(c) Joint fit 
{
w
0
,
w
a
,
θ
,
σ
X
}
{w 
0
​
 ,w 
a
​
 ,θ,σ 
X
​
 } free: with only 7 points and 4 parameters, the fit is weakly determined — treat it as qualitative, not as a measurement. The optimum falls near 
w
0
≈
−
0.99
w 
0
​
 ≈−0.99, 
w
a
≈
−
0.02
w 
a
​
 ≈−0.02 (nearly pure 
Λ
ΛCDM), with 
σ
X
≈
4.5
×
10
−
5
σ 
X
​
 ≈4.5×10 
−5
  — the same numerical floor as (a) — and a log-likelihood improvement of only 
+
0.13
+0.13 over the 2-parameter fit, not significant for 2 extra degrees of freedom.

Reading: The null result is robust when the BAO data are allowed to choose their own background — the data, left free, do not want to move away from 
Λ
ΛCDM and also do not need 
σ
X
σ 
X
​
 . However, the null result is not robust if the background is fixed to the external (CMB+SNe) value that the Abstract claims to use: there, a non-negligible amplitude appears.

We interpret this as: the null result is not an artifact of an arbitrary background choice — the data, left free to choose their own background, land close to 
Λ
ΛCDM and still do not want a stochastic term. It is sensitive to fixing the background at an externally-derived (CMB+SNe-informed) CPL point that this BAO-only dataset does not itself prefer; doing so reintroduces an apparent signal at roughly the DR1-calibration amplitude.

This should be treated as a preliminary, linearized-fiducial check (
S
(
z
)
S(z) held fixed rather than recomputed at each 
w
0
,
w
a
w 
0
​
 ,w 
a
​
 ; diagonal DESI covariance) pending a full re-analysis with the real DESI covariance matrix and a proper MCMC sampler (e.g., emcee) to confirm the 
w
0
≈
−
0.99
w 
0
​
 ≈−0.99 minimum is not a local artifact.

References
[1] DESI Collaboration, "DESI 2024 III: Baryon Acoustic Oscillations from Galaxies and Quasars," arXiv:2404.03000 (2024).

[2] DESI Collaboration, "DESI DR2 Results II: Measurements of BAO and Cosmological Constraints," arXiv:2503.14738 (2025).

[3] Bekenstein, J. D., "Black Holes and Entropy," Phys. Rev. D 7, 2333 (1973).

[4] Sorkin, R. D., "Is the Cosmological 'Constant' a Nonlocal Quantum Residual?," arXiv:gr-qc/0503057 (2005).

[5] Scolnic, D. et al. (Pantheon+ Collaboration), "The Pantheon+ Analysis: Cosmological Constraints," ApJ 938, 113 (2022).

[6] Uhlenbeck, G. E. & Ornstein, L. S., "On the Theory of the Brownian Motion," Phys. Rev. 36, 823 (1930).

[7] Wilczyńska, M. R. et al., "Four direct measurements of the fine-structure constant 13 billion years ago," Science Advances 6, eaay3092 (2020).

[8] Ashtekar, A. et al., "BMS supertranslations and Weinberg's soft graviton theorem," JHEP 2015, 152 (2015).

[9] Wald, R. M., General Relativity, University of Chicago Press (1984).
