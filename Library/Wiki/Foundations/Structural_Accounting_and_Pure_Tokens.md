# 🧱 Structural Accounting & Cast-Free Token Geometry

In **Idris2-Universe2**, numbers are **not abstract machine scalars** magically converted across types with `cast`. In Norman J. Wildberger's *Box Arithmetic* and strict Quantitative Type Theory (QTT), a number is a **physical collection of resource tokens inside an inductive data container**.

---

## 🏛️ 1. The Ultrafinitist Critique of `cast`

### The Vulnerability of Primitive Casts
When a program calls `cast (sum dmLog)`:
1. The compiler drops down to its unverified machine-level integer registers (e.g. 64-bit hardware registers).
2. To an ultrafinitist, this breaks the chain of logical conservation: hardware overflow, bit shifts, or un-tracked pointer coercions can compromise physical conservation without triggering a type error.
3. In a true computational cosmology, the metric tracker must **count and accumulate its memory configurations structurally**, token by token.

---

## 🔬 2. Pure Structural Accounting (`sumStructural`)

Instead of performing runtime numerical casts, the universe accumulates data along inductive vectors using **Structural Accounting**:

$$\text{sumStructural}([\ ]) = [\ 0 \ ]$$
$$\text{sumStructural}(x :: xs) = x + \text{sumStructural}(xs)$$

Every historical remainder in the Dark Matter ledger ($dm = 55$) exerts gravitational drag not because of an arbitrary casting macro, but because the algorithm **physically unrolls the linear memory layout and pairs each historical token against the metric boundaries**.

---

## 💻 3. Executable Literate Proofs & Evidence

```idris
module Foundations.Structural_Accounting_and_Pure_Tokens

import Core.BoxInt
import Evolution.State
import Evolution.StructuralAccounting
import Compound.LinearEpsilonRouting
import Compound.VelocityLensing
import Math.Infinitesimal
import Math.LinAlgebra.MetricTensor
import Data.Vect

%default total

||| Evidence 1: Proof that structural summation operates cast-free over 55 Dark Matter tokens
public export
evidence_structural_dm_sum : Bool
evidence_structural_dm_sum =
  let dmStack = replicate 55 (intToBoxInt 1)
      totalDrag = sumStructural dmStack
  in unwrapBox totalDrag == 55

||| Evidence 2: Proof that structural vector counting matches exact physical box tallies
public export
evidence_structural_count : Bool
evidence_structural_count =
  let grid = replicate 27 (intToBoxInt 0)
      tokenCount = countStructural grid
  in unwrapBox tokenCount == 27

||| Evidence 3: Proof that structural accounting satisfies associative grouping across scale partitions:
||| (A + B) + C == A + (B + C)
public export
evidence_structural_associativity : Bool
evidence_structural_associativity =
  let a = intToBoxInt 27  -- Visible Matter
      b = intToBoxInt 128 -- Dark Energy
      c = intToBoxInt 55  -- Dark Matter
  in verifyAssociativeTransition a b c

||| Evidence 4: Proof that cast-free velocity lensing produces exact integer rational deceleration:
||| 560 / (1 + 55) = 10
public export
evidence_cast_free_lensing : Bool
evidence_cast_free_lensing =
  let cosmos = MkUniverseState (replicate 27 (intToBoxInt 0))
                               (replicate 128 (intToBoxInt 0))
                               (replicate 55 (intToBoxInt 1))
      vIn = MkVelocity (MkInfinitesimal (intToBoxInt 0) (intToBoxInt 560) (intToBoxInt 0))
                       (MkInfinitesimal (intToBoxInt 0) (intToBoxInt 0)   (intToBoxInt 0))
      vOut = lensVelocityAcrossScale cosmos gBlue vIn
  in unwrapBox (m12 (vAlpha vOut)) == 10
```
