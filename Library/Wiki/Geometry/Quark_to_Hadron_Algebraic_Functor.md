# 🌌 The Quark-to-Hadron Algebraic Functor & Confinement Homomorphisms

This chapter formalizes the **Quark-to-Hadron Algebraic Functor**, demonstrating how fractional quark tokens ($(r, g, b)$ color cochains) compose constructively into color-neutral hadronic singlets (protons, neutrons, and mesons) via strict algebraic homomorphisms.

```idris
module Geometry.Quark_to_Hadron_Algebraic_Functor

import Core.BoxInt
import Core.Multiset
import Core.VexelMaxel
import Core.UnixelFraction
import Math.FourGeometries
import Math.PauliExclusion
import Compound.HadronicConfinement
import Compound.QuarkHadronAlgebra
import Reflect.InvariantAuditor

%default total
```

---

## 💡 1. The Algebraic Functor Architecture

Following **Algebra-Driven Design (ADD)** (*Sandy Maguire*):
1. **Quark Carrier Sort**: Each `QuarkToken` carries:
   - Flavor: $u, d, s, c, b, t \in \text{QuarkFlavor}$.
   - Fractional Electric Charge: $Q_u = +2/3 e$, $Q_d = -1/3 e$ as exact `UnixelFraction`.
   - Baryon Fraction: $B = 1/3$ (quarks) or $B = -1/3$ (antiquarks).
   - SU(3) Color Charge: $\text{Red}, \text{Green}, \text{Blue} \in \text{ColorCharge}$.
2. **Hadronic Combinator**: The algebraic functor `contractBaryonTriad` maps three quark tokens $(q_R, q_G, q_B)$ into a composite `Hadron`.
3. **Observation Homomorphisms**:
   - **Charge Homomorphism**: $\text{charge}(q_1 \otimes q_2 \otimes q_3) \equiv \text{charge}(q_1) + \text{charge}(q_2) + \text{charge}(q_3)$.
     - Proton $(uud)$: $\frac{2}{3} + \frac{2}{3} - \frac{1}{3} = \frac{3}{3} = +1 e$.
     - Neutron $(udd)$: $\frac{2}{3} - \frac{1}{3} - \frac{1}{3} = \frac{0}{3} = 0 e$.
   - **Baryon Number Homomorphism**: $B(q_1 \otimes q_2 \otimes q_3) \equiv \frac{1}{3} + \frac{1}{3} + \frac{1}{3} = 1$.
   - **Color Singlet Invariance**: Red $+$ Green $+$ Blue $=$ White Singlet ($\text{Tr}(F) = 0$).

---

## 📜 2. Formal Invariants & Verification

```idris
public export
proofOfQuarkHadronAlgebra : Bool
proofOfQuarkHadronAlgebra =
  auditQuarkHadronAlgebraProof
```

### Verified Algebraic Invariants:
1. **Proton Charge**: $Q(p) = +1 e$ ($3/3$).
2. **Neutron Charge**: $Q(n) = 0 e$ ($0/3$).
3. **Pion+ Meson Charge**: $Q(\pi^+) = +1 e$ ($3/3$), $B(\pi^+) = 0$.
4. **SU(3) Confinement**: All composite hadrons are color singlets.
