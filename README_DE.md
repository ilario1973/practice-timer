# 🎵 Practice Timer — SuonARte

**Miss deine echte Übungszeit** | *Misura il tuo tempo di studio reale* | *Measure your real practice time*

> Ein intelligentes Werkzeug für Musiker, das die **tatsächliche** Übungszeit misst — nicht nur die Zeit, die vor dem Notenständer verbracht wird.

🔗 **Live-App:** [ilario1973.github.io/practice-timer](https://ilario1973.github.io/practice-timer)

---

## So funktioniert es

Practice Timer verwendet das **Gerätemikrofon**, um automatisch zu erkennen, wann du spielst. Der Übungstimer läuft nur, wenn Klang erkannt wird — kurze Pausen zwischen Noten unterbrechen die Zählung nicht.

### Erkennungslogik

| Situation | Was passiert |
|---|---|
| Du spielst | ✅ Übungstimer läuft |
| Stille < 30 Sekunden | ✅ Übungstimer läuft weiter (kurze Pause) |
| Stille ≥ 30 Sekunden | ⏸ Übungstimer stoppt, Pausenzähler startet |
| 4 Sekunden lang wieder spielen | ▶️ Übungstimer läuft weiter (+ die 4 Bestätigungssekunden) |

### Audio-Engine

- **Gewichtete Spektralanalyse je Instrument** — jedes Instrument hat eine Sub-Band-Karte mit unterschiedlichen Gewichtungen, kalibriert auf seine Grundfrequenzen
- **Adaptive Hintergrundgeräusch-Kalibrierung** — in den ersten 3 Sekunden misst die App automatisch den Grundpegel der Umgebung
- **Asymmetrisches Smoothing** — schnelle Reaktion beim Tonanstieg, langsam beim Abklingen (verhindert falsches Stoppen bei kurzen Noten)

---

## Unterstützte Instrumente

| Instrument | Analysiertes Band | Hinweise |
|---|---|---|
| 🪈 Querflöte | 500–4000 Hz | Grundfrequenzen 3-fach gewichtet |
| 🎻 Geige | 200–6000 Hz | Reiche Obertöne, hohes Smoothing |
| 🎹 Klavier | 80–5000 Hz | Anschlag- und Abklinglogik |
| 🎸 Gitarre | 80–3000 Hz | Mittel-tiefe Grundfrequenzen |
| 🎺 Trompete | 200–3500 Hz | Helle Blechbläserklänge |
| 🥁 Schlagzeug | 60–8000 Hz | Transienten-Erkennung |

---

## Funktionen

- 🎙 Automatische Klangerkennung über Mikrofon
- 📊 Tagesstatistiken (Übungszeit, Sitzungen, aufeinanderfolgende Tage)
- 🌍 Benutzeroberfläche auf **Italienisch, Englisch und Deutsch**
- 🎚 Einstellbare Mikrofonempfindlichkeit (5 Stufen)
- 💡 Bildschirm bleibt während der Sitzung an (Android/Chrome)
- 📲 Als **PWA** (Progressive Web App) auf dem Startbildschirm installierbar
- 🌙 Automatischer Dunkelmodus
- 💾 Sitzungsverlauf lokal gespeichert

---

## Als App installieren (PWA)

Keine Installation aus einem Store nötig. Öffne den Link im Browser und folge diesen Schritten:

**Android (Chrome)**
1. Öffne [ilario1973.github.io/practice-timer](https://ilario1973.github.io/practice-timer)
2. Tippe auf das Menü ⋮ → „Zum Startbildschirm hinzufügen"

**iPhone/iPad (Safari)**
1. Öffne [ilario1973.github.io/practice-timer](https://ilario1973.github.io/practice-timer)
2. Tippe auf die Teilen-Schaltfläche ⬆ → „Zum Home-Bildschirm"

> ⚠️ Auf iPhone/iPad unterstützt Safari kein Wake Lock: Der Bildschirm kann während einer Sitzung in den Standby gehen. Erhöhe als Workaround das Bildschirm-Timeout in den iOS-Einstellungen.

---

## Erforderliche Berechtigungen

- **Mikrofon** — für die Audioerkennung erforderlich. Der Browser fragt beim ersten Start nach der Erlaubnis.

> Audio wird niemals aufgezeichnet oder übertragen. Die gesamte Verarbeitung erfolgt lokal auf dem Gerät.

---

## Lizenz

Copyright © 2025 **Ilario Nocentini** — SuonARte

Die Nutzung, Änderung und Weitergabe dieser Software ist gestattet, sofern:
- Der ursprüngliche Autor genannt wird: **Ilario Nocentini (SuonARte)**
- Der vollständige Quellcode immer verfügbar gemacht wird
- **Keine kommerzielle Nutzung** ohne ausdrückliche schriftliche Genehmigung des Autors erfolgt

Für kommerzielle Nutzung: Autor kontaktieren.

---

## Version

**v1.02** — [Commit-Verlauf auf GitHub](https://github.com/ilario1973/practice-timer/commits/main)

---

*gli strumenti di SuonARte*
