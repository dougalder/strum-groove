# StrumGroove v2.7 — Strum Trainer

A self-contained web app to help guitarists and ukulele players learn and practice strumming patterns. Built entirely in HTML, CSS, and vanilla JavaScript — no dependencies, no servers, no signup required.

## Features

✨ **46 Built-in Patterns**  
Classic strumming patterns for folk, pop, rock, reggae, waltz, funk, flamenco, and more.

🎵 **Web Audio Synthesis**  
All sounds are generated on-the-fly using the Web Audio API. No audio files to download.

🥁 **Complementary Drum Patterns**  
6 drum presets (rock, reggae, bossa, waltz, folk, funk) play underneath your strums. Independent volume control lets you focus on the strum pattern once you've got the timing down.

⚡ **Build Your Own Beat**  
Create custom patterns by tapping 8 slots through Rest → Down → Up → Ghost cycles. Save, edit, or duplicate as many as you want.

📋 **Queue & Playback**  
Build a practice session by queueing patterns with repeat counts. Practice at your own tempo (40–200 BPM).

💾 **Save & Load**  
Export your custom patterns and queue as JSON. Import patterns from other sessions or share with friends.

🎨 **Light & Dark Mode**  
Toggle between light and dark themes; preference is saved automatically.

💡 **Screen Wake Lock (iOS 16.4+)**  
Keep your screen awake while practicing — tap the bulb icon in the header.

🔊 **Sound Options**  
Choose from warm, bright, mellow, and sharp sounds for both down and up strokes.

## Getting Started

1. **Open the app**: Download `strumgroove.html` and open it in any modern browser (Chrome, Safari, Firefox, Edge)
2. **No installation needed** — the entire app runs in your browser
3. **On mobile**: Add to your Home Screen (iOS Safari) or install as PWA (Chrome/Android) for offline access
4. **Offline**: After the initial load, the app works completely offline (only Google Fonts require internet)

## How to Use

### Play Tab
- Select a pattern from the grid
- Adjust tempo with BPM slider or presets (40, 60, 80, 100, 120, 140, 160, 180, 200)
- Toggle drums on/off and adjust volume
- Press the play button (▶) to hear the pattern
- Each beat is highlighted as it plays; lights flash orange for downstrokes, teal for upstrokes

### Patterns Tab
- Click any pattern tile to see the full beat diagram with colour-coded arrows
- **Orange arrows** = downstroke  
- **Teal arrows** = upstroke  
- **Grey dashed arrows** = ghost/muted strum  
- **Faded circles** = rest (silence)
- **⧉ Duplicate & Edit** button lets you copy any pattern to customize

### Build Your Own Beat
- Tap each of the 8 slots to cycle through Rest → Down → Up → Ghost
- Preview before saving
- Name your pattern and click **+ Add to Patterns**
- Your patterns appear in a teal-highlighted **My Patterns** section with edit (✏️) and delete (✕) buttons
- Edit a pattern by clicking the pencil icon; click ✕ to delete it

### Queue Tab
- Add patterns to your practice session
- Set repeat counts for each pattern
- Reorder by dragging the handle (⠿)
- Watch progress as patterns play in sequence

### Sounds Tab
- Choose different sounds for down and up strokes:
  - **Warm** — mellow, acoustic tone
  - **Bright** — clear, ringing tone
  - **Mellow** — soft, rounded tone
  - **Sharp** — crisp, percussive tone
- Toggle sound on/off with the sound panel header

### Files Tab
- **Export** saves your custom patterns and current queue as a timestamped JSON file
- **Import** loads patterns from a file (merges with existing, never overwrites)
- About section explains how the app works

### Screen Wake Lock (iOS 16.4+ Safari)
- Tap the 💡 bulb icon in the header to keep your screen awake
- Icon turns orange when active; tap again to release

## Technologies Used

- **HTML5**: Semantic markup, Web Audio API, Web Wake Lock API
- **CSS3**: CSS custom properties (variables), grid layout, flexbox, media queries
- **JavaScript (ES5)**: Vanilla, no frameworks or build tools
- **Web Audio API**: Oscillators, noise buffers, and gain nodes for sound synthesis
- **Google Fonts**: Nunito family (open source)
- **LocalStorage**: Theme preference persistence

## Browser Support

- **Desktop**: Chrome 86+, Safari 14+, Firefox 79+, Edge 86+
- **Mobile**: Safari 14.4+ (iOS), Chrome 86+ (Android)
- **Features requiring OS support**:
  - Screen Wake Lock (iOS 16.4+ Safari, Chrome 84+)
  - Clipboard paste (most modern browsers)

## Performance

- **File size**: ~75 KB (single HTML file, no external dependencies except fonts)
- **Load time**: ~500ms–1s on typical connection
- **Offline**: Fully functional after first load
- **Storage**: ~5–50 KB for localStorage theme preference and custom patterns

## Credits

- **Built with**: HTML, CSS, vanilla JavaScript
- **Design inspired by**: Modern minimalist interfaces with focus on clarity and usability
- **Audio synthesis**: Web Audio API
- **Font**: Nunito by Vernon Adams, Cyreal, and Google Fonts

## License

StrumGroove is released under the **MIT License**. See LICENSE file for details.

### Third-Party Licenses

- **Nunito Font** (Google Fonts): SIL Open Font License 1.1 — see FONTS_LICENSE.txt
- **Web Audio API**: W3C Recommendation (browser-native)
- **Web Wake Lock API**: W3C Candidate Recommendation (browser-native)

## Roadmap & Feedback

- **Custom time signatures** (3/4, 5/4, 6/8 with smart builders)
- **Pattern difficulty ratings** for progression
- **Metronome click track** option
- **Chord voicing suggestions** paired with patterns
- **Community pattern sharing** (open to discussion)

Have feedback? Found a bug? Want to contribute patterns? Open an issue or reach out!

## Development

The app is a single, self-contained HTML file with no build process. To modify:

1. Edit `strumgroove.html` in any text editor
2. Open in a browser to test
3. All changes are instant (no compilation needed)

To add new patterns, edit the `PATTERNS_BUILTIN` array in the JavaScript section. Each pattern object needs:
- `n`: unique number
- `name`: display name
- `desc`: short description
- `goodFor`: usage context (e.g., "folk and country")
- `steps`: array of step types (`'D'`, `'U'`, `'R'`, `'gD'`)

---

**StrumGroove**: Learn. Practice. Groove. 🎸🎵
