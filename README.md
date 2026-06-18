# 🎵 Audio Fluid Visualizer

Ein immersiver Audio-Visualizer, der mehrere fortgeschrittene Web-Technologien zu einem einheitlichen System vereint. Die Integration von WebGL Fluid Simulation, Echtzeit-Audio-Analyse, Beat-Detection und reaktiver Waveform-Visualisierung erforderte umfangreiche Entwicklungsarbeit in den Bereichen Audio-Processing, Shader-Programmierung und Performance-Optimierung. Das System reagiert in Echtzeit auf Sub-Bass, Bass, Mitten und Höhen mit einer kinematischen Palette aus tiefen Weinrot- und Blautönen.

## 🔴 Live Demo

**[robderoy.de/apps/sound](https://robderoy.de/apps/sound/)**

![Audio Fluid Visualizer](auio-visualisierung.gif)

## ✨ Features

- **WebGL Fluid Simulation** – Organische Flüssigkeitsbewegung, die von der Musik angetrieben wird
- **Beat Detection** – Separate Trigger für Sub-Bass, Bass, Mitten und Höhen
- **Waveform Circle** – Rotierender Kreis, der die Wellenform visualisiert
- **Average Circle** – Pulsierender Ring basierend auf der Gesamtlautstärke
- **4K Support** – Optimiert für hochauflösende Displays
- **Playlist & Multi-Select** – Laden von Audiodateien (mp3, flac, wav, ogg/oga, m4a/aac, opus, weba) und Playlist-Dateien (m3u/m3u8, pls, asx, xspf)
- **Maus-/Touch-Interaktion** – Manuelles Zeichnen in die Flüssigkeit
- **Auswahl eines Hintergrundbildes** – Cover, gestreckt oder Original
- **Verwende eine Farben**
- **Eigene Amplituden-Höher einstellen**

## 🚀 Demo

**Live:** [robderoy.de/apps/sound](https://robderoy.de/apps/sound/)

**Lokal:** Öffne `index.html` in deinem Browser, lade eine oder mehrere Audiodateien oder eine Playlist und genieße.

## 🎨 Farbpalette

- Öffne das Farb-Panel über den Button "🎨 Farben".
- Overlay steuern:
  - Waveform: Stroke/Fill jeweils für Normal und Peak.
  - Average Circle: Line/Fill jeweils für Normal und Peak, inkl. separater Alpha-Regler.
- Fluid-Farben: Eigene Farben für Sub, Bass A/B, Mid, Treble A/B.
- Persistenz: Einstellungen werden in `localStorage` (`vab_palette`) gespeichert und beim Start geladen.
- Zurücksetzen: Stellt die Standardpalette wieder her.
- Hinweis: Nur Farben/Helligkeit werden geändert, Physik/Bewegung bleibt unverändert.

## 📁 Installation

```bash
git clone https://github.com/Wolfram33/Visual_Audio_Booster-for-Browsers.git
cd Visual_Audio_Booster-for-Browsers
# Öffne index.html in deinem Browser
```

Keine Abhängigkeiten oder Build-Tools erforderlich — reines HTML/CSS/JavaScript.

## 🎛️ Steuerung

| Aktion | Funktion |
|--------|----------|
| 📁 Audio/Playlist laden | Audiodateien (mp3, flac, wav, ogg/oga, m4a/aac, opus, weba) oder Playlist-Dateien (m3u/m3u8, pls, asx, xspf) auswählen |
| ⏮️ | Vorheriger Track |
| ▶️ / ⏸️ | Abspielen / Pause |
| ⏹️ Stopp | Wiedergabe stoppen und auf den Anfang zurückspulen |
| ⏭️ | Nächster Track |
| 🎨 Farben | Farb-Panel ein-/ausblenden |
| 🖼️ Hintergrund | Hintergrundbild-Panel ein-/ausblenden |
| Ziehen mit Maus/Touch | In die Flüssigkeit zeichnen |

## 🆕 Änderungen

**Neueste Version**

- Kick-basierte Beat-Detection: Der dominante Hauptbeat wird über ein eigenes Bassdrum-Band (50–120 Hz) erkannt – mit adaptiver Schwelle (laufender Mittelwert + Standardabweichung) und Refraktärzeit gegen Doppeltrigger. Fein justierbar über `KICK_SENSITIVITY`, `KICK_REFRACTORY`, `KICK_PUMP` und `KICK_FORCE`.
- Auflösungsunabhängige Frequenzbänder: Bänder werden in Hertz definiert und intern auf die aktuelle `fftSize`/`sampleRate` gemappt – gleiches Verhalten unabhängig von der Bildschirmauflösung.
- Stopp-Button: Pausiert die Wiedergabe und spult auf den Anfang zurück (Play startet den Track wieder von vorne).
- Strikte CSP möglich: Keine Inline-Scripts oder `on*`-Attribute mehr – sämtliche Bedienelemente werden per `addEventListener` verdrahtet, das JavaScript ist vollständig ausgelagert.
- Klar unterscheidbare Bedienelemente: Funktions-Farben statt Grau-in-Grau (Grün = Laden, Blau = Navigation, Orange = Stopp/Entfernen, Braun = Werkzeuge/Auswahl) mit sichtbarem Aktiv-Zustand.
- Responsive Bedienleiste: Bricht auf kleinen Bildschirmen um, touch-freundliche Buttongrößen.

**Frühere Änderungen**

- Farb-Panel: Live anpassbare Palette für Overlay (inkl. Alpha) und Fluid.
- Persistenz: Speichert Benutzerfarben in `localStorage` und lädt sie beim Start.
- Adaptive FFT: `analyser.fftSize` passt sich der Bildschirmauflösung an (512/1024/2048/4096).
- Blau-Intensität (Mid/Treble) verstärkt für bessere Sichtbarkeit.
- Erweiterte Audio-Unterstützung: mp3, flac, wav, ogg/oga, m4a/aac, opus, weba.
- Native Playlist-Unterstützung: m3u/m3u8, pls, asx, xspf (lokale Einträge werden mit hochgeladenen Dateien abgeglichen; Remote-URLs werden direkt verwendet).

## 🙏 Credits & Danksagungen

Dieses Projekt kombiniert und erweitert die exzellente Arbeit von:

### WebGL Fluid Simulation
**Pavel Dobryakov**
- GitHub: [github.com/PavelDoGreat/WebGL-Fluid-Simulation](https://github.com/PavelDoGreat/WebGL-Fluid-Simulation)
- Grundlage für die Fluid-Simulation
- MIT Lizenz

### Waveform Circle & Average Circle
**Noel Delgado** (@pixelia_me)
- CodePen: [codepen.io/noeldelgado/pen/EaNjBy](https://codepen.io/noeldelgado/pen/EaNjBy)
- Website: [pixelia.me](https://pixelia.me)
- Inspiration für Waveform Circle und Average Circle
- Musik im Original-Demo: Term and Conditions Mixes

### Umfangreiche System-Integration & Eigenentwicklung
**Rob de Roy** – [www.robderoy.de](https://www.robderoy.de)

**Technische Kernentwicklung:**
- **Audio-Engine Integration:** Vollständige WebAudio API Implementierung mit AnalyserNode, frequenzspezifischer Filterung und Echtzeit-FFT-Analyse
- **Advanced Beat Detection System:** Eigenentwickelte Multi-Band-Erkennung für Sub-Bass (20-60Hz), Bass (60-250Hz), Mitten (250Hz-2kHz) und Höhen (2kHz+) mit adaptiven Schwellwerten
- **Audio-Reactive Fluid Dynamics:** Komplexe Mapping-Logik zwischen Frequenzbändern und WebGL-Shader-Parametern (Splat-Radius, Velocity, Curl, Dissipation)
- **Multi-Emitter System:** 5-Punkt-Emitter-Array mit frequenzbasierter Farbzuordnung und dynamischer Positionierung
- **Dual-Canvas Rendering Pipeline:** Synchronisierte Darstellung von WebGL-Fluid (Background) und 2D-Overlay (Waveform/Average Circle)
- **Performance-Optimierung:** Frame-Timing, RequestAnimationFrame-Synchronisation, Audio-Buffer-Management für flüssige 60fps auch bei 4K
- **Playlist-Engine:** Parser für M3U/M3U8, PLS, ASX, XSPF mit Multi-Format-Audio-Support (MP3, FLAC, WAV, OGG/OGA, M4A/AAC, Opus, WebA)
- **Color System:** Frequenz-zu-Farb-Mapping mit HSL-Berechnungen für atmosphärische Visualisierung
- **Cross-Browser Compatibility:** WebGL 1/2 Fallback-Logic, Audio-Context-Handling, Touch-/Mouse-Event-Normalisierung

**Entwicklungsaufwand:**
Die Integration der verschiedenen Technologien und die Entwicklung eines stabilen, performanten Systems stellte erhebliche technische Herausforderungen dar. Die Synchronisation von Audio-Analyse, Shader-basierter Fluid-Simulation und Canvas-Rendering erforderte intensive Arbeit an Timing, Memory-Management und Browser-Kompatibilität.

## 📄 Lizenz

MIT Lizenz – siehe [LICENSE](LICENSE)

```
MIT License

Copyright (c) 2024

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

## 🤝 Mitwirken

Pull Requests sind willkommen! Bei größeren Änderungen bitte zuerst ein Issue öffnen.

## 💝 Unterstützung

Wenn dir dieses Projekt gefällt, kannst du mich mit einer kleinen Spende unterstützen:

[![PayPal](https://img.shields.io/badge/PayPal-Spenden-blue?logo=paypal)](https://www.paypal.com/paypalme/robderoy)

Oder direkt via PayPal an: **robderoy@protonmail.ch**

---
Ideen, was man noch für Funktionen einbauen könnte?
Gemacht mit 🎵 und WebGL
