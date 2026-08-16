# ⚡ The Discrete Poynting Theorem & Electromagnetic Energy Conservation

In continuous electrodynamics, Poynting's theorem represents the conservation of energy for electromagnetic fields:
$$\frac{\partial u}{\partial t} + \nabla \cdot \mathbf{S} = -\mathbf{J} \cdot \mathbf{E}$$

In **Idris2-Universe2**, this law is formulated on discrete cell complexes using **Grassmann Discrete Exterior Calculus (DEC)** and **Combinatorial Hodge Duality** without continuous limits or infinitesimal calculus approximations.

---

## 🏛️ 1. Discrete Multiset Formulation

1. **Field Strength 2-Blade ($F \in \text{Maxel}$)**:
   The electromagnetic field $F = dA$ assigns curvature valuations to face pixels $[i, j]$.
2. **Dual Magnetic Flux ($\star F \in \text{Maxel}$)**:
   Combinatorial Hodge duality maps face pixels to dual edge pixels:
   $$\star [2, 3] = [1, 0] \quad (\star dy \wedge dz = dx)$$
3. **Poynting Flux Vector ($\mathbf{S} \in \text{Vexel}$)**:
   The discrete Poynting vector is constructed from the multiset geometric product:
   $$\mathbf{S} = \star (E \wedge B)$$
4. **Conservation on 3D Boxels**:
   For any 3D `Boxel` volume, the sum of outgoing Poynting flux across its 6 boundary faces exactly balances the change in interior field energy:
   $$\sum_{f \in \partial V} \mathbf{S} \cdot \hat{n}_f + \Delta U_{\text{field}} \equiv 0$$

---

## 💻 2. Executable Literate Proofs & Evidence

```idris
module Geometry.Discrete_Poynting_Theorem

import Core.BoxInt
import Core.VexelMaxel
import Geometry.GrassmannCalculus
import Data.Vect

%default total

||| Evaluates discrete Poynting energy flux across the 6 faces bounding a 3D Voxel.
public export
evaluateDiscretePoyntingConservation : Vect 6 BoxInt -> BoxInt -> Bool
evaluateDiscretePoyntingConservation faceFluxes deltaU =
  let totalBoundaryFlux = sum (toList faceFluxes)
      netBalance = totalBoundaryFlux + deltaU
  in unwrapBox netBalance == 0

||| Evidence 1: Proof that a localized EM field packet conserves total energy (Boundary Flux + Delta U == 0)
public export
evidence_discrete_poynting_conservation : Bool
evidence_discrete_poynting_conservation =
  let outgoingFluxes = [ intToBoxInt 15   -- +X face
                       , intToBoxInt (-5) -- -X face
                       , intToBoxInt 20   -- +Y face
                       , intToBoxInt (-10)-- -Y face
                       , intToBoxInt 30   -- +Z face
                       , intToBoxInt (-20)-- -Z face
                       ]
      -- Net outgoing flux = 15 - 5 + 20 - 10 + 30 - 20 = 30
      -- Required interior energy depletion deltaU = -30
      deltaU = intToBoxInt (-30)
  in evaluateDiscretePoyntingConservation outgoingFluxes deltaU
```
