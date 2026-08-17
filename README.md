# 📚 Idris2-Universe2-Wiki

**Literate Documentation, Formal Specifications, and Property Verification Suite for [Idris2-Universe2](https://github.com/justinkelly-ie/Idris2-Universe2).**

[![Idris2](https://img.shields.io/badge/Idris2-Verified_Wiki-blue.svg)](https://github.com/idris-lang/Idris2)
[![Macro Audits](https://img.shields.io/badge/Elaborator_Macros-50_Verified-brightgreen.svg)]()
[![Tests](https://img.shields.io/badge/Runtime_Tests-100_Passed-success.svg)]()
[![Literate Chapters](https://img.shields.io/badge/Literate_Chapters-96_Compiled-purple.svg)]()

---

## 📖 Introduction

`Idris2-Universe2-Wiki` is the executable literate knowledge base for `Idris2-Universe2`. The codebase formalizes physical and geometric laws in constructive discrete mathematics using Idris 2's Quantitative Type Theory (QTT) and Elaborator Reflection macros (`%macro`).

All physical invariants, conservation theorems, and geometric classifications are verified at compile time without floating-point approximations or continuous infinities.

### 🗺️ Quick Reference & Catalogs
* **[The Universal Rosetta Stone](Library/Wiki/Foundations/Universal_Rosetta_Stone.md)** — Comparative mapping across Finite Mathematics, Cosmological Physics, and Idris 2 QTT.
* **[The Emergent Physical Laws & Academic Bibliography](Library/Wiki/Verification/Physical_Laws_Bibliography_and_Sources.md)** — Verified citations, DOIs, and primary literature for all emergent physical laws (Laws 1–18).
* **[Type Signatures & API Catalog](Library/Wiki/Verification/Type_Signatures_and_API_Catalog.md)** — Dynamically generated, authoritative index of all records, data types, and primary state transitions.

---

## 🧭 Documentation Sections

The documentation is organized into 5 thematic sections:

### [1. Foundational Mathematics & Discrete Calculus](Library/Wiki/Foundations/Index.md)
Axiomatic box arithmetic, signed integers as difference pairs (Pixels), nilpotent dual numbers, multiset algebras, and quantum measurement foundations.

### [2. Spacetime & Geometry](Library/Wiki/Geometry/Index.md)
The 4 fundamental geometries, the emergent physical laws (Laws 1–18), Grassmann cochain exterior calculus, Yang-Mills gauge theories, macromolecular bonding, and non-equilibrium thermodynamics.

### [3. Evolutionary Dynamics & Law Encoding](Library/Wiki/Evolution/Index.md)
Pre-geometric genesis, dark matter law accumulation, cyclotomic polynomial division, linear QTT state pipelines, and cyclic cosmological expansion.

### [4. Kinematics & Astrodynamics](Library/Wiki/Kinematics/Index.md)
Symplectic leapfrog integrators, discrete Noether momentum invariants, toroidal N-body dynamics, rational Kepler orbital mechanics, and asymptotic galactic rotation curves.

### [5. Metatheory & Verification](Library/Wiki/Verification/Index.md)
Comprehensive verification matrix, [Physical Laws Bibliography](Library/Wiki/Verification/Physical_Laws_Bibliography_and_Sources.md), structural associativity proofs, cosmological inferences, elaborator reflection audit logs, and the complete [Type Signatures & API Catalog](Library/Wiki/Verification/Type_Signatures_and_API_Catalog.md).

---

## 🛠️ Building & Verifying

To build the entire documentation suite and execute all 96 runtime invariant audits:

```bash
# Build documentation executable with pack
pack build Idris2-Universe2-Wiki.ipkg

# Run verification suite
./build/exec/universe2-verify

# Regenerate dynamic Type Signatures & API Catalog
python3 Scripts/generate_type_catalog.py
```
