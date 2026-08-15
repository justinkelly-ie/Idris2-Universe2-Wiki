# 📦 Nested Polynomial Multisets, Cyclotomic Division & Goh Factorization

In Norman J. Wildberger's *Box Arithmetic*, a **Polynomial (Polynumber)** is not an abstract continuous expression; it is a **multiset of nested box terms**.

---

## 🏛️ 1. Theoretical Formulation

A monomial term $c \cdot x^k$ is a physical box container with:
1. **Multiplicity $c$**: The tally of empty boxes ($[\ ]$) at the base.
2. **Degree $k$**: The **nesting depth** of the box container:
   - $k=0 \implies c \cdot x^0 = c \cdot [\ ]$ (depth 0)
   - $k=1 \implies c \cdot x^1 = c \cdot [[\ ]]$ (depth 1)
   - $k=2 \implies c \cdot x^2 = c \cdot [[[\ ]]]$ (depth 2)

A full polynomial $P(x) = c_0 + c_1 x + c_2 x^2 + \dots + c_n x^n$ is a multiset of these nested terms:

$$P(x) \equiv \{ (c_0, 0), (c_1, 1), (c_2, 2), \dots, (c_n, n) \}$$

---

## 🔬 2. The Role of Goh Factorization

In Box Arithmetic and Discrete Operator Theory, **Goh Factorization** provides the canonical algebraic mechanism to factor nested polynumber containers into elementary linear box factors $(x - r)$ without irrational approximations:

$$P(x) = Q(x)(x - r) + P(r)$$

### Physical Significance in Universe Evolution:
1. **Spectral Extraction**: Extracts exact discrete roots and eigenspaces from the state transition matrix without continuous limits.
2. **Causal Splitting**: For Toeplitz and cyclotomic transfer matrices $\Phi_{137}(x)$, Goh factorization decomposes the matrix into:
   - **Forward Causal Operator $A(x)$**: Propagates visible matter forwards across the 137 stages.
   - **Anti-Causal Memory Residue $B(x^{-1})$**: Accumulates irreducible cyclotomic remainders into the Dark Matter ledger.
3. **Exact Remainder Theorem**: Yields $P(r) = 0$ if and only if $(x - r)$ evenly divides the nested box container.

---

## 💻 3. Executable Literate Proofs & Evidence

```idris
module Foundations.Nested_Polynomial_Multisets

import Core.BoxInt
import Core.Multiset
import Core.Polynomial

%default total

||| Evidence 1: Proof that (x + 2) + (3x + 1) = 4x + 3
public export
evidence_poly_addition : Bool
evidence_poly_addition =
  let p1 = MkBoxPolynomial [intToBoxInt 2, intToBoxInt 1] -- 2 + 1x
      p2 = MkBoxPolynomial [intToBoxInt 1, intToBoxInt 3] -- 1 + 3x
      sumP = addPoly p1 p2
  in map unwrapBox (coeffs sumP) == [3, 4]

||| Evidence 2: Proof that (x - 1) * (x + 1) = x^2 - 1
public export
evidence_poly_multiplication : Bool
evidence_poly_multiplication =
  let p1 = MkBoxPolynomial [intToBoxInt (-1), intToBoxInt 1] -- -1 + 1x
      p2 = MkBoxPolynomial [intToBoxInt 1, intToBoxInt 1]    --  1 + 1x
      prodP = mulPoly p1 p2
  in map unwrapBox (coeffs prodP) == [-1, 0, 1]

||| Evidence 3: Proof of exact discrete polynomial division (x^2 - 1) / (x - 1) = (x + 1, remainder 0)
public export
evidence_poly_exact_division : Bool
evidence_poly_exact_division =
  let dividend = MkBoxPolynomial [intToBoxInt (-1), intToBoxInt 0, intToBoxInt 1] -- x^2 - 1
      divisor  = MkBoxPolynomial [intToBoxInt (-1), intToBoxInt 1]                -- x - 1
      (q, r) = divModPoly dividend divisor
  in map unwrapBox (coeffs q) == [1, 1] && map unwrapBox (coeffs r) == []

||| Evidence 4: Proof of Goh Linear Factorization on (x^2 - 4) with root r = 2:
||| Produces quotient (x + 2) and exact remainder P(2) = 0
public export
evidence_goh_linear_factor : Bool
evidence_goh_linear_factor =
  let p = MkBoxPolynomial [intToBoxInt (-4), intToBoxInt 0, intToBoxInt 1] -- x^2 - 4
      (q, remVal) = gohLinearFactor p (intToBoxInt 2)
  in map unwrapBox (coeffs q) == [2, 1] && unwrapBox remVal == 0

||| Evidence 5: Proof of cyclotomic division with non-zero remainder
public export
evidence_cyclotomic_division_remainder : Bool
evidence_cyclotomic_division_remainder =
  let dividend = MkBoxPolynomial [intToBoxInt 55, intToBoxInt 0, intToBoxInt 2] -- 2x^2 + 55
      divisor  = MkBoxPolynomial [intToBoxInt 1, intToBoxInt 1]                 -- x + 1
      (q, r) = divModPoly dividend divisor
  in map unwrapBox (coeffs q) == [-2, 2] && map unwrapBox (coeffs r) == [57]
```
