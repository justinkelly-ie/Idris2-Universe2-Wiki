# 🌌 Dynamic Grid Expansion (`expandAndUnfoldGeneric`)

To transition the **Idris2-Universe2** architecture forward from the initial macro-canvas into expanded higher-order matrix spaces, the engine uses the generalized **`expandAndUnfoldGeneric`** transformation pipeline.

To adhere strictly to un-hardcoded, resource-conserving constraints, this function contains **no hardcoded dimension constants** in its type parameters or logic. Instead, it reads the dimensions of incoming spatial arrays directly from dependent type indices, uses **Structural Accounting (`sumStructural`)** to measure background history mass, and uses a generic **Tensor Product Outer Product** to expand grid rows and columns dynamically into a pure **`Maxel`**.

---

## 🏛️ 1. Theoretical Architecture

```
                    THE CHIRAL OUTER PRODUCT HANDSHAKE
             chiralBra: [b1, b2, b3, b4]  (1 x N row vector)
          ┌─────────────────────────────────────────────────┐
   c  k₁  │  (k₁·b₁)    (k₁·b₂)    (k₁·b₃)    (k₁·b₄)       │
   h  k₂  │  (k₂·b₁)    (k₂·b₂)    (k₂·b₃)    (k₂·b₄)       │  => N x N Active Cells
   i  k₃  │  (k₃·b₁)    (k₃·b₂)    (k₃·b₃)    (k₃·b₄)       │
   r  k₄  │  (k₄·b₁)    (k₄·b₂)    (k₄·b₃)    (k₄·b₄)       │
   a      └─────────────────────────────────────────────────┘
   lKet (N x 1 column)

   Ancestral Anchor: (Pixel N N => historyMass)
   Active Manifold:  (Pixel 1 1 => gridWeight)
```

### A. The 4 Stages of Generalized Inflation
1. **QTT State Consumption**:
   Consumes `(1 priorState : UniverseState currentVM de dm)` under strict Quantitative Type Theory linearity.
2. **Structural Accounting of Background History**:
   Walks the Dark Matter vector array structurally via `sumStructural dmLog` (yielding mass 56 for Epoch 38).
3. **Chiral Outer Product Summation**:
   Multiplies the incoming chiral ket and bra vectors to calculate the aggregate matrix mass ($M = \sum_i \sum_j k_i b_j$).
4. **Macro Maxel Unfold**:
   Anchors historical mass at the outer boundary `(nextScale, nextScale)` while embedding active field tokens at `(1, 1)` in a unified `Maxel`.

---

## 💻 2. Executable Literate Proofs & Evidence

```idris
module Evolution.Dynamic_Grid_Expansion

import Core.BoxInt
import Core.VexelMaxel
import Evolution.State
import Evolution.StructuralAccounting
import Evolution.Expansion
import Data.Vect

%default total

||| Scenario: 38th Epoch universe at 3x3 macro-grid state (vm=9, de=128, dm=56)
public export
macroState3x3 : UniverseState 9 128 56
macroState3x3 = MkUniverseState (replicate 9 (intToBoxInt 0))
                                (replicate 128 (intToBoxInt 38))
                                (replicate 56 (intToBoxInt 1))

||| Chiral state vectors for next scale tick (Length = 4)
public export
ketVector4 : Vect 4 Int
ketVector4 = [1, 0, 1, 0]

public export
braVector4 : Vect 4 Int
braVector4 = [1, 1, 0, 1]

||| Evidence 1: Verification that the outer product sum equals exactly 6 mass units.
public export
evidence_outer_product_mass : Bool
evidence_outer_product_mass =
  let mass = computeOuterProductSum ketVector4 braVector4
  in mass == 6

||| Evidence 2: Verification that ancestral Dark Matter history (56) is anchored at (4, 4).
public export
evidence_ancestral_history_anchor : Bool
evidence_ancestral_history_anchor =
  let manifold = expandAndUnfoldGeneric macroState3x3 ketVector4 braVector4
  in unwrapBox (lookupPixel (MkPixel 4 4) manifold) == 56

||| Evidence 3: Verification that the active grid weight (6) is anchored at (1, 1).
public export
evidence_active_grid_weight : Bool
evidence_active_grid_weight =
  let manifold = expandAndUnfoldGeneric macroState3x3 ketVector4 braVector4
  in unwrapBox (lookupPixel (MkPixel 1 1) manifold) == 6

||| Evidence 4: Verification that total manifold weight equals sum of active grid (6) and history (56) = 62.
public export
evidence_total_manifold_weight : Bool
evidence_total_manifold_weight =
  let manifold = expandAndUnfoldGeneric macroState3x3 ketVector4 braVector4
  in unwrapBox (totalMaxelWeight manifold) == 62
```
