# 🌌 Causal Posets & Inductive Dark Matter Lensing

In **Idris2-Universe2**, velocity routing across scale jumps is lensed and retarded by the Dark Matter residue.

---

## 💻 1. Executable Literate Proofs & Evidence

```idris
module Kinematics.Causal_Posets_and_Lensing

import Core.BoxInt
import Evolution.State
import Evolution.Bootstrap
import Math.LinAlgebra.MetricTensor
import Math.Infinitesimal
import Compound.LinearEpsilonRouting
import Compound.VelocityLensing
import Data.Vect

%default total

||| Evaluates lensing of velocity across an accumulated 55-unit Dark Matter drag ledger.
public export
testLensingVelocity : Integer
testLensingVelocity =
  let state = MkUniverseState {vmSize=0} {deSize=0} {dmSize=1} [] [] [intToBoxInt 55]
      vIn = MkVelocity (MkInfinitesimal (intToBoxInt 0) (intToBoxInt 560) (intToBoxInt 0))
                       (MkInfinitesimal (intToBoxInt 0) (intToBoxInt 0)   (intToBoxInt 0))
      vOut = lensVelocityAcrossScale state Math.LinAlgebra.MetricTensor.gBlue vIn
  in unwrapBox (m12 (vAlpha vOut))

||| Evidence 1: Proof that lensing velocity across the 55-state Dark Matter drag scales velocity by (1 + 55 = 56) (560 / 56 = 10)
public export
evidence_lensing_drag_scale : Bool
evidence_lensing_drag_scale =
  Kinematics.Causal_Posets_and_Lensing.testLensingVelocity == 10
```
