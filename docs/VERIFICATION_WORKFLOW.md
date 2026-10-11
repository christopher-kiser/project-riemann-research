# Verification workflow: from conjecture to auditable evidence

This document describes the **methodology** used in the private Project Riemann verifier. It is a portfolio case study, **not** a claim that the whole theorem has been solved or that the private implementation has been published.

## 1. Separate hypothesis from computation

Start by expressing the narrowly scoped mathematical statement, domain, and logical dependencies. Approximate root locations and numerical plots are useful for proposing a computational cover, but they do not themselves certify a theorem.

## 2. Construct rigorous local checks

Where applicable, the verifier uses Arb/FLINT ball arithmetic, Rouché inequalities, zero-free enclosures, contour arguments, and interval bounds. These replace numerical confidence with explicit strict inequalities **for the specified finite regions**, conditional on the correctness of the underlying analytic definitions and implementation.

## 3. Preserve a machine-readable record

Proof candidates produce certificates recording intervals, covers, handoffs, and strict predicate outcomes. Separate replay logic checks exact-rational bounds and rejects any required condition that is absent or false.

## 4. Use complementary verification paths

The project records a primary and an alternate transcription of certain special-function calculations. The two paths improve error detection, but share libraries and mathematical foundations; agreement alone does not imply complete formal independence.

Selected algebraic identities have also been represented in Lean 4. Those checks are **not** a formalization of the full k=2 claim.

## 5. Make failure meaningful

A trustworthy verifier must fail closed. The project treats a timeout, a missing certificate, a non-strict interval sign, or an incomplete domain as **inconclusive**, not passing. Negative-control tests intentionally corrupt proof data to verify rejection behavior.

## 6. Require a complete chain of reasoning

Correct local computations do not establish a global theorem. The finite branches, the infinite tail, the special-function majorants, and all handoffs must fit together under fully validated premises. The public [research status](RESEARCH_STATUS.md) says exactly which obligations remain open.

## 7. Publish responsibly

The current public repository documents the process without exposing the private implementation. To become independently reproducible, a future public release needs versioned source, installation instructions, tests, representative proof certificates, output hashes, and mathematical review of what each certificate actually entails.

## Engineering lessons and transferable skills

- Write explicit acceptance criteria before interpreting a result.
- Preserve provenance and test artifacts.
- Use automation for regression tests but do not equate automation with proof.
- Design an independent validation step for consequential claims.
- Distinguish **developing a workflow with AI assistance** from independently mastering every underlying programming language and mathematical method.
