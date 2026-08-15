# 📚 Idris2-Universe2-Wiki

**Literate Documentation, Formal Specifications, and Property Verification Suite for [Idris2-Universe2](https://github.com/justinkelly-ie/Idris2-Universe2).**

[![Idris2](https://img.shields.io/badge/Idris2-Verified_Wiki-blue.svg)](https://github.com/idris-lang/Idris2)
[![Epochs](https://img.shields.io/badge/Epochs-1_to_37-green.svg)]()
[![Ternary](https://img.shields.io/badge/Ternary_States-27_Closed-purple.svg)]()
[![Modules](https://img.shields.io/badge/Literate_Chapters-28_Verified-brightgreen.svg)]()
[![Tests](https://img.shields.io/badge/Test_Suite-22_Passed-success.svg)]()

---

## 🗺️ The Universal Rosetta Stone: Finite Math, Physics & Programming

The cornerstone of **Idris2-Universe2** is the strict mathematical isomorphism linking **Constructive Finitist Mathematics**, **Fundamental Physics**, and **Type-Theoretic Programming (Idris 2 QTT)**:

| Category | 📐 Finite / Rational Mathematics | 🌌 Cosmological Physics | 💻 Programming (Idris 2 / QTT) |
| :--- | :--- | :--- | :--- |
| **Number Genesis** | **Box Arithmetic**<br>Empty multisets: $[\ ] = 0, [[\ ]] = 1, \dots$ | **Pre-Geometric Void & Genesis**<br>Matter emergence from absolute zero state | **Inductive Data Types**<br>`data WildNat = EmptyBox \| NestBox WildNat` |
| **Signed Quantities** | **Grothendieck Group Completion**<br>Equivalence pairs $(P, N) \in \mathbb{N} \times \mathbb{N}$ | **Matter / Antimatter Asymmetry**<br>Flux cancellation and charge neutrality | **Algebraic Record Structure**<br>`record BoxInt where constructor (pos, neg)` |
| **Conservation Laws** | **Exact Integer Arithmetic**<br>Zero fractional or continuous leakage | **First Law of Thermodynamics**<br>Energy, momentum, and charge conservation ($\nabla \cdot \vec{J} = 0$) | **Quantitative Type Theory (QTT)**<br>Linear resource tracking `(1 x : BoxInt)` |
| **Spacetime Coordinates** | **Balanced Ternary Ring**<br>$\mathbb{Z}_3 = \{-1, 0, +1\}$ with cyclic addition | **3D Discrete Spacetime**<br>3 spatial axes forming the 27-cell maxel grid | **Sum Types & Bijections**<br>`data TernaryBit = MinusOne \| ZeroBit \| PlusOne` |
| **Global Topology** | **Toroidal Neighborhood Graph**<br>Periodic boundary 3-torus $T^3 \equiv \mathbb{Z}_3^3$ | **Boundaryless Compact Space**<br>Eliminates edge-leakage ($\partial M = \emptyset$) | **Modulo Indexing & Vectors**<br>`shiftTernaryForward`, `Vect 27 BoxInt` |
| **Quantum Phase & Limits**| **Nilpotent Dual Numbers**<br>Matrix unit $\epsilon = \begin{pmatrix} 0 & 1 \\ 0 & 0 \end{pmatrix}, \ \epsilon^2 = 0$ | **Quantum Calculus & Symplectic Phase**<br>Exact first derivatives without infinite limits ($\mathbb{R}$) | **Dual Number Records**<br>`record DualComplex where constructor (r, eps)` |
| **Curvature & Metrics** | **Ternary Metric Classification**<br>27 metric tensors (Elliptic, Hyperbolic, Parabolic) | **General Relativity & Light Cones**<br>Relational spacetime metric from matter/energy ratios | **Dependent Pattern Matching**<br>`data MetricTensor2D`, `classifyMetric` |
| **Electrodynamics** | **Discrete Exterior Calculus (DEC)**<br>1-form potentials $A$, 2-form curvature $F = dA$ | **Maxwell's Equations & Gauge Theory**<br>Bianchi identity ($dF = 0$) and Gauss-Ampère Law | **Cell Complex Differential Operators**<br>`d0 : C0 -> C1`, `d1 : C1 -> C2` |
| **Strong Force / QCD** | **Triadic Partitioning**<br>3 orthogonal $Z$-slices ($3 \times 9 = 27$) | **$SU(3)$ Color Confinement**<br>Red, Green, Blue balance in color-neutral hadrons | **Color Charge Enums & Filters**<br>`data ColorCharge = RedColor \| GreenColor \| BlueColor` |
| **Atomic Clustering** | **Hierarchical Spatial Embedding**<br>$4 \times 27 = 108$ cells (Tetrahedral maxels) | **Nuclear Physics (Alpha Particle)**<br>4-nucleon composite $^4\text{He}$ atomic core | **Nested Dependent Vectors**<br>`Vect 4 HadronState -> Vect 108 BoxInt` |
| **Time & Entropy** | **Monomial Goh Factorization**<br>Division by 137th Cyclotomic Polynomial $\Phi_{137}(x)$ | **Arrow of Time & 2nd Law**<br>Monotonic entropy growth and temporal shear ($g_{22} = 0$) | **Append-Only Immutable Lists**<br>`updatedDM = remainder :: dmLogData` ($dm \to S\ dm$) |
| **Gravitational Inertia** | **Scale Impedance Ratio**<br>Quotient scaling $\frac{1}{1 + \sum r_i}$ | **Gravitational Lensing & Mass**<br>Scale-dependent velocity deceleration by Dark Matter | **Linear Vector Transformations**<br>`lensVelocityAcrossScale` |
| **Cosmic Evolution** | **Primorial Budget Sequences**<br>Primorial partitions: $210 = 27 + 128 + 55$ | **Cosmological Epochs**<br>Vacuum expansion from Epoch 1 to Ground State Epoch 37 | **Dependent State Records**<br>`record UniverseState (vm : Nat) (de : Nat) (dm : Nat)` |
| **Metatheory & Validation**| **Constructive Proof Witnesses**<br>Curry-Howard isomorphism ($A \cong \text{Type}$) | **Physical Law Invariance**<br>Non-negotiable compile-time consistency of reality | **Elaborator Reflection Macros**<br>`%macro`, `Reflect.InvariantAuditor`, `Refl` |

---

## 🧭 Master Table of Contents

### 1. Foundations & Philosophy
* [The Universal Mapping](Library/Wiki/Foundations/Universal_Mapping.md) — Correspondence between Idris 2 QTT / Elaborator Reflection and Cosmological Physics.
* [Box Arithmetic & Inductive Multisets](Library/Wiki/Foundations/Box_Arithmetic.md) — Deriving Natural Numbers from empty boxes ($[\ ] = 0, [[\ ]] = 1, [[\ ] [\ ]] = 2, \dots$) and physical conservation.
* [Pure Box Integers as Grothendieck Pairs](Library/Wiki/Foundations/Grothendieck_Box_Integers.md) — Signed integers as pairs of positive/negative empty box containers $(P, N)$.
* [Nested Polynomial Multisets](Library/Wiki/Foundations/Nested_Polynomial_Multisets.md) — Polynomials as multisets of nested terms, Goh Factorization, and exact cyclotomic long division.
* [Nilpotent Infinitesimal Calculus](Library/Wiki/Foundations/Nilpotent_Infinitesimals.md) — Matrix representations of $\epsilon$ ($\epsilon^2 = 0$) and discrete Taylor calculus.
* [Emergent Quantum Mechanics](Library/Wiki/Foundations/Emergent_Quantum_Mechanics.md) — Wildberger's finitist quantum framework: dual numbers, rational spreads, symplectic commutators, and rational Born tally ratios.
* [Quantum Measurement & Superposition](Library/Wiki/Foundations/Quantum_Measurement_and_Superposition.md) — Resolving the double-slit experiment, destructive phase cancellation, observer-free collapse, and toroidal entanglement.
* [Structural Accounting & Pure Tokens](Library/Wiki/Foundations/Structural_Accounting_and_Pure_Tokens.md) — Eliminating unverified runtime `cast` operations through pure inductive BoxInt vector unrolling and associative grouping.
* [Contradictions with Standard Physics](Library/Wiki/Foundations/Contradictions_With_Standard_Physics.md) — Comparative analysis against $\Lambda\text{CDM}$, General Relativity, and Continuum QFT.

### 2. Spacetime & Geometry
* [The 27 Ternary Geometries](Library/Wiki/Geometry/Ternary_Multiverse_27.md) — Permuting $\{-1, 0, 1\}$ into Elliptic, Hyperbolic, and Parabolic metric manifolds.
* [3D Lattice Topology & Conserved Flux](Library/Wiki/Geometry/Lattice_Topology_and_Flux.md) — The discrete 3-torus $T^3$, coordinate bijections, 6-face neighbors, and discrete Laplacian flux conservation ($\sum \Delta V = 0$).
* [Emergence of the 3-Torus Topology](Library/Wiki/Geometry/Emergent_Toroidal_Topology.md) — How the flat 3-torus $T^3$ emerges from the $\mathbb{Z}_3$ cyclic coordinate ring, QTT zero boundary leakage, and $g_{\text{Toroidal}}$ modular shear.
* [The 12 Emergent Laws of Physics](Library/Wiki/Geometry/Emergent_Pillars_of_Physics.md) — Deriving Conservation, Time's Arrow, Gravitational Inertia, Maxwell DEC, Quantum Infinitesimals, QCD Color Confinement, Speed of Light Locality, Fine Structure 137, Pauli Exclusion, Gravitational Waves, Nuclear Binding, and Baryon Asymmetry.
* [Intra-Epoch Hadronic Confinement (Epoch 3)](Library/Wiki/Geometry/Hadronic_Color_Confinement.md) — Triadic Chromogeometric color charge partitioning (Red, Green, Blue) and color-neutral nucleon singlets.
* [Emergent Higher-Order Physics](Library/Wiki/Geometry/Emergent_Higher_Order_Physics.md) — Deriving Electrodynamics, Causal Posets, and Hamiltonian mechanics from $1\times 1 \to 2\times 2 \to 3\times 3\times 3$ grid expansion.
* [Archimedes' Function & Quadrea](Library/Wiki/Geometry/Archimedes_Function_and_Quadrea.md) — Gram determinants on $2\times 2$ maxels, collinear geodesics ($A=0$), and Quadrea flux.
* [Discrete Exterior Calculus & Gauge Fields](Library/Wiki/Geometry/Discrete_Exterior_Calculus_and_Gauge.md) — Cell complexes, curvature 2-forms $F = dA$, and $SU(3)$ color confinement.
* [2D Maxwell Field Equations](Library/Wiki/Geometry/Maxwell_Field_Equations.md) — Exact discrete electrodynamics running via structural accounting (`sumStructural`).
* [Relational Metric Inference](Library/Wiki/Evolution/Non_Hardcoded_Cosmic_State.md) — Eliminating magic numbers through internal density ratios.

### 3. Evolutionary Dynamics & Law Encoding
* [Pre-Geometric Genesis (The vm = 0 Void)](Library/Wiki/Evolution/Pre_Geometric_Genesis.md) — Why Visible Matter is 0 before the 27-state metric tensor emerges.
* [Dark Matter as the Cosmic Law Ledger](Library/Wiki/Evolution/Dark_Matter_Law_Storage.md) — How the accumulated cyclotomic remainder ledger encodes gravitational drag, the 2nd Law of Thermodynamics, and time's arrow.
* [Cyclotomic Encoding & Decoding Protocol](Library/Wiki/Evolution/Cyclotomic_Encoding_and_Decoding.md) — How state polynomials are divided by $\Phi_{137}(x)$, encoded into remainder tokens, and decoded into kinematic drag and metric shear.
* [Bootstrapping Epoch 1 to 37](Library/Wiki/Evolution/Bootstrap_Epoch_1_to_37.md) — Genesis vacuum, multi-epoch folding, and the 55-state Dark Matter residue at Primorial 210.
* [137-Stage Cycles & Lattice Expansion](Library/Wiki/Evolution/Cycle_137_and_Expansion.md) — Discrete grid expansion ($1\times 1 \to 2\times 2 \to 3\times 3$) and fine-structure cycle limits.
* [Hierarchical Matter Replication & The Alpha Cluster (Epoch 4)](Library/Wiki/Evolution/Alpha_Cluster_Replication.md) — 4 bonded 27-cell nucleons expanding into a 108-cell composite $^4\text{He}$ core.

### 4. Kinematics & Gauge Dynamics
* [Causal Posets & Inductive Lensing](Library/Wiki/Kinematics/Causal_Posets_and_Lensing.md) — Velocity routing through $g_{\text{EM}}$ vs $g_{\text{Substrate}}$ and Dark Matter gravitational drag.

### 5. Metatheory & Verification
* [Verification Matrix](Library/Wiki/Verification/Verification_Matrix.md) — 100% comprehensive property checklist and reflection audit logs.
* [Structural Associativity Proof](Library/Wiki/Verification/Structural_Associativity_Proof.md) — Formal verification proving `sumStructural` associativity across scale partitions $((A \mathbin{+\!\!+} B) \mathbin{+\!\!+} C \equiv A \mathbin{+\!\!+} (B \mathbin{+\!\!+} C))$.

---

## 🚀 Running Verification Tests

To compile and run the full verification test suite:

```bash
cd Idris2-Universe2-Wiki
toolbox run -c fedora-toolbox-44 pack run Idris2-Universe2-Wiki.ipkg
```

---

© Justin Kelly. All rights reserved.
