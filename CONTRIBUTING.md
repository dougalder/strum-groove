# Contributing to StrumGroove

Thank you for your interest in contributing! StrumGroove is open source and welcomes contributions from the community.

## How to Contribute

### Reporting Issues
If you find a bug or have a suggestion:
1. Check [existing issues](https://github.com/yourusername/strumgroove/issues) first
2. Open a new issue with:
   - Clear description of the problem
   - Steps to reproduce (for bugs)
   - Expected vs. actual behavior
   - Screenshots if applicable
   - Device/browser info (especially for mobile issues)

### Feature Requests
Have an idea? We'd love to hear it:
1. Open an issue with the **enhancement** label
2. Describe the feature and why it would be useful
3. If possible, explain how you'd use it in your practice

### Code Contributions

#### Setup
1. Fork the repository
2. Clone your fork: `git clone https://github.com/yourusername/strumgroove.git`
3. No build process needed — edit `strumgroove.html` directly
4. Test in your browser by opening the file locally

#### Making Changes
1. Create a descriptive branch: `git checkout -b feature/my-feature`
2. Make your changes to `strumgroove.html`
3. Test thoroughly in multiple browsers/devices
4. Keep changes focused and atomic

#### Testing Before Submitting
- **Desktop**: Chrome, Safari, Firefox, Edge
- **Mobile**: iOS Safari, Android Chrome
- **Both themes**: Test light and dark mode
- **Screen sizes**: Desktop, tablet, phone

#### Submitting a Pull Request
1. Push to your fork
2. Open a pull request with:
   - Clear description of what changed and why
   - Reference any related issues (#123)
   - Screenshots if UI changes
   - Test results (browsers tested, etc.)

### Adding Strumming Patterns
Want to add new patterns? 

1. Find the `PATTERNS_BUILTIN` array in `strumgroove.html`
2. Each pattern needs:
   ```javascript
   {
     n: 47,  // unique number (increment from highest)
     name: "Your Pattern Name",
     desc: "Short description",
     goodFor: "Context for when to use this pattern",
     steps: ['D', 'D', 'U', 'D', 'U']  // array of 'D', 'U', 'R', 'gD'
   }
   ```
3. Test your pattern:
   - Click in the Patterns grid to view the beat diagram
   - Play it on the Play tab at different tempos
   - Verify it works on mobile

### Code Style Guidelines

- **No external dependencies** — keep it vanilla JavaScript
- **Keep it readable** — comments for complex logic
- **Use meaningful names** — variables should be clear
- **No minification** — we want readable code
- **One file** — all HTML, CSS, JS in `strumgroove.html`

### JavaScript Style
```javascript
// Good: clear names, comments
function playDown() {
  // Create oscillator for downstroke sound
  var osc = audioCtx.createOscillator();
  // ... rest of function
}

// Avoid: unclear names, no comments
function pD() {
  var o = audioCtx.createOscillator();
  // ...
}
```

### CSS Style
- Use CSS custom properties (variables) for colors
- Mobile-first approach: start simple, enhance for larger screens
- Use semantic class names: `.builder-btn` not `.btn-blue`

### Documentation
If your change affects how the app works:
1. Update `MANUAL.md` with user-facing changes
2. Update `README.md` if it affects key features
3. Update `TECHNOLOGIES.md` if adding new dependencies (though we avoid this)

## Community Standards

- **Be respectful** — we're all here because we love music and learning
- **Be constructive** — focus on the idea, not the person
- **Give credit** — mention contributors in your PR
- **Test your work** — don't break existing functionality

## Questions?

- Check the `README.md` for project info
- Read the `MANUAL.md` for how the app works
- Look at existing issues/PRs for similar questions

---

**Thank you for contributing to StrumGroove!** 🎸🎵

Learn. Practice. Groove.
