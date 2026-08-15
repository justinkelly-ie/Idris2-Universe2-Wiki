# 🌀 Nilpotent Infinitesimal Calculus & Dual Numbers

Continuous calculus relies on non-constructive limit processes ($\lim_{\Delta x \to 0}$). In **Idris2-Universe2**, exact differentiation is achieved via the **nilpotent matrix unit** $\epsilon = \begin{pmatrix}0&1\\0&0\end{pmatrix}$ where $\epsilon^2 = 0$.

---

## 🏛️ 1. The Nilpotent Matrix Algebra

$$\epsilon = \begin{pmatrix}0&1\\0&0\end{pmatrix} \implies \epsilon^2 = \begin{pmatrix}0&1\\0&0\end{pmatrix}\begin{pmatrix}0&1\\0&0\end{pmatrix} = \begin{pmatrix}0&0\\0&0\end{pmatrix} = 0$$

A **Dual Complex Number** $z = a + b\epsilon$ allows evaluating discrete Taylor series to exact first order without error:

$$f(x + \epsilon) = f(x) + f'(x)\epsilon$$

---

## 💻 2. Executable Literate Proofs & Evidence

```idris
module Foundations.Nilpotent_Infinitesimals

import Core.BoxInt
import Math.Infinitesimal

%default total

||| Evidence 1: Proof that epsilon squared vanishes identically
public export
evidence_epsilon_nilpotence : unwrapBox (mulEpsilon Math.Infinitesimal.epsilon Math.Infinitesimal.epsilon) = 0
evidence_epsilon_nilpotence = Refl

||| Evidence 2: Proof that dual complex multiplication (3 + 1ε) * (2 + 0ε) = 6 + 2ε
public export
evidence_dual_multiplication : 
  let d1 = MkDual (intToBoxInt 3) (intToBoxInt 1)
      d2 = MkDual (intToBoxInt 2) (intToBoxInt 0)
      prod = d1 * d2
  in (unwrapBox (realPart prod) = 6, unwrapBox (epsPart prod) = 2)
evidence_dual_multiplication = (Refl, Refl)
```
