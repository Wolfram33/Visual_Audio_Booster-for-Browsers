## ✨ Was ist neu in v1.1.0

### 🎨 Farb-Panel (Neu!)
- Live anpassbare Palette für Overlay (Waveform & Circle) und Fluid-Effekte
- Color-Picker für individuelle Anpassung ohne Physik zu beeinflussen
- Alpha-Regler für Circle-Transparenz (Line/Fill, normal/Peak)
- Farb-Einstellungen werden in `localStorage` gespeichert

### ⚡ Performance & Kompatibilität
- Adaptive `analyser.fftSize`: 512 (HD), 1024 (Full HD), 2048 (4K), 4096 (4K+)
- Blau-Intensität (Mid/Treble) 3x verstärkt für bessere Sichtbarkeit
- Automatische Anpassung an Bildschirmauflösung

### 📚 Anleitung
1. Öffne das Farb-Panel über "🎨 Farben" Button
2. Passe Overlay- und Fluid-Farben per Color-Picker an
3. Regle Alpha über die Slider (nur für Circle)
4. Einstellungen werden automatisch gespeichert
5. "Zurücksetzen" stellt die Standardpalette wieder her

---

**Technische Details:**
- Farb-Palette in `index.js` mit Getter/Setter-Logik
- Persistenz via `localStorage` (`vab_palette`)
- Zeichenfunktionen (`drawWaveform()`, `drawAverageCircle()`) lesen aus Palette
- Keine Änderungen an Fluid-Physik oder Audio-Analyse

**Credits:** Rob de Roy – www.robderoy.de
