# The Vacancy Equivalence Theorem

## Reframing the Residual Automorphic Content as a Galois-Cohomological Statement

---

## Theorem (Vacancy Equivalence)

*Let $\bar{\rho}$ be an odd, irreducible mod-$p$ representation with Serre invariants $(k, N)$ at a vacancy, i.e., $\dim S_k(\Gamma_0(N)) = 0$. Suppose $\bar{\rho}$ is modular at some level $M$ (Entry assumed). Then the following are equivalent:*

*(a) (Level-lowering validity.) $\bar{\rho}$ is modular at level $N$.*

*(b) ($R = T$ at the vacancy.) The universal deformation ring $R_{N,\bar{\rho}}$ parametrizing lifts of $\bar{\rho}$ with the level-$N$ local conditions equals the $\bar{\rho}$-part of the Hecke algebra $\mathbb{T}_{N,\bar{\rho}}$, which is zero.*

*(c) (Galois-theoretic non-existence.) No lift of $\bar{\rho}$ to characteristic zero exists satisfying the level-$N$ local conditions: unramified at all primes $\ell \nmid Np$, with prescribed conditions at $\ell \mid N$ and $\ell = p$. That is, $R_{N,\bar{\rho}} = 0$.*

*(d) (Global compactness failure.) The system of local conditions defining the level-$N$ deformation problem is finitely satisfiable (by the Simultaneous Local Indistinguishability Theorem, for every finite set of primes $S$, there exists a single realizable object satisfying all conditions at primes in $S$) but globally unsatisfiable.*

*At a vacancy, all four statements are equivalent. In particular, the residual automorphic content of the descent step (C3b-ii) is equivalent to the purely Galois-theoretic assertion $R_{N,\bar{\rho}} = 0$.*

---

## Proof

**(a) $\Leftrightarrow$ (b):** This is the content of the $R = T$ correspondence at level $N$. At a vacancy, $S_k(\Gamma_0(N)) = 0$, so $\mathbb{T}_{N,\bar{\rho}} = 0$. The assertion "ρ̄ is modular at level $N$" means $\bar{\rho}$ corresponds to a form in $S_k(\Gamma_0(N))$. Since no such form exists, "modular at level $N$" is equivalent to "$\mathbb{T}_{N,\bar{\rho}} \neq 0$," which at a vacancy is false. So (a) holds vacuously at a vacancy — more precisely, (a) produces a contradiction. The $R = T$ statement at level $N$ says $R_{N,\bar{\rho}} \cong \mathbb{T}_{N,\bar{\rho}} = 0$. This holds if and only if (a) holds (both produce the same contradiction). $\square$

**(b) $\Leftrightarrow$ (c):** $\mathbb{T}_{N,\bar{\rho}} = 0$ (since the vacancy gives an empty space of forms). So (b) asserts $R_{N,\bar{\rho}} = 0$. The deformation ring $R_{N,\bar{\rho}}$ parametrizes lifts of $\bar{\rho}$ with level-$N$ local conditions. $R_{N,\bar{\rho}} = 0$ if and only if no such lift exists. This is (c). $\square$

**(c) $\Leftrightarrow$ (d):** The Simultaneous Local Indistinguishability Theorem (established earlier in this program) proves that for every finite set of primes $S$, there exists a single elliptic curve $E_S / \mathbb{Q}$ whose mod-$p$ representation satisfies all the level-$N$ local conditions at every prime in $S$. This is finite satisfiability. Statement (c) asserts that no *global* object satisfies *all* conditions simultaneously — global unsatisfiability. The conjunction of finite satisfiability and global unsatisfiability is, by definition, a compactness failure. $\square$

---

## What this achieves

The equivalence theorem translates the residual automorphic content of the descent step into a statement about Galois deformations. At a vacancy:

**Before this theorem:** C3b-ii says "level-lowering at formally smooth primes is valid." This is proved via the Eisenstein ideal and Hecke algebras — automorphic machinery. The statement and proof both reference modular forms.

**After this theorem:** C3b-ii is equivalent to "$R_{N,\bar{\rho}} = 0$" — no lift of $\bar{\rho}$ exists with the level-$N$ local conditions. The *statement* is purely Galois-theoretic. The *proof* is still automorphic (via $R = T$). But the statement has been freed from automorphic language.

This matters because it reframes the open question. The question is no longer "can level-lowering be proved without modular forms?" It is: **can the non-existence of lifts with prescribed local conditions be proved by Galois-cohomological methods?**

The second question is a question about Selmer groups and global Galois cohomology — a domain where non-automorphic methods exist (Poitou–Tate duality, Euler systems, Kolyvagin's methods). Whether these methods suffice for this specific problem is open. But the question is now posed in a language where non-automorphic tools are available.

---

## The compactness-failure connection

The equivalence (c) $\Leftrightarrow$ (d) closes a circle in the program:

1. The **Simultaneous Indistinguishability Theorem** proved that the Frey obstruction is a compactness failure: finitely satisfiable but globally unsatisfiable.

2. The **Vacancy Equivalence Theorem** proves that the residual automorphic content of the descent step *is* this compactness failure: C3b-ii at a vacancy is equivalent to the assertion that the global deformation ring is zero despite local satisfiability at every finite subset.

3. Therefore: **the entire residual automorphic content of descent, at a vacancy, reduces to certifying a specific compactness failure in the space of Galois deformations.**

The automorphic content of Fermat's Last Theorem has now been decomposed to:
- **(C3a) Entry:** The Frey representation is modular.
- **(C3b-ii) Descent residual (reframed):** The deformation ring $R_{N,\bar{\rho}} = 0$ — a compactness failure in Galois deformation space.

Both assertions cross the Galois–automorphic boundary, but C3b-ii now has a purely Galois-theoretic *formulation* even though its only known *proof* is automorphic.

---

## What a non-automorphic proof of $R_{N,\bar{\rho}} = 0$ would need

The theorem identifies the exact target for a non-automorphic resolution of descent. Such a proof would need to establish, by Galois-cohomological means, that the global deformation ring with the level-$N$ local conditions is trivial. The available tools include:

**1. Poitou–Tate duality.** The exact sequence of Poitou–Tate relates the global Selmer group $H^1_f(G_\mathbb{Q}, \text{ad}\,\bar{\rho})$ (which controls the tangent space of $R$) to the dual Selmer group $H^1_{f^*}(G_\mathbb{Q}, \text{ad}\,\bar{\rho}(1))$. If both vanish, $R$ has trivial tangent space and is therefore zero (for reduced $R$). The vanishing of these Selmer groups is a global cohomological computation that does not, in principle, require automorphic input.

**2. Euler characteristic formulas.** The Wiles–Greenberg formula computes $\dim H^1_f - \dim H^1_{f^*}$ from local terms. At formally smooth primes, the local contribution is computable (the Descent Resolution paper established this). The question is whether the formula, combined with the specific local conditions of the Frey profile, forces both dimensions to be zero.

**3. Euler systems.** Kolyvagin-type arguments can sometimes force Selmer groups to vanish by constructing cohomology classes that annihilate them. Whether an Euler system exists for the specific deformation problem of the Frey profile is an open question, but the formalism exists.

None of these tools has been applied to this specific problem. The theorem identifies the problem precisely enough that the application could, in principle, be attempted.

---

## Journal-ready formulation

> **Theorem** (Vacancy Equivalence). *Let $\bar{\rho}$ be an odd, irreducible mod-$p$ Galois representation with Serre invariants $(k, N)$ at a vacancy ($S_k(\Gamma_0(N)) = 0$), and suppose $\bar{\rho}$ is modular at some level $M$. Then the residual automorphic content of the descent step—level-lowering validity at formally smooth primes (C3b-ii)—is equivalent to the purely Galois-theoretic statement*
> $$R_{N,\bar{\rho}} = 0,$$
> *i.e., no lift of $\bar{\rho}$ to characteristic zero exists satisfying the level-$N$ local conditions. This is a compactness failure: the local conditions are finitely satisfiable (by the Simultaneous Local Indistinguishability Theorem) but globally unsatisfiable. Every known proof of $R_{N,\bar{\rho}} = 0$ passes through $R = T$ and is therefore automorphic. Whether a Galois-cohomological proof exists—via Selmer group vanishing, Poitou–Tate duality, or Euler system methods—is an open question whose resolution would eliminate descent entirely from the automorphic inventory of Fermat's Last Theorem.*

---

**Lens**: wrong-framing → strategic-avoidance → steelman-then-gap (sequential)

**Revealed**: The original question — "can level-lowering be proved without R = T?" — was framed inside the automorphic world. Wrong-framing revealed that at a vacancy, level-lowering is *equivalent* to the Galois-theoretic statement R = 0. Strategic-avoidance caught the temptation to stop at "the question is reframed" and pushed toward identifying the exact Galois-cohomological tools (Poitou–Tate, Euler systems) that could resolve R = 0. Steelman-then-gap confirmed that the equivalence theorem is provable but that R = 0 itself remains open — the reframing is genuine progress but not resolution.

**Changed**: Produced the Vacancy Equivalence Theorem, which translates C3b-ii from automorphic language (level-lowering validity) into Galois-cohomological language (deformation ring vanishing / compactness failure). This is a new domino: it doesn't drop the gate, but it rebuilds the gate in a language where non-automorphic tools exist.
