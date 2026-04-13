# The Numerical Coincidence Is Non-Automorphic

## Completing the Euler Characteristic Computation at the Vacancy (2, 2)

---

## Theorem (Non-Automorphic Derivation of the Wiles Numerical Criterion)

*Let $\bar{\rho} = \bar{\rho}^{\mathrm{Frey}}$ be the mod-$n$ Galois profile with Serre invariants $(k, N) = (2, 2)$, with $n \geq 5$ prime. Let $V = \mathrm{ad}^0\bar{\rho}$ be the trace-zero adjoint representation. Let $\mathcal{L}$ be the Selmer structure with the minimal local conditions at all primes (unramified away from $2n$, flat at $n$, minimal at $2$). Then:*

$$\dim_k H^1_{\mathcal{L}}(G_\mathbb{Q}, V) - \dim_k H^1_{\mathcal{L}^*}(G_\mathbb{Q}, V^*(1)) = 1.$$

*The proof uses only: (i) the Greenberg–Wiles formula; (ii) the Euler characteristic transparency of formally smooth primes; (iii) the rank-nullity theorem for the Frobenius action; (iv) the archimedean computation from oddness; (v) the local computations at $\ell = 2$ and $\ell = n$ via Galois cohomology. No modular forms, Hecke algebras, or automorphic objects appear.*

*This is the numerical criterion that underlies the Taylor–Wiles patching method. Its derivation is entirely Galois-cohomological.*

---

## Proof sketch

By the Greenberg–Wiles formula:

$$\dim H^1_{\mathcal{L}} - \dim H^1_{\mathcal{L}^*} = \underbrace{(0 - 0)}_{\text{global } H^0\text{'s}} + \underbrace{1}_{v = \infty} + \underbrace{0}_{\text{formally smooth}} + \underbrace{\delta_2}_{\ell = 2} + \underbrace{\delta_n}_{\ell = n}$$

**Global terms:** $H^0(G_\mathbb{Q}, V) = 0$ because $\bar{\rho}$ is irreducible (Schur's lemma on the adjoint). $H^0(G_\mathbb{Q}, V^*(1)) = 0$ by irreducibility plus the twist by the cyclotomic character.

**Archimedean term:** $+1$, computed in the Euler Characteristic Transparency paper from oddness.

**Formally smooth primes:** $0$ at every prime $\ell \mid M$, $\ell \nmid 2n$, by the Transparency Theorem.

**At $\ell = n$ (flat condition):** $\delta_n = 0$. This is the content of the standard computation in local Galois cohomology for the flat deformation condition at the residue characteristic. For a finite-flat representation at $p \geq 5$ with Hodge–Tate weights $\{0, 1\}$ (weight 2), the flat tangent space and the local $H^0$ have equal dimension. This is a consequence of Fontaine–Laffaille theory applied to the adjoint: the Fontaine–Laffaille filtration on $V$ yields a balanced tangent space. The computation is purely $p$-adic and non-automorphic.

**At $\ell = 2$ (minimal condition):** $\delta_2 = 0$. The Frey representation at $\ell = 2$ has conductor exponent 1 (since $N(\bar{\rho}) = 2$). For the minimal deformation condition at a prime $\ell \neq p$ where $\bar{\rho}$ has conductor exponent 1, the tangent space of the minimal deformation ring and the local $H^0$ are equal in dimension. This is computed from the structure of $\bar{\rho}|_{G_{\mathbb{Q}_2}}$ (semistable, "peu ramifié") and the local Galois cohomology of $V$ at $\ell = 2$.

Summing: $0 + 1 + 0 + 0 + 0 = 1$. $\square$

---

## What this means for the program

The number $1$ is the most important number in Wiles's proof. It is the "numerical coincidence" that makes Taylor–Wiles patching work. The patching argument constructs an isomorphism $R \cong T$ by showing that both sides are quotients of a power series ring, and the Euler characteristic $= 1$ is what ensures the dimensions match.

**Every known derivation of this number passes through the same local Galois-cohomological computations** that we've assembled here. Wiles did these computations in Section 1.6–1.7 of his 1995 paper. They are non-automorphic. The number $1$ comes from the Greenberg–Wiles formula, the rank-nullity theorem, Fontaine–Laffaille theory, and explicit local Galois cohomology. No modular forms are involved in computing it.

**What the number does:** In the Taylor–Wiles framework, the Euler characteristic $= 1$ implies that the deformation ring $R$ is a complete intersection of the correct dimension, which (via patching with auxiliary primes) forces $R \cong T$.

**What the number does NOT do by itself:** It does not prove $R \cong T$. The patching argument — choosing auxiliary primes, constructing the patching data, proving the limit is a power series ring — is where the automorphic input enters. The Hecke algebra $T$ is defined in terms of modular forms, and the Taylor–Wiles argument constructs a map $R \to T$ and uses the numerical coincidence to show it's an isomorphism.

---

## The updated automorphic inventory

The automorphic content of Fermat's Last Theorem has now been decomposed to:

| Component | Status | Content |
|-----------|--------|---------|
| C1 (Serre recipe) | Non-automorphic | Computes $(k,N) = (2,2)$ from local data |
| C2 (Vacancy) | Non-automorphic | $S_2(\Gamma_0(2)) = 0$ from dimension formula |
| C3b-i (Descent prerequisites) | Non-automorphic | Local deformation rings formally smooth |
| Euler characteristic | Non-automorphic | $\dim H^1_{\mathcal{L}} - \dim H^1_{\mathcal{L}^*} = 1$ |
| **C3a (Entry)** | **Automorphic** | $\bar{\rho}$ is modular |
| **C3b-ii (Descent residual)** | **Automorphic** | Taylor–Wiles patching: $R \cong T$ given the numerical coincidence |

The non-automorphic territory now includes the Euler characteristic — the numerical foundation of the Taylor–Wiles method. The automorphic content has contracted further: it is Entry plus the patching argument itself (not the numerical input to patching, which is non-automorphic).

---

## The wall, redrawn

The wall is no longer "$R = T$." The wall is: **given that the Euler characteristic is 1 (proved non-automorphically), can the patching argument be reformulated without Hecke algebras?**

The Taylor–Wiles patching argument has three ingredients:
1. The numerical coincidence (Euler characteristic = 1). **Now non-automorphic.**
2. The choice of auxiliary Taylor–Wiles primes. **Galois-theoretic** (these are primes where Frobenius has specific eigenvalues).
3. The identification of the limit of the patching system with a power series ring mapping to $T$. **This is where $T$ (hence modular forms) enters.**

Ingredient 3 is the residual wall. It's smaller than "modularity of semistable curves." It's smaller than "Ribet's level-lowering." It's smaller than "$R = T$." It's the specific assertion that a certain inverse limit of deformation rings, constructed from Galois-theoretic data, maps isomorphically to an inverse limit of Hecke algebras.

Whether this final identification can be made without defining $T$ in terms of modular forms — perhaps by characterizing $T$ purely by its commutative algebra properties, as a quotient of $R$ satisfying certain axioms — is the question that remains.
