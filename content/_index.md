---
title: Welcome to LibreKeys documentation
geekdocNav: true
geekdocAlign: center
geekdocAnchor: false
---

<!-- markdownlint-capture -->
<!-- markdownlint-disable MD033 -->

<!-- markdownlint-restore -->


The LibreKeys project is developing a cross‑platform configuration application that lets users manage security key devices, credentials, policies, and firmware updates through a clear graphical interface. The goal of the app is to expose advanced features (such as multiple profiles, PIN and touch policies, backup/restore flows, and diagnostics) without sacrificing simplicity, so both newcomers and experts can safely operate their security devices.

LibreKeys is also maintaining community‑driven and fully FOSS forks of the PicoKeys firmwares, unifying them into a coherent, fully open source suite for hardware security keys. We aim to modernize and extend the HSM, FIDO2, and OpenPGP capabilities, while keeping the codebase auditable, modular, and easy to adapt to new microcontrollers and use cases.

The entire effort is run in a transparent, community‑oriented way: open governance (design discussions in public), contributor‑friendly documentation, and automated testing and reproducible builds to strengthen trust. Over time, the project could define open standards for interoperability between different devices and toolchains, becoming a reference platform for hobbyists, researchers, and organizations that want vendor‑neutral, privacy‑respecting security keys.


{{< button size="large" relref="overview/getting-started/" >}}Getting Started{{< /button >}}

## Feature overview

{{< columns >}}

### FIDO2

Personal FIDO2 passkey for secure passwordless logins, letting you register and authenticate credentials with online services using FIDO2 and WebAuthn standard. The FIDO2 feature also allows storing ssh keys on your security device

<--->

### PGP

OpenPGP‑compatible smartcard implementation so you can keep PGP keys on a dedicated device for secure email, signing, and encryption operations via GnuPG and similar tools.

<--->

### HSM

Build a compact hardware security module that can generate, store, and use many private and secret keys for encryption, decryption, and digital signatures designed to integrate with common cryptographic tools and public key infrastructures for managing secure communications.


{{< /columns >}}
