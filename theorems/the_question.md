# An Open Question in Galois Cohomology

## Selmer Vanishing at Automorphic Vacancies Without Automorphic Comparison

---

### Question

Let $p \geq 5$ be prime, let $k = \mathbb{F}_p$, and let $\bar{\rho} : G_{\mathbb{Q}} \to \mathrm{GL}_2(k)$ be a continuous, odd, irreducible representation with Serre invariants $(k(\bar{\rho}), N(\bar{\rho})) = (2, 2)$.

The space $S_2(\Gamma_0(2)) = 0$ — a vacancy: no cuspform of weight 2 and level 2 exists.

Define the Selmer structure $\mathcal{L}$ on $V = \mathrm{ad}^0\bar{\rho}$ by imposing:

- the unramified condition at every prime $\ell \nmid 2p$,
- the flat (Fontaine–Laffaille) condition at $\ell = p$,
- the minimal condition at $\ell = 2$.

The Greenberg–Wiles formula gives $\dim_k H^1_{\mathcal{L}} - \dim_k H^1_{\mathcal{L}^*} = 1$, computed entirely from local Galois cohomology without automorphic input.

The universal deformation ring $R_{\mathcal{L}}$ parametrizing lifts of $\bar{\rho}$ with these local conditions has tangent space $H^1_{\mathcal{L}}(G_{\mathbb{Q}}, V)$.

In the Taylor–Wiles framework, the modularity theorem proves $R_{\mathcal{L}} \cong \mathbb{T}$, where $\mathbb{T}$ is the relevant Hecke algebra. At the vacancy, $\mathbb{T} = 0$, so the modularity theorem gives $R_{\mathcal{L}} = 0$ — no lifts exist with these local conditions. This produces the Fermat contradiction: the Frey representation would need to lift to a modular form at level 2, but no such form exists, and $R = 0$ confirms no compatible lift exists at all.

Every known proof that $R_{\mathcal{L}} = 0$ passes through the identification $R \cong \mathbb{T}$ and is therefore automorphic — it requires defining the Hecke algebra in terms of modular forms.

**The question:**

> *Does there exist a proof that $R_{\mathcal{L}} = 0$ — that no lift of $\bar{\rho}$ to characteristic zero exists with the prescribed local conditions — by methods internal to Galois cohomology, without invoking Hecke algebras, modularity lifting, or the theory of automorphic forms?*

> *Equivalently: can the global incompatibility of the local lifting conditions be certified by Galois-cohomological means — via Selmer group vanishing, Poitou–Tate duality, Euler system arguments, or obstruction theory in the deformation ring — when the target automorphic slot is vacant?*

---

### Context

This question isolates the residual automorphic content of the proof of Fermat's Last Theorem after systematic structural decomposition. The program establishing this decomposition proves:

1. The proof's automorphic content is concentrated in a single gate (the modularity bridge C3), with all other components — the Frey construction, the Serre recipe, the vacancy computation — being non-automorphic.

2. The gate splits into two independent sub-gates: Entry (the representation is modular at some level) and Descent (the level reduces to the Serre-predicted value).

3. Within Descent, the Galois-theoretic prerequisites — formal smoothness of local deformation rings at all removable primes, conductor concentration at $\ell = 2$ — are unconditionally resolved by non-automorphic means.

4. The formally smooth primes are Euler-characteristic-transparent: they contribute zero to the Greenberg–Wiles formula, making the Selmer Euler characteristic at the vacancy computable from local data at $\ell = 2$, $\ell = p$, and $v = \infty$ alone.

5. The completed computation gives Euler characteristic $= 1$, the numerical coincidence underlying Taylor–Wiles patching, derived without automorphic input.

6. The local conditions are finitely satisfiable — for any finite set of primes, a single elliptic curve simultaneously matches the Frey profile at all primes in the set — but globally unsatisfiable. This is a compactness failure: the non-existence of lifts ($R = 0$) is an essentially infinitary phenomenon.

The question therefore asks whether this specific compactness failure can be certified without automorphic comparison — whether the tools of Galois cohomology suffice to detect a global inconsistency that is invisible to any finite collection of local checks.

---

### What a positive answer would require

A proof that $R_{\mathcal{L}} = 0$ by non-automorphic means would need to establish, from the global structure of $G_{\mathbb{Q}}$ and the prescribed local conditions, that no compatible characteristic-zero lift exists. The available tools include:

**(a) Selmer vanishing via Poitou–Tate.** The exact sequence of Poitou–Tate relates $H^1_{\mathcal{L}}$ to $H^1_{\mathcal{L}^*}$ via local terms. The Euler characteristic $= 1$ constrains but does not determine the individual dimensions. A vanishing result for $H^1_{\mathcal{L}}$ (which would give $R$ trivial tangent space, hence $R = 0$ for reduced $R$) would require $\dim H^1_{\mathcal{L}^*} = -1$, which is impossible. So direct Selmer vanishing from the Euler characteristic alone does not work. **A subtler approach is needed** — one that uses additional structure beyond the Euler characteristic.

**(b) Euler systems.** Kolyvagin-type arguments construct cohomology classes that annihilate Selmer groups. Classical Euler systems are built from Heegner points on modular curves — but at a vacancy, no modular forms exist, so classical Heegner points are unavailable. The question becomes whether an Euler system can be constructed from the deformation-theoretic data (the Taylor–Wiles auxiliary primes, the structure of the local deformation rings) without passing through the automorphic world. The Taylor–Wiles primes provide a supply of cohomology classes at auxiliary levels; whether these can be organized into an Euler system that forces $R = 0$ at the vacancy is an open problem.

**(c) Obstruction theory in $R$.** The deformation ring $R$ is a quotient of a power series ring by relations coming from the global Galois cohomology obstruction group $H^2$. If $H^2$ with the prescribed local conditions is large enough to kill all of $H^1$, then $R = 0$. The computation of the relevant $H^2$ — the global obstruction to lifting with prescribed local conditions — is a Galois-cohomological problem that does not reference automorphic objects. Whether it yields $R = 0$ in this specific case is unknown.

**(d) Motivic or categorical methods.** The non-existence of lifts may be detectable by invariants of the representation that are defined within the motivic or tannakian framework — extension classes, period relations, or compatibility conditions in the conjectural category of mixed motives. This approach is the most speculative and depends on the development of tools that do not yet exist in the required form.

---

### What a negative answer would mean

A proof that $R_{\mathcal{L}} = 0$ *cannot* be established without automorphic comparison would be a result about the proof-theoretic necessity of the Langlands correspondence for arithmetic problems. It would establish that the Galois-automorphic bridge is not merely one available route to detecting the Frey obstruction but the *only* route — that the compactness failure in the space of Galois deformations is detectable only by methods that, at some level, reproduce the correspondence between Galois representations and automorphic forms.

Such a result would be a meta-mathematical theorem of a kind that does not currently exist in arithmetic geometry: a proof-theoretic independence result establishing that certain arithmetic facts require automorphic methods. The tools for proving such results (reverse mathematics for arithmetic geometry, proof-theoretic ordinal analysis at the level of étale cohomology) do not currently exist.

---

### Why this question could not have been asked before

The classical formulation — "can FLT be proved without modularity?" — is too broad to be mathematically productive. The structural decomposition narrows it to a single, precisely stated problem about a specific deformation ring at a specific vacancy. The inputs to this problem (the Euler characteristic, the local deformation theory, the conductor computation, the compactness-failure structure) are now fully established by non-automorphic means. What remains is a single question about the global deformation ring, stated in the language of Galois cohomology, with concrete candidate approaches.

The question is well-posed, falsifiable in both directions, and connected to active research programs in the theory of Galois deformations, Euler systems, and the Langlands correspondence. Its resolution — in either direction — would constitute a significant advance in understanding the logical architecture of arithmetic geometry.
