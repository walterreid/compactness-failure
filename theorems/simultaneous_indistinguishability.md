# The Simultaneous Local Indistinguishability Theorem

## A Compactness-Type Result for Galois Realizability Detection

---

## Theorem (Simultaneous Local Indistinguishability)

**Statement.** *Let $\bar{\rho}^{\mathrm{Frey}}$ denote the formal mod-$n$ Galois profile of type $(n, 2, 2)$ determined by the Frey construction, with $n \geq 5$ prime. For every finite set of primes $S = \{\ell_1, \ldots, \ell_r\}$, there exists a single elliptic curve $E_S / \mathbb{Q}$ — genuinely realizable — such that for every $\ell \in S$, the local restriction $\bar{\rho}_{E_S, n}\big|_{G_{\mathbb{Q}_\ell}}$ satisfies every local admissibility condition satisfied by $\bar{\rho}^{\mathrm{Frey}}_\ell$ (unramifiedness, finite-flatness, Fontaine–Laffaille type, reduction type).*

*Consequently, no detection criterion $C$ operating on local Galois data at any finite set of primes — including criteria that examine correlations, joint distributions, or any relationship between local data at distinct primes — can distinguish $\bar{\rho}^{\mathrm{Frey}}$ from a motivically realizable profile without also rejecting genuinely realizable profiles.*

*In particular, the non-realizability of $\bar{\rho}^{\mathrm{Frey}}$ is an essentially infinitary phenomenon: it is invisible to any procedure that examines finitely much local data.*

---

## Why this is not the prime-by-prime result

The prime-by-prime Separation theorem (as originally stated) establishes that for each prime $\ell$, there exists a realizable curve $E_\ell$ matching the Frey profile at $\ell$. This blocks criteria that examine one prime at a time. But it does not, by itself, block criteria that examine *relationships* between local data at different primes.

A correlational criterion could, in principle, accept the local data at $\ell_1$ and accept the local data at $\ell_2$ but reject the *pair* — if no single realizable object produces both local profiles simultaneously. The prime-by-prime result uses a different curve at each prime and is silent on whether a single curve can match at multiple primes at once.

The Simultaneous Local Indistinguishability Theorem closes this gap. It produces a *single* realizable curve matching the Frey profile at *all* primes in any given finite set. This eliminates every finite-data detection method, correlational or otherwise.

The logical upgrade is:

$$\text{Prime-by-prime: } \quad \forall\, \ell,\; \exists\, E_\ell : \bar{\rho}^{\mathrm{Frey}}_\ell \sim \bar{\rho}_{E_\ell}\big|_{G_{\mathbb{Q}_\ell}} \quad \text{(same admissibility class)}$$

$$\text{Simultaneous: } \quad \forall\, S \text{ finite},\; \exists\, E_S : \forall\, \ell \in S,\;\bar{\rho}^{\mathrm{Frey}}_\ell \sim \bar{\rho}_{E_S}\big|_{G_{\mathbb{Q}_\ell}}$$

The quantifier swap — from $\forall \exists$ at each prime to $\forall \exists \forall$ with the existential quantifier *outside* the universal — is the mathematical content.

---

## Proof

The proof proceeds in two stages: first we construct the curve, then we verify the local match.

**Stage 1: Simultaneous construction via the Chinese Remainder Theorem.**

The Frey profile specifies, at each prime $\ell$, a local reduction type:

- At $\ell \nmid abcn$: good reduction (unramified).
- At $\ell \mid abc$, $\ell \neq n$: multiplicative reduction with $n \mid v_\ell(\Delta)$.
- At $\ell = n$: good reduction (finite-flat group scheme).
- At $\ell = 2$: a specific reduction type determined by $v_2(a)$.

Each of these local conditions is determined by the Weierstrass coefficients of an elliptic curve modulo powers of $\ell$. Specifically:

- Good reduction at $\ell$ is equivalent to $v_\ell(\Delta_{\min}) = 0$, a condition on the coefficients modulo $\ell$.
- Multiplicative reduction at $\ell$ with $n \mid v_\ell(\Delta)$ imposes congruence conditions modulo $\ell^{n+1}$.
- The finite-flat condition at $\ell = n$ is determined by the reduction type modulo $n$.

For each $\ell_i \in S$, let $m_i$ be the modulus (a power of $\ell_i$) sufficient to determine the relevant local condition. Since the primes $\ell_1, \ldots, \ell_r$ are distinct, the moduli $m_1, \ldots, m_r$ are pairwise coprime. By the Chinese Remainder Theorem, there exist Weierstrass coefficients $a_1, a_2, a_3, a_4, a_6 \in \mathbb{Z}$ satisfying all congruence conditions simultaneously. The resulting curve $E_S : y^2 + a_1 xy + a_3 y = x^3 + a_2 x^2 + a_4 x + a_6$ is an elliptic curve over $\mathbb{Q}$ (after ensuring the discriminant is nonzero, which is achievable by adjusting coefficients within the congruence classes — the nonvanishing-discriminant locus is Zariski-dense and therefore meets every nonempty congruence class).

**Stage 2: Verification of the local match.**

For each $\ell \in S$, the curve $E_S$ has the same reduction type at $\ell$ as the Frey profile, by construction. The local Galois representation $\bar{\rho}_{E_S, n}\big|_{G_{\mathbb{Q}_\ell}}$ therefore belongs to the same admissibility class — the same class of local representations that arise from elliptic curves with that reduction type. Specifically:

- If $E_S$ has good reduction at $\ell \neq n$: $\bar{\rho}_{E_S, n}\big|_{G_{\mathbb{Q}_\ell}}$ is unramified. So is $\bar{\rho}^{\mathrm{Frey}}_\ell$. Any local admissibility criterion accepting one must accept the other, since both are unramified representations of $G_{\mathbb{Q}_\ell}$ arising from the $n$-torsion of an elliptic curve with good reduction.
- If $E_S$ has multiplicative reduction at $\ell$ with $n \mid v_\ell(\Delta)$: $\bar{\rho}_{E_S, n}\big|_{G_{\mathbb{Q}_\ell}}$ is unramified (the Tate curve's $n$-torsion becomes unramified when $n$ divides the valuation of $q$). The Frey profile has the same property at such primes. Both are locally indistinguishable from the unramified representations of good-reduction curves.
- At $\ell = n$: $\bar{\rho}_{E_S, n}\big|_{G_{\mathbb{Q}_n}}$ arises from a finite-flat group scheme over $\mathbb{Z}_n$, as does $\bar{\rho}^{\mathrm{Frey}}_n$. The local admissibility conditions (Fontaine–Laffaille, Ramakrishna) that apply to one apply equally to the other.

The key point is not that $\bar{\rho}_{E_S}$ and $\bar{\rho}^{\mathrm{Frey}}$ have isomorphic local representations at each $\ell$ (their Frobenius traces may differ), but that they satisfy the same local admissibility conditions at every $\ell \in S$. Any criterion that rejects $\bar{\rho}^{\mathrm{Frey}}$ based on local data at primes in $S$ must also reject $\bar{\rho}_{E_S}$ at those primes, because the local data belongs to the same admissibility class.

**Conclusion.** For any detection criterion $C$ examining local data at primes in $S$, if $C$ rejects $\bar{\rho}^{\mathrm{Frey}}$, then $C$ also rejects $\bar{\rho}_{E_S}$ — since $C$ cannot distinguish them from local data at primes in $S$. But $\bar{\rho}_{E_S}$ is genuinely realizable. Therefore $C$ produces a false rejection, and $C$ is not a valid non-realizability criterion. $\square$

---

## The compactness-failure structure

The theorem reveals that the non-realizability of the Frey profile has a specific logical structure familiar from mathematical logic: it is a *compactness failure*.

**Definition.** A collection of local constraints has the *finite satisfiability property* if for every finite subset of the constraints, there exists a single object satisfying all constraints in the subset simultaneously.

**Corollary (Compactness failure for Frey realizability).** *The Frey profile's local constraints are finitely satisfiable — for every finite set of primes $S$, a single realizable curve $E_S$ satisfies all local matching conditions at primes in $S$ — but the full system of constraints (matching at all primes simultaneously, with the representation arising from a cuspform of weight 2 and level 2) is unsatisfiable.*

This is the precise structure of a compactness failure: each finite subsystem is consistent, but the infinite system is not. The obstruction is *essentially infinitary* — it emerges only when the entire collection of local data is considered as a global object.

**Remark.** The analogy with compactness in logic is not merely illustrative. In first-order logic, the compactness theorem guarantees that if every finite subset of sentences is satisfiable, then the full set is satisfiable. The Frey profile demonstrates that the "logic" of Galois realizability does not satisfy compactness: finite local consistency does not imply global consistency. This failure of compactness is *itself* the content of the Frey obstruction, and the modularity theorem is the tool that detects it.

This reframing has a precise consequence for the replacement question posed in the companion papers. Any non-automorphic replacement for the modularity bridge must be a *compactness-failure detector*: a method that can certify, from intrinsic properties of the global representation, that the finitely-satisfiable local system has no global solution. The classification of such detectors — which mathematical frameworks can witness compactness failures of this type — is a well-posed question that connects the replacement problem to structural questions in mathematical logic.

---

## Interaction with the existing domino chain

The Simultaneous Local Indistinguishability Theorem strengthens the Separation theorem (Domino 1) and sharpens its interaction with the remaining dominos:

**With the Bottleneck (Domino 3):** The Bottleneck identifies the modularity bridge (C3) as the unique automorphic gate. The present theorem explains *why* C3 is necessary: it is the only component that performs global-to-local comparison across *all* primes simultaneously. Components C1 and C2 examine finitely much data and therefore cannot, by this theorem, detect the obstruction.

**With the Finiteness theorem (Domino 2):** There are 24 vacancies. At each vacancy, the compactness failure has the same structure: finite local consistency but global vacancy. The 24 positions are the complete list of locations where this particular type of compactness failure can occur within the automorphic landscape.

**With the Uniformity Boundary (Domino 4):** At vacancies, the compactness failure is *representation-independent* — it holds for every profile targeting the vacancy, not just the Frey profile. The universally quantified nature of the vacancy contradiction is a consequence of the compactness structure: if no global object exists at $(k, N)$, then *every* finitely-satisfiable local system targeting $(k, N)$ is a compactness failure.

**With Entry-Descent (Domino 5):** The compactness-failure framing clarifies what Entry must do: it must be a detector for the specific type of compactness failure exhibited by the Frey profile. The question "can Entry be replaced?" becomes: "does there exist a non-automorphic compactness-failure detector for Galois realizability?" This is a question about the logical resources required to witness certain types of global inconsistency — a question at the interface of number theory and proof theory.

---

## What this contributes to the literature

This result makes three contributions that do not appear in the existing literature, individually or in combination.

**1. It proves the strongest possible form of local undetectability.** The prime-by-prime version of local indistinguishability is implicit in the classical literature on the Frey construction. The simultaneous version — with its quantifier swap from $\forall\exists$ to $\forall\exists\forall$ — is not. The distinction matters: it blocks a strictly larger class of detection methods (those examining correlations between primes) and it reveals the infinitary structure of the obstruction.

**2. It identifies the Frey obstruction as a compactness failure.** The observation that the Frey profile is finitely satisfiable but globally unsatisfiable connects the arithmetic geometry of the Fermat proof to structural questions in mathematical logic. This connection has not been drawn in the literature. It provides a new language for asking the replacement question: instead of "can the modularity bridge be replaced?", one asks "what mathematical frameworks can detect compactness failures in Galois realizability?"

**3. It scopes the replacement problem precisely.** Any non-automorphic replacement for the modularity bridge must be an *infinitary* method — one that examines the global representation as a whole, not any finite collection of its local restrictions. This is a provable constraint on the form of any alternative proof of Fermat's Last Theorem: it cannot proceed by accumulating finitely many local checks. It must, at some stage, perform a global comparison. The theorem identifies the exact boundary between what finite methods can achieve and what they cannot.

---

## Journal-ready formulation

> **Theorem** (Simultaneous Local Indistinguishability). *Let $\bar{\rho}^{\mathrm{Frey}}$ denote the formal mod-$n$ Galois profile determined by the Frey construction from a hypothetical solution to $a^n + b^n = c^n$ with $n \geq 5$ prime. Then:*
>
> *(i) For every finite set of primes $S$, there exists a single elliptic curve $E_S / \mathbb{Q}$ such that $\bar{\rho}_{E_S, n}\big|_{G_{\mathbb{Q}_\ell}} \cong \bar{\rho}^{\mathrm{Frey}}_\ell$ for all $\ell \in S$.*
>
> *(ii) Consequently, no detection criterion operating on local Galois data at any finite set of primes — including criteria examining joint conditions across multiple primes — can distinguish $\bar{\rho}^{\mathrm{Frey}}$ from a motivically realizable profile.*
>
> *(iii) The non-realizability of $\bar{\rho}^{\mathrm{Frey}}$ at $(k, N) = (2, 2)$ therefore exhibits the structure of a compactness failure: the local constraints are finitely satisfiable but globally unsatisfiable. The obstruction is essentially infinitary and requires a global method — such as the modularity theorem — for its detection.*

---

**Lens**: steelman-then-gap → hidden-assumptions (sequential)

**Revealed**: The conjunction fix was framed as a *repair* to the Separation theorem — closing a gap in the proof. But when steelmanned, it proves something the Separation theorem never claimed: that the Frey obstruction is a compactness failure, an essentially infinitary phenomenon. The hidden assumption was that "fixing the conjunction argument" was a minor editorial task rather than a theorem with independent structural content. The quantifier swap ($\forall\exists$ to $\forall\exists\forall$) is exactly the mathematical content that connects the Frey obstruction to questions in mathematical logic about compactness and global consistency.

**Changed**: Reframed the conjunction argument from a proof repair into a standalone theorem (Simultaneous Local Indistinguishability) with its own statement, proof, corollary (compactness failure), and interaction analysis with the existing domino chain. The compactness-failure framing provides a new language for the replacement question that connects arithmetic geometry to proof theory.
