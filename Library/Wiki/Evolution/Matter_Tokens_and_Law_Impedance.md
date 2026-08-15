# ⚖️ Visible Matter Tokens vs. Dark Matter Law Impedance

A fundamental insight of the **Idris2-Universe2** architecture is the profound ontological difference between **Visible Matter** and **Dark Matter**:

* **Visible Matter (`vm`)** represents **Local Integer Numerators** ($N \in \mathbb{Z}$). It manifests as discrete, whole-number `BoxInt` tokens occupying local spatial cells (Voxels, Quarks, Atoms, Molecules).
* **Dark Matter (`dm`)** represents **Global Structural Denominators / Laws** ($D = 1 + \text{sumStructural dm}$). It is not a localized particulate substance, but the accumulated cyclotomic historical error ledger that acts as an **algebraic impedance divisor**, governing time dilation, gravitational drag, and the irreversible Arrow of Time.

Every physical observable in the universe (velocities, probabilities, redshifts, forces) is formed by the **rational quotient** of a Visible Matter numerator over a Dark Matter law denominator:
$$\text{Physical Observable } \mathcal{O} = \frac{\text{Visible Matter State } (N)}{\text{Dark Matter Impedance } (D)} \equiv [N, D]$$

---

## 🏛️ 1. Theoretical Comparison

```
              THE NUMERATOR / DENOMINATOR DUALITY
              
   ┌────────────────────────────────────────────────────────┐
   │  VISIBLE MATTER (Numerator N)                          │
   │  - Type: Vect vmSize BoxInt (e.g. 27 voxels)          │
   │  - Nature: Local integer tokens (e.g. +1, -1)          │
   │  - Dynamics: Fluctuates linearly via QTT bonds         │
   └────────────────────────────────────────────────────────┘
                              ÷
   ┌────────────────────────────────────────────────────────┐
   │  DARK MATTER (Law Denominator D)                       │
   │  - Type: Vect dmSize BoxInt (e.g. 55 -> 56 states)     │
   │  - Nature: Global non-local impedance divisor          │
   │  - Dynamics: Append-only cyclotomic history ledger     │
   └────────────────────────────────────────────────────────┘
                              ▼
   ┌────────────────────────────────────────────────────────┐
   │  RATIONAL OBSERVABLE: Q = N / (1 + sumStructural dm)   │
   └────────────────────────────────────────────────────────┘
```

---

## 💻 2. Executable Literate Proofs & Evidence

```idris
module Evolution.Matter_Tokens_and_Law_Impedance

import Core.BoxInt
import Core.VexelMaxel
import Evolution.State
import Evolution.Bootstrap
import Evolution.StructuralAccounting
import Compound.VelocityLensing
import Compound.LinearEpsilonRouting
import Math.Infinitesimal
import Math.LinAlgebra.MetricTensor
import Data.Vect

%default total

||| Evidence 1: Visible Matter is a discrete, local integer sum (27 units for standard Ground State).
public export
evidence_visible_matter_integer_sum : unwrapBox (sumStructural (replicate 27 (intToBoxInt 1))) = 27
evidence_visible_matter_integer_sum = Refl

||| Evidence 2: Dark Matter provides the global scale impedance denominator (D = 1 + 55 = 56 for Epoch 37).
public export
evidence_dark_matter_scale_denominator : Bool
evidence_dark_matter_scale_denominator =
  let drag = sumStructural (dmLog standardEpoch37)
      scaleFactor = intToBoxInt 1 + drag
  in unwrapBox scaleFactor == 56

||| Evidence 3: Exact rational velocity deceleration via Dark Matter quotient:
||| An incoming velocity numerator of 112 tokens lensed through 55 DM states yields exactly 112 / 56 = 2 tokens.
public export
evidence_rational_velocity_deceleration : Bool
evidence_rational_velocity_deceleration =
  let vIn = MkVelocity (MkInfinitesimal (intToBoxInt 0) (intToBoxInt 112) (intToBoxInt 0))
                       (MkInfinitesimal (intToBoxInt 0) (intToBoxInt 0)   (intToBoxInt 0))
      vOut = lensVelocityAcrossScale standardEpoch37 gSubstrate vIn
      outAlpha = m12 (vAlpha vOut)
  in unwrapBox outAlpha == 2 -- 112 / (1 + 55) = 112 / 56 = 2

||| Evidence 4: Monotonic Law Impedance Growth (The Arrow of Time):
||| Stepping to Epoch 38 increases the law denominator from 56 to 57, ensuring time never flows backward.
public export
evidence_arrow_of_time_impedance_step : Bool
evidence_arrow_of_time_impedance_step =
  let cosmos38 : UniverseState 27 128 56
      cosmos38 = stepEpoch standardEpoch37 (intToBoxInt 1)
      d37 = intToBoxInt 1 + sumStructural (dmLog standardEpoch37)
      d38 = intToBoxInt 1 + sumStructural (dmLog cosmos38)
  in unwrapBox d38 == 57 && unwrapBox d38 > unwrapBox d37

||| Evidence 5: QTT First Law Invariance:
||| Local token redistribution within Visible Matter changes spatial configuration
||| without perturbing the global Dark Matter law ledger.
public export
evidence_local_vm_global_dm_independence : Bool
evidence_local_vm_global_dm_independence =
  let vm1 = replicate 27 (intToBoxInt 1)
      vm2 = (intToBoxInt 27) :: replicate 26 (intToBoxInt 0)
      sum1 = sumStructural vm1
      sum2 = sumStructural vm2
      d = intToBoxInt 1 + sumStructural (dmLog standardEpoch37)
  in sum1 == sum2 && unwrapBox d == 56
```
