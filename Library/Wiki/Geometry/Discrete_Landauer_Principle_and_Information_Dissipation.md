# Law 6: The Discrete Landauer Principle & Information Erasure Dissipation

## 1. Physical Principle & Constructive Foundation
In continuum thermodynamics and computation theory, Landauer's principle states that erasing $N_{\text{bits}}$ bits of information in a system coupled to a thermal bath at temperature $T$ must dissipate a minimum quantity of heat into the environment:
$$\Delta Q \ge N_{\text{bits}} \cdot k_B T \ln 2$$

In our constructivist multiset framework, information is stored as non-zero bit tokens within active computational memory registers (e.g. the $128$-slot Dark Energy ROM or $27$-slot Visible Matter lattice), while the thermodynamic heat bath is the **Parabolic Sector ($\det g = 0$, $55$ DM Green Sector)**.

---

## 2. Token Relocation & Exact QTT Conservation
Quantitative Type Theory (QTT) strictly forbids the destruction of physical information tokens (`(1 x : BoxInt)`). Therefore, "erasing" an informational bit does not vanish into the void; rather, it **relocates** active computational tokens into the append-only parabolic Dark Matter ledger (`dmLog`):

1. **Erasing $b$ Bits at Temperature Scale $T$**:
   $$\Delta Q_{\text{dissipated}} = b \cdot T$$
2. **Active Energy Decrease**:
   $$E_{\text{active}}(t+1) = E_{\text{active}}(t) - \Delta Q$$
3. **Parabolic Sink Residue Increase**:
   $$E_{\text{sink}}(t+1) = E_{\text{sink}}(t) + \Delta Q$$
4. **Global Total Conservation**:
   $$E_{\text{total}} = E_{\text{active}} + E_{\text{sink}} \equiv \text{constant}$$

---

## 3. Geometric Metric Partition & Irreversibility
- **Elliptic Sector ($\det g = +1$, $27$ VM)**: Active spatial computational cells undergoing state transitions.
- **Hyperbolic Sector ($\det g = -1$, $128$ DE)**: Archival bit registers tracking system state.
- **Parabolic Sector ($\det g = 0$, $55$ DM)**: Irreversible dissipation sink ($p_{\text{null}} = (0, 0)$) receiving the dissipated heat tokens.
- **Substrate Causal Arrow ($g_{22} = 0, g_{12} = 1$)**: Prevents retro-causal spontaneous recovery of dissipated tokens, enforcing monotonic thermodynamic entropy growth ($\Delta S_{\text{sink}} \ge 0$).
