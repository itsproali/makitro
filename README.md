<div align="center">

# Makitro

**Small, native menu-bar utilities for the annoying parts of macOS.**

Clipboard history, a colour picker, classic mouse scrolling and keyboard cleaning in one lightweight app.
Free, private, and close to zero idle cost.

[![Latest release](https://img.shields.io/github/v/release/itsproali/makitro?label=release)](https://github.com/itsproali/makitro/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/itsproali/makitro/total)](https://github.com/itsproali/makitro/releases)
![macOS 14+](https://img.shields.io/badge/macOS-14%20Sonoma%2B-blue)
![Apple silicon and Intel](https://img.shields.io/badge/Apple%20silicon%20%26%20Intel-universal-lightgrey)

[**Download**](https://github.com/itsproali/makitro/releases/latest/download/Makitro.dmg) ·
[Website](https://makitro.mdali.dev) ·
[Report a bug](https://github.com/itsproali/makitro/issues/new) ·
[Support](https://makitro.mdali.dev/support)

</div>

---

> [!NOTE]
> **Makitro 0.9 is a developer preview.** It's signed by the developer but not yet notarized by Apple, so
> macOS asks you to confirm the first time you open it ([see below](#first-launch)). Version 1.0 will be
> notarized.

## Features

| Utility | What it does |
|---|---|
| **Clipboard History** | Keeps what you copy (text, links, colours and images) on your Mac. Press **⌃⌘V** to search it and paste any item where you were typing. Pin favourites, pause recording, exclude apps, and set a history limit (500 items by default). Copies from password managers are never saved. |
| **Scroll Reverser** | Keeps natural scrolling on the trackpad while an external mouse scrolls the classic way. No more flipping a system setting every time you plug in a mouse. |
| **Color Picker** | Press **⌃⌘C** to pick any colour on screen with the system magnifier and copy it as HEX, `rgb()` or `hsl()` (sRGB). No Screen Recording permission needed. |
| **Keyboard Cleaning** | Locks every key, including media and brightness keys, while you wipe your keyboard. Unlocks with one click, or by itself after 1–5 minutes. |

Every utility can be turned off on its own, and a turned-off utility stops completely. Shortcuts can be
changed in Settings.

## Install

### Homebrew

```bash
brew install --cask itsproali/tap/makitro
```

### Direct download

1. Download [**Makitro.dmg**](https://github.com/itsproali/makitro/releases/latest/download/Makitro.dmg).
2. Open it and drag **Makitro** to **Applications**.
3. Open Makitro from Applications. It lives in the menu bar; there's no Dock icon.

### First launch

Because the preview isn't notarized yet, macOS blocks it the first time:

1. Open Makitro. When macOS says it can't verify the app, click **Done**.
2. Open **System Settings › Privacy & Security**, scroll down, and click **Open Anyway** next to Makitro.
3. Confirm with your password or Touch ID.

You only do this once. After that, Makitro opens normally and updates itself.

## Requirements

- macOS 14 Sonoma or later
- Apple silicon or Intel Mac

## Privacy

Makitro is built to be trusted with your clipboard.

- **Everything stays on your Mac.** No account, no cloud sync, no analytics, no tracking.
- **The only network request is the update check**, and Makitro asks before checking automatically. It
  sends nothing about you or your Mac.
- Clipboard history is stored only in `~/Library/Application Support/dev.mdali.Makitro/`, readable only by
  your user account. Clear History deletes it for real.
- Copies that password managers mark as private (the standard nspasteboard.org markers) are never recorded.
- Clipboard content is hidden from screen sharing and recordings.

Full details: [Privacy policy](https://makitro.mdali.dev/privacy).

## Permissions

Makitro asks for a permission only when you turn on something that needs it, never at launch, and
always explains why first.

| Permission | Used by | Why |
|---|---|---|
| Accessibility | Scroll Reverser | To change the scroll direction of mouse events |
| Accessibility | Keyboard Cleaning | To block key presses during a cleaning session |
| Accessibility | Clipboard History (optional) | To paste the item you choose; without it, Makitro copies instead |

Screen Recording and Input Monitoring are never requested.

## Updates

Makitro updates itself through [Sparkle](https://sparkle-project.org). Every update is verified with a
cryptographic signature before it's installed. To check manually, use **Check for Updates…** under
**General › Updates**. Homebrew installs update the same way.

## Uninstall

Quit Makitro, then delete it from Applications. To remove your data as well:

```bash
rm -rf ~/Library/Application\ Support/dev.mdali.Makitro
defaults delete dev.mdali.Makitro
```

With Homebrew: `brew uninstall --zap --cask makitro`.

## Feedback and support

- **Bugs:** use **Report a Bug** in Makitro's menu bar (it opens a pre-filled email you can edit), or
  [open an issue](https://github.com/itsproali/makitro/issues/new). Include your Makitro and macOS
  versions; **General › Help & feedback › Copy Diagnostics** copies them for you.
- **Questions and ideas:** [itsproali@gmail.com](mailto:itsproali@gmail.com)
- **Help:** [makitro.mdali.dev/support](https://makitro.mdali.dev/support)

## About this repository

This repository hosts Makitro's releases and issue tracker. The source code isn't public.

Makitro is free to use. © 2026 Mohammad Ali. All rights reserved.
