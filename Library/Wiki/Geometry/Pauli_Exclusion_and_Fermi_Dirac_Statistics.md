# Law 9: The Pauli Exclusion Principle & Fermi-Dirac Statistics

## 1. Physical Principle & Constructive Foundation
In quantum mechanics, fermions (spin-$1/2$ particles like electrons, quarks, and neutrinos) obey the **Pauli Exclusion Principle**: no two identical fermions can occupy the same quantum state simultaneously.

In **Idris2-Universe2**, this principle emerges directly from **Grassmann Blade Nilpotency** in Exterior Multiset Algebra:
1. **Grassmann Blade Nilpotency**:
   $$v \wedge v \equiv 0$$
   An attempt to create a two-particle wedge state from identical basis singletons collapses the multiset amplitude to zero ($0$).
2. **Strict Fermionic Binary Occupancy**:
   $$n_k \in \{0, 1\}$$
   Each discrete spatial cell mode is either `Vacant` ($0$) or `Occupied` ($1$).
3. **Discrete Fermi-Dirac Distribution**:
   $$n(E) = \frac{1}{1 + \text{drag}}$$
   At zero temperature ($T=0$), this yields a sharp step function at the Fermi level $E_F$:
   $$n(E) = \begin{cases} 1 & \text{if } E \le E_F \\ 0 & \text{if } E > E_F \end{cases}$$

---

## 2. Geometric Metric Partition
- **Elliptic Sector ($\det g = +1$, $27$ VM)**: Bound atomic shell occupancies and valence electron configurations ($n_k \le 1$).
- **Hyperbolic Sector ($\det g = -1$, $128$ DE)**: Relativistic momentum exchange maintaining degeneracy pressure across the Fermi sea.
- **Parabolic Sector ($\det g = 0$, $55$ DM)**: Quantum dissipation drain receiving thermalized excitation remnants.
- **Substrate Causal Arrow ($g_{22} = 0, g_{12} = 1$)**: Enforces unidirectional state transitions preventing unphysical anti-particle pair loops.
