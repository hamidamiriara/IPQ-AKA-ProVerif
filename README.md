# IPQ-AKA: Formal Verification Models (ProVerif)

This repository contains the formal ProVerif models used to verify the security properties of the **IPQ-AKA (Improved Post-Quantum Authentication and Key Agreement)** protocol.

The models support the security analysis presented in the corresponding research paper and are provided to ensure transparency, reproducibility, and independent verification of the results.

---

## Overview

IPQ-AKA is a post-quantum–enhanced Authentication and Key Agreement protocol designed for next-generation (5G-Advanced / 6G) mobile networks. The protocol integrates:

- Post-Quantum Key Encapsulation Mechanism (KEM)
- Ephemeral session key derivation
- SUCI concealment enhancement
- Perfect Forward Secrecy (PFS)
- Resistance against advanced active and passive attacks

This repository contains one ProVerif model per formal security claim.

---

## Verification Environment

- Tool: ProVerif 2.05
- Attacker Model: Dolev–Yao
- Cryptographic Abstractions:
  - XOR equational theory
  - Abstracted KEM encapsulation/decapsulation
  - Symbolic KDF modeling
- Verification Method: Automatic resolution

---

## Claim Mapping

| Paper Claim | Security Property | File |
|-------------|-------------------|------|
| Claim 2 | Perfect Forward Secrecy (PFS) | claim2_PFS.pv |
| Claim 3 | Mutual Authentication | claim3_mutual_authentication.pv |
| Claim 4 | Replay Protection | claim4_replay_protection.pv |
| Claim 5 | MITM Resistance | claim5_MITM.pv |
| Claim 7 | Ephemeral Secret Leakage (ESL) Resistance | claim7_ESL.pv |
| Claim 8 | Unknown Key Share (UKS) Resistance | claim8_UKS.pv |


Each model is self-contained and includes detailed comments mapping the formal verification to the corresponding section of the manuscript.

---

## How to Run the Models
Ensure ProVerif 2.05 is installed.

Run:
proverif claim2_PFS.pv

or on Windows:
proverif.exe claim2_PFS.pv

The output will indicate whether the specified secrecy or correspondence queries are satisfied.

---

**"IPQ-AKA: A Post-Quantum Secure Authentication and Key Agreement Protocol"**
(In preparation)

---

## Modeling Assumptions

- Symbolic Dolev–Yao adversary with full network control
- Perfect cryptography assumption
- KEM abstracted at symbolic level (not computational proof)

These models provide symbolic security guarantees and do not replace computational security proofs.

---

## License

Released under the MIT License for academic and research use.

---

## Reproducibility & Citation

If you use or reference these models, please cite the corresponding paper.
