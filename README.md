[English](README.md) | [日本語](README.ja.md)

# Gigant Monitor Plus

**Gigant Monitor Plus** is the **direct-download edition** of "Gigant Monitor", a menu bar utility for macOS that
shows your system status on purple-and-yellow liquid meters. Its artwork is inspired by 1970s anime instrument panels,
and it is a tool for enjoying the view of your system's activity.

This repository is the **distribution point for Gigant Monitor Plus (notarized binaries)**.

> The standard edition, "Gigant Monitor", is available on the [Mac App Store](https://apps.apple.com/app/gigant-monitor/id6777906549) (free).
> The Plus edition is a Developer ID direct-download build that has everything the App Store edition has, plus **power consumption**.
>
> Up to v2.2.2 it was called "Gigant Monitor Pro". It was renamed "Gigant Monitor Plus" in v2.3.0 (features and settings carry over as they are).

---

## Differences from the standard edition

| | Gigant Monitor (App Store) | Gigant Monitor Plus (this repo) |
|---|---|---|
| Liquid meters (CPU / Network / Disk) | ✅ | ✅ |
| Timelines (Network / Disk) | ✅ | ✅ |
| CPU timeline | ✅ | ✅ (Power & CPU Timeline) |
| **Power meter** (switch in the CPU window) | ― | ✅ |
| **Power & CPU Timeline** | ― | ✅ |
| Distribution | Mac App Store | Notarized binary (direct download) |

Reading power draw requires something that is not available inside the App Store sandbox
(direct access to the System Management Controller, SMC), so the App Store edition cannot include it.
**If power draw isn't something you care about, the App Store edition is all you need.**

---

## Download

### Homebrew (recommended)

```sh
brew install --cask EVAtiter/tap/gigant-monitor-plus
```

> If Homebrew refuses to load the tap because it is not trusted,
> run `brew trust --cask EVAtiter/tap/gigant-monitor-plus` first.
>
> If you installed it under the old name `gigant-monitor-pro`, `brew upgrade` moves you over automatically.

### Manual

Get the latest version from [Releases](https://github.com/EVAtiter/gigant-monitor-pro-release/releases/latest).

1. Download `Gigant-Monitor-Plus-<version>.zip`
2. Unzip it and move `Gigant Monitor Plus.app` to the Applications folder
3. If a confirmation appears the first time you open it, click "Open" (it is notarized, so it passes Gatekeeper)

---

## Features

- **Three liquid meters**: CPU / Network (up & down) / Disk (read & write)
- **Power meter** (Plus only): switch the CPU window between CPU usage and power draw.
  On a laptop Mac it shows the power of the chip (SoC); on a desktop Mac it shows the power of the whole Mac
- **Three timelines**: Power & CPU (Plus only; CPU usage on top, power draw below) / Network / Disk history,
  drawn as smooth filled curves. The right edge is now, and history flows to the left (off by default)
  - Network grows from a center line: upload above, download below
  - Disk grows from a center line: read above, write below
- **The default layout gives each metric its own column**, with its timeline right below the liquid meter
- 10 color themes, switched from the menu. Liquid color, liquid transparency, and panel transparency are all
  adjustable and stored per theme
- Per-window size and position lock; shared "Always on Top" and "Pin to Wallpaper" toggles
- **Quick Reveal**: rest the cursor at the bottom of the screen for half a second to bring visible windows
  to the front for a moment (off by default)
- Network, disk, and power are shown against their recent peak as 100%
  (Peak Memory: 5 / 15 / 30 min / 1 hour / unlimited)
- Arrange menu (vertical, side by side, Reset to Initial)
- Low Power Mode (lowers the frame rate to save power). It also lowers the frame rate on its own when idle,
  and stops drawing while the display sleeps or the window is fully hidden behind others
- Per-display position memory for multi-monitor setups
- Japanese / English UI
- The app itself makes no network connections of its own

## Requirements

- macOS 14 Sonoma or later
- Apple Silicon (arm64) only
- Notarized by Apple

## Privacy

Gigant Monitor Plus **collects no data of any kind**.
All measurements stay on your Mac and are never sent anywhere.
For details, see the
[privacy policy](https://github.com/EVAtiter/gigant-monitor-support/blob/main/PRIVACY.md)
shared with the standard edition.

## Support

Questions, requests, and bug reports go to the channel shared with the standard edition:

- [Discussions](https://github.com/EVAtiter/gigant-monitor-support/discussions)
- [Issues](https://github.com/EVAtiter/gigant-monitor-support/issues)

---

Copyright © 2026 EVA Titer. All rights reserved.
