<div align="center">

# 🐜 Antlas — Releases

**Signed desktop builds & auto-update feed for [Antlas](https://orbilyte.de).**

[![Latest release](https://img.shields.io/github/v/release/orbilyte/antlas-releases?style=flat-square&label=latest)](https://github.com/orbilyte/antlas-releases/releases/latest)
[![Platforms](https://img.shields.io/badge/platforms-macOS%20·%20Windows-2b2b2b?style=flat-square)](#downloads)
[![orbilyte.de](https://img.shields.io/badge/by-orbilyte.de-0a7d5a?style=flat-square)](https://orbilyte.de)

</div>

---

## What is Antlas?

**Antlas is a memory & overview layer for [Claude Code](https://claude.com/claude-code).**

Every Claude Code session is a conversation that, once closed, slips out of reach.
Antlas turns those `~/.claude` session logs into something you can actually *use*:

- 🔍 **Searchable history** — full-text search across every session, project, and tool call.
- 🧠 **Persistent project memory** — each repo gets a curated, opt-in `.wiki` that survives across sessions, so architecture, decisions, and learnings carry over instead of being rediscovered every time.
- 🗺️ **Overview at a glance** — a repo-grouped map of what you've been working on, with a graph view of how it all connects.

It lives **primarily inside Claude Code** (as a plugin: skill + commands + hook + MCP server) and offers this **optional desktop app** as a visual companion.

> **Read-only & private by design.** Antlas never modifies your session logs and never writes into your repos on its own — all memory is proposed and only written after your explicit confirmation. Nothing leaves your machine.

---

## This repository

This repo holds **only the published, signed release assets** for the Antlas desktop app — no source code.

- ✅ Cryptographically **signed** installers (`.dmg`, `.msi`) and their update signatures
- ✅ The `latest.json` auto-update manifest consumed by the in-app updater
- 🔒 Source code stays in a separate, private repository

Builds are produced and signed automatically by CI; the desktop app verifies every update's signature against a public key baked into the binary before installing.

## Downloads

Grab the newest build from the **[latest release »](https://github.com/orbilyte/antlas-releases/releases/latest)**

| Platform | Asset |
|----------|-------|
| **macOS** (Universal — Intel & Apple Silicon) | `.dmg` |
| **Windows** | `.msi` |

Once installed, the app keeps itself up to date automatically.

---

## Installing on macOS

> **Heads-up:** the macOS builds are **not yet Apple-notarized**, so on first launch
> Gatekeeper blocks the app with a *“Antlas is damaged and can’t be opened”* or
> *“unidentified developer”* message. This is expected and **does not mean the app is
> harmful** — it's signed and its updates are cryptographically verified, it just hasn't
> gone through Apple's notary service yet. Proper notarization is on the roadmap; until
> then, one of the steps below gets you running.

**Recommended — remove the quarantine flag (most reliable):**

1. Open the downloaded `.dmg` and drag **Antlas** into your **Applications** folder.
2. Open **Terminal** and run:
   ```bash
   xattr -dr com.apple.quarantine /Applications/Antlas.app
   ```
3. Launch **Antlas** normally from Launchpad or the Applications folder.

**Alternative — right-click to open:**

1. Drag **Antlas** into **Applications** as above.
2. In Finder, **right-click** (or Control-click) `Antlas.app` → **Open**, then confirm
   **Open** in the dialog. (On Apple Silicon this sometimes still shows “damaged” — if so,
   use the Terminal command above.)

You only need to do this **once**. After the first launch, the in-app updater keeps Antlas
up to date automatically and no further workaround is needed.

---

<div align="center">

Made by **[orbilyte](https://orbilyte.de)** · [orbilyte.de](https://orbilyte.de)

</div>
