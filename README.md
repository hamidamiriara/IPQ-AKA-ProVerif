# IPQ-AKA ProVerif Models

This repository contains the ProVerif models used for the formal verification of the IPQ-AKA protocol.

## Verification Environment

- Tool: ProVerif 2.05
- Attacker Model: Dolev–Yao
- Equational Theory: XOR + KEM abstraction

## Claim Mapping

| Paper Claim | Security Property | File |
|-------------|-------------------|------|
| Claim 2 | Perfect Forward Secrecy (PFS) | claim2_PFS.pv |
| Claim 3 | Mutual Authentication | claim3_mutual_authentication.pv |
| Claim 4 | Replay Protection | claim4_replay_protection.pv |
| Claim 5 | MITM Resistance | claim5_MITM.pv |
| Claim 7 | Ephemeral Secret Leakage (ESL) Resistance | claim7_ESL.pv |
| Claim 8 | Unknown Key Share (UKS) Resistance | claim8_UKS.pv |
