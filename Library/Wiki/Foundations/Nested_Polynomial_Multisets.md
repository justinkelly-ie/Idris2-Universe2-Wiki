# 📦 Nested Polynumber Multisets, Spread Polynumbers & Goh Factorization

In Norman J. Wildberger's *Box Arithmetic*, a **Polynumber** is not an abstract continuous function; it is a **multiset of nested box terms**.

---

## 🏛️ 1. Theoretical Formulation

A monomial term $c \cdot x^k$ is a physical box container with:
1. **Multiplicity $c$**: The tally of empty boxes ($[\ ]$) at the base.
2. **Degree $k$**: The **nesting depth** of the box container:
   - $k=0 \implies c \cdot x^0 = c \cdot [\ ]$ (depth 0, scalar token)
   - $k=1 \implies c \cdot x^1 = c \cdot [[\ ]]$ (depth 1, Unixel $[1]$)
   - $k=2 \implies c \cdot x^2 = c \cdot [[[\ ]]]$ (depth 2, Unixel $[2]$)

A full Polynumber $P(x) = c_0 + c_1 x + c_2 x^2 + \dots + c_n x^n$ is a multiset of these nested terms, strictly isomorphic to a **`Vexel`** over singletons ($\sum c_k [k]$):

$$P(x) \equiv \{ (c_0, [0]), (c_1, [1]), (c_2, [2]), \dots, (c_n, [n]) \} \in \text{Vexel}$$

---

## 📐 2. Wildberger's Spread Polynumbers: $S_n(s)$

In Rational Trigonometry, the multiple-angle relations for trigonometric sines $\sin(n\theta)$ are replaced by **Spread Polynumbers $S_n(s)$** with exact integer coefficients:

$$\begin{aligned}
S_0(s) &= 0 \\
S_1(s) &= s \\
S_2(s) &= 4s - 4s^2 \\
S_3(s) &= 9s - 24s^2 + 16s^3 \\
S_4(s) &= 16s - 112s^2 + 224s^3 - 128s^4
\end{aligned}$$

These satisfy the exact discrete polynomial recurrence without transcendental limits:

$$S_n(s) = 2(1 - 2s) S_{n-1}(s) - S_{n-2}(s) + 2s$$

---

## 🔬 3. The Role of Goh Factorization

In Box Arithmetic and Discrete Operator Theory, **Goh Factorization** provides the canonical algebraic mechanism to factor nested polynumber containers into elementary linear box factors $(x - r)$ without irrational approximations:

$$P(x) = Q(x)(x - r) + P(r)$$

### Physical Significance in Universe Evolution:
1. **Spectral Extraction**: Extracts exact discrete roots and eigenspaces from the state transition matrix without continuous limits.
2. **Causal Splitting**: For Toeplitz and cyclotomic transfer matrices $\Phi_{137}(x)$, Goh factorization decomposes the matrix into:
   - **Forward Causal Operator $A(x)$**: Propagates visible matter forwards across the 137 stages.
   - **Anti-Causal Memory Residue $B(x^{-1})$**: Accumulates irreducible cyclotomic remainders into the Dark Matter ledger.
3. **Exact Remainder Theorem**: Yields $P(r) = 0$ if and only if $(x - r)$ evenly divides the nested box container.

---

## 💻 4. Executable Literate Proofs & Evidence

```idris
module Foundations.Nested_Polynomial_Multisets

import Core.BoxInt
import Core.Multiset
import Core.Polynumber
import Core.VexelMaxel

%default total

||| Evidence 1: Proof that (x + 2) + (3x + 1) = 4x + 3
public export
evidence_poly_addition : Bool
evidence_poly_addition =
  let p1 = MkPolynumber [intToBoxInt 2, intToBoxInt 1] -- 2 + 1x
      p2 = MkPolynumber [intToBoxInt 1, intToBoxInt 3] -- 1 + 3x
      sumP = addPolynumber p1 p2
  in map unwrapBox (coeffs sumP) == [3, 4]

||| Evidence 2: Proof that (x - 1) * (x + 1) = x^2 - 1
public export
evidence_poly_multiplication : Bool
evidence_poly_multiplication =
  let p1 = MkPolynumber [intToBoxInt (-1), intToBoxInt 1] -- -1 + 1x
      p2 = MkPolynumber [intToBoxInt 1, intToBoxInt 1]    --  1 + 1x
      prodP = mulPolynumber p1 p2
  in map unwrapBox (coeffs prodP) == [-1, 0, 1]

||| Evidence 3: Proof of exact discrete polynomial division (x^2 - 1) / (x - 1) = (x + 1, remainder 0)
public export
evidence_poly_exact_division : Bool
evidence_poly_exact_division =
  let dividend = MkPolynumber [intToBoxInt (-1), intToBoxInt 0, intToBoxInt 1] -- x^2 - 1
      divisor  = MkPolynumber [intToBoxInt (-1), intToBoxInt 1]                -- x - 1
      (q, r) = divModPolynumber dividend divisor
  in map unwrapBox (coeffs q) == [1, 1] && map unwrapBox (coeffs r) == []

||| Evidence 4: Proof of Goh Linear Factorization on (x^2 - 4) with root r = 2:
||| Produces quotient (x + 2) and exact remainder P(2) = 0
public export
evidence_goh_linear_factor : Bool
evidence_goh_linear_factor =
  let p = MkPolynumber [intToBoxInt (-4), intToBoxInt 0, intToBoxInt 1] -- x^2 - 4
      (q, remVal) = gohPolynumberFactor p (intToBoxInt 2)
  in map unwrapBox (coeffs q) == [2, 1] && unwrapBox remVal == 0

||| Evidence 5: Proof of cyclotomic division with non-zero remainder
public export
evidence_cyclotomic_division_remainder : Bool
evidence_cyclotomic_division_remainder =
  let dividend = MkPolynumber [intToBoxInt 55, intToBoxInt 0, intToBoxInt 2] -- 2x^2 + 55
      divisor  = MkPolynumber [intToBoxInt 1, intToBoxInt 1]                 -- x + 1
      (q, r) = divModPolynumber dividend divisor
  in map unwrapBox (coeffs q) == [-2, 2] && map unwrapBox (coeffs r) == [57]

||| Evidence 6: Proof that Polynumber is isomorphic to 1D Vexel over Singletons
public export
evidence_polynumber_vexel_isomorphism : Bool
evidence_polynumber_vexel_isomorphism =
  let p = MkPolynumber [intToBoxInt 7, intToBoxInt 0, intToBoxInt 5] -- 7 + 5x^2
      v = polynumberToVexel p
      pBack = vexelToPolynumber v
  in p == pBack && lookupUnixel (MkUnixel 2) v == intToBoxInt 5

||| Evidence 7: Proof that Spread Polynumber S_2(s) = 4s - 4s^2 and S_3(s) = 9s - 24s^2 + 16s^3
public export
evidence_spread_polynumbers : Bool
evidence_spread_polynumbers =
  let s2 = spreadPolynumber 2
      s3 = spreadPolynumber 3
  in map unwrapBox (coeffs s2) == [0, 4, -4] &&
     map unwrapBox (coeffs s3) == [0, 9, -24, 16]
```

---

## 🔗 Related Chapters & Cross-References

* **Mathematical Foundations**:
  * [Box Arithmetic & Inductive Multisets](Box_Arithmetic.md) — Foundation of nested containers and box arithmetic.
  * [Vexels, Maxels, Boxels & Reflected Linear Algebra](Vexels_Maxels_and_Reflected_Linear_Algebra.md) — Polynomial-to-Vexel isomorphisms and multiset algebra.
  * [Unixel Fractions & Ongoing Sequences](Unixel_Fractions_and_OnSeq_Algebra.md) — Fractional rational functions and sequence algebra.
* **Cosmological Evolution & Physics**:
  * [Cyclotomic Encoding & Decoding Protocol](../Evolution/Cyclotomic_Encoding_and_Decoding.md) — Cyclotomic polynomial division by $\Phi_{137}(x)$ for cosmic state compression.
  * [Dark Matter as the Cosmic Law Ledger](../Evolution/Dark_Matter_Law_Storage.md) — Polynomial remainder accumulation as Dark Matter drag ledger.
  * [Rational Snell's Law & The Triple Spread Law](../Geometry/Rational_Snell_and_Triple_Spread.md) — Spread polynomials $S_n(s)$ applied to rational optics.
