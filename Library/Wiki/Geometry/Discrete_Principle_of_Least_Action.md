# ⚡ The Discrete Principle of Least Action & Asymmetric Euler-Lagrange Dynamics

In **Epoch 37**, classical mechanics and geodesic motion emerge without continuous limits or infinitesimal calculus through the **Discrete Principle of Least Action** across the **4 Fundamental Geometries** (Elliptic, Hyperbolic, Parabolic, Substrate).

---

## 🏛️ 1. Theoretical Framework

```
                 THE DISCRETE VARIATIONAL LATTICE
  ┌─────────────────────────────────────────────────────────────────┐
  │ 1. Discrete Trajectory: γ = [x₀, x₁, x₂, ..., x_N]              │
  │    Ordered sequence of spatial box coordinates on the 3-torus   │
  │                               │                                 │
  │                               ▼                                 │
  │ 2. Discrete Lagrangian:                                         │
  │    L(x_k, x_{k+1}) = 1/2 Q_g(x_{k+1} - x_k) - V(x_k)            │
  │                               │                                 │
  │                               ▼                                 │
  │ 3. Discrete Euler-Lagrange Equation:                            │
  │    g · (x_{k+1} - 2x_k + x_{k-1}) = -∇V(x_k)  (Discrete F = ma) │
  │                               │                                 │
  │                               ▼                                 │
  │ 4. Substrate Action Asymmetry:                                  │
  │    S[forward] ≠ S[reverse] (Arrow of Time in Action)            │
  └─────────────────────────────────────────────────────────────────┘
```

### A. Discrete Variation & Newtonian Acceleration
Rather than taking continuous time derivatives $\frac{d}{dt}$, a trajectory on the discrete lattice $\gamma = (x_0, x_1, \dots, x_N)$ has discrete action:
$$S[\gamma] = \sum_{k=0}^{N-1} L(x_k, x_{k+1}) = \sum_{k=0}^{N-1} \left( \frac{1}{2} Q_g(x_{k+1} - x_k) - V(x_k) \right)$$

Extremizing $S[\gamma]$ with respect to intermediate lattice positions $x_k$ yields the **Discrete Euler-Lagrange (DEL) Equation**:
$$g \cdot (x_{k+1} - 2 x_k + x_{k-1}) = -\nabla V(x_k)$$
where $\Delta^2 x = x_{k+1} - 2 x_k + x_{k-1}$ is the exact second-order discrete acceleration, recovering **Newton's Second Law ($F = m a$)** on the lattice!

### B. Geodesic Least Action Optimality
For a free particle ($V=0$), the straight discrete worldline $\gamma_{\text{straight}} = [(0,0), (1,1), (2,2)]$ has action $S = 4$, whereas any deflected path $\gamma_{\text{perturbed}} = [(0,0), (0,2), (2,2)]$ has action $S = 8$. Thus:
$$S[\gamma_{\text{straight}}] < S[\gamma_{\text{perturbed}}]$$
confirming that free tokens strictly follow geodesic paths of least multiset information distance.

### C. The Causal Arrow of Time in Hamilton's Principle
Under the **Substrate metric** ($g_{22} = 0, g_{12} = 1$), time-reversal symmetry is spontaneously broken at the Lagrangian level:
$$S[(0,0) \to (1,2)] = 5 \quad \neq \quad 3 = S[(1,2) \to (0,0)]$$
yielding an irreversible action deficit $\Delta S = 2$, embedding the **Cosmological Arrow of Time** directly into the Action Principle.

---

## 💻 2. Executable Literate Code & Verification

```idris
module Geometry.Discrete_Principle_of_Least_Action

import Core.BoxInt
import Core.VexelMaxel
import Math.DiscreteActionPrinciple

%default total

||| Verifies that the Discrete Euler-Lagrange equation produces zero residual for uniform motion.
public export
verifyDiscreteEulerLagrangeEquivalence : Bool
verifyDiscreteEulerLagrangeEquivalence =
  auditDiscreteEulerLagrangeEquivalenceProof

||| Verifies that the Substrate metric creates an irreversible action deficit.
public export
verifySubstrateActionAsymmetry : Bool
verifySubstrateActionAsymmetry =
  auditSubstrateActionAsymmetryProof

||| Verifies that straight geodesic paths strictly minimize discrete Action.
public export
verifyGeodesicLeastActionOptimality : Bool
verifyGeodesicLeastActionOptimality =
  auditGeodesicLeastActionOptimalityProof
```
