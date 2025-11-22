# Digital Sorcery - Implementation Plan

## Goal Description
Build "Digital Sorcery", a platform engineering and automation consulting services website. The site will use SvelteKit 2, Svelte 5, and Tailwind CSS 4, featuring a unique "Alchemical Observatory in 10th–11th century al-Andalus" theme.

## User Review Required
> [!IMPORTANT]
> Confirming usage of Svelte 5 (Runes) and Tailwind CSS 4 (Alpha/Beta). These are cutting-edge versions.

## Proposed Changes

### Project Setup
#### [NEW] [digital-sorcery](file:///Users/diegoquiroga/.gemini/antigravity/scratch/digital-sorcery)
- Initialize SvelteKit project with `npm create svelte@latest`.
- Select Svelte 5 preview if available or install `@sveltejs/kit` and `svelte@next`.
- Install `tailwindcss` (v4) and `@tailwindcss/vite`.

### Design System
#### [NEW] [app.css](file:///Users/diegoquiroga/.gemini/antigravity/scratch/digital-sorcery/src/app.css)
- Define CSS variables for the Andalus palette.
- Configure Tailwind theme to use these variables.

### Components
#### [NEW] [AndalusShell.svelte](file:///Users/diegoquiroga/.gemini/antigravity/scratch/digital-sorcery/src/lib/components/AndalusShell.svelte)
- Global layout component with navigation and footer.

#### [NEW] [WorkshopSection.svelte](file:///Users/diegoquiroga/.gemini/antigravity/scratch/digital-sorcery/src/lib/components/WorkshopSection.svelte)
- Section wrapper with tone variants.

#### [NEW] [ArchCard.svelte](file:///Users/diegoquiroga/.gemini/antigravity/scratch/digital-sorcery/src/lib/components/ArchCard.svelte)
- Reusable card component with arch styling.

### Pages
#### [NEW] [+page.svelte](file:///Users/diegoquiroga/.gemini/antigravity/scratch/digital-sorcery/src/routes/+page.svelte)
- Home page implementation.

#### [NEW] [services/+page.svelte](file:///Users/diegoquiroga/.gemini/antigravity/scratch/digital-sorcery/src/routes/services/+page.svelte)
- Services page.

## Verification Plan
### Automated Tests
- Run `npm run build` to verify SvelteKit build.
- Run `npm run dev` and check console for errors.

### Manual Verification
- Visually inspect the "Andalus" theme elements (colors, fonts, spacing).
- Verify navigation between all pages.
- Check responsiveness on mobile and desktop.
