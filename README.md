# Finite-$q$ Corrections to the Carnot Capacity Identification (LC-O3)

This repository contains the source of the paper
*Finite-$q$ Corrections to the Carnot Capacity Identification
(LC-O3 of the Lorentz-Capacity Sub-Programme)*
(`Beau2026lco3`).

## Overview

The Lorentz-capacity sub-programme derives the temporal residual
$F^\tau_n = \sqrt{1 - B_n^2}$ from the bounded Born-Infeld capacity budget of
the admissibility cascade on $\mathrm{Heis}_3(\mathbb{Z}/q\mathbb{Z})$. The
technical note `Beau2026n` and the temporal residual paper `Beau2026tp`
give, under the hypotheses stated there, the quadratic identity

$$B_n^2 + (F^\tau_n)^2 = 1,$$

whose reading as time dilation requires in addition the hypothesis [H-cone] of `Beau2026tp`. The
problem, stated in Section 7.2 of `Beau2026tp`, is the status of the quadratic
law and of the parabolic Carnot capacity identification near the finite-$q$
saturation boundary $n \simeq q/2$. The present paper closes this open problem
(LC-O3).

## Main Result

LC-O3 is closed by a precise separation between two statements that were
conflated in the open problem:

1. **The quadratic Lorentz-capacity identity is exact and receives no
   correction.** For every $n$, with $B_n$ the exact finite-$q$ torus load,

   $$B_n^2 + (F^\tau_n)^2 = 1, \qquad F^\tau_n := \sqrt{1 - B_n^2}.$$

2. **The parabolic Carnot--Carath\'eodory formula is corrected outside the
   pre-saturation regime.** Setting $R := (q-1)/2$ and $n = R + m$, the exact
   torus count is

   $$B_n^{\mathrm{torus}} = \frac{q(2m+1) + 2R^2 - 2m^2}{q^2},$$

   and the deviation from the unfolded parabolic formula
   $B_n^{\mathrm{parab}} = (2n^2 + 2n + 1)/q^2$ is

   $$\Delta_q(n) := B_n^{\mathrm{parab}} - B_n^{\mathrm{torus}} = \frac{4 m^2}{q^2}.$$

In the macroscopic folded regime $n/q \to \alpha > 1/2$, the correction
converges to $\Delta_q(n) \to 4(\alpha - 1/2)^2 > 0$ and the parabolic
identification is **not** asymptotically valid. In the pre-saturation regime
($n \leq R$) and in the sublinear boundary layer ($m/q \to 0$), the correction
vanishes and the Carnot identification is exactly recovered.

Thus LC-O3 is a correction to the Carnot approximation, **not** to the capacity
law.

## Key features

- **The quadratic capacity identity is unconditional.** It holds for every $n$
  once $B_n$ is the exact torus load, by the very definition
  $F^\tau_n = \sqrt{1 - B_n^2}$ supplied by the temporal residual map of
  `Beau2026tp`.
- **The Carnot identification has a precise domain of validity.** It is exact
  for $n \leq (q-1)/2$ (no cyclic folding) and asymptotically valid in any
  sublinear neighbourhood of the folding boundary.
- **Folded-regime correction is finite and explicit.** $\Delta_q(n) = 4m^2/q^2$
  is closed-form, and the parabolic formula even exceeds $1$ (becomes
  unphysical) for sufficiently large $m$ at fixed $q$.
- **Scope.** The finite-$q$ domain concerns the spatial load only and uses no co-metric coefficient. The
  kinematic statements of the sub-programme remain conditional on a supplied co-metric and on [H-cone], and
  the gravitational capacity-metric bridge LC-O2-O1 is open (`Beau2026lco2o1`).

## Status

- Pre-saturation parabolic formula (Lemma): **proved**
- Exact torus count after cyclic folding (Lemma): **proved**
- Finite-$q$ correction theorem $\Delta_q(n) = 4m^2/q^2$: **proved**
- Domain of validity of the Carnot identification (three regimes): **proved**
- Asymptotic Carnot recovery (Corollary): **proved**
- Closure of LC-O3: **proved**

## Position in the sub-programme

```
LorCap -> TempProj -> LC-O2 -> LC-O2-O1
                            \-> LC-O1
                            \-> LC-O3
```

## Dependencies

| Paper | Role |
|-------|------|
| N (`Beau2026n`) | Weil factorisation $\Sigma^{\mathrm{tot}}_n = 1 - B_n$ |
| TempProj (`Beau2026tp`) | Temporal residual map $F^\tau_n = \sqrt{1 - B_n^2}$; statement of LC-O3 (Section 7.2) |

## Repository Contents

```
lc-o3/
|-- out/              # Compiled PDF
|-- tex/
|   |-- lc-o3.tex
|   |-- cosmochrony-bibliography.bib
|-- compile.sh
|-- zenodo.json
|-- README.md
```

## Compilation

```bash
bash compile.sh
```

## Citation

> J. Beau, *Finite-$q$ Corrections to the Carnot Capacity Identification*,
> Preprint, 2026.

## Acknowledgements

Portions of the editorial refinement benefited from iterative interactions with
large language models used as analytical assistants.
All claims, interpretations, and final formulations remain the sole
responsibility of the author.
