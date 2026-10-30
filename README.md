<h1 align="center">SMPJRecompAndroid</h1>
<p align="center">by ORIKAMI</p>

<p align="center"><i>A native Android port of Super Mario Party Jamboree (Nintendo Switch). Bring your own legally dumped copy and keys. No game files, keys or source code are published here. Runs with <a href="https://github.com/orikami-dev/masu">Masu</a>.</i></p>

<p align="center">
  <a href="https://github.com/orikami-dev/SMPJRecompAndroid/releases">📦 All versions</a>
  ·
  <a href="CHANGELOG.md">📝 Changelog</a>
</p>

---

## 🎮 The project

This port runs **Super Mario Party Jamboree** natively on Android. It is not a general-purpose emulator: the game's ARM64 code runs directly on the phone's processor, and only the Switch's system and the NVN graphics API are replaced by native Android and Vulkan code.

**This repository only publishes release notes.** It contains no code, no game data and no keys: you need your own copy of the game and your own keys, extracted from your console.

| | |
|---|---|
| 🎮 **Native game** | The game's ARM64 code runs as is on the phone, with sound. |
| 🖼️ **NVN to Vulkan** | The Switch's shaders are translated in advance. |
| 🕹️ **Controllers** | Physical controllers 1 to 4 and a touch controller in party colors. |
| 📱 **Made for foldables** | Landscape, full screen on the external display as on a foldable's inner screen. |
| 🧰 **Logbook** | Crash report, shareable log and a ready-to-send e-mail after an incident. |
| 📦 **Launched by Masu** | [Masu](https://github.com/orikami-dev/masu) prepares the game (keys, dump, extraction) then launches it. |

## ✨ Highlights

- 🚀 Fast loading: a 35 s test went down to 46 ms.
- 🕹️ Same touch controller on both foldable screens, x2 button to speed up the game.
- 📊 Discreet frames-per-second counter, with temperatures.
- 🛟 After a crash: a full report, a log and a ready-to-send e-mail.
- 🔒 No game file and no key: everything stays on your device.

## ⭐ Major updates

| Version | What it brought |
|---|---|
| 1.0.0 | Local multiplayer up to 4, new touch controller, Settings menu, cast and DeX, fast startup. |
| 0.97 | Local multiplayer with physical controllers and a new touch controller. |
| 0.95 | Characters' dialogue bubbles displayed. |
| 0.83 | Less heat and smoother play. |
| 0.77 | Board spaces displayed (indirect draws executed). |
| 0.74 | Flattened characters fixed. |
| 0.70 | Characters, NPCs and Bowser in color. |
| 0.64 | Characters animated by the graphics card finally drawn. |
| 0.59 | The graphics driver and its version are shown in game. |
| 0.58 | Checks and a health line in the logs. |
| 0.57 | End of a crash when loading boards. |
| 0.52 | Fast loading, new touch controller, x2 button. |
| 0.49 | 3D scenery appears. |
| 0.33 | Sound arrives. |
| 0.22 | Character selection reached. |
| 0.15 | Title screen and main menu. |

## 🛠️ The repository

| File | Content |
|---|---|
| `docs/releases/` | The notes of each version |
| `CHANGELOG.md` | The changelog |

## ⚖️ Good to know

Personal use only, with a copy of the game that you own. No game file, key or code is published in this repository.

Not affiliated with Nintendo. The names and trademarks mentioned belong to their owners.
