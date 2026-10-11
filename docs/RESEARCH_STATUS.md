# Research status and evidence boundaries

**Updated: October 2026** · **Status: incomplete and not peer-reviewed**

## Central question

We investigate the motion of zeros in Haglund's deformation
`F_t(z) = Xi_2(z) + t Phi_3(z)`, for `0 <= t <= 1`.
A successful proof would require both complete coverage and valid mathematical premises, not just isolated passing computations.

## Evidence classification

| Level | What it means in this project |
|---|---|
| Exploratory / observed | Numerical behavior or candidate trajectories, not a rigorous proof |
| Computationally checked | Interval-based or exact-rational conditions reported as satisfied for a specified finite domain |
| Conditionally certified | A computational certificate whose force still depends on its analytic prerequisites, implementation correctness, and completeness |
| Independently established theorem | Mathematical result with sufficiently reviewed assumptions and deductions; **not reached for the full k=2 conjecture** |

## Reported checkpoints from the private verifier

| Component | Internal result | Limitation |
|---|---|---|
| Central Xi2 contour | Arb winding number 7; transcript replay and alternate recomputation | Finite contour, not global |
| Upper Xi2 contour | Arb winding number 26; replay and alternate recomputation | Finite contour, not global |
| Starting roots | 26/26 disjoint radius-10^-6 Rouché isolations with two implementations | Initial roots only |
| Local first collision | Nondegenerate real double-zero/local pair conditions recorded | Local neighborhood only |
| Branch 1 | 12/12 linked logarithmic continuation cells; 94,208 exact interval boxes per evaluator, with replay | One collision branch |
| Branch 2 | 14/14 linked continuation cells; uniform-parameter Rouché checks, tube-sign checks and exact replay | One collision branch |
| Remaining 24 branches | **Not independently certified by the verifier** | Major open obligation |
| Global infinite tail | **Not independently certified by the verifier** | Major open obligation |

The passing branch-2 internal workflow also recorded rejection of five deliberately corrupted certificates. Both numerical evaluators share Arb/FLINT and related analytic methodology, so they are not completely independent mathematical formalisms.

## What is NOT established

- No complete, independently verified proof of the **k=2 zero-motion conjecture**.
- No proof of the **Riemann Hypothesis**.
- No journal acceptance or expert peer review of the complete argument.
- No public reproduction instructions for the private evidence bundles, until that material is deliberately released.
- No assertion that passing code alone proves the underlying analytic arguments.

## Release standards

Before publishing source or proof objects, we intend to check licensing, provenance, identities and private data, dependencies, documentation, and the exact meaning of each claimed result. Public evidence should include specific code revisions, independent replay instructions, expected outputs, limitations, and fail-closed criteria.

This page records the internal project's stated research scope; it is not a substitute for external replication.
