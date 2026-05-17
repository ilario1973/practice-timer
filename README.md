# 🎵 Practice Timer — SuonARte

**Misura il tuo tempo di studio reale** | *Measure your real practice time* | *Miss deine echte Übungszeit*

> Uno strumento intelligente per musicisti che vuole misurare il tempo **effettivo** di pratica, non quello trascorso davanti allo spartito.

🔗 **App live:** [ilario1973.github.io/practice-timer](https://ilario1973.github.io/practice-timer)

---

## Come funziona

Practice Timer usa il **microfono del dispositivo** per rilevare automaticamente quando stai suonando. Il timer della pratica avanza solo quando c'è suono — le pause brevi tra una nota e l'altra non interrompono il conteggio.

### Logica di rilevamento

| Situazione | Cosa succede |
|---|---|
| Stai suonando | ✅ Timer pratica avanza |
| Silenzio < 30 secondi | ✅ Timer pratica continua (pausa breve) |
| Silenzio ≥ 30 secondi | ⏸ Timer pratica si ferma, inizia contatore pause |
| Riprendi a suonare per 4 secondi | ▶️ Timer pratica riprende (+ i 4 secondi di conferma) |

### Motore audio

- **Analisi spettrale pesata per strumento** — ogni strumento ha una mappa di sub-bande con pesi diversi, calibrata sulle sue frequenze fondamentali
- **Calibrazione adattiva del rumore di fondo** — nei primi 3 secondi l'app misura automaticamente il livello base dell'ambiente
- **Smoothing asimmetrico** — risposta rapida all'attacco del suono, lenta al rilascio (evita falsi stop su note brevi)

---

## Strumenti supportati

| Strumento | Banda analizzata | Note |
|---|---|---|
| 🪈 Flauto traverso | 500–4000 Hz | Frequenze fondamentali pesate 3x |
| 🎻 Violino | 200–6000 Hz | Armonici ricchi, smoothing alto |
| 🎹 Pianoforte | 80–5000 Hz | Logica attacco + decadimento |
| 🎸 Chitarra | 80–3000 Hz | Fondamentali medio-basse |
| 🎺 Tromba | 200–3500 Hz | Ottoni brillanti |
| 🥁 Batteria | 60–8000 Hz | Rilevamento transitori |

---

## Funzionalità

- 🎙 Rilevamento automatico del suono via microfono
- 📊 Statistiche giornaliere (tempo pratica, sessioni, giorni consecutivi)
- 🌍 Interfaccia in **italiano, inglese e tedesco**
- 🎚 Sensibilità microfono regolabile (5 livelli)
- 💡 Schermo sempre acceso durante la sessione (Android/Chrome)
- 📲 Installabile come **PWA** (Progressive Web App) sulla schermata home
- 🌙 Dark mode automatica
- 💾 Storico sessioni salvato localmente

---

## Installazione come app (PWA)

Non è necessario installare nulla da uno store. Apri il link nel browser e segui questi passi:

**Android (Chrome)**
1. Apri [ilario1973.github.io/practice-timer](https://ilario1973.github.io/practice-timer)
2. Tocca il menu ⋮ → "Aggiungi a schermata Home"

**iPhone/iPad (Safari)**
1. Apri [ilario1973.github.io/practice-timer](https://ilario1973.github.io/practice-timer)
2. Tocca il tasto condividi ⬆ → "Aggiungi a schermata Home"

> ⚠️ Su iPhone/iPad Safari non supporta il blocco dello schermo: il display potrebbe andare in standby durante la sessione. Aumenta il timeout schermo nelle Impostazioni iOS come soluzione alternativa.

---

## Permessi richiesti

- **Microfono** — necessario per il rilevamento audio. Il browser chiederà il permesso al primo avvio.

> L'audio non viene mai registrato né trasmesso. Tutto il processing avviene localmente sul dispositivo.

---

## Licenza

Copyright © 2025 **Ilario Nocentini** — SuonARte

È consentito usare, modificare e ridistribuire questo software a condizione che:
- Venga citato l'autore originale: **Ilario Nocentini (SuonARte)**
- Il codice sorgente completo venga sempre reso disponibile
- **Non venga usato per scopi commerciali** senza esplicito consenso scritto dell'autore

Per usi commerciali: contattare l'autore.

---

## Versione

**v1.02** — [Cronologia modifiche su GitHub](https://github.com/ilario1973/practice-timer/commits/main)

---

*gli strumenti di SuonARte*
