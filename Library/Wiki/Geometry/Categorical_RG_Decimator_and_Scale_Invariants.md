# Categorical RG Decimator & Scale-Invariant Fixed Points

## 1. Physical Principle & Constructive Foundation
In continuous quantum field theory, Wilsonian renormalization relies on integrating out high-momentum degrees of freedom. In **Idris2-Universe2**, multi-scale lattice coarse-graining is formulated constructively through the `RGDecimator micro macro` interface:
1. **Categorical Decimation Projection**:
   $$\Pi: \text{Plaquette}_{2\times 2} \longrightarrow \text{MacroPlaquette}$$
   $$\text{MacroFlux} = f_{00} + f_{01} + f_{10} + f_{11}$$
2. **Topological Fixed-Point Preservation**:
   $$\mathcal{R}(C_1) = \sum_{i} \text{MacroPlaquette}_i \equiv C_1$$
   The First Chern Number and Wilson loop holonomies are strict topological fixed points under recursive block decimation.

---

## 2. Geometric Metric Partition
- **Elliptic Sector ($\det g = +1$, $27$ VM)**: Microscopic $2\times 2$ plaquettes hosting localized Berry curvatures.
- **Hyperbolic Sector ($\det g = -1$, $128$ DE)**: Geodesic scale transitions connecting micro and macro levels.
- **Parabolic Sector ($\det g = 0$, $55$ DM)**: Multi-scale history tracking coarse-grained information loss.
- **Substrate Causal Arrow ($g_{22} = 0, g_{12} = 1$)**: Directs the unidirectional RG flow from UV to IR.
