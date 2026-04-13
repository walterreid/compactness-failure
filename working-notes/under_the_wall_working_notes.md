# Going Under the Wall

## The wrong frame I was in

I assumed: R = 0 requires H^1 = 0 (trivial tangent space).
The Euler characteristic forces H^1 >= 1.
Therefore R ≠ 0.
Therefore the gate can't be crossed.

But this reasoning has a hidden assumption: that R is a
LOCAL ring whose tangent space faithfully represents its
structure. Let me examine this assumption.

## When R = 0 despite H^1 ≠ 0

Case 1: R is not a domain. R could have nilpotents that
make it zero in a quotient that matters, even though its
tangent space is nontrivial.

Actually no — R = 0 means R is the zero ring. If the
tangent space t_R = H^1 is nontrivial, then R has a
surjection to k[epsilon]/(epsilon^2) (the dual numbers),
which is nonzero. So R ≠ 0 if H^1 ≠ 0.

Wait. Is that right? The tangent space of R is
Hom(R, k[epsilon]/(epsilon^2)). If this is nontrivial,
then there exists a nonzero map R → k[epsilon]/(epsilon^2),
which means R ≠ 0.

So R = 0 DOES require H^1 = 0.

And H^1 ≥ 1 (from chi = +1).

So R ≠ 0. Full stop.

## ... unless I'm computing H^1 of the wrong thing.

WAIT. Let me reconsider what R we're talking about.

In the FLT argument, the contradiction comes from
R = T and T = 0 at the vacancy. But R here is the
deformation ring parametrizing lifts with SPECIFIC local
conditions — the "level N" conditions.

The Selmer group H^1_L that I'm computing — which H^1 is
this? It's H^1 with the level-N local conditions.

BUT: there are DIFFERENT versions of "level-N conditions."

Version A: The deformation ring R_N parametrizing lifts
of rho-bar that are:
- unramified at all ell �174mid Np
- satisfy the Serre-recipe condition at ell | N
- satisfy the crystalline/flat condition at p

Version B: The deformation ring R_N^new parametrizing
lifts that are "new at level N" — lifts that don't come
from a lower level.

In Wiles's proof, R = T is proved for Version A. But at
a vacancy, T = 0 means there are no forms at level N,
INCLUDING oldforms. Wait — no. S_k(Gamma_0(N)) = 0 means
no forms at all, old or new. So T_N = 0 means T for
the full space at level N, not just newforms.

Hmm, but actually that's the vacancy condition.
S_2(Gamma_0(2)) = 0 means no cuspforms of any kind. So
T = 0 for the full Hecke algebra at level 2.

And R = T = 0 means no lifts with the level-2 conditions.

But H^1 (the Selmer group for the level-2 conditions) is
≥ 1 by the Euler characteristic. This means the tangent
space of R is nontrivial, which means R ≠ 0.

CONTRADICTION with R = T = 0?

No. Because R = T requires the MODULARITY THEOREM. R is
nonzero as a deformation ring. T is zero as a Hecke algebra.
R = T says these are isomorphic. This means R is FORCED
to be zero by the isomorphism — but R, as an abstract ring
without the automorphic comparison, is nonzero.

## THE REAL INSIGHT

R ≠ 0 as a Galois deformation ring.
T = 0 as a Hecke algebra.
R ≅ T forces R = 0.

But R is GENUINELY NONZERO without the automorphic input.

This means: there exist characteristic-zero lifts of rho-bar
with the level-N local conditions. These lifts are legitimate
Galois representations. They satisfy all the local conditions.
They just don't correspond to any modular form.

The modularity theorem says: these lifts don't exist BECAUSE
every lift must be modular (and no modular form exists at
level 2). But the lifts exist as solutions to the deformation
problem. The modularity theorem kills them by declaring that
non-modular lifts are impossible.

## What this means for going under the wall

Going UNDER the wall would mean: showing that the lifts
parametrized by R (which exist, since R ≠ 0) have a
PROPERTY that contradicts the vacancy — WITHOUT using
modularity.

For example: if every characteristic-zero lift with the
level-N conditions had to be modular (by SOME non-automorphic
argument), and no modular form exists at level N, then
R would be forced to zero.

But "every lift must be modular" IS the modularity theorem.
So going under the wall in this direction is just going
through the wall.

ALTERNATIVELY: showing that the lifts parametrized by R
are not GEOMETRIC — they don't come from motives. If no
geometric lift exists at level N (because the motivic slot
is empty), and you could show this by motivic/tannakian
methods, you'd have R = 0 in the "geometric" quotient.

But this is the Fontaine-Mazur conjecture approach, and
every known proof goes through modularity.

## A genuinely different direction: going under

What if the ant goes under the wall by not trying to
prove R = 0 AT ALL?

The contradiction in FLT requires:
1. rho-bar has invariants (2, 2)
2. No form exists at (2, 2)
3. rho-bar must correspond to a form at (2, 2)

What if we replace step 3 with:
3'. rho-bar has a PROPERTY P that is incompatible with
    the vacancy at (2, 2), where P is provable without
    automorphic methods.

Property P doesn't have to be "rho-bar is modular."
It could be any property that:
(a) is provable from the Galois-theoretic structure alone,
(b) is inconsistent with S_2(Gamma_0(2)) = 0.

What properties of rho-bar are inconsistent with a vacancy?

The vacancy says: no cuspform of weight 2 and level 2 exists.
This is a fact about modular forms, not about Galois
representations. For a Galois representation to "see" the
vacancy, it must INTERACT with the automorphic landscape.

Unless... the vacancy has a GALOIS-THEORETIC shadow.

## The Galois-theoretic shadow of a vacancy

The vacancy S_2(Gamma_0(2)) = 0 means:
- No weight-2 newform of level 2 exists.
- Equivalently: no elliptic curve over Q has conductor 2.

THAT second statement is purely geometric/arithmetic.
No elliptic curve over Q has conductor 2. This is a
theorem of Ogg (1966) that predates modularity.

Can we use Ogg's result instead of the modularity theorem?

Ogg proved: there is no elliptic curve over Q with
conductor N for N = 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 12.

His proof is non-automorphic — it uses the arithmetic of
elliptic curves directly (Néron models, Tate's algorithm).

If the Frey curve's mod-n representation had to come from
an elliptic curve of conductor 2, and Ogg says no such
curve exists, we'd have a non-automorphic contradiction.

But the Frey representation doesn't have to come from a
curve of conductor 2. It comes from the Frey curve, which
has conductor rad(abc). The modularity theorem forces it
to CORRESPOND to a form at level 2, which would come from
a curve of conductor 2 if it existed. Without modularity,
the Frey curve sits happily at its own conductor.

Still... Ogg's theorem proves the vacancy non-automorphically
(no elliptic curve of conductor 2 exists), and our program
proves the Serre recipe non-automorphically (rho-bar has
invariants (2,2)). The gap is STILL step 3: forcing
rho-bar to occupy the vacant slot.

## Is there a DIFFERENT property P?

What if P is not "rho-bar is modular" but "rho-bar comes
from an elliptic curve whose conductor must divide 2"?

The Frey curve has conductor rad(abc). If we could show,
by non-automorphic means, that the MOD-N representation
of the Frey curve must also arise from an elliptic curve
of conductor dividing 2...

This is EXACTLY what Ribet's theorem does (level-lowering).
And that's automorphic.

But wait. Faltings's isogeny theorem (the Tate conjecture
for abelian varieties) says: if two elliptic curves have
isomorphic Tate modules, they're isogenous. So if rho-bar
arises from the Frey curve AND from another curve E', then
E and E' are isogenous, hence have the same conductor.

So rho-bar can't arise from a curve of conductor 2 unless
the Frey curve itself has conductor 2. Which it doesn't
(it has conductor rad(abc)).

This doesn't help directly. But Faltings is non-automorphic.

## The ant's path

What if we go under like this:

1. rho-bar_{E,n} arises from the Frey curve E (conductor
   rad(abc)).
2. If rho-bar_{E,n} also arises from a curve E' of
   conductor 2, then E and E' are isogenous (Faltings).
3. Isogenous curves have the same conductor.
4. rad(abc) ≠ 2 (since a^n + b^n = c^n with n >= 5
   forces abc to have primes > 2).
5. Contradiction.

Steps 2-4 are non-automorphic. Step 1 is definitional.

THE MISSING STEP: "rho-bar also arises from a curve E'
of conductor 2." This is what modularity + level-lowering
gives you. Without it, we don't know rho-bar arises from
ANY other curve.

But what if we flip it? Instead of showing rho-bar arises
from a curve of conductor 2, show that rho-bar DOESN'T
arise from any curve of conductor 2 (because no such curve
exists, by Ogg), and THEN show this non-existence implies
something about the Frey curve itself?

The Frey curve exists (hypothetically). Its mod-n
representation exists. We need to derive a contradiction.
The classical route: rho-bar is modular → it corresponds
to a form at level 2 → no such form → contradiction.

The ant's route would need: rho-bar has property P →
P implies existence of a curve of conductor 2 → no such
curve exists (Ogg) → contradiction.

What is P? It would need to be:
- provable from the Frey construction
- implying that rho-bar has a "shadow" at conductor 2
- not requiring the full modularity theorem

This is essentially asking for a PARTIAL modularity result:
not "rho-bar is modular" but "rho-bar has enough modularity
to force a conductor-2 shadow."

The level-lowering aspect (going from conductor rad(abc)
to conductor 2) is what requires Ribet's theorem. But
Ribet's theorem was proved BEFORE Wiles (1990 vs 1995).
And Ribet's proof uses the Eisenstein ideal, which is
partly automorphic but much simpler than full modularity.

What if the ant's path is: assume JUST enough modularity
to apply Ribet (not full modularity of semistable curves),
use Ribet to get to level 2, use Ogg to kill it?

But Ribet's theorem ASSUMES rho-bar is modular at some
level M. That's Entry (C3a). Without Entry, Ribet has
nothing to work with.

## The actual bottom

The ant can't go under this wall because the wall IS
the floor. The modularity statement — rho-bar enters the
automorphic world — is the foundational step. Everything
else (Ribet, Ogg, the vacancy, the Serre recipe) is
built on top of it.

Going under the wall would mean finding a FLOOR beneath
the floor. A pre-automorphic, pre-motivic reason that
rho-bar is constrained. This is Conjecture 1 from the
parent paper: the pre-automorphic realizability obstruction.

And the program has been showing, systematically, that
this floor — if it exists — is not accessible by local
methods, not accessible by Selmer vanishing, not accessible
by reverse-Ramakrishna, and not accessible by twisting.

The remaining possibility: it's accessible by something
nobody has thought of yet. Or it doesn't exist, and the
automorphic floor is the actual floor.

That's Outcome (B) of the dichotomy.
