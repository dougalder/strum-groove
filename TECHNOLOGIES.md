# Technologies & Licenses

StrumGroove uses the following technologies and libraries, all free and open source.

## Core Technologies

| Technology | License | Usage |
|---|---|---|
| **HTML5** | W3C Standard | Document structure, semantic markup |
| **CSS3** | W3C Standard | Styling, layout (grid, flexbox), animations |
| **JavaScript (ES5)** | ECMA Standard | Application logic, no frameworks |
| **Web Audio API** | W3C Recommendation | Sound synthesis (oscillators, filters, gain nodes) |
| **Web Wake Lock API** | W3C Candidate Recommendation | Screen wake lock on iOS/Android |
| **localStorage** | W3C Standard | Persistent storage (theme preference) |

## Fonts

| Font | License | Source |
|---|---|---|
| **Nunito** | SIL Open Font License 1.1 | Google Fonts |

See [FONTS_LICENSE.txt](FONTS_LICENSE.txt) for full details.

## Standards & APIs

All browser APIs used in StrumGroove are standardized by the W3C and are natively implemented in modern browsers. No external JavaScript libraries are required.

### Web Audio API
- **Status**: W3C Recommendation
- **Usage**: Synthesizes all sounds (strum tones, drums)
- **Browser Support**: Chrome 14+, Safari 6+, Firefox 25+, Edge 12+
- **License**: W3C (free to use)
- **Reference**: https://www.w3.org/TR/webaudio/

### Screen Wake Lock API
- **Status**: W3C Candidate Recommendation
- **Usage**: Keeps screen awake on iOS 16.4+ and Android browsers
- **Browser Support**: Safari 16.4+, Chrome 84+
- **License**: W3C (free to use)
- **Reference**: https://www.w3.org/TR/screen-wake-lock/

### Web Storage API (localStorage)
- **Status**: W3C Living Standard
- **Usage**: Stores theme preference
- **Browser Support**: All modern browsers
- **License**: W3C (free to use)
- **Reference**: https://html.spec.whatwg.org/multipage/webstorage.html

## Why No Frameworks?

StrumGroove deliberately avoids JavaScript frameworks and build tools for these reasons:

1. **Performance**: Single 75 KB file, loads in <1 second
2. **Portability**: Works anywhere — download, open, use
3. **Maintenance**: No dependency updates, no version conflicts
4. **Offline**: No CDN calls after first load (fonts only)
5. **Simplicity**: Easier to understand, modify, and extend

## Privacy & Data

StrumGroove stores data **only locally** in your browser:
- Theme preference (light/dark) → localStorage
- Custom patterns → localStorage or exported JSON
- No analytics, no tracking, no servers

All data stays on your device. We never collect, store, or transmit any information about your usage.

## Licensing Summary

StrumGroove itself: **MIT License** (free to use, modify, distribute)

Dependencies:
- **Nunito Font**: SIL Open Font License 1.1 (free, with attribution)
- **All W3C Standards**: Free to implement and use

You are free to use, modify, and redistribute StrumGroove under the MIT License, provided you include the license text.
