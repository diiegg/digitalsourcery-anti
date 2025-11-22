# Digital Sorcery - Walkthrough

## Overview
Digital Sorcery is a platform engineering and automation consulting website built with SvelteKit 2, Svelte 5, and Tailwind CSS 4. The design is inspired by an alchemical observatory in 10th–11th century al-Andalus.

## Features
- **Svelte 5 (Runes)**: Uses the latest Svelte reactivity model.
- **Tailwind CSS 4**: Configured with the "Andalus" color palette and design tokens.
- **Netlify Adapter**: Ready for deployment to Netlify.
- **Responsive Design**: Fully responsive layout with mobile navigation.

## Project Structure
- `src/lib/components`: Reusable UI components.
  - `AndalusShell.svelte`: Global layout with navigation and footer.
  - `WorkshopSection.svelte`: Section wrapper with theme variants.
  - `ArchCard.svelte`: Card component with arch design.
  - `WorkshopHero.svelte`: Home page hero with celestial animation.
  - `GrimoireTimeline.svelte`: Process visualization.
  - `SummonForm.svelte`: Contact form with Netlify Forms support.
- `src/routes`: Page routes.
  - `+layout.svelte`: Root layout importing `AndalusShell`.
  - `app.css`: Global styles and Tailwind configuration.

## How to Run
### Development
```bash
npm run dev
```
Open [http://localhost:5173](http://localhost:5173) to view the site.

### Build
```bash
npm run build
```
This generates the production build using the Netlify adapter.

## Design System
The design system is defined in `src/app.css` using CSS variables within the `@theme` directive of Tailwind CSS 4.
- **Colors**: `andalus-night`, `courtyard-plaster`, `caliphate-gold`, `mezquita-red`, etc.
- **Fonts**: Inter (sans-serif) used for both display and body.

## Verification
The project has been successfully built using `npm run build`.
- **Responsive Check**: The layout uses standard Tailwind breakpoints (`md`, `lg`) to ensure responsiveness.
- **Netlify Check**: The adapter is configured in `svelte.config.js`.
