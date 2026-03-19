# MoanMod — macOS Installation Guide (CrossOver)

> MelonLoader does not have an Apple Silicon (ARM64) build, so the mod cannot run natively on modern Macs. The workaround is to run the Windows version of MDRG inside CrossOver.

---

## Table of Contents

- [Requirements](#requirements)
- [Installation](#installation)
  - [Step 1 — Create a CrossOver Bottle](#step-1--create-a-crossover-bottle)
  - [Step 2 — Install the Game](#step-2--install-the-game)
  - [Step 3 — Install MelonLoader](#step-3--install-melonloader)
  - [Step 4 — Fix MelonLoader Not Loading](#step-4--fix-melonloader-not-loading-important)
  - [Step 5 — First Launch](#step-5--first-launch)
  - [Step 6 — Install the Mod](#step-6--install-the-mod)
  - [Step 7 — Launch and Test](#step-7--launch-and-test)
- [Troubleshooting](#troubleshooting)
- [Links](#links)

---

## Requirements

| What | Where |
|------|-------|
| CrossOver | https://www.codeweavers.com/crossover (paid, has a free trial) |
| MDRG Windows version | https://incontinentcell.itch.io/factorial-omega |
| MelonLoader v0.7.2 | https://github.com/LavaGang/MelonLoader/releases/tag/v0.7.2 — download `MelonLoader.Installer.exe` |
| MoanMod | https://github.com/IkariDevGIT/MDRGMoanMod/releases — download the latest release zip |
| Torrent Version of CrossOver | https://www.torrentmac.net/crossover-26-0-0/ |
---

## Installation

### Step 1 — Create a CrossOver Bottle

1. Open CrossOver and create a new bottle
2. Name it whatever you want (e.g. `MDRG`)
3. Set it to **Windows 10, 64-bit**
4. In the bottle settings, set the following:

| Setting | Value |
|---------|-------|
| MSYNC | On |
| ESYNC | On |
| D3DMetal | On |
| DXVK | Off |

---

### Step 2 — Install the Game

1. Download the **Windows** version of MDRG from itch.io — it comes as a zip
2. Unzip it on your Mac
3. In CrossOver, open your bottle and click **Open C: Drive**
4. Navigate to `C:/Program Files/` and copy the unzipped MDRG folder in there

---

### Step 3 — Install MelonLoader

1. In CrossOver, run `MelonLoader.Installer.exe` inside your bottle
2. Click **Add game manually**
3. Navigate to `C:/Program Files/My Dystopian Robot Girlfriend/` and select `My Dystopian Robot Girlfriend.exe`
4. Click the game in the selection menu
5. **Do NOT** enable nightly builds — select version **0.7.2**
6. Hit **Install**

---

### Step 4 — Fix MelonLoader Not Loading (Important)

MelonLoader won't load under Wine/CrossOver without this fix:

1. Go to your game folder inside the bottle (`C:/Program Files/My Dystopian Robot Girlfriend/`)
2. Find `version.dll` and rename it to `winhttp.dll`
3. In CrossOver, open your bottle's **Wine Configuration**
4. Go to the **Libraries** tab
5. Add `winhttp` and set it to **Native then Builtin**

---

### Step 5 — First Launch

Launch the game once through CrossOver by running `My Dystopian Robot Girlfriend.exe` directly. This lets MelonLoader create the `Mods/` folder. You should see the MelonLoader splash screen if everything worked.

---

### Step 6 — Install the Mod

1. Open your bottle's C: drive and navigate to:

```
C:/users/crossover/AppData/LocalLow/IncontinentCell/My Dystopian Robot Girlfriend/Mods/
```

On Mac this folder is located at:

```
~/Library/Application Support/CrossOver/Bottles/[your bottle name]/drive_c/users/crossover/AppData/LocalLow/IncontinentCell/My Dystopian Robot Girlfriend/Mods/
```

> **Tip:** Press `Cmd+Shift+G` in Finder to paste a path directly.

2. Extract the MoanMod zip and place the files so the structure looks like this:

```
Mods/
├── MoanMod.dll
└── MoanMod/
    ├── cumming/
    │   ├── start/
    │   ├── while/
    │   └── end/
    ├── while/
    └── breath/
```

---

### Step 7 — Launch and Test

Launch the game again. If MelonLoader loaded correctly you will see its splash screen on startup. The mod activates automatically once the prologue is finished.

---

## Troubleshooting

**No MelonLoader splash screen on launch**
> The `winhttp.dll` rename or Wine Configuration step was not done correctly. Go back and double check [Step 4](#step-4--fix-melonloader-not-loading-important).

**Mod installed but no audio**
> Check that your WAV audio files are actually inside the correct subfolders. The `MoanMod/cumming/while/` folder must contain at least one `.wav` file or the mod will silently fail to load.

**Mod not working after prologue**
> Make sure your in-game stats are high enough. The mod requires sympathy above 5 and lust above 10 before it does anything.

**Game crashes on launch**
> Install the following inside your CrossOver bottle via the **Install a Windows Application** option:
> - Microsoft Visual C++ Redistributables (2015–2019)
> - .NET 6.0 Desktop Runtime

## If troubleshooting didnt help u dm me
> laouuuuu on discord
---

## Links

- Original mod: https://github.com/IkariDevGIT/MDRGMoanMod
- MelonLoader: https://github.com/LavaGang/MelonLoader/releases/tag/v0.7.2
- CrossOver: https://www.codeweavers.com/crossover
- MDRG on itch.io: https://incontinentcell.itch.io/factorial-omega
- Torrent Crossover: https://www.torrentmac.net/crossover-26-0-0/
