# Mario Digital Signature

A static digital signature page with Matrix-style digital rain effects and SVG logo.

## Technical Specification

### Architecture
- HTML5 with semantic markup and accessibility features
- SVG logo for scalable rendering
- CSS3 with custom properties, animations, and @font-face declarations
- Vanilla JavaScript with secure DOM manipulation
- Static hosting, no backend required

### Security
- Content Security Policy (CSP) implementation
- XSS prevention through safe DOM methods
- No external dependencies
- Security headers: X-Frame-Options, X-Content-Type-Options, Permissions-Policy

### Performance
- Memory leak prevention with automatic cleanup
- Rate limiting for DOM operations
- Visibility API integration
- Reduced motion support
- Maximum 80 concurrent rain columns

### Color Scheme
```css
--bg-color: #0a0a0a           /* Background */
--rain-color: #9333ea         /* Rain color */
--rain-opacity: 0.15           /* Rain opacity */
--logo-color: #000000         /* Logo color */
```

### Typography
- Primary: JetBrains Mono (self-hosted WOFF2)
- Fallback: SF Mono, Monaco, Menlo, Consolas, monospace
- Weights: 400, 700

### Animations
- Matrix Rain: 15-25s duration, immediate initialization
- Orbital Drift: 25s figure-8 pattern
- JavaScript: Immediate DOM execution

### File Structure
```
digitalcard/
├── index.html          # Main HTML document
├── css/style.css       # Styles and animations
├── js/main.js          # Matrix rain engine
├── fonts/              # JetBrains Mono fonts
├── .github/workflows/  # GitHub Pages deployment
├── netlify.toml        # Netlify config
├── vercel.json         # Vercel config
└── README.md           # Documentation
```

### Deployment
- GitHub Pages: Automated via workflow
- Netlify: Configuration provided
- Vercel: Configuration provided
- Manual: Copy to any static host

### Browser Support
- Modern browsers (Chrome 60+, Firefox 55+, Safari 12+, Edge 79+)
- Mobile responsive

### Configuration
Modify `js/main.js`:
```javascript
const CONFIG = {
    INITIAL_COLUMNS: 40,        // Starting columns
    COLUMN_CREATION_INTERVAL: 300,  // Interval (ms)
    MAX_COLUMNS: 80,            // Max columns
    MIN_COLUMN_LENGTH: 10,      // Min length
    MAX_COLUMN_LENGTH: 30,      // Max length
    MIN_ANIMATION_DURATION: 15,  // Min duration
    MAX_ANIMATION_DURATION: 25   // Max duration
};
```