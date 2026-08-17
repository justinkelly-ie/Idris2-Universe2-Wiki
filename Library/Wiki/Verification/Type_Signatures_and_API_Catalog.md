# 📋 Type Signatures & API Catalog

This document provides an **automatically generated, authoritative reference** for all data types, records, type aliases, and primary state transitions in `Idris2-Universe2`.

> [!NOTE]
> This catalog is generated dynamically from the codebase source files via `Scripts/generate_type_catalog.py`.

---

## <a id="table-of-contents"></a>📑 Table of Contents

- [**1. Core Foundations & Data Structures**](#section-1)
  - [`Core.BoxInt`](#mod-core-boxint)
  - [`Core.Multiset`](#mod-core-multiset)
  - [`Core.MultisetTree`](#mod-core-multisettree)
  - [`Core.OnSeq`](#mod-core-onseq)
  - [`Core.Polynomial`](#mod-core-polynomial)
  - [`Core.Polynumber`](#mod-core-polynumber)
  - [`Core.UnixelFraction`](#mod-core-unixelfraction)
  - [`Core.VexelMaxel`](#mod-core-vexelmaxel)
- [**2. Spacetime, Geometries & Metrics**](#section-2)
  - [`Derivation.PureGeometricClassifier`](#mod-derivation-puregeometricclassifier)
  - [`Geometry.GrassmannCalculus`](#mod-geometry-grassmanncalculus)
  - [`Geometry.InformationGeometry`](#mod-geometry-informationgeometry)
  - [`Geometry.LatticeTopology`](#mod-geometry-latticetopology)
  - [`Math.FourGeometries`](#mod-math-fourgeometries)
  - [`Math.LinAlgebra.BilinearProduct`](#mod-math-linalgebra-bilinearproduct)
  - [`Math.LinAlgebra.MetricTensor`](#mod-math-linalgebra-metrictensor)
  - [`Math.LinAlgebra.TernaryClassifier`](#mod-math-linalgebra-ternaryclassifier)
- [**3. Cosmological State & Linear Evolution**](#section-3)
  - [`Evolution.Bootstrap`](#mod-evolution-bootstrap)
  - [`Evolution.Contraction`](#mod-evolution-contraction)
  - [`Evolution.Expansion`](#mod-evolution-expansion)
  - [`Evolution.Init`](#mod-evolution-init)
  - [`Evolution.LinearPipeline`](#mod-evolution-linearpipeline)
  - [`Evolution.State`](#mod-evolution-state)
  - [`Evolution.StructuralAccounting`](#mod-evolution-structuralaccounting)
- [**4. Emergent Physical Laws & Gauge Theories**](#section-4)
  - [`Math.AharonovBohmHolonomy`](#mod-math-aharonovbohmholonomy)
  - [`Math.CliffordAlgebra`](#mod-math-cliffordalgebra)
  - [`Math.ConstructiveBaryogenesis`](#mod-math-constructivebaryogenesis)
  - [`Math.DiscreteActionPrinciple`](#mod-math-discreteactionprinciple)
  - [`Math.DiscreteBoltzmannDistribution`](#mod-math-discreteboltzmanndistribution)
  - [`Math.DiscreteCasimirEffect`](#mod-math-discretecasimireffect)
  - [`Math.DiscreteChiralAnomaly`](#mod-math-discretechiralanomaly)
  - [`Math.DiscreteDiracSpinor`](#mod-math-discretediracspinor)
  - [`Math.DiscreteHolographicBound`](#mod-math-discreteholographicbound)
  - [`Math.DiscreteJarzynskiEquality`](#mod-math-discretejarzynskiequality)
  - [`Math.DiscreteLandauerPrinciple`](#mod-math-discretelandauerprinciple)
  - [`Math.DiscretePoyntingTheorem`](#mod-math-discretepoyntingtheorem)
  - [`Math.DiscreteWheelerDeWitt`](#mod-math-discretewheelerdewitt)
  - [`Math.FineStructure`](#mod-math-finestructure)
  - [`Math.FractionalQuantumHall`](#mod-math-fractionalquantumhall)
  - [`Math.GalacticRotationCurve`](#mod-math-galacticrotationcurve)
  - [`Math.GaugeSpinorCoupling`](#mod-math-gaugespinorcoupling)
  - [`Math.GravitationalWaveDynamics`](#mod-math-gravitationalwavedynamics)
  - [`Math.HelmholtzFreeEnergy`](#mod-math-helmholtzfreeenergy)
  - [`Math.Infinitesimal`](#mod-math-infinitesimal)
  - [`Math.PauliExclusion`](#mod-math-pauliexclusion)
  - [`Math.QuantumTransition`](#mod-math-quantumtransition)
  - [`Math.RGDecimator`](#mod-math-rgdecimator)
  - [`Math.RationalTrig`](#mod-math-rationaltrig)
  - [`Math.RenormalizationInformationFlow`](#mod-math-renormalizationinformationflow)
  - [`Math.ShannonHuffmanOptimality`](#mod-math-shannonhuffmanoptimality)
  - [`Math.SuperconductingFluxQuantization`](#mod-math-superconductingfluxquantization)
  - [`Math.TopologicalChernNumber`](#mod-math-topologicalchernnumber)
  - [`Math.ToroidalAstrodynamics`](#mod-math-toroidalastrodynamics)
  - [`Math.WilsonPolyhedra`](#mod-math-wilsonpolyhedra)
- [**5. Compound Structures & Chemical Networks**](#section-5)
  - [`Compound.AlphaReplication`](#mod-compound-alphareplication)
  - [`Compound.HadronicConfinement`](#mod-compound-hadronicconfinement)
  - [`Compound.HydrogenBonding`](#mod-compound-hydrogenbonding)
  - [`Compound.LinearEpsilonRouting`](#mod-compound-linearepsilonrouting)
  - [`Compound.MacromolecularChirality`](#mod-compound-macromolecularchirality)
  - [`Compound.MolecularBonding`](#mod-compound-molecularbonding)
  - [`Compound.PlasmaRecombination`](#mod-compound-plasmarecombination)
  - [`Compound.StellarNucleosynthesis`](#mod-compound-stellarnucleosynthesis)
  - [`Compound.SymplecticIntegrator`](#mod-compound-symplecticintegrator)
  - [`Compound.VelocityLensing`](#mod-compound-velocitylensing)
  - [`Compound.WatsonCrickBasePairing`](#mod-compound-watsoncrickbasepairing)
- [**6. Elaborator Reflection & Invariant Macros**](#section-6)
  - [`Reflect.InvariantAuditor`](#mod-reflect-invariantauditor)
  - [`Reflect.PermutationSolver`](#mod-reflect-permutationsolver)

---

## <a id="section-1"></a>1. Core Foundations & Data Structures

### <a id="mod-core-boxint"></a>Module `Core.BoxInt`

#### 📦 Records

```idris
record BoxInt where
  constructor MkBoxInt
  value : Integer
```

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-core-multiset"></a>Module `Core.Multiset`

#### 📦 Records

```idris
record IntegerPartition where
  constructor MkPartition
  parts : List Multiplicity
```

```idris
record Box a where
  constructor MkBox
  items : List (a, BoxInt)
```

#### 🏷️ Algebraic Data Types

```idris
data Multiplicity : Type where
  Count : (val : Nat) -> (qty : Nat) -> Multiplicity
```

```idris
data BoxSpec : Type where
  Leaf : BoxSpec
  Node : {n : Nat} -> Vect n BoxSpec -> BoxSpec
```

```idris
data Polynumber : (0 spec : BoxSpec) -> Type where
  Zero : Polynumber Leaf
  Nest : (1 elements : Vect n (Polynumber childSpec)) -> 
         Polynumber (Node (replicate n childSpec))

||| Wildberger Natural numbers defined as multisets of empty boxes.
||| - WZero = Leaf ([]) = 0
||| - WNil  = Node []
||| - WSucc WZero WNil = Node [Leaf] ([[]]) = 1
||| - WSucc WZero (WSucc WZero WNil) = Node [Leaf, Leaf] ([[] []]) = 2
```

```idris
data WildNat : (0 spec : BoxSpec) -> Type where
  WZero : WildNat Leaf
  WNil  : WildNat (Node [])
  WSucc : {0 xs : Vect n BoxSpec} -> 
          (1 zeroElement : WildNat Leaf) -> 
          (1 rest : WildNat (Node xs)) -> 
          WildNat (Node (Leaf :: xs))

||| Tallies the physical count of empty box tokens inside a WildNat.
```

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-core-multisettree"></a>Module `Core.MultisetTree`

#### 🏷️ Algebraic Data Types

```idris
data MultisetTree a =
    Leaf
  | Node (MultisetTree a) a Nat (MultisetTree a)
```

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-core-onseq"></a>Module `Core.OnSeq`

#### 📦 Records

```idris
record OnSeq a where
  constructor MkOnSeq
  start : Nat
  at    : Nat -> a

||| A finite consecutive subsequence (clip) extracted from an ongoing sequence.
```

```idris
record Clip a where
  constructor MkClip
  startIdx : Nat
  elements : List a
```

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-core-polynomial"></a>Module `Core.Polynomial`

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-core-polynumber"></a>Module `Core.Polynumber`

#### 📦 Records

```idris
record PolynumberTerm where
  constructor MkPolynumberTerm
  coeff  : BoxInt
  degree : Nat
```

```idris
record Polynumber where
  constructor MkPolynumber
  coeffs : List BoxInt -- coeffs[k] is coefficient of x^k
```

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-core-unixelfraction"></a>Module `Core.UnixelFraction`

#### 📦 Records

```idris
record FractionalBox (numType : Type) where
  constructor OverUnixel
  numerator   : numType
  denominator : Unixel

||| Smart constructor for FractionalBox ensuring non-zero denominator.
```

```idris
record UnixelFraction where
  constructor MkUnixelFraction
  num : BoxInt
  den : Unixel

||| Smart constructor building a UnixelFraction with clamped non-zero denominator.
```

#### 🏷️ Algebraic Data Types

```idris
data SternBrocotBranch = BranchL | BranchR
```

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-core-vexelmaxel"></a>Module `Core.VexelMaxel`

#### 📦 Records

```idris
record Unixel where
  constructor MkUnixel
  index : Nat
```

```idris
record Pixel where
  constructor MkPixel
  row : Nat
  col : Nat
```

```idris
record Voxel where
  constructor MkVoxel
  axisX : Nat
  axisY : Nat
  axisZ : Nat
```

```idris
record Vexel where
  constructor MkVexel
  terms : List (Unixel, BoxInt)
```

```idris
record Maxel where
  constructor MkMaxel
  pixels : List (Pixel, BoxInt)
```

```idris
record Boxel where
  constructor MkBoxel
  voxels : List (Voxel, BoxInt)
```

```idris
record GeneBoxel where
  constructor MkGene
  codons : Boxel

||| Fundamental Amino Acids transcribed from genetic triplet codons:
||| - Methionine (AUG / [0, 1, 2] - Start Codon)
||| - Alanine (GCU / [2, 1, 0])
||| - Glycine (GGU / [2, 2, 0])
||| - Serine (UCU / [1, 1, 0])
||| - StopCodon (UAA / [1, 0, 0])
||| - UnknownAcid
```

```idris
record Tesseract where
  constructor MkTesseract
  x : Nat
  y : Nat
  z : Nat
  t : Nat
```

```idris
record HyperBoxel where
  constructor MkHyperBoxel
  cells : List (Tesseract, BoxInt)
```

```idris
record BalanceArray (n : Nat) where
  constructor MkBalanceArray
  posWeights : Vect n Nat
  negWeights : Vect n Nat
```

```idris
record MagicMaxel (n : Nat) where
  constructor MkMagicMaxel
  grid : Vect n (Vect n Nat)
```

#### 🏷️ Algebraic Data Types

```idris
data AminoAcid = Methionine | Alanine | Glycine | Serine | StopCodon | UnknownAcid
```

[↑ Back to Top](#table-of-contents)

---

## <a id="section-2"></a>2. Spacetime, Geometries & Metrics

### <a id="mod-derivation-puregeometricclassifier"></a>Module `Derivation.PureGeometricClassifier`

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-geometry-grassmanncalculus"></a>Module `Geometry.GrassmannCalculus`

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-geometry-informationgeometry"></a>Module `Geometry.InformationGeometry`

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-geometry-latticetopology"></a>Module `Geometry.LatticeTopology`

#### 📦 Records

```idris
record Coord3D where
  constructor MkCoord3D
  coordX : TernaryBit
  coordY : TernaryBit
  coordZ : TernaryBit
```

#### 🏷️ Algebraic Data Types

```idris
data CardinalDir = DirEast | DirWest | DirNorth | DirSouth | DirUp | DirDown

||| Computes the adjacent face neighbor coordinate along a cardinal direction.
```

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-math-fourgeometries"></a>Module `Math.FourGeometries`

#### 🏷️ Algebraic Data Types

```idris
data FundamentalGeometry = 
    EllipticGeom 
  | HyperbolicGeom 
  | ParabolicGeom 
  | SubstrateGeom
```

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-math-linalgebra-bilinearproduct"></a>Module `Math.LinAlgebra.BilinearProduct`

#### 📦 Records

```idris
record InfinitesimalStep2D where
  constructor MkStep2D
  dx : Maxel
  dy : Maxel
```

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-math-linalgebra-metrictensor"></a>Module `Math.LinAlgebra.MetricTensor`

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-math-linalgebra-ternaryclassifier"></a>Module `Math.LinAlgebra.TernaryClassifier`

#### 🏷️ Algebraic Data Types

```idris
data TernaryBit = MinusOne | ZeroBit | PlusOne
```

```idris
data MetricSignature = 
    SigElliptic    -- det(g) > 0  (Euclidean / Matter canvas)
  | SigHyperbolic  -- det(g) < 0  (Minkowski / Causal / Symplectic)
  | SigParabolic   -- det(g) == 0 (Degenerate / Spread / Boolean)
```

[↑ Back to Top](#table-of-contents)

---

## <a id="section-3"></a>3. Cosmological State & Linear Evolution

### <a id="mod-evolution-bootstrap"></a>Module `Evolution.Bootstrap`

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-evolution-contraction"></a>Module `Evolution.Contraction`

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-evolution-expansion"></a>Module `Evolution.Expansion`

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-evolution-init"></a>Module `Evolution.Init`

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-evolution-linearpipeline"></a>Module `Evolution.LinearPipeline`

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-evolution-state"></a>Module `Evolution.State`

#### 📦 Records

```idris
record UniverseState (vmSize : Nat) (deSize : Nat) (dmSize : Nat) where
  constructor MkUniverseState
  visibleMatter : Vect vmSize BoxInt -- Active spatial field lattice
  darkEnergy    : Vect deSize BoxInt -- Background ROM capacity
  darkMatter    : Vect dmSize BoxInt -- Historical error/residue ledger

||| Extracts the Dark Matter log as a read-only reference.
```

```idris
record CosmicMultiset where
  constructor MkCosmicMultiset
  visible    : Boxel
  darkEnergy : Maxel
  darkMatter : Vexel

||| Calculates total active state energy across the cosmic multiset.
```

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-evolution-structuralaccounting"></a>Module `Evolution.StructuralAccounting`

[↑ Back to Top](#table-of-contents)

---

## <a id="section-4"></a>4. Emergent Physical Laws & Gauge Theories

### <a id="mod-math-aharonovbohmholonomy"></a>Module `Math.AharonovBohmHolonomy`

#### 🏷️ Algebraic Data Types

```idris
data GaussianLink = PlusOne | PlusI | MinusOne | MinusI
```

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-math-cliffordalgebra"></a>Module `Math.CliffordAlgebra`

#### 📦 Records

```idris
record Multivector where
  constructor MkMultivector
  scalarPart   : BoxInt
  vectorPart   : Vexel
  bivectorPart : Maxel
  trivectorPart: Boxel
```

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-math-constructivebaryogenesis"></a>Module `Math.ConstructiveBaryogenesis`

#### 📦 Records

```idris
record BaryonState where
  constructor MkBaryonState
  baryonPos    : BoxInt
  baryonNeg    : BoxInt
  photonTokens : BoxInt
```

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-math-discreteactionprinciple"></a>Module `Math.DiscreteActionPrinciple`

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-math-discreteboltzmanndistribution"></a>Module `Math.DiscreteBoltzmannDistribution`

#### 📦 Records

```idris
record EnergyLevel where
  constructor MkEnergyLevel
  energyIndex  : Nat
  multiplicity : Nat
```

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-math-discretecasimireffect"></a>Module `Math.DiscreteCasimirEffect`

#### 📦 Records

```idris
record CavityBoundary where
  constructor MkCavityBoundary
  plateSeparation : Nat
```

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-math-discretechiralanomaly"></a>Module `Math.DiscreteChiralAnomaly`

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-math-discretediracspinor"></a>Module `Math.DiscreteDiracSpinor`

#### 📦 Records

```idris
record DiracSpinor4 where
  constructor MkDiracSpinor4
  comp1 : Pixel
  comp2 : Pixel
  comp3 : Pixel
  comp4 : Pixel
```

```idris
record ChiralComponents where
  constructor MkChiralComponents
  leftHanded  : BoxInt
  rightHanded : BoxInt
```

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-math-discreteholographicbound"></a>Module `Math.DiscreteHolographicBound`

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-math-discretejarzynskiequality"></a>Module `Math.DiscreteJarzynskiEquality`

#### 📦 Records

```idris
record NonEquilibriumPath where
  constructor MkNonEquilibriumPath
  pathWork   : BoxInt
  pathWeight : Nat
```

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-math-discretelandauerprinciple"></a>Module `Math.DiscreteLandauerPrinciple`

#### 📦 Records

```idris
record BitMemoryState where
  constructor MkBitMemoryState
  activeBits   : Nat
  activeEnergy : BoxInt
  sinkEnergy   : BoxInt
```

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-math-discretepoyntingtheorem"></a>Module `Math.DiscretePoyntingTheorem`

#### 📦 Records

```idris
record DiscreteEMCell where
  constructor MkDiscreteEMCell
  electricEnergy : BoxInt
  magneticEnergy : BoxInt
  poyntingFluxOut: BoxInt
  jouleWork      : BoxInt
```

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-math-discretewheelerdewitt"></a>Module `Math.DiscreteWheelerDeWitt`

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-math-finestructure"></a>Module `Math.FineStructure`

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-math-fractionalquantumhall"></a>Module `Math.FractionalQuantumHall`

#### 📦 Records

```idris
record LaughlinState where
  constructor MkLaughlinState
  fillingNumerator : Nat
  fillingDenominator : Nat
```

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-math-galacticrotationcurve"></a>Module `Math.GalacticRotationCurve`

#### 📦 Records

```idris
record GalacticProfile where
  constructor MkGalacticProfile
  coreBaryonMass : BoxInt
  diskMassSlope  : BoxInt
```

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-math-gaugespinorcoupling"></a>Module `Math.GaugeSpinorCoupling`

#### 📦 Records

```idris
record GaugeCoupledSpinor where
  constructor MkGaugeCoupledSpinor
  spinor      : DiracSpinor4
  gaugeCharge : BoxInt
  connectionA : (BoxInt, BoxInt, BoxInt, BoxInt)
```

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-math-gravitationalwavedynamics"></a>Module `Math.GravitationalWaveDynamics`

#### 📦 Records

```idris
record MetricShearTT where
  constructor MkMetricShearTT
  hPlus  : BoxInt
  hCross : BoxInt
```

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-math-helmholtzfreeenergy"></a>Module `Math.HelmholtzFreeEnergy`

#### 📦 Records

```idris
record CosmicBudgetPartition where
  constructor MkCosmicBudgetPartition
  vmTokens : BoxInt
  deTokens : BoxInt
  dmTokens : BoxInt
```

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-math-infinitesimal"></a>Module `Math.Infinitesimal`

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-math-pauliexclusion"></a>Module `Math.PauliExclusion`

#### 🏷️ Algebraic Data Types

```idris
data FermionOccupancy = Vacant | Occupied
```

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-math-quantumtransition"></a>Module `Math.QuantumTransition`

#### 📦 Records

```idris
record DualAmplitude where
  constructor MkDualAmplitude
  real : BoxInt
  imag : BoxInt
```

```idris
record QuantumState where
  constructor MkQuantumState
  amplitudes : List (Unixel, DualAmplitude)
```

```idris
record QuantumOperator where
  constructor MkQuantumOperator
  matrix : List (Pixel, DualAmplitude)
```

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-math-rgdecimator"></a>Module `Math.RGDecimator`

#### 📦 Records

```idris
record Plaquette2x2 where
  constructor MkPlaquette2x2
  f00 : BoxInt
  f01 : BoxInt
  f10 : BoxInt
  f11 : BoxInt
```

```idris
record MacroPlaquette where
  constructor MkMacroPlaquette
  totalFlux : BoxInt
```

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-math-rationaltrig"></a>Module `Math.RationalTrig`

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-math-renormalizationinformationflow"></a>Module `Math.RenormalizationInformationFlow`

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-math-shannonhuffmanoptimality"></a>Module `Math.ShannonHuffmanOptimality`

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-math-superconductingfluxquantization"></a>Module `Math.SuperconductingFluxQuantization`

#### 📦 Records

```idris
record SuperconductingLoop where
  constructor MkSuperconductingLoop
  cooperPairCharge : BoxInt
  fluxQuantumPhi0  : BoxInt
  windingNumber    : BoxInt
```

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-math-topologicalchernnumber"></a>Module `Math.TopologicalChernNumber`

#### 📦 Records

```idris
record TorusPlaquette where
  constructor MkTorusPlaquette
  gridX : Nat
  gridY : Nat
  berryFluxNumerator : Integer
  berryFluxDenominator : Integer
```

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-math-toroidalastrodynamics"></a>Module `Math.ToroidalAstrodynamics`

#### 📦 Records

```idris
record ToroidalPos where
  constructor MkToroidalPos
  posX : BoxInt
  posY : BoxInt
  posZ : BoxInt
  boxL : BoxInt
```

```idris
record MassToken where
  constructor MkMassToken
  mass : BoxInt
  pos  : ToroidalPos
  vel  : (BoxInt, BoxInt, BoxInt)
```

```idris
record RationalOrbit where
  constructor MkRationalOrbit
  semiMajorQuadrance : BoxInt -- Q_a = a^2
  focalQuadrance     : BoxInt -- Q_c = c^2
  orbitalPeriod      : BoxInt -- T
```

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-math-wilsonpolyhedra"></a>Module `Math.WilsonPolyhedra`

#### 📦 Records

```idris
record ColorState where
  constructor MkColorState
  redAmp   : DualAmplitude
  greenAmp : DualAmplitude
  blueAmp  : DualAmplitude
```

```idris
record WilsonPolyhedron where
  constructor MkWilsonPolyhedron
  faceEast  : QuantumOperator -- +X face
  faceWest  : QuantumOperator -- -X face
  faceNorth : QuantumOperator -- +Y face
  faceSouth : QuantumOperator -- -Y face
  faceUp    : QuantumOperator -- +Z face
  faceDown  : QuantumOperator -- -Z face
```

[↑ Back to Top](#table-of-contents)

---

## <a id="section-5"></a>5. Compound Structures & Chemical Networks

### <a id="mod-compound-alphareplication"></a>Module `Compound.AlphaReplication`

#### 📦 Records

```idris
record NuclearCluster (k : Nat) where
  constructor MkNuclearCluster
  nucleons : Vect k HadronState

||| Flattens a NuclearCluster into a contiguous (k * 27)-cell Visible Matter vector.
```

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-compound-hadronicconfinement"></a>Module `Compound.HadronicConfinement`

#### 📦 Records

```idris
record HadronState where
  constructor MkHadronState
  latticeGrid : Vect 27 BoxInt

||| Creates a balanced Hadronic Ground State at Epoch 3.
||| Injects 1 unit of Quark flux into each cell (9 Red + 9 Green + 9 Blue = 27 total flux).
```

#### 🏷️ Algebraic Data Types

```idris
data ColorCharge = RedColor | GreenColor | BlueColor
```

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-compound-hydrogenbonding"></a>Module `Compound.HydrogenBonding`

#### 📦 Records

```idris
record HydrogenBond where
  constructor MkHydrogenBond
  donorAtom    : Nat
  hydrogenAtom : Nat
  acceptorAtom : Nat
  energyTenths : Nat -- Energy in 1/10ths of covalent single bond (typically 1-2 tenths)
```

```idris
record WaterCluster (n : Nat) where
  constructor MkWaterCluster
  waterCount : Nat
  hBondCount : Nat
  hBondMaxel : Maxel

||| Tetrahedral Water Hexamer (6 H2O molecules in hexagonal/tetrahedral liquid percolation).
||| In a fully coordinated liquid network, each H2O participates in up to 4 H-bonds (2 donor, 2 acceptor).
```

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-compound-linearepsilonrouting"></a>Module `Compound.LinearEpsilonRouting`

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-compound-macromolecularchirality"></a>Module `Compound.MacromolecularChirality`

#### 📦 Records

```idris
record SignedVoxel where
  constructor MkSignedVoxel
  sX : BoxInt
  sY : BoxInt
  sZ : BoxInt
```

```idris
record AminoAcidMonomer where
  constructor MkAminoAcidMonomer
  monomerName     : String
  monomerFormula  : String
  carbonCount     : Nat
  hydrogenCount   : Nat
  nitrogenCount   : Nat
  oxygenCount     : Nat
  chirality       : Chirality
```

```idris
record Dipeptide where
  constructor MkDipeptide
  dipeptideName    : String
  dipeptideFormula : String
  carbonCount      : Nat
  hydrogenCount    : Nat
  nitrogenCount    : Nat
  oxygenCount      : Nat
  isHomochiral     : Bool
  chirality        : Chirality
```

#### 🏷️ Algebraic Data Types

```idris
data Chirality = LeftHanded | RightHanded | Achiral
```

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-compound-molecularbonding"></a>Module `Compound.MolecularBonding`

#### 📦 Records

```idris
record CovalentBond where
  constructor MkCovalentBond
  atom1 : Nat
  atom2 : Nat
  order : Nat

||| Converts a list of covalent bonds into a pure Maxel adjacency matrix.
```

```idris
record Molecule (numAtoms : Nat) where
  constructor MkMolecule
  formula     : String
  elements    : Vect numAtoms Element
  bondMatrix  : Maxel

||| Total valence requirement across all constituent atoms in the molecule.
```

```idris
record Coord3D where
  constructor MkCoord3D
  cx : BoxInt
  cy : BoxInt
  cz : BoxInt
```

```idris
record Molecule3D where
  constructor MkMolecule3D
  name  : String
  atoms : Boxel
  bonds : Maxel

||| 3D Conformation of Methane (CH4) centered at [1, 1, 1] on the discrete 3x3x3 grid:
||| - Carbon at [1, 1, 1] (Z=6)
||| - Hydrogen 1 at [2, 2, 2] (Z=1)
||| - Hydrogen 2 at [2, 0, 0] (Z=1)
||| - Hydrogen 3 at [0, 2, 0] (Z=1)
||| - Hydrogen 4 at [0, 0, 2] (Z=1)
```

#### 🏷️ Algebraic Data Types

```idris
data Element = Hydrogen | Carbon | Nitrogen | Oxygen
```

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-compound-plasmarecombination"></a>Module `Compound.PlasmaRecombination`

#### 📦 Records

```idris
record PlasmaCell where
  constructor MkPlasmaCell
  protons   : Nat
  electrons : Nat
```

```idris
record DecoupledGas where
  constructor MkDecoupledGas
  neutralAtoms     : Nat
  decoupledPhotons : Nat
  residualProtons  : Nat
  residualElectrons: Nat
```

#### 🏷️ Algebraic Data Types

```idris
data ParticleCharge = ProtonPositive | ElectronNegative | NeutralHydrogen
```

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-compound-stellarnucleosynthesis"></a>Module `Compound.StellarNucleosynthesis`

#### 📦 Records

```idris
record Carbon12Nucleus where
  constructor MkCarbon12Nucleus
  alphaCount  : Nat
  totalVoxels : Nat
  protons     : Nat
  neutrons    : Nat
```

#### 🏷️ Algebraic Data Types

```idris
data StellarElement =
    ElemH   -- Hydrogen (Z=1, Valence=1)
  | ElemHe  -- Helium (Z=2, Valence=0, Alpha Core)
  | ElemC   -- Carbon (Z=6, Valence=4, Triple-Alpha)
  | ElemN   -- Nitrogen (Z=7, Valence=3, CNO Cycle)
  | ElemO   -- Oxygen (Z=8, Valence=2, Alpha Capture on Carbon)
  | ElemNe  -- Neon (Z=10, Valence=0, Alpha Capture on Oxygen)
  | ElemMg  -- Magnesium (Z=12, Valence=2, Alpha Capture on Neon)
  | ElemSi  -- Silicon (Z=14, Valence=4, Alpha Capture on Magnesium)
  | ElemP   -- Phosphorus (Z=15, Valence=5, Polyphosphate Backbone)
  | ElemFe  -- Iron (Z=26, Valence=2, Silicon Burning Peak)
```

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-compound-symplecticintegrator"></a>Module `Compound.SymplecticIntegrator`

#### 📦 Records

```idris
record PhaseState where
  constructor MkPhaseState
  position : Vexel
  momentum : Vexel
```

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-compound-velocitylensing"></a>Module `Compound.VelocityLensing`

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-compound-watsoncrickbasepairing"></a>Module `Compound.WatsonCrickBasePairing`

#### 📦 Records

```idris
record ATPMolecule where
  constructor MkATPMolecule
  phosphateGroups : Nat -- 3 (Alpha, Beta, Gamma)
  phosphoAnhydrideBonds : Nat -- 2 high-energy P-O-P bonds

||| Canonical ATP ground state.
```

```idris
record HydrolysisResult where
  constructor MkHydrolysisResult
  adpPhosphates : Nat -- 2
  inorganicPhosphate : Nat -- 1
  energyTokensReleased : Nat -- Discrete thermodynamic drive (30 kJ/mol equivalent)

||| Executes ATP Hydrolysis: Cleaves 1 phosphoanhydride bond, releasing 1 Pi and energy.
```

#### 🏷️ Algebraic Data Types

```idris
data Nucleobase = Adenine | Thymine | Guanine | Cytosine | Uracil
```

[↑ Back to Top](#table-of-contents)

---

## <a id="section-6"></a>6. Elaborator Reflection & Invariant Macros

### <a id="mod-reflect-invariantauditor"></a>Module `Reflect.InvariantAuditor`

[↑ Back to Top](#table-of-contents)

---

### <a id="mod-reflect-permutationsolver"></a>Module `Reflect.PermutationSolver`

[↑ Back to Top](#table-of-contents)

---
