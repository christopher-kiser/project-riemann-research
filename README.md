# Project Riemann
### AI-assisted mathematical research · Computational verification · Reproducible workflows

[**ATLAS // Systems portfolio**](https://christopher-kiser.github.io/atlas-systems/) · [**Research status**](docs/RESEARCH_STATUS.md) · [**Verification workflow**](docs/VERIFICATION_WORKFLOW.md)

> [!IMPORTANT]
> **Research in progress — no complete proof is claimed.** This project investigates a proposed proof of Haglund's `k=2` zero-motion conjecture. The full conjecture has **not** been independently established or peer-reviewed. Recorded computer-assisted checks cover limited components, not the entire theorem.

## Why this project exists

A mathematical argument is only as reliable as its weakest unverified step. Project Riemann explores how AI-assisted research can be combined with explicit assumptions, interval arithmetic, independently replayable certificates, automated testing, and a transparent record of what remains uncertain.

The mathematical setting is Haglund's family

[
F_t(z) = Xi_2(z) + t,Phi_3(z),qquad 0leq tleq1.
]

The research concerns the motion of zeros in this family. It is **not a claim to have proved the Riemann Hypothesis**.

## What the project demonstrates

| Area | Research/engineering practice |
|---|---|
| Evidence quality | Distinguish numerical observations, conditional computational certificates, conjectures, and established mathematical facts |
| Numerical verification | Use Arb/FLINT complex interval enclosures rather than relying on floating-point approximations alone |
| Independent checking | Compare separately transcribed evaluators and replay generated certificates using exact-rational checks |
| Fail-closed verification | Treat missing data, inconclusive bounds, failed tests, and timeouts as **not proved** |
| Reproducibility | Track source revisions, recorded outputs, hash manifests, and Linux-based CI runs |
| AI workflow supervision | Use AI to assist with code and mathematical exploration while explicitly reviewing assumptions and documenting limitations |

## Current research checkpoint

These are **internally recorded computational results**, not third-party-validated proof of the entire conjecture.

- Finite initial-zero checks: **26 of 26** reported disjoint Rouché isolations.
- Collision branch 1: **12 of 12** continuation cells with reference/alternate interval calculations and exact-certificate replay.
- Collision branch 2: **14 of 14** continuation cells with interval checks, parameter-cover arguments, exact replays, and negative controls.
- The other **24 finite branches** and the **global infinite-tail theorem** are **not independently certified by the verification repository**.
- Rigorous review of the analytic premises, special-function bounds, implementation assumptions, and overall proof completeness remains outstanding.

Read [the detailed status and limitations](docs/RESEARCH_STATUS.md). The underlying implementation and full evidence bundles currently remain in a **private research repository**; this public portfolio is not yet a standalone reproducibility package.

## A representative technical workflow

1. **State a narrowly scoped claim** and its mathematical prerequisites.
2. **Compute exploratory candidates** without treating approximate numerical output as proof.
3. **Generate rigorous intervals** for inequalities or contour checks when possible.
4. **Replay the certificate independently** and test deliberate corruptions.
5. **Record the outcome and its scope**, including failures and unresolved dependencies.
6. **Re-evaluate the research claim** before extending it to the next branch.

See [Verification workflow](docs/VERIFICATION_WORKFLOW.md) for a more detailed explanation.

## Project role and disclosure

This is an **AI-assisted, independently directed research initiative**. My work includes shaping the research questions, organizing verification stages, evaluating reported results against stated criteria, and maintaining project documentation and review priorities. AI tools have materially assisted in drafting mathematics and software; the existence of Python, Lean 4, or CI files is **not** presented as proof of my independent professional proficiency in each technology.

This public repository intentionally shares the **methods, work structure, and evidence boundaries**, not unreleased code or a claim of a mathematical breakthrough.

## Next milestones

- Make selected certificates and minimal reproducer code publicly auditable, after a deliberate release review.
- Expand independent verification beyond the first two completed computational branch checks.
- Obtain expert review of the mathematical premises and computational implementation.
- Provide stable, permanent storage for any large proof artifacts intended for external review.
- Add a clear contribution history and technical walkthroughs that can be defended in an interview.

## Reference

J. Haglund, *Some conjectures on the zeros of approximates to the Riemann Xi-function and incomplete gamma functions* (2011), [arXiv:0910.5228](https://arxiv.org/abs/0910.5228).

---

**Portfolio context:** The cloud/infrastructure training program [Project Atlas](https://christopher-kiser.github.io/atlas-systems/) is separate from this mathematical research. Neither should be mistaken for formal employment or an externally certified theorem.
