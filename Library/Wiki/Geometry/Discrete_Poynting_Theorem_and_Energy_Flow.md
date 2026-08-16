# Law 7: The Discrete Poynting Theorem & Electromagnetic Energy Flux

## 1. Physical Principle & Constructive Foundation
In classical continuum electrodynamics, Poynting's theorem governs local conservation of electromagnetic energy:
$$\nabla \cdot \vec{S} + \frac{\partial u}{\partial t} = -\vec{J} \cdot \vec{E}$$
where $u = \frac{1}{2}(\epsilon_0 E^2 + \frac{1}{\mu_0} B^2)$ is electromagnetic energy density, $\vec{S} = \frac{1}{\mu_0} \vec{E} \times \vec{B}$ is the Poynting energy flux density vector, and $\vec{J} \cdot \vec{E}$ is the rate of work done by electromagnetic fields on electric currents.

In **Idris2-Universe2**, this law is formulated on the discrete 27-cell 3-torus ($T^3$) using Discrete Exterior Calculus (DEC):
1. **Discrete Energy Density ($u$)**: A 0-cochain (voxel volume density) evaluating total squared field quadrance:
   $$u = E^2 + B^2$$
2. **Poynting Flux 1-Form ($S$)**: A discrete 1-cochain along cell boundary edges:
   $$S = \star(E \wedge B)$$
3. **Discrete Divergence ($\delta S$)**: Evaluates net outward energy flux across cell faces.
4. **Joule Work ($J \cdot E$)**: Discrete contraction between 1-form current density $J$ and electric field $E$.

---

## 2. Discrete Poynting Energy Balance
For each discrete spatial cell over time step $\Delta t = 1$:
$$\Delta u + \delta S + (J \cdot E) = 0 \implies u(t+1) = u(t) - \delta S - (J \cdot E)$$

---

## 3. Global Toroidal Conservation
Because the 3-torus $T^3$ is compact and boundaryless ($\partial T^3 = \emptyset$):
$$\sum_{v \in T^3} \delta S(v) \equiv 0$$
In the vacuum absence of electric currents ($\vec{J} = 0$), the total electromagnetic field energy across all 27 cells is strictly constant:
$$\sum_{v=0}^{26} u(t+1) \equiv \sum_{v=0}^{26} u(t)$$

---

## 4. Geometric Metric Partition
- **Hyperbolic Sector ($\det g = -1$, $128$ DE)**: Propagating electromagnetic gauge flux and cross-product rotors $E \wedge B$.
- **Elliptic Sector ($\det g = +1$, $27$ VM)**: Active spatial vertices hosting charge density $\rho$ and current $J$.
- **Parabolic Sector ($\det g = 0$, $55$ DM)**: Remainder dissipation drain receiving ohmic losses $J \cdot E$ without kinetic feedback.
