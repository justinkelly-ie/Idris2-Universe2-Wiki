# Law 15: Discrete Jarzynski Equality & Non-Equilibrium Work Relations

## 1. Physical Principle & Constructive Foundation
In non-equilibrium statistical mechanics, Jarzynski's equality connects the distribution of non-equilibrium work $W$ performed along arbitrary dynamical trajectories to the equilibrium Helmholtz free energy change $\Delta F$:

1. **Non-Equilibrium Trajectory Work & Dissipation**:
   For any cyclic or non-equilibrium protocol, dissipated work is defined as:
   $$W_{\text{diss}, i} = W_i - \Delta F$$
   By the Second Law of Thermodynamics, the ensemble average satisfies:
   $$\langle W_{\text{diss}} \rangle = \langle W \rangle - \Delta F \ge 0$$
2. **The Discrete Jarzynski Identity**:
   $$\langle e^{-\beta W} \rangle = e^{-\beta \Delta F} \iff \langle e^{-\beta (W - \Delta F)} \rangle = 1$$
   Formally proven in normalized discrete multiset probability spaces.
3. **Fluctuation-Dissipation Relation**:
   In the near-equilibrium linear response regime:
   $$\langle W_{\text{diss}} \rangle = \frac{1}{2} \beta \sigma_W^2$$
   Directly linking energy dissipation to the statistical variance of trajectory fluctuations $\sigma_W^2$.

---

## 2. Geometric Metric Partition
- **Elliptic Sector ($\det g = +1$, $27$ VM)**: Bound-state internal energy $U$ and mechanical work input.
- **Hyperbolic Sector ($\det g = -1$, $128$ DE)**: Geodesic trajectory paths in state configuration space.
- **Parabolic Sector ($\det g = 0$, $55$ DM)**: The entropy sink absorbing dissipated work $\langle W_{\text{diss}} \rangle$.
- **Substrate Causal Arrow ($g_{22} = 0, g_{12} = 1$)**: Enforces the thermodynamic arrow of time ensuring $\langle W_{\text{diss}} \rangle \ge 0$ monotonically.
