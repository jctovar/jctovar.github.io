# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a personal portfolio website for Juan Carlos Tovar Gómez. It's a static GitHub Pages site built with vanilla HTML, CSS, and JavaScript—no build tools, frameworks, or package managers.

## Project Structure

- **index.html** - Single-page portfolio with all content, styling, and functionality
- **jctovar.png** - Profile image (external resource also available via HTTPS)
- **README.md** - Repository description

## Key Architecture

The portfolio is a single-document application with:

1. **CSS Variables** (`--primary-color`, `--secondary-color`, `--accent-color`, etc.) - Centralized color theme management
2. **Responsive Grid Layouts** - Uses CSS Grid for profile section, skills cards, contact cards, and timelines
3. **Scroll-based Animations** - JavaScript detects when sections enter viewport and applies `.active` class for fade-in effects
4. **Parallax Hero Section** - Background image in hero scrolls at 0.5× the scroll speed
5. **Smooth Navigation** - Links in nav bar smoothly scroll to section IDs
6. **Mobile-first Responsive Design** - Media query at 768px handles tablet/phone layouts

## Styling Approach

- **Medieval/Professional Theme** - Gold accents (`#c9a961`), dark blues, serif fonts (Georgia, Palatino)
- **Decorative Elements** - Animated patterns, gradient borders, unicode symbols (❖, ✉)
- **Animations** - CSS keyframes for fade-in/out, and scroll-triggered reveal animations
- **Grid System** - Flexible responsive grids using `grid-template-columns: repeat(auto-fit, minmax(...))`

## Making Changes

When editing the portfolio:

- **Color Changes** - Update CSS custom properties in `:root` selector (lines 12-21)
- **Content Updates** - Edit text in corresponding section elements (e.g., skills in `.skill-card` divs)
- **Adding Sections** - Create new `<section id="...">` element with `.reveal` class to get scroll animations automatically
- **Profile Image** - Currently hosted externally; replace `src="https://jctovar.github.io/jctovar.png"` with local path if needed
- **Navigation Links** - Add new `<li><a href="#section-id">Label</a></li>` in nav, ensure matching section ID
- **Responsive Behavior** - Test changes at 768px breakpoint; adjust media query values if needed

## Deployment

This site is hosted on GitHub Pages. Any changes to `index.html` on the main branch are automatically published to https://jctovar.github.io.

No build process, no linting, no testing framework—changes are live immediately upon commit.
