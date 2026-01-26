# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Personal portfolio website for Garrett Wong. Static HTML/CSS/JS site hosted on GitHub Pages at garrettwong99.github.io.

## Development

**Running locally:**
```bash
python -m http.server 8000
# or
npx http-server
```

**Deployment:** Automatic via GitHub Pages when pushing to `main` branch. No build step required.

## Architecture

- **Pure static site** - No build system, bundler, or package manager
- **Bootstrap 4.5.2** - Loaded via CDN for responsive grid and components
- **jQuery/Popper.js** - Loaded via CDN for Bootstrap modal functionality

### Page Structure

| File | Purpose |
|------|---------|
| `index.html` | Homepage with about section and contact links |
| `projects.html` | Project portfolio with modal details (JS-generated cards) |
| `certifications.html` | Courses and certifications |
| `styles.css` | Centralized styling with brown/tan/olive color scheme |

### Key Implementation Details

- **Project cards** in `projects.html` are dynamically generated via inline JavaScript using a `projects` array
- **Navigation** is duplicated across HTML files (not templated)
- **Assets** live in `assets/` with project images organized in `assets/project_imgs/`
