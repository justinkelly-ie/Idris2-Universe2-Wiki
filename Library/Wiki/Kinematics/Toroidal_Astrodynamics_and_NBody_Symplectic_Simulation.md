# 3D Toroidal Astrodynamics & Symplectic N-Body Simulation

## 1. Physical Principle & Constructive Foundation
In a finite, boundaryless 3-torus universe ($T^3 = \mathbb{Z}^3 / (L \mathbb{Z}^3)$), gravitational attraction obeys periodic minimum image geometry without edge singularities:
1. **Minimum Image Toroidal Metric**:
   $$\Delta x = ((x_1 - x_2 + L/2) \pmod L) - L/2$$
   $$Q(\Delta \vec{q}) = \Delta x^2 + \Delta y^2 + \Delta z^2$$
2. **Softened Gravitational Force with Cyclotomic Drag Divisor**:
   $$F_{ij} = \frac{G \cdot m_i \cdot m_j \cdot \Delta \vec{q}_{ij}}{(Q(\Delta \vec{q}_{ij}) + \epsilon^2) \cdot (1 + \text{drag})}$$
   The denominator factor $(1 + \text{drag})$ encodes the accumulated Dark Matter law impedance, directly giving rise to relativistic perihelion orbital precession on discrete integer lattices.
3. **Symplectic Momentum Conservation**:
   $$\sum_{i} \vec{F}_i \equiv \vec{0} \implies \sum_{i} \vec{p}_i(t) = \text{const}$$

---

## 2. Geometric Metric Partition
- **Elliptic Sector ($\det g = +1$, $27$ VM)**: Bound mass tokens orbiting in stable Keplerian trajectories.
- **Hyperbolic Sector ($\det g = -1$, $128$ DE)**: Periodic gauge flux propagating across the 3-torus fundamental domain.
- **Parabolic Sector ($\det g = 0$, $55$ DM)**: The cyclotomic law ledger $(1 + \text{drag})$ exerting kinematic resistance and driving orbital precession.
- **Substrate Causal Arrow ($g_{22} = 0, g_{12} = 1$)**: Enforces the irreversible time direction for symplectic step updates.
