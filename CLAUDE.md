# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Development Commands

| Command | Description |
|---------|-------------|
| `npm install` | Install all dependencies (including sass-embedded) |
| `npm run dev` | Start development server at `localhost:4321` |
| `npm run build` | Build production site to `./dist/` |
| `npm run preview` | Preview production build locally |
| `npm run astro` | Run Astro CLI commands |

## Dependencies

- **sass-embedded**: Required for SCSS compilation. Install with `npm install -D sass-embedded`

## Project Architecture

This is an Astro-based static site generator project with a glassmorphism design theme.

### Key Architecture Components

- **Framework**: Astro 5.10.2 with TypeScript strict configuration
- **Build System**: Astro's built-in Vite-based build system
- **Styling**: SCSS with modular design system focused on glassmorphism effects
- **Project Structure**: Standard Astro layout with pages, components, layouts, and styles directories

### Design System Structure

The project implements a comprehensive glassmorphism design system:

**Variables** (`src/styles/_variables.scss`):
- Color palette: white, soft-snow, powder-blue, sunset-orange
- Typography: Inter Tight (primary), Bebas Neue (display)
- Spacing scale: xs (0.5rem) to xxl (4rem)
- Border radius: sm (8px) to xl (24px)
- Responsive breakpoints: mobile (480px) to wide (1280px)

**Glassmorphism System** (`src/styles/_glassmorphism.scss`):
- Mixins for different glass opacity levels (light, medium, dark)
- Accent variations for blue and orange themes
- Pre-built components: `.glass-card`, `.glass-button`, `.glass-nav`, `.glass-hero-text`
- Consistent backdrop blur, borders, and shadow effects
- Hover and active state transitions

### Development Notes

- Uses Astro's file-based routing in `src/pages/`
- TypeScript configuration extends Astro's strict tsconfig
- Static assets go in `public/` directory
- Components can be placed in `src/components/` (currently empty but structured for future use)
- Layouts directory exists for shared page templates

