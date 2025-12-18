# 🎵 Audio Fluid Visualizer

An immersive audio visualizer that blends a WebGL fluid simulation with a reactive waveform circle. It responds in real time to sub-bass, bass, mids, and highs with a cinematic palette of deep wine reds and blues.

## 🔴 Live Demo

**[robderoy.de/apps/sound](https://robderoy.de/apps/sound/)**

![Audio Fluid Visualizer](preview.gif)

## ✨ Features

- **WebGL Fluid Simulation** – Organic fluid motion driven by the music
- **Beat Detection** – Separate triggers for sub-bass, bass, mids, and highs
- **Waveform Circle** – Rotating circle that visualizes the waveform
- **Average Circle** – Pulsing ring based on overall loudness
- **4K Support** – Tuned for high-resolution displays
- **Playlist & Multi-select** – Load audio files (mp3, flac, wav, ogg/oga, m4a/aac, opus, weba) and playlist files (m3u/m3u8, pls, asx, xspf)
- **Mouse/Touch Interaction** – Draw into the fluid manually

## 🚀 Demo

**Live:** [robderoy.de/apps/sound](https://robderoy.de/apps/sound/)

Locally: open `index.html` in your browser, load one or more audio files or a playlist, and enjoy.

## 🎨 Color Palette

- **Sub-bass & Bass:** Deep wine red → magenta
- **Mids:** Deep indigo
- **Highs:** Deep blue

## 📁 Installation

```bash
git clone https://github.com/Wolfram33/Visual_Audio_Booster-for-Browsers.git
cd Visual_Audio_Booster-for-Browsers
# Open index.html in your browser
```

No dependencies or build tools needed — pure HTML/CSS/JavaScript.

## 🎛️ Controls

| Action | Function |
|--------|----------|
| 📁 Load Audio/Playlist | Select audio files (mp3, flac, wav, ogg/oga, m4a/aac, opus, weba) or playlist files (m3u/m3u8, pls, asx, xspf) |
| ⏮️ | Previous track |
| ▶️ / ⏸️ | Play / Pause |
| ⏭️ | Next track |
| Drag with mouse/touch | Draw into the fluid |

## 🆕 What changed

- Broader audio support: mp3, flac, wav, ogg/oga, m4a/aac, opus, weba.
- Native playlist support: m3u/m3u8, pls, asx, xspf (local entries are matched to uploaded files; remote URLs are used directly).

## 🙏 Credits & Attribution

This project combines and extends the excellent work of:

### WebGL Fluid Simulation
**Pavel Dobryakov**
- GitHub: [github.com/PavelDoGreat/WebGL-Fluid-Simulation](https://github.com/PavelDoGreat/WebGL-Fluid-Simulation)
- Foundation for the fluid simulation
- MIT License

### Waveform Circle & Average Circle
**Noel Delgado** (@pixelia_me)
- CodePen: [codepen.io/noeldelgado/pen/EaNjBy](https://codepen.io/noeldelgado/pen/EaNjBy)
- Website: [pixelia.me](https://pixelia.me)
- Inspiration for the waveform circle and average circle
- Music in the original demo: Term and Conditions Mixes

### Combination & Extensions
**Rob de Roy** – [www.robderoy.de](https://www.robderoy.de)
- Audio-reactive fluid tuning
- Beat detection for sub-bass, bass, mids, highs
- Color optimization for dark, atmospheric visuals
- 4K display tuning
- Playlist functionality

## 📄 License

MIT License – see [LICENSE](LICENSE)

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

## 🤝 Contributing

Pull requests are welcome! For larger changes, please open an issue first.

## 💡 Ideas for Extensions

- [ ] Microphone input support
- [ ] Switchable color schemes
- [ ] Fullscreen button
- [ ] Adjustable sensitivity
- [ ] Export to video

---

Made with 🎵 and WebGL
