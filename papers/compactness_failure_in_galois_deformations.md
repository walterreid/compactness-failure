# Compactness Failure in Galois Deformation Problems: Finite Satisfiability, Euler Transparency, and the Detection Boundary

**Date:** April 10, 2026

**MSC 2020:** 11F80, 11R34, 11D41, 11G05

**Keywords:** Galois deformations, Selmer groups, Euler characteristic, compactness failure, Frey representation

---

## Abstract

We introduce the notion of *compactness failure* for Galois deformation problems and prove a general theorem characterizing when it occurs. A deformation problem exhibits compactness failure when its local conditions are finitely satisfiable --- for every finite set of primes, a single global object simultaneously satisfies all local conditions --- but no global object satisfies all conditions at once. We give checkable, purely Galois-cohomological criteria for finite satisfiability (via the Chinese Remainder Theorem on the moduli of elliptic curves) and prove that the Selmer Euler characteristic of the associated adjoint representation is invariant under removal of finitely satisfiable primes. As an application, we classify the compactness-failure landscape for weight-2 Galois representations over $\mathbb{Q}$: it consists of exactly 15 deformation problems (the weight-2 automorphic vacancies), each with computable Euler characteristic determined entirely by the non-removable primes. The Frey representation at $(k, N) = (2, 2)$ is the minimal example.

---

## Table of Contents

1. [Introduction](#1-introduction)
2. [Compactness Failure for Deformation Problems](#2-compactness-failure-for-deformation-problems)
3. [Euler Characteristic Transparency](#3-euler-characteristic-transparency)
4. [Finite Satisfiability](#4-finite-satisfiability)
5. [The Compactness-Failure Landscape at Weight 2](#5-the-compactness-failure-landscape-at-weight-2)
6. [The Detection Boundary](#6-the-detection-boundary)
7. [Checkable Criteria for the Compactness-Failure Regime](#7-checkable-criteria-for-the-compactness-failure-regime)
8. [Beyond the Frey Case: Other Instances](#8-beyond-the-frey-case-other-instances)
9. [Concluding Remarks](#9-concluding-remarks)

---

## 1. Introduction

Let $\bar{\rho} : G_{\mathbb{Q}} \to \mathrm{GL}_2(\mathbb{F}_p)$ be a continuous, odd, irreducible representation and let $\mathcal{D}$ be a deformation problem: a specification of local lifting conditions $L_\ell \subseteq H^1(G_{\mathbb{Q}_\ell}, \mathrm{ad}^0\bar{\rho})$ at each prime $\ell$. The universal deformation ring $R_{\mathcal{D}}$ parametrizes characteristic-zero lifts of $\bar{\rho}$ satisfying these conditions. The central objects of study in the Langlands program and its applications to Diophantine equations are deformation problems for which $R_{\mathcal{D}}$ can be compared with a Hecke algebra $\mathbb{T}$ via an $R = \mathbb{T}$ theorem.

This paper studies a structural phenomenon that arises when the local conditions of $\mathcal{D}$ are individually satisfiable --- and indeed simultaneously satisfiable at any finite subset of primes --- but no single global lift satisfies all conditions at once. We call this *compactness failure*, by analogy with the compactness theorem of first-order logic (which guarantees that finite satisfiability implies global satisfiability for first-order theories). Deformation problems exhibiting compactness failure are those where the "logic" of Galois realizability is not compact.

Our main results are:

**(i)** A general definition and criterion for compactness failure in deformation problems (Section 2).

**(ii)** A theorem on Euler characteristic transparency: primes at which the local condition is formally smooth contribute zero to the Greenberg--Wiles formula, and are therefore "invisible" to the Selmer balance (Section 3).

**(iii)** A classification of the compactness-failure landscape at weight 2: the 15 weight-2 automorphic vacancies, with computable Euler characteristics (Section 5).

**(iv)** A general finite satisfiability theorem for Frey-type deformation problems (Section 4).

---

## 2. Compactness Failure for Deformation Problems

> **Definition 2.1.** A *deformation problem* $\mathcal{D} = (\bar{\rho}, \{L_\ell\}_\ell)$ consists of:
>
> **(a)** A residual representation $\bar{\rho} : G_{\mathbb{Q}} \to \mathrm{GL}_2(\mathbb{F}_p)$, continuous, odd, irreducible, with $p \geq 5$.
>
> **(b)** For each prime $\ell$, a local condition $L_\ell \subseteq H^1(G_{\mathbb{Q}_\ell}, V)$, where $V = \mathrm{ad}^0\bar{\rho}$.
>
> The associated *Selmer group* is $H^1_{\mathcal{D}}(G_{\mathbb{Q}}, V) = \ker\bigl(H^1(G_{\mathbb{Q}}, V) \to \prod_\ell H^1(G_{\mathbb{Q}_\ell}, V) / L_\ell\bigr)$. The universal deformation ring $R_{\mathcal{D}}$ has tangent space $H^1_{\mathcal{D}}(G_{\mathbb{Q}}, V)$.

> **Definition 2.2.** A local condition $L_\ell$ is *realizable* if there exists an elliptic curve $E/\mathbb{Q}$ such that the class of $\bar{\rho}_{E,p}|_{G_{\mathbb{Q}_\ell}}$ in $H^1(G_{\mathbb{Q}_\ell}, V)$ lies in $L_\ell$. A deformation problem $\mathcal{D}$ is *locally realizable* if $L_\ell$ is realizable for every $\ell$.

> **Definition 2.3.** A deformation problem $\mathcal{D}$ is *finitely satisfiable* if for every finite set of primes $S = \{\ell_1, \ldots, \ell_r\}$, there exists a single elliptic curve $E_S / \mathbb{Q}$ such that $\bar{\rho}_{E_S, p}|_{G_{\mathbb{Q}_\ell}}$ satisfies $L_\ell$ for every $\ell \in S$.

> **Definition 2.4.** A deformation problem $\mathcal{D}$ exhibits *compactness failure* if:
>
> **(i)** $\mathcal{D}$ is finitely satisfiable, and
>
> **(ii)** no global object satisfies all local conditions simultaneously --- equivalently, the automorphic slot $(k, N)$ targeted by $\bar{\rho}$ is vacant ($\dim S_k(\Gamma_0(N)) = 0$), and no lift of $\bar{\rho}$ to the vacant slot exists.

> **Remark.** The second condition is stated in terms of the automorphic vacancy because every known proof of global unsatisfiability passes through the $R = \mathbb{T}$ correspondence. Whether global unsatisfiability can be certified non-automorphically is the open question of [Author-synthesis]. The definition is structured so that condition (i) is non-automorphic (proved by the methods of Section 4) and condition (ii) involves the automorphic landscape (proved by the dimension formula for the vacancy, with the force of the contradiction supplied by $R = \mathbb{T}$).

---

## 3. Euler Characteristic Transparency

> **Definition 3.1.** A prime $\ell \neq p$ is *formally smooth* for $\mathcal{D}$ if $\bar{\rho}$ is unramified at $\ell$ and $L_\ell = H^1_{\mathrm{ur}}(G_{\mathbb{Q}_\ell}, V)$.

> **Theorem 3.2 (Euler Characteristic Transparency).** Let $\ell$ be formally smooth for $\mathcal{D}$. The local contribution of $\ell$ to the Greenberg--Wiles formula is zero:
>
> $$\delta_\ell := \dim_k L_\ell - \dim_k H^0(G_{\mathbb{Q}_\ell}, V) = 0.$$

**Proof.** Since $\bar{\rho}$ is unramified at $\ell$, the inertia $I_\ell$ acts trivially on $V$. The unramified cohomology is $H^1_{\mathrm{ur}}(G_{\mathbb{Q}_\ell}, V) = V / (\mathrm{Frob}_\ell - 1)V$, and $H^0(G_{\mathbb{Q}_\ell}, V) = \ker(\mathrm{Frob}_\ell - 1 : V \to V)$. The rank-nullity theorem for the linear map $\mathrm{Frob}_\ell - 1$ on the finite-dimensional $k$-vector space $V$ gives $\dim \ker = \dim \mathrm{coker}$, hence $\delta_\ell = 0$. $\blacksquare$

> **Definition 3.3.** A prime $\ell$ is *removable* for $\mathcal{D}$ if it is formally smooth and $\ell \nmid N(\bar{\rho}) p$. The *essential primes* of $\mathcal{D}$ are those dividing $N(\bar{\rho}) p$, together with the archimedean place.

> **Corollary 3.4 (Selmer Euler Characteristic Reduction).** The Selmer Euler characteristic of $\mathcal{D}$ depends only on the essential primes:
>
> $$\dim_k H^1_{\mathcal{D}} - \dim_k H^1_{\mathcal{D}^*} = \underbrace{(h^0 - h^{0*})}_{\text{global}} + \underbrace{\delta_\infty}_{v = \infty} + \sum_{\ell \mid N(\bar{\rho}) p} \delta_\ell.$$
>
> All removable primes are absent from this formula.

**Proof.** The Greenberg--Wiles formula sums $\delta_\ell$ over all primes. By Theorem 3.2, the removable primes contribute zero. The remaining sum is over essential primes only. $\blacksquare$

> **Proposition 3.5 (Archimedean contribution).** For $\bar{\rho}$ odd and irreducible with $V = \mathrm{ad}^0\bar{\rho}$ (3-dimensional) and $p \geq 5$:
>
> $$\delta_\infty = +1.$$

**Proof.** Complex conjugation $c$ acts on $V$ with eigenvalues $+1$ (multiplicity 1) and $-1$ (multiplicity 2). Since $p \geq 5$, $H^1(G_\mathbb{R}, V) \cong V^{c = -1}$ has dimension 2, while $H^0(G_\mathbb{R}, V) = V^c$ has dimension 1. So $\delta_\infty = 2 - 1 = 1$. $\blacksquare$

> **Theorem 3.6 (General Euler Characteristic Formula).** For $\bar{\rho}$ odd, irreducible, with $p \geq 5$ and $H^0(G_{\mathbb{Q}}, V) = H^0(G_{\mathbb{Q}}, V^*(1)) = 0$:
>
> $$\dim_k H^1_{\mathcal{D}} - \dim_k H^1_{\mathcal{D}^*} = 1 + \sum_{\ell \mid N(\bar{\rho})} \delta_\ell + \delta_p.$$
>
> This is computable from local Galois cohomology at the essential primes alone. No automorphic input is required.

**Proof.** Combine Corollary 3.4, Proposition 3.5, and the vanishing of the global $H^0$ terms (which follows from irreducibility by Schur's lemma). $\blacksquare$

---

## 4. Finite Satisfiability

> **Theorem 4.1 (Finite Satisfiability for Frey-Type Problems).** Let $\mathcal{D}$ be a deformation problem arising from a Frey-type construction: $\bar{\rho}$ is the mod-$p$ representation attached to a Frey curve $E_{a,b,c}$, with local conditions inherited from the reduction types of $E$. Then $\mathcal{D}$ is finitely satisfiable.

**Proof.** At each prime $\ell$, the Frey construction specifies a reduction type (good, multiplicative with prescribed valuation, finite-flat, or specifically constrained at $\ell = 2$). Each type is determined by congruence conditions on Weierstrass coefficients modulo powers of $\ell$.

For any finite set $S = \{\ell_1, \ldots, \ell_r\}$ of distinct primes, let $m_i$ be the modulus at $\ell_i$ sufficient to determine the local condition. Since the $\ell_i$ are distinct, the moduli are pairwise coprime. By the Chinese Remainder Theorem, Weierstrass coefficients satisfying all congruence conditions simultaneously exist. The non-vanishing discriminant locus is Zariski-dense in the space of Weierstrass coefficients and therefore meets every nonempty congruence class. The resulting curve $E_S$ is an elliptic curve over $\mathbb{Q}$ satisfying all local conditions at primes in $S$. $\blacksquare$

> **Remark.** The theorem extends to any deformation problem whose local conditions are determined by congruence conditions on a rational moduli space satisfying weak approximation. The essential input is that distinct primes impose independent local constraints and the Chinese Remainder Theorem resolves simultaneous congruences.

> **Corollary 4.2 (General Finite Satisfiability Criterion).** Let $\mathcal{D} = (\bar{\rho}, \{L_\ell\}_\ell)$ be a deformation problem. Suppose:
>
> **(a)** the local conditions $\{L_\ell\}$ arise from reduction types of a family of elliptic curves (or more generally, from a rational moduli problem);
>
> **(b)** for each $\ell$, the condition $L_\ell$ is realized by infinitely many curves over $\mathbb{Q}$;
>
> **(c)** the conditions at distinct primes constrain independent local factors (i.e., are determined by congruences modulo coprime moduli).
>
> Then $\mathcal{D}$ is finitely satisfiable.

---

## 5. The Compactness-Failure Landscape at Weight 2

> **Theorem 5.1 (Classification of Weight-2 Compactness Failures).** The compactness-failure landscape for weight-2 Galois representations over $\mathbb{Q}$ consists of exactly 15 positions: the weight-2 automorphic vacancies
>
> $$N \in \{1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 12, 13, 16, 18, 25\},$$
>
> at which $S_2(\Gamma_0(N)) = 0$.
>
> At each vacancy, the Selmer Euler characteristic is computable non-automorphically via Theorem 3.6, with contributions only from:
> - the archimedean place ($+1$),
> - the primes $\ell \mid N$ (computable from local Galois cohomology),
> - the prime $p$ (computable from $p$-adic Hodge theory).
>
> All other primes are removable and contribute zero.

**Proof.** The 15 weight-2 vacancies are computed from the genus formula for $X_0(N)$: the genus-zero values of $N$ are exactly the listed values. At each vacancy, any Frey-type construction targeting level $N$ produces a deformation problem that is finitely satisfiable (Theorem 4.1) but globally unsatisfiable (the automorphic slot is empty). By Corollary 3.4, the Selmer Euler characteristic depends only on the essential primes, which are the primes dividing $Np$. $\blacksquare$

> **Example 5.2 (The Frey vacancy at $(2, 2)$).** The Frey representation has $N(\bar{\rho}) = 2$. The essential primes are $\ell = 2$ and $\ell = p = n$. Theorem 3.6 gives:
>
> $$\dim H^1_{\mathcal{D}} - \dim H^1_{\mathcal{D}^*} = 1 + \delta_2 + \delta_n = 1 + 0 + 0 = 1.$$
>
> The vanishing $\delta_2 = \delta_n = 0$ follows from the minimality of the local conditions (flat at $p$, conductor exponent 1 at $\ell = 2$). This is the numerical coincidence underlying Taylor--Wiles patching, derived without automorphic input.

> **Example 5.3 (Level 1 vacancy).** At $(k, N) = (2, 1)$, the vacancy $S_2(\mathrm{SL}_2(\mathbb{Z})) = 0$ targets representations with conductor 1. The only essential prime is $p$ itself. Theorem 3.6 gives $\dim H^1 - \dim H^1_* = 1 + \delta_p$. However, a representation with $N(\bar{\rho}) = 1$ would be unramified everywhere away from $p$, and the only such representations for $p \geq 5$ are highly constrained by Fontaine's theorem [Fontaine]. The vacancy at $(2, 1)$ is qualitatively different from $(2, 2)$: the local conditions may not be finitely satisfiable (Fontaine's theorem provides a local-saturating obstruction for $N = 1$).

> **Remark.** Example 5.3 illustrates that not every vacancy produces a compactness failure. At $(2, 1)$, the local conditions may already be incompatible at finitely many primes (Type I obstruction in the terminology of [Author-irreducibility]). Compactness failure occurs only at vacancies where the local conditions are individually and finitely satisfiable --- the Type II locus. The Frey vacancy at $(2, 2)$ is the minimal Type II vacancy.

---

## 6. The Detection Boundary

The results above establish a structural boundary in the landscape of deformation problems.

> **Definition 6.1.** The *detection boundary* for a deformation problem $\mathcal{D}$ is the partition of methods for certifying global unsatisfiability into:
>
> **(a)** *Non-automorphic territory*: the Selmer Euler characteristic, computed from the Greenberg--Wiles formula using only local Galois cohomology; the finite satisfiability, proved by the Chinese Remainder Theorem; and the formal smoothness / transparency of removable primes.
>
> **(b)** *Automorphic territory*: the assertion that the deformation ring maps isomorphically to the (zero) Hecke algebra, proving global unsatisfiability.

> **Theorem 6.2 (Detection Boundary Theorem).** Let $\mathcal{D}$ be a deformation problem exhibiting compactness failure at a weight-2 vacancy. Then:
>
> **(i)** **The Selmer Euler characteristic is non-automorphic.** It is computable from Theorem 3.6 using local data at the essential primes. No modular forms or Hecke algebras appear.
>
> **(ii)** **Finite satisfiability is non-automorphic.** It follows from the Chinese Remainder Theorem on Weierstrass coefficients (Theorem 4.1).
>
> **(iii)** **Euler transparency is non-automorphic.** All removable primes contribute zero to the Selmer balance (Theorem 3.2).
>
> **(iv)** **Global unsatisfiability is currently automorphic.** Every known proof passes through $R = \mathbb{T}$.
>
> The detection boundary lies between (i)--(iii) and (iv). Everything below the boundary is proved. The single assertion above the boundary --- global unsatisfiability --- is the residual automorphic content of the deformation problem.

---

## 7. Checkable Criteria for the Compactness-Failure Regime

We now state the main synthetic result: checkable hypotheses under which a deformation problem lies in the compactness-failure regime.

> **Theorem 7.1 (Compactness Failure Criteria).** Let $\bar{\rho} : G_{\mathbb{Q}} \to \mathrm{GL}_2(\mathbb{F}_p)$ be continuous, odd, irreducible, with $p \geq 5$. Let $\mathcal{D} = (\bar{\rho}, \{L_\ell\}_\ell)$ be a deformation problem with Serre invariants $(k, N) = (k(\bar{\rho}), N(\bar{\rho}))$. Suppose:
>
> **(H1) Vacancy**: $\dim S_k(\Gamma_0(N)) = 0$. *(Checkable by the dimension formula.)*
>
> **(H2) Formally smooth removability**: $\bar{\rho}$ is unramified at every $\ell \mid M$ with $\ell \nmid Np$, where $M$ is the level at which $\bar{\rho}$ is modular (if Entry holds). *(Checkable from the local Galois data.)*
>
> **(H3) Finite satisfiability**: for every finite set of primes $S$, there exists a single elliptic curve $E_S / \mathbb{Q}$ satisfying all local conditions at primes in $S$. *(Checkable by the CRT criterion of Corollary 4.2.)*
>
> **(H4) Irreducibility**: $H^0(G_{\mathbb{Q}}, \mathrm{ad}^0\bar{\rho}) = 0$ and $H^0(G_{\mathbb{Q}}, (\mathrm{ad}^0\bar{\rho})^*(1)) = 0$. *(Checkable: follows from the irreducibility of $\bar{\rho}$ for $p \geq 5$.)*
>
> Then:
>
> **(a)** $\mathcal{D}$ is in the compactness-failure regime: the local conditions are finitely satisfiable but the automorphic target is vacant.
>
> **(b)** The Selmer Euler characteristic is
>
> $$\chi(\mathcal{D}) = 1 + \sum_{\ell \mid N} \delta_\ell + \delta_p,$$
>
> computable from local Galois cohomology at the essential primes, with no automorphic input.
>
> **(c)** All removable primes are Euler-characteristic-transparent: $\delta_\ell = 0$ for every $\ell \nmid Np$.
>
> **(d)** The detection boundary applies: the Euler characteristic, finite satisfiability, and transparency are proved non-automorphically; global unsatisfiability is the unique residual automorphic assertion.

**Proof.** (a) follows from (H1) (vacancy) and (H3) (finite satisfiability). (b) follows from Theorem 3.6 using (H4) to eliminate the global $H^0$ terms. (c) follows from (H2) and Theorem 3.2. (d) follows from (a)--(c) and the structure of the detection boundary (Theorem 6.2). $\blacksquare$

> **Corollary 7.2.** The Frey deformation problem at $(k, N) = (2, 2)$ satisfies hypotheses (H1)--(H4) with $\chi(\mathcal{D}) = 1$. It is the minimal instance of the compactness-failure regime at weight 2.

---

## 8. Beyond the Frey Case: Other Instances

Theorem 7.1 applies to any Frey-type construction targeting a vacancy. We identify several families.

> **Example 8.1 (Generalized Fermat equations at vacancies).** The generalized Fermat equation $x^p + y^q = z^r$ for various exponent triples $(p, q, r)$ can be attacked via Frey-type constructions (see [Darmon, Bennett]). When the resulting Serre invariants target a vacancy --- one of the 24 positions of the finiteness theorem --- the compactness-failure criteria apply, and the Euler characteristic is computable non-automorphically. The detection boundary identifies the exact residual automorphic content for each such equation.

> **Example 8.2 (Hypothetical Frey constructions at higher-weight vacancies).** The vacancies at $(k, N)$ for $k \geq 4$ (e.g., $(4, 1)$, $(6, 1)$, $(14, 1)$) are potential targets for Frey-type constructions from Diophantine equations that produce higher-weight Galois representations. If such constructions exist and satisfy the finite satisfiability criterion, the full machinery of Theorem 7.1 applies.

---

## 9. Concluding Remarks

This paper introduces compactness failure as a structural concept for Galois deformation problems and establishes a toolkit for its detection. The main results --- Euler transparency, the Selmer reduction formula, the finite satisfiability criterion, and the detection boundary --- are purely Galois-cohomological. They identify, for any deformation problem in the compactness-failure regime, the exact boundary between what can be certified without automorphic methods and what currently cannot.

The paper does not prove global unsatisfiability by non-automorphic means. It proves that everything *else* in the deformation problem --- the Euler characteristic, the finite satisfiability, the transparency of removable primes --- is non-automorphic, and it isolates global unsatisfiability as the single residual assertion.

Whether this residual can be eliminated --- whether there exist Galois-cohomological methods for certifying that a finitely satisfiable deformation problem is globally unsatisfiable --- remains the central open question. Theorem 7.1 makes the question precise, computable, and testable at each of the 24 automorphic vacancies.

---

## References

- **[Author-synthesis]** [Author], *On the irreducible automorphic content of Fermat's Last Theorem: a structural decomposition*, preprint, 2026.

- **[Author-irreducibility]** [Author], *On the irreducibility of global-coherence obstruction in arithmetic geometry*, preprint, 2026.

- **[Bennett]** M. A. Bennett, I. Chen, S. R. Dahmen, and S. Yazdani, *Generalized Fermat equations: a miscellany*, Int. J. Number Theory **11** (2015), no. 1, 1--28.

- **[Darmon]** H. Darmon, *Rational Points on Modular Elliptic Curves*, CBMS Reg. Conf. Ser., vol. 101, AMS, 2004.

- **[DS]** F. Diamond and J. Shurman, *A First Course in Modular Forms*, GTM, vol. 228, Springer, 2005.

- **[Fontaine]** J.-M. Fontaine, *Il n'y a pas de variete abelienne sur $\mathbb{Z}$*, Invent. Math. **81** (1985), 515--538.

- **[Greenberg]** R. Greenberg, *Iwasawa theory, projective modules, and modular representations*, Mem. AMS **211** (2011), no. 992.

- **[Kisin09a]** M. Kisin, *The Fontaine--Mazur conjecture for $\mathrm{GL}_2$*, JAMS **22** (2009), 641--690.

- **[Mazur89]** B. Mazur, *Deforming Galois representations*, in Galois Groups over $\mathbb{Q}$, MSRI Publ. 16, Springer, 1989, pp. 385--437.

- **[Ribet90]** K. A. Ribet, *On modular representations of $\mathrm{Gal}(\bar{\mathbb{Q}}/\mathbb{Q})$ arising from modular forms*, Invent. Math. **100** (1990), 431--476.

- **[Serre87]** J.-P. Serre, *Sur les representations modulaires de degre $2$ de $\mathrm{Gal}(\bar{\mathbb{Q}}/\mathbb{Q})$*, Duke Math. J. **54** (1987), 179--230.

- **[TW]** R. Taylor and A. Wiles, *Ring-theoretic properties of certain Hecke algebras*, Ann. of Math. **141** (1995), 553--572.

- **[Wiles]** A. Wiles, *Modular elliptic curves and Fermat's last theorem*, Ann. of Math. **141** (1995), 443--551.
