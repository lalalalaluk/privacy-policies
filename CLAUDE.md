# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static HTML/CSS website that serves as a central hub for managing privacy policies across multiple mobile applications. It is designed to be deployed on GitHub Pages without any build process or framework dependencies.

## Architecture

### Site Structure
- **index.html**: Landing page with a card-based grid layout displaying all apps. Each card links to its corresponding privacy policy page.
- **app[N]-privacy.html**: Individual privacy policy pages for each app. Use `app1-privacy.html` as the template.
- **style.css**: Single shared stylesheet for all pages with responsive design and gradient theme (purple by default).

### Page Layout Pattern
All pages share the same structure:
1. Standard HTML5 boilerplate with `lang="zh-TW"` for Traditional Chinese
2. Link to `style.css` in the `<head>`
3. Container div with specific class-based sections
4. Footer with copyright information

## Adding New Apps

When adding a new app's privacy policy:

1. **Copy the template**: Duplicate `app1-privacy.html` to `appN-privacy.html`
2. **Update the new privacy page**:
   - `<title>` tag
   - `<h1>` with app name
   - Privacy policy content sections
   - Contact information in section 10
   - Last updated date in `<time>` tag
   - Footer copyright

3. **Add card to index.html**: Insert within `<main class="app-grid">`:
```html
<div class="app-card">
    <div class="app-icon">[emoji]</div>
    <h2 class="app-name">[App Name]</h2>
    <p class="app-description">[Description]</p>
    <a href="appN-privacy.html" class="btn-primary">查看隱私權政策</a>
</div>
```

## Deployment

This is a pure static site with no build step:

```bash
# Deploy changes
git add .
git commit -m "Update privacy policy for [App Name]"
git push
```

GitHub Pages serves from the `main` branch root directory. Changes are live within 1-2 minutes after push.

## Styling Conventions

- Purple gradient theme: `#667eea` to `#764ba2`
- Responsive breakpoints: 768px (tablet), 480px (mobile)
- Card-based layout with hover animations
- All pages use identical CSS classes from `style.css`
- Emoji icons for visual app identification

## URL Structure

- Homepage: `/` or `/index.html`
- App privacy pages: `/app[N]-privacy.html`
- All pages are at root level (no subdirectories)
