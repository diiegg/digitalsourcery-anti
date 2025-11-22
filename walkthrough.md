# Digital Sorcery - Project Walkthrough

## Overview
The **Digital Sorcery** website has been transmuted to the **Solarpunk Alchemist** theme.

### Tech Stack
- **Framework:** SvelteKit 2
- **Library:** Svelte 5 (Runes enabled)
- **Styling:** Tailwind CSS 4 (Alpha/Beta)
- **Language:** TypeScript

## Theme Details: Solarpunk Alchemist
A bright, ethereal aesthetic blending ancient wisdom with utopian technology.

### Color Palette
| Name | Hex | Usage |
|------|-----|-------|
| `sandstone` | `#FDF6E3` | Background (Parchment/Warm White) |
| `emerald` | `#10B981` | Nature/Growth (Primary Accent) |
| `energy` | `#EA580C` | Burnt Orange (Secondary Accent) |
| `silver` | `#94A3B8` | Holographic/Metallic (Neutral) |
| `text` | `#1F2937` | Dark Grey (Readability) |

### Typography
- **Headers:** `Syne` (Modern Geometric, Art Nouveau inspired)
- **Body:** `Space Grotesk` (Clean, Technical)
- **Accents:** `Pinyon Script` (Ancient Wisdom)

### Visual Language
- **Glassmorphism:** Frosted white glass with soft blurs.
- **Geometry:** Floating circles, squares, and sacred geometry patterns.
- **Motion:** Gentle floating animations (`animate-float`) and soft transitions.

## Site Structure
1.  **Home (`/`)**:
    - Hero with floating geometric elements.
    - "The Alchemists" about section with glassmorphic cards.
    - "Elemental Arts" services preview.
2.  **Services (`/services`)**:
    - Detailed "Grimoire" of offerings using nature/elemental metaphors.
    - Tech stack tags in emerald green.
3.  **Contact (`/contact`)**:
    - "Summon Us" form with floating label inputs.
    - Contact info with hover effects.

## How to Run
1.  **Install Dependencies**:
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
