# Minimal Website Design Principles

## Core Philosophy
**"Security through simplicity. Speed through minimalism."**

This document outlines ultra-minimal web design principles inspired by the "motherfuckingwebsite.com" philosophy, adapted for those who value security, speed, and substance over flashy design.

## Design Rules

### 1. Layout & Structure
- **Max width**: 73% of viewport
- **Margin**: 5% auto (centered)
- **Mobile**: 95% width with 5% margin on small screens
- **No containers, wrappers, or complex grid systems**
- **Semantic HTML5**: Use proper heading hierarchy (h1, h2, h3)

### 2. Typography
- **Font stack**: `-apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif`
- **Font size**: 16px base (never smaller)
- **Line height**: 1.8 (generous breathing room)
- **Text shadow**: `0 1px 0 #ffffff` (subtle enhancement)
- **No web fonts** - system fonts only for speed

### 3. Colors
- **Background**: `#f2f2f2` (soft off-white)
- **Text**: `#444444` (dark gray, not harsh black)
- **Links**: `#444444` with `1px solid` underline
- **Link hover**: Remove underline only
- **Code background**: `white`

### 4. Security-First Requirements
- **Zero JavaScript** - Completely script-free
- **No external dependencies** - Self-contained
- **Content Security Policy**: `script-src 'none'`
- **Security headers**: X-Frame-Options DENY, X-Content-Type-Options nosniff
- **HTTPS only** (when deployed)

### 5. Content Structure
- **Links in lists**: `<strong><a href="#">Project Name</a></strong> – Description`
- **Status indicators**: Use `<em>(Work in Progress)</em>` or `<em>(Coming Soon)</em>`
- **Quotes**: Use `<blockquote>` with `<em>` attribution
- **Code**: Inline `<code>` with white background, blocks with `<pre><code>`

### 6. Navigation
- **No navigation bars** - Keep it brutally simple
- **Breadcrumb style**: `<a href="../">← Back</a> | <a href="next.html">Next →</a>`
- **Project links**: Direct in-content linking with clear descriptions

### 7. Performance Requirements
- **Total CSS**: Under 1KB
- **Page size**: Under 10KB including HTML
- **No images** unless absolutely necessary
- **No animations or transitions**
- **Instant loading** on any connection

### 8. Responsive Design
```css
@media (max-width: 768px) {
    body {
        margin: 5%;
        max-width: 95%;
    }
}
```

### 9. Accessibility
- **Semantic HTML** for screen readers
- **Proper heading hierarchy**
- **High contrast** text
- **No motion** (respects prefers-reduced-motion)
- **Keyboard navigable**

### 10. File Organization
```
/
├── index.html          # Homepage
├── styles.css          # Single CSS file (<1KB)
├── .htaccess          # Security headers
├── robots.txt         # SEO
├── .well-known/
│   └── security.txt   # Security contact
└── projects/
    ├── project1.html
    └── project2.html
```

## What NOT to Include
- ❌ JavaScript frameworks
- ❌ CSS frameworks
- ❌ Image sliders/carousels
- ❌ Social media widgets
- ❌ Analytics tracking
- ❌ External fonts
- ❌ Animations
- ❌ Gradients or drop shadows
- ❌ Complex layouts or grids
- ❌ Navigation menus

## Content Guidelines
- **Professional tone** - No profanity in production
- **Technical accuracy** - Cybersecurity focused
- **Concise descriptions** - One line per project
- **Clear status indicators** - Work in Progress, Coming Soon, etc.
- **Lowercase branding** - "security-studies.net" for retro/tech vibe

## Inspiration
Based on the principles of:
- [motherfuckingwebsite.com](http://motherfuckingwebsite.com)
- [bettermotherfuckingwebsite.com](http://bettermotherfuckingwebsite.com)
- [evenbettermotherfucking.website](http://evenbettermotherfucking.website)

Adapted for those who value substance over style.

---

**Remember**: Every design decision should ask "Does this make the site faster, more secure, or more readable?" If not, don't add it. 