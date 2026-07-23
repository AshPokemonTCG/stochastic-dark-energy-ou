# Honest headlines for this corpus

**Author:** Jesús Morales Souhail  
**Date:** July 2026  
**Status:** Editorial / press discipline — not a scientific claim sheet  
**Hard claims live in:** [`manuscript/PREPRINT.md`](../manuscript/PREPRINT.md) · [`amplification-gap.md`](amplification-gap.md)

---

## What is *not* ours (never put it in the subject line)

| Phrase | Why banned |
|:-------|:-----------|
| “We calculated the vacuum energy” / “energy of the vacuum” as *our* result | \(\rho_\Lambda\) is **imported** standard cosmology (Planck-class \(H_0,\Omega_\Lambda\)). This corpus does **not** derive a new \(\Lambda\). |
| “We discovered the texture of dark energy” | No positive detection; NP-B path RMS is hand-placed kinematics, not derived open-kernel proof. |
| “The model is discarded without excuses” (null lensing) | Null excludes a **tested corner**, not the open R1 kernel. |
| “Gap \(10^{56}\)” attached to DESI \(\sigma_X=1.5\times 10^{-4}\) density math | That ratio is \(\sim 10^{57}\). Use \(10^{56}\) only for the Euclid-scale target \(\sim 10^{-5}\). |

---

## What *is* ours (verified)

1. **Measured residual bound:** \(\sigma_X < 1.5\times 10^{-4}\) (95% CL, OU kernel, DESI DR2 BAO public stats) — null, honest.  
2. **Model kill:** coherent tachyonic growth excluded with correct covariance.  
3. **Amplification walls:** soft \(r\sim 64\) (Euclid target) / \(\sim 66\) (DESI ceiling); path \(\sqrt{N}=\mathcal{O}(10\)–\(100)\); machine Routes 1–3.  
4. **Two independent routes hit the same wall class** (desqueezing soft gain vs geometric path accumulation): neither closes \(G_{\mathrm{Euclid}}\sim 10^{56}\) or \(G_{\mathrm{DESI}}\sim 10^{57}\).  
5. **Discipline:** automated tests, gap label rule, anti-binary locks.

---

## Recommended headlines (pick one register)

### A — Measurement (null result, sober physics style)

> **Dark energy shows no fluctuations above 1.5 parts in \(10^{4}\), from a rigorous DESI DR2 BAO residual analysis**

True; matches how real limit papers are titled. Does not claim a new \(\Lambda\).

### B — Original contribution (recommended)

> **How far is quantum vacuum noise from being seen: a factor \(\sim 10^{56}\) to Euclid-scale residuals — measured two independent ways that hit the same wall**

Substance: not only “we saw nothing,” but **how much is missing**, with soft open (\(r\sim 64\)) and path accumulation (\(\mathcal{O}(10\)–\(100)\)) both failing to close the gap. Skeptical physicists can check the audit and not find a bait-and-switch.

**Precision variant (if the audience is technical):**

> **Sorkin seed to DESI ceiling is \(\sim 10^{57}\); to Euclid residual \(\sim 10^{-5}\) is \(\sim 10^{56}\) — both unbridgeable by audited soft amplifiers**

### C — Method (less press-friendly, most accurate meta-claim)

> **A stochastic cosmology pipeline where every claim was checked twice before publication — and what survived**

True about process; weaker as a physics headline.

---

## One-line abstract for sharing outside the chat

> We do **not** compute a new vacuum energy density. We bound fractional late-time DE residuals with DESI DR2 (\(\sigma_X<1.5\times 10^{-4}\), 95% CL), exclude coherent tachyonic growth, and show that a pure Sorkin seed sits \(\sim 10^{56}\) (Euclid target) to \(\sim 10^{57}\) (DESI ceiling) below residual scales — a gap soft amplifiers do not close.

---

## Reproduce the gap numbers

```bash
python scripts/gap_two_targets.py
```

---

*End of headline discipline note.*
