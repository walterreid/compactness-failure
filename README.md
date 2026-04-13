# Compactness Failure in Galois Deformation Problems

## What this is

This repository contains a structural decomposition of the proof of Fermat's Last Theorem into its automorphic and non-automorphic components, culminating in a precise open question.

The work was developed collaboratively with Claude (Anthropic) -- I directed the mathematical inquiry and Claude executed the formal arguments. I want to be clear about what's mine, what's the framework, and what remains open.

## The story

I started with a simple question: *what exactly in the proof of Fermat's Last Theorem requires the theory of modular forms, and what doesn't?*

The answer turned out to be surprisingly precise. The proof factors into components, and you can trace exactly which ones need automorphic input. Most of the heavy lifting -- the Frey construction, the Serre recipe, the vacancy computation, the local deformation theory, even the numerical coincidence underlying Taylor-Wiles patching -- turns out to be non-automorphic. It's all computable from local Galois cohomology.

What's left is a single assertion: that the global deformation ring $R$ maps isomorphically to a Hecke algebra $\mathbb{T}$ that happens to be zero at the vacancy. That's the wall.

I spent a long time trying to get past the wall. Every approach failed -- but the failures were informative. The Euler characteristic blocks direct Selmer vanishing. The cyclotomic twist flips the archimedean sign but can't be connected back without automorphic input. Ogg's theorem and Faltings give a non-automorphic route to the vacancy itself, but Entry (the representation is modular) remains the floor, not just a wall. These negative results constrain the open question as tightly as the positive results do.

## What's actually proved

**The main theorem (Paper II, Theorem 7.1)** gives four checkable hypotheses (H1-H4) under which a Galois deformation problem is in the "compactness-failure regime." Under those hypotheses:

1. **Finite satisfiability** is proved non-automorphically -- for every finite set of primes, a single elliptic curve simultaneously satisfies all local conditions (via CRT on Weierstrass coefficients).

2. **The Selmer Euler characteristic** is computable from local Galois cohomology at the essential primes alone -- no modular forms appear.

3. **All removable primes are transparent** -- they contribute zero to the Selmer balance (Euler Characteristic Transparency theorem).

4. **The detection boundary is identified** -- everything above is non-automorphic; the single remaining assertion (global unsatisfiability, i.e., $R_{\mathcal{D}} = 0$) requires automorphic comparison via $R = \mathbb{T}$.

**What is NOT proved:** $R_{\mathcal{D}} = 0$ by non-automorphic means. That remains the open question. The Euler characteristic $\chi = 1$ actually forces $\dim H^1_{\mathcal{L}} \geq 1$, meaning $R$ is *nonzero* as an abstract deformation ring. The assertion "$R = 0$" only holds after the modularity theorem identifies $R$ with $\mathbb{T} = 0$. So the open question isn't purely "can we prove $R = 0$ by Galois cohomology?" -- it's the subtler question of whether the *relevant quotient* of $R$ can be characterized and shown to vanish without automorphic input.

## What's mine vs. what others could build on

**My contribution:** The question, the direction, and the persistence. I asked what in FLT is automorphic, pushed until it became a precise decomposition, named the compactness-failure phenomenon, and steered through every failed approach until the failures themselves became results. The architectural choices -- how to factor the proof, what to call the components, where to draw the detection boundary -- are mine.

**The framework (developed with Claude):** The formal proofs, the AMS-formatted papers, the checkable criteria (H1-H4), the Euler Characteristic Transparency theorem, the Vacancy Equivalence, the 24-vacancy classification, and the Detection Boundary theorem. These are the pieces that make the open question precise and that others could use or extend.

**What's open:** Whether $R_{\mathcal{D}} = 0$ can be certified without automorphic comparison. The working notes document why every approach I tried leads back to $R = \mathbb{T}$, and each failure narrows the space of possible solutions. The Leveling Sophistication analysis examines the question from multiple perspectives and identifies the most promising directions (axiomatic characterization of $\mathbb{T}$; deformation-theoretic Euler systems).

---

## Reading Guide

### The Papers

**[Paper I: On the Irreducible Automorphic Content of Fermat's Last Theorem](papers/automorphic_content_of_FLT.md)** ([PDF](papers/automorphic_content_of_FLT.pdf) | [LaTeX](papers/automorphic_content_of_FLT.tex))
The complete structural decomposition in nine pages. Seven theorems, AMS format. Start here.

**[Paper II: Compactness Failure in Galois Deformation Problems](papers/compactness_failure_in_galois_deformations.md)** ([PDF](papers/compactness_failure_in_galois_deformations.pdf) | [LaTeX](papers/compactness_failure_in_galois_deformations.tex))
The general theory. Introduces compactness failure as a reusable concept, proves the detection boundary in full generality, classifies the weight-2 landscape (15 positions), and gives the checkable criteria (H1-H4).

### The Standalone Theorems

| File | What it proves |
|------|---------------|
| [The One Theorem](theorems/the_one_theorem.md) | The Separation theorem via simultaneous local indistinguishability (CRT). The provable core -- where the program started. |
| [Simultaneous Indistinguishability](theorems/simultaneous_indistinguishability.md) | The quantifier upgrade from $\forall\exists$ to $\forall\exists\forall$ that blocks correlational criteria and reveals the compactness-failure structure. |
| [Vacancy Equivalence](theorems/vacancy_equivalence_theorem.md) | At a vacancy, the descent residual is equivalent to $R_{N,\bar{\rho}} = 0$ -- a Galois-theoretic *statement* whose only known *proof* is automorphic. |
| [Numerical Coincidence](theorems/numerical_coincidence.md) | $\chi = 1 + \delta_2 + \delta_n = 1$, derived entirely from local Galois cohomology. The numerical foundation of Taylor-Wiles patching, without automorphic input. |
| [The Question](theorems/the_question.md) | The precisely formulated open problem, with full context, candidate approaches, and the dichotomy (positive: Langlands is one of several witnesses; negative: Langlands is the *necessary* language). |

### The Analysis

**[Leveling Sophistication](analysis/leveling_sophistication.md)** -- The open question examined from four expertise perspectives and five probability-conditioned scenarios. The key insight: the Euler system approach self-destructs against the Euler characteristic (Gradient #3), and the proof-theoretic independence scenario (Gradient #5) is now a well-posed question.

### The Working Notes

The wrong turns are load-bearing. Each one closes a door and constrains the open question.

| File | What it documents | Why it matters |
|------|-------------------|----------------|
| [C3b-ii Working Notes](working-notes/c3bii_working_notes.md) | Every attempt to prove $R = 0$ non-automorphically. | Shows that every path leads back to $R = \mathbb{T}$. |
| [Delta Computation](working-notes/delta_computation_working_notes.md) | Computing $\delta_2 = 0$ and $\delta_n = 0$, including a critical error caught in real time. | The error ($R = 0$ vs. $R \neq 0$) reveals the deepest tension in the program. |
| [Euler Survey](working-notes/euler_survey_all_vacancies.md) | All 24 vacancies have $\chi \geq 1$ under standard conditions. | Blocks the reverse-Ramakrishna strategy everywhere. |
| [Twist Strategy](working-notes/twist_strategy_working_notes.md) | $\chi(V(1)) = -1$ -- the cyclotomic twist flips the archimedean sign. | Proves $\chi = +1$ is structural, not accidental. Connecting back requires automorphic input. |
| [Under the Wall](working-notes/under_the_wall_working_notes.md) | Final attempt via Ogg's theorem and Faltings. | Entry isn't a wall but the floor. There is no "under." |

## License

See [LICENSE](LICENSE).

## Acknowledgments

This work was developed in collaboration with Claude (Anthropic). The mathematical content was produced through an iterative process: I posed questions, directed the investigation, and identified when approaches failed or succeeded; Claude executed the formal arguments, wrote the proofs, and produced the papers. The working notes preserve this process.
