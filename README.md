# riemann-zeta-1m-certification

# Rigorous Certification and Spectral Analysis of 1,000,000 Riemann Zeta Zeros

This repository documents a reproducible computational certification and numerical analysis of the first **1,000,000 nontrivial Riemann zeta zero entries**.

Each certified zero is represented in the form:

\[
\rho_n = \frac12 + i\gamma_n,\qquad n=1,\dots,1{,}000{,}000.
\]

The certification used Python with **FLINT/Arb ball arithmetic** through `python-flint`.

> **Important:** This is **not a proof of the Riemann Hypothesis**.  
> The Riemann Hypothesis is an infinite statement about all nontrivial zeros. This release certifies and analyzes a finite initial segment of 1,000,000 zero entries.

---

## Release Summary

This release includes:

- Rigorous FLINT/Arb certification
- Certified zero certificate CSV
- Input zero list
- Run logs and environment information
- SHA-256 checksums
- Hilbert-space spectral model
- GUE nearest-neighbor spacing comparison
- GUE CDF comparison
- Montgomery/GUE pair-correlation analysis
- Spectral staircase fluctuation analysis
- Prime-error reconstruction
- Zero-count sensitivity ladders
- Final report and figures

---

## Main Certification Result

Entries certified:

\[
1{,}000{,}000
\]

First certified zero ordinate:

\[
\gamma_1 =
14.1347251417346937904572519835624702707
\]

1,000,000th certified zero ordinate:

\[
\gamma_{1,000,000}
=
600269.67701244495552123391427049074397
\]

Certification checks:

- All real-part balls contain \(1/2\): **YES**
- All consecutive ordinate balls rigorously ordered/nonoverlapping: **YES**
- Returned list indexed as zeros 1 through 1,000,000: **YES**

---

## Key Numerical Results

### Hilbert-Space Spectral Model

The finite operator

\[
(H\psi)_n = \gamma_n\psi_n
\]

was tested as a finite-dimensional self-adjoint multiplication operator.

Key results:

- Zeros loaded: 1,000,000
- Mean unfolded gap: 1.000000133409
- Relative self-adjointness error: \(7.263351\times 10^{-15}\)

### GUE Spacing Comparison

The unfolded gaps were compared with the GUE Wigner-surmise density:

\[
p(s)=\frac{32}{\pi^2}s^2e^{-4s^2/\pi}.
\]

Key result:

- Approximate maximum CDF deviation from GUE: 0.013762938033

### Pair-Correlation Analysis

Compared against the Montgomery/GUE pair-correlation curve:

\[
1-\left(\frac{\sin(\pi s)}{\pi s}\right)^2.
\]

Key results:

- Pairs counted: 4,502,053
- Maximum absolute deviation: 0.042241608269
- RMS deviation: 0.015175098397

### Spectral Staircase

The zero-counting function \(N(T)\) was compared with the smooth Riemann-von Mangoldt approximation.

Key results:

- Mean fluctuation: 0.499999971028
- Standard deviation: 0.327766178752
- Final fluctuation at \(n=1,000,000\): 0.428705380647

### Prime-Error Reconstruction

The prime-error signal studied was:

\[
\psi(x)-x.
\]

Using 1,000,000 zeros, the reconstruction achieved:

Gaussian damping:

- Correlation: 0.999911340876
- RMSE: 0.625079907388
- MAE: 0.144780615346

No damping:

- Correlation: 0.999927413114
- RMSE: 0.565617113448
- MAE: 0.190355622896

---

## Download

The full release package is available from the GitHub **Releases** section.

Expected release files:

```text
riemann_1M_rigorous_release.zip
riemann_1M_rigorous_release.zip.sha256
