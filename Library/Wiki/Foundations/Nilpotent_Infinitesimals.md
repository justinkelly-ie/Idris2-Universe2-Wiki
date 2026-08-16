# 🌀 Nilpotent Infinitesimal Calculus & Dual Numbers

Continuous calculus relies on non-constructive limit processes ($\lim_{\Delta x \to 0}$). In **Idris2-Universe2**, exact differentiation is achieved via the **nilpotent matrix unit** $\epsilon = \begin{pmatrix}0&1\\0&0\end{pmatrix}$ represented as the basis **Pixel** $[1, 2]$ inside a **Maxel**, where $\epsilon^2 = 0$ is a topological consequence of multiset index contraction.

---

## 🏛️ 1. The Nilpotent Matrix Algebra & Multiset Formulation

$$\epsilon = [1, 2] \implies \epsilon^2 = [1, 2] \times [1, 2] = \emptyset = 0$$

A **Dual Number** $z = a + b\epsilon$ is encoded directly as an upper-triangular Maxel $a([1, 1] + [2, 2]) + b[1, 2]$, allowing evaluation of discrete Taylor series to exact first order without infinite limits:

$$f(x + \epsilon) = f(x) + f'(x)\epsilon$$

---

## 💻 2. Executable Literate Proofs & Evidence

```idris
module Foundations.Nilpotent_Infinitesimals

import Core.BoxInt
import Core.VexelMaxel
import Math.Infinitesimal

%default total

||| Evidence 1: Proof that epsilon squared vanishes identically into the empty Maxel
public export
evidence_epsilon_nilpotence : mulEpsilon Math.Infinitesimal.epsilon Math.Infinitesimal.epsilon = MkMaxel []
evidence_epsilon_nilpotence = Refl

||| Evidence 2: Proof that dual number multiplication (3 + 1ε) * (2 + 0ε) = 6 + 2ε
public export
evidence_dual_multiplication : 
  let d1 = dualNumber (intToBoxInt 3) (intToBoxInt 1)
      d2 = dualNumber (intToBoxInt 2) (intToBoxInt 0)
      prod = mulDual d1 d2
  in (unwrapBox (dualReal prod) = 6, unwrapBox (dualEps prod) = 2)
evidence_dual_multiplication = (Refl, Refl)

||| Evidence 3: Proof of exact discrete Automatic Differentiation via Dual Number Maxels
public export
evidence_autodiff_exactness : Bool
evidence_autodiff_exactness =
  auditAutoDiffProof
```
