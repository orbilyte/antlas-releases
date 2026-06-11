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

<div align="center">

Made by **[orbilyte](https://orbilyte.de)** · [orbilyte.de](https://orbilyte.de)

</div>
