# Sorter Web — Project Guide

## Frontend Design Skill

This project uses a distinctive, production-grade frontend aesthetic. When building or modifying any UI, follow these guidelines.

### Design Thinking

Before coding, understand the context and commit to a clear aesthetic direction:

- **Purpose**: What problem does this interface solve? Who uses it?
- **Tone**: Pick an extreme — brutally minimal, maximalist chaos, retro-futuristic, organic/natural, luxury/refined, playful/toy-like, editorial/magazine, brutalist/raw, art deco/geometric, soft/pastel, industrial/utilitarian. Use these for inspiration but design one that is true to the aesthetic direction.
- **Constraints**: Technical requirements (framework, performance, accessibility).
- **Differentiation**: What makes this UNFORGETTABLE? What's the one thing someone will remember?

Choose a clear conceptual direction and execute it with precision. Bold maximalism and refined minimalism both work — the key is intentionality, not intensity.

### Aesthetics Guidelines

- **Typography**: Choose fonts that are beautiful, unique, and interesting. Avoid generic fonts like Arial and Inter. Pair a distinctive display font with a refined body font.
- **Color & Theme**: Commit to a cohesive aesthetic. Use CSS variables for consistency. Dominant colors with sharp accents outperform timid, evenly-distributed palettes.
- **Motion**: Prioritize CSS-only animations. Focus on high-impact moments — one well-orchestrated page load with staggered reveals creates more delight than scattered micro-interactions. Use scroll-triggering and hover states that surprise.
- **Spatial Composition**: Unexpected layouts. Asymmetry. Overlap. Diagonal flow. Grid-breaking elements. Generous negative space OR controlled density.
- **Backgrounds & Visual Details**: Create atmosphere and depth. Apply gradient meshes, noise textures, geometric patterns, layered transparencies, dramatic shadows, and grain overlays where appropriate.

**Never** use: overused font families (Inter, Roboto, Arial, system fonts), clichéd color schemes (purple gradients on white), predictable layouts, or cookie-cutter patterns that lack context-specific character.

### Current Aesthetic

The Sorter landing page uses a **clean macOS aesthetic**:
- Font stack: `-apple-system, BlinkMacSystemFont, "SF Pro Display"`
- Palette: Blue (`#0071e3`) / White / Slate (`#1d1d1f`)
- Frosted glass nav, subtle drop shadows, ample white space
- All Apple asset usage must comply with Apple Marketing Guidelines

### Project Structure

```
sorter-web/
├── index.html       — single-page landing
├── styles.css       — all styles via CSS custom properties
├── CNAME            — sorterapp.net
└── assets/
    ├── icon.png     — 1024×1024 app icon (from AppIcon.icns)
    └── mas-badge.svg — official Apple Mac App Store badge (do not modify)
```

All paths are root-relative. No build step — pure HTML/CSS/JS deployed via GitHub Pages.

### Apple Compliance

- Use only official Apple badge artwork (`assets/mas-badge.svg`) — never recreate it
- Include trademark credit in the footer when the badge is present
- Correct terminology: "Mac App Store", "macOS" — never "Apple App Store" or "OSX"
- Update `href="#"` on the badge link once the App Store URL is known

### Contact Form

Submissions go to `rubie@sorterapp.net` via Formspree (`mwvwrazv`).
Uses `@formspree/ajax@1` CDN — no build step needed.
The `mailto:rubie@sorterapp.net` link is retained as a fallback.
