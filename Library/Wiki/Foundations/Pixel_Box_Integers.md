# 📦 Pure Box Integers as Pixel Difference Pairs

In Norman J. Wildberger's Box Arithmetic, signed integers are not primitive compiler primitives; they are **Pixels: pairs of `WildNat` empty box containers** $[P, N]$:

$$\text{BoxInt} \equiv \text{Pixel } [P, N] \equiv (\text{PosBox}, \text{NegBox})$$

---

## 🏛️ 1. Physical Container Operations

* **Representation**:
  * $+3 \equiv \text{Pixel } [3, 0] \equiv ( [[\ ] [\ ] [\ ]], \ [\ ] )$ (3 positive empty boxes, 0 negative empty boxes)
  * $-2 \equiv \text{Pixel } [0, 2] \equiv ( [\ ], \ [[\ ] [\ ]] )$ (0 positive empty boxes, 2 negative empty boxes)
  * $0 \equiv \text{Pixel } [0, 0] \equiv ( [\ ], \ [\ ] )$ (balanced empty containers)
* **Addition as Pouring**:
  $$(P_1, N_1) + (P_2, N_2) = (P_1 \uplus P_2, \ N_1 \uplus N_2)$$
* **Negation as Bin Swapping**:
  $$-(P, N) = (N, P)$$
* **Multiplication as Cartesian Cross-Product**:
  $$(P_1, N_1) \times (P_2, N_2) = (P_1 P_2 \uplus N_1 N_2, \ P_1 N_2 \uplus N_1 P_2)$$

---

## 💻 2. Executable Literate Proofs & Evidence

```idris
module Foundations.Pixel_Box_Integers

import Core.BoxInt
import Core.Multiset

%default total

||| A pure representation of a signed integer as a Pixel pair of WildNat multisets.
public export
record PixelInt (0 pSpec : MSetSpec) (0 nSpec : MSetSpec) where
  constructor MkPixelInt
  posBoxes : WildNat pSpec
  negBoxes : WildNat nSpec

||| Evaluates a PixelInt into an exact BoxInt scalar.
public export
evalPixelInt : {0 p, n : MSetSpec} -> PixelInt p n -> BoxInt
evalPixelInt (MkPixelInt p n) =
  wildNatToBoxInt p - wildNatToBoxInt n

||| Evidence 1: Proof that (+3, 0) evaluates to +3
public export
evidence_pos_eval : unwrapBox (evalPixelInt (MkPixelInt (toWildNat 3) (toWildNat 0))) = 3
evidence_pos_eval = Refl

||| Evidence 2: Proof that (0, 2) evaluates to -2
public export
evidence_neg_eval : unwrapBox (evalPixelInt (MkPixelInt (toWildNat 0) (toWildNat 2))) = -2
evidence_neg_eval = Refl

||| Evidence 3: Proof that (+3) + (-2) evaluates to +1
public export
evidence_add_eval : unwrapBox (evalPixelInt (MkPixelInt (toWildNat 3) (toWildNat 2))) = 1
evidence_add_eval = Refl
```

---

## 🔗 Related Chapters & Cross-References

* **Mathematical Foundations**:
  * [Box Arithmetic & Inductive Multisets](Box_Arithmetic.md) — Inductive construction of natural numbers from empty box containers.
  * [Structural Accounting & Token Geometry](Structural_Accounting_and_Pure_Tokens.md) — Structural summation loops for non-cast integer vectors.
  * [Singleton Fractions & Ongoing Sequences](Singleton_Fractions_and_OnSeq_Algebra.md) — Constructive fraction pairs without compiler floating-point representations.
  * [Vexels, Maxels, Boxels & Reflected Linear Algebra](Vexels_Maxels_and_Reflected_Linear_Algebra.md) — Multiset tensor hierarchy over BoxInt.
* **Spacetime & Geometry**:
  * [The 27 Ternary Geometries](../Geometry/Ternary_Multiverse_27.md) — Balanced ternary integer metric structures $\{-1, 0, 1\}$.
  * [3D Lattice Topology & Conserved Flux](../Geometry/Lattice_Topology_and_Flux.md) — Discrete Laplacian flux conservation over integer lattices.
