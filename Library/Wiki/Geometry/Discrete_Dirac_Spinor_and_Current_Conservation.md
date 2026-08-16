# Law 8: The Discrete Dirac Spinor Equation & Conserved 4-Current

## 1. Physical Principle & Constructive Foundation
In continuous relativistic quantum mechanics, the Dirac equation describes spin-$1/2$ fermions:
$$(i \gamma^\mu \partial_\mu - m)\psi = 0$$
where $\gamma^\mu$ are $4 \times 4$ complex Dirac matrices satisfying the Clifford anticommutation relation $\{\gamma^\mu, \gamma^\nu\} = 2 g^{\mu\nu}$.

In **Idris2-Universe2**, the Dirac spinor is formulated constructively without continuous limits or imaginary numbers:
1. **Discrete Bispinor State (`DiracSpinor4`)**: A 4-tuple of signed Pixel difference pairs $[P_k, N_k]$ ($k \in \{1, 2, 3, 4\}$).
2. **Probability & Charge Density ($j^0$)**:
   $$j^0 = \sum_{k=1}^4 (P_k - N_k)^2 \ge 0$$
   Guarantees strict non-negativity and positive Born probabilities.
3. **Conserved 4-Current ($j^\mu$)**:
   $$\sum_{\mu=0}^3 \nabla_\mu j^\mu \equiv 0$$
4. **Discrete Chiral Projectors ($P_L, P_R$)**:
   $$P_L = \frac{1 - \gamma^5}{2}, \quad P_R = \frac{1 + \gamma^5}{2}$$
   Satisfying exact algebraic idempotency ($P_L^2 = P_L, P_R^2 = P_R$) and completeness ($P_L + P_R = 1$).

---

## 2. Geometric Metric Partition
- **Elliptic Sector ($\det g = +1$, $27$ VM)**: Active spatial components of the Dirac probability density.
- **Hyperbolic Sector ($\det g = -1$, $128$ DE)**: Relativistic boost and chiral rotations within the Clifford multivector rotor algebra.
- **Parabolic Sector ($\det g = 0$, $55$ DM)**: Null-momentum projection ensuring zero mass-loss during relativistic propagation.
- **Substrate Causal Arrow ($g_{22} = 0, g_{12} = 1$)**: Enforces unidirectional forward-time fermion propagation, breaking $CPT$ time-inversion loops.
