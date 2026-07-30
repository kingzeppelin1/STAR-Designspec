---
name: star-explorer-design
description: Use this skill to generate well-branded interfaces and assets for STAR Explorer, either for production or throwaway prototypes/mocks/etc. Contains essential design guidelines, colors, type, fonts, assets, and UI kit components for prototyping.
user-invocable: true
---

Read the README.md file within this skill, and explore the other available files.

If creating visual artifacts (slides, mocks, throwaway prototypes, etc), copy assets out and create static HTML files for the user to view. If working on production code, you can copy assets and read the rules here to become an expert in designing with this brand.

If the user invokes this skill without any other guidance, ask them what they want to build or design, ask some questions, and act as an expert designer who outputs HTML artifacts _or_ production code, depending on the need.

## Quick reference

- **Tokens**: `colors_and_type.css` — import this file and you have the entire system (colors, type, spacing, radii, shadows, motion).
- **Logos**: `assets/logo-*.png` — horizontal + brandmark, in blue and white.
- **Fonts**: `fonts/TitilliumWeb-*.ttf` — self-hosted, referenced by `colors_and_type.css`.
- **Specimens**: `preview/*.html` — small visual cards demonstrating each token group; useful as direct copy-paste references.

## Brand pillars (don't forget)

1. **Calm surfaces.** ~85% of any view is warm-white / beige / light grey. Saturated color is rare and intentional.
2. **Color = role.** Aqua only for collaborate. Brown only for constant/archival. Yellow only for curious/exploratory. Green only for in-flight progress (NOT generic success). Marine for "official STAR". Pink for relational. Status colors only for system feedback.
3. **One family.** Titillium Web for everything. Display uses ExtraLight (200), body Regular (400), emphasis SemiBold (600).
4. **No decoration.** No emoji, no gradients in product UI, no hand-drawn illustration, no patterns/textures, no bouncy motion. Borders do structural work, not shadows.

