# Digital Sorcery - Project Walkthrough

## Overview
The **Digital Sorcery** website is now fully implemented with the **Technomancer's Grimoire** theme.

### Tech Stack
- **Framework:** SvelteKit 2
- **Library:** Svelte 5 (Runes enabled)
- **Styling:** Tailwind CSS 4 (Alpha/Beta)
- **Language:** TypeScript

## Site Structure

### Pages
1.  **Home (`/`)**:
    - Hero section with "Summon Us" CTA.
    - "The Technomancers" about section.
    - Featured services preview.
2.  **Services (`/services`)**:
    - Detailed grid of offerings (Platform Engineering, Automation, Cloud, Security, Observability, Legacy Transmutation).
    - Tech stack tags for each service.
3.  **Contact (`/contact`)**:
    - Functional-looking contact form.
    - Contact information and social placeholders.

### Components (`src/lib/components`)
- **`Button.svelte`**: Primary (Mana), Secondary (Arcane), and Ghost variants.
- **`Card.svelte`**: Glassmorphic container with hover glow effects.
- **`Section.svelte`**: Standard layout wrapper with consistent padding.
- **`Input.svelte`**: Floating label inputs for forms.
- **`Header.svelte`**: Responsive navigation bar.
- **`Footer.svelte`**: Site footer.

## Theme Details
- **Colors**: Void (`#050505`), Mana (`#00f3ff`), Arcane (`#9d00ff`), Gold (`#ffd700`).
- **Fonts**: `Cinzel` (Headers), `JetBrains Mono` (Body).
- **Effects**: Glow animations, glassmorphism, gradient text.

## How to Run
1.  **Install Dependencies** (if not already done):
    ```bash
    npm install
    ```
2.  **Start Dev Server**:
    ```bash
    npm run dev
    ```
3.  **Build for Production**:
    ```bash
    npm run build
    ```
