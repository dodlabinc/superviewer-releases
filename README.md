# superviewer

See what your AI makes — instantly.

superviewer is a lightweight desktop app that displays outputs from AI coding agents. When an agent generates an image, chart, HTML page, or video, it calls `show()` and the result pops up in a native window on your screen. No more digging through folders or opening browser tabs.

It works across machines too. If your AI agent runs on a remote server, superviewer can display its outputs on your local desktop over Tailscale or LAN.

## Download

**[Download latest release](https://github.com/dodlabinc/superviewer-releases/releases/latest)**

| Platform | File | Architecture |
|----------|------|-------------|
| macOS | `.dmg` | Apple Silicon |
| Windows | `.msi` | x64 |

## Getting Started

1. Install and open superviewer. It runs as a tray app.
2. Open Settings and enable the MCP server.
3. That's it. Your agent can now call `show()` and outputs appear on your screen.

## macOS Note

The app is code-signed but not yet notarized by Apple. On first launch, right-click the app and select **Open**. After that it opens normally.

## Auto-Update

superviewer checks for updates on launch and notifies you when a new version is ready.

---

Made by [Dodlab, Inc.](https://dodlab.kr)
