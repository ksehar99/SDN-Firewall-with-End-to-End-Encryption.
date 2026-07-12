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
men eus repo k naam ki repo bna li thi, can i import in that repo? ya new hi bnani hogi?Weighed repo conflict and deliberated between deletion or renamingWeighed repo conflict and deliberated between deletion or renamingAchi baat pooch li — GitHub ka Import tool sirf naya repo bana kar hi import karta hai, ye kisi existing/already-bani-hui repo mein import nahi karta. Agar tumne pehle se ussi naam ki empty repo bana rakhi hai, to Import karte waqt conflict ho sakta hai (kyunke wo naam already tumhare account mein use ho chuka hai).
Do options hain:
Option 1: Purani empty repo delete kar do, phir import karo (Recommended)

Jo empty repo tumne bana rakhi hai, usay delete kar do:

Us repo mein jao → Settings → sabse neeche scroll karo → "Delete this repository"
Confirm karne ke liye repo ka naam type karna hoga


Delete hone ke baad, Import repository feature use karo (jo maine bataya tha), aur same naam de do naye import ke waqt — ab conflict nahi hoga

Option 2: Import ko thoda different naam se karo
Agar purani empty repo delete nahi karni (kisi wajah se), to import karte waqt naya/thoda different naam de do (jaise network-security-sdn instead of jo pehle wala naam tha).

Meri recommendation: Option 1 behtar hai — purani empty repo ko delete kar do (usme kuch nahi hai to koi loss nahi), phir clean import karo same naam ke saath. Zyada organized rahega.
Purani empty repo delete karne mein koi hesitation ho (jaise usme koi settings already ki hain), bata dena, warna seedha delete kar ke import step pe chalte hain.README (10).mdmdtheek ab innki readme ko update krne ka time..
iska btao, how is it.. what should be done more..Identified missing file content; requested direct paste for reviewIdentified missing file content; requested direct paste for reviewLagta hai is baar file ka actual content mere paas context mein nahi aaya — sirf upload ka reference dikh raha hai, text visible nahi hai. Pehle jaisa tumne paste kiya tha (copy-paste text), waisa is README (10) ka content bhi paste kar do please, taake main dekh ke review kar sakun.README (10).mdmdab?Deciphered project role clarification through documentation reviewDeciphered project role clarification through documentation reviewYe README bohot detailed aur technically impressive hai — actually is se ek achi cheez clear ho gayi: is document se pata chal raha hai tumhara specific role Member 3 tha — Security Layer (Encryption + Zero Trust authentication), jo humne pehle "yaad nahi" bola tha uska jawab mil gaya!
Ye README bohot strong hai overall. Kuch observations aur improvements:
Achha kya hai:

Extremely thorough — architecture diagrams, code snippets, test results, performance metrics sab kuch hai
Testing results table (MITM prevention, encryption tests) — ye bohot impressive hai, real security validation dikhata hai
Clear separation of team members ka kaam

Improvements chahiye:

Bohot lamba hai for GitHub README — 464 lines ka report, ye ek academic project report jaisa lagta hai, GitHub README jaisa nahi. GitHub README zyada scannable/concise hona chahiye, poora technical report nahi. Suggestion: Isay do documents mein split karo:

README.md — Short, clean overview (Overview, Architecture diagram, Key Features, How to Run, Results summary, Team)
docs/full-report.md ya docs/technical-report.pdf — Ye poora detailed report yahan move kar do, README mein sirf link do: "📄 Full Technical Report"


Broken numbering — Section 8 mein "8.1 Core Files" hai but "8.4 Utilities" seedha aata hai (8.2, 8.3 missing), aur items 9, 10, 12 numbered hain lekin 3-8 gayab hain files list mein. Fix karo ya simplify kar do.
Missing: Tech stack summary at top — Turant pata nahi chalta kis language/framework mein bana hai jab tak neeche na pahonchо. Top pe ek "Tech Stack" line add karo: Python, Mininet, Ryu SDN, Cryptography library
"Awaiting Evaluation" — Ye line hata do ya update karo agar grade mil chuka hai, warna ye "abhi tak assess nahi hua" wala unfinished feel deta hai.
Missing: Your specific contribution highlighted clearly — Chunki ye README poore team ka combined kaam dikhata hai, apna naam/role top pe ya alag se clearly likho:

My Contribution: Security Layer implementation (Section 2-4) — encryption, Zero Trust authentication, and intrusion detection logic.




Sabse important suggestion: GitHub README ko short aur clean rakho (Overview + Architecture + Features + How to run + link to full report), aur ye detailed report ko separate file mein daal do. Ye zyada professional lagega aur recruiters/clients turant scan kar sakenge bina overwhelm hue.
Chahogi to main short version ka README draft bana du (jo top pe show hoga), aur ye poora content "full report" ke taur pe reference ho?theek hia, readme btao phr bna k kia honi chhiye iski, kesi honi chhaiye.. bna k do, bs text, i'll pasteArchitected professional README highlighting security layer contributionsArchitected professional README highlighting security layer contributionsYahan clean, concise README hai — poora technical detail full report mein reference kiya hai:
markdown# SDN Firewall with End-to-End Encryption

A secure Software-Defined Networking (SDN) solution integrating a simulated enterprise network topology, a Ryu SDN controller with firewall policy enforcement, and a Zero Trust security layer with end-to-end encryption — built as a team project to demonstrate protection against common network attacks.

---

## My Contribution

This repository highlights my role as the **Security Layer Lead** on a 3-member team. My work focused on:
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
mininet> secstats
```

---

## Full Technical Report

For detailed architecture diagrams, complete test results, CLI command reference, and implementation code, see the [Full Technical Report](https://github.com/ksehar99/SDN-Firewall-with-End-to-End-Encryption./blob/main/report-document.md)

---

## Team

This project was completed as a group assignment, integrating three components:
- **Network Topology** — Mininet-based HQ/Branch/Cloud simulation
- **SDN Controller** — Ryu-based firewall with policy enforcement
- **Security Layer** — Encryption & Zero Trust authentication *(my contribution)*
