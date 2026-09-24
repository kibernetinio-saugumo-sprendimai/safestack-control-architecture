# SafeStack — Control Architecture

## Overview

SafeStack Control Architecture defines a structured, privacy-first technical control model covering routing logic, authenticated encryption boundaries, infrastructure trust design, and Zero-Trust identity separation.

It is an architectural framework designed for autonomous, verifiable systems operating under the SafeStack philosophy.

---

## Canonical Alignment & Governance

- **Ecosystem:** SafeStack Decentralized Security Framework
- **Root Canon Compliance:** [`safestack-canon`](https://github.com/kibernetinio-saugumo-sprendimai/safestack-canon) v1.0.0
- **Technical Canon Compliance:** [`safestack-technical-canon`](https://github.com/kibernetinio-saugumo-sprendimai/safestack-technical-canon) v1.0.0
- **Project Identity:** Registered as `project-006` in [`safestack-project-public-keys`](https://github.com/kibernetinio-saugumo-sprendimai/safestack-project-public-keys)
  - Public Key: `51ImThnp0+4SJPQg1gR87BS9/+hLhrsBSdLNlOna3ZM=`
  - Key Fingerprint: `SHA256:e91f92abe2e4ca9d4b65dd6c49e8230ff2d7266c0a6990d91e104628a89b6766`
- **Validation Status:** Registered in [`safestack-validation-registry`](https://github.com/kibernetinio-saugumo-sprendimai/safestack-validation-registry)

---

## Core Philosophy: The Layered Control Model

> **"Intention is allowed. Command is forbidden."**  
> *Security is layered discipline. Trust is established through verification, not authority.*

SafeStack divides systems into five explicit layers with strict boundaries:

### 1. Network Layer (Transport & Routing)
- Routing control at kernel level (`wg0`).
- Strict default gateway routing preventing DNS resolution leaks.
- Split-tunnel isolation preventing unauthorized side-channel egress.

### 2. Encryption Layer (Cryptographic Discipline)
- Authenticated encryption via ChaCha20-Poly1305.
- Ephemeral key exchange via Curve25519 (Noise IK Handshake pattern).
- Perfect Forward Secrecy (PFS) ensuring retrospective immunity against compromise.

### 3. Infrastructure Layer (Node Sovereignty)
- Infrastructure defines the physical boundary of trust.
- Self-hosted autonomous nodes eliminate centralized command-and-control (C2) risk.
- Absolute exclusion of connection metadata, IP mapping, and telemetry.

### 4. Application Layer (Entropy Containment)
- Application isolation: VPN encryption does not automatically sanitize browser entropy.
- Explicit mitigation of WebRTC IP leaks, canvas fingerprints, and timing side-channels.

### 5. Identity Layer (Zero-Trust Enforcement)
- Transport masking does not equal authentication anonymity.
- Local-first Zero-Trust policy engine ([`Safestack-Zero-Trust`](https://github.com/kibernetinio-saugumo-sprendimai/Safestack-Zero-Trust)) enforces default deny, posture checks, and cryptographic decision trails.

---

## The SafeStack Invariants

SafeStack architectures strictly enforce:
1. **No Central Command-and-Control:** Nodes act autonomously; no remote master key or remote kill-switch exists.
2. **Read-Only Observation:** The observer layer monitors node state without write or execution capabilities.
3. **Autonomy Severance:** In case of forced tampering or canonical violation, nodes sever trust locally and self-terminate rather than operate under compromise.

---

## Dossier Publication

The canonical web dossier is published at `index.html` and served via GitHub Pages.

---

## A Note to the Engineer

Maintain structural integrity.
Layer boundaries must remain explicit.
Design decisions must be documented.
Complexity must be justified.

Discipline is not optional.

---

## License

Licensed under the Creative Commons Attribution-NonCommercial 4.0 International ([CC BY-NC 4.0](LICENSE)).
