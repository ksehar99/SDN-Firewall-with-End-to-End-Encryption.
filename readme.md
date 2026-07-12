# SDN Firewall with End-to-End Encryption

A secure Software-Defined Networking (SDN) solution integrating a simulated enterprise network topology, a Ryu SDN controller with firewall policy enforcement, and a Zero Trust security layer with end-to-end encryption — built as a team project to demonstrate protection against common network attacks.

---

## My Contribution

This repository highlights my role as the **Security Layer Lead**. My work focused on:
- Designing and implementing hybrid encryption (RSA + Fernet) for secure data transmission
- Building a Zero Trust authentication system for host-to-host verification
- Adding intrusion detection and logging to the SDN controller
- Integrating the security module with the network topology and firewall controller built by teammates

---

## Tech Stack
`Python` `Mininet` `Ryu SDN Framework` `Cryptography (Fernet, RSA)` `Zero Trust Architecture`

---

## Architecture Overview

A simulated enterprise network connecting an HQ office and Branch office through a Cloud router, with security enforced at every hop:   
HQ Office (10.0.1.0/24) ↔ Cloud Router (10.0.100.0/24) ↔ Branch Office (10.0.2.0/24)   

Every host communicates only after mutual Zero Trust verification, with all traffic encrypted end-to-end.

---

## Key Security Features

- **Hybrid Encryption** — RSA-2048 for secure key exchange, Fernet (AES-128 + HMAC-SHA256) for fast, authenticated data encryption
- **Zero Trust Authentication** — Every connection requires signature-based identity verification before communication is allowed
- **Intrusion Detection** — Unverified hosts are automatically blocked and logged; plaintext traffic is flagged
- **SDN Integration** — Security checks embedded directly into the Ryu controller's packet-handling pipeline

---

## Results Summary

| Test | Result |
|---|---|
| Data Encryption/Decryption | ✅ Passed |
| Zero Trust Authentication | ✅ Passed |
| Cross-Site Encrypted Communication | ✅ Passed |
| MITM Attack Prevention | ✅ Passed |
| Unauthorized Access Blocking | ✅ Passed |

Average encryption latency: **~2.5ms per KB**, with under 10ms total overhead per packet — minimal performance impact for full end-to-end security.

---

## Quick Start

```bash
sudo bash run_secure_network.sh

# Inside Mininet CLI:
mininet> authenticate hqpc1 brpc1
mininet> encrypt hqpc1 brpc1 "hello"
```

---

## Full Technical Report

For detailed architecture diagrams, complete test results, CLI command reference, and implementation code, see the [Full Technical Report](report-document.md).

---

## Team

This project was completed as a group assignment, integrating three components:
- **Network Topology** — Mininet-based HQ/Branch/Cloud simulation
- **SDN Controller** — Ryu-based firewall with policy enforcement
- **Security Layer** — Encryption & Zero Trust authentication

