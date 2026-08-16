# Law 4: Topological First Chern Number & Quantized Hall Conductance

## 1. Physical Principle & Constructive Foundation
In continuous condensed matter physics, the integer quantum Hall effect is described by integrating the Berry curvature over a continuous Brillouin zone 2-torus $T^2$.

On the discrete 3-torus, the momentum lattice is a finite multiset of $N \times N$ discrete plaquettes $P = \{ p_{j,k} \}$.
Each plaquette $p$ carries a discrete Berry flux $F_{xy}(p)$.

---

## 2. Integer Quantization via Telescoping Boundary Cancellation
When summing the discrete Berry curvature over the closed 2-torus, all interior link variables cancel pairwise:
$$C_1 = \frac{1}{2\pi} \sum_{p \in P} F_{xy}(p) \in \mathbb{Z}$$

Because internal links cancel identically, the First Chern Number $C_1$ is strictly quantized to exact integers ($C_1 \in \{0, 1, 2, \dots\}$), guaranteeing complete topological immunity against continuous metric deformations:
$$\frac{\partial C_1}{\partial g_{ij}} = 0$$

Transversal Hall conductance across the 2D Maxel lattice is locked to this topological invariant:
$$\sigma_{xy} = C_1 \cdot \frac{e^2}{h}$$
