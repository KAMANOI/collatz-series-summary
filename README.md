# A Research Program on Collatz Synchronization Dynamics

**Final Summary — Papers A–P**

Comprehensive summary of the research program establishing four components: exact mixing theory (Papers A–E), local cascade geometry (Papers F–M), Hensel-chain reformulation (Papers N–O), and a negative mixing result (Paper P). Identifies the central open problem.

> This repository does not claim a proof of the Collatz conjecture.

---

## Erratum (2026-11-12)

- **Theorem SR and the "one-shot" part of Theorem Monotonicity are withdrawn.** Consecutive jumps of the same height occur (1643 -> 2465 -> 1849 -> 1387 -> 2081, a_t = 1, 5, 3, 1, 5), and a height K >= 4 can be reached more than once in one orbit (139: height 4 at 139 -> 209 and again at 11 -> 17). Height records are increasing only by definition.
- Source of the error: the cascade law q -> 3q was applied to the jump step. After a height-K jump the odd core is (3q + 1) / 2^K (see the erratum of Paper H).
- The contrast drawn in Section 3 between "one-shot" record renewals in actual orbits and revisited levels in the Haar model is therefore not established.
- Theorems UPI, MC, PC and PG rest on the same transport step; their proofs are not public and they should be treated as unverified.
- Unaffected: the mixing results of Papers A-E, Theorems VD and OC (inside a cascade), JE, JE2, the Hensel nesting, and part (a) of Theorem HMC.

The PDF in `paper/` is the original, uncorrected version.

---

## Overview

The summary organises the complete series into two layers and four components, and states the single open problem that remains after all proved results are accounted for.

**Component 1 (Papers A–E)**: The 2-adic Haar Markov kernel P_K mixes to Haar uniform in exactly K−1 steps (Theorem TMix). Exact covariance decay and finite total mutual information (2 log 2) established.

**Component 2 (Papers F–M)**: The valuation process obeys exact algebraic laws. Height records are strictly increasing and each height K ≥ 4 is achieved at most once (Theorem Monotonicity). Cascade transport is exact.

**Component 3 (Papers N–O)**: Gate-2 jump formula established. If a Collatz orbit has infinitely many gate-1 records at heights Kᵢ → ∞, then q_{τᵢ} → −3⁻¹ in ℤ₂ (Theorem HMC).

**Component 4 (Paper P — Negative result)**: In the infinite Haar renewal model, every Hensel level K is hit infinitely often almost surely. Mixing increases accessibility to targets but is insufficient to prove Collatz — the missing ingredient is the deterministic starting-position constraint.

---

## Main Results

### Proved (Rigorous)

| Result | Papers | Status |
|--------|--------|--------|
| Theorem TMix: P_K mixes in exactly K−1 steps | A–E | ✓ proved |
| Exact covariance Cov_π(k₀, kₙ) = 2·(1/2)^N | A | ✓ proved |
| Total mutual information Σ I_π = 2 log 2 | A | ✓ proved |
| Theorem Monotonicity: height records strictly increasing | F–M | true by definition only; "each height once" is false, see Erratum |
| Theorem HMC: 2-adic convergence to −3⁻¹ | N–O | ✓ proved |
| Paper P (Negative): mixing alone insufficient | P | ✓ proved |

---

## Structure

```
§1   Four components of the research program
§2   Complete theorem list
§3   The two-layer structure
§4   The open problem
§5   Honest assessment
```

---

## Open Problems

- **Open Problem 1** (One-shot Hensel traversal): Does any Collatz orbit traverse the Hensel chain q_{τ₁} ≡ r_{K₁}, q_{τ₂} ≡ r_{K₂}, … (mod 2^{Kᵢ}), K₁ < K₂ < ··· → ∞ infinitely often, each Kᵢ used exactly once, while q_{τᵢ} → +∞ in ℝ?

---

## Repository Structure

```
collatz-series-summary/
├── README.md
├── paper/
│   └── series_summary_papers_a_to_p.pdf
└── LICENSE
```

---

## Related Work

This paper is part of a series on Collatz dynamics:

- [collatz-act1](https://github.com/KAMANOI/collatz-act1) — Foundational paper: prime survival dynamics and Chen-type theorem (v11)
- [collatz-renewal-structure](https://github.com/KAMANOI/collatz-renewal-structure) — Paper A: exact operator structure and finite information memory
- [collatz-finite-mixing-geometry](https://github.com/KAMANOI/collatz-finite-mixing-geometry) — Paper B: finite-level mixing geometry
- [collatz-spectral-amplification](https://github.com/KAMANOI/collatz-spectral-amplification) — Paper C: spectral amplification
- [collatz-scale-coherence](https://github.com/KAMANOI/collatz-scale-coherence) — Paper D: scale-coherence rigidity
- [collatz-valuation-renewal](https://github.com/KAMANOI/collatz-valuation-renewal) — Valuation renewal, finite residue connectivity, and orbitwise gap
- [collatz-residual-core](https://github.com/KAMANOI/collatz-residual-core) — The residual core: structural decomposition
- [collatz-congruence-synchronization](https://github.com/KAMANOI/collatz-congruence-synchronization) — Paper H: nested congruence constraints on synchronization
- [collatz-record-renewal](https://github.com/KAMANOI/collatz-record-renewal) — Paper N: record renewal compatibility
- [collatz-hensel-escape](https://github.com/KAMANOI/collatz-hensel-escape) — Paper O: Hensel memory and 2-adic escape target
- [collatz-hensel-scarcity](https://github.com/KAMANOI/collatz-hensel-scarcity) — Paper T: Hensel conditional scarcity and telescoping contradiction
- [collatz-prefix-counting](https://github.com/KAMANOI/collatz-prefix-counting) — Paper V: direct prefix counting and synchronization collapse
- [collatz-first-passage](https://github.com/KAMANOI/collatz-first-passage) — Paper W: first-passage obstruction (closes series A–V)
- [collatz-series-summary](https://github.com/KAMANOI/collatz-series-summary) — Series summary: research program on Collatz synchronization dynamics
- [collatz-prime-survival](https://github.com/KAMANOI/collatz-prime-survival) — Paper X v20: prime survival in affine Collatz dynamics

---

## Author

Hiroki Kamanoi
hirokikamanoi@gmail.com
2026

---
Related research and services by HDR (Human Driven Reality): https://hdr-ai.com/#research
