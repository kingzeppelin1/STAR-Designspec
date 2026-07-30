# STAR Explorer — Design System

A minimalist, light-toned design system for STAR Explorer. Three pillars: **calm surfaces** (off-white, light grey, warm beige), **purposeful color** (each accent encodes one specific UI meaning), and **a single type family** — Titillium Web for everything from wordmark to caption.

> "We use a minimalist and light color palette with different shades of white, beige and light grey. The colors are used purposefully and each color signals something specific throughout all our UIs, to lead the user to the UI element they are looking for."

---

## Brand context

STAR Explorer's visual identity is anchored in a navy shield-mark (the "S" brandmark, "Genuine Marine" #103451). The system pairs that serious, official-feeling primary navy with a quietly warm neutral palette and a small set of meaning-bearing accents. Saturated color appears deliberately, not decoratively — it always *means something*.

Every color is a **9-step scale** (50, 100, 200, 300, 400, 500, 600, 700, 800, 900). On **light** backgrounds, the main step of each color is **600**. On **dark** backgrounds, the main step is **300**. Use 50–100 for tints (banner backgrounds, chips), 200–400 for borders and graphics, 600 for primary fills on light surfaces, 700–900 for text and emphasis.

| Color                              | Role                                              | Main on light |
|------------------------------------|---------------------------------------------------|---------------|
| **Genuine Marine** (Primary)       | Official STAR — primary actions, headers, logo    | `#103451` (600) |
| **Commitment Pink** (Secondary)    | Relational moments — testimonials, "we're with you" | `#C86254` (600) |
| **Constant Brown** (Accent)        | Stable / unchanging / archival                    | `#825642` (600) |
| **Collaborate Aqua** (Aid)         | Shared / multi-user / collaborative elements      | `#319BA2` (600) |
| **Curious Yellow** (Discovery)     | Exploratory / educational                         | `#C59A0A` (600) |
| **Progress Green** (Create)        | In-flight progress / growth (≠ Success)           | `#31A373` (600) |
| **Danger / Success / Warning**     | System feedback only                              | — |

Numerical aliases match the Figma source ("primary-600", "marine-300", etc.) so designers and engineers stay in sync.

---

## Sources

- **Figma**: STAR Explorer OG Design System (read 2026-04-28). Pages explored: Colors (light + dark + scheme + WCAG examples), Light scale, Dark scale.
- **Uploaded brand assets**: 4 logo PNGs (brandmark + horizontal lockup, blue + white), 9 color swatch PNGs, 10 Titillium Web TTFs, status color swatches.
- **No codebase, product Figma, or product screens** were attached — UI kits are intentionally not included until product context is provided. See "Caveats & next steps".

---

## Index

- [`colors_and_type.css`](./colors_and_type.css) — all color, type, spacing, radius, shadow, and motion tokens. Drop-in import.
- [`README.md`](./README.md) — this file.
- [`SKILL.md`](./SKILL.md) — Agent Skills entry point (works in Claude Code).
- [`assets/`](./assets/) — logos (brandmark + horizontal, blue + white).
- [`fonts/`](./fonts/) — Titillium Web TTFs.
- [`preview/`](./preview/) — design-system specimen cards rendered in the Design System tab.

---

## Content fundamentals

STAR Explorer's voice is **measured, grown-up, and quietly confident**. The brand reads as a service that takes itself seriously without being stiff — respectful of the reader's time.

**Tone & vibe**
- Calm, not loud. Declarative, not promotional.
- Plural-first ("We", "Your team") for relational moments; "you" for direct guidance.
- No exclamation points in product UI. Save the energy for the noun.
- No emoji. Use a colored dot, an icon, or a status chip instead.

**Casing**
- **Sentence case** everywhere — buttons, menus, tabs, headings. ("Save changes", not "Save Changes".)
- The word **STAR** is the exception: always all-caps when standalone. The brand pair is "STAR Explorer" — both words capitalized.
- Acronyms allowed: API, PDF, URL.

**Copy patterns**
- **Buttons**: verb-led, ≤3 words. *Save changes · Invite people · Continue*
- **Empty states**: one sentence of context + one CTA. *No projects yet. Start by importing a file.*
- **Errors**: name the problem in plain language, then offer a next step. *That email's already in use. Try signing in instead.*
- **Microcopy length**: caption text ≤80 chars; body paragraphs ≤2 sentences in product UI.

**What we don't do**
- No "Awesome!" / "Oops!" / hype words.
- No metaphor stretching ("Let's blast off!"). The brand is grounded.
- No corporate softeners ("Please kindly…").

---

## Visual foundations

**Color application**
- Surfaces: `--bg` (#FAFAFA off-white) and `--surface` (#F6F6F5), with `--neutral-200` (#E0DEDE) dividers. The page should feel like good paper.
- Each saturated color is **one role**. Aqua never appears as decoration — only when something is collaborative. Yellow never appears as a generic accent — only when something is exploratory.
- Tints (50–100) are used for soft fills (chip backgrounds, banners). Mids (300–500) for icons and graphics. Darks (700–900) for text on light surfaces.
- Ratio rule: ~85% neutral surfaces, ~10% Genuine Marine, ~5% one accent at a time. Never two saturated colors competing in the same view.

**Typography**
- **Titillium Web** is the single brand family. It carries everything — the wordmark, display headings, UI labels, body copy, captions.
- Headings use SemiBold (600) at 28 / 21 / 18; large display moments use Light (300) or Regular (400) at 47 / 33.
- Body sits at **14px / 1.55**, with Regular (400) for paragraph text and SemiBold (600) for emphasis.
- Italic is used sparingly — only for true citations or product names within prose.
- Both `--font-ui` and `--font-display` tokens resolve to Titillium Web; do not introduce other families.

**Spacing**
- 4-pt grid. Component padding usually lands on 8 / 12 / 16 / 24. Section spacing on 48 / 64 / 96.

**Backgrounds**
- Solid warm whites and beiges. **No gradients** in the product UI. **No repeating patterns or textures.** **No hand-drawn illustrations.** The brand is sober.
- Marketing surfaces *may* use a single full-bleed photographic image, treated cool/desaturated, with a Marine overlay at ~70% for legibility.
- Imagery vibe: **cool and slightly desaturated**, modest grain acceptable. Never warm-saturated, never highly stylized.

**Borders & dividers**
- Default border: 1px `--neutral-200` (#E0DEDE). Strong border: 1px `--neutral-300` (#C9C8C5).
- Borders do most of the structural work — *not* shadows.

**Shadows**
- Restrained. Three levels (`--shadow-1/2/3`), all soft, all using ink-tinted shadow color. Cards generally use `--shadow-1` or no shadow + a neutral border.
- No coloured shadows, no glow effects.

**Corner radii**
- Default: **8px** (`--radius-md`). Buttons, inputs, dense components.
- Small chips and tags: **4px** (`--radius-sm`).
- Large surface cards / modals: **12px** (`--radius-lg`) — this is the radius used by the swatch cards in the source Figma.
- Pills (status, filter chips): **999px**.

**Cards**
- Surface: `--paper` (white) or `--surface` (off-white), depending on whether the parent is `--bg` or already `--surface`.
- Border: 1px `--neutral-200`. Optional `--shadow-1` only when the card needs to "lift" off content (e.g. a popover).
- Corner: `--radius-lg` (12px).
- No filled headers — section breaks within a card are done with a hairline divider.

**Hover states**
- Surfaces (rows, list items): background goes to `--neutral-100`.
- Buttons: primary fills shift one step *darker* (Marine-600 → Marine-700); ghost buttons fill with `--marine-50`.
- Links: color goes to `--marine-700` and underline darkens.
- Icon-only buttons: 6% ink overlay.

**Press / active states**
- Surfaces darken one more step (`--neutral-100` → `--neutral-200`).
- Buttons shift fill one step darker (Marine-700 on press). No scale changes, no springs.

**Focus**
- Always visible. `--shadow-focus` (3px Marine-tinted ring at ~22% opacity). Replaces native outline.

**Animation**
- Purposeful, never decorative. Three durations: 120 / 200 / 320ms. Easing: standard `cubic-bezier(.2,0,.2,1)` for most things; emphasized `cubic-bezier(.2,0,0,1)` for entrances.
- Fades and small translations only. **No bounces, no springs, no parallax.**

**Transparency & blur**
- Used only for overlays (modals, sheets) and fixed nav. Modal scrim: `rgba(8,24,37,.40)`. A single 8px blur is acceptable on the modal scrim itself for marketing surfaces.

**Layout**
- Fixed top nav: 64px. Side nav: 240px (collapsed 64px).
- Max content width on marketing: 1200px. In-app: fluid with 24–32px page gutters.

**Protection / contrast**
- For text on imagery, prefer a **solid Marine-700 capsule** behind text (with `--radius-md`) rather than a gradient overlay. Capsules are honest; gradients hedge.

---

## Iconography

No icon set was supplied with the brand assets. The system standardises on **Lucide** as a substitute that matches STAR's aesthetic: 1.5px stroke, 24×24 grid, rounded line caps, outline-only (no fills). Lucide is CDN-available and stylistically aligned with a minimalist, light-tone UI.

> **Substitution flag:** Lucide is a *placeholder*. If STAR has a proprietary icon set, please share it and we'll swap. The CSS tokens and component code don't depend on Lucide specifically — only on a 24×24, 1.5px-stroke, outline icon vocabulary.

**CDN usage**
```html
<script src="https://unpkg.com/lucide@latest"></script>
<i data-lucide="search"></i>
<script>lucide.createIcons();</script>
```

**Rules**
- Default size 20px in dense UI, 24px in marketing.
- Color matches surrounding text by default. When an icon carries semantic meaning, color it with the corresponding role token (e.g. `--role-collaborate` for a "Shared" icon).
- Never fill an outline icon. Never mix outline and filled icon sets.
- **Emoji are not used** anywhere in product or marketing.
- **Unicode glyphs as icons** (★, →, ✓) are not used in product UI; use a real icon. They are acceptable in body copy.

**The brand mark itself** is the navy shield-with-S — only used as identity (top-left of the app, footer, splash). Never used inline as an icon or decoration.

---

## Caveats & next steps

**What's complete**
- Full color system with 9-step scales (50–900) for all 9 brand colors plus the neutral spine, sourced directly from the STAR Figma file.
- Single-family type system on Titillium Web (self-hosted from the supplied TTFs).
- Spacing, radius, shadow, and motion tokens.
- Brand asset library (logos) ready to use.
- Specimen cards in `preview/` for the Design System tab.

**What's missing — please help iterate**
1. **No product/codebase context** was supplied. To build pixel-perfect UI kits I need a connected codebase, a product Figma, or screenshots of core surfaces.
2. **Icon set is a substitution** (Lucide). If STAR has a proprietary icon set, share it and I'll swap.
3. **No imagery / illustration guidance** was supplied. The visual foundations section makes a recommendation (cool, slightly desaturated photography, no illustration) — confirm or redirect.
4. **No tone-of-voice document** was supplied. The Content Fundamentals section is a reasonable inference — confirm or redirect.

If you can share any of the above, I'll fill the gaps.

