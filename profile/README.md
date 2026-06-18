<div align="center">
  <img src="https://github.com/lqxp.png" width="96" height="96" style="border-radius: 50%;" alt="lqxp logo" />

  <br />

  <img src="https://qxch.at/image.png" alt="QxProtocol Banner" width="100%" />

  <br /><br />

  # light qxp protocol

  **A lightweight, end-to-end encrypted messaging network built for privacy.**

  [![MIT-0 License](https://img.shields.io/badge/license-MIT--0-blue?style=flat-square)](https://github.com/lqxp/lqxp/blob/main/LICENSE)
  [![Built with Rust](https://img.shields.io/badge/server-Rust-orange?style=flat-square&logo=rust)](https://github.com/lqxp/lqxp)
  [![Client in Vue](https://img.shields.io/badge/client-Vue-42b883?style=flat-square&logo=vue.js)](https://github.com/lqxp/client)
  [![Website](https://img.shields.io/badge/website-qxch.at-purple?style=flat-square)](https://qxch.at)

</div>

---

## What is lqxp?

**lqxp** (Light QX Protocol) is an open, IRC-inspired messaging protocol designed from the ground up with end-to-end encryption at its core. No metadata harvesting, no surveillance, no accounts tied to your identity — just rooms, messages, and cryptographic privacy.

Think of it as a modern, minimal alternative to IRC, where every message is encrypted client-side before it ever touches the wire.

> Rooms are ephemeral. Keys stay with you. The server sees nothing.

---

## Repositories

### [`lqxp/lqxp`](https://github.com/lqxp/lqxp) — the protocol server
> **Rust** · MIT-0

The core of the project. A lightweight, high-performance WebSocket server implementing the QX Protocol. Handles room management, message relay, presence, voice signaling, and more — without ever seeing the plaintext content of your messages.

---

### [`lqxp/client`](https://github.com/lqxp/client) — web client
> **Vue** · MIT-0

`QxpClient` is the official browser-based client for the lqxp protocol. Built with Vue 3, it handles E2EE in-browser using the Web Crypto API, supports voice calls via WebRTC, file attachments, reactions, typing indicators, and a full offline-capable UI. No Electron, no native binary required — just open the browser and go.

---

### [`lqxp/app`](https://github.com/lqxp/app) — desktop & mobile app
> **Nix** · Tauri-based

`QxpApp` is the official packaged application wrapping `QxpClient` into a native experience using Tauri. Available for desktop (Linux, macOS, Windows) and Android. Built and distributed via Nix for reproducible, auditable builds. Same client code, native notifications, system tray, and device-level audio support.

---

### [`lqxp/site`](https://github.com/lqxp/site) — website
> **Vue** · MIT-0

The source code for [qxch.at](https://qxch.at) — the public-facing website for the project. Landing page, documentation, and download links.

---

## Key features

- 🔒 **End-to-end encryption** — AES-GCM encryption client-side, room keys never leave your device
- 🔑 **Room tokens** — share a single token to grant access and the encryption key at once
- 🎙️ **Voice calls** — WebRTC-based, peer-to-peer audio with optional noise gate and per-user volume
- 📎 **File attachments** — send images, audio, video and arbitrary files, encrypted like any message
- 👤 **Pseudonymous** — username-based, no email, no phone number required
- 🌐 **Self-hostable** — run your own lqxp server in minutes

---

## Getting started

The fastest way to try lqxp is at **[qxch.at](https://qxch.at)** — the public hosted instance.

To self-host or contribute, start with the server:

```sh
git clone https://github.com/lqxp/lqxp
cd lqxp
cargo build --release
```

Then point `QxpClient` or `QxpApp` at your server's WebSocket URL.

---

<div align="center">
  <sub>Built in Iceland · Open source · No tracking</sub>
  <br />
  <a href="https://qxch.at">qxch.at</a>
</div>
