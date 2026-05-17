# 🎵 Practice Timer — SuonARte

**Measure your real practice time** | *Misura il tuo tempo di studio reale* | *Miss deine echte Übungszeit*

> An intelligent tool for musicians that measures **actual** practice time — not just the time spent in front of the music stand.

🔗 **Live app:** [ilario1973.github.io/practice-timer](https://ilario1973.github.io/practice-timer)

---

## How it works

Practice Timer uses the **device microphone** to automatically detect when you are playing. The practice timer only advances when sound is detected — short pauses between notes do not interrupt the count.

### Detection logic

| Situation | What happens |
|---|---|
| You are playing | ✅ Practice timer advances |
| Silence < 30 seconds | ✅ Practice timer continues (short pause) |
| Silence ≥ 30 seconds | ⏸ Practice timer stops, break counter starts |
| Resume playing for 4 seconds | ▶️ Practice timer resumes (+ the 4 confirmation seconds) |

### Audio engine

- **Weighted spectral analysis per instrument** — each instrument has a sub-band map with different weights, calibrated on its fundamental frequencies
- **Adaptive background noise calibration** — in the first 3 seconds the app automatically measures the base level of the environment
- **Asymmetric smoothing** — fast response on sound attack, slow on release (avoids false stops on short notes)

---

## Supported instruments

| Instrument | Analysed band | Notes |
|---|---|---|
| 🪈 Flute | 500–4000 Hz | Fundamental frequencies weighted 3x |
| 🎻 Violin | 200–6000 Hz | Rich harmonics, high smoothing |
| 🎹 Piano | 80–5000 Hz | Attack + decay logic |
| 🎸 Guitar | 80–3000 Hz | Mid-low fundamentals |
| 🎺 Trumpet | 200–3500 Hz | Bright brass tones |
| 🥁 Drums | 60–8000 Hz | Transient detection |

---

## Features

- 🎙 Automatic sound detection via microphone
- 📊 Daily statistics (practice time, sessions, consecutive days)
- 🌍 Interface in **Italian, English and German**
- 🎚 Adjustable microphone sensitivity (5 levels)
- 💡 Screen always on during session (Android/Chrome)
- 📲 Installable as a **PWA** (Progressive Web App) on the home screen
- 🌙 Automatic dark mode
- 💾 Session history saved locally

---

## Installing as an app (PWA)

No store installation needed. Open the link in your browser and follow these steps:

**Android (Chrome)**
1. Open [ilario1973.github.io/practice-timer](https://ilario1973.github.io/practice-timer)
2. Tap the menu ⋮ → "Add to Home Screen"

**iPhone/iPad (Safari)**
1. Open [ilario1973.github.io/practice-timer](https://ilario1973.github.io/practice-timer)
2. Tap the share button ⬆ → "Add to Home Screen"

> ⚠️ On iPhone/iPad, Safari does not support screen wake lock: the display may go to standby during a session. As a workaround, increase the screen timeout in iOS Settings.

---

## Required permissions

- **Microphone** — required for audio detection. The browser will ask for permission on first launch.

> Audio is never recorded or transmitted. All processing happens locally on the device.

---

## Licence

Copyright © 2025 **Ilario Nocentini** — SuonARte

You are free to use, modify and redistribute this software provided that:
- The original author is credited: **Ilario Nocentini (SuonARte)**
- The complete source code is always made available
- **It is not used for commercial purposes** without the author's explicit written consent

For commercial use: contact the author.

---

## Version

**v1.02** — [Commit history on GitHub](https://github.com/ilario1973/practice-timer/commits/main)

---

*gli strumenti di SuonARte*
