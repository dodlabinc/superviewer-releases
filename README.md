<p align="center">
  <img src="logo.svg" width="80" height="80" alt="superviewer icon">
</p>

<h1 align="center">superviewer</h1>

<p align="center">
  <strong>AI agent builds it. superviewer shows it.</strong><br>
  <sub>Instant desktop viewer for AI-generated artifacts — images, HTML, video, docs — via MCP.</sub>
</p>

<p align="center">
  <a href="https://github.com/dodlabinc/superviewer-releases/releases/latest">
    <img src="https://img.shields.io/github/v/release/dodlabinc/superviewer-releases?style=flat-square&color=2dd4a8&label=download" alt="Latest Release">
  </a>
  <img src="https://img.shields.io/badge/platform-macOS-333?style=flat-square" alt="macOS">
  <img src="https://img.shields.io/badge/MCP-compatible-a78bfa?style=flat-square" alt="MCP">
</p>

<br>

<p align="center">
  <img src="marketing/hero.png" width="720" alt="superviewer — main view">
</p>

---

## What is superviewer?

When AI agents (like Claude Code) generate files — screenshots, HTML pages, charts, videos — you normally have to find them in Finder, open them in a browser, or switch between apps. **superviewer** eliminates that friction.

One MCP tool call → content renders instantly in a persistent desktop viewer.

<p align="center">
  <img src="marketing/workflow.png" width="720" alt="superviewer workflow — Claude Code → superviewer → Remote Peer">
</p>

## Features

- **Instant render** — Image, HTML, video, audio, markdown, documents. No browser needed.
- **MCP integration** — Single `show()` tool call from Claude Code. Zero config after install.
- **Symmetric nodes** — Every device both serves and views. No central server.
- **Remote peers** — Send artifacts to any machine on your network via Tailscale/LAN.
- **Ephemeral serving** — Resources auto-expire with configurable TTL.
- **Feed history** — Searchable, filterable timeline of all artifacts.
- **Auto-update** — Built-in updater with one-click install.

## Download

**[Download latest release](https://github.com/dodlabinc/superviewer-releases/releases/latest)**

| Platform | File | Architecture |
|----------|------|-------------|
| macOS | `.dmg` | Apple Silicon |

## Quick Start

### 1. Install

Download the `.dmg`, drag to Applications, and open. On first launch, right-click → **Open** (not yet notarized by Apple).

### 2. Enable MCP

Open superviewer → Settings → MCP section → **Install**.

This registers superviewer as an MCP server in `~/.claude/settings.json`.

### 3. Use from Claude Code

```
show("./chart.png", "image")
show("./report.html", "html", { title: "Q3 Report" })
```

Content appears instantly in superviewer.

## MCP Tools

| Tool | Description |
|---|---|
| `show(source, type, meta?)` | Render a single file |
| `show_group(items, meta?)` | Render multiple files as a group |
| `capture(window?, meta?)` | Capture a screen/window and display |

## Remote Peers

Send artifacts to another machine running superviewer:

```
show("./design.png", "image", { target: "imac-office" })
```

Manage peers in Settings → Peers. Devices discover each other via Tailscale IP or LAN.

## Auto-Update

superviewer checks for updates on launch and notifies you when a new version is ready. You can also check manually via the app menu → **Check for Updates**.

---

Made by [Dodlab, Inc.](https://dodlab.kr)
