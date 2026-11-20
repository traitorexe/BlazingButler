# Blazing Butler

Automated farming assistant for **Naruto Blazing Revival**, built with a custom Six Paths interface, live HUD stage recognition, global server-cap protection, and an encrypted in-memory asset vault.

---

## Features

### Farming Modes
* **Ninja Road + Phantom Castle (Dual Mode):** Farms Ninja Road continuously and automatically switches over to Phantom Castle every 20 minutes whenever PC stamina regenerates, then returns to Ninja Road. If an active Ninja Road run is already in progress, the Butler finishes or retreats at your target map before switching.
* **Ninja Road Only:** Loops Ninja Road back-to-back with live `MAP 1/20`–`20/20` HUD stage recognition (supporting mid-run start and pause/resume), declines Pearl refills, and waits automatically when stamina runs dry.
* **Ninja Road Planned Retreats (`NR RETREAT`):** Choose between **Full Run (Clear / Wipe)** or automatic planned retreats **After Map 5**, **After Map 10**, or **After Map 15** to farm Granny Cat Coins and XP quickly without fighting later boss stages.
* **Phantom Castle Only:** Spends all available PC orbs, logs Wins & Losses (`W - L`), enforces persistent **40-match hourly** and **150-match daily** server limits (resetting globally at `00:00 UTC`), and waits 25 minutes between stamina cycles.
* **Standard Mission:** Contextual sub-menus for **Ramen** (`S`, `A`, `B`, `C`), **Scrolls** (`A`, `B`, `C`), **Ryo** (`B`, `C`), **Impact** (`S`, `A`, `B`), and **Emergency** (`A`, `B`, `C`). Selecting your mission type and difficulty automatically sets the exact stamina regeneration wait timer.
* **Trial Mission:** Supports **A Rank** (30 Stamina) and **B Rank** (20 Stamina). Automatically navigates from Emergency Missions into Trial Missions, selects the top Helper, enables Auto-Battle, and loops runs.

### Event & Resource Controls
* **Half Stamina Mode (`HALF STAMINA`):** Automatically syncs during 50%-off stamina events (or can be toggled manually) to halve all difficulty stamina costs and wait timers across Ninja Road, Standard Missions, and Trial Missions.
* **Configurable Pearl Refills (`BURN PEARLS` + `MAX`):** Available for Standard and Trial Missions—spends up to your chosen `MAX` Ninja Pearl cap on stamina refills before switching to safe stamina regeneration waits.

### Stability, Recovery & Interface
* **Any-Screen Startup & Daily Reset Recovery:** Start the bot from the Warning Screen, Title Screen, Home Screen, or mid-run. Automatically handles daily reset popups, Title Screen login, Data Updates, Login Bonuses, News banners, and resets the 150-battle PC daily limit at `00:00 UTC`.
* **Multi-Emulator ADB & Low-Idle Footprint:** Auto-connects across **BlueStacks, LDPlayer, Nox, MuMu, and MEmu**, uses sparse screenshot sampling during long stamina cooldowns to keep CPU and RAM usage minimal, and includes a screen-freeze watchdog that never sends blind taps.
* **Shinobi Access Terminal & Encrypted Vault:** Protected launch gate with encrypted in-memory `assets.dat` storage and one-click **GitHub Releases Auto-Updater** (`UPDATE`).

---

## Setup & Usage Guide

### 1. Emulator Configuration (Required)
1. Open your Android emulator settings (BlueStacks, LDPlayer, Nox, MuMu, or MEmu).
2. Set the display resolution to **720 × 1280 (Portrait)** with **240–320 DPI**.
3. Enable **ADB Debugging** (Android Debug Bridge) in your emulator's settings.
4. Launch **Naruto Blazing Revival** and leave it on any screen (Warning, Title Screen, Home Screen, or inside your chosen mode).

### 2. Installation & First Launch
1. Download the latest release `.zip` from the [Releases](../../releases) page and extract all files into a single folder (keep `BlazingButler.exe`, `assets.dat`, and `_internal` together).
2. Run **`BlazingButler.exe`**.
3. Enter your access code in the **Shinobi Access Terminal** and click **Unlock Access**.

### 3. Running a Farming Session
1. **Choose a Mode (`MISSION SCROLL`):**
   * For **Ninja Road** or **Dual Mode**, optionally pick an **NR Retreat** threshold (`Full Run`, `After Map 5`, `After Map 10`, or `After Map 15`).
   * For **Standard Mission**, select the **Mission** category (`Ramen`, `Scrolls`, `Ryo`, `Impact`, or `Emergency`) and its **Difficulty** (`S`, `A`, `B`, or `C`).
   * For **Trial Mission**, select **Difficulty** (`A Rank` or `B Rank`).
2. **Configure Event & Pearl Options:**
   * Check **HALF STAMINA** if a 50% stamina event is active (if not already auto-enabled).
   * For Standard or Trial Missions, leave **BURN PEARLS** unchecked to wait for natural stamina regeneration, or check **BURN PEARLS** and set **MAX** to cap Pearl spending.
   * For **Standard Mission**, open your target stage (or leave the emulator on the **Select Helper** or **Start Mission** screen) before starting.
3. Click **START MISSION**.

---

## Controls & Hotkeys

| Control / Key | Function |
| :--- | :--- |
| **`F3` / PAUSE** | Pauses or resumes automation immediately while freezing the active Butler Shift timer. |
| **`F4` / FINISH & STOP** | Finishes the current Ninja Road run, Phantom Castle cycle, or mission cleanly, then stops and prints the full **Butler Automation Report**. |
| **STOP NOW** | Halts automation immediately and prints the session summary. |
| **HOW TO USE** | Opens the in-app Field Manual with mode and setup instructions. |
| **UPDATE** | Checks GitHub Releases for newer versions and applies updates automatically. |
| **COPY LOG / CLEAR** | Copies the colour-coded Shinobi Battle Log to your clipboard or clears the console. |
