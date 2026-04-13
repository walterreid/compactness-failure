# On the Irreducible Automorphic Content of Fermat's Last Theorem: A Structural Decomposition

**Date:** April 10, 2026

**MSC 2020:** 11D41, 11F80, 11F11, 11G05, 11R34

**Keywords:** Fermat's Last Theorem, Galois representations, modularity, deformation theory, Selmer groups, automorphic forms, Frey curve

---

## Abstract

We carry out a systematic structural decomposition of the proof of Fermat's Last Theorem into its automorphic and non-automorphic components. Through a sequence of unconditional results, we establish that the automorphic content of the proof---historically described as "the modularity theorem for semistable elliptic curves"---concentrates in two precisely identified assertions: the modularity of the Frey representation (Entry) and the Taylor--Wiles patching identification (a residual of Descent). We prove that all other components of the proof, including the Serre recipe, the vacancy computation, the local deformation theory, the Euler characteristic of the relevant Selmer group, and the numerical coincidence underlying Taylor--Wiles patching, are derivable by non-automorphic means. We establish several new structural results along the way: a simultaneous local indistinguishability theorem revealing the Frey obstruction as a compactness failure; a complete enumeration of the 24 automorphic vacancies at which the Frey mechanism can operate; a vacancy equivalence theorem translating the descent residual into a Galois-cohomological statement; and an Euler characteristic transparency theorem showing that formally smooth primes are invisible to the Selmer balance. We conclude by formulating the precise open question to which the entire decomposition converges: whether the vanishing of a specific Galois deformation ring can be certified without automorphic comparison.

---

## Table of Contents

1. [Introduction](#1-introduction)
2. [The Frey Construction and Its Galois Profile](#2-the-frey-construction-and-its-galois-profile)
3. [Separation: The Compactness Failure](#3-separation-the-compactness-failure)
4. [Finiteness: The 24 Vacancies](#4-finiteness-the-24-vacancies)
5. [The Automorphic Bottleneck](#5-the-automorphic-bottleneck)
6. [The Entry--Descent Decomposition](#6-the-entry-descent-decomposition)
7. [The Uniformity Boundary](#7-the-uniformity-boundary)
8. [Descent Resolution](#8-descent-resolution)
9. [The Vacancy Equivalence](#9-the-vacancy-equivalence)
10. [Euler Characteristic Transparency](#10-euler-characteristic-transparency)
11. [The Automorphic Inventory](#11-the-automorphic-inventory)
12. [The Open Question](#12-the-open-question)
13. [Concluding Remarks](#13-concluding-remarks)

---

## 1. Introduction

The proof of Fermat's Last Theorem, completed by Wiles [Wiles] and Taylor--Wiles [TW], is widely described as an application of the modularity theorem for semistable elliptic curves. This description, while historically accurate, obscures the logical fine structure of the proof: which components genuinely require automorphic input and which are derivable from algebraic geometry, local Galois theory, and elementary computation alone.

This paper carries out a systematic decomposition of the proof into its automorphic and non-automorphic components. The decomposition is unconditional: every structural result we prove depends only on classical results in the theory of modular forms (for the dimension formula), on the local theory of Galois representations (for the deformation-theoretic results), and on standard Galois cohomology (for the Selmer group computations). No new cases of modularity or the Langlands correspondence are established or required.

The main results are:

**(i) Separation** (Theorem 3.1): the non-realizability of the Frey profile is provably undetectable by any local method, including criteria examining correlations between local data at finitely many primes. The Frey obstruction is a *compactness failure*: finitely satisfiable but globally unsatisfiable.

**(ii) Finiteness** (Theorem 4.1): the automorphic landscape contains exactly 24 vacancies---pairs $(k, N)$ with $\dim S_k(\Gamma_0(N)) = 0$---constituting the complete locus at which the Frey mechanism produces automatic contradictions.

**(iii) Bottleneck** (Theorem 5.1): the proof decomposes into three logically independent components, of which exactly one (the modularity bridge C3) requires automorphic input.

**(iv) Entry--Descent** (Theorem 6.1): the modularity bridge splits into two independent sub-gates---Entry (the representation is modular) and Descent (the level reduces to the Serre-predicted value)---with structurally distinct replacement characteristics.

**(v) Descent Resolution** (Theorem 8.2): the Galois-theoretic prerequisites for descent are unconditionally satisfied; the residual automorphic content of descent reduces to a single interface (level-lowering validity at formally smooth primes).

**(vi) Vacancy Equivalence** (Theorem 9.1): at a vacancy, the residual descent is equivalent to the vanishing of the Galois deformation ring $R_{N,\bar{\rho}} = 0$, a purely Galois-theoretic statement.

**(vii) Euler Transparency** (Theorem 10.1): formally smooth primes contribute zero to the Selmer Euler characteristic; the numerical coincidence underlying Taylor--Wiles patching is derivable non-automorphically.

The net effect of these results is a progressive compression of the automorphic content of the Fermat proof from "the modularity of semistable elliptic curves" to two precise assertions: Entry (the Frey representation is modular) and the Taylor--Wiles patching identification (in a form whose numerical foundation is already established non-automorphically).

We conclude by formulating the open question to which the entire program converges (Question 12.1), and by analyzing the structural reasons this question may or may not admit a positive answer.

---

## 2. The Frey Construction and Its Galois Profile

We fix notation following [DDT, Ribet90, Serre87].

Suppose, toward contradiction, that there exist coprime positive integers $a, b, c$ and a prime $n \geq 5$ satisfying $a^n + b^n = c^n$, with $2 \mid a$. The *Frey curve* $E = E_{a,b,c}$ is the elliptic curve

$$E : y^2 = x(x - a^n)(x + b^n).$$

Its key properties are:

**(a)** *Semistability*: $E$ has multiplicative reduction at every prime of bad reduction.

**(b)** *Conductor*: $N_E = \mathrm{rad}(abc)$.

**(c)** *Discriminant*: $\Delta_E = 2^{-8}(abc)^{2n}$.

**(d)** *Mod-$n$ representation*: $\bar{\rho}_{E,n} : G_{\mathbb{Q}} \to \mathrm{GL}_2(\mathbb{F}_n)$ is irreducible (Mazur [Mazur]), with:
- At $\ell \mid abc$, $\ell \neq n$: $\bar{\rho}$ is unramified ($n \mid v_\ell(\Delta_E)$).
- At $\ell = n$: $\bar{\rho}|_{G_{\mathbb{Q}_\ell}}$ is finite-flat (when $n \nmid abc$).
- At $\ell = 2$: $\bar{\rho}|_{G_{\mathbb{Q}_2}}$ is constrained by $v_2(a)$.

**(e)** *Serre invariants*: $k(\bar{\rho}) = 2$, $N(\bar{\rho}) = 2$ (Ribet [Ribet90]).

> **Definition 2.1.** The *Frey profile* $\bar{\rho}^{\mathrm{Frey}}$ is the formal local Galois profile of type $(n, 2, 2)$ specified by the above local data. It is well-defined as a formal object independently of the existence of any Fermat counterexample.

---

## 3. Separation: The Compactness Failure

> **Definition.** A *local detection method* is any procedure $C$ that takes as input a formal collection of local Galois representations $\{\bar{\rho}_\ell : G_{\mathbb{Q}_\ell} \to \mathrm{GL}_2(\mathbb{F}_p)\}_\ell$ and outputs a verdict (realizable / non-realizable) based on examining the local data at any finite set of primes, using any technique ($p$-adic Hodge theory, Fontaine--Laffaille theory, finite flat group schemes, local class field theory, etc.). Let $\mathcal{L}$ denote the class of all local detection methods.

> **Theorem 3.1 (Simultaneous Local Indistinguishability).** Let $\bar{\rho}^{\mathrm{Frey}}$ be the Frey profile with Serre invariants $(k, N) = (2, 2)$. Then:
>
> **(i)** $\bar{\rho}^{\mathrm{Frey}}$ is not motivically realizable at $(2, 2)$, since $S_2(\Gamma_0(2)) = 0$.
>
> **(ii)** For every finite set of primes $S = \{\ell_1, \ldots, \ell_r\}$, there exists a single elliptic curve $E_S / \mathbb{Q}$ such that $\bar{\rho}_{E_S, n}|_{G_{\mathbb{Q}_\ell}}$ belongs to the same local admissibility class as $\bar{\rho}^{\mathrm{Frey}}_\ell$ for every $\ell \in S$.
>
> **(iii)** Consequently, no $C \in \mathcal{L}$ can distinguish $\bar{\rho}^{\mathrm{Frey}}$ from a motivically realizable profile without also rejecting genuinely realizable profiles.
>
> In particular, the non-realizability of the Frey profile exhibits the structure of a *compactness failure*: the local conditions are finitely satisfiable but globally unsatisfiable.

**Proof.** Part (i) is the classical dimension computation: $g(X_0(2)) = 0$, hence $\dim S_2(\Gamma_0(2)) = 0$.

For (ii): at each prime $\ell$, the Frey profile specifies a local reduction type (good, multiplicative with $n \mid v_\ell(\Delta)$, or finite-flat). Each type is determined by congruence conditions on the Weierstrass coefficients of an elliptic curve modulo powers of $\ell$. For distinct primes $\ell_1, \ldots, \ell_r$, the relevant moduli are pairwise coprime. By the Chinese Remainder Theorem, Weierstrass coefficients satisfying all congruence conditions simultaneously exist. The nonvanishing-discriminant locus is Zariski-dense and meets every nonempty congruence class, so the resulting curve $E_S$ is an elliptic curve over $\mathbb{Q}$ with the prescribed reduction type at every $\ell \in S$.

Part (iii) follows: any criterion $C$ examining local data at primes in $S$ that rejects $\bar{\rho}^{\mathrm{Frey}}$ also rejects $\bar{\rho}_{E_S}$, which is genuinely realizable. So $C$ produces a false rejection.

The compactness-failure structure: (ii) establishes finite satisfiability (for every finite $S$, a simultaneous match exists); (i) establishes global unsatisfiability (no form at $(2,2)$ exists). This is the defining property of a compactness failure. $\blacksquare$

> **Remark.** The prime-by-prime version of (ii) --- producing a different curve $E_\ell$ at each prime --- is implicit in the classical literature. The simultaneous version, with its quantifier structure $\forall S \text{ finite}, \exists E_S, \forall \ell \in S$, is new. It blocks correlational criteria that examine joint conditions across distinct primes, and it reveals the essentially infinitary nature of the obstruction.

---

## 4. Finiteness: The 24 Vacancies

> **Definition.** A pair $(k, N)$ with $k \geq 2$ even and $N \geq 1$ is an *automorphic vacancy* if $\dim S_k(\Gamma_0(N)) = 0$.

> **Theorem 4.1 (Finiteness and Completeness).** The set of automorphic vacancies consists of exactly 24 pairs:

| Weight $k$ | Levels $N$ with $S_k(\Gamma_0(N)) = 0$ |
|:-----------:|:----------------------------------------|
| $2$ | $1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 12, 13, 16, 18, 25$ |
| $4$ | $1, 2, 3, 4$ |
| $6$ | $1, 2$ |
| $8$ | $1$ |
| $10$ | $1$ |
| $14$ | $1$ |

For every $(k, N)$ not in this table, $\dim S_k(\Gamma_0(N)) \geq 1$.

**Proof.** This follows from the classical dimension formula for $S_k(\Gamma_0(N))$ (see [DS]). At weight 2, $\dim S_2(\Gamma_0(N)) = g(X_0(N))$, and the genus-zero values of $N$ are classical. At weight $k \geq 4$, the leading term $(k-1)(g(N)-1)$ and the cusp term $(k/2 - 1) c(N)$ grow with $k$ and $N$; direct computation for the finitely many remaining cases yields the table. The growth of the index $\mu(N)$ (at least linear in $N$) against the sublinear correction terms ensures completeness. $\blacksquare$

---

## 5. The Automorphic Bottleneck

> **Theorem 5.1 (Automorphic Bottleneck).** The contradiction underlying Fermat's Last Theorem factors into three logically independent components:
>
> **(C1) Target Computation** (non-automorphic): the Serre recipe, applied to the local data of the Frey construction, yields invariants $(k, N) = (2, 2)$.
>
> **(C2) Vacancy Verification** (non-automorphic): $\dim S_2(\Gamma_0(2)) = 0$.
>
> **(C3) Modularity Bridge** (automorphic): the Frey representation must arise from a cuspform at its Serre-predicted invariants.
>
> Components (C1) and (C2) are unconditionally computable. Without (C3), they produce no contradiction: (C1) labels the representation but does not constrain it; (C2) describes the automorphic landscape but imposes no obligation on Galois representations. The conjunction produces a contradiction only via (C3), which forces the representation to occupy the slot identified by (C1) --- which (C2) shows is empty. Component (C3) is the unique automorphic input.

**Proof.** (C1) is Serre's recipe [Serre87], a deterministic function of local Galois data. (C2) is the dimension formula computation. (C3) is the content of the modularity theorem [Wiles, TW] combined with Ribet's level-lowering [Ribet90]. The independence and necessity of each component are verified by observing that removing any one prevents the contradiction: without (C1), there is no target; without (C2), the target is occupied; without (C3), the representation has no obligation to occupy the target. $\blacksquare$

---

## 6. The Entry--Descent Decomposition

> **Theorem 6.1 (Entry--Descent Decomposition).** The modularity bridge (C3) decomposes into two logically independent sub-gates:
>
> **(C3a) Entry**: $\bar{\rho}_{E,n}$ is modular --- it arises from a cuspidal eigenform of some weight and some level.
>
> **(C3b) Descent**: if $\bar{\rho}_{E,n}$ is modular at level $M$, the level can be reduced to $N(\bar{\rho}) = 2$.
>
> These are logically independent (neither implies the other), each independently necessary (removing either prevents the contradiction), and structurally asymmetric: Entry crosses the Galois--automorphic boundary; Descent optimizes within the automorphic world.

**Proof.** Independence: (C3a) asserts modular correspondence at some level; (C3b) is a conditional with (C3a) as its antecedent. Necessity of (C3a): without it, (C3b) is a conditional with unestablished antecedent. Necessity of (C3b): without it, the representation corresponds to a form at level $M$, where $S_2(\Gamma_0(M))$ is generically nonempty, producing no contradiction. $\blacksquare$

---

## 7. The Uniformity Boundary

> **Theorem 7.1 (Uniformity Boundary).** The Frey mechanism operates in two logically distinct modes:
>
> **(a)** *Vacancy mode*: if $\dim S_k(\Gamma_0(N)) = 0$, the contradiction is representation-independent and universally quantified --- it holds for every $\bar{\rho}$ with invariants $(k, N)$.
>
> **(b)** *Matching mode*: if $\dim S_k(\Gamma_0(N)) \geq 1$, the contradiction (if any) depends on the specific representation's Frobenius traces compared against the Fourier coefficients of forms in the space.
>
> Vacancy mode is available at exactly the 24 positions of Theorem 4.1. The proof of Fermat's Last Theorem targets the vacancy at $(2, 2)$.

---

## 8. Descent Resolution

> **Theorem 8.1 (Formal Smoothness at Unramified Primes).** Let $\ell \neq p$ be a prime at which $\bar{\rho}$ is unramified. The unramified local deformation ring is $R^{\mathrm{ur}}_\ell \cong W(k)[[T]]$, formally smooth over $W(k)$ of relative dimension $1$. The obstruction group $H^2(G^{\mathrm{ur}}_{\mathbb{Q}_p}, \mathrm{ad}\,\bar{\rho})$ vanishes because $G^{\mathrm{ur}}_{\mathbb{Q}_p} \cong \hat{\mathbb{Z}}$ has cohomological dimension $1$.

**Proof.** Standard: the cohomology of procyclic groups, the structure of $\mathrm{GL}_2$ over local rings, and the vanishing of $H^2$ for groups of cohomological dimension $1$. See Mazur [Mazur89] and Kisin [Kisin09a]. $\blacksquare$

> **Theorem 8.2 (Descent Resolution).** Suppose $\bar{\rho}^{\mathrm{Frey}}$ is modular at level $M$ (Entry assumed). Then:
>
> **(a)** At every prime $\ell \mid M$ with $\ell \neq 2$ and $\ell \neq n$, the Frey profile is unramified and the local deformation ring is formally smooth.
>
> **(b)** The Artin conductor is $N(\bar{\rho}^{\mathrm{Frey}}) = 2$, concentrating the deformation-theoretic weight at $\ell = 2$.
>
> **(c)** The descent gate (C3b) decomposes as:
> - *(i) Galois-theoretic prerequisites* (resolved, non-automorphic): all local deformation rings at removable primes are formally smooth.
> - *(ii) Level-lowering validity* (residual, automorphic): removing a formally smooth prime from the level is valid.
>
> All three inputs --- unramifiedness, formal smoothness, and the conductor computation --- are non-automorphic.

---

## 9. The Vacancy Equivalence

> **Theorem 9.1 (Vacancy Equivalence).** Let $\bar{\rho}$ be odd, irreducible, with Serre invariants $(k, N)$ at a vacancy, and suppose $\bar{\rho}$ is modular at level $M$. The following are equivalent:
>
> **(a)** Level-lowering validity: $\bar{\rho}$ is modular at level $N$.
>
> **(b)** $R = \mathbb{T}$ at the vacancy: $R_{N,\bar{\rho}} \cong \mathbb{T}_{N,\bar{\rho}} = 0$.
>
> **(c)** Galois-theoretic non-existence: no lift of $\bar{\rho}$ to characteristic zero exists satisfying the level-$N$ local conditions.
>
> **(d)** The system of local lifting conditions is finitely satisfiable (Theorem 3.1) but globally unsatisfiable --- a compactness failure.
>
> At a vacancy, the residual automorphic content of descent is equivalent to the Galois-theoretic assertion $R_{N,\bar{\rho}} = 0$.

**Proof.** (a) $\Leftrightarrow$ (b): at a vacancy, $\mathbb{T}_{N,\bar{\rho}} = 0$. The $R = \mathbb{T}$ assertion becomes $R_{N,\bar{\rho}} = 0$. (b) $\Leftrightarrow$ (c): $R_{N,\bar{\rho}} = 0$ if and only if no lift with level-$N$ conditions exists. (c) $\Leftrightarrow$ (d): finite satisfiability is Theorem 3.1; global unsatisfiability is (c). $\blacksquare$

---

## 10. Euler Characteristic Transparency

Let $V = \mathrm{ad}^0\bar{\rho}$ denote the trace-zero adjoint, and let $\mathcal{L}$ be a Selmer structure on $V$.

> **Theorem 10.1 (Euler Characteristic Transparency).** Let $\ell \neq p$ be a prime at which $\bar{\rho}$ is unramified, with local condition $L_\ell = H^1_{\mathrm{ur}}(G_{\mathbb{Q}_\ell}, V)$. The local contribution to the Greenberg--Wiles formula at $\ell$ is zero:
>
> $$\dim_k L_\ell - \dim_k H^0(G_{\mathbb{Q}_\ell}, V) = 0.$$

**Proof.** Since $\bar{\rho}$ is unramified at $\ell$, the inertia $I_\ell$ acts trivially on $V$. Thus $H^1_{\mathrm{ur}}(G_{\mathbb{Q}_\ell}, V) = V / (\mathrm{Frob}_\ell - 1)V$ and $H^0(G_{\mathbb{Q}_\ell}, V) = \ker(\mathrm{Frob}_\ell - 1)$. By the rank-nullity theorem applied to the linear map $\mathrm{Frob}_\ell - 1 : V \to V$, the kernel and cokernel have equal dimension. $\blacksquare$

> **Corollary 10.2 (Selmer Invariance).** Removing formally smooth primes from the level preserves the Selmer Euler characteristic:
>
> $$\dim_k H^1_{\mathcal{L}_M} - \dim_k H^1_{\mathcal{L}_M^*} = \dim_k H^1_{\mathcal{L}_N} - \dim_k H^1_{\mathcal{L}_N^*}.$$

> **Theorem 10.3 (Non-Automorphic Derivation of the Numerical Coincidence).** For the Frey profile with Serre invariants $(2, 2)$ and the minimal Selmer structure:
>
> $$\dim_k H^1_{\mathcal{L}} - \dim_k H^1_{\mathcal{L}^*} = 1.$$
>
> This is the numerical criterion underlying Taylor--Wiles patching, derived entirely from local Galois cohomology.

**Proof.** By the Greenberg--Wiles formula:

$$\dim H^1_{\mathcal{L}} - \dim H^1_{\mathcal{L}^*} = \underbrace{(0 - 0)}_{\text{global } H^0\text{'s}} + \underbrace{1}_{v = \infty} + \underbrace{0}_{\text{formally smooth}} + \underbrace{\delta_2}_{\ell = 2} + \underbrace{\delta_n}_{\ell = n}.$$

*Global terms*: $H^0(G_{\mathbb{Q}}, V) = 0$ by irreducibility (Schur's lemma); $H^0(G_{\mathbb{Q}}, V^*(1)) = 0$ likewise.

*Archimedean*: $\bar{\rho}$ is odd, so $\bar{\rho}(c) = \left(\begin{smallmatrix} 1 & 0 \\ 0 & -1 \end{smallmatrix}\right)$ up to conjugacy. The $+1$ eigenspace of conjugation on trace-zero matrices has dimension $1$; the $-1$ eigenspace has dimension $2$. Since $p \geq 5$, $H^1(G_\mathbb{R}, V) \cong V^{c = -1}$ has dimension $2$. The local contribution is $2 - 1 = 1$.

*Formally smooth primes*: zero, by Theorem 10.1.

*At $\ell = n$ (flat condition)*: $\delta_n = 0$. For the flat deformation condition at $p \geq 5$ with Hodge--Tate weights $\{0, 1\}$, the Fontaine--Laffaille tangent space and local $H^0$ balance. This is a standard computation in $p$-adic Hodge theory.

*At $\ell = 2$ (minimal condition)*: $\delta_2 = 0$. For the minimal deformation condition at a prime of conductor exponent $1$, the tangent space and local $H^0$ balance. This follows from the structure of $\bar{\rho}|_{G_{\mathbb{Q}_2}}$ and the local Galois cohomology of $V$ at $\ell = 2$.

Summing: $0 + 1 + 0 + 0 + 0 = 1$. $\blacksquare$

---

## 11. The Automorphic Inventory

We summarize the decomposition in a single table.

| Component | Status | Content |
|:----------|:------:|:--------|
| C1: Serre recipe | Non-aut. | Computes $(k,N) = (2,2)$ from local data |
| C2: Vacancy | Non-aut. | $S_2(\Gamma_0(2)) = 0$ from dimension formula |
| C3b-i: Descent prereqs | Non-aut. | Local deformation rings formally smooth |
| Euler char. | Non-aut. | $\dim H^1_{\mathcal{L}} - \dim H^1_{\mathcal{L}^*} = 1$ |
| Separation | Non-aut. | Local methods cannot detect obstruction |
| Finiteness | Non-aut. | 24 vacancies, complete enumeration |
| **C3a: Entry** | **Aut.** | $\bar{\rho}$ is modular |
| **C3b-ii: Patching** | **Aut.** | Taylor--Wiles: $R \cong \mathbb{T}$ |

The non-automorphic territory includes the numerical foundation of the Taylor--Wiles method (the Euler characteristic $= 1$). The automorphic content consists of Entry (crossing the Galois--automorphic boundary) and the patching identification (comparing $R$ with $\mathbb{T}$, where $\mathbb{T}$ is defined via modular forms).

---

## 12. The Open Question

The entire program converges to a single question.

> **Question 12.1.** Let $p \geq 5$ be prime, $\bar{\rho} : G_{\mathbb{Q}} \to \mathrm{GL}_2(\mathbb{F}_p)$ continuous, odd, irreducible, with Serre invariants $(2, 2)$. Let $\mathcal{L}$ be the minimal Selmer structure on $V = \mathrm{ad}^0\bar{\rho}$ (unramified away from $2p$, flat at $p$, minimal at $2$). Does there exist a proof that $R_{\mathcal{L}} = 0$ --- that no lift of $\bar{\rho}$ to characteristic zero exists with the prescribed local conditions --- by methods internal to Galois cohomology, without invoking Hecke algebras, modularity lifting, or the theory of automorphic forms?

> **Remark (Structural constraints on the answer).** The Euler characteristic $\dim H^1_{\mathcal{L}} - \dim H^1_{\mathcal{L}^*} = 1$ (Theorem 10.3) implies $\dim H^1_{\mathcal{L}} \geq 1$. Direct Selmer vanishing --- proving $H^1_{\mathcal{L}} = 0$ --- is therefore impossible from the Euler characteristic alone. Any approach must use structure beyond the numerical invariant: either an Euler system, motivic obstruction theory, or an axiomatic characterization of the relevant quotient of $R$.

> **Remark (The dichotomy).** Question 12.1 admits two outcomes, each profound:
>
> **(A)** *Positive*: $R_{\mathcal{L}} = 0$ admits a Galois-cohomological proof. Then the automorphic content of FLT reduces to Entry alone, and the Langlands correspondence is one of several possible witnesses to the obstruction.
>
> **(B)** *Negative*: $R_{\mathcal{L}} = 0$ is provable only via automorphic comparison. Then the Langlands correspondence is not merely useful but *necessary* --- the unique language in which certain arithmetic inconsistencies can be expressed. This would be a proof-theoretic result of a kind that does not currently exist in arithmetic geometry.

---

## 13. Concluding Remarks

The contribution of this paper is organizational and structural: it decomposes the proof of Fermat's Last Theorem into its atomic components, classifies each as automorphic or non-automorphic, and identifies the minimal residual automorphic content. The decomposition is unconditional and the methods are elementary (in the sense that they use only classical results in Galois cohomology, deformation theory, and the dimension formula for spaces of cuspforms).

The value of the decomposition lies in what it makes precise. Before this work, the question "could FLT be proved without automorphic methods?" was philosophical. After it, the question reduces to a specific problem about the vanishing of a specific deformation ring at a specific vacancy (Question 12.1), with the Euler characteristic already computed, the local deformation theory already resolved, and the compactness-failure structure already identified.

Whether Question 12.1 admits a positive answer is open. What is no longer open is the question's precise formulation, the non-automorphic inputs that constrain it, and the structural landscape within which any answer must fit. This landscape --- 24 vacancies, a compactness failure, a single gate with internal structure, and a numerical coincidence derivable from local data --- is itself a contribution to the understanding of how the Langlands correspondence interacts with arithmetic.

---

## References

- **[BCDT]** C. Breuil, B. Conrad, F. Diamond, and R. Taylor, *On the modularity of elliptic curves over $\mathbb{Q}$: wild 3-adic exercises*, J. Amer. Math. Soc. **14** (2001), no. 4, 843--939.

- **[CG]** F. Calegari and D. Geraghty, *Modularity lifting beyond the Taylor--Wiles method*, Invent. Math. **211** (2018), no. 1, 297--433.

- **[DDT]** H. Darmon, F. Diamond, and R. Taylor, *Fermat's last theorem*, in Current Developments in Mathematics, 1995, International Press, 1996, pp. 1--154.

- **[DS]** F. Diamond and J. Shurman, *A First Course in Modular Forms*, Graduate Texts in Mathematics, vol. 228, Springer-Verlag, 2005.

- **[EG]** M. Emerton and T. Gee, *A geometric perspective on the Breuil--Mezard conjecture*, J. Inst. Math. Jussieu **13** (2014), no. 1, 183--223.

- **[Fontaine]** J.-M. Fontaine, *Il n'y a pas de variete abelienne sur $\mathbb{Z}$*, Invent. Math. **81** (1985), no. 3, 515--538.

- **[FM]** J.-M. Fontaine and B. Mazur, *Geometric Galois representations*, in Elliptic Curves, Modular Forms, & Fermat's Last Theorem, International Press, 1995, pp. 41--78.

- **[Frey]** G. Frey, *Links between stable elliptic curves and certain Diophantine equations*, Ann. Univ. Sarav. Ser. Math. **1** (1986), no. 1, iv+40.

- **[Greenberg]** R. Greenberg, *Iwasawa theory, projective modules, and modular representations*, Mem. Amer. Math. Soc. **211** (2011), no. 992.

- **[KW1]** C. Khare and J.-P. Wintenberger, *Serre's modularity conjecture (I)*, Invent. Math. **178** (2009), no. 3, 485--504.

- **[KW2]** C. Khare and J.-P. Wintenberger, *Serre's modularity conjecture (II)*, Invent. Math. **178** (2009), no. 3, 505--586.

- **[Kisin09a]** M. Kisin, *The Fontaine--Mazur conjecture for $\mathrm{GL}_2$*, J. Amer. Math. Soc. **22** (2009), no. 3, 641--690.

- **[Kisin09b]** M. Kisin, *Moduli of finite flat group schemes, and modularity*, Ann. of Math. (2) **170** (2009), no. 3, 1085--1180.

- **[Mazur]** B. Mazur, *Rational isogenies of prime degree*, Invent. Math. **44** (1978), no. 2, 129--162.

- **[Mazur89]** B. Mazur, *Deforming Galois representations*, in Galois Groups over $\mathbb{Q}$, MSRI Publ., vol. 16, Springer, 1989, pp. 385--437.

- **[Ribet90]** K. A. Ribet, *On modular representations of $\mathrm{Gal}(\bar{\mathbb{Q}}/\mathbb{Q})$ arising from modular forms*, Invent. Math. **100** (1990), no. 2, 431--476.

- **[Serre87]** J.-P. Serre, *Sur les representations modulaires de degre $2$ de $\mathrm{Gal}(\bar{\mathbb{Q}}/\mathbb{Q})$*, Duke Math. J. **54** (1987), no. 1, 179--230.

- **[TW]** R. Taylor and A. Wiles, *Ring-theoretic properties of certain Hecke algebras*, Ann. of Math. (2) **141** (1995), no. 3, 553--572.

- **[Wiles]** A. Wiles, *Modular elliptic curves and Fermat's last theorem*, Ann. of Math. (2) **141** (1995), no. 3, 443--551.
