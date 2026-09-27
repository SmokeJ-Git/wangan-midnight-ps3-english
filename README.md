# 🏁🌃 Wangan Midnight (PS3) — English Patch!

Ever wanted to race the Devil Z down the Wangan in **Wangan Midnight** (湾岸ミッドナイト), Genki's 2007 PlayStation 3 street-racing game based on Michiharu Kusunoki's manga, and actually understand what everyone's saying? Now you can! 🎉

The menus, the story and the on-screen text are all in English. 🇬🇧 (The voice acting and videos are still in Japanese.)

| | |
|---|---|
| 🎮 **Platform** | Sony PlayStation 3 |
| 💿 **Serial** | BLJM60028 (Japan), disc version 01.02 |
| 🩹 **Patch format** | xdelta3, applied to `WMN.DAT` and `WMN.TOC` only |
| 🧪 **Tested on** | RPCS3 |
| 🚧 **Status** | v0.5.0 beta |
| ⬇️ **Download** | grab it from [**Releases**](../../releases) |

---

## 📸 Screenshots

| 🎞️ Story cutscene | 💬 Race cut-in | 🏁 Title screen |
|:---:|:---:|:---:|
| ![Story photo cutscene: the Japanese vertical text stays, with an English subtitle](screenshots/screenshot-1-story-cutscene.png) | ![In-race cut-in with the Japanese line and the English line under it](screenshots/screenshot-2-race-cutin.png) | ![Title screen with the English copyright line](screenshots/screenshot-3-title-screen.png) |
| 🎬 **Midnight Theater** | 🏆 **Results** | 🃏 **Card View** |
| ![Midnight Theater menu in English](screenshots/screenshot-4-midnight-theater.png) | ![Time Attack results screen in English](screenshots/screenshot-5-results.png) | ![Card View screen in English](screenshots/screenshot-6-card-view.png) |

*Taken from the patched game in RPCS3.*

---

## ✅ What's translated

- 📋 **All the menus**: title, main menu, Story Mode, Time Attack, Free Run, One Match, options, save and install dialogs, the pause menu
- 📖 **Story Mode**: scenario and series select, the series synopses and the comic cutscene dialogue
- 🎞️ **The photo story cutscenes**: the original vertical Japanese text stays as part of the art, and an **English subtitle** appears at the bottom of the screen
- 💬 **In-race cut-ins**: the Japanese line is shown horizontally, with the **English line under it**
- 🏁 **Racing**: the HUD, mission banners, loading tips, road signs, results and the retry screen
- 🃏 **Card Set Up**: menus, card details and the card faces
- 🎬 **Midnight Theater**: every **Character File** biography and **Car Library** entry
- 🎨 **Graphics redrawn in English**: button prompts, character name badges, arc and episode title cards, status badges, the boot notices and the title-screen copyright
- 🔤 **A new English font** with proportional letter spacing
- 🧑 **Character names** follow the English names used by fans of the manga and anime

### 🇯🇵 Still in Japanese

- 🎙️ The voice acting
- 🎬 The videos
- 🎞️ The vertical text in the photo cutscenes, on purpose (it has an English subtitle)

---

## 📦 What you need

The Japanese disc **BLJM60028, version 01.02**, dumped as a game folder (`PS3_GAME` + `PS3_DISC.SFB`). Only two files get patched, both in `PS3_GAME\USRDIR\PS3\`:

| File | Size (bytes) | CRC32 | MD5 |
|---|---|---|---|
| `WMN.DAT` | 914,235,392 | `d41ab9c3` | `1459fb12e07831370eab5cf2fce9b491` |
| `WMN.TOC` | 229,192 | `5cc1f15a` | `8f775d3d521236b28ef3f0627ab39306` |

SHA-1 of `WMN.DAT`: `7031528a066bc8f3b59deddc7531b8d334f55437`

👉 **Only these two files get patched.** Leave `EBOOT.BIN` and everything else exactly as they are. No game patch (`patch.yml`) is needed.

> ⚠️ This repo contains **only patch files**. No game data is included, so you need your own copy of the game.

---

## 🛠️ How to apply

1. 💾 **Back up** your `WMN.DAT` and `WMN.TOC` first!
2. 🩹 Apply each `.xdelta` to its file with any xdelta3 tool:
- 🪟 **Windows app:** [Delta Patcher](https://github.com/marco-calautti/DeltaPatcher) or xdeltaUI
- 🌐 **In your browser:** [Rom Patcher JS](https://www.marcrobledo.com/RomPatcher.js/) (the 900 MB `WMN.DAT` may be too big for some browsers; use a desktop tool if it fails)
- 💻 **Command line:**
```
xdelta3 -d -s "original WMN.DAT" "Wangan Midnight - English v0.5.0 (WMN.DAT).xdelta" "WMN.DAT"
xdelta3 -d -s "original WMN.TOC" "Wangan Midnight - English v0.5.0 (WMN.TOC).xdelta" "WMN.TOC"
```
3. 📝 Put the two patched files back in `PS3_GAME\USRDIR\PS3\` **under their original names**.
4. 🎮 Boot `PS3_GAME\USRDIR\EBOOT.BIN` in RPCS3, or copy the game folder to a PS3 running custom firmware / HEN and start it from webMAN or multiMAN.

### 🔍 Check your result

| File | Size (bytes) | CRC32 | MD5 |
|---|---|---|---|
| Patched `WMN.DAT` | 912,773,120 | `057425cc` | `1ee60751790cf625320954a8e8b553a3` |
| Patched `WMN.TOC` | 229,192 | `a85306fc` | `e81782415a75351e0a394575d8220ec3` |
| Patch file (`WMN.DAT`) | 21,330,290 | `eaa257b2` | `681842dd4af2911dc0790daebcf64280` |
| Patch file (`WMN.TOC`) | 9,076 | `c143519f` | `bfd0d7383b71f632ab2706f835a53ecb` |

SHA-1 of the patched `WMN.DAT`: `5e3e6ca16812f8c0bd23f54e3809742783b27bde`

📏 The patched `WMN.DAT` is **1,462,272 bytes smaller** than the original. That's expected, don't worry!

❌ If the patcher complains about a checksum or source mismatch, your files aren't from the 01.02 disc listed above.

---

## 🚧 Known limits (v0.5.0 beta)

- 🖥️ Tested on emulator (RPCS3) only. It hasn't been tried on real PS3 hardware yet.
- 👀 Not checked on screen yet: story cutscenes past the opening of each arc, the Character File and Car Library entries (they unlock as you play), a cut-in with the portrait on the right, and online mode (Wangan Connection).
- 🤏 The title-screen copyright line is correct but small.

Found something still in Japanese, or text that runs off the screen? Open an [issue](../../issues) with a screenshot! 🙏

---

## 🤓 Technical notes

- 🗂️ All the game's text and graphics live in one big archive (`WMN.DAT`, indexed by `WMN.TOC`). The patch rebuilds that archive; the game program itself isn't touched. A rebuild with no changes reproduces the original archive byte for byte.
- 🔤 Text is stored as plain Shift-JIS, and English lines are broken by hand, since the game doesn't wrap text by itself. The font atlases got new Latin letters and a proportional width table.
- 🎞️ The photo cutscenes draw their text vertically. Each vertical line keeps its Japanese, and the cutscene script gets an extra call that shows the English line in the game's own horizontal subtitle box.
- 💬 The race cut-in text box is switched from vertical to horizontal in its scene file, and each line shows the Japanese with the English under it.
- 🧰 Everything was rebuilt with custom tools: archive repacking, text tables, scene-graph text, texture injection (DXT) and cutscene script patching.

---

## ⚖️ Disclaimer

This is an unofficial, non-commercial fan project ❤️. It is not affiliated with or endorsed by Genki, Kodansha, or the original author, Michiharu Kusunoki. *Wangan Midnight* and all related characters and marks belong to their respective owners. Please support the official releases! 🙏

🤖 **AI assistance:** AI tools helped with parts of this project.
