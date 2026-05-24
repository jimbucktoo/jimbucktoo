# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Personal portfolio website for Jimmy Liang (jimbucktoo.com), hosted on Firebase Hosting. It is a static single-page site with no build process.

## Development Commands

```bash
firebase serve      # Local development server
firebase deploy     # Deploy to Firebase Hosting (requires firebase-tools)
```

## Architecture

All site content lives in `public/`:
- `index.html` — the entire page (single HTML file; JS is inline in script tags)
- `style.css` — all custom styles, with responsive breakpoints at 600px, 900px, and 1200px
- `images/` — project screenshots and logos

Firebase configuration:
- `.firebaserc` — project ID (`jimbucktoo-7fed6`)
- `firebase.json` — points hosting to `public/`
- `database.rules.json` — all Realtime Database read/write disabled

## Key Technologies

All external libraries are loaded via CDN (no npm, no bundler):
- **Materialize CSS v1.0.0** — Material Design components and parallax scrolling
- **jQuery v2.2.4** — DOM manipulation
- **ScrollReveal** — scroll-based reveal animations
- **Firebase JS SDK v5.0.4** — initialized but used minimally
- **Google Analytics** — UA-171797864-1
