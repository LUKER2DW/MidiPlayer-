<div align="center">

# Midi Player+

**A modern piano autoplayer for Roblox.**
Loads `.mid` files and plays them on the game's virtual keyboard —
respecting tempo, velocity and sustain.

![version](https://img.shields.io/badge/version-0.1.0--alpha-89b4fa?style=flat-square)
![platform](https://img.shields.io/badge/platform-Windows%2010%2F11%20x64-cba6f7?style=flat-square)
![status](https://img.shields.io/badge/status-alpha-f38ba8?style=flat-square)
![source](https://img.shields.io/badge/source-coming%20soon-a6adc8?style=flat-square)

[**⬇ Download latest**](../../releases/latest) · [Report a bug](../../issues/new) · [Request a feature](../../issues/new)

</div>

---

## Quick start

1. Download **`MidiPlayer.exe`** from [Releases](../../releases/latest).
2. Double-click it. The installer sets everything up into
   `Documents\Midi Player+\` automatically.
3. Drop `.mid` files into `Documents\Midi Player+\midi\`.
4. Open the app, pick a song, tab into Roblox, hit **F1**. Done.

## Features

- 🎹 **88-key and 61-key** layouts, auto-detected or manual
- 🎚️ **Velocity + sustain** handled properly (no flat, robotic playback)
- ⌨️ **Global hotkeys** — F1/F2/F3 work while Roblox is focused
- 🪟 **Overlay mode** — floating always-on-top window that doesn't steal focus
- 👤 **Unlimited profiles** — separate tempo / transpose / settings per game
- 🎨 **Modern themes** (Catppuccin + others)
- 📦 **Portable** — no registry keys, no admin needed, clean uninstaller

## Why another autoplayer?

Inspired by **MIDI++**, **NanoMIDI** and the popular AHK scripts, but
built as a proper desktop app with a UI, profiles, overlay mode, and a
clean installer.

| | AHK scripts | NanoMIDI | MIDI++ | **Midi Player+** |
|---|:---:|:---:|:---:|:---:|
| Graphical UI           | ❌ | ✅ | ✅ | ✅ |
| 88 + 61-key            | partial | ✅ | ✅ | ✅ |
| Velocity               | ❌ | partial | ✅ | ✅ |
| Sustain (CC64)         | ❌ | ✅ | partial | ✅ |
| Overlay over Roblox    | ❌ | ❌ | ✅ | ✅ |
| Multiple profiles      | ❌ | ❌ | partial | ✅ |
| Modern theming         | ❌ | ✅ | ❌ | ✅ |
| Installer/Uninstaller  | ❌ | ❌ | ❌ | ✅ |

### Performance

Measured on a real track (~100 keystrokes):

| | p50 | p95 | p99 | max |
|---|---:|---:|---:|---:|
| Scheduling drift             | **0.5 ms** | 1.5 ms | 2.1 ms | 5.6 ms |
| Key press (SendInput)        | **1.0 ms** | 2.4 ms | 3.2 ms | 3.3 ms |
| **End-to-end latency**       | **~1.5 ms** | ~3.9 ms | ~5.3 ms | ~9 ms |

Well below the ~10 ms perceptual threshold for audio alignment — dense
chords and fast passages stay tight.

The one honest trade-off is **disk size** — the `.exe` is ~300 MB
because it ships a full runtime. Shrinking this is on the roadmap.

## Default hotkeys

| | | | | |
|:---:|:---|:---:|:---:|:---|
| `F1` | Play       || `F7`  | Reload library |
| `F2` | Pause      || `F8`  | Previous song  |
| `F3` | Stop       || `F9`  | Next song      |
| `F4` | Speed +5 % || `F10` | Toggle loop    |
| `F5` | Speed −5 % || `F11` | Toggle overlay |
| `F6` | Restart    || `F12` | **Panic** (release all keys) |

All remappable in **Settings → Keybinds**.

## Requirements

- Windows 10 / 11 (64-bit)
- ~800 MB free disk space
- **Run as Administrator** recommended — Roblox can block synthetic
  input from non-elevated processes.

## Uninstall

Run `Uninstaller.exe` inside `Documents\Midi Player+\`. It confirms
before doing anything, and asks separately whether to delete your MIDIs
and settings. No registry touched.

## FAQ

**Do I need Python / Node / anything installed?** No. The `.exe` is
self-contained.

**Will I get banned?** Piano autoplayers are widely tolerated on Roblox
and this app doesn't inject code or touch game files — it just sends
keystrokes. That said, **use at your own risk.**

**Is the source open?** Not yet. It'll be published once it's out of
alpha. Only compiled binaries live here for now.

**Why so big?** Bundled Python + Chromium-based UI runtime. Fixing this
is a priority for v0.2.

## Roadmap

- [ ] Shrink the installer (~300 MB → <100 MB target)
- [ ] Code-sign the binary
- [ ] Open-source the project
- [ ] MIDI device input (play a real keyboard *through* the app)
- [ ] Custom theme builder
- [ ] Full midi hub to download, use and upload your own midis

## Credits

Inspired by [**MIDI++**](https://github.com/Zephkek/MIDIPlusPlus) and [**NanoMIDI**](https://github.com/NotHammer043/nanoMIDIPlayer) - thanks
to the Roblox piano community and midi community for keeping this scene alive.

---

<div align="center">

**Midi Player+** · v0.1.0-alpha · Made with ♥ for the Roblox piano community.

</div>
