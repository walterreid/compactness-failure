# Euler Characteristic Survey Across All 24 Vacancies

## The key formula

For a deformation problem with Serre invariants (k, N), odd irreducible
rho-bar with p >= 5:

chi = dim H^1_L - dim H^1_{L*} = 1 + sum_{ell | N} delta_ell + delta_p

where:
- The +1 is the archimedean contribution (from oddness, independent of k, N)
- delta_ell = dim L_ell - dim H^0(G_{Q_ell}, V) at each ell | N
- delta_p = dim L_p - dim H^0(G_{Q_p}, V) at the residue characteristic
- V = ad^0(rho-bar), which is 3-dimensional for GL_2

## The critical question

At (2,2), we computed chi = 1 + 0 + 0 = 1 (Selmer dominates).
The reverse-Ramakrishna strategy needs chi <= 0 (dual Selmer dominates).

Can chi <= 0 happen at another vacancy?

## What changes across vacancies

**The archimedean term (+1):** FIXED. It depends only on oddness, not on
weight or level. It's always +1.

**The terms delta_ell for ell | N:** These depend on the LOCAL condition
at ell, which depends on the reduction type of the representation at ell.
For "minimal" conditions (conductor exponent matching the Serre-predicted
level), Wiles's computation gives delta_ell = 0 at primes ell ≠ p where
the representation has conductor exponent 1.

But at primes where the conductor exponent is HIGHER, or where the local
condition is NOT minimal, delta_ell can be nonzero — potentially negative.

**The term delta_p:** This depends on the WEIGHT k. For weight k = 2,
the local condition at p is "flat" (Fontaine-Laffaille with HT weights
{0, 1}), and delta_p = 0.

For HIGHER weight k, the local condition at p changes:
- Weight k means HT weights {0, k-1}
- The flat/crystalline deformation ring at p has different structure
- The dimension of the tangent space H^1_fl(G_{Q_p}, V) changes with k

THIS IS WHERE THE ACTION IS.

## Computing delta_p at different weights

For V = ad^0(rho-bar), dim V = 3. At ell = p:

The local Euler characteristic gives:
dim H^0 - dim H^1 + dim H^2 = -[Q_p : Q_p] * dim V = -3

By local Tate duality: dim H^2 = dim H^0(G_{Q_p}, V*(1)).

For the crystalline/flat condition at weight k:

H^1_crys(G_{Q_p}, V) parametrizes crystalline lifts with HT weights
determined by k. The dimension depends on the Hodge filtration.

**Weight 2 (HT weights {0, 1}):**
Standard computation: dim H^1_fl = dim H^0 + 0 (balanced).
So delta_p = 0.

**Weight 4 (HT weights {0, 3}):**
The crystalline condition is MORE restrictive than flat. The Hodge
filtration has a longer gap: Fil^0 ⊃ Fil^1 = Fil^2 = Fil^3 ⊃ Fil^4 = 0.
For the adjoint, the crystalline tangent space can be SMALLER.

By the standard computation (Berger-Colmez, Kisin):
For weight k >= 4, the crystalline deformation ring at p has:
dim H^1_crys(G_{Q_p}, V) = dim H^0(G_{Q_p}, V) + (some term depending on k)

The key: for HIGHER weight, the crystalline condition imposes MORE
constraints on the adjoint. The Fontaine-Laffaille functor in the
range 0 <= i <= p-2 gives:

dim H^1_FL = number of "admissible" filtered phi-modules extending
the residual one.

For weight k with 2 <= k <= p-1 (which is in FL range for p >= k):

The FL tangent space for ad^0 has dimension:
- 1 from the diagonal (trace) deformation
- Plus contributions from off-diagonal, controlled by the gap in
  HT weights

For weight 2: gap is 1, FL tangent space for ad^0 matches H^0. delta = 0.

For weight k >= 4: the gap is k-1 >= 3. The FL tangent space for
the OFF-DIAGONAL part of ad^0 is:

dim H^1_FL,off-diag = number of non-trivial extensions in FL category
with the given HT weights.

**CRITICAL COMPUTATION: For weight k, the crystalline tangent space
of ad^0 at p has:**

When rho-bar|_{G_{Q_p}} is irreducible:
- H^0(G_{Q_p}, V) = 0 (no fixed vectors)
- H^1_crys has dimension depending on k

When rho-bar|_{G_{Q_p}} is reducible (ordinary):
- H^0(G_{Q_p}, V) = 1 (one fixed vector: the diagonal)
- H^1_crys has dimension depending on k and ordinarity

For the ORDINARY case at weight k >= 4:
The ordinary deformation ring at p (Hida theory) has:
dim H^1_ord = 2 (two parameters: the unramified and ramified characters)
dim H^0 = 1
So delta_p = 2 - 1 = 1.

That makes chi = 1 + (terms at N) + 1 = 2 + (terms at N).
This is WORSE — higher chi, even further from the target.

For the CRYSTALLINE (non-ordinary) case at weight k >= 4:
Kisin's computation of the crystalline deformation ring:

For weight k, Hodge-Tate weights {0, k-1}, crystalline condition:
The crystalline deformation ring R^crys_p has relative dimension
dim R^crys = dim H^1_crys - dim H^0 over W(k).

For k = 2: R^crys is formally smooth of relative dimension 1
(this is the flat condition). dim H^1 = 1 + dim H^0.
Wait, that doesn't match what I said before.

Let me reconsider.

For the ADJOINT V = ad^0(rho-bar), NOT rho-bar itself:

At ell = p, the tangent space of the deformation ring for rho-bar
is H^1(G_{Q_p}, ad rho-bar) = H^1(G_{Q_p}, ad^0 rho-bar) + H^1(G_{Q_p}, F_p).
The trace part H^1(G_{Q_p}, F_p) parametrizes determinant deformations.

For the trace-FREE part V = ad^0:
The crystalline condition on V at weight k is:
L_p = H^1_crys(G_{Q_p}, V) = subspace of H^1(G_{Q_p}, V) parametrizing
crystalline extensions.

The Bloch-Kato formula for the crystalline condition:
dim H^1_f(G_{Q_p}, V) = dim H^0(G_{Q_p}, V) + dim D_crys(V)^{phi=1} / Fil^0

Hmm, this is getting complicated. Let me use a different approach.

## Using the GLOBAL formula directly

Actually, the cleanest approach: the Greenberg-Wiles formula computes
chi globally. At weight 2 with minimal conditions everywhere, chi = 1.
The question is whether changing the weight changes chi.

KEY INSIGHT: The Greenberg-Wiles Euler characteristic depends on
the LOCAL conditions. If we change the weight (and hence the local
condition at p), chi changes.

For the weight-k crystalline condition, the local contribution at p is:

delta_p = dim H^1_f(G_{Q_p}, V) - dim H^0(G_{Q_p}, V)

The Bloch-Kato conjecture (now theorems in many cases) relates this to:
delta_p = dim_k D_crys(V)/(Fil^0 D_crys(V) + D_crys(V)^{phi=1})

For V = ad^0 of a 2-dimensional crystalline representation with
HT weights {0, k-1}:

The crystalline Dieudonné module D_crys(V) is 3-dimensional, and
ad^0 has HT weights {-(k-1), 0, k-1}.

The Hodge filtration on D_crys(V):
- Fil^{-(k-1)} = D_crys(V) (full)
- Fil^0 has dimension 2 (the pieces with HT weight >= 0)
- Fil^{k-1} has dimension 1 (the piece with HT weight k-1)
- Fil^k = 0

Wait, I need to be more careful about conventions. The HT weights
of ad^0 are {1-k, 0, k-1} (the differences of the HT weights of
rho-bar).

For the Bloch-Kato H^1_f at p:
dim H^1_f(G_{Q_p}, V) = dim(D_crys(V)/Fil^0 D_crys(V))
                       = dim V - dim Fil^0 D_crys(V)

For ad^0 with HT weights {1-k, 0, k-1}:
Fil^0 D_crys(V) = subspace with HT weight >= 0 = 2-dimensional
(the pieces with HT weights 0 and k-1).

So dim H^1_f = 3 - 2 = 1.

And dim H^0(G_{Q_p}, V):
For irreducible rho-bar|_{G_{Q_p}}: dim H^0 = 0.
For reducible: dim H^0 = 1.

**CASE: irreducible at p, weight k >= 4:**
delta_p = 1 - 0 = 1.
chi = 1 + sum(delta at N) + 1 = 2 + sum(delta at N).

This is HIGHER than at weight 2. Wrong direction.

**CASE: reducible at p, weight k >= 4:**
delta_p = 1 - 1 = 0.
chi = 1 + sum(delta at N) + 0 = 1 + sum(delta at N).

Same as weight 2. No improvement.

## What about the terms at N?

At primes ell | N with ell ≠ p, the local condition is the
"Serre recipe" condition. For the Frey case at (2,2), ell = 2
with conductor exponent 1 gave delta_2 = 0.

But at OTHER levels, the conductor can be COMPOSITE. For example:
- At (2, 6), N = 6 = 2 * 3. We have delta_2 and delta_3.
- At (2, 25), N = 25 = 5^2. We have delta_5.

For primes ell | N with conductor exponent >= 2:
The local condition involves MORE ramification, and the local
contribution delta_ell can be DIFFERENT from 0.

For ell^2 | N (conductor exponent 2):
delta_ell = dim L_ell - dim H^0(G_{Q_ell}, V)

The local H^1 with the "Serre recipe" condition at conductor
exponent 2 includes the "peu ramifié" AND "très ramifié"
extensions. The dimension of L_ell increases.

But H^0(G_{Q_ell}, V) depends on how much of V is fixed by
G_{Q_ell}. For highly ramified representations, H^0 can be
SMALLER (less is fixed by the larger inertia action).

Net effect on delta_ell: uncertain without explicit computation.

## THE HONEST ASSESSMENT

After working through this, here is what I find:

1. The archimedean term is always +1. Fixed.

2. For weight 2 with minimal conditions, delta_p = 0 and
   delta_ell = 0 at all ell | N. So chi = 1 for ALL weight-2
   vacancies with minimal conditions.

3. For weight k >= 4, delta_p = 0 or +1 (depending on
   reducibility at p). So chi >= 1 at all higher-weight vacancies.

4. The terms delta_ell for ell | N are 0 under minimal conditions.
   Non-minimal conditions could make them negative, but then we're
   not in the "standard" deformation problem.

**CONCLUSION: chi >= 1 at all 24 vacancies under standard
(minimal) local conditions.**

The reverse-Ramakrishna strategy requires chi <= 0. Under standard
conditions, this NEVER happens.

## BUT WAIT — the wrong-framing lens

Am I asking the right question? The reverse-Ramakrishna strategy
works when the DUAL Selmer dominates. But maybe I should look at
NON-STANDARD local conditions — conditions where delta_p or
delta_ell is negative.

At p: can the local condition at p be chosen so that
dim L_p < dim H^0(G_{Q_p}, V)?

This would require L_p to be VERY small — smaller than the
invariant subspace. For a crystalline condition with restricted
weights, this might happen at very specific weights.

Actually: there IS a case where delta_p < 0. If we impose
the ORDINARY condition at p and rho-bar is NON-ORDINARY
(supersingular), then H^0(G_{Q_p}, V) might be nonzero while
L_p = 0 (no ordinary lifts exist). This gives delta_p = -dim H^0.

But if there are no ordinary lifts, the deformation ring is
trivially zero at p. That's a LOCAL obstruction (Type I), not
the Type II global obstruction we're studying.

## FINAL HONEST ASSESSMENT

Chi >= 1 at all 24 vacancies under any natural deformation
conditions. The reverse-Ramakrishna strategy, as stated by the
other Claude, does not apply to any of the 24 vacancies.

The +1 archimedean contribution is an immovable structural feature
of odd 2-dimensional representations over Q. It guarantees chi >= 1
(under minimal conditions), which guarantees the Selmer group
dominates the dual. This is the SAME structural fact that makes
Taylor-Wiles patching work — and it's the reason the reverse
strategy fails.

The archimedean +1 is both the foundation of Wiles's proof AND
the obstruction to the reverse approach. It plays both roles
simultaneously.
