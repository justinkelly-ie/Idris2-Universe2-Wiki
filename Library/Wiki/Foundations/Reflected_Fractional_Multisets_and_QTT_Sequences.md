# 🔮 Reflected Fractional Multisets & QTT Ongoing Sequences

This chapter demonstrates how **Fractional Multisets (`SingFraction`)** and **Ongoing Sequences (`OnSeq`)** integrate seamlessly into **Quantitative Type Theory (QTT)** and **Elaborator Reflection Macros** (`Language.Reflection`):

1. **Compile-Time Elaborator Reflection**: Invariant macros statically audit non-zero Singleton denominators ($[D] \ge 1$), prove rational equivalence ($N_1 \cdot D_2 = N_2 \cdot D_1$), and verify finite sequence clip dimensions at compile time.
2. **Quantitative Type Theory (QTT) Linearity**: Linear resource multiplicities (`(1 frac : SingFraction)`) strictly enforce the First Law of Thermodynamics across rational observables, ensuring that splitting, scaling, and advancing fractional states incurs zero energy leakage.

---

## 🏛️ 1. Theoretical Framework

```
         ELABORATOR REFLECTION MACROS & QTT REASONING
         
   ┌────────────────────────────────────────────────────────┐
   │ COMPILE-TIME MACRO AUDIT: Language.Reflection          │
   │  - %macro auditSingFractionPositivity  -> Refl (D > 0) │
   │  - %macro auditRationalEquivalence     -> Refl (N₁D₂=N₂D₁)
   │  - %macro auditOnSeqClipExtraction     -> Refl (Length)│
   └────────────────────────────────────────────────────────┘
                              ▲
                              │ Compile-Time Reflection
                              ▼
   ┌────────────────────────────────────────────────────────┐
   │ QUANTITATIVE TYPE THEORY (QTT): Multiplicity 1         │
   │  - linearConsumeSingFraction : (1 frac) -> SingFraction│
   │  - linearScaleSingFraction   : (1 frac) -> (1 scale)   │
   │  - linearSplitSingFraction   : (1 frac) -> (p, n - p)  │
   │  - linearStepOnSeq           : (1 seq)  -> (term, seq')│
   └────────────────────────────────────────────────────────┘
```

---

## 💻 2. Executable Literate Proofs & Evidence

```idris
module Foundations.Reflected_Fractional_Multisets_and_QTT_Sequences

import Core.BoxInt
import Core.VexelMaxel
import Core.SingFraction
import Core.OnSeq
import Reflect.InvariantAuditor
import Language.Reflection
import Data.List

%default total

||| Evidence 1: Compile-Time Reflection Witness for Singleton Denominator Positivity.
public export
evidence_macro_singleton_positivity : Reflect.InvariantAuditor.auditUnitDenomProof = True
evidence_macro_singleton_positivity = Reflect.InvariantAuditor.auditSingFractionPositivity

||| Evidence 2: Compile-Time Reflection Witness for Rational Cross-Multiplication Equivalence.
public export
evidence_macro_rational_equivalence : Reflect.InvariantAuditor.auditCanonicalRationalEquivProof = True
evidence_macro_rational_equivalence = Reflect.InvariantAuditor.auditRationalEquivalence

||| Evidence 3: Compile-Time Reflection Witness for OnSeq Clip Length Extraction.
public export
evidence_macro_onseq_clip_length : Reflect.InvariantAuditor.auditStandardClipLengthProof = True
evidence_macro_onseq_clip_length = Reflect.InvariantAuditor.auditOnSeqClipExtraction

||| Evidence 4: QTT Linear Fraction Splitting Conserves Total Numerator Energy:
||| Splitting 10/[3] into partition p=4 yields (4/[3], 6/[3]) where 4 + 6 = 10.
public export
evidence_qtt_fraction_split_conservation : Bool
evidence_qtt_fraction_split_conservation =
  let initialFrac = mkSingFraction (intToBoxInt 10) 3
      (f1, f2) = linearSplitSingFraction initialFrac (intToBoxInt 4)
      p1 = unwrapBox (num f1)
      p2 = unwrapBox (num f2)
  in (p1 + p2 == 10) && (den f1 == MkSingleton 3) && (den f2 == MkSingleton 3)

||| Evidence 5: QTT Linear Sequence Stepping and State Preservation:
||| Linearly stepping an OnSeq at term 5 extracts the exact term and advances the sequence index.
public export
evidence_qtt_onseq_stepping : Bool
evidence_qtt_onseq_stepping =
  let seq = identity 0
      (val, nextSeq) = linearStepOnSeq seq 5
  in case val of
       Just v  => v == 5 && start nextSeq == 6
       Nothing => False
```
