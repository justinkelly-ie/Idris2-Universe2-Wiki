# 📚 Idris2-Universe2-Wiki

**Literate Documentation, Formal Specifications, and Property Verification Suite for [Idris2-Universe2](https://github.com/justinkelly-ie/Idris2-Universe2).**

[![Idris2](https://img.shields.io/badge/Idris2-Verified_Wiki-blue.svg)](https://github.com/idris-lang/Idris2)
[![Epochs](https://img.shields.io/badge/Epochs-1_to_37-green.svg)]()
[![Ternary](https://img.shields.io/badge/Ternary_States-27_Closed-purple.svg)]()
[![Modules](https://img.shields.io/badge/Literate_Chapters-35_Verified-brightgreen.svg)]()
[![Tests](https://img.shields.io/badge/Test_Suite-29_Passed-success.svg)]()

---

## 🗺️ The Universal Rosetta Stone: Finite Math, Physics & Programming

The cornerstone of **Idris2-Universe2** is the strict mathematical isomorphism linking **Constructive Finitist Mathematics**, **Fundamental Physics**, and **Type-Theoretic Programming (Idris 2 QTT)**:

| Category | 📐 Finite / Rational Mathematics | 🌌 Cosmological Physics | 💻 Programming (Idris 2 / QTT) |
| :--- | :--- | :--- | :--- |
| **Number Genesis** | **Box Arithmetic**<br>Empty multisets: $[\ ] = 0, [[\ ]] = 1, \dots$ | **Pre-Geometric Void & Genesis**<br>Matter emergence from absolute zero state | **Inductive Data Types**<br>`data WildNat = EmptyBox \| NestBox WildNat` |
| **Signed Quantities** | **Pixel Difference Pairs**<br>Equivalence pairs $(P, N) \in \mathbb{N} \times \mathbb{N}$ as **Pixels** $[P, N]$ | **Matter / Antimatter Asymmetry**<br>Flux cancellation and charge neutrality | **Pixel Isomorphism & BoxInt**<br>`record Pixel where [pos, neg]`, `record BoxInt` |
| **Conservation Laws** | **Exact Integer Arithmetic**<br>Zero fractional or continuous leakage | **First Law of Thermodynamics**<br>Energy, momentum, and charge conservation ($\nabla \cdot \vec{J} = 0$) | **Quantitative Type Theory (QTT)**<br>Linear resource tracking `(1 x : BoxInt)` |
| **Spacetime Coordinates** | **Balanced Ternary Ring & Voxels**<br>$\mathbb{Z}_3 = \{-1, 0, +1\}$ with coordinate **Voxels** $[x, y, z]$ | **3D Discrete Spacetime**<br>3 spatial axes forming the 27-voxel lattice | **Coordinate Voxels & Bits**<br>`data TernaryBit`, `record Voxel [x,y,z]` |
| **Global Topology** | **Toroidal Neighborhood Graph**<br>Periodic boundary 3-torus $T^3 \equiv \mathbb{Z}_3^3$ | **Boundaryless Compact Space**<br>Eliminates edge-leakage ($\partial M = \emptyset$) | **Modulo Indexing & Vectors**<br>`shiftTernaryForward`, `Vect 27 BoxInt` |
| **Quantum Phase & Limits**| **Nilpotent Dual Numbers**<br>Matrix unit $\epsilon = \begin{pmatrix} 0 & 1 \\ 0 & 0 \end{pmatrix}, \ \epsilon^2 = 0$ | **Quantum Calculus & Symplectic Phase**<br>Exact first derivatives without infinite limits ($\mathbb{R}$) | **Dual Number Records & Pixels**<br>`record DualComplex where constructor (r, eps)` |
| **Curvature & Metrics** | **Maxel Metric Classification**<br>27 symmetric Maxels (Elliptic, Hyperbolic, Parabolic) | **General Relativity & Light Cones**<br>Relational spacetime metric from matter/energy ratios | **Maxels & Determinant Functions**<br>`record Maxel`, `detMetric`, `classifyTernaryMetric` |
| **Electrodynamics & Gauge**| **Grassmann Coboundary Calculus**<br>0-, 1-, 2-, 3-Blade cochains, coboundaries $d_0, d_1, d_2$, Hodge dual $\star$ | **Maxwell's Equations & Yang-Mills Gauge**<br>Bianchi identity ($d_2(d_1 A) = 0$) and Dihedron color confinement | **Grassmann Cochains as Multisets**<br>`Vexel` (0-form), `Maxel` (1,2-form), `Boxel` (3-form) |
| **Strong Force / QCD** | **Triadic Partitioning & Quark Vexels**<br>3 orthogonal $Z$-slices ($3 \times 9 = 27$) over color Singletons | **$SU(3)$ Color Confinement**<br>Red, Green, Blue balance in color-neutral hadrons | **Hadron Boxels & Color Enums**<br>`seedHadronBoxel`, `ColorCharge` |
| **Atomic Clustering** | **Hierarchical Spatial Embedding**<br>$4 \times 27 = 108$ voxels (Tetrahedral Boxel) | **Nuclear Physics (Alpha Particle)**<br>4-nucleon composite $^4\text{He}$ atomic core | **108-Voxel Alpha Core Boxel**<br>`alphaCoreBoxel : Boxel` |
| **Time & Entropy** | **Monomial Goh Factorization**<br>Division by 137th Cyclotomic Polynomial $\Phi_{137}(x)$ | **Arrow of Time & 2nd Law**<br>Monotonic entropy growth and temporal shear ($g_{22} = 0$) | **Append-Only Immutable Lists**<br>`updatedDM = remainder :: dmLogData` ($dm \to S\ dm$) |
| **Gravitational Inertia** | **Scale Impedance Ratio & Structural Sums**<br>Quotient scaling $\frac{1}{1 + \text{sumStructural } \text{dmLog}}$ | **Gravitational Lensing & Mass**<br>Scale-dependent velocity deceleration by Dark Matter | **Linear Vexel & Maxel Actions**<br>`lensVelocityAcrossScale` |
| **Cosmic Evolution** | **Primorial Budget Sequences**<br>Primorial partitions: $210 = 27 + 128 + 55$ | **Cosmological Epochs**<br>Vacuum expansion from Epoch 1 to Ground State Epoch 37 | **Dependent State Records**<br>`record UniverseState (vm : Nat) (de : Nat) (dm : Nat)` |
| **Metatheory & Validation**| **Constructive Proof Witnesses**<br>Curry-Howard isomorphism ($A \cong \text{Type}$) | **Physical Law Invariance**<br>Non-negotiable compile-time consistency of reality | **Elaborator Reflection Macros**<br>`%macro`, `Reflect.InvariantAuditor`, `Refl` |

---

## 🧭 Master Table of Contents

### 1. Foundational Mathematics & Discrete Calculus
* [Universal Mapping & Notation](Library/Wiki/Foundations/Universal_Mapping.md) — Grounding modern physics in constructivist discrete math.
* [Box Arithmetic & Type Theory](Library/Wiki/Foundations/Box_Arithmetic.md) — Multiplicities, erase levels, and Quantitative Type Theory.
* [Pure Box Integers as Pixel Difference Pairs](Library/Wiki/Foundations/Pixel_Box_Integers.md) — Constructing $\mathbb{Z}$ from equivalence classes of positive and negative multisets (Pixels $[P, N]$).
* [Nested Polynomial Multisets](Library/Wiki/Foundations/Nested_Polynomial_Multisets.md) — Polynomials as multisets of nested terms, Goh Factorization, and exact cyclotomic long division.
* [Nilpotent Infinitesimal Calculus](Library/Wiki/Foundations/Nilpotent_Infinitesimals.md) — Matrix representations of $\epsilon$ ($\epsilon^2 = 0$) and discrete Taylor calculus.
* [Emergent Quantum Mechanics](Library/Wiki/Foundations/Emergent_Quantum_Mechanics.md) — Wildberger's finitist quantum framework: dual numbers, rational spreads, symplectic commutators, and rational Born tally ratios.
* [Quantum Measurement & Superposition](Library/Wiki/Foundations/Quantum_Measurement_and_Superposition.md) — Double-slit resolution, observer-free cyclotomic collapse, and toroidal entanglement.
* [Structural Accounting & Token Geometry](Library/Wiki/Foundations/Structural_Accounting_and_Pure_Tokens.md) — Eliminating compiler integer coercions via pure inductive vector unrolling (`sumStructural`).
* [Vexels, Maxels, Boxels & Reflected Linear Algebra](Library/Wiki/Foundations/Vexels_Maxels_and_Reflected_Linear_Algebra.md) — Singletons $[n]$, Pixels $[i, j]$, Voxels $[x, y, z]$, Vexels (1D), Maxels (2D), Boxels (3D), and Elaborator Reflection macros.
* [Fractional Multisets & Ongoing Sequences (OnSeq)](Library/Wiki/Foundations/Singleton_Fractions_and_OnSeq_Algebra.md) — Non-zero Singleton denominators ($[D] \ge 1$), division-by-zero immunity, and Wildberger's constructive on-sequence and clip algebra.
* [Reflected Fractional Multisets & QTT Sequences](Library/Wiki/Foundations/Reflected_Fractional_Multisets_and_QTT_Sequences.md) — Elaborator Reflection invariant macros auditing non-zero denominators, cross-multiplication proofs, and QTT linear sequence resource conservation.
* [Hehner's Scale Conversion & Constructive Information Geometry](Library/Wiki/Foundations/Hehner_Scale_Conversion_and_Information_Geometry.md) — Unifying Bits ($b$), States ($s = 2^b$), and Chance ($c = 1/s$) without continuous logarithms or real numbers.
* [Multiset-Based Clifford Geometric Algebra](Library/Wiki/Foundations/Clifford_Multivector_Algebra.md) — Multivectors, geometric product $uv = \langle u, v \rangle + u \wedge v$, rotors, and conserved Dirac spinor currents.
* [Quantum State Transitions & Wilson Plaquettes](Library/Wiki/Foundations/Quantum_State_Transitions_and_Wilson_Loops.md) — Constructive state Vexels, discrete unitary S-matrices, Born probability conservation, and gauge-invariant Wilson loop plaquettes.
* [Contradictions With Standard Physics](Library/Wiki/Foundations/Contradictions_With_Standard_Physics.md) — Direct side-by-side refutations of continuous infinities, real numbers, wave collapse mystique, and singularity paradoxes.

### 2. Spacetime & Geometry
* [The 27 Ternary Geometries](Library/Wiki/Geometry/Ternary_Multiverse_27.md) — Permuting $\{-1, 0, 1\}$ into Elliptic, Hyperbolic, and Parabolic metric manifolds.
* [3D Lattice Topology & Conserved Flux](Library/Wiki/Geometry/Lattice_Topology_and_Flux.md) — The discrete 3-torus $T^3$, coordinate bijections, 6-face neighbors, and discrete Laplacian flux conservation ($\sum \Delta V = 0$).
* [Emergence of the 3-Torus Topology](Library/Wiki/Geometry/Emergent_Toroidal_Topology.md) — How the flat 3-torus $T^3$ emerges from the $\mathbb{Z}_3$ cyclic coordinate ring, QTT zero boundary leakage, and $g_{\text{Toroidal}}$ modular shear.
* [The 12 Emergent Laws of Physics](Library/Wiki/Geometry/Emergent_Pillars_of_Physics.md) — Deriving Conservation, Time's Arrow, Gravitational Inertia, Maxwell DEC, Quantum Infinitesimals, QCD Color Confinement, Speed of Light Locality, Fine Structure 137, Pauli Exclusion, Gravitational Waves, Nuclear Binding, and Baryon Asymmetry.
* [Geometric-Informational Duality & Cosmic Intelligence](Library/Wiki/Geometry/Geometric_Information_Duality_and_Cosmic_Intelligence.md) — Unifying Hyperbolic Geodesics, Clifford Collinearity, Chromogeometric Budgets, and the Holographic Principle.
* [Intra-Epoch Hadronic Confinement (Epoch 3)](Library/Wiki/Geometry/Hadronic_Color_Confinement.md) — Triadic Chromogeometric color charge partitioning (Red, Green, Blue) and color-neutral nucleon singlets.
* [Emergent Higher-Order Physics](Library/Wiki/Geometry/Emergent_Higher_Order_Physics.md) — Deriving Electrodynamics, Causal Posets, and Hamiltonian mechanics from $1\times 1 \to 2\times 2 \to 3\times 3\times 3$ grid expansion.
* [Archimedes' Function & Quadrea](Library/Wiki/Geometry/Archimedes_Function_and_Quadrea.md) — Gram determinants on $2\times 2$ maxels, collinear geodesics ($A=0$), and Quadrea flux.
* [Discrete Exterior Calculus & Gauge Fields](Library/Wiki/Geometry/Discrete_Exterior_Calculus_and_Gauge.md) — Cell complexes, curvature 2-forms $F = dA$, and $SU(3)$ color confinement.
* [2D Maxwell Field Equations](Library/Wiki/Geometry/Maxwell_Field_Equations.md) — Exact discrete electrodynamics running via structural accounting (`sumStructural`).
* [Grassmann Exterior Calculus & Yang-Mills Gauge Theory](Library/Wiki/Geometry/Grassmann_and_Yang_Mills.md) — Grassmann cochain hierarchy ($C_0, C_1, C_2, C_3$), exact Bianchi $d_2(d_1 A) = 0$, combinatorial Hodge duality, and Dihedron non-Abelian color flux confinement.
* [Yang-Mills Curvature as Plaquette Cross-Entropy](Library/Wiki/Geometry/Yang_Mills_Curvature_and_Plaquette_Cross_Entropy.md) — Discrete gauge connection circulation and cross-entropy deficit on 2-faces.
* [The Discrete Poynting Theorem](Library/Wiki/Geometry/Discrete_Poynting_Theorem.md) — Exact electromagnetic energy flux balance across 3D Boxel faces without continuous limits.
* [Rational Snell's Law & The Triple Spread Law](Library/Wiki/Geometry/Rational_Snell_and_Triple_Spread.md) — Rational trigonometry optics, exact spread refraction ($n_1^2 s_1 = n_2^2 s_2$), and the Triple Spread polynomial law.
* [The Constructive Dirac Spinor Equation](Library/Wiki/Geometry/Constructive_Dirac_Spinor.md) — Fermionic Dirac spinors and conserved vector currents formulated via Clifford multivector geometric algebra.
* [The Discrete Holographic Area Law](Library/Wiki/Geometry/Discrete_Holographic_Area_Law.md) — Topological state capacity scaling bounded by 2D boundary face Maxel count ($\text{Rank}(B) \le |\partial B|$).
* [Molecular Bonding & Chemical Graph Contraction](Library/Wiki/Geometry/Molecular_Bonding.md) — Tier 5 chemical molecular bonding, covalent Maxel contraction, Water Archimedes quadrea ($A=3$), and alkane saturation series ($C_n H_{2n+2}$).
* [Relational Metric Inference](Library/Wiki/Evolution/Non_Hardcoded_Cosmic_State.md) — Eliminating magic numbers through internal density ratios.

### 3. Evolutionary Dynamics & Law Encoding
* [Pre-Geometric Genesis (The vm = 0 Void)](Library/Wiki/Evolution/Pre_Geometric_Genesis.md) — Why Visible Matter is 0 before the 27-state metric tensor emerges.
* [Dark Matter as the Cosmic Law Ledger](Library/Wiki/Evolution/Dark_Matter_Law_Storage.md) — How the accumulated cyclotomic remainder ledger encodes gravitational drag, the 2nd Law of Thermodynamics, and time's arrow.
* [Visible Matter Tokens vs. Dark Matter Law Impedance](Library/Wiki/Evolution/Matter_Tokens_and_Law_Impedance.md) — The fundamental duality between local integer numerators (matter tokens) and global structural divisors (law impedance $1 + \text{drag}$).
* [Landauer's Principle as Linear Token Relocation](Library/Wiki/Evolution/Landauer_Principle_and_Linear_Token_Relocation.md) — QTT type-theoretic erasure relocating active VM tokens into the DM history ledger.
* [Cyclotomic Encoding & Decoding Protocol](Library/Wiki/Evolution/Cyclotomic_Encoding_and_Decoding.md) — How state polynomials are divided by $\Phi_{137}(x)$, encoded into remainder tokens, and decoded into kinematic drag and metric shear.
* [Dynamic Grid Expansion (`expandAndUnfoldGeneric`)](Library/Wiki/Evolution/Dynamic_Grid_Expansion.md) — Generalized non-hardcoded expansion pipeline scaling spatial arrays via chiral ket/bra outer products and structural history accumulation.
* [Renormalization Group & Multi-Scale Information Invariance](Library/Wiki/Evolution/Renormalization_Group_and_Scale_Invariance.md) — Scale expansion preserving 100% of topological invariants via multiset compactness.
* [Bootstrapping Epoch 1 to 37](Library/Wiki/Evolution/Bootstrap_Epoch_1_to_37.md) — Genesis vacuum, multi-epoch folding, and the 55-state Dark Matter residue at Primorial 210.
* [137-Stage Cycles & Lattice Expansion](Library/Wiki/Evolution/Cycle_137_and_Expansion.md) — Discrete grid expansion ($1\times 1 \to 2\times 2 \to 3\times 3$) and fine-structure cycle limits.
* [Hierarchical Matter Replication & The Alpha Cluster (Epoch 4)](Library/Wiki/Evolution/Alpha_Cluster_Replication.md) — 4 bonded 27-cell nucleons expanding into a 108-cell composite $^4\text{He}$ core.


### 4. Kinematics & Astrodynamics
* [Causal Posets & Inductive Lensing](Library/Wiki/Kinematics/Causal_Posets_and_Lensing.md) — Velocity routing through $g_{\text{EM}}$ vs $g_{\text{Substrate}}$ and Dark Matter gravitational drag.
* [Discrete Noether's Theorem & Symplectic Invariants](Library/Wiki/Kinematics/Discrete_Noether_Symplectic.md) — Conserved Noether momentum charges ($Q = p^T \delta q$) and symplectic area preservation ($dq \wedge dp$) on discrete lattices.
* [Discrete Symplectic Leapfrog Integrator](Library/Wiki/Kinematics/Symplectic_Leapfrog_Integrator.md) — Split kick-drift-kick Hamiltonian phase space flow and discrete energy conservation.

### 5. Metatheory & Verification
* [Verification Matrix](Library/Wiki/Verification/Verification_Matrix.md) — 100% comprehensive property checklist and reflection audit logs.
* [Structural Associativity Proof](Library/Wiki/Verification/Structural_Associativity_Proof.md) — Formal verification proving `sumStructural` associativity across scale partitions $((A \mathbin{+\!\!+} B) \mathbin{+\!\!+} C \equiv A \mathbin{+\!\!+} (B \mathbin{+\!\!+} C))$.
* [Cosmological Inferences, Quantum Deductions & Elaborator Verification](Library/Wiki/Verification/Cosmological_Inferences_and_Deductions.md) — Exact synthesis of the 7 core physical inferences derived from constructivist information geometry and QTT.



---

## 🚀 Running Verification Tests

To compile and run the full verification test suite:

```bash
cd Idris2-Universe2-Wiki
toolbox run -c fedora-toolbox-44 pack run Idris2-Universe2-Wiki.ipkg
```

---

© Justin Kelly. All rights reserved.
