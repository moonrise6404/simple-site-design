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

### 4. Image Standards
When images are absolutely necessary:

#### File Organization
```
/images/
├── project-name/
│   ├── descriptive-filename.png
│   └── another-image.png
└── shared/
    └── diagrams.png
```

#### HTML Structure
```html
<figure>
    <img src="../images/project-name/descriptive-filename.png" 
         alt="Detailed description of what the image shows">
    <figcaption>Brief caption explaining the image context</figcaption>
</figure>
```

#### CSS Styling
```css
figure {
    margin: 2em 0;
    text-align: center;
}

figure img {
    max-width: 100%;
    height: auto;
    border-radius: 8px;
    box-shadow: 0 4px 8px rgba(0,0,0,0.1);
    display: block;
    margin: 0 auto;
}

figcaption {
    margin-top: 0.5em;
    font-style: italic;
    color: #666;
    font-size: 0.9em;
}
```

#### Image Guidelines
- **Use sparingly**: Only when they add genuine value
- **Semantic filenames**: `cloudwatch-alarms.png` not `image14.png`
- **Proper alt text**: Describe what the image shows, not "screenshot of..."
- **Responsive**: Always use `max-width: 100%`
- **Organized folders**: Group by project in `/images/project-name/`

### 5. Security-First Requirements
- **Zero JavaScript** - Completely script-free
- **No external dependencies** - Self-contained
- **Content Security Policy**: `script-src 'none'`
- **Security headers**: X-Frame-Options DENY, X-Content-Type-Options nosniff
- **HTTPS only** (when deployed)

### 6. Content Structure
- **Links in lists**: `<strong><a href="#">Project Name</a></strong> – Description`
- **Status indicators**: Use `<em>(Work in Progress)</em>` or `<em>(Coming Soon)</em>`
- **Quotes**: Use `<blockquote>` with `<em>` attribution
- **Code**: Inline `<code>` with white background, blocks with `<pre><code>`

### 7. Navigation
- **No navigation bars** - Keep it brutally simple
- **Breadcrumb style**: `<a href="../">← Back</a> | <a href="next.html">Next →</a>`
- **Project links**: Direct in-content linking with clear descriptions

### 8. Performance Requirements
- **Total CSS**: Under 1KB
- **Page size**: Under 10KB including HTML (excluding essential images)
- **Images**: Optimized, only when necessary
- **No animations or transitions**
- **Instant loading** on any connection

### 9. Responsive Design
```css
@media (max-width: 768px) {
    body {
        margin: 5%;
        max-width: 95%;
    }
}
```

### 10. Accessibility
- **Semantic HTML** for screen readers
- **Proper heading hierarchy**
- **High contrast** text
- **No motion** (respects prefers-reduced-motion)
- **Keyboard navigable**
- **Descriptive alt text** for all images

### 11. File Organization
```
/
├── index.html          # Homepage
├── styles.css          # Single CSS file (<1KB)
├── .htaccess          # Security headers
├── robots.txt         # SEO
├── .well-known/
│   └── security.txt   # Security contact
├── images/
│   ├── project-name/
│   └── shared/
└── pages/             # Renamed from projects/
    ├── project1.html
    └── project2.html
```

## HTML Template
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Page description here">
    <title>Page Title - yourdomain.com</title>
    <link rel="stylesheet" href="../styles.css">
</head>
<body>
    <h1>Page Title</h1>
    <p><strong>Brief description</strong></p>
    <p><em>Technologies used • Status</em></p>

    <h2>Section Header</h2>
    <p>Content here...</p>

    <!-- Image when necessary -->
    <figure>
        <img src="../images/project/filename.png" alt="Description">
        <figcaption>Image caption</figcaption>
    </figure>

    <hr>
    <p><a href="../index.html">← Back to Projects</a></p>
</body>
</html>
```

## CSS Template
```css
body {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
    line-height: 1.8;
    margin: 5% auto;
    max-width: 73%;
    color: #444;
    background-color: #f2f2f2;
    font-size: 16px;
    text-shadow: 0 1px 0 #ffffff;
}

a {
    color: #444;
    text-decoration: underline solid 1px;
}

a:hover {
    text-decoration: none;
}

code {
    background-color: white;
    padding: 2px 4px;
}

figure {
    margin: 2em 0;
    text-align: center;
}

figure img {
    max-width: 100%;
    height: auto;
    border-radius: 8px;
    box-shadow: 0 4px 8px rgba(0,0,0,0.1);
    display: block;
    margin: 0 auto;
}

figcaption {
    margin-top: 0.5em;
    font-style: italic;
    color: #666;
    font-size: 0.9em;
}

@media (max-width: 768px) {
    body {
        margin: 5%;
        max-width: 95%;
    }
}
```

## What NOT to Include
- ❌ JavaScript frameworks
- ❌ CSS frameworks
- ❌ Image sliders/carousels
- ❌ Social media widgets
- ❌ External fonts
- ❌ Animations
- ❌ Gradients or drop shadows
- ❌ Complex layouts or grids
- ❌ Navigation menus

## Content Guidelines
- **Professional tone** - Clean, technical language
- **Technical accuracy** - Cybersecurity focused
- **Concise descriptions** - One line per project
- **Clear status indicators** - Work in Progress, Coming Soon, etc.
- **Lowercase branding** - "security-studies.net" for retro/tech vibe
- **Descriptive filenames** - No generic names like "image1.png"


## Inspiration
Based on the principles of:
- [motherfuckingwebsite.com](http://motherfuckingwebsite.com)
- [bettermotherfuckingwebsite.com](http://bettermotherfuckingwebsite.com)
- [evenbettermotherfucking.website](http://evenbettermotherfucking.website)
