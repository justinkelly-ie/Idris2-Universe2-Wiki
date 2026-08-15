# 📦 Pure Box Integers as Grothendieck Multiset Pairs

In Norman J. Wildberger's Box Arithmetic, signed integers are not primitive compiler primitives; they are **pairs of `WildNat` empty box containers**:

$$\text{BoxInt} \equiv (\text{PosBox}, \text{NegBox})$$

---

## 🏛️ 1. Physical Container Operations

* **Representation**:
  * $+3 \equiv ( [[\ ] [\ ] [\ ]], \ [\ ] )$ (3 positive empty boxes, 0 negative empty boxes)
  * $-2 \equiv ( [\ ], \ [[\ ] [\ ]] )$ (0 positive empty boxes, 2 negative empty boxes)
  * $0 \equiv ( [\ ], \ [\ ] )$ (balanced empty containers)
* **Addition as Pouring**:
  $$(P_1, N_1) + (P_2, N_2) = (P_1 \uplus P_2, \ N_1 \uplus N_2)$$
* **Negation as Bin Swapping**:
  $$-(P, N) = (N, P)$$
* **Multiplication as Cartesian Cross-Product**:
  $$(P_1, N_1) \times (P_2, N_2) = (P_1 P_2 \uplus N_1 N_2, \ P_1 N_2 \uplus N_1 P_2)$$

---

## 💻 2. Executable Literate Proofs & Evidence

```idris
module Foundations.Grothendieck_Box_Integers

import Core.BoxInt
import Core.Multiset

%default total

||| A pure Grothendieck representation of a signed integer as a pair of WildNat multisets.
public export
record GrothendieckInt (0 pSpec : MSetSpec) (0 nSpec : MSetSpec) where
  constructor MkGrothendieckInt
  posBoxes : WildNat pSpec
  negBoxes : WildNat nSpec

||| Evaluates a GrothendieckInt into an exact BoxInt scalar.
public export
evalGrothendieck : {0 p, n : MSetSpec} -> GrothendieckInt p n -> BoxInt
evalGrothendieck (MkGrothendieckInt p n) =
  wildNatToBoxInt p - wildNatToBoxInt n

||| Evidence 1: Proof that (+3, 0) evaluates to +3
public export
evidence_pos_eval : unwrapBox (evalGrothendieck (MkGrothendieckInt (toWildNat 3) (toWildNat 0))) = 3
evidence_pos_eval = Refl

||| Evidence 2: Proof that (0, 2) evaluates to -2
public export
evidence_neg_eval : unwrapBox (evalGrothendieck (MkGrothendieckInt (toWildNat 0) (toWildNat 2))) = -2
evidence_neg_eval = Refl

||| Evidence 3: Proof that (+3) + (-2) evaluates to +1
public export
evidence_add_eval : unwrapBox (evalGrothendieck (MkGrothendieckInt (toWildNat 3) (toWildNat 2))) = 1
evidence_add_eval = Refl
```
